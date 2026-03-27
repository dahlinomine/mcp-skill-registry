# MCP Skill Registry

![mcp](https://img.shields.io/badge/mcp-blue?style=flat-square) ![tools](https://img.shields.io/badge/tools-blue?style=flat-square) ![registry](https://img.shields.io/badge/registry-blue?style=flat-square)

A centralized hub for Model Context Protocol servers to share and discover new agent tools.

## Overview
The MCP Skill Registry provides a unified interface for managing and distributing specialized capabilities across the Model Context Protocol ecosystem. It acts as a bridge between tool developers and AI agents, allowing for the seamless indexing, versioning, and retrieval of server-side functions to enhance agentic workflows.

## Features
*   **Centralized Discovery:** Easily browse and search for available MCP servers and specific tools.
*   **Dynamic Registration:** Register new tools and capabilities via a simple Python-based API.
*   **Version Management:** Track updates and maintain compatibility across different tool versions.
*   **Agent Integration:** Streamlined endpoints for LLM agents to fetch tool definitions and schemas.

## Installation
Ensure you have Python 3.10+ installed. Clone the repository and install the necessary dependencies:

```bash
git clone https://github.com/your-username/mcp-skill-registry.git
cd mcp-skill-registry
pip install -r requirements.txt
```

## Usage
To launch the registry service, run the main entry point:

```bash
python main.py
```

You can then register a new tool using the registry client:

```python
from mcp_registry import RegistryClient

client = RegistryClient("http://localhost:8000")
client.register_tool(
    name="weather_fetcher",
    description="Get current weather data for a city",
    endpoint="http://my-weather-server/mcp"
)
```

## Contributing
Contributions are welcome! Please submit a Pull Request or open an issue to discuss proposed changes. Ensure that your code adheres to the project's formatting standards and includes appropriate test coverage for new features.

## License
This project is licensed under the [MIT License](LICENSE).