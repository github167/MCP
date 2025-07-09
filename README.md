# MCP examples: [https://modelcontextprotocol.io/examples]

server-filesystem [https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem]
```
# One line
npx -y @modelcontextprotocol/server-filesystem F:\\ <<<  '{"method":"tools/list","jsonrpc":"2.0","id":1}'

```
or input through stdio; copy and paste the following jsonrpc to test
```
npx -y @modelcontextprotocol/server-filesystem F:\\

# sometimes you may need to handshake with the mcp client first
{"method":"initialize","params":{"protocolVersion":"","capabilities":{},"clientInfo":{"name":"", "version":""}},"jsonrpc":"2.0","id":0}
{"method":"notifications/initialized","jsonrpc":"2.0"}


{"method": "tools/list", "jsonrpc":"2.0","id":1}
{"method": "ping","jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"list_directory","arguments":{"path":"F:\\pwa"}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"get_file_info","arguments":{"path":"F:\\pwa\\道.zip"}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"write_file","arguments":{"path":"F:\\pwa\\abc.txt", "content":"hello world"}},"jsonrpc":"2.0","id":1}

```

server-everything [https://github.com/modelcontextprotocol/servers/tree/main/src/everything]
```
# One line
npx -y @modelcontextprotocol/server-everything <<< '{"method":"tools/list","jsonrpc":"2.0","id":1}'

# stdio input, copy and paste the json-rpc to test
npx -y @modelcontextprotocol/server-everything

{"method": "ping","jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"echo","arguments":{"message":"hello world1"}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"add","arguments":{"a":3, "b":4}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"sampleLLM","arguments":{"prompt":"what is your name?"}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"getTinyImage","arguments":{}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"printEnv","arguments":{}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"annotatedMessage","arguments":{"messageType":"error"}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"getResourceReference","arguments":{"resourceId":73}},"jsonrpc":"2.0","id":1}
```

Inspector [https://modelcontextprotocol.io/docs/tools/inspector]
```
npx @modelcontextprotocol/inspector npx -y @modelcontextprotocol/server-everything

# grab page from a url
npx @modelcontextprotocol/inspector uvx mcp-server-fetch --ignore-robots-txt

# CRUD a sqlite db (default "sqlite_mcp_server.db")
npx @modelcontextprotocol/inspector uvx mcp-server-sqlite --db-path ./test.db

# check and convert time
npx @modelcontextprotocol/inspector uvx mcp-server-time --local-timezone=Asia/Hong_Kong

#http://127.0.0.1:6274

```

[https://www.youtube.com/@%E8%B5%8B%E8%8C%83%E8%AF%BE%E5%A0%82/videos](https://www.youtube.com/watch?v=lXW32JXVHrg)

[https://www.youtube.com/@01coder30](https://www.youtube.com/@01coder30/videos)

https://www.youtube.com/@nateherk/videos


