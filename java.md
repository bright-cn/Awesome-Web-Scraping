# Java 网页抓取

本文档列出了在 Java 中可用于网络爬取的库和资源。

## 目录

- [库](#库)
  - [网络](#网络)
    - [HTTP 和 WebSocket 客户端](#http-和-websocket-客户端)
    - [WebSockets](#websockets)
    - [底层网络](#底层网络)
  - [解析器](#解析器)
    - [通用解析器](#通用解析器)
    - [HTML 解析器](#html-解析器)
    - [XML 解析器](#xml-解析器)
    - [URL 解析器](#url-解析器)
    - [CSV 解析器](#csv-解析器)
    - [JSON 解析器](#json-解析器)
    - [邮件解析器](#邮件解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [YAML 解析器](#yaml-解析器)
    - [SQL 解析器](#sql-解析器)
    - [Office 文件解析器](#office-文件解析器)
    - [其他](#其他)
  - [网络爬取](#网络爬取)
    - [框架](#框架)
    - [代理集成](#代理集成)
    - [CAPTCHA 解决](#captcha-解决)
  - [网络自动化](#网络自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
    - [其他](#其他-1)
  - [数据处理](#数据处理)
    - [通用](#通用)
    - [字符编码](#字符编码)
    - [JSON](#json)
    - [日期和时间](#日期和时间)
    - [价格](#价格)
    - [电话号码](#电话号码)
    - [Slugs](#slugs)
    - [语言](#语言)
  - [其他](#其他-2)
    - [任务调度](#任务调度)
- [流行的网络爬虫技术栈](#流行的网络爬虫技术栈)
  - [静态网页](#静态网页)
    - [HTTP 客户端 + HTML 解析器](#http-客户端-html-解析器)
    - [一体化解决方案](#一体化解决方案)
  - [动态网页](#动态网页)
- [指南和教程](#指南和教程)
  - [通用指南](#通用指南)
  - [对比](#对比)

---

## 库

**注意**：所有选择的库都处于活跃维护状态或被广泛使用。

### 网络

#### HTTP 和 WebSocket 客户端

- [HttpClient](https://docs.oracle.com/en/java/javase/23/docs/api/java.net.http/java/net/http/HttpClient.html)：Java 11 内置的 HTTP 客户端，用于发送请求并获取响应。
- [HttpURLConnection](https://docs.oracle.com/en/java/javase/23/docs/api/java.base/java/net/HttpURLConnection.html)：Java 内置类，用于向 HTTP 服务器发起单次请求。
- [HttpsURLConnection](https://docs.oracle.com/en/java/javase/23/docs/api/java.base/javax/net/ssl/HttpsURLConnection.html)：HttpURLConnection 的扩展，增加了 HTTPS 特有功能。
- [Apache HttpClient](https://github.com/apache/httpcomponents-client)：适用于 Java 的同步 HTTP 和 WebSocket 客户端库。
- [Apache AsyncHttpClient](https://github.com/AsyncHttpClient/async-http-client)：适用于 Java 的异步 HTTP 和 WebSocket 客户端库。
- [OkHttp](https://github.com/square/okhttp)：适用于 JVM、Android 以及 GraalVM 的精细 HTTP 客户端。
- [Jetty HttpClient](https://github.com/jetty/jetty.project)：支持 HTTP/2、HTTP/1.1、HTTP/1.0、WebSocket、Servlet 等的 HTTP 客户端。
- [Google HTTP Client Library For Java](https://github.com/googleapis/google-http-java-client)：一个灵活、高效、功能强大的 Java 库，可通过 HTTP 访问任意 Web 资源。
- [Retrofit](https://github.com/square/retrofit)：一个类型安全的 HTTP 客户端，适用于 Android 与 JVM。

#### WebSockets

- [WebSocket](https://docs.oracle.com/en/java/javase/23/docs/api/java.net.http/java/net/http/WebSocket.html)：Java 内置的 WebSocket 客户端。
- [Java-WebSocket](https://github.com/TooTallNate/Java-WebSocket)：一个 100% 纯 Java 编写的精简版 WebSocket 客户端和服务器实现。

#### 底层网络

- [pcap4j](https://github.com/kaitoy/pcap4j)：一个用于捕获、构建和发送数据包的 Java 库。

### 解析器

#### 通用解析器

- [Apache Tika](https://github.com/apache/tika)：一个工具包，可检测并从 PPT、XLS、PDF 等数千种文件类型中提取元数据和文本。
- [Jackson Text Dataformats](https://github.com/FasterXML/jackson-dataformats-text)：用于部分标准 Jackson 文本格式后端（如 CSV、properties、yaml）的综合项目。

#### HTML 解析器

- [jsoup](https://github.com/jhy/jsoup)：一个 Java HTML 解析器，支持 HTML 编辑、清理、爬取以及 XSS 安全。
- [HtmlCleaner](https://htmlcleaner.sourceforge.net/)：用 Java 编写的开源 HTML 解析器。
- [JFiveParse](https://github.com/digitalfondue/jfiveparse)：符合 HTML5 标准的 Java 解析器。

#### XML 解析器

- [JAXP](https://docs.oracle.com/en/java/javase/23/docs/api/java.xml/module-summary.html#JAXP)：Java 内置 API，用于 XML 处理。

#### URL 解析器

- [URI](https://docs.oracle.com/en/java/javase/23/docs/api/java.base/java/net/URI.html)：Java 内置的 URI API，可进行标准化、解析和相对化处理。

#### CSV 解析器

- [Apache Commons CSV](https://github.com/apache/commons-csv)：提供简单接口，可读写多种类型的 CSV 文件。

#### JSON 解析器

- [JSON Path](https://github.com/json-path/JsonPath)：一个 Java DSL，用于读取 JSON 文档。

#### 邮件解析器

- [Angus Mail](https://github.com/eclipse-ee4j/angus-mail)：一个库，提供与平台、协议无关的框架，用于构建邮件和消息应用。
- [Apache Commons Email](https://github.com/apache/commons-email)：一个库，简化了 JavaMail API，可用于发送电子邮件。

#### Markdown 解析器

- [Flexmark](https://mvnrepository.com/artifact/com.vladsch.flexmark/flexmark-all)：一个Java版 CommonMark/Markdown 解析器，带有AST、HTML 转 MD、MD 转 PDF、MD 转 DOCX等转换模块。
- [CommonMark](https://github.com/commonmark/commonmark-java)：一个用于解析并渲染 CommonMark (Markdown) 的 Java 库。

#### YAML 解析器

- [SnakeYAML](https://bitbucket.org/snakeyaml/snakeyaml)：JVM 的完整 YAML 1.1 解析器。

#### SQL 解析器

- [JSqlParser](https://github.com/JSQLParser/JSqlParser)：一个解析 SQL 语句并转换为 Java 类层级结构的库。

#### Office 文件解析器

- [Apache POI](https://github.com/apache/poi)：一个 Java API，可访问微软格式文件（如 Excel、Word、PowerPoint 等）。

#### 其他

- [Rome](https://github.com/rometools/rome)：一个 Java 库，用于解析 RSS 和 Atom feeds。
- [uap-java](https://github.com/ua-parser/uap-java)：[ua-parser](https://github.com/faisalman/ua-parser-js) 的 Java 实现。
- [Yauaa](https://github.com/nielsbasjes/yauaa)：又一个 User-Agent 分析器。

### 网络爬取

#### 框架

- [Apache Nutch](https://github.com/apache/nutch)：一个可扩展、可伸缩的网络爬虫。
- [WebMagic](https://github.com/code4craft/webmagic)：Java可伸缩网络爬虫框架。
- [Jaunt](https://jaunt-api.com/)：一个Java库，用于网络爬取、网络自动化以及 JSON 查询。
- [ACHE Focused Crawler](https://github.com/ViDA-NYU/ache)：一个面向特定领域搜索的网络爬虫。
- [Gecco](https://github.com/xtuhcy/gecco)：一个易于使用的轻量级网络爬虫。
- [StormCrawler](https://github.com/DigitalPebble/storm-crawler)：基于Apache Storm的可扩展、成熟且多功能的网络爬虫。

#### 代理集成

- [Bright Data的代理服务](https://bright.cn/proxy-types)：提供超过 7200 万个 IP 的代理网络，包括优质的住宅、数据中心、移动和 ISP 代理，支持州、国家、ZIP 以及 ASN 级别定位，覆盖 195 个国家，可与任意 HTTP 客户端或爬虫库搭配使用 [**Bright Data 解决方案**]

#### CAPTCHA 解决

- [CAPTCHA Solver](https://bright.cn/products/web-unlocker/captcha-solver)：一个快速、自动化的CAPTCHA解决方案，可处理reCAPTCHA、hCaptcha、px_captcha、SimpleCaptcha、GeeTest等 [**Bright Data解决方案**]

### 网络自动化

#### 浏览器自动化框架

- [Selenium](https://github.com/SeleniumHQ/selenium)：一个浏览器自动化框架与生态系统。
- [Playwright](https://github.com/microsoft/playwright-java)：[Playwright](https://playwright.dev/)的Java版本，用于测试与自动化。
- [HtmlUnit](https://htmlunit.sourceforge.io/)：为Java程序提供的无GUI浏览器，模拟HTML文档并提供API访问页面、填写表单、点击链接等。
- [Jauntium](https://jauntium.com/)：一个Java库，可轻松自动化Chrome、Firefox、Safari、Edge、IE等现代浏览器。

#### 其他

- [WebDriverManager](https://github.com/bonigarcia/webdrivermanager)：一个库，为 Java 中的Selenium WebDriver 提供自动化驱动管理及其他辅助功能。

### 数据处理

#### 通用

- [Jackson](https://github.com/FasterXML/jackson)：适用于Java（及JVM平台）的一组数据处理工具，包括核心流式 JSON 解析/生成器、数据绑定库（POJO与JSON的双向转换），以及支持Avro、BSON、CBOR、CSV、Smile、Properties、Protobuf、TOML、XML、YAML等多种格式的扩展模块，以及对Guava、Joda、PCollections等众多常用数据类型的支持（详情见下）。

#### 字符编码

- [Charset](https://docs.oracle.com/en/java/javase/23/docs/api/java.base/java/nio/charset/Charset.html)：Java内置类，定义了用于在字节与Unicode字符之间转换的charset、decoder、encoder。
- [Apache Commons Codec](https://commons.apache.org/proper/commons-codec/)：一个包含Base16、Base32、Base64、digest以及Hexadecimal等多种格式编码解码器的库。

#### JSON

- [JSON](https://github.com/stleary/JSON-java)：JSON在Java中的参考实现。

#### 日期和时间

- [LocalDate](https://docs.oracle.com/en/java/javase/23/docs/api/java.base/java/time/LocalDate.html)：Java内置类，表示不可变的日期对象。
- [LocalTime](https://docs.oracle.com/en/java/javase/23/docs/api/java.base/java/time/LocalTime.html)：Java内置类，表示不可变的时间对象。
- [Jode-Time](https://github.com/JodaOrg/joda-time)：在Java SE 8之前被广泛使用的日期时间类替代方案。

#### 价格

- [JSR 354](https://github.com/JavaMoney/jsr354-api)：提供用于表示、传输、执行货币和金额综合运算的API。

#### 电话号码

- [libphonenumber](https://github.com/google/libphonenumber)：一个解析、格式化和验证国际电话号码的库。

#### Slugs

- [Slugify](https://github.com/slugify/slugify)：一个小型工具库，可生成易读的URL。

#### 语言

- [Apache Commons Lang](https://commons.apache.org/proper/commons-lang/)：为 java.lang API 提供大量辅助工具函数的库，特别包括字符串操作、基本数值方法、对象反射、并发以及对象创建和序列化及系统属性等。

### 其他

#### 任务调度

- [Wisp](https://github.com/Coreoz/Wisp)：一个占用内存小且API简洁的Java调度库。

## 流行的网络爬虫技术栈

### 静态网页

#### HTTP 客户端 + HTML 解析器

- **HTTP 客户端**: HttpClient、Apache HttpClient、Apache AsyncHttpClient、OkHttp、Jetty HttpClient、Google HTTP Client Library For Java 或 Retrofit

- **HTML 解析器**: Jsoup 或 HtmlCleaner

#### 一体化解决方案

- Jsoup

### 动态网页

- Selenium、Playwright 或 HtmlUnit

## 指南和教程

### 通用指南

- [Java网络爬取 - 完整指南 2024](https://bright.cn/blog/how-tos/java-web-scraping)
- [使用 Jsoup 进行 Java 网络爬取：分步指南](https://bright.cn/blog/how-tos/web-scraping-with-jsoup)

### 对比

- [Java vs Python - 对比指南](https://bright.cn/blog/web-data/java-vs-python)
- [Java vs C# 网页抓取对比](https://bright.cn/blog/web-data/java-vs-c-sharp)
- [Playwright vs. Selenium 2024 对比](https://bright.cn/blog/web-data/playwright-vs-selenium)
