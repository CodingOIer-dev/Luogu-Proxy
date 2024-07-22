# Luogu-Proxy 洛谷本地代理

## 注意事项

本仓库按照 GNU GPLv3 开源。

不接受 PR 等请求，但可以提出 issue。

## 脚本功能

请求速率限制为任意时刻最多有两个并发请求。

在本地的 `http://127.0.0.1:9000` 开启一个发送到洛谷的本地代理，请求可以使用 `src/luogu.py`。

## 快速开始

1. 将 `src/server.py` 放置到同服务器任意位置。

2. 运行 `python server.py`。（确定本地 `9000` 端口未被占用）

3. 把 `src/luogu.py` 放置到你的脚本同目录。

4. 将所有 `import requests` 更改为 `import luogu as requests` 即可。

> [!TIP]
>
> `luogu.py` 仅仅实现了 GET 和 POST 请求，且仅支持超链接、请求头、`json` 格式数据这 $3$ 个参数。
>
> 如有需要可以自行实现。