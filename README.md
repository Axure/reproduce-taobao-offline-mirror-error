#

You may have to manually remove the yarn local cache for `@types/prop-types` to reproduce the error.

```bash
rm -rf ~/Library/Caches/Yarn/v4/npm-@types-prop-types-15.7.*
```

After ensuring the cache does not exists, you can run

```bash
yarn --offline
```

to see the error.
 
