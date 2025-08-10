# React・Next.js 学習プロジェクト

このプロジェクトは、React・Next.jsの初学者向けの学習用プロジェクトです。[`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app)でブートストラップされたNext.js 15プロジェクトです。

## プロジェクト構成

```
.
├── public/                   # 静的ファイル（画像、アイコン等）
├── src/
│   └── app/                 # App Router ディレクトリ
│       ├── globals.css      # グローバルスタイル
│       ├── layout.tsx       # ルートレイアウト
│       └── page.tsx         # ホームページ
├── package.json             # 依存関係とスクリプト
├── next.config.ts           # Next.js設定
├── tsconfig.json           # TypeScript設定
├── eslint.config.mjs       # ESLint設定
└── postcss.config.mjs      # PostCSS設定（Tailwind用）
```

## 使用技術

- **Next.js 15**: React フレームワーク（App Router使用）
- **React 19**: ユーザーインターフェースライブラリ
- **TypeScript**: 型安全なJavaScript
- **Tailwind CSS v4**: ユーティリティファーストCSS フレームワーク
- **ESLint**: コード品質ツール

## コマンド説明

### 開発用コマンド

```bash
# 開発サーバーを起動（推奨）
npm run dev
```
- **用途**: 開発中に使用するコマンド
- **機能**: 
  - ホットリロード（ファイル変更時の自動更新）
  - Turbopackによる高速ビルド
  - 開発用エラー表示
- **URL**: http://localhost:3000

### 本番用コマンド

```bash
# 本番用にビルド
npm run build

# 本番サーバーを起動
npm start
```
- **`npm run build`**: 本番用の最適化されたアプリケーションを生成
- **`npm start`**: ビルド後のアプリケーションを本番モードで実行

### コード品質チェック

```bash
# ESLintでコードチェック
npm run lint
```
- **用途**: コードの品質とスタイルをチェック
- **機能**: 潜在的なエラーやベストプラクティスからの逸脱を検出

## 開発の始め方

### 1. 依存関係のインストール
```bash
npm install
```

### 2. 開発サーバーの起動
```bash
npm run dev
```

### 3. ブラウザでアクセス
http://localhost:3000 をブラウザで開いてください。

### 4. コードの編集を開始
- `src/app/page.tsx` を編集してホームページをカスタマイズ
- ファイルを保存すると自動的にブラウザが更新されます

## 学習リソース

### 公式ドキュメント
- [Next.js ドキュメント](https://nextjs.org/docs) - Next.jsの機能とAPI
- [React ドキュメント](https://react.dev) - Reactの基本概念
- [TypeScript ハンドブック](https://www.typescriptlang.org/docs/) - TypeScript学習

### チュートリアル
- [Learn Next.js](https://nextjs.org/learn) - インタラクティブなNext.jsチュートリアル
- [React チュートリアル](https://react.dev/learn) - React公式チュートリアル

### 開発のヒント
1. **App Router**: Next.js 13以降の新しいルーティングシステム
2. **Server Components**: デフォルトでサーバーサイドレンダリング
3. **TypeScript**: 型安全性でバグを防止
4. **Tailwind CSS**: ユーティリティクラスでスタイリング

## 次のステップ

1. **基本的なコンポーネントの作成**
   - `src/app/components/` ディレクトリを作成
   - 再利用可能なコンポーネントを作成

2. **ルーティングの追加**
   - `src/app/` 内に新しいディレクトリを作成して新しいページを追加

3. **スタイリングの学習**
   - Tailwind CSSのユーティリティクラスを使用
   - カスタムCSSコンポーネントの作成

4. **状態管理の学習**
   - React Hooks（useState、useEffect等）
   - コンテキストAPI

5. **デプロイ**
   - [Vercel Platform](https://vercel.com/new) での簡単デプロイ

## トラブルシューティング

### よくある問題
- **ポート3000が使用中**: 別のアプリケーションがポート3000を使用している場合
  ```bash
  # 別のポートで起動
  npm run dev -- -p 3001
  ```

- **依存関係エラー**: package.jsonとnode_modulesの不整合
  ```bash
  # node_modulesを削除して再インストール
  rm -rf node_modules package-lock.json
  npm install
  ```
