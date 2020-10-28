# homepage
サークルのホームページ

## 概要
- Nuxt.jsのプロジェクトである．
- UIフレームワークはVuetifyを用いる．

## Nuxt導入の仕方
まずはNode.jsのダウンロードが必要．
- [Node.js公式/ダウンロード](https://nodejs.org/ja/download/)

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org)

## .envファイルの設定

.envファイルは環境変数を管理することができる．これを用いることでtokenなど公開したくない情報を環境変数にしてスクリプトに渡すことができる．Nuxtで用いるために必要な設定をまとめる．

### .envファイルの作成
.envファイルをプロジェクトのルートディレクトリに作成する．その際、.gitignoreに.envファイルを登録することでgitの管理対象から外す．

### dotenvのインストール
dotenv というモジュールは，.envファイルから環境変数を読み込むために用いる．

```
$ npm install dotenv
```

 ### nuxt.config.jsの設定
 ```
 require('dotenv').config()
const { 環境変数名 } = process.env
 ```
また，export defaultの中に
```
env: {
    環境変数名
}
```
と，modelesの項目に
```
modules: [
    '@nuxtjs/dotenv'
  ],
```
を追加する．

### scriptでの使用
ここまでの設定の上でscript内では
```
process.env.環境変数名
```
でそれぞれの環境変数に設定した値を用いることができる．