# babel-vscode-source-map-woes

[![Greenkeeper badge](https://badges.greenkeeper.io/cdaringe/babel-vscode-source-map-woes.svg)](https://greenkeeper.io/)

- `npm|yarn install`
- `babel input.js --source-maps > out.js`
- `node --debug-brk out.js`
  - observe `sourceMaps: true` in the attach config
- Attach, and observe

If you look inside of `input.js`, you will see some cues for trying debugging
with a debugger statement, and using the built in VSCode red breakpoints.

I wager what you discover is:

- on entry, sourcemaps are not immediately loaded
- VSCode breakpoints are not honored
