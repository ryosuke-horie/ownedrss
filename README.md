# OwnedRss

## 概要

自作のRSSリーダー。
完全個人用に実装する。Remix＋Cloudflareの技術スタック習得と自分用にカスタマイズしたRSSリーダーが欲しいので実装する。

## Typegen

`wrangler.toml`を修正する度に以下を実行する必要がある。:

```sh
npm run typegen
```

## Development

Run the Vite dev server:

```sh
npm run dev
```

To run Wrangler:

```sh
npm run build
npm run start
```

## Deployment

> [!WARNING]  
> Cloudflare は `wrangler.toml` をデプロイメント バインディングを構成するために使用しません。
> Cloudflareダッシュボードでデプロイメントバインディングを手動で構成する必要があります

最初に実稼働用にビルドし

```sh
npm run build
```

pegesへデプロイする。

```sh
npm run deploy
```

## スタック

TODO：ここにライブラリ等をまとめていく。

- Remix
- Cloudflare
  - D1
  - workers & pages
- dependabot
- Biome ... Linter&Formatter
- lefthook ... git hooks biomeの実行をgit hooksで実行するため [https://github.com/evilmartians/lefthook#install](lefthook)
- Github Actions ... CI/CD
