# コーディング規約構造

このプロジェクトのコーディング規約は、以下の8つのファイルに分割されています：

## 📁 ファイル構成

| ファイル | 対象 | 内容 | 優先度 |
|---------|------|------|--------|
| `01_basic_principles.mdc` | 全ファイル | 基本方針・プロセス・技術スタック | 1（最高） |
| `02_code_style.mdc` | TS/JS ファイル | コードスタイル・命名規則・エラー処理 | 2 |
| `03_ui_styling.mdc` | UI関連ファイル | TailwindCSS・デザイン・アクセシビリティ | 3 |
| `04_architecture.mdc` | ストア・API・テスト | 状態管理・アーキテクチャ・テスト・DB | 4 |
| `05_development_support.mdc` | 全ファイル | 国際化・ドキュメント・開発サポート | 5 |
| `06_testing.mdc` | テストファイル | t-wadaのTDDプラクティス・テスト環境 | 6 |
| `07_tdd_templates.mdc` | テストファイル | TDDテンプレート・Red-Green-Refactor | 7 |
| `requirements.mdc` | 全ファイル | 要件定義ガイドライン | 特殊 |

## 🎯 適用対象

各ファイルは `globs` パターンで適用対象を制限し、`auto_apply: true` により自動適用されます：

- **基本方針**: すべてのファイル (`["**/*"]`)
- **コードスタイル**: TypeScript/JavaScriptファイル (`["**/*.ts", "**/*.tsx", "**/*.js", "**/*.jsx"]`)
- **UI/スタイリング**: コンポーネント・ページ・スタイルファイル (`["src/components/**/*", "src/pages/**/*", "**/*.css", "**/*.scss", "tailwind.config.js", "postcss.config.js"]`)
- **アーキテクチャ**: ストア・フック・API・テストファイル (`["src/store/**/*", "src/hooks/**/*", "src/api/**/*", "src/**/*.test.*", "src/**/__tests__/**/*"]`)
- **開発サポート**: すべてのファイル (`["**/*"]`)
- **テスト実践**: テストファイル (`["**/*.test.ts", "**/*.test.tsx", "**/*.spec.ts", "**/*.spec.tsx", "**/__tests__/**/*"]`)
- **TDDテンプレート**: テストファイル (`["**/*.test.ts", "**/*.test.tsx", "**/*.spec.ts", "**/*.spec.tsx", "**/__tests__/**/*"]`)
- **要件定義**: すべてのファイル (`["**/*"]`) ※トリガー: `["要件定義！！！"]`

## 📋 確認メッセージ

各ルールファイルが適用されると、以下のメッセージが表示されます：

- **基本方針**: 「基本プロセス確認完了！」
- **コードスタイル**: 「コードスタイル規約確認完了！」
- **UI/スタイリング**: 「UI/スタイリング規約確認完了！」
- **アーキテクチャ**: 「アーキテクチャ規約確認完了！」
- **開発サポート**: 「開発サポート規約確認完了！」
- **テスト実践**: 「t-wadaのTDD実践開始！」
- **TDDテンプレート**: 「TDDテンプレート適用開始！」
- **要件定義**: 「要件定義やるやで！！！」

## 🔧 技術スタック

プロジェクトの技術スタックは以下の通りです：

- **フロントエンド**: React, TypeScript, TailwindCSS
- **状態管理**: Zustand
- **データベース**: Supabase (PostgreSQL)
- **テスト**: Jest, React Testing Library
- **国際化**: i18next, react-i18next
- **開発**: TDD (Test-Driven Development)

## 🏷️ フロントマター情報

各ルールファイルには以下のフロントマター項目が設定されています：

- **description**: ルールの概要説明
- **globs**: 適用対象ファイルパターン（配列形式）
- **tags**: 分類用タグ（配列形式）
- **priority**: 適用優先度（1が最高、7が最低）
- **auto_apply**: 自動適用フラグ（すべて `true`）
- **triggers**: 特定のキーワードでの起動（requirements.mdcのみ）

## 🎨 TDD実践ワークフロー

テスト駆動開発（TDD）の実践には以下のワークフローを使用します：

1. **Red フェーズ**: 失敗するテストを作成
2. **Green フェーズ**: テストを通す最小限の実装
3. **Refactor フェーズ**: コードの品質向上
4. **Coverage フェーズ**: テストカバレッジの分析

各フェーズでは `07_tdd_templates.mdc` に定義されたCursorプロンプトを活用できます。

## 🔄 メンテナンス

- **特定領域のルール変更**: 対応するファイルのみを編集
- **全体的な方針変更**: `01_basic_principles.mdc` を編集
- **テスト戦略の変更**: `06_testing.mdc` と `07_tdd_templates.mdc` を編集
- **要件定義プロセスの変更**: `requirements.mdc` を編集

フロントマターの変更時は、globsパターンとpriorityの整合性を確認してください。