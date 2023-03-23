# @heiwa4126/convert-imports-to-mjs (npm-convert-imports-to-mjs)

- [English](./README.md)
- [日本語](./README-ja.md)

A script that allows ES modules generated from TypeScript in TCS to work properly.

It refers to all ".js" files in the specified directory and performs the following:

- If the module reference of import/export is a relative path and has no extension, ".mjs" is added.
- Rename the file extension from ".js" to ".mjs".

## Installation

```bash
npm install -D @heiwa4126/convert-imports-to-mjs
```

## Usage

In the scripts field of the target project's package.json,

```json
"scripts" : {
    "build:esm" : "tsc -p tsconfig.esm.json && convert-imports-to-mjs ./dist/esm"
}
```

Use it like `npm run build:esm` .
