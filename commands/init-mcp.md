---
allowed-tools: "Read", "Edit", "MultiEdit", "Write", "Glob", "Grep", "LS", "Bash", "TodoWrite", "TodoRead", "Bash(git:*)", "Bash(gh:*)", "Bash(say:*)"
description: MCPの設定を初期化するコマンド
---

# やること

- コマンドを実行したプロジェクトで後述のMCPが設定されているかを確認し、未設定であればセットするコマンド

# MCPの設定

## 共通事項

- 事前に設定済みかどうかを必ずチェックし、設定済みであれば対応をスキップすること

## Serena MCP

- 参考
  - https://github.com/oraios/serena
- 事前準備
    ```bash
    # uvがインストールされていなければHomebrewでuvをインストール
    $ brew install uv
    ```
- 設定コマンド
    ```bash
    $ claude mcp add serena -s project -- uvx --from git+https://github.com/oraios/serena serena start-mcp-server --context ide-assistant --project $(pwd)
    ```
- セットアップ
    ```
    # LLMのChatに以下を入力
    Serena のオンボーディングを開始してください。
    ```
