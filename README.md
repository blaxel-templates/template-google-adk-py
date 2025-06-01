# Blaxel Google ADK Agent

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/downloads/release/python-3100/)
[![UV](https://img.shields.io/badge/UV-synced-green.svg)](https://github.com/astra-sh/uv)
[![Blaxel CLI](https://img.shields.io/badge/Blaxel_CLI-installed-green.svg)](https://docs.blaxel.ai/Get-started)

</div>

A template implementation of a conversational agent using Google ADK and GPT-4. This agent demonstrates the power of Google ADK for building interactive AI agents with tool integration capabilities.

## Table of Contents

- [Features](#features)
- [Quick Start](#quick-start)
- [Installation](#installation)
- [Usage](#usage)
  - [Running Locally](#running-locally)
  - [Testing Your Agent](#testing-your-agent)
- [Deployment](#deployment)
- [API Reference](#api-reference)
- [Project Structure](#project-structure)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [Support](#support)
- [License](#license)

## Features

- Interactive conversational interface
- Tool integration support (including weather and search capabilities)
- Streaming responses for real-time interaction
- Built on Google ADK for efficient agent orchestration
- Easy deployment and integration with Blaxel platform

## Quick Start

### Clone the repository

```bash
git clone https://github.com/blaxel-ai/template-google-adk-py.git
```

### Navigate to project directory

```bash
cd template-google-adk-py
```

## Installation

### Prerequisites

- Python 3.10 or later
- [UV](https://github.com/astra-sh/uv): Fast Python package manager
- [Blaxel CLI](https://docs.blaxel.ai/Get-started)

### Install dependencies

```bash
uv sync
```

### Apply Blaxel manifests

```bash
bl apply -f .blaxel
```

### Blaxel login

```bash
bl login YOUR-WORKSPACE
```

## Usage

### Running Locally

Start the development server with hot reloading:

```bash
bl serve --hotreload
```

### Testing Your Agent

Using chat interface:

```bash
bl chat --local blaxel-agent
```

With specific input:

```bash
bl run agent blaxel-agent --local --data '{"inputs": "What is the weather in Paris?"}'
```

## Deployment

Deploy your application:

```bash
bl deploy
```

## API Reference

```bash
POST /agents/{agent_id}/run
GET /agents/{agent_id}/info
GET /health
```

## Project Structure

- `src/main.py` - Application entry point
- `src/agent.py` - Core agent implementation with Google ADK integration
- `src/server/` - Server implementation and routing
- `pyproject.toml` - UV package manager configuration
- `blaxel.toml` - Blaxel deployment configuration

## Troubleshooting

- Ensure Python 3.10+ is installed
- Verify network connectivity and API keys
- Check Blaxel CLI installation
- Re-run `uv sync` to update dependencies

## Contributing

Contributions are welcome! To get started:

1. Fork the repository
2. Create a feature branch:
   ```bash
   git checkout -b my-feature
   ```
3. Commit your changes:
   ```bash
   git add .
   git commit -m 'Add my feature'
   ```
4. Push to the branch:
   ```bash
   git push origin my-feature
   ```
5. Submit a pull request

## Support

- Report bugs and feature requests on [GitHub Issues](https://github.com/blaxel-ai/template-google-adk-py/issues)
- Reach out on [Blaxel Discord](https://discord.gg/GsNzqUPcHP)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
