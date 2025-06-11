# MCP Deployment Server

A Model Context Protocol (MCP) server for deployment demonstrations.

## Installation

### Option 1: Run directly from GitHub

You can run the MCP server directly from the GitHub repository using `uvx`:

```bash
uvx --from git+https://github.com/ceesib/mcpserverexample.git mcp-server
```

### Option 2: Local installation

1. Clone the repository:
```bash
git clone https://github.com/ceesib/mcpserverexample.git
cd mcpserverexample
```

2. Install the package:
```bash
uv pip install -e .
```

3. Run the server:
```bash
uv run mcp-server
```

## MCP Client Configuration

Add the following configuration to your MCP client settings:

```json
{
  "mcpServers": {
    "deployment-server": {
      "command": "uvx",
      "args": [
        "--from",
        "git+https://github.com/ceesib/mcpserverexample.git",
        "mcp-server"
      ]
    }
  }
}
```

## Features

- Simple addition tool for demonstration purposes
- Compatible with MCP protocol
- Easy deployment via `uvx`

## Requirements

- Python >= 3.13
- uv package manager