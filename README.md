# Alibaba Cloud DMS MCP Server

A Model Context Protocol server for Alibaba Cloud DMS(Data Management).

This server facilitates unified metadata access and cross-engine data querying for large language models working with diverse database ecosystems.

---

## Overview  
**DMS MCP Server** provides:  
- Standardized interface for database metadata operations  

---

## Configuration  
Download from Github
```shell
git clone https://github.com/aliyun/alibabacloud-dms-mcp-server.git
```
Add the following configuration to the MCP client configuration file:
```json5
"mcpServers": {
  "dms-mcp-server": {
    "command": "uv",
    "args": [
      "--directory",
      "/path/to/alibabacloud-dms-mcp-server/src/alibabacloud_dms_mcp_server",
      "run",
      "server.py"
    ],
    "env": {
      "ALIBABA_CLOUD_ACCESS_KEY_ID": "access_id",
      "ALIBABA_CLOUD_ACCESS_KEY_SECRET": "access_key",
      "ALIBABA_CLOUD_SECURITY_TOKEN": "sts_security_token"  // optional, required when using STS Token
    }
  }
}
```
