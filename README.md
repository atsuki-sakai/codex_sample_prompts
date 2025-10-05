# codex_sample_prompts

このリポジトリは、Git／Pull Request／ブランチ運用／仕様設計などに関するサンプルプロンプトやテンプレート群をまとめたものです。  
AI（例：GitHub Copilot, ChatGPT, Claude 等）に対するプロンプト設計の参考として活用することを想定しています。

## 目次

1. [📂 ディレクトリ構成](#-ディレクトリ構成)  
2. [🎯 利用方法](#-利用方法)  
3. [🧰 各ファイルの説明](#-各ファイルの説明)  
4. [🛠 カスタマイズのヒント](#-カスタマイズのヒント)  
5. [🧩 利用例](#-利用例ワークフロー例)  
6. [📜 ライセンス](#-ライセンス)  

---

## 📂 ディレクトリ構成

```
/
├── git:add.md                  # Git add 操作用プロンプト
├── git:commit.md               # コミットメッセージ生成用テンプレート
├── git:pr.md                   # Pull Request 作成用テンプレート
├── git:pull-branch.md          # ブランチプル操作用プロンプト
├── git:pull-main.md            # メインブランチからのプル用テンプレート
├── git:push.md                 # リモートプッシュ用プロンプト
├── git:sync-file.md            # ファイル同期用テンプレート
├── kiro:spec-design.md         # 仕様設計用プロンプト
├── kiro:spec-impl.md           # 実装仕様落とし込み用テンプレート
├── kiro:spec-init.md           # プロジェクト初期設計用プロンプト
├── kiro:spec-requirements.md   # 要件整理用プロンプト
├── kiro:spec-status.md         # 進捗ステータス整理用テンプレート
├── kiro:spec-tasks.md          # タスク分割・優先順位づけ用プロンプト
├── kiro:steering-custom.md     # カスタムステアリング用プロンプト
├── kiro:steering.md            # 標準プロジェクト進行管理テンプレート
├── kiro:validate-design.md     # 設計妥当性チェック用プロンプト
├── kiro:validate-gap.md        # 要件ギャップ解析用テンプレート
└── README.md                   # このファイル
```

### カテゴリ分類

- **`git:*.md` 系**：Git 操作・ワークフローに関するプロンプトテンプレート  
- **`kiro:*.md` 系**：仕様設計、タスク分割、検証、ステアリング（進行管理）などのテンプレート  

---

## 🎯 利用方法

### 基本的な使い方

1. **リポジトリを取得**
   ```bash
   git clone <このリポジトリのURL>
   cd codex_sample_prompts
   ```

2. **必要なテンプレートファイルを選択**
   ```bash
   # 例：Pull Request用テンプレートを確認
   cat git:pr.md
   ```

3. **プレースホルダーを置換**
   - テンプレート中の `{issue_title}`, `{feature_name}` などを実際の値に置換
   - または、AI にプレースホルダーも含めてプロンプトとして渡す

4. **AI にプロンプトを入力**
   - ChatGPT, Claude, GitHub Copilot など、お好みのAIサービスに入力

5. **応答をレビュー・調整**
   - 生成された内容を確認し、必要に応じて修正

### 💡 プロンプト設計のコツ

- **明確な指示**：曖昧さを避け、期待する出力形式を明示する
- **コンテキスト提供**：プロジェクトの背景情報を含める
- **段階的アプローチ**：複雑なタスクは小さなステップに分割
- **評価基準の明記**：「良い出力」の基準を明確にする

---

## 🧰 各ファイルの説明

| カテゴリ | ファイル名 | 用途 | 主な用例 |
|---------|------------|------|----------|
| **Git操作** | `git:add.md` | 変更のステージング指示 | ファイル選択の自動化、変更説明の生成 |
| | `git:commit.md` | コミットメッセージ自動生成 | 規約準拠メッセージ、変更内容の要約 |
| | `git:pr.md` | Pull Request説明文生成 | PR概要、レビューポイントの整理 |
| | `git:pull-branch.md` | ブランチプル手順 | マージ前確認、コンフリクト対応 |
| | `git:pull-main.md` | メインブランチ同期 | 最新化手順、ベースブランチ更新 |
| | `git:push.md` | リモートプッシュ指示 | プッシュ前チェック、権限確認 |
| | `git:sync-file.md` | ファイル同期 | 個別ファイルの反映、部分同期 |
| **仕様設計** | `kiro:spec-init.md` | プロジェクト初期設計 | 要件定義、アーキテクチャ方針策定 |
| | `kiro:spec-requirements.md` | 要件整理 | ユーザーストーリー、機能要件の整理 |
| | `kiro:spec-design.md` | 詳細設計 | 技術仕様、API設計、データ設計 |
| | `kiro:spec-impl.md` | 実装仕様 | 設計の実装レベル落とし込み |
| | `kiro:spec-tasks.md` | タスク分割 | 作業分解、優先順位づけ、工数見積もり |
| | `kiro:spec-status.md` | 進捗管理 | ステータス報告、マイルストーン管理 |
| **品質管理** | `kiro:validate-design.md` | 設計検証 | アーキテクチャレビュー、整合性チェック |
| | `kiro:validate-gap.md` | ギャップ分析 | 要件と実装の乖離検出、課題特定 |
| **プロジェクト管理** | `kiro:steering.md` | 標準進行管理 | 定例会議、進捗追跡、リスク管理 |
| | `kiro:steering-custom.md` | カスタム進行管理 | プロジェクト特有の管理手法 |

---

## 🛠 カスタマイズのヒント

### 基本的なカスタマイズ

1. **プロジェクト固有の情報を追加**
   ```markdown
   プロジェクト名: {project_name}
   使用技術: {tech_stack}
   チーム構成: {team_structure}
   ```

2. **出力フォーマットの指定**
   ```markdown
   出力形式: JSON / Markdown / 表形式
   文字数制限: 〇〇字以内
   言語: 日本語 / 英語
   ```

3. **評価基準の明記**
   ```markdown
   評価観点:
   - 可読性（他の開発者が理解しやすい）
   - 網羅性（必要な情報が含まれている）
   - 簡潔さ（冗長でない）
   - 実用性（すぐに使える）
   ```

### 高度なカスタマイズ

- **チェーン型プロンプト**: 複数のテンプレートを組み合わせて使用
- **条件分岐**: プロジェクトの状況に応じてプロンプトを切り替え
- **フィードバックループ**: 生成結果を元に追加質問を行う

---

## 🧩 利用例（ワークフロー例）

### ケース1: Pull Request作成

```bash
# 1. PR用テンプレートを確認
cat git:pr.md

# 2. 変更内容を整理
git --no-pager diff --name-only
git --no-pager log --oneline -5

# 3. テンプレートをカスタマイズしてAIに入力
# (feature_name, changes_summary等を実際の値に置換)

# 4. 生成されたPR説明文をGitHubに使用
```

### ケース2: 仕様設計フロー

```bash
# 1. 初期設計
cat kiro:spec-init.md
# → 要件整理とアーキテクチャ方針を生成

# 2. 詳細設計
cat kiro:spec-design.md
# → 技術仕様書を生成

# 3. 設計検証
cat kiro:validate-design.md
# → 設計の妥当性をチェック

# 4. 実装仕様
cat kiro:spec-impl.md
# → 実装レベルの詳細を生成
```

### ケース3: 開発進行管理

```bash
# 週次進捗確認
cat kiro:steering.md
# → 進捗報告とリスク管理

# ギャップ分析
cat kiro:validate-gap.md
# → 計画と実績の乖離を分析
```

---

## 🔄 更新・貢献

### 新しいテンプレートの追加

1. 適切なカテゴリプレフィックスを使用（`git:`, `kiro:`など）
2. ファイル名は目的が分かりやすい名前に
3. テンプレート内にコメントで使用方法を記載

### 改善提案

- Issue でテンプレートの改善案を提案
- Pull Request でテンプレートの修正を提案
- 新しいカテゴリの提案も歓迎

---

## 📜 ライセンス

MIT License

Copyright (c) 2025 codex_sample_prompts

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## 🚀 クイックスタート

```bash
# リポジトリをクローン
git clone <repository-url>
cd codex_sample_prompts

# PR用プロンプトをすぐに試す
cat git:pr.md

# 仕様設計を始める
cat kiro:spec-init.md
```

**Happy Prompting! 🤖✨**