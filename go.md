# Go Web Scraping

本文档包含 Go 中的网页抓取库和资源列表。

## 目录

- [库](#库)
  - [网络](#网络)
    - [HTTP 客户端](#http-客户端)
    - [WebSockets](#websockets)
    - [低级网络](#低级网络)
    - [其他](#其他)
  - [解析器](#解析器)
    - [HTML/XML 解析器](#html-xml-解析器)
    - [URL 解析器](#url-解析器)
    - [日期和时间解析器](#日期和时间解析器)
    - [JSON 解析器](#json-解析器)
    - [PDF 解析器](#pdf-解析器)
    - [Email 解析器](#email-解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [SQL 解析器](#sql-解析器)
    - [其他](#其他-1)
  - [网页抓取](#网页抓取)
    - [框架](#框架)
    - [代理集成](#代理集成)
    - [CAPTCHA 解决](#captcha-解决)
  - [网页自动化](#网页自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
    - [工具和插件](#工具和插件)
    - [其他](#其他-2)
  - [数据导出](#数据导出)
    - [序列化](#序列化)
    - [JSON](#json)
    - [CSV](#csv)
    - [其他](#其他-3)
  - [数据处理](#数据处理)
    - [文本处理](#文本处理)
    - [字符编码](#字符编码)
    - [日期和时间](#日期和时间)
    - [电话号码](#电话号码)
    - [Slug 处理](#slug-处理)
  - [其他](#其他-4)
    - [多进程](#多进程)
    - [任务调度](#任务调度)
- [热门网页抓取栈](#热门网页抓取栈)
  - [静态网页](#静态网页)
    - [HTTP 客户端 + HTML 解析器](#http-客户端-html-解析器)
    - [一体化网页抓取框架](#一体化网页抓取框架)
  - [动态网页](#动态网页)
    - [一体化浏览器自动化框架](#一体化浏览器自动化框架)
- [指南和教程](#指南和教程)
  - [通用指南](#通用指南)
  - [代理](#代理)
  - [对比](#对比)

## 库

**注意**：所有选择的库均为广泛使用或活跃维护的库。

### 网络

#### HTTP 客户端

- [net/http](https://pkg.go.dev/net/http): Go 内置的 HTTP 客户端和服务器实现
- [fasthttp](https://github.com/valyala/fasthttp): 一个快速的 Go HTTP 实现
- [resty](https://github.com/go-resty/resty): Go 的简单 HTTP 和 REST 客户端库
- [req](https://github.com/imroc/req): 带有“黑魔法”的简单 Go HTTP 客户端
- [gorequest](https://github.com/parnurzeal/gorequest): 一个简化的 HTTP 客户端

#### WebSockets

- [gorilla](https://github.com/gorilla/websocket): 一个快速、经过良好测试且广泛使用的 Go WebSocket 实现

#### 低级网络

- [net](https://pkg.go.dev/net): Go 内置的网络 I/O 接口，包括 TCP/IP、UDP 和 Unix 域套接字

#### 其他

- [caddy](https://github.com/caddyserver/caddy): 一个快速、可扩展的多平台 HTTP/1-2-3 Web 服务器，支持自动 HTTPS

### 解析器

#### HTML/XML 解析器

- [goquery](https://github.com/PuerkitoBio/goquery): 提供类似 jQuery 的语法和功能的 Go 包

#### JSON 解析器

- [jsonparser](https://github.com/buger/jsonparser): 一个无需模式的快速 JSON 解析器

### 网页抓取

#### 框架

- [colly](https://github.com/gocolly/colly): 一个优雅的 Go 抓取和爬虫框架

#### 代理集成

- [Bright Data's proxy services](https://bright.cn/proxy-types): 提供超过 7200 万个 IP 的代理网络，支持高级代理功能 [**Bright Data 解决方案**]

#### CAPTCHA 解决

- [Bright Data CAPTCHA Solver](https://bright.cn/products/web-unlocker/captcha-solver): 一个快速、自动化的 CAPTCHA 解决工具 [**Bright Data 解决方案**]

### 数据导出

#### JSON

- [encoding/json](https://pkg.go.dev/encoding/json): Go 内置的 JSON 编码和解码实现

#### CSV

- [encoding/csv](https://pkg.go.dev/encoding/csv): 读取和写入 CSV 文件的内置 Go 包

### 数据处理

#### 电话号码

- [phonenumbers](https://github.com/nyaruka/phonenumbers): Google's libphonenumber 的 Go 实现

### 任务调度

- [cron](https://github.com/robfig/cron): 一个 Go 的 cron 库

## 热门网页抓取栈

### 静态网页

#### HTTP 客户端 + HTML 解析器

- **HTTP 客户端**: net/http 或 go-retryablehttp
- **HTML 解析器**: goquery

#### 一体化网页抓取框架

- colly

## 指南和教程

### 通用指南

- [Go 中的网页抓取：完整指南](https://bright.cn/blog/how-tos/web-scraping-go)

### 代理

- [Go 代理服务器指南](https://bright.cn/blog/how-tos/go-proxy-servers)

### 对比

- [Go 与 Python 的对比指南](https://bright.cn/blog/web-data/go-vs-python)