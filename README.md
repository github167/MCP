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

赋范课堂 https://www.youtube.com/@%E8%B5%8B%E8%8C%83%E8%AF%BE%E5%A0%82/videos (long course!)

01coder30 https://www.youtube.com/@01coder30

Nate Herk | AI Automation https://www.youtube.com/@nateherk/videos

技术爬爬虾 https://www.youtube.com/@tech-shrimp/videos

程序员老王 https://www.youtube.com/@programmer-wang/videos

马克的技术工作坊 https://www.youtube.com/@%E9%A9%AC%E5%85%8B%E7%9A%84%E6%8A%80%E6%9C%AF%E5%B7%A5%E4%BD%9C%E5%9D%8A

Cline 60000+ prompt message: https://www.yuque.com/xuanyuanzhifeng-xofk5/yie9fu/xex3cyng7o8q5si5#

```
SYSTEM: 
使用三個雙引號中提供的文章來回答問題。如果在文章中找不到答案，請回答「我找不到答案。」

USER:
"""

藍委邀外部顧問共同考察核四，台電：不符保安規定

中央通訊社是中華民國的國家通訊社，是台灣最具影響力的新聞媒體。秉持「正確、領先、客觀、詳實」的基本原則，中央社專業新聞團隊每天以中、英、日、西文即時對外發出上千則新聞、照片、圖表、影音與資訊，是台灣唯一多語文新聞媒體，服務對象從媒體客戶擴大為閱聽大眾；從台灣民眾延伸至全球華僑與讀者，充分扮演「華人之眼，世界之窗」。



國民黨立委翁曉玲、賴士葆與王鴻薇9日將前往核四廠考察，並要求清大核工所教授李敏等外部顧問共同參與。台電透過新聞稿說明，基於遵守核子保防要求，台電僅能同意國家賦予職權者如立委、監委等因問政要求進入。

（中央社）國民黨立委翁曉玲、賴士葆與王鴻薇9日將前往核四廠考察，並要求清大核工所教授李敏等外部顧問共同參與。台電8日表示，基於遵守國際最高核子保防要求，僅能同意國家賦予職權者如立委、監委等因問政要求進入核電廠，外部顧問不符合保安規定，無法核准進入。

台電透過新聞稿說明，基於遵守國際最高核子保防要求以維護門禁有效管控，台電僅能同意國家賦予職權者如立法委員（含國會助理）、監察委員等因問政要求進入核電廠。

台電舉例，立法院經濟委員會2021年8月9日即依此原則，邀集時任國民黨立委孔文吉、洪孟楷、陳玉珍；時任民進黨立委賴品妤、時任民眾黨立委蔡壁如等15位朝野立委及助理進入核二廠考察。

台電強調，竭誠歡迎立委到廠視察，其他外部顧問並不符合保安規定，因此無法一併同意核准參訪，請立委支持核電廠各項保安規定與門禁要求。

台電說明，由於龍門資產管理中心（原核四廠）內仍有台美核能和平利用合作協定列管的核子設備與組件，須遵守國際原子能總署（IAEA）制定的保安實體防護規範，除了核能發電相關管制稽查機關人員可申請執行核能發電相關管制稽查業務外，立委、監委等則依問政需求，經申請獲台電核准後，可實地了解核電廠運作。

外界質疑日前立委考察核三廠時，學者專家可陪同，台電則澄清，立法院社會福利及衛生環境委員會為考察屏東地區環境概況，今年7月10日赴核三廠南部展示館聽取「核三廠除役及光電開發建置影響行為現勘」簡報，並入廠現地勘查。考察過程核三廠周邊地方民意代表參與，是以利害關係人身份因環保議題受衛環委員會邀請，且為履行監督地方重大設施義務與責任，與此次參訪立委欲另邀請核能顧問截然不同，不應混為一談。

台電強調，台電核能場域均恪遵國際原子能總署核子保防機制與保安實體防護規範，獲國際原子能總署評列為「所有核物料均用於核能和平用途國家」的最高評等，台電歡迎立委到訪考察，亦請立委支持保安門禁與人員出入管控，以共同努力維繫國際最高核子保防評鑑成果。

"""
問題: 有哪學大學的教授參與考察?
```

Generate model https://lmarena.ai/
```
Using the nano-banana model, create a 1/7 scale commercialized figurine of the characters in the picture, in a realistic style, in a real environment. The figurine is placed on a computer desk. The figurine has a round transparent acrylic base, with no text on the base. The content on the computer screen is the Zbrush modeling process of this figurine. Next to the computer screen is a BANDAI-style toy packaging box printed with the original artwork. The packaging features two-dimensional flat illustrations.

Please turn this photo into a figurine. Behind it, there should be a Model packaging box with the character from this photo printed on it. In front of the box on a round plastic base place the fiqure version of the photo I gave you. l'd like the PVC material to be clearly represented. It would be even better if the background is indoors.
```
