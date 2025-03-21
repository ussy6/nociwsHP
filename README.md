# NOCIWS - 学生宇宙開発サークルのウェブサイト

このプロジェクトは、学生宇宙開発サークル「NOCIWS」のウェブサイトです。Next.jsを使用して構築されており、サークルの活動内容、ロケット開発、探査機開発などの情報を発信するプラットフォームとなっています。

## 機能

- レスポンシブなデザイン（モバイル対応）
- お問い合わせフォーム
- Markdownで管理するブログ機能
- ユーザー認証（メンバー専用ページ）
- ロケット・探査機開発プロジェクトのページ

## 技術スタック

- [Next.js](https://nextjs.org/) - Reactフレームワーク
- [Tailwind CSS](https://tailwindcss.com/) - CSSフレームワーク
- [React Hook Form](https://react-hook-form.com/) - フォーム管理
- [NextAuth.js](https://next-auth.js.org/) - 認証機能
- [MDX](https://mdxjs.com/) - Markdownコンテンツ管理

## 始め方

### 前提条件

- Node.js 16.8.0以上
- npm または yarn

### インストール

```bash
# リポジトリをクローン
git clone https://github.com/yourusername/nociws.git
cd nociws

# 依存関係のインストール
npm install
# または
yarn install
```

### 開発サーバーの起動

```bash
npm run dev
# または
yarn dev
```

ブラウザで [http://localhost:3000](http://localhost:3000) を開くと、開発版のウェブサイトが表示されます。

### ビルドと本番環境での実行

```bash
# ビルド
npm run build
# または
yarn build

# 本番環境での実行
npm run start
# または
yarn start
```

## プロジェクト構造

```
nociws/
├── app/
│   ├── about/           # 団体について
│   ├── blog/            # ブログ
│   ├── contact/         # お問い合わせ
│   ├── rocket/          # ロケット開発
│   ├── spacecraft/      # 探査機開発
│   ├── dashboard/       # メンバー専用ダッシュボード
│   ├── api/             # APIルート
│   ├── layout.js        # ルートレイアウト
│   └── page.js          # トップページ
├── components/          # 共通コンポーネント
├── content/             # ブログコンテンツ
├── lib/                 # ユーティリティ関数
└── public/              # 静的ファイル
```

## ブログ記事の追加方法

新しいブログ記事を追加するには:

1. `content/blog/` ディレクトリに新しい `.mdx` ファイルを作成します
2. 以下のフロントマターを含める必要があります:

```yaml
---
title: '記事タイトル'
date: 'YYYY-MM-DD'
excerpt: '記事の概要'
coverImage: '/images/blog-image.jpg'
author:
  name: '著者名'
  role: '役職'
  avatar: '/images/author-avatar.jpg'
categories: ['カテゴリー1', 'カテゴリー2']
---

# ここからMarkdownの本文が始まります
```

## 環境変数の設定

本番環境では、以下の環境変数を `.env.local` ファイルまたはホスティング環境で設定してください:

```env
NEXTAUTH_URL=https://your-domain.com
NEXTAUTH_SECRET=your-secret-key
# その他の必要な環境変数
```

## ユーザー認証

現在の実装ではデモ用の簡易認証を使用しています。本番環境では以下のユーザー認証方法を実装することを推奨します:

- データベースを使用した認証
- OAuth/ソーシャルログイン（Google, Githubなど）
- JWT認証のカスタマイズ

## デプロイ

このプロジェクトは以下のプラットフォームに簡単にデプロイできます:

- [Vercel](https://vercel.com/) (推奨)
- [Netlify](https://www.netlify.com/)
- [AWS Amplify](https://aws.amazon.com/amplify/)

## ライセンス

このプロジェクトは [MIT License](LICENSE) の下で公開されています。

## お問い合わせ

質問や提案がある場合は、[お問い合わせフォーム](https://your-domain.com/contact)からご連絡ください。
