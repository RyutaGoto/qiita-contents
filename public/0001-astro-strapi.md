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

### なんで Astro と Strapi？

件のサイトですが、簡単に要件をまとめると

- 静的サイトである
- 管理者側でコンテンツ管理がしたい
- マークダウンは書かない

こんなところです。要件と言えるか怪しいレベルでのざっくり加減ですね。
この要件で私の無い頭ふりしぼった結果選ばれたのがそう、Strapi と Astro でした。選定理由としては Strapi はパッと見の情報が多いかなと感じたのと、Astro は爆速と噂だったのと最近のメンテナンスがしっかり（早すぎるくらいに）継続的になされていたのと使ってみたいというのがありました。

## やってみました

### Astro のプロジェクト作る

まずは公式に書いてある通りにセットアップと実際に開発サーバーを立ち上げてみるところからですね

```console
npm create astro@latest
npm run dev
```

### Strapi のアカウント作成

### 両者を連携させる

## 感想戦
