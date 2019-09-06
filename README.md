# Reproduce Offline Mirror Errors for Scoped Packages on the Taobao Registry

You may have to manually remove the yarn local cache for `@types/prop-types` and `prop-types` to reproduce the error.

```bash
rm -rf ~/Library/Caches/Yarn/v4/npm-@types-prop-types-15.7.*
rm -rf ~/Library/Caches/Yarn/v4/npm-prop-types-15.7.*
```

After ensuring the cache does not exists, you can run

```bash
yarn --offline
```

to see the "cannot make request" error. Or run

```bash
yarn
```

to see the "integrity check failed" error (which happens randomly, depending on which package is to be fetched first I think).
 
Or you can execute `reproduce.sh` over and over again to see the caches and errors changing.
