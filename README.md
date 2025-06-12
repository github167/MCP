# MCP

MCP example[https://modelcontextprotocol.io/examples]

npx -y @modelcontextprotocol/server-filesystem F:\\ <<<  '{"method":"tools/list","jsonrpc":"2.0","id":1}'

npx -y @modelcontextprotocol/server-filesystem F:\\
{"method":"tools/call","params":{"name":"list_directory","arguments":{"path":"F:\\pwa"}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"get_file_info","arguments":{"path":"F:\\pwa\\道.zip"}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"write_file","arguments":{"path":"F:\\pwa\\abc.txt", "content":"hello world"}},"jsonrpc":"2.0","id":1}

npx -y @modelcontextprotocol/server-everything <<< '{"jsonrpc":"2.0","method":"tools/list","id":1}'

npx -y @modelcontextprotocol/server-everything
{"method":"tools/call","params":{"name":"echo","arguments":{"message":"hello world1"}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"add","arguments":{"a":3, "b":4}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"sampleLLM","arguments":{"prompt":"what is your name?"}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"getTinyImage","arguments":{}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"printEnv","arguments":{}},"jsonrpc":"2.0","id":1}
{"method":"tools/call","params":{"name":"getResourceReference","arguments":{"resourceId":73}},"jsonrpc":"2.0","id":1}
