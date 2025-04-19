<p align="center">
  <a href="README.ja.md"><img src="https://img.shields.io/badge/ドキュメント-日本語-white.svg" alt="JA doc"/></a>
  <a href="README.md"><img src="https://img.shields.io/badge/english-document-white.svg" alt="EN doc"></a>
</p>

<p align="center">
  <img src="assets/logo.png" width="200"/>
  <img src="assets/logo2.png" width="200"/>
</p>

<h1 align="center">Claude Hands</h1>

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/r488it/claude_hands?style=social)](https://github.com/r488it/claude_hands/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<!-- Tech Stack Badges -->
<img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white" alt="Docker" />
<img src="https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white" alt="Node.js" />
<img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white" alt="TypeScript" />
<img src="https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white" alt="Jupyter" />
<img src="https://img.shields.io/badge/MCP-222?logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjIwIiBoZWlnaHQ9IjIwIiBmaWxsPSIjNjY2Ii8+PHRleHQgeD0iNSIgeT0iMTUiIGZvbnQtc2l6ZT0iMTAiIGZpbGw9IndoaXRlIj5NQ1A8L3RleHQ+PC9zdmc+" alt="MCP" />

</div>

Claude Hands is a project that recreates Manus implementation using Claude Desktop and MCP (Model Control Protocol).


## Update

- 2025.4.19 Refined Docker setup to support Windows environment.
- 2025.3.29 Browser operation supported.   
- 2025.3.29 ChatGPT Desktop supported. chatgpt_mcp_agent.config.yaml

## Recommended Model
- Claude 3.7 Sonnet
- Claude 3.7 Sonnet think mode

## Demo

https://github.com/user-attachments/assets/615c8973-c117-4012-9111-e44d594d6869

## 🚀 Features

- Pre-configured Docker environment for Claude Code development
- Enhanced information retrieval with Tavily search integration
- Seamless compatibility with Claude Desktop through MCP interfaces
- Powerful graphic recording-style infographic generation capabilities

## Prerequisites

- Docker and Docker Compose
- Claude Desktop application
- Tavily API key

## 🛠 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/r488it/claude_hands.git
cd claude_hands
```

### 2. Configure Environment Variables

Create a `.env` file in the root directory:

```bash
touch .env
```

Add your Tavily API key to the `.env` file:

```
TAVILY_API_KEY=your_tavily_api_key_here
```

### 3. Update Docker Volume Paths

Edit the `docker-compose.yml` file to match your system's paths:

```yaml
volumes:
  - /path/to/your/workspace:/workspace
```

### 4. Start the Services

```bash
docker-compose up -d
```

This command will:
- Pull the required Docker images (if not already available)
- Start the Claude Code and Tavily services
- Make the services available on the configured ports

## Connecting with Claude Desktop

1. Copy the `claude_desktop_config.json` file to your Claude Desktop configuration directory
2. Restart Claude Desktop
3. You can now use the MCP servers through Claude Desktop

## Usage

1. Create a new project
<div align="center" style="display: flex; gap: 20px;">
    <img src="assets/01_make_project.png" alt="Create project" width="600" />
</div>

2. Set up your prompt
<div align="center" style="display: flex; gap: 20px;">
    <img src="assets/02_set_prompt.png" alt="Set prompt" width="600" />
</div>

3. Add knowledge template (optional)
<div align="center" style="display: flex; gap: 20px;">
    <img src="assets/03_set_knowledge.png" alt="Add knowledge" width="600" />
</div>

## 📚 Additional Documentation
- [Knowledge Base](knowledge.md)
- [Prompt (EN)](prompt.md)
- [Prompt (JA)](prompt.ja.md)

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=r488it/claude_hands&type=Date)](https://www.star-history.com/#r488it/claude_hands&Date)
