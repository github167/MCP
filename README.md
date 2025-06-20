# MCP clients and servers: [https://github.com/MarkTechStation/VideoCode/tree/main/MCP%20%E4%B8%8E%20Function%20Calling%20%E5%88%B0%E5%BA%95%E4%BB%80%E4%B9%88%E5%85%B3%E7%B3%BB/MarkChat]

Install
```
git clone -b mcp_clients https://github.com/github167/MCP
cd MC
uv sync

```
Prepare .env file
```
OPENROUTER_API_KEY=xxx
```
run server
```
uv run start.py
# surf to URL: http://127.0.0.1:5000/
```
