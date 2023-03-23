# @heiwa4126/convert-imports-to-mjs (npm-convert-imports-to-mjs)

- [English](./README.md)
- [日本語](./README-ja.md)

tcs で TypeScript から生成した ES のモジュールを動作するようにするスクリプト。

指定したディレクトリ以下の".js"ファイルをすべて参照して、

- import/export のモジュール参照が相対パスで、かつ拡張子がない場合、".mjs"を付加する。
- ファイルの拡張子を ".js" から ".mjs" にリネームする。

## インストール

```bash
npm install -D @heiwa4126/convert-imports-to-mjs
```

## 使い方

対象のプロジェクトの package.json の scripts フィールドで

```json
"scripts" : {
    "build:esm" : "tsc -p tsconfig.esm.json && convert-imports-to-mjs ./dist/esm"
}
```

のようにして `npm run build:esm` のように使う。
