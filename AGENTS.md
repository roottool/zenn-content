# AGENTS.md

このファイルは、このリポジトリで作業するAIアシスタント向けのガイダンスを提供します。

## プロジェクト概要

このリポジトリはZennプラットフォーム向けの記事と書籍コンテンツを管理します。

- リポジトリ名: `zenn-content`
- 著者: roottool
- ライセンス: MIT

## 開発コマンド

| コマンド | 説明 |
| --- | --- |
| `bun run preview` | Zennプレビューサーバーを起動（ローカルで記事・書籍をプレビュー） |
| `bun run new:article` | 新しい記事を作成 |
| `bun run new:book` | 新しい書籍を作成 |

## アーキテクチャと構造

### ディレクトリ構造

```txt
zenn-content/
├── articles/         # 記事ファイルを格納
├── books/            # 書籍ファイルを格納
├── .github/          # GitHub設定（Renovate等）
├── .editorconfig     # エディタ設定
├── .gitignore        # Git除外設定
├── package.json      # プロジェクト設定
└── bun.lock          # Bunロックファイル
```

### 主要コンポーネント

- **articles/**: Zenn記事（Markdown形式）を配置
- **books/**: Zenn書籍（複数のMarkdownファイルで構成）を配置
- **zenn-cli**: Zenn公式CLIツール（v0.2.10）でコンテンツ管理とプレビュー機能を提供

## 重要な設定

### パッケージマネージャ

- Bun
- ロックファイル: `bun.lock`

## 使用方法

1. **新しい記事を作成**: `bun run new:article`
2. **新しい書籍を作成**: `bun run new:book`
3. **プレビュー**: `bun run preview` でローカルサーバーを起動して確認
4. 参考リンク:
   - [Zenn CLIガイド](https://zenn.dev/zenn/articles/zenn-cli-guide)
   - [Zenn Markdownガイド](https://zenn.dev/zenn/articles/markdown-guide)

## ブランチ戦略

- メインブランチ: `main`
- 機能ブランチから `main` へPRを作成

## 依存関係

- **zenn-cli** (v0.2.10): Zenn公式CLIツール
