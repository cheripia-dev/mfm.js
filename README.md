# mfm.js
An MFM parser implementation with TypeScript.

[![Test](https://github.com/cheripia-dev/mfm.js/actions/workflows/test.yml/badge.svg)](https://github.com/cheripia-dev/mfm.js/actions/workflows/test.yml)

This is the Cheripia fork of [misskey-dev/mfm.js](https://github.com/misskey-dev/mfm.js).
The package name is `mfm-js`, but installing `mfm-js` from npm does not install this fork.

## Installation
Install this fork from GitHub, replacing `<commit-sha>` with the full commit SHA to pin:

```sh
npm install 'mfm-js@git+https://github.com/cheripia-dev/mfm.js.git#<commit-sha>'
```

## Usage
Please see [docs](./docs/index.md) for the detail.

TypeScript:
```ts
import * as mfm from 'mfm-js';

const inputText =
`<center>
Hello $[tada everynyan! 🎉]

I'm @ai, A bot of cherrypick!

https://github.com/syuilo/ai
</center>`;

// Generate an MFM tree from the full MFM text.
const mfmTree = mfm.parse(inputText);

// Generate an MFM tree from the simple MFM text.
const simpleMfmTree = mfm.parseSimple('I like the hot soup :soup:​');

// Reverse to an MFM text from the MFM tree.
const text = mfm.toString(mfmTree);

```

## Develop
### 1. Clone
```
git clone https://github.com/cheripia-dev/mfm.js.git
```

### 2. Install packages
```
cd mfm.js

# This repository uses pnpm as its package manager.
pnpm i
```

### 3. Build
```
pnpm run build
```

### Use the interactive CLI parser
full parser:
```
pnpm run parse
```

simple parser:
```
pnpm run parse-simple
```

## License
This software is released under the [MIT License](LICENSE).
