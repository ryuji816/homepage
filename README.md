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

## .envファイルの設定方法
.envファイルは環境変数を管理することができる．これを用いることでtokenなど公開したくない情報を環境変数にしてスクリプトに渡すことができる．

### .envファイルの作成
.envファイルをプロジェクトのルートディレクトリに作成する．その際、.gitignoreに.envファイルを登録することでgitの管理対象から外す．

### 環境変数の設定
.envファイルに
```
KEY = VALUE
```
の形で書いていけば良い

### 現在の設定内容

- API_KEY : slack apiより作成したAppであるClient DataのBot User OAuth Access Token


## デプロイ手順

```shell
cd makehomepage
npm install
npm run generate
# https://github.com/kobe-pablo/kobe-pablo.github.io
# のリポジトリの.gitと.gitignore以外を削除してmakehomepage/dist内のファイルを全てkobe-pablo.github.ioにコピペ
# そしてkobe-pablo.github.ioをpushする
```
