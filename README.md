# 日期时间服务 

一个为AI助手提供实时日期、时间和时区信息的MCP服务器。
An MCP server that provides real-time date, time and time zone information for AI assistants.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| get-current-datetime | Returns the current date and time. Optionally specify a timezone. |
| get-day-of-week | Returns the day of the week for a given date or today. |
| get-timezone-info | Returns information about the current or specified timezone. |
| format-date | Format a date in various styles (short, medium, long, full). |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659373059](https://mcp.xiaobenyang.com/inspector/1777316659373059)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659373059](https://mcp.xiaobenyang.com/inspector/1777316659373059)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "日期时间服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659373059/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "日期时间服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659373059/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "日期时间服务": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659373059",
          },
          "transport": "stdio"
        }
      }
}

```
