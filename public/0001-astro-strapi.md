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

### Astro.js からデータを取得する

まずは公式に書いてある通りにセットアップと実際に開発サーバーを立ち上げてみるところからですね

```console
npm create astro@latest
npm run dev
```

## 感想戦
