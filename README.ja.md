# Claude Hands (日本語版)

<p align="center">
  <img src="assets/logo.png" width="200"/>
  <img src="assets/logo2.png" width="200"/>
</p>

<p align="center">
  <a href="README.ja.md"><img src="https://img.shields.io/badge/ドキュメント-日本語-white.svg" alt="JA doc"/></a>
  <a href="README.md"><img src="https://img.shields.io/badge/english-document-white.svg" alt="EN doc"></a>
</p>

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/r488it/claude_hands?style=social)](https://github.com/r488it/claude_hands/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<!-- 技術スタックバッジ -->

<img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white" alt="Docker" />
<img src="https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white" alt="Node.js" />
<img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white" alt="TypeScript" />
<img src="https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white" alt="Jupyter" />
<img src="https://img.shields.io/badge/MCP-222?logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjIwIiBoZWlnaHQ9IjIwIiBmaWxsPSIjNjY2Ii8+PHRleHQgeD0iNSIgeT0iMTUiIGZvbnQtc2l6ZT0iMTAiIGZpbGw9IndoaXRlIj5NQ1A8L3RleHQ+PC9zdmc+" alt="MCP" />

</div>

Claude Handsは、Manusの再現実装をClaude DesktopとMCPを活用して再現したプロジェクトです。

## 🆕 更新情報
2025.3.29 Browser operation supported.   
2025.3.29 ChatGPT Desktop supported. chatgpt_mcp_agent.config.yaml

## 🤖 推奨モデル
- Claude 3.7 Sonnet
- Claude 3.7 Sonnet think mode

## 🚀 機能

- Claude Code開発用の事前設定されたDocker環境
- 情報検索を強化するTavily検索統合
- MCP（Model Control Protocol）インターフェースを通じてClaude Desktopと互換性あり
- グラフィックレコーディングスタイルのインフォグラフィック生成機能

## 🔧 前提条件

- DockerとDocker Compose
- Claude Desktopアプリケーション
- Tavily APIキー

## 🛠 セットアップ手順

### 1. リポジトリのクローン

```bash
git clone https://github.com/r488it/claude_hands.git
cd claude_hands
```

### 2. 環境変数の設定

ルートディレクトリに`.env`ファイルを作成します：

```bash
touch .env
```

`.env`ファイルにTavily APIキーを追加します：

```
TAVILY_API_KEY=your_tavily_api_key_here
```

### 3. Dockerボリュームパスの更新

`docker-compose.yml`ファイルを編集して、ボリュームパスをシステムに合わせて更新します：

```yaml
volumes:
  - /path/to/your/workspace:/workspace
```

### 4. サービスの起動

```bash
docker-compose up -d
```

このコマンドにより：
- 必要なDockerイメージがまだ利用可能でない場合はプルされます
- Claude CodeとTavilyサービスが起動します
- 設定されたポートでサービスが公開されます

## 💻 Claude Desktopとの接続

1. `claude_desktop_config.json`ファイルをClaude Desktop設定ディレクトリにコピーします
2. Claude Desktopを再起動します
3. これでMCPサーバーをClaude Desktopで使用できるようになります

## 📝 使用方法

1. 新しいプロジェクトを作成する
<div align="center" style="display: flex; gap: 20px;">
    <img src="assets/01_make_project.png" alt="プロジェクト作成" width="600" />
</div>

2. プロンプトを設定する
<div align="center" style="display: flex; gap: 20px;">
    <img src="assets/02_set_prompt.png" alt="プロンプト設定" width="600" />
</div>

3. ナレッジテンプレートを追加する（オプション）
<div align="center" style="display: flex; gap: 20px;">
    <img src="assets/03_set_knowledge.png" alt="ナレッジ追加" width="600" />
</div>

## 📚 追加ドキュメント
- [ナレッジベース](docs/knowledge.md)
- [プロンプト（EN）](docs/prompt.md)
- [プロンプト（JA）](docs/prompt.ja.md)

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=r488it/claude_hands&type=Date)](https://www.star-history.com/#r488it/claude_hands&Date)
