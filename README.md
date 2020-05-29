# Electron with rxdb
Specifically to recreate [this issue](https://github.com/pubkey/rxdb/issues/1886)
## Steps I took to make this repo:
1. I started with [this minimal electron boilerplate](https://github.com/pbarbiero/basic-electron-react-boilerplate)
2. Copied and pasted the main parts of `main.js` and `database.js` from the [electron example](https://github.com/pubkey/rxdb/tree/master/examples/electron) from the rxdb
3. Ran `yarn dev`
4. Recieved the following error:
    ```
    yarn run v1.17.3
$ webpack-dev-server --hot --host 0.0.0.0 --config=./webpack.dev.config.js
⚠ ｢wds｣: The `setup` option is deprecated and will be removed in v4. Please update your config to use `before`
ℹ ｢wds｣: Project is running at http://0.0.0.0:8080/
ℹ ｢wds｣: webpack output is served from /
ℹ ｢wds｣: Content not from webpack is served from /Users/joe307bad/Source/electron-with-rxdb/dist
Since version 8.4.0 the module 'express-pouchdb' is not longer delivered with RxDB.
You can install it with 'npm install express-pouchdb'
creating hero-collection..
start server
(node:16185) UnhandledPromiseRejectionWarning: TypeError: ExpressPouchDB is not a function
    at RxDatabaseBase.spawnServer [as server] (/Users/joe307bad/Source/electron-with-rxdb/node_modules/rxdb/dist/lib/plugins/server.js:163:18)
    at createDb (/Users/joe307bad/Source/electron-with-rxdb/main.js:80:12)
    at processTicksAndRejections (internal/process/task_queues.js:85:5)
    at async App.<anonymous> (/Users/joe307bad/Source/electron-with-rxdb/main.js:100:3)
(node:16185) UnhandledPromiseRejectionWarning: TypeError: ExpressPouchDB is not a function
    at RxDatabaseBase.spawnServer [as server] (/Users/joe307bad/Source/electron-with-rxdb/node_modules/rxdb/dist/lib/plugins/server.js:163:18)
    at createDb (/Users/joe307bad/Source/electron-with-rxdb/main.js:80:12)
    at processTicksAndRejections (internal/process/task_queues.js:85:5)
    at async App.<anonymous> (/Users/joe307bad/Source/electron-with-rxdb/main.js:100:3)
(node:16185) UnhandledPromiseRejectionWarning: Unhandled promise rejection. This error originated either by throwing inside of an async function without a catch block, or by rejecting a promise which was not handled with .catch(). (rejection id: 1)
(node:16185) UnhandledPromiseRejectionWarning: Unhandled promise rejection. This error originated either by throwing inside of an async function without a catch block, or by rejecting a promise which was not handled with .catch(). (rejection id: 1)
(node:16185) [DEP0018] DeprecationWarning: Unhandled promise rejections are deprecated. In the future, promise rejections that are not handled will terminate the Node.js process with a non-zero exit code.
(node:16185) [DEP0018] DeprecationWarning: Unhandled promise rejections are deprecated. In the future, promise rejections that are not handled will terminate the Node.js process with a non-zero exit code.
    ``` 