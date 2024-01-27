---
title: AstroにヘッドレスCMSのStrapi導入してみた
tags:
  - "Astro.js"
  - "strapi"
  - "HeadlessCMS"
private: false
updated_at: ""
id: null
organization_url_name: null
slide: false
ignorePublish: false
---

## はじめに

### この記事 is なに

先日お仕事でとあるサイトを作ることになりました（開発中なので色々と伏せるのですが）。そのサイトの色々な要件を鑑みて Headless CMS の Strapi と Astro.js を使用することになりまして、導入するまでの過程を記事にしてみました。

### なんで Astro.js と Strapi？

件のサイトですが、ざっくりと簡単に要件をまとめると

- 静的サイトである
- 管理者側でコンテンツ管理がしたい
- マークダウンは書かない

こんなところです。まじでざっくりしててすんません。
この要件で私の無い頭ふりしぼった結果選ばれたのがそう、Strapi と Astro.js でした。Strapi はパッと見の情報が多いかなと感じたのと、Astro は爆速と噂だったのと最近のメンテナンスがしっかり（早すぎるくらいに）継続的になされていたことがきっかけで採用候補にあがりました。使ってみたところ、良さそうだったので採用しました。

## やってみました

### Strapi のプロジェクト作成

まずは公式に書いてある通りにセットアップ

```console
npx create-strapi-app@latest my-project
npm run develop
```

そうすると`http://localhost:1337/admin`が新規タブで自動で開きます。（開かなかったら自分でアクセスしてくだせえ）
メールアドレスとパスワードを入力して自分のアカウントを作成すると次のような画面が開きます。
![スクリーンショット 2024-01-27 23.47.46.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2883302/ccf9313f-693c-bbb4-b63c-b39fb0324628.png)

そのあとは「Content-Type Builder」ってとこからスキーマを定義して、そのスキーマに基づく実際のデータを「Content Manager」からどんどん追加していってください。

なんか例えばの話でカテゴリという名前のスキーマを作ったんで画像だけでも置いておきますね。

![スクリーンショット 2024-01-27 23.54.31.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2883302/dd80d318-c494-f362-4538-c57882d47dbd.png)
「Content-Type Builder」と

![スクリーンショット 2024-01-27 23.54.36.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2883302/8b906237-6e8c-99b9-c847-cd006526bc48.png)
「Content Manager」

### Astro.js からデータを取得する

まずは公式に書いてある通りにセットアップと実際に開発サーバーを立ち上げてみるところからですね

```console
npm create astro@latest
npm run dev
```

## 感想戦
