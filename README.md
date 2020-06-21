# 1. Nuxt.js を使ってテストアプリの構築、2. jest を使ってテスト環境を整える

## 概要

Nuxt.js を使ってアプリを構築する。また、コンポーネントの関数に対してユニットテストを行う(Jest を使用)。store のテストも行うため、firestore を作成し、そこにデータの追加、取得をできるようにし、store で管理する。
ついでに Veutify の使用感も確かめる。

- 動作の様子<br>
  ![todoの追加、削除(このデータはfirestoreで管理)](https://github.com/smoto-shei/Nuxt.js/blob/ReadmeImages/Nuxt_test.gif)

## Nuxt.js とは

Vue.js のフレームワーク。Vue.js で開発する際に大変なところを、やさしく包みこんでくれるフレームワークです。開発環境の構築や、ミドルウェアなどの仕組み、いい感じのディレクトリ構成や、SSR/静的化など、かゆいところをサポートしてくれるため、本当に大切な機能の開発に集中できます。

## Jest とは

Jest は、Facebook 社が OSS として開発を進めている、JavaScript のユニットテストのためのツールです。

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

- jest_app がサンプルアプリ

### 起動の手順

1. README_DOCKER.md を参考にイメージの作成、コンテナの作成を行う

   - テストもしたいのでコンテナの中で起動、停止を行う。

2. npm run dev でサーバーを立てる
   - 17 秒ほどかかる。ローカル動くようであればローカルで動かしても良いと思う。

### テストの仕方

1. npm run test で test ディレクトリ以下の spec.js ファイルがテストされる。

## Nuxt を使ってみての感想

- pages に vue ファイルを配置するだけでルーティングなどを設定してくれるのはすごく楽だと感じた。他にも test などの設定がアプリ作成時点で完了しているので楽。ディレクトリ構造もわかりやすい。
- 既存のアプリをこちらに移動するのはめんどくさいがアリかもしれない。typescript も使えるようにしたのでそこは良い。

## Jest を使ってみての感想

- かなり楽。test コードを描けるようにならねば。

# 参考

## 全体

[NuxtJS 公式](https://ja.nuxtjs.org/guide/installation/)<br>
[Jest 公式](https://jestjs.io/ja/)<br>
[docker で Nuxt.js を構築する(dockerfile は参考にしない方がいい)](https://qiita.com/reflet/items/e7c33f84ab43ab237ee4)<br>
[create-nuxt-app のススメ](https://qiita.com/cheez921/items/fdfd224099f686e3173d)<br>
[SSR,SPA どっちにするか](https://qiita.com/nishinoshake/items/f42e2f03663b00b5886d)<br>
[ESlint, Pritter](https://qiita.com/soarflat/items/06377f3b96964964a65d)<br>
[Jest]()
[Vuetify](https://vuetifyjs.com/ja/)<br>

## 実装

[Nuxt で.env を扱う](https://qiita.com/taichi0514/items/3939af222dee21a44413)
