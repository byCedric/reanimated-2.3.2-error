# reanimated 2.3.2 error

A demonstration of the react-native-reanimated issue [Package json main points to non existing file in 2.3.2](https://github.com/software-mansion/react-native-reanimated/issues/3026)

## Installation

```
$ yarn install
```

## Reproduction

```
$ node --print "require.resolve('react-native-reanimated')"
```

You should see the result:

```
node:internal/modules/cjs/loader:361
      throw err;
      ^

Error: Cannot find module '/Users/josh/apps/temp/reanimated-2.3.2-error/node_modules/react-native-reanimated/lib/Animated.js'. Please verify that the package.json has a valid "main" entry
    at tryPackage (node:internal/modules/cjs/loader:353:19)
    at Function.Module._findPath (node:internal/modules/cjs/loader:566:18)
    at Function.Module._resolveFilename (node:internal/modules/cjs/loader:919:27)
    at Function.resolve (node:internal/modules/cjs/helpers:108:19)
    at [eval]:1:9
    at Script.runInThisContext (node:vm:129:12)
    at Object.runInThisContext (node:vm:305:38)
    at node:internal/process/execution:75:19
    at [eval]-wrapper:6:22
    at evalScript (node:internal/process/execution:74:60) {
  code: 'MODULE_NOT_FOUND',
  path: '/Users/josh/apps/temp/reanimated-2.3.2-error/node_modules/react-native-reanimated/package.json',
  requestPath: 'react-native-reanimated'
}
```
