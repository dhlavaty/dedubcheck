# Dedubcheck

This tool check your monorepo for diferent versions of the same dependencies (by recursively looking for `package.json` file).

To ignore certain package, create `.dedubcheck.js` file in your root dir containing:

```javascript
module.exports = [['packages/web/package.json', 'lodash'], ['<path-to-package.json>', '<name-of-package>'], [...]];
```

To run this thing, just do:

```bash
$ dedubcheck
```

For some debug info:

```bash
$ dedubcheck --debug
```
