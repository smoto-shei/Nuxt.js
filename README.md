# 1. Nuxt.js を使ってテストアプリの構築、2. jest を使ってテスト環境を整える

## 概要

## Nuxt.jsとは
Vue.js のフレームワーク。Vue.jsで開発する際に大変なところを、やさしく包みこんでくれるフレームワークです。開発環境の構築や、ミドルウェアなどの仕組み、いい感じのディレクトリ構成や、SSR/静的化など、かゆいところをサポートしてくれるため、本当に大切な機能の開発に集中できます。

## Jest とは
Jestは、Facebook社がOSSとして開発を進めている、JavaScriptのユニットテストのためのツールです。

## ディレクトリ構造
```bash
.
├── README.md
└── jest_app
    ├── Dockerfile
    ├── README.md
    ├── README_DOCKER.md
    ├── assets
    ├── components
    ├── content
    ├── coverage
    ├── dist
    ├── jest.config.js
    ├── jsconfig.json
    ├── layouts
    ├── middleware
    ├── node_modules
    ├── nuxt.config.js
    ├── package-lock.json
    ├── package.json
    ├── pages
    ├── plugins
    ├── static
    ├── store
    ├── test
    └── tsconfig.json
```
- jest_appがサンプルアプリ

### 起動の手順
1. README_DOCKER.md を参考にイメージの作成、コンテナの作成を行う
    - テストもしたいのでコンテナの中で起動、停止を行う。

2. npm run dev でサーバーを立てる
    - 17秒ほどかかる。ローカル動くようであればローカルで動かしても良いと思う。

### テストの仕方
1. npm run test で testディレクトリ以下のspec.js ファイルがテストされる。


## Nuxt を使ってみての感想
- pages に vueファイルを配置するだけでルーティングなどを設定してくれるのはすごく楽だと感じた。他にも test などの設定がアプリ作成時点で完了しているので楽。ディレクトリ構造もわかりやすい。
- 既存のアプリをこちらに移動するのはめんどくさいがアリかもしれない。typescript も使えるようにしたのでそこは良い。

## Jest を使ってみての感想
- かなり楽。testコードを描けるようにならねば。

# 参考

## 全体
[NuxtJS公式](https://ja.nuxtjs.org/guide/installation/)<br>
[Jest公式](https://jestjs.io/ja/)<br>
[dockerでNuxt.jsを構築する(dockerfileは参考にしない方がいい)](https://qiita.com/reflet/items/e7c33f84ab43ab237ee4)<br>
[create-nuxt-appのススメ](https://qiita.com/cheez921/items/fdfd224099f686e3173d)<br>
[SSR,SPAどっちにするか](https://qiita.com/nishinoshake/items/f42e2f03663b00b5886d)<br>
[ESlint, Pritter](https://qiita.com/soarflat/items/06377f3b96964964a65d)<br>
[Jest]()
[Vuetify](https://vuetifyjs.com/ja/)<br>

## 実装
[Nuxtで.envを扱う](https://qiita.com/taichi0514/items/3939af222dee21a44413)