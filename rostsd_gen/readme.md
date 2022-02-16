# rostsd-gen

A node.js script that creates and updates the TypeScript interfaces.d.ts declaration file with type declarations for the generated interfaces (messages and services).

Run this script everytime new interfaces are generated, see script/generate_messages.js

# run

You can update the interfaces.d.ts types manually by running the generate_tsd.js script.

```bash
node node_modules/rclnodejs/scripts/generate_tsd.js
```

Or, if you need further control of where the interfaces are saved...

```js
const tsdGenerator = require('rclnodejs/rostsd_gen/index.js');

tsdGenerator.generateAll({
  outputTsdPath: path.join(__dirname, '../some-directory/interfaces.d.ts')
});
```
