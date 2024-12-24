# Go Web Scraping

本文档包含 Go 中的网页抓取库和资源列表。

## 目录

- [库](#库)
  - [网络](#网络)
    - [HTTP 客户端](#http-客户端)
    - [WebSockets](#websockets)
    - [底层网络](#底层网络)
    - [其他](#其他)
  - [解析器](#解析器)
    - [HTML/XML 解析器](#htmlxml-解析器)
    - [URL 解析器](#url-解析器)
    - [日期和时间解析器](#日期和时间解析器)
    - [JSON 解析器](#json-解析器)
    - [PDF 解析器](#pdf-解析器)
    - [邮件解析器](#邮件解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [SQL 解析器](#sql-解析器)
    - [其他](#其他-1)
  - [网络爬取](#网络爬取)
    - [框架](#框架)
    - [代理集成](#代理集成)
    - [CAPTCHA 解决](#captcha-解决)
  - [网络自动化](#网络自动化)
    - [浏览器自动化框架](#浏览器-自动化框架)
    - [工具和插件](#工具和插件)
    - [其他](#其他-2)
  - [数据导出](#数据导出)
    - [序列化](#序列化)
    - [JSON](#json)
    - [CSV](#csv)
    - [其他](#其他-3)
  - [数据处理](#数据处理)
    - [文本](#文本)
    - [字符编码](#字符编码)
    - [日期和时间](#日期和时间)
    - [电话号码](#电话号码)
    - [Slugs](#slugs)
  - [其他](#其他-4)
    - [多进程](#多进程)
    - [任务调度](#任务调度)
- [常用网络爬虫技术栈](#常用网络爬虫技术栈)
  - [静态网页](#静态网页)
    - [HTTP 客户端 + HTML 解析器](#http-客户端--html-解析器)
    - [一体化网络爬取框架](#一体化网络爬取框架)
  - [动态网页](#动态网页)
    - [一体化浏览器自动化框架](#一体化浏览器自动化框架)
- [指南和教程](#指南和教程)
  - [通用指南](#通用指南)
  - [代理](#代理)
  - [对比](#对比)

## 库

**注意**：以下列出的库都被广泛使用或积极维护。

### 网络

#### HTTP 客户端

- [net/http](https://pkg.go.dev/net/http)：Go内置包，提供HTTP客户端和服务器实现。
- [fasthttp](https://github.com/valyala/fasthttp)：一个为Go提供的快速HTTP实现。
- [resty](https://github.com/go-resty/resty)：一个简单的Go HTTP和REST客户端库。
- [req](https://github.com/imroc/req)：一个带有“黑魔法”的简单Go HTTP客户端。
- [requests](https://github.com/earthboundkid/requests)：为Gophers提供的HTTP请求库。
- [heimdall](https://github.com/gojek/heimdall)：Go的增强型HTTP客户端。
- [go-retryablehttp](https://github.com/hashicorp/go-retryablehttp)：一个Go中的可重试HTTP客户端。
- [retryablehttp-go](https://github.com/projectdiscovery/retryablehttp-go)：提供自动重试和指数退避，并具有熟悉HTTP客户端接口的包。
- [sling](https://github.com/dghubble/sling)：一个用于创建和发送API请求的Go HTTP客户端库。
- [gorequest](https://github.com/parnurzeal/gorequest)：一个简化的HTTP客户端（受Node.js的[SuperAgent](https://ladjs.github.io/superagent/)启发）。

#### WebSockets

- [gorilla](https://github.com/gorilla/websocket)：一个快速、经过充分测试且被广泛使用的Go WebSocket实现。
- [websocket](https://github.com/coder/websocket)：一个最小化且符合Go风格的WebSocket库。

#### 底层网络

- [net](https://pkg.go.dev/net)：Go内置可移植的网络I/O接口，包括TCP/IP、UDP、域名解析和Unix域套接字。
- [gots](https://github.com/Comcast/gots)：一个Go库，用于在Go中处理MPEG传输流。

#### 其他

- [caddy](https://github.com/caddyserver/caddy)：一个快速且可扩展的多平台HTTP/1-2-3 Web服务器，内置自动HTTPS功能。

### 解析器

#### HTML/XML 解析器

- [goquery](https://github.com/PuerkitoBio/goquery)：一个将 [jQuery](https://jquery.com/) 的语法和功能特性带到Go语言的包。
- [encoding/xml](https://pkg.go.dev/encoding/xml)：Go内置的简单XML 1.0解析器，支持XML命名空间。
- [net/html](https://pkg.go.dev/golang.org/x/net/html)：Go内置的HTML包，实现了符合HTML5标准的标记器和解析器。
- [xml-stream-parser](https://github.com/tamerh/xml-stream-parser)：一个Go的XML流解析器。
- [pagser](https://github.com/foolin/pagser)：基于goquery和结构体标签的简单、可扩展、可配置的HTML页面解析库，可将HTML页面反序列化为struct，适用于Go爬虫。

#### URL 解析器

- [net/url](https://pkg.go.dev/net/url)：Go内置包，用于解析URL并实现查询转义。
- [urlquery](https://github.com/hetiansu5/urlquery)：基于Go的URL查询字符串编码和解析库。

#### 日期和时间解析器

- [dateparse](https://github.com/araddon/dateparse)：一个库，可在未知格式情况下解析多种日期字符串。

#### JSON 解析器

- [jsonparser](https://github.com/buger/jsonparser)：Go中最快的替代JSON解析器之一，且不需要schema。

#### PDF 解析器

- [pdfcpu](https://github.com/pdfcpu/pdfcpu)：一个用Go编写的PDF处理器。
- [pdf](https://github.com/ledongthuc/pdf)：Go语言中的PDF读取器。

#### 邮件解析器

- [net/mail](https://pkg.go.dev/net/mail)：Go内置包，实现邮件消息的解析。

#### Markdown 解析器

- [markdown](https://github.com/gomarkdown/markdown)：Go的Markdown解析和HTML渲染器。
- [blackfriday](https://github.com/russross/blackfriday)：Go的Markdown解析器。
- [goldmark](https://github.com/yuin/goldmark)：用Go编写的Markdown解析器。易于扩展，遵循标准（[CommonMark](https://commonmark.org/)）且结构良好。

#### SQL 解析器

- [vitess-sqlparser](https://github.com/blastrain/vitess-sqlparser)：一个Go的简单SQL解析器（由vitess和TiDB驱动）。
- [sqlparser](https://github.com/xwb1989/sqlparser)：一个用Go实现的SQL解析器。

#### 其他

- [grobotstxt](https://github.com/jimsmart/grobotstxt)：谷歌robots.txt解析器和匹配器库的Go原生移植。
- [gofeed](https://github.com/mmcdole/gofeed)：一个用于解析RSS、Atom和JSON feeds的Go库。
- [go-flags](https://github.com/jessevdk/go-flags)：Go的命令行选项解析库。
- [toml](https://github.com/BurntSushi/toml)：一个Go的TOML解析器，支持反射。

### 网络爬虫

#### 框架

- [colly](https://github.com/gocolly/colly)：一个优雅的Go抓取和爬虫框架。
- [surf](https://github.com/headzoo/surf)：一个Go的有状态可编程网页浏览库。
- [gospider](https://github.com/jaeles-project/gospider)：一个用Go编写的快速网页蜘蛛。
- [ferret](https://github.com/MontFerret/ferret)：一个声明式网页抓取库。
- [pholcus](https://github.com/andeya/pholcus)：一个用纯Go编写的分布式高并发爬虫软件。

#### 代理集成

- [Bright Data的代理服务](https://bright.cn/proxy-types)：一个拥有超过7200万个IP的代理网络，提供优质的住宅、数据中心、移动和ISP代理。支持按州、国家、ZIP和ASN级别定位，覆盖195个国家。适用于任何HTTP客户端或抓取库[**Bright Data的解决方案**]。
- [goproxy](https://github.com/elazarl/goproxy)：Go的HTTP代理库。

#### CAPTCHA 解决

- [CAPTCHA Solver](https://bright.cn/products/web-unlocker/captcha-solver)：一个快速、自动化的CAPTCHA解决方案，可解决reCAPTCHA、hCaptcha、px_captcha、SimpleCaptcha、GeeTest CAPTCHA等[**Bright Data的解决方案**]。
- [captcha](https://github.com/dchest/captcha)：一个生成并验证图片和音频CAPTCHA的包。

### 网络自动化

#### 浏览器自动化框架

- [chromedp](https://github.com/chromedp/chromedp)：通过[Chrome DevTools Protocol](https://chromedevtools.github.io/devtools-protocol/)驱动浏览器的更快速、更简单的方式。
- [rod](https://github.com/go-rod/rod)：一个Chrome DevTools协议的驱动程序，用于网络自动化和爬虫。
- [selenium](https://github.com/tebeka/selenium)：Go的Selenium/Webdriver客户端。
- [playwright-go](https://github.com/playwright-community/playwright-go)：一个浏览器自动化库，用于通过单一API控制Chromium、Firefox和WebKit。基于[Playwright](https://playwright.dev/)的Go移植版本。

#### 工具和插件

- [go-rod/stealth](https://github.com/go-rod/stealth)：一个与rod搭配使用的反机器人检测插件。

#### 其他

- [robotgo](https://pkg.go.dev/github.com/go-vgo/robotgo)：一个Go原生的跨平台RPA和GUI自动化库。

### 数据导出

#### 序列化

- [mus-go](https://github.com/mus-format/mus-go)：一组用于Golang的序列化原语。

#### JSON

- [encoding/json](https://pkg.go.dev/encoding/json)：Go内置的用于编码和解码JSON（符合RFC 7159）的包。

#### CSV

- [encoding/csv](https://pkg.go.dev/encoding/csv)：Go内置的读取和写入用逗号分隔值（CSV）文件的包。

#### 其他

- [unioffice](https://github.com/unidoc/unioffice)：一个纯Go的库，用于创建和处理Office Word(.docx)、Excel(.xlsx)和PowerPoint(.pptx)文档。
- [yaml](https://github.com/go-yaml/yaml)：Go语言的YAML支持。

### 数据处理

#### 文本

- [x/text](https://pkg.go.dev/golang.org/x/text)：Go的内置库，用于文本处理，其中许多涉及Unicode。
- [strings](https://pkg.go.dev/strings)：Go的内置包，实现了对UTF-8编码字符串的简单操作函数。

#### 字符编码

- [enconding](https://pkg.go.dev/encoding)：Go内置的库，定义了在其他包之间共享的数据转换接口，用于字节级和文本级表示转换。
- [utf8](https://pkg.go.dev/unicode/utf8)：Go的内置包，实现了对UTF-8编码文本的支持函数和常量。

#### 日期和时间

- [time](https://pkg.go.dev/time)：Go内置的一个包，用于测量和显示时间。
- [goment](https://github.com/nleeper/goment)：一个受[Moment.js](https://momentjs.com/)启发的Go时间库。
- [now](https://github.com/jinzhu/now)：一个Go的时间工具库。
- [carbon](https://github.com/golang-module/carbon)：一个简单、语义化、且对开发者友好的Golang时间处理包。

#### 电话号码

- [phonenumbers](https://github.com/nyaruka/phonenumbers)：一个Google libphonenumber库的Go版本。
- [phonenumber](https://github.com/dongri/phonenumber)：一个库，通过给定国家和电话号码，验证并格式化该号码为E.164标准。

#### Slugs

- [slug](https://github.com/gosimple/slug)：一个支持多语言的URL友好slug生成库。

### 其他

#### 多进程

- [async](https://github.com/StudioSol/async)：一种在发生恐慌时可恢复地异步执行函数的安全方式。还提供一个错误堆栈以帮助发现故障原因。

#### 任务调度

- [gocron](https://github.com/jasonlvhit/gocron)：一个Golang的任务调度包。
- [go-quartz](https://github.com/reugn/go-quartz)：一个极简且零依赖的Golang调度库。
- [cron](https://github.com/robfig/cron)：一个Go的cron库。

## 常用网络爬虫技术栈

### 静态网页

#### HTTP 客户端 + HTML 解析器

- **HTTP 客户端**: net/http, req 或 go-retryablehttp
- **HTML 解析器**: goquery

#### 一体化网络爬取框架

- colly

### 动态网页

#### 一体化浏览器自动化框架

- chromedp, rod 或 playwright-go

## 指南和教程

### 通用指南

- [Go中的网页抓取：完整指南](https://bright.cn/blog/how-tos/web-scraping-go)

### 代理

- [Go 代理服务器 – 用Go设置代理服务器的指南](https://bright.cn/blog/how-tos/go-proxy-servers)

### 比较

- [Go vs. Python - 对比指南](https://bright.cn/blog/web-data/go-vs-python)
