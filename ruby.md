# Ruby 网页抓取

本文档包含用于 Ruby 网页抓取的 gem 和资源列表。

## 目录

- [库](#库)
  - [网络](#网络)
    - [HTTP 客户端](#http-客户端)
    - [WebSockets](#websockets)
    - [低级操作](#低级操作)
    - [其他](#其他)
  - [解析器](#解析器)
    - [HTML 和 XML 解析器](#html-和-xml-解析器)
    - [日期和时间解析器](#日期和时间解析器)
    - [PDF 解析器](#pdf-解析器)
    - [HTTP 解析器](#http-解析器)
    - [URL 解析器](#url-解析器)
    - [电子邮件解析器](#电子邮件解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [SQL 解析器](#sql-解析器)
    - [Office 文件解析器](#office-文件解析器)
    - [其他](#其他-1)
  - [网页抓取](#网页抓取)
    - [框架](#框架)
    - [工具和插件](#工具和插件)
    - [其他](#其他-2)
    - [代理集成](#代理集成)
    - [CAPTCHA 解决](#captcha-解决)
  - [网页自动化](#网页自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
  - [数据导出](#数据导出)
    - [JSON](#json)
    - [CSV](#csv)
    - [其他](#其他-3)
  - [数据处理](#数据处理)
    - [通用](#通用)
    - [字符编码](#字符编码)
    - [价格](#价格)
    - [电话号码](#电话号码)
    - [计量单位](#计量单位)
    - [URL 和网络地址](#url-和网络地址)
    - [语言](#语言)
  - [其他](#其他-4)
    - [多进程](#多进程)
    - [事件处理](#事件处理)
    - [任务调度](#任务调度)
- [常见网页抓取技术栈](#常见网页抓取技术栈)
  - [静态网页](#静态网页)
    - [HTTP 客户端 + HTML 解析器](#http-客户端-html-解析器)
    - [一体化解决方案](#一体化解决方案)
  - [动态网页](#动态网页)
- [指南和教程](#指南和教程)
  - [通用指南](#通用指南)
  - [比较](#比较)

## 库

**注意**：所有选定的 gem 均被广泛使用或积极维护，并与 Ruby 3+ 兼容。

### 网络

#### HTTP 客户端

- [httparty](https://github.com/jnunemaker/httparty)：让 HTTP 再次有趣！
- [HTTP](https://github.com/httprb/http.rb)：一个快速的 Ruby HTTP 客户端，支持链式 API、流处理和超时功能。
- [Typhoeus](https://github.com/typhoeus/typhoeus)：一个封装 [libcurl](https://curl.se/libcurl/) 的 gem，用于快速可靠的请求。
- [excon](https://github.com/excon/excon)：一个简单、快速、实用的 Ruby HTTP 1.1 客户端。
- [nestful](https://github.com/maccman/nestful)：一个简单的 Ruby HTTP/REST 客户端，具有合理的 API。
- [Faraday](https://github.com/lostisland/faraday)：一个简单但灵活的 HTTP 客户端库，支持多种后端。
- [EM-HTTP-Request](https://github.com/igrigorik/em-http-request)：一个异步 HTTP 客户端（基于 EventMachine 和 Ruby）。
- [Http Client](https://github.com/nahi/httpclient)：一个提供类似 libwww-perl (LWP) 功能的 Ruby gem。
- [Http-2](https://github.com/igrigorik/http-2)：一个纯 Ruby 实现的 HTTP/2 协议。
- [Patron](https://github.com/toland/patron)：基于 libcurl 的 Ruby HTTP 客户端。
- [REST Client](https://github.com/rest-client/rest-client)：一个简单的 Ruby HTTP 和 REST 客户端，受微框架语法启发，用于指定操作。
- [Spyke](https://github.com/balvig/spyke)：一个以 ActiveRecord 风格与 REST 服务交互的 gem。

# Ruby 网页抓取

本文档包含用于 Ruby 网页抓取的 gem 和资源列表。

## 目录

- [库](#库)
  - [网络](#网络)
    - [HTTP 客户端](#http-客户端)
    - [WebSockets](#websockets)
    - [低级操作](#低级操作)
    - [其他](#其他)
  - [解析器](#解析器)
    - [HTML 和 XML 解析器](#html-和-xml-解析器)
    - [日期和时间解析器](#日期和时间解析器)
    - [PDF 解析器](#pdf-解析器)
    - [HTTP 解析器](#http-解析器)
    - [URL 解析器](#url-解析器)
    - [电子邮件解析器](#电子邮件解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [SQL 解析器](#sql-解析器)
    - [Office 文件解析器](#office-文件解析器)
    - [其他](#其他-1)
  - [网页抓取](#网页抓取)
    - [框架](#框架)
    - [工具和插件](#工具和插件)
    - [其他](#其他-2)
    - [代理集成](#代理集成)
    - [CAPTCHA 解决](#captcha-解决)
  - [网页自动化](#网页自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
  - [数据导出](#数据导出)
    - [JSON](#json)
    - [CSV](#csv)
    - [其他](#其他-3)
  - [数据处理](#数据处理)
    - [通用](#通用)
    - [字符编码](#字符编码)
    - [价格](#价格)
    - [电话号码](#电话号码)
    - [计量单位](#计量单位)
    - [URL 和网络地址](#url-和网络地址)
    - [语言](#语言)
  - [其他](#其他-4)
    - [多进程](#多进程)
    - [事件处理](#事件处理)
    - [任务调度](#任务调度)
- [常见网页抓取技术栈](#常见网页抓取技术栈)
  - [静态网页](#静态网页)
    - [HTTP 客户端 + HTML 解析器](#http-客户端-html-解析器)
    - [一体化解决方案](#一体化解决方案)
  - [动态网页](#动态网页)
- [指南和教程](#指南和教程)
  - [通用指南](#通用指南)
  - [比较](#比较)

## 库

**注意**：所有选定的 gem 均被广泛使用或积极维护，并与 Ruby 3+ 兼容。

### 网络

#### HTTP 客户端

- [httparty](https://github.com/jnunemaker/httparty)：让 HTTP 再次有趣！
- [HTTP](https://github.com/httprb/http.rb)：一个快速的 Ruby HTTP 客户端，支持链式 API、流处理和超时功能。
- [Typhoeus](https://github.com/typhoeus/typhoeus)：一个封装 [libcurl](https://curl.se/libcurl/) 的 gem，用于快速可靠的请求。
- [excon](https://github.com/excon/excon)：一个简单、快速、实用的 Ruby HTTP 1.1 客户端。
- [nestful](https://github.com/maccman/nestful)：一个简单的 Ruby HTTP/REST 客户端，具有合理的 API。
- [Faraday](https://github.com/lostisland/faraday)：一个简单但灵活的 HTTP 客户端库，支持多种后端。
- [EM-HTTP-Request](https://github.com/igrigorik/em-http-request)：一个异步 HTTP 客户端（基于 EventMachine 和 Ruby）。
- [Http Client](https://github.com/nahi/httpclient)：一个提供类似 libwww-perl (LWP) 功能的 Ruby gem。
- [Http-2](https://github.com/igrigorik/http-2)：一个纯 Ruby 实现的 HTTP/2 协议。
- [Patron](https://github.com/toland/patron)：基于 libcurl 的 Ruby HTTP 客户端。
- [REST Client](https://github.com/rest-client/rest-client)：一个简单的 Ruby HTTP 和 REST 客户端，受微框架语法启发，用于指定操作。
- [Spyke](https://github.com/balvig/spyke)：一个以 ActiveRecord 风格与 REST 服务交互的 gem。


#### Markdown Parsers

- [Redcarpet](https://github.com/vmg/redcarpet)：一个用于 Markdown 处理的 Ruby 库，设计独特，功能强大。

#### SQL 解析器

- [pg_query](https://github.com/pganalyze/pg_query)：一个 Ruby 扩展，用于解析、反解析和标准化 SQL 查询，基于 PostgreSQL 查询解析器。

#### Office 文件解析器

- [Xsv](https://github.com/martijn/xsv)：一个高性能、轻量级的 .xlsx 解析器，仅提供与 CSV 解析器相同的功能。

#### 其他

- [loofah](https://github.com/flavorjones/loofah)：一个用于 HTML/XML 转换和清理的 Ruby 库。
- [HappyMapper](https://github.com/dam5s/happymapper)：一个基于 Nokogiri 的对象到 XML 映射库。
- [Ruby CSS Parser](https://github.com/premailer/css_parser)：一个 Ruby 的 CSS 解析器。
- [Ruby Readability](https://github.com/cantino/ruby-readability)：一个 Ruby gem，用于将文档分解为图像、文本、页面和 PDF。
- [ROXML](https://github.com/Empact/roxml)：一个将 Ruby 类绑定到 XML 的模块。
- [Sitemap Parser](https://github.com/benbalter/sitemap-parser)：一个用于解析符合 Sitemaps.org 标准的网站地图的 gem。
- [RSS](https://github.com/ruby/rss)：RSS 的读取和写入工具。

### Web Scraping

#### 框架

- [Mechanize](https://github.com/sparklemotion/mechanize)：一个 Ruby 库，可以轻松实现自动化网页交互。
- [Wombat](https://github.com/felipecsl/wombat)：一个轻量级的 Ruby 网络爬虫/抓取工具，具有优雅的 DSL，可以从页面中提取结构化数据。
- [Spidr](https://github.com/postmodern/spidr)：一个多功能的 Ruby 网络爬虫库，可爬取站点、多个域名、特定链接或无限链接，速度快且易于使用。
- [Metainspector](https://github.com/jaimeiniesta/metainspector)：一个用于网页抓取的 Ruby gem，可以抓取给定 URL 的标题、元描述、元关键词、链接、图像等。
- [Upton](https://github.com/propublica/upton)：一个包含多种功能的框架，便于进行网页抓取。

#### 工具和插件

- [HTML::Pipeline](https://github.com/jch/html-pipeline)：一个提供 HTML 处理过滤器和实用程序的库。

#### 其他

- [docsplit](http://documentcloud.github.io/docsplit/)：一个命令行工具和 Ruby 库，用于将文档分解为组件部分。

#### 代理集成

- [Bright Data's proxy services](https://brightdata.com/proxy-types)：一个拥有超过 7200 万 IP 的代理网络，提供优质的住宅、数据中心、移动和 ISP 代理服务。支持按国家、州、省、市、ZIP 和 ASN 级别的目标定位，适用于任何 HTTP 客户端或抓取库。[**Bright Data's solution**]

#### CAPTCHA 解决

- [CAPTCHA Solver](https://brightdata.com/products/web-unlocker/captcha-solver)：一个快速、自动化的 CAPTCHA 解决方案，可以解决 reCAPTCHA、hCaptcha、px_captcha、SimpleCaptcha、GeeTest CAPTCHA 等挑战。[**Bright Data's solution**]
- [Ruby 2Captcha API Client](https://github.com/2captcha/2captcha-ruby)：一个 Ruby gem，用于轻松集成 2Captcha 的 API，绕过 reCAPTCHA、hCaptcha、FunCaptcha、GeeTest 等验证码。

### Web Automation

#### 浏览器自动化框架

- [selenium-webdriver](https://github.com/SeleniumHQ/selenium/wiki/Ruby-Bindings)：[Selenium/WebDriver](https://www.selenium.dev/) 的 Ruby 绑定。
- [Watir](https://github.com/watir/watir)：一个 Ruby gem，通过模拟用户与网站的交互来实现自动化测试。
- [playwright-ruby-client](https://github.com/YusukeIwaki/playwright-ruby-client)：[Playwright](https://playwright.dev/) 的 Ruby 客户端。
- [puppeteer-ruby](https://github.com/YusukeIwaki/puppeteer-ruby)：[Puppeteer](https://pptr.dev/) 的 Ruby 移植版本。

### 数据导出

#### JSON

- [JSON:API](https://github.com/jsonapi-serializer/jsonapi-serializer)：一个快速的 JSON:API 序列化工具，适用于 Ruby。
- [Panko](https://github.com/yosiat/panko_serializer)：一个高性能的 JSON 序列化工具，适用于 ActiveRecord 和 Ruby 对象。
- [JSON](https://ruby-doc.org/3.3.5/exts/json/JSON.html)：一个内置的 Ruby 库，用于处理 JSON 数据。
- [oj](https://github.com/ohler55/oj)：一个快速的 JSON 解析器和对象编组器，以 Ruby gem 的形式提供。
#### CSV

- [CSV](https://ruby-doc.org/3.3.5/stdlibs/csv/CSV.html)：Ruby 内置的标准库，用于处理 CSV 文件和数据。
- [SmarterCSV](https://github.com/tilo/smarter_csv)：一个方便读取和写入 CSV 文件的 Ruby gem。

#### 其他

- [HexaPDF](https://github.com/gettalong/hexapdf)：一个多功能的 PDF 创建和操作库，适用于 Ruby。
- [YAML](https://ruby-doc.org/3.3.5/stdlibs/yaml/YAML.html)：Ruby 内置的接口，用于 YAML 格式的数据序列化。
- [docx](https://github.com/ruby-docx/docx)：一个用于与 .docx 文件交互的 Ruby 库/库 gem。

### 数据处理

#### 通用

- [Kiba](https://github.com/thbar/kiba)：Ruby 的数据处理和 ETL 框架。

#### 字符编码

- [Encoding::Converter](https://ruby-doc.org/3.3.5/Encoding/Converter.html)：Ruby 内置的编码转换类。

#### 价格

- [RubyMoney](https://github.com/RubyMoney/money)：一个处理货币和货币转换的 Ruby 库。

#### 电话号码

- [Phonelib](https://github.com/daddyz/phonelib)：基于 Google libphonenumber 数据的电话验证和格式化 Ruby gem。
- [phone](https://github.com/carr/phone)：用于解析、验证和格式化电话号码的 Ruby 库。

#### 度量单位

- [Ruby Units](https://github.com/olbrich/ruby-units)：一个 Ruby 的单位处理库。
- [Unitwise](https://github.com/joshwlewis/unitwise)：用于物理量和单位转换及数学运算的 Ruby 库。

#### URL 和网络地址

- [Bundler::URI](https://ruby-doc.org/3.3.5/stdlibs/bundler/Bundler/URI.html)：Ruby 内置的模块，提供处理统一资源标识符 (RFC2396) 的类。

#### 语言

- [ChinesePinyin](https://github.com/flyerhzm/chinese_pinyin)：一个将汉字转换为拼音的 Ruby gem。

### 其他

#### 多进程

- [Thread](https://ruby-doc.org/3.3.5/Thread.html)：Ruby 内置的并发编程模型实现。
- [Concurrent Ruby](https://github.com/ruby-concurrency/concurrent-ruby)：现代并发工具，包括代理、期货、承诺、线程池、监督者等，灵感来自 Erlang、Clojure、Scala、Go、Java、JavaScript 和经典并发模式。
- [Celluloid](https://github.com/celluloid/celluloid)：一个基于 Actor 模型的 Ruby 并发对象框架。
- [Parallel](https://github.com/grosser/parallel)：一个简化并加快并行处理的 Ruby gem。
- [childprocess](https://github.com/jarib/childprocess)：一个跨平台的 Ruby 库，用于管理子进程。

#### 事件处理

- [EventMachine](https://github.com/eventmachine/eventmachine)：一个快速、简单的事件处理库，适用于 Ruby 程序。

#### 任务调度

- [rufus-scheduler](https://github.com/jmettraux/rufus-scheduler)：一个用于 Ruby 的调度器（支持 at、in、cron 和 every 任务）。

## 流行的网页抓取技术栈

### 静态网页

#### HTTP 客户端 + HTML 解析器

- **HTTP 客户端**：httparty

- **HTML 解析器**：Nokogiri

#### 一体化解决方案

- Mechanize

### 动态网页

- selenium-webdriver、Watir 或 playwright-ruby-client

## 指南和教程

### 通用指南

- [使用 Ruby 进行网页抓取：完整指南 {2024 更新}](https://brightdata.com/blog/how-tos/web-scraping-with-ruby)

### 比较

- [Ruby vs JavaScript：哪个更适合选择？](https://brightdata.com/blog/web-data/ruby-vs-javascript)

- [Playwright vs. Selenium 对比 2024](https://brightdata.com/blog/web-data/playwright-vs-selenium)
