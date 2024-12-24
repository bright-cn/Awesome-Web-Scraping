# Python 网络爬取

本文档包含 Python 中用于网络爬取的库和资源列表。

## 目录

- [库](#库)
  - [网络](#网络)
    - [HTTP 客户端](#http-客户端)
    - [WebSockets](#websockets)
    - [底层网络](#底层网络)
  - [解析器](#解析器)
    - [HTML/XML 解析器](#htmlxml-解析器)
    - [URL 解析器](#url-解析器)
    - [CSV 解析器](#csv-解析器)
    - [文本解析器](#文本解析器)
    - [日期和时间解析器](#日期和时间解析器)
    - [PDF 解析器](#pdf-解析器)
    - [HTTP 解析器](#http-解析器)
    - [邮件解析器](#邮件解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [YAML 解析器](#yaml-解析器)
    - [SQL 解析器](#sql-解析器)
    - [Office 文件解析器](#office-文件解析器)
    - [其他](#其他)
  - [网络爬取](#网络爬取)
    - [框架](#框架)
    - [工具和插件](#工具和插件)
    - [反爬绕过](#反爬绕过)
    - [代理集成](#代理集成)
    - [验证码解决](#验证码解决)
    - [用户代理伪装](#用户代理伪装)
    - [爬虫管理](#爬虫管理)
  - [网络自动化](#网络自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
    - [工具和插件](#工具和插件-1)
    - [其他](#其他-1)
  - [数据导出](#数据导出)
    - [JSON](#json)
    - [CSV](#csv)
    - [其他](#其他-2)
  - [数据处理](#数据处理)
    - [字符编码](#字符编码)
    - [日期和时间](#日期和时间)
    - [价格](#价格)
    - [人名](#人名)
    - [电话号码](#电话号码)
    - [Slugs](#slugs)
    - [URL 和网络地址](#url-和网络地址)
    - [语言](#语言)
  - [其他](#其他-3)
    - [多进程](#多进程)
    - [任务调度](#任务调度)
- [常用网络爬取技术栈](#常用网络爬取技术栈)
  - [静态网页](#静态网页)
  - [动态网页](#动态网页)
- [指南与教程](#指南与教程)
  - [通用指南](#通用指南)
  - [代理相关](#代理相关)
  - [用户代理设置](#用户代理设置)
  - [解析相关](#解析相关)
  - [爬取常用站点](#爬取常用站点)
  - [反爬绕过](#反爬绕过-1)
  - [对比分析](#对比分析)

## 库

**注意**: 所有选择的库都经过维护，并兼容 Python 3+。

### 网络

#### HTTP 客户端

- [requests](https://github.com/kennethreitz/requests): 一个简单而优雅的 HTTP 库。
- [httpx](https://github.com/encode/httpx): 新一代 Python HTTP 客户端。
- [aiohttp](https://github.com/aio-libs/aiohttp): 一个异步 HTTP 客户端/服务器框架，适用于 [asyncio](https://docs.python.org/3/library/asyncio.html) 和 Python。
- [uplink](https://github.com/prkumar/uplink): 一个声明式的 HTTP 客户端。
- [grequests](https://github.com/spyoungtech/grequests): 使用 Gevent 使 HTTP 请求轻松异步化的库。
- [treq](https://github.com/twisted/treq): 基于 Twisted HTTP 客户端构建的 Python 类似 Requests 的 API。
- [pycurl](https://github.com/pycurl/pycurl): [libcurl](http://curl.haxx.se/libcurl/) 的 Python 接口。
- [urllib3](https://github.com/shazow/urllib3): 一个用户友好的 Python HTTP 客户端库。
- [httplib2](https://github.com/httplib2/httplib2): 一个小型且快速的 Python HTTP 客户端库，支持持久连接、缓存和 Google App Engine。
- [urllib](https://docs.python.org/3/library/urllib.html): Python 标准库模块，用于处理网络请求。

#### WebSockets

- [websockets](https://github.com/python-websockets/websockets): 用于构建 Python WebSocket 服务器和客户端的库。
- [websocket-client](https://github.com/websocket-client/websocket-client): 一个 Python WebSocket 客户端。
- [AutobahnPython](https://github.com/tavendo/AutobahnPython): 用于 Twisted 和 asyncio 的 WebSocket 和 WAMP 库。
- [WebSocket-for-Python](https://github.com/Lawouach/WebSocket-for-Python): 一个适用于 Python 2 和 3 以及 PyPy 的 WebSocket 客户端和服务器库 (ws4py 0.5.1)。
- [simple-websocket](https://github.com/miguelgrinberg/simple-websocket): 一个简单的 WebSocket 服务器和客户端。
- [wsproto](https://github.com/python-hyper/wsproto): 一个 Sans-IO WebSocket 协议实现。

#### 底层网络

- [dpkt](https://github.com/kbandla/dpkt): 快速且简单的数据包创建/解析，支持基本 TCP/IP 协议。
- [pyopenssl](https://github.com/pyca/pyopenssl): OpenSSL 库的 Python 包装器。
- [scapy](https://github.com/secdev/scapy): 一个基于 Python 的交互式数据包操作程序和库。
- [impacket](https://github.com/SecureAuthCorp/impacket/): 用于处理网络协议的 Python 类集合。
- [socket](https://docs.python.org/3/library/socket.html): Python 标准库模块，提供 BSD 套接字接口的访问。


### 解析器

#### HTML/XML 解析器

- [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/): 一个用于 HTML 页面数据提取的库 [**[Beautiful Soup 代理集成](https://bright.cn/integration/beautifulsoup)**]
- [lxml](https://github.com/lxml/lxml/): 功能丰富且易于使用的 XML 和 HTML 处理库
- [pyquery](https://github.com/gawel/pyquery): 一个类似 jQuery 的 Python 库，用于对 XML 和 HTML 文档进行查询
- [html5lib](https://github.com/html5lib/html5lib-python): 一个符合标准的库，用于解析和序列化 HTML 文档和片段
- [parsel](https://github.com/scrapy/parsel): 允许使用 XPath 或 CSS 选择器从 XML/HTML 文档中提取数据的库
- [xmltodict](https://github.com/martinblech/xmltodict): 使 XML 的操作像操作 JSON 一样简单的 Python 模块
- [untangle](https://github.com/stchris/untangle): 将 XML 转换为 Python 对象的库
- [selectolax](https://github.com/rushter/selectolax): 使用 Modest 和 Lexbor 引擎的 Python 绑定 (快速 HTML5 解析器，支持 CSS 选择器)
- [html5-parser](https://github.com/kovidgoyal/html5-parser): 一个基于 C 的快速 HTML5 解析库
- [html.parser](https://docs.python.org/3/library/html.parser.html): Python 标准库模块，用于解析 HTML 和 XHTML 格式的文本文件

#### URL 解析器

- [urllib.parse](https://docs.python.org/3/library/urllib.parse.html): 一个 Python 标准库模块，用于解析 URL 的组件
- [furl](https://github.com/gruns/furl): 一个使 URL 解析和操作变得简单的 Python 库
- [purl](https://github.com/codeinthehole/purl): 提供一个简单、不变的 URL 类和干净的 API 用于操作和查询 URL
- [micawber](https://github.com/coleifer/micawber): 一个小型库，用于从 URL 中提取丰富内容

#### CSV 解析器

- [CleverCSV](https://github.com/alan-turing-institute/CleverCSV): 一个用于处理混乱 CSV 文件的 Python 库

#### 文本解析器

- [textract](https://github.com/deanmalmgren/textract): 一个从任意文档中提取文本的库
- [rows](https://github.com/turicas/rows): 提供统一美观的接口来操作表格数据，无论其格式如何

#### 日期和时间解析器

- [dateparser](https://github.com/scrapinghub/dateparser): 一个用于解析人类可读日期的 Python 库
- [ciso8601](https://github.com/closeio/ciso8601): 一个用 C 编写的快速 ISO8601 日期时间解析器

#### PDF 解析器

- [PyPDF2](https://github.com/mstamy2/PyPDF2): 一个纯 Python 实现的 PDF 库，支持拆分、合并、裁剪和转换 PDF 文件的页面
- [pdftables](https://pypi.python.org/pypi/pdftables): 直接从 PDF 文件中提取表格数据
- [PyMuPDF](https://github.com/pymupdf/PyMuPDF): 一个高性能的 Python 库，用于 PDF（以及其他文档）的数据提取、分析、转换和操作


#### HTTP 解析器

- [httptools](https://github.com/MagicStack/httptools): Node.js HTTP 解析器的 Python 绑定
- [http-parser](https://github.com/benoitc/http-parser): 用 C 编写的 Python HTTP 请求/响应解析器

#### 邮件解析器

- [flanker](https://github.com/mailgun/flanker): 一个用于解析电子邮件地址和 MIME 的 Python 库

#### Markdown 解析器

- [Python-Markdown](https://github.com/waylan/Python-Markdown): John Gruber 的 Markdown 的 Python 实现，支持扩展
- [mistune](https://github.com/lepture/mistune): 一个快速且功能强大的 Python Markdown 解析器，支持渲染器和插件
- [python-frontmatter](https://github.com/eyeseast/python-frontmatter): 一个用于解析和管理带有 YAML (或其他) 前置内容的文章的库
- [markdown2](https://github.com/trentm/python-markdown2): 一个快速且完整的 Markdown Python 实现

#### YAML 解析器

- [PyYAML](https://github.com/yaml/pyyaml): 一个功能全面的 Python YAML 处理框架

#### SQL 解析器

- [sqlparse](https://sqlparse.readthedocs.org/): 一个非验证型的 SQL 解析器
- [sqlglot](https://github.com/tobymao/sqlglot): 一个 Python SQL 解析器和转译器

#### Office 文件解析器

- [python-docx](https://github.com/python-openxml/python-docx): 一个用于创建和修改 Word 文档的 Python 库
- [XlsxWriter](https://github.com/jmcnamara/XlsxWriter): 一个用于创建 Excel XLSX 文件的 Python 模块

#### 其他

- [feedparser](https://github.com/kurtmckee/feedparser): 一个用于解析 Atom 和 RSS feed 的库
- [rss-parser](https://github.com/dhvcc/rss-parser): 一个基于 `xmltodict` 和 `pydantic` 的 Python RSS 解析模块
- [reppy](https://github.com/seomoz/reppy): 一个现代化的 robots.txt Python 解析器
- [ultimate-sitemap-parser](https://github.com/GateNLP/ultimate-sitemap-parser): 支持所有站点地图格式的解析器
- [psd-tools](https://github.com/kmike/psd-tools): 一个用于读取 Adobe Photoshop PSD 文件的 Python 库
- [chompjs](https://github.com/Nykakin/chompjs): 一个将 JavaScript 对象解析为 Python 数据结构的库
- [xhtml2pdf](https://github.com/xhtml2pdf/xhtml2pdf): 一个用于将 HTML 转换为 PDF 的库
- [html2text](https://github.com/Alir3z4/html2text): 一个将 HTML 转换为 Markdown 格式文本的库

### 网络爬虫

#### 框架

- [scrapy](https://github.com/scrapy/scrapy): 一个快速且高级的 Python 爬虫和抓取框架 [**[Scrapy 代理集成](https://bright.cn/integration/scrapy)**]
- [autoscraper](https://github.com/alirezamika/autoscraper): 一个智能、自动、快速且轻量级的 Python 爬虫工具
- [requests-html](https://github.com/psf/requests-html): 一个使 HTML 解析（例如网络抓取）尽可能简单直观的库
- [ruia](https://github.com/howie6879/ruia): 一个基于 asyncio 的异步 Python 3.6+ 爬虫微框架
- [gazpacho](https://github.com/maxhumber/gazpacho/): 一个简单、快速、现代的网络爬取库
- [dude](https://github.com/roniemartinez/dude): 一个使用 Python 装饰器编写爬虫的简单框架
- [mechanize](https://github.com/python-mechanize/mechanize): 一个用于自动化与 HTTP Web 服务器交互的库

#### 工具和插件

- [cssselect](https://github.com/scrapy/cssselect): 一个 BSD 许可证的 Python 库，用于解析 CSS3 选择器并将其转换为 XPath 1.0 表达式
- [scrapy-splash](https://github.com/scrapy-plugins/scrapy-splash): 用于 Scrapy 和 Splash 的 JavaScript 集成
- [jusText](https://github.com/miso-belica/jusText): 一个用于从 HTML 页面中移除导航链接、页眉和页脚等模板内容的工具
- [extruct](https://github.com/scrapinghub/extruct): 一个从 HTML 标记中提取嵌入式元数据的库
- [htmldate](https://github.com/adbar/htmldate): 一个快速且健壮的网页日期提取工具
- [lassie](https://github.com/michaelhelmick/lassie): 一个用于检索网站基本内容的 Python 库
- [youtube-dl](http://rg3.github.io/youtube-dl/): 一个命令行工具，用于从 YouTube.com 和其他视频网站下载视频
- [dragnet](https://github.com/dragnet-org/dragnet): 一个网页内容提取工具
- [extractnet](https://github.com/currentsapi/extractnet): Dragnet 的分支，支持从上下文中提取作者、标题、日期、关键字，以及内置的元数据提取

#### 反机器人检测

- [cloudscraper](https://github.com/venomous/cloudscraper): 一个用于绕过 Cloudflare 反机器人页面的 Python 模块
- [curl-impersonate](https://github.com/lwthiker/curl-impersonate): 一个可以模拟 Chrome 和 Firefox 的 curl 特殊构建版本

#### 代理集成

- [Bright Data's proxy services](https://bright.cn/proxy-types): 提供超过 7200 万个 IP 的代理网络，包含住宅、数据中心、移动和 ISP 代理，支持按国家、州、省、市、ZIP 和 ASN 级别目标定位，覆盖 195 个国家。兼容任何 HTTP 客户端或抓取库 [**Bright Data 的解决方案**]

#### CAPTCHA 解决

- [CAPTCHA Solver](https://bright.cn/products/web-unlocker/captcha-solver): 一种快速、自动化的 CAPTCHA 解决工具，可处理 reCAPTCHA、hCaptcha、px_captcha、SimpleCaptcha、GeeTest CAPTCHA 等挑战 [**Bright Data 的解决方案**]
- [captcha_solver](https://github.com/lorien/captcha_solver): 一个通用的 Python CAPTCHA 解决服务 API
- [python-anticaptcha](https://github.com/ad-m/python-anticaptcha): 支持 Anticaptcha.com 的客户端库，用于解决 CAPTCHA
- [unicaps](https://github.com/sergey-scat/unicaps): 一个统一的 Python CAPTCHA 解决服务 API
- [python3-anticaptcha](https://github.com/AndreiDrang/python3-anticaptcha): 一个针对 AntiCaptcha 的 Python 库

#### 用户代理伪装

- [fake-useragent](https://github.com/fake-useragent/fake-useragent): 一个简单的用户代理伪造工具，包含真实世界的用户代理数据库
- [python-user-agents](https://github.com/selwin/python-user-agents): 一个 Python 库，通过解析用户代理字符串，轻松识别移动设备、平板电脑及其功能
- [user_agent](https://github.com/lorien/user_agent): 一个生成 User-Agent 请求头的工具

#### 爬虫管理

- [Gerapy](https://github.com/Gerapy/Gerapy): 一个基于 Scrapy、Scrapyd、Django 和 Vue.js 的分布式爬虫管理框架
- [scrapydweb](https://github.com/my8100/scrapydweb): 一个用于 Scrapyd 集群管理的 Web 应用，支持 Scrapy 日志分析与可视化、自动打包、定时任务、监控与警报、移动端界面等功能

### 网络自动化

#### 浏览器自动化框架

- [selenium](https://github.com/SeleniumHQ/selenium): 一个浏览器自动化框架和生态系统
- [playwright](https://github.com/microsoft/playwright-python): Playwright 测试和自动化库的 Python 版本
- [pyppeteer](https://github.com/pyppeteer/pyppeteer): 一个基于 Chrome/Chromium 的无头浏览器自动化库（[Puppeteer](https://pptr.dev/) 的非官方 Python 移植版）
- [seleniumbase](https://github.com/seleniumbase/SeleniumBase): 一个集成了爬取、抓取、测试和报告功能的 Python 全能框架。支持 pytest，提供隐匿模式（UC Mode），包含许多工具
- [splash](https://github.com/scrapinghub/splash): 一个轻量级的可编写脚本的浏览器，提供 HTTP API
- [crawlee](https://github.com/apify/crawlee-python): 一款 Python 网络爬取和浏览器自动化库，用于构建可靠的爬虫。适合为 AI、LLM、RAG 或 GPTs 提取数据，支持下载 HTML、PDF、JPG、PNG 等文件。兼容 BeautifulSoup、Playwright 和原生 HTTP，支持有头和无头模式，包含代理轮换功能
- [botasaurus](https://github.com/omkarcloud/botasaurus): 一个构建强大爬虫的全能框架
- [splinter](https://github.com/cobrateam/splinter): 一个用于 Web 应用测试的 Python 框架
- [MechanicalSoup](https://github.com/hickford/MechanicalSoup): 一个用于自动化网站交互的 Python 库


#### 工具和插件

- [requestium](https://github.com/tryolabs/requestium): 一个集成 Requests 和 Selenium 的工具，用于自动化网页操作
- [playwright_stealth](https://github.com/AtuboDad/playwright_stealth): [puppeteer-extra-plugin-stealth](https://github.com/berstend/puppeteer-extra/tree/master/packages/puppeteer-extra-plugin-stealth) 插件的 Python 移植版本
- [pyppeteerstealth](https://github.com/dgtlmoon/pyppeteerstealth): Pyppeteer 的隐身插件，用于模拟普通浏览器行为

#### 其他

- [ninjemail](https://github.com/david96182/ninjemail): 一个用于自动创建电子邮件账户的 Python 库，支持主流电子邮件服务商，轻松创建多个账户

### 数据导出

#### JSON

- [json](https://docs.python.org/3/library/json.html): Python 标准库模块，用于编码和解码 JSON 数据
- [orjson](https://github.com/ijl/orjson): 一款快速、准确的 Python JSON 库，支持数据类、日期时间和 [NumPY](https://numpy.org/)
- [ujson](https://github.com/esnme/ultrajson): 一个用 C 编写的超快 JSON 编解码器，提供 Python 绑定

#### CSV

- [csv](https://docs.python.org/3/library/csv.html): Python 标准库模块，用于读取和写入 CSV 文件

#### 其他

- [msgspec](https://github.com/jcrist/msgspec): 一个快速的序列化和验证库，内置支持 JSON、MessagePack、YAML 和 TOML
- [msgpack](https://github.com/msgpack/msgpack-python): MessagePack 的 Python 序列化实现

### 数据处理

#### 字符编码

- [ftfy](https://github.com/LuminosoInsight/python-ftfy): 一个修复 Unicode 文本中乱码和其他问题的库
- [unidecode](https://pypi.python.org/pypi/Unidecode): 用于将 Unicode 文本转为 ASCII 的工具
- [chardet](https://github.com/chardet/chardet): 一个 Python 字符编码检测工具
- [cchardet](https://github.com/PyYoshi/cChardet): 一个通用的字符编码检测工具

#### 日期与时间

- [datetime](https://docs.python.org/3/library/datetime.html): Python 标准库模块，用于操作日期和时间
- [dateutil](https://github.com/dateutil/dateutil): 一个为 Python 标准日期时间功能提供有用扩展的库

#### 价格

- [price-parser](https://github.com/scrapinghub/price-parser): 一个从原始文本字符串中提取价格和货币符号的库

#### 人名

- [python-nameparser](https://github.com/derek73/python-nameparser): 一个简单的 Python 模块，用于将人名解析为各个组成部分

#### 电话号码

- [phonenumbers](https://github.com/daviddrysdale/python-phonenumbers): Google [libphonenumber](https://github.com/google/libphonenumber) 的 Python 移植版

#### Slugs

- [python-slugify](https://github.com/un33k/python-slugify): 一个生成 Unicode slugs 的 Python 库

#### URLs 和网络地址

- [netaddr](https://github.com/drkjam/netaddr): 一个用于网络地址操作的 Python 库
- [tldextract](https://github.com/john-kurkowski/tldextract): 一个库，可准确分离 URL 的子域、域名和公共后缀，基于公共后缀列表 (PSL)

#### 语言

- [xpinyin](https://github.com/lxneng/xpinyin): 一个将中文汉字转换为拼音的库
- [pytils](https://github.com/j2a/pytils): 一个提供俄语特定字符串工具的库

### 其他

#### 多线程处理

- [threading](http://docs.python.org/3/library/threading.html): Python 标准库模块，用于基于线程的并行处理
- [multiprocessing](http://docs.python.org/3/library/multiprocessing.html): Python 标准库模块，用于基于进程的并行处理
- [concurrent-futures](https://docs.python.org/3/library/concurrent.futures.html): Python 标准库模块，提供异步执行调用对象的高级接口

#### 任务调度

- [apscheduler](https://github.com/agronholm/apscheduler): 一个用于任务调度的 Python 库
- [python-crontab](https://gitlab.com/doctormo/python-crontab): 一个用于读取和写入 crontab 文件并通过直接 API 简化系统 cron 访问的模块


## 流行的网页抓取技术栈

### 静态网页

#### HTTP 客户端 + HTML 解析器

- **HTTP 客户端**: requests、HTTPX、AIOHTTP 或 urllib3
- **HTML 解析器**: Beautiful Soup 或 lxml

#### 一体化网页抓取框架

- Scrapy 或 requests-html

### 动态网页

#### 一体化浏览器自动化框架

- Selenium、Playwright 或 pyppeteer

#### 网页抓取框架 + JavaScript 引擎

- **网页抓取框架**: Scrapy  
- **JavaScript 引擎**: scrapy-splash

## 指南和教程

### 通用指南

- [Python 网页抓取 – 2024 完整指南](https://bright.cn/blog/how-tos/web-scraping-with-python)
- [使用 Python 抓取动态网站 - 2024 指南](https://bright.cn/blog/how-tos/scrape-dynamic-websites-python)
- [Python 网页爬取 - 2024 指南](https://bright.cn/blog/how-tos/web-crawling-with-python)
- [掌握 Python HTTP 请求：2024 高级指南](https://bright.cn/blog/web-data/python-requests-guide)
- [BeautifulSoup 网页抓取：分步教程](https://bright.cn/blog/how-tos/beautiful-soup-web-scraping)
- [使用 Selenium 抓取网页指南（2024）](https://bright.cn/blog/how-tos/using-selenium-for-web-scraping)
- [如何使用 lxml 抓取网页](https://bright.cn/blog/web-data/lxml-web-scraping)
- [Python 与 cURL 集成指南](https://bright.cn/blog/how-tos/curl-with-python)
- [使用 Python 和 Wget 下载网页](https://bright.cn/blog/how-tos/wget-with-python)
- [用 Python 抓取网站图片 - 2024 指南](https://bright.cn/blog/how-tos/scrape-images-from-websites)

### 代理

- [Python 代理服务器是什么？](https://bright.cn/blog/proxy-101/python-proxy-server)
- [在 Python Requests 中使用代理的指南](https://bright.cn/blog/proxy-101/proxy-with-python-requests)
- [如何在 AIOHTTP 中设置代理](https://bright.cn/blog/how-tos/proxy-in-aiohttp)

### 用户代理设置

- [Python Requests 用户代理指南：设置与更改](https://bright.cn/blog/web-data/requests-user-agent)

### 数据解析

- [最佳 5 个 Python HTML 解析器](https://bright.cn/blog/web-data/best-python-html-parsers)
- [最佳 Python HTTP 客户端用于网页抓取](https://bright.cn/blog/web-data/best-python-http-clients)
- [如何解析 JSON 数据（Python 教程）](https://bright.cn/blog/how-tos/parse-json-data-with-python)
- [如何解析 XML 数据？多种方法详解](https://bright.cn/blog/how-tos/parsing-xml-in-python)

### 抓取热门网站

- [抓取 Google 搜索的终极指南 (Python)](https://bright.cn/blog/web-data/scraping-google-with-python)
- [如何用 Python 抓取 YouTube](https://bright.cn/blog/how-tos/how-to-scrape-youtube-in-python)
- [抓取 LinkedIn 数据 - 2024 指南](https://bright.cn/blog/how-tos/linkedin-scraping-guide)
- [如何抓取 Airbnb 数据 - 2024 指南](https://bright.cn/blog/how-tos/how-to-scrape-airbnb-guide)
- [抓取 Yelp 数据的分步指南 (Python)](https://bright.cn/blog/how-tos/how-to-scrape-yelp-guide)
- [如何抓取 Yahoo Finance 数据 - 2024 指南](https://bright.cn/blog/how-tos/scrape-yahoo-finance-guide)
- [抓取 Craigslist 数据的分步指南 (Python)](https://bright.cn/blog/how-tos/how-to-scrape-craigslist-in-python)
- [如何抓取 GitHub 仓库](https://bright.cn/blog/how-tos/how-to-scrape-github-repositories-in-python)
- [如何抓取 Amazon 数据 - 2024 指南](https://bright.cn/blog/how-tos/how-to-scrape-amazon)
- [抓取 Reddit 数据的指南 (Python)](https://bright.cn/blog/web-data/how-to-scrape-reddit-python)
- [抓取 Glassdoor 数据的分步指南（2024）](https://bright.cn/blog/web-data/how-to-scrape-glassdoor)
- [如何构建 Zalando 抓取器](https://bright.cn/blog/how-tos/how-to-build-a-zalando-scraper-with-python)
- [用 Python 抓取 eBay 数据进行价格监控](https://bright.cn/blog/how-tos/how-to-scrape-ebay-in-python)

### 绕过反爬虫

- [使用 Python 绕过 CAPTCHA 技术（2024）](https://bright.cn/blog/web-data/bypass-captchas-with-python)
- [使用 cURL Impersonate 进行网页抓取](https://bright.cn/blog/web-data/web-scraping-with-curl-impersonate)
- [用 Selenium 绕过 CAPTCHA 的指南（Python）](https://bright.cn/blog/web-data/bypass-captchas-with-selenium)
- [通过 Playwright Stealth 避免机器人检测](https://bright.cn/blog/how-tos/avoid-bot-detection-with-playwright-stealth)

### 对比

- [JavaScript 与 Python 的网页抓取对比](https://bright.cn/blog/web-data/javascript-vs-python)
- [Java 与 Python - 对比指南](https://bright.cn/blog/web-data/java-vs-python)
- [C# 与 Python 的网页抓取对比](https://bright.cn/blog/how-tos/c-sharp-vs-python-for-web-scraping)
- [Go 与 Python - 对比指南](https://bright.cn/blog/web-data/go-vs-python)
- [Python 与 C++ 网页抓取对比](https://bright.cn/blog/web-data/python-vs-c-plus-plus-for-web-scraping)
- [Scrapy 与 Beautiful Soup：详细对比](https://bright.cn/blog/web-data/scrapy-vs-beautiful-soup)
- [Scrapy 与 Selenium：如何选择？](https://bright.cn/blog/web-data/scrapy-vs-selenium)
- [Scrapy 与 Puppeteer 网页抓取对比](https://bright.cn/blog/web-data/scrapy-vs-puppeteer)
