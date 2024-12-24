# PHP 网络爬取

本文档列出了用于 PHP 网络爬取的库和资源。

## 目录

- [库](#库)
  - [网络](#网络)
    - [HTTP 客户端](#http-客户端)
    - [WebSocket](#websocket)
  - [解析器](#解析器)
    - [HTML 和 XML 解析器](#html-和-xml-解析器)
    - [CSV 解析器](#csv-解析器)
    - [JSON 解析器](#json-解析器)
    - [PDF 解析器](#pdf-解析器)
    - [电子邮件解析器](#电子邮件解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [YAML 解析器](#yaml-解析器)
    - [SQL 解析器](#sql-解析器)
    - [Office 文件解析器](#office-文件解析器)
    - [其他解析器](#其他解析器)
  - [网络爬取](#网络爬取)
    - [框架](#框架)
    - [代理集成](#代理集成)
    - [验证码解决方案](#验证码解决方案)
  - [网络自动化](#网络自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
  - [数据导出](#数据导出)
    - [JSON](#json)
    - [CSV](#csv)
    - [其他导出](#其他导出)
  - [数据处理](#数据处理)
    - [通用](#通用)
    - [字符编码](#字符编码)
    - [日期和时间](#日期和时间)
    - [价格处理](#价格处理)
    - [电话号码](#电话号码)
    - [单位转换](#单位转换)
    - [Slugs](#slugs)
    - [URL 和网络地址](#url-和网络地址)
  - [其他功能](#其他功能)
    - [多进程](#多进程)
    - [事件处理](#事件处理)
    - [软件自动化管理](#软件自动化管理)
    - [任务调度](#任务调度)
- [常用网络爬取技术栈](#常用网络爬取技术栈)
  - [静态网页](#静态网页)
    - [HTTP 客户端 + HTML 解析器](#http-客户端-html-解析器)
    - [一体化解决方案](#一体化解决方案)
  - [动态网页](#动态网页)
- [指南和教程](#指南和教程)
  - [通用指南](#通用指南)
  - [代理设置](#代理设置)
  - [HTTP 客户端教程](#http-客户端教程)

## 库

**注**：所有列出的库均为活跃维护或广泛使用的资源。

### 网络

#### HTTP 客户端

- **[PHP cURL](https://www.php.net/manual/en/book.curl.php)**: 内置 PHP 库，基于 [libcurl](https://curl.se/libcurl/)，支持与各种协议的服务器通信。
- **[Guzzle](https://github.com/guzzle/guzzle)**: 功能强大的 PHP HTTP 客户端，轻松发送请求并集成 Web 服务。[**[Guzzle 代理集成教程](https://brightdata.com/blog/how-tos/proxy-with-guzzle)**]
- **[HttpClient](https://github.com/symfony/http-client)**: Symfony 的低级 HTTP 客户端组件。
- **[Buzz](https://github.com/kriswallsmith/Buzz)**: 轻量级 PHP HTTP 客户端，代码量少于 1000 行。
- **[amphp/http-client](https://github.com/amphp/http-client)**: 高级异步 HTTP 客户端库，支持并发请求。
- **[Requests](https://github.com/rmccue/Requests)**: 简单易用的 HTTP 请求库，用于与其他站点交互。
- **[HTTPFul](https://github.com/nategood/httpful)**: REST 友好型 PHP HTTP 客户端，支持 PHP 流包装器和 cURL。

#### WebSocket

- **[Sockets](https://www.php.net/manual/en/intro.sockets.php)**: 内置 PHP 扩展，支持低级别的套接字通信功能。
- **[Ratchet](https://github.com/ratchetphp/Ratchet)**: 异步 WebSocket 服务库。
- **[Pawl](https://github.com/ratchetphp/Pawl)**: 异步 WebSocket 客户端库。

### 解析器

#### HTML 和 XML 解析器

- [Simple Html Dom Parser for PHP](https://github.com/voku/simple_html_dom): 一个现代化且简单的 PHP HTML DOM 解析器。
- [HTML5-PHP](https://github.com/Masterminds/html5-php): PHP 的 HTML5 解析器和序列化工具。
- [DiDOM](https://github.com/Imangazaliev/DiDOM): 一个简单快速的 HTML 和 XML 解析器。
- [QueryPath](https://github.com/GravityPDF/querypath): 支持 PHP 8.3 的 HTML(5)/XML 查询库，支持 CSS 4 和 XPath。
- [DomCrawler](https://github.com/symfony/dom-crawler): Symfony 组件，用于轻松浏览 HTML 和 XML 文档的 DOM。
- [PHP Html Parser](https://github.com/paquettg/php-html-parser): 一个支持操作 HTML DOM 的解析器，类似 jQuery 的选择器功能。
- [DOM](https://www.php.net/manual/en/intro.dom.php): PHP 内置扩展，允许通过 DOM API 操作 XML 和 HTML 文档。
- [XML Document Parser PHP](https://github.com/laravie/parser): 一个框架无关的库，提供将 XML 解析为数组的简单方式。

#### CSV 解析器

- [ParseCsv](https://github.com/parsecsv/parsecsv-for-php): PHP 的 CSV 数据解析器。

#### JSON 解析器

- [JSON Parser](https://github.com/cerbero90/json-parser): 一个轻量、依赖少的 JSON 解析器，可以高效处理大规模 JSON 数据。
- [JsonMachine](https://github.com/halaxa/json-machine): 高效且易用的 PHP JSON 流式解析器。

#### PDF 解析器

- [PdfParser](https://github.com/smalot/pdfparser): 一个独立的 PHP 库，提供多种工具从 PDF 文件中提取数据。

#### 电子邮件解析器

- [EmailReplyParser](https://github.com/willdurand/EmailReplyParser): 一个用于解析纯文本电子邮件内容的 PHP 库。

#### Markdown 解析器

- [CommonMark PHP](https://github.com/thephpleague/commonmark): 一个高度可扩展的 PHP Markdown 解析器，完全支持 CommonMark 和 GFM 规范。
- [PHP Markdown](https://github.com/michelf/php-markdown): 基于 Markdown.pl 的 Markdown 和 Markdown Extra 解析器。
- [Parsedown](https://github.com/erusev/parsedown): 一个更好的 PHP Markdown 解析器。

#### YAML 解析器

- [Dallgoot: YAML library for PHP](https://github.com/dallgoot/yaml): PHP 的 YAML 文件加载和解析库。

#### SQL 解析器

- [PHP-SQL-Parser](https://github.com/greenlion/PHP-SQL-Parser): 一个专注于 MySQL 方言的纯 PHP SQL 解析器。
- [SQL Parser](https://github.com/phpmyadmin/sql-parser): 一个验证 SQL 的词法分析器和解析器，专注于 MySQL 方言。

#### Office 文件解析器

- [SimpleXLSX](https://github.com/shuchkin/simplexlsx): 一个 PHP 库，用于解析和读取 Excel XLSX 文件。

#### 其他解析器

- [PHP Domain Parser](https://github.com/jeremykendall/php-domain-parser): 基于公共后缀列表的 PHP 域名解析库。
- [RSS & Atom Feeds for PHP](https://github.com/dg/rss-php): 一个小型易用的 RSS 和 Atom 提要库。
- [PHP CSS Parser](https://github.com/MyIntervals/PHP-CSS-Parser): 用于解析和提取 CSS 数据的 PHP 库。
- [SitemapParser](https://github.com/VIPnytt/SitemapParser): 符合 Sitemaps.org 协议的 XML 站点地图解析器。
- [robots-txt-parser](https://github.com/bopoda/robots-txt-parser): 一个 PHP 类，用于解析 robots.txt 文件中所有的指令。

### 网络爬取

#### 框架

- [Crawler](https://github.com/crwlrsoft/crawler): 快速开发网络爬虫和抓取工具的库。
- [Roach](https://github.com/roach-php/core): 完整的 PHP 网络爬取工具包。
- [PHP-Spider](https://github.com/mvdbos/php-spider): 可配置和扩展的 PHP 网络爬虫。
- [Embed](https://github.com/oscarotero/Embed): 一个 PHP 库，用于从任意网页或服务中获取信息。
- [PHPScraper](https://github.com/spekulatius/phpscraper): 一个多功能 PHP 网络工具。

#### 代理集成

- [Bright Data's proxy services](https://brightdata.com/proxy-types): 提供超过 7200 万个 IP 的代理网络，包括住宅、数据中心、移动和 ISP 代理，支持按国家、州、ZIP 和 ASN 级别的定位。[**Bright Data 的解决方案**]

 
#### CAPTCHA 解决方案

- [CAPTCHA Solver](https://brightdata.com/products/web-unlocker/captcha-solver): 一种快速自动的 CAPTCHA 解决方案，可破解 reCAPTCHA、hCaptcha、px_captcha、SimpleCaptcha、GeeTest CAPTCHA 等。[**Bright Data 解决方案**]
- [PHP Module for 2Captcha API](https://github.com/2captcha/2captcha-php): 一个 PHP 包，用于轻松集成 2captcha 的 API，绕过 recaptcha、hcaptcha、funcaptcha、geetest 等验证码。
- [captcha-solver-php](https://github.com/metabypass/captcha-solver-php): 基于 PHP 的易用实现，适用于解决各种验证码，提供 Metabypass 支持。

### 网络自动化

#### 浏览器自动化框架

- [Panther](https://github.com/symfony/panther): 一个用于 PHP 和 Symfony 的浏览器测试和网络爬取库。
- [php-webdriver](https://github.com/facebook/php-webdriver): Selenium/WebDriver 协议的 PHP 客户端。
- [chrome-php/chrome](https://github.com/chrome-php/chrome): 一个用于在 PHP 中操作无头 Chrome/Chromium 的库。
- [Mink](https://github.com/minkphp/Mink): PHP 的网络浏览器模拟器抽象库。

### 数据导出

#### JSON

- [PHP JSON library](https://github.com/josantonius/php-json): 一个用于管理 JSON 文件的简单 PHP 库。

#### CSV

- [CSV](https://github.com/thephpleague/csv): 一个用于简化 CSV 解析、写入和过滤的 PHP 库。

#### 其他

- [mPDF](https://github.com/mpdf/mpdf): 一个用于从 UTF-8 编码的 HTML 生成 PDF 文件的 PHP 库。
- [PhpSpreadsheet](https://github.com/PHPOffice/PhpSpreadsheet): 一个纯 PHP 库，用于读取和写入电子表格文件。
- [PHPWord](https://github.com/PHPOffice/PHPWord): 一个用于读写文字处理文档的纯 PHP 库。
- [PHPPowerPoint](https://github.com/PHPOffice/PHPPowerPoint): 一个用于读写演示文稿文档的纯 PHP 库。

### 数据处理

#### 通用

- [Stringy](https://github.com/danielstjules/Stringy): 一个支持多字节的 PHP 字符串操作库。

#### 字符编码

- [ANSI to HTML5](https://github.com/sensiolabs/ansi-to-html): 一个 ANSI 到 HTML5 的转换器。

#### 日期和时间

- [Brick\DateTime](https://github.com/brick/date-time): 一个用于处理日期和时间的 PHP 库。

#### 价格

- [Brick\Money](https://github.com/brick/money): 一个用于处理货币和金额的 PHP 库。
- [PHP Prices](https://github.com/whitecube/php-prices): 一个用于复杂货币价格管理的简单 PHP 库。

#### 电话号码

- [LibPhoneNumber for PHP](https://github.com/giggsey/libphonenumber-for-php): Google's phone number library 的 PHP 版本。
- [Brick\PhoneNumber](https://github.com/brick/phonenumber): 一个用于处理电话号码的 PHP 库。

#### 度量单位

- [PhpUnitsOfMeasure](https://github.com/PhpUnitsOfMeasure/php-units-of-measure): 一个用于处理物理量及其单位的 PHP 库。

#### Slugs

- [Urlify](https://github.com/jbroadway/urlify): 一个快速的 PHP Slug 生成和转译库，可将非 ASCII 字符转换为 URL 使用。
- [Slugify](https://github.com/cocur/slugify): 一个 PHP 库，将字符串转换为 Slug。支持 Symfony、Silex、Laravel 等多种集成。

#### URL 和网络地址

- [Purl](https://github.com/jwage/purl): 一个简单的面向对象的 URL 操作库，支持 PHP 7.2+。
- [Uri](https://github.com/thephpleague/uri): 一个 PHP 包，为管理 URI 提供简单直观的类。
- [Url](https://github.com/crwlrsoft/url): 一个功能全面的 PHP URL 操作库。

### 其他

#### 多进程处理

- [amphp/parallel](https://github.com/amphp/parallel): 一个先进的 PHP 并行化库，可优化资源利用率并通过多线程提升应用性能。

#### 事件处理

- [React](https://github.com/reactphp/react): 一个基于事件驱动的 PHP 非阻塞 I/O 库。
- [Evenement](https://github.com/igorw/evenement): 一个非常简单的 PHP 事件调度库。
- [Event](https://github.com/thephpleague/event): 专注于领域事件的事件库。

#### 软件自动化管理

- [Salt](https://github.com/saltstack/salt): 用于大规模自动化管理和配置基础设施或应用程序的软件。
- [Puppet](https://github.com/puppetlabs/puppet): 一个服务器自动化框架和应用。

#### 任务调度

- [PHP Cron Scheduler](https://github.com/peppeocchi/php-cron-scheduler): 一个 PHP 定时任务调度程序。
- [Crunz](https://github.com/crunzphp/crunz): 一个基于 PHP 的任务调度工具。

## 常用网络爬取技术栈

### 静态网页

#### HTTP 客户端 + HTML 解析器

- **HTTP 客户端**: PHP cURL、Guzzle 或 Symfony 的 HttpClient。
- **HTML 解析器**: Simple Html Dom Parser for PHP、DomCrawler、HTML5-PHP 或 DiDOM。

#### 一体化解决方案

- Crawler、Roach 或 PHP-Spider。

### 动态网页

- Panther 或 php-webdriver。

## 指南与教程

### 通用指南

- [使用 PHP 进行网络爬取 - 完整指南](https://brightdata.com/blog/how-tos/web-scraping-php)
- [使用 Laravel 的网络爬取分步指南](https://brightdata.com/blog/web-data/web-scraping-with-laravel)
- [使用 cURL 进行网络爬取](https://brightdata.com/blog/how-tos/how-to-use-curl-for-web-scraping)

### 代理相关

- [如何在 Guzzle 中设置代理（2024）](https://brightdata.com/blog/how-tos/proxy-with-guzzle)
- [PHP 代理服务器：如何在 PHP 中设置代理](https://brightdata.com/blog/how-tos/php-proxy-servers)

### HTTP 客户端

- [使用 PHP 的 cURL 进行 GET 请求](https://brightdata.com/blog/how-tos/curl-get-request-with-php)
