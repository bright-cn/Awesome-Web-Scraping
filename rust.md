# Rust 网络爬虫

本文档包含在 Rust 中用于网络爬虫的库和资源列表。

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
    - [HTTP 解析器](#http-解析器)
    - [CSV 解析器](#csv-解析器)
    - [PDF 解析器](#pdf-解析器)
    - [Email 解析器](#email-解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [YAML 解析器](#yaml-解析器)
    - [SQL 解析器](#sql-解析器)
    - [Office 文件解析器](#office-文件解析器)
    - [其他](#其他-1)
  - [网络爬虫](#网络爬虫)
    - [框架](#框架)
    - [代理集成](#代理集成)
    - [CAPTCHA 解决](#captcha-解决)
  - [网络自动化](#网络自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
    - [工具和插件](#工具和插件)
  - [数据处理](#数据处理)
  - [序列化](#序列化)
    - [字符编码](#字符编码)
    - [文本](#文本)
    - [日期和时间](#日期和时间)
    - [电话号码](#电话号码)
    - [人名解析](#人名解析)
    - [Slug 生成](#slug-生成)
  - [其他](#其他-2)
    - [多进程](#多进程)
    - [任务调度](#任务调度)
- [常用爬虫技术栈](#常用爬虫技术栈)
  - [静态网页](#静态网页)
    - [HTTP 客户端 + HTML 解析器](#http-客户端--html-解析器)
    - [一体化爬虫框架](#一体化爬虫框架)
  - [动态网页](#动态网页)
    - [一体化浏览器自动化框架](#一体化浏览器自动化框架)
- [指南和教程](#指南和教程)
  - [通用指南](#通用指南)
  - [代理](#代理)
  - [对比](#对比)

## 库

**注意**: 所有选择的库都是广泛使用或正在积极维护的。

### 网络

#### HTTP 客户端

- [reqwest](https://github.com/seanmonstar/reqwest): 一个优雅、功能齐全的 HTTP 客户端库。
- [ureq](https://github.com/algesten/ureq): 一个简单、安全的 HTTP 客户端。
- [curl-rust](https://github.com/alexcrichton/curl-rust): [libcurl](https://curl.se/libcurl/) 的 Rust 绑定。
- [attohttpc](https://github.com/sbstp/attohttpc): 一个轻量级的 Rust HTTP 1.1 客户端。
- [actix-web](https://github.com/actix/actix-web): 一个强大、实用且极快的 Rust 网络框架。
- [isahc](https://github.com/sagebind/isahc): 一个有趣且实用的 HTTP 客户端。

#### WebSockets

- [rust-websocket](https://github.com/websockets-rs/rust-websocket): 一个用 Rust 编写的 WebSocket（RFC6455）库。
- [tungstenite-rs](https://github.com/snapview/tungstenite-rs): 一个轻量级、基于流的 WebSocket 实现。
- [websocket.rs](https://github.com/nurmohammed840/websocket.rs): 一个支持客户端和服务器的 WebSocket 实现。

#### 底层网络

- [hyper](https://github.com/hyperium/hyper): 一个低级、高效的 HTTP 库，适合作为其他库和应用程序的基础。
- [tiny-http](https://github.com/tiny-http/tiny-http): 一个低级 HTTP 服务器库。
- [libpnet](https://github.com/libpnet/libpnet): 一个用于跨平台低级网络操作的 Rust 库。
- [pcap](https://github.com/rust-pcap/pcap): 一个用于访问 libpcap 抓包功能的 Rust 库。
- [rustls](https://github.com/rustls/rustls): 一个现代的 Rust TLS 库。


#### 其他

- [hyper-util](https://github.com/hyperium/hyper-util): 一组用于处理 hyper 常见任务的实用工具集合。
- [reqwest-middleware](https://github.com/TrueLayer/reqwest-middleware): 一个封装 reqwest 的库，支持客户端中间件链。

### 解析器

#### HTML/XML 解析器

- [scraper](https://github.com/rust-scraper/scraper): 支持使用 CSS 选择器进行 HTML 解析和查询的库。
- [html5ever](https://github.com/servo/html5ever): 高性能、浏览器级的 HTML5 解析器。
- [select.rs](https://github.com/utkarshkukreti/select.rs): 一个适合用于网络爬虫的 Rust 库，用于从 HTML 文档中提取有用数据。
- [quick-xml](https://github.com/tafia/quick-xml): 一个高性能的 XML 读写库。
- [roxmltree](roxmltree): 一个用于将 XML 文档表示为只读树的 Rust crate。

#### URL 解析器

- [rust-url](https://github.com/servo/rust-url): 一个用于 Rust 的 URL 解析器。

#### HTTP 解析器

- [httparse](https://github.com/seanmonstar/httparse): 一个用于 Rust 的 HTTP 1.x 协议的推送解析器。

#### CSV 解析器

- [rust-csv](https://github.com/BurntSushi/rust-csv): 一个支持 [Serde](https://serde.rs/) 的 Rust CSV 解析器。

#### PDF 解析器

- [pdf-extract](https://github.com/jrmuizel/pdf-extract): 用于从 PDF 中提取内容的 Rust 库。

#### Email 解析器

- [mailparse](https://github.com/staktrace/mailparse): 一个用于解析邮件文件的 Rust 库。

#### Markdown 解析器

- [pulldown-cmark](https://github.com/pulldown-cmark/pulldown-cmark): 一个高效、可靠的 [CommonMark](https://commonmark.org/) 标准 Markdown 解析器。
- [markdown-rs](https://github.com/wooorm/markdown-rs): 一个支持 AST 和扩展的 Rust CommonMark 兼容 Markdown 解析器。

#### YAML 解析器

- [yaml-rust](https://github.com/chyh1990/yaml-rust): 一个纯 Rust 的 YAML 实现。

#### SQL 解析器

- [datafusion-sqlparser-rs](https://github.com/apache/datafusion-sqlparser-rs): 一个可扩展的 Rust SQL 词法分析器和解析器。

#### Office 文件解析器

- [calamine](https://github.com/tafia/calamine): 一个纯 Rust 的 Excel/OpenDocument 表格文件读取器。

#### 其他

- [pest](https://github.com/pest-parser/pest): 一个通用解析器，专注于易用性、正确性和性能。
- [rust-cssparser](https://github.com/servo/rust-cssparser): CSS 语法第 3 级的 Rust 实现。
- [ammonia](https://github.com/rust-ammonia/ammonia): 用于修复和保护不受信任 HTML 的 crate。
- [ttf-parser](https://github.com/RazrFalcon/ttf-parser): 一个高层次、安全、零分配的 TrueType 字体解析器。
- [robotstxt](https://github.com/Folyd/robotstxt): 谷歌 robots.txt 解析器和匹配器 C++ 库的 Rust 原生移植。
- [rss](https://github.com/rust-syndication/rss): 一个用于 RSS 网络内容订阅格式序列化的库。
- [collie](https://github.com/collie-reader/collie): 一个极简的 RSS 阅读器。

### 网络爬虫

#### 框架

- [spider](https://github.com/spider-rs/spider): 一个用于 Rust 的网络爬虫和爬取框架。
- [dyer](https://github.com/hominee/dyer): 一个设计为可靠、灵活且快速的 Rust 网络爬虫 crate，提供高层次全面功能的同时保持速度。

#### 代理集成

- [Bright Data 的代理服务](https://brightdata.com/proxy-types): 一个拥有超过 7200 万 IP 的代理网络，提供高质量的住宅、数据中心、移动和 ISP 代理服务。支持按州、国家、邮政编码和 ASN 定位，覆盖 195 个国家，与任何 HTTP 客户端或爬虫库兼容 [**Bright Data 的解决方案**]。

#### CAPTCHA 解决方案

- [CAPTCHA Solver](https://brightdata.com/products/web-unlocker/captcha-solver): 一个快速、自动化的 CAPTCHA 解决方案，可处理 reCAPTCHA、hCaptcha、px_captcha、SimpleCaptcha、GeeTest CAPTCHA 等 [**Bright Data 的解决方案**]。
- [challenge-bypass-ristretto](https://github.com/brave-intl/challenge-bypass-ristretto): 使用 [Ristretto group](https://ristretto.group/) 实现隐私通行密码学协议的 Rust 实现。

### 网络自动化

#### 浏览器自动化框架

- [rust-headless-chrome](https://github.com/rust-headless-chrome/rust-headless-chrome): 一个高层次 API，用于通过 DevTools 协议控制无头 Chrome 或 Chromium，是 [Puppeteer](https://pptr.dev/) 的 Rust 等效实现。
- [thirtyfour](https://github.com/Vrtgs/thirtyfour): 一个 Rust Selenium WebDriver 客户端，用于网站的自动化测试。
- [chromiumoxide](https://github.com/mattsse/chromiumoxide): 一个 Rust crate，提供通过 [DevTools Protocol](https://chromedevtools.github.io/devtools-protocol/) 控制 Chrome 或 Chromium 的高层次异步 API。
- [playwright-rust](https://github.com/octaltree/playwright-rust): 一个 [Playwright](https://playwright.dev/) 的 Rust 移植。


#### 工具和插件

- [webdriver-downloader](https://github.com/ik1ne/webdriver-downloader): 一个用于下载 WebDriver 的 CLI 接口和库。

### 数据处理

### 序列化

- [serde](https://github.com/serde-rs/serde): 一个用于 Rust 的序列化框架。

#### 字符编码

- [rust-base64](https://github.com/marshallpierce/rust-base64): 一个用于以字节或 UTF-8 形式编码和解码 Base64 的 Rust crate。
- [encoding_rs](https://github.com/hsivonen/encoding_rs): 基于 Gecko 的 Rust 编码标准实现 [Encoding Standard](https://encoding.spec.whatwg.org/)。

#### 文本处理

- [rust-lexical](https://github.com/Alexhuszagh/rust-lexical): 一个提供快速数字字符串转换功能的 Rust crate。

#### 日期和时间

- [chrono](https://github.com/chronotope/chrono): 一个用于 Rust 的日期和时间库。
- [time](https://github.com/time-rs/time): Rust 中最常用的日期和时间处理库。
- [httpdate](https://github.com/pyfisch/httpdate): 用于 HTTP 日期解析和格式化的库。

#### 电话号码

- [rust-phonenumber](https://github.com/whisperfish/rust-phonenumber): 一个用于解析、格式化和验证国际电话号码的库。

#### 人名

- [human-name](https://github.com/djudd/human-name): 一个用于解析和比较人名的 Rust 库。

#### Slugs

- [slug-rs](https://github.com/Stebalien/slug-rs): 一个用于从 Unicode 字符串生成 ASCII slugs 的小型库。

### 其他

#### 多线程处理

- [tokio](https://github.com/tokio-rs/tokio): 一个用于使用 Rust 编写可靠异步应用程序的运行时，提供 I/O、网络、调度、计时器等功能。
- [rayon](https://github.com/rayon-rs/rayon): 一个用于 Rust 的数据并行库。
- [async-task](https://github.com/smol-rs/async-task): 一个用于构建执行器的任务抽象。

#### 任务调度

- [clokwerk](https://github.com/mdsherry/clokwerk): 一个简单的 Rust 调度器。

## 流行的网络爬虫技术栈

### 静态网页

#### HTTP 客户端 + HTML 解析器

- **HTTP 客户端**: reqwest, ureq, curl-rust
- **HTML 解析器**: scraper, html5ever, select.rs 或 quick-xml

#### 一体化网络爬虫框架

- spider

### 动态网页

#### 一体化浏览器自动化框架

- rust-headless-chrome, thirtyfour 或 chromiumoxide

## 指南和教程

### 通用指南

- [使用 Rust 进行网络爬虫](https://brightdata.com/blog/how-tos/web-scraping-with-rust)

### 代理

- [Rust 代理服务器：如何在 Rust 中设置代理](https://brightdata.com/blog/how-tos/rust-proxy-servers)

### 比较

- [JavaScript 与 Rust：哪个更适合网络爬虫](https://brightdata.com/blog/web-data/javascript-vs-rust-web-scraping)
