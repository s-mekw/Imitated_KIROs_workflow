# Imitated KIRO's Workflow

このリポジトリは、ユーザーの初期リクエストを元に、ソフトウェア開発に必要な各種ドキュメントをAIを用いて自動生成するワークフローのデモンストレーションです。
開発エージェントKIROにインスパイアされています。

## 概要

`user_request.md` にユーザーの要望を記述することで、用意されたプロンプトファイルを使って `requirements.md`、`design.md`、`tasks.md` を順次生成することができます。

これにより、要件定義から具体的なタスク分割まで、一貫性のある開発ドキュメント群を迅速に作成することが可能になります。

## ワークフロー

このリポジトリには、2つの主要な開発ワークフローが含まれています。

### 1. 標準ワークフロー

汎用的なアプリケーション開発のためのワークフローです。

-   **ディレクトリ:** `imitated_KIRO_flow_EN/`, `imitated_KIRO_flow_JP/`
-   **プロセス:**
    1.  **要件生成:** `user_request.md` を基に `requirements.md` を作成します。ユーザーストーリーと受け入れ条件を定義します。
    2.  **設計生成:** `requirements.md` を基に `design.md` を作成します。技術スタック、アーキテクチャ、データモデルなどを定義します。
    3.  **タスク生成:** `requirements.md` と `design.md` を基に `tasks.md` を作成します。開発作業を具体的で管理可能なタスクに分割します。

### 2. TDD (テスト駆動開発) ワークフロー

TDD（テスト駆動開発）の手法に特化したワークフローです。Red-Green-Refactorのサイクルを円滑に進めるための成果物を生成するようにプロンプトが設計されています。

-   **ディレクトリ:** `TDD_flow_EN/`, `TDD_flow_JP/` (もし存在すれば)
-   **プロセス:**
    1.  **TDD指向の要件生成:** 要件をテスト可能な最小の振る舞い単位まで分解した `requirements.md` を作成します。
    2.  **TDD指向の設計生成:** テスト容易性とシンプルな初期設計（YAGNI）に焦点を当てた `design.md` を作成します。"Tidy First" の計画も含まれます。
    3.  **TDDタスク生成:** 各振る舞いに対してRed-Green-Refactorのサイクルに沿ったタスク構成を持つ `tasks.md` を作成します。

## 利用方法

1.  利用したいワークフローと言語を選択します（例: `TDD_flow_EN`）。
2.  作業ディレクトリに、開発したいアプリケーションの要望を記述した `user_request.md` を作成します。
3.  `user_request.md` の内容と `requirements-generation-prompt.md` のプロンプトを組み合わせてAIに入力し、`requirements.md` を生成します。
4.  次に、生成された `requirements.md` と `design-generation-prompt.md` のプロンプトを組み合わせてAIに入力し、`design.md` を生成します。
5.  最後に、生成された `requirements.md` と `design.md` を `tasks-generation-prompt.md` のプロンプトと組み合わせて `tasks.md` を生成します。

これらの手順に従うことで、AIが生成したドキュメントを基に、体系的に開発を進めることができます。

## ディレクトリ構成

-   `imitated_KIRO_flow_EN/`: 標準ワークフローのプロンプト (英語)
-   `imitated_KIRO_flow_JP/`: 標準ワークフローのプロンプト (日本語)
-   `TDD_flow_EN/`: TDDワークフローのプロンプト (英語)
-   `TDD_flow_JP/`: TDDワークフローのプロンプト (日本語)