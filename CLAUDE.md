# CLAUDE.md

必ず日本語で回答してください。

このファイルは、Claude Code (claude.ai/code) がこのリポジトリでコードを扱う際のガイダンスを提供します。

## 開発コマンド

- **開発サーバー起動**: `npm run dev`（高速ビルドのためTurbopackを使用）
- **本番用ビルド**: `npm run build`
- **本番サーバー起動**: `npm start`  
- **コードリント**: `npm run lint`

## プロジェクト構成

これはTypeScriptとTailwind CSSを使用するNext.js 15 Reactアプリケーションです。Next.js App Routerアーキテクチャに従っています：

- **App ディレクトリ構造**: ルーティングにApp Routerを使用した`src/app/`構造
- **フォント**: `next/font/google`経由でGeist SansとGeist Monoフォントを設定
- **スタイリング**: PostCSS設定を含むTailwind CSS v4
- **TypeScript**: ストリクトモードとパスマッピング（`@/*` → `./src/*`）を有効化

## 主要設定

- **Next.js**: `next.config.ts`でデフォルト設定を使用
- **ESLint**: Next.jsのcore-web-vitalsとTypeScriptルールを拡張
- **TypeScript**: ストリクトモードとbundlerモジュール解決でNext.js用に設定
- **Tailwind**: PostCSS統合を含むv4を使用

## ファイル構造

- `src/app/layout.tsx`: フォント設定とメタデータを含むルートレイアウト
- `src/app/page.tsx`: ホームページコンポーネント
- `src/app/globals.css`: グローバルスタイル
- `public/`: 静的アセット（SVGアイコン）
