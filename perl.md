# Perl 网络爬取

本文档列出了用于 Perl 网络爬取的库和资源。

## 目录

- [库](#库)
  - [网络](#网络)
    - [通用](#通用)
    - [HTTP 客户端](#http-客户端)
    - [WebSocket](#websocket)
    - [低级网络](#低级网络)
    - [其他](#其他)
  - [解析器](#解析器)
    - [HTML 解析器](#html-解析器)
    - [XML 解析器](#xml-解析器)
    - [URL 解析器](#url-解析器)
    - [HTTP 解析器](#http-解析器)
    - [电子邮件解析器](#电子邮件解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [SQL 解析器](#sql-解析器)
    - [其他解析器](#其他解析器)
  - [网络爬取](#网络爬取)
    - [框架](#框架)
    - [代理集成](#代理集成)
    - [验证码解决方案](#验证码解决方案)
  - [网络自动化](#网络自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
    - [工具和插件](#工具和插件)
    - [其他工具](#其他工具)
  - [数据导出](#数据导出)
    - [JSON](#json)
    - [CSV](#csv)
    - [YAML](#yaml)
    - [其他导出](#其他导出)
  - [数据处理](#数据处理)
    - [字符编码](#字符编码)
    - [日期和时间处理](#日期和时间处理)
    - [单位转换](#单位转换)
    - [电话号码处理](#电话号码处理)
    - [URL 和网络地址](#url-和网络地址)
    - [语言处理](#语言处理)
  - [其他功能](#其他功能)
    - [多进程](#多进程)
    - [任务调度](#任务调度)
- [常用网络爬取技术栈](#常用网络爬取技术栈)
  - [静态网页](#静态网页)
    - [HTTP 客户端 + HTML 解析器](#http-客户端-html-解析器)
    - [一体化网络爬取框架](#一体化网络爬取框架)
  - [动态网页](#动态网页)
    - [一体化浏览器自动化框架](#一体化浏览器自动化框架)
- [指南和教程](#指南和教程)

## 库

### 网络

#### 通用

- **[LWP](https://github.com/libwww-perl/libwww-perl)**：提供一致的接口与万维网交互的 Perl 模块集合。
- **[Plack](https://github.com/plack/Plack)**：一个 [PSGI](https://metacpan.org/pod/PSGI) 工具包和服务器适配器。
- **[Mojo](https://github.com/mojolicious/mojo)**：一个实时 Perl Web 框架。

#### HTTP 客户端

- **[LWP::UserAgent](https://metacpan.org/pod/LWP::UserAgent)**：实现 Web 用户代理的类。
- **[HTTP::Tiny](https://github.com/Perl-Toolchain-Gang/HTTP-Tiny)**：一个小巧、简单且符合 HTTP/1.1 标准的客户端。
- **[WWW::Mechanize](https://github.com/libwww-perl/WWW-Mechanize)**：用于方便 Web 浏览的 Perl 对象。

#### WebSocket

- **[Mojo::WebSocket](https://metacpan.org/pod/Mojo::WebSocket)**：实现 RFC 6455 中定义的 WebSocket 协议的库。

#### 低级网络

- **[Net::HTTP](https://github.com/libwww-perl/Net-HTTP)**：低级 HTTP 连接客户端。

### 解析器

#### HTML 解析器

- **[HTML::TreeBuilder](https://github.com/kentfredric/HTML-Tree)**：构建 HTML 语法树的解析器。
- **[HTML::Parser](https://github.com/libwww-perl/HTML-Parser)**：从 HTML 文档中解析并提取信息的模块。

#### XML 解析器

- **[XML::Parser](https://github.com/cpan-authors/XML-Parser)**：用于解析 XML 文档的 Perl 模块。

#### URL 解析器

- **[URI::Info](https://github.com/perlancar/perl-URI-Info)**：从 URI 中提取各种信息的库。

#### HTTP 解析器

- **[HTTP::Entity::Parser](https://github.com/kazeburo/HTTP-Entity-Parser)**：符合 PSGI 的 HTTP 实体解析器。
- **[HTTP::Parser::XS](https://github.com/kazuho/p5-http-parser-xs)**：快速的 HTTP 请求解析器。

### 网络爬取

#### 框架

- **[Scrappy](https://metacpan.org/pod/Scrappy)**：功能强大的 Web 爬取框架。
- **[Web::Query](https://github.com/tokuhirom/Web-Query)**：类似 jQuery 的爬取库。

#### 代理集成

- **[Bright Data 的代理服务](https://brightdata.com/proxy-types)**：提供 7200 万个以上的 IP，支持国家、州、省、市、邮编等精确定位。

#### 验证码解决方案

- **[CAPTCHA Solver](https://brightdata.com/products/web-unlocker/captcha-solver)**：自动化解决 reCAPTCHA、hCaptcha 等验证码问题。

### 数据导出

#### JSON

- **[JSON](https://github.com/makamaka/JSON)**：JSON 编码/解码的 Perl 实现。

#### CSV

- **[Text::CSV](https://github.com/makamaka/Text-CSV)**：操作逗号分隔值文件的模块。

#### YAML

- **[YAML::XS](https://github.com/ingydotnet/yaml-libyaml-pm)**：使用 XS 和 [libyaml](https://github.com/yaml/libyaml) 的 YAML 序列化模块。

### 数据处理

#### 日期和时间处理

- **[DateTime](https://github.com/houseabsolute/DateTime.pm)**：Perl 的日期时间对象。
- **[Mojo::Date](https://metacpan.org/pod/Mojo::Date)**：基于 HTTP 日期和时间功能的库。

#### 单位转换

- **[Class::Measure](https://github.com/bluefeet/Class-Measure)**：用于创建、比较和转换测量单位的库。

### 常用网络爬取技术栈

#### 静态网页

- **HTTP 客户端**：推荐使用 LWP::UserAgent、HTTP::Tiny。
- **HTML 解析器**：推荐 HTML::TreeBuilder。

#### 动态网页

- **浏览器自动化框架**：推荐 WWW::Mechanize::Chrome。

## 指南和教程

- [Perl 网络爬取 - 分步教程](https://brightdata.com/blog/web-data/web-scraping-with-perl)