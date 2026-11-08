# Creative Portfolio (Astro)

ダークネイビー × ブルーを基調にした、総合クリエイター向けポートフォリオのトップページ雛形です。

## 1. ローカルで確認

Node.js の LTS 版をインストール後、このフォルダで実行します。

```bash
npm install
npm run dev
```

表示された `http://localhost:4321` をブラウザで開きます。

## 2. 公開前に必ず変更する箇所

- `src/pages/index.astro`
  - `YOUR_EMAIL@example.com` を問い合わせ用メールアドレスに変更
  - フッターの `YOUR CREATOR NAME` を表示名に変更
  - 仮の作品タイトル・説明を実際の作品に差し替え
- `src/layouts/BaseLayout.astro`
  - ページタイトル・説明文を調整
- `astro.config.mjs`
  - `YOUR_GITHUB_USERNAME` をGitHubユーザー名に変更

## 3. GitHub Pages で無料公開

1. GitHubで新しいリポジトリを作成します。
2. `src/`、`public/`、`.github/`、`package.json`、`astro.config.mjs` などをリポジトリにアップロードします。
3. リポジトリの Settings → Pages → Build and deployment で、Source を **GitHub Actions** にします。
4. `main` ブランチへ push すると、ワークフローがビルドして公開します。

### リポジトリ名について

最も簡単なのはリポジトリ名を `YOUR_GITHUB_USERNAME.github.io` にする方法です。
この場合、`astro.config.mjs` の `base: "/"` のままで公開できます。

通常のリポジトリ名（例: `portfolio`）で公開する場合は、`base: "/portfolio"` に変更してください。

公開URLは通常、`https://YOUR_GITHUB_USERNAME.github.io/` または
`https://YOUR_GITHUB_USERNAME.github.io/portfolio/` になります。

## 4. 次に追加したいもの

- 実際の作品サムネイル・動画埋め込み
- 作品詳細ページ
- ABOUT の経歴・プロフィール
- SNSリンク
- OGP画像（SNS共有時のプレビュー）
- お問い合わせフォーム（外部サービス連携）

## 構成

```text
creative-portfolio/
├── .github/workflows/deploy.yml
├── public/
├── src/
│   ├── layouts/BaseLayout.astro
│   └── pages/index.astro
├── astro.config.mjs
├── package.json
└── README.md
```
