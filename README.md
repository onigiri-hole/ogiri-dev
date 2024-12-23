# ogirin

## これは何

- 大喜利のお題を生成AIを使って、作成してくれるサービス「大喜林」


## 構成図

```mermaid

flowchart TB
  node_1["VM"]
  node_2["Supabase\nPostgres\nDatabase"]
  node_3["Vercel"]
  node_1 --"生成されたお題を投入"--> node_2
  node_2 --"お題を取得"--> node_3
  node_3 --"リクエストを送信"--> node_1
```

## 詳細

### VM


### Supabase
- Postgres　Databaseでお題を管理
- 認証機能は随時実装予定

### Vercel
- Nextjsで実装
- お題の残り件数が足りなくなった時点でAPIを呼び出し


This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

You can stop this project by pressing `Ctrl + C` in your terminal.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
