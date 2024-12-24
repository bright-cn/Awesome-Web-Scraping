# Perl 网页抓取

本文档列出了在 Perl 中可用于网页抓取的库和资源。

## 目录

- [库](#库)
  - [网络](#网络)
    - [通用](#通用)
    - [HTTP 客户端](#http-客户端)
    - [WebSockets](#websockets)
    - [底层](#底层)
    - [其他](#其他)
  - [解析器](#解析器)
    - [HTML 解析器](#html-解析器)
    - [XML 解析器](#xml-解析器)
    - [URL 解析器](#url-解析器)
    - [HTTP 解析器](#http-解析器)
    - [邮件解析器](#邮件解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [SQL 解析器](#sql-解析器)
    - [其他](#其他-1)
  - [网络爬取](#网络爬取)
    - [框架](#框架)
    - [代理集成](#代理集成)
    - [CAPTCHA 解决](#captcha-解决)
  - [网络自动化](#网络自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
    - [工具和插件](#工具和插件)
    - [其他](#其他-2)
  - [数据导出](#数据导出)
    - [JSON](#json)
    - [CSV](#csv)
    - [YAML](#yaml)
    - [其他](#其他-3)
  - [数据处理](#数据处理)
    - [字符编码](#字符编码)
    - [日期和时间](#日期和时间)
    - [度量单位](#度量单位)
    - [电话号码](#电话号码)
    - [URL 和网络地址](#url-和网络地址)
    - [语言](#语言)
  - [其他](#其他-4)
    - [多进程](#多进程)
    - [任务调度](#任务调度)
- [常用网络爬虫技术栈](#常用网络爬虫技术栈)
  - [静态网页](#静态网页)
    - [HTTP 客户端 + HTML 解析器](#http-客户端-html-解析器)
    - [一体化网络爬取框架](#一体化网络爬取框架)
  - [动态网页](#动态网页)
    - [一体化浏览器自动化框架](#一体化浏览器自动化框架)
- [指南和教程](#指南和教程)

---

## 库

**注意**：所有所选库均为活跃维护或被广泛使用。

### 网络

#### 通用

- [LWP](https://github.com/libwww-perl/libwww-perl)：一组 Perl 模块，提供一个简洁、一致的 API 访问万维网。
- [Plack](https://github.com/plack/Plack)：一个 [PSGI](https://metacpan.org/pod/PSGI) 工具包和服务器适配器。
- [Mojo](https://github.com/mojolicious/mojo)：一个 Perl 实时 Web 框架。

#### HTTP 客户端

- [LWP::UserAgent](https://metacpan.org/pod/LWP::UserAgent)：一个类，用于实现 Web 用户代理。
- [HTTP::Tiny](https://github.com/Perl-Toolchain-Gang/HTTP-Tiny)：一个小型、简单且符合 HTTP/1.1 的客户端。
- [Mojo::UserAgent](https://metacpan.org/pod/Mojo::UserAgent)：一个非阻塞式 I/O 的 HTTP 和 WebSocket 用户代理。
- [WWW::Mechanize](https://github.com/libwww-perl/WWW-Mechanize)：一个用于在 Perl 对象中进行便捷 Web 浏览的库。
- [WWW::Curl::UserAgent](https://github.com/xing/curl-useragent)：基于 [libcurl](https://curl.se/libcurl/) 的 Web 用户代理。
- [REST::Client](https://github.com/milescrawford/cpan-rest-client)：一个用于与 RESTful HTTP/HTTPS 资源交互的简单客户端。
- [HTTP::Async](https://github.com/evdb/HTTP-Async)：一个可并行处理多个 HTTP 请求的库，且无需阻塞。

#### WebSockets

- [Mojo::WebSocket](https://metacpan.org/pod/Mojo::WebSocket)：一个实现 RFC 6455 描述的 WebSocket 协议的库。

#### 底层

- [Net::HTTP](https://github.com/libwww-perl/Net-HTTP)：一个底层的 HTTP 连接客户端。

#### 其他

- [CGI](https://github.com/leejo/CGI.pm)：处理公共网关接口（CGI）请求和响应的库。

### 解析器

#### HTML 解析器

- [HTML::TreeBuilder](https://github.com/kentfredric/HTML-Tree)：一个构建 HTML 语法树的解析器。
- [HTML::Parser](https://github.com/libwww-perl/HTML-Parser)：一组可解析并从 HTML 文档中提取信息的模块。
- [Mojo::DOM](https://metacpan.org/pod/Mojo::DOM)：一个轻量级的 HTML/XML DOM 解析器，支持 CSS 选择器。
- [HTML::HTML5::Parser](https://github.com/tobyink/p5-html-html5-parser)：一个 Perl 库，可可靠地解析 HTML。

#### XML 解析器

- [XML::Parser](https://github.com/cpan-authors/XML-Parser)：一个 Perl 模块，用于解析 XML 文档。
- [XML::LibXML](https://github.com/shlomif/perl-XML-LibXML)：[libxml2](https://gitlab.gnome.org/GNOME/libxml2) 的 Perl 绑定。

#### URL 解析器

- [URI::Info](https://github.com/perlancar/perl-URI-Info)：从 URI（URL）中提取各种信息的库。

#### HTTP 解析器

- [HTTP::Entity::Parser](https://github.com/kazeburo/HTTP-Entity-Parser)：一个符合 PSGI 的 HTTP 内容解析器。
- [HTTP::Parser::XS](https://github.com/kazuho/p5-http-parser-xs)：一个快速、原始级别的 HTTP 请求解析器。
- [Plack::HTTPParser](https://metacpan.org/pod/Plack::HTTPParser)：解析 HTTP 头的库。
- [HTTP::Body](https://metacpan.org/pod/HTTP::Body)：一个 HTTP body 解析器。
- [HTTP::Parser](https://metacpan.org/pod/HTTP::Parser)：一个库，将 HTTP/1.1 请求解析为 HTTP::Request/Response 对象。
- [HTTP::Link::Parser](https://github.com/tobyink/p5-http-link-parser)：用于解析 HTTP “Link” 头的库。
- [HTTP::MultiPartParser](https://github.com/chansen/p5-http-multipartparser)：处理多部分 MIME 数据流的底层 API。

#### 邮件解析器

- [Email::Address::XS](https://github.com/pali/Email-Address-XS)：解析并格式化 RFC 5322 邮件地址和组的库。

#### Markdown 解析器

- [Markdown::Parser](https://gitlab.com/jackdeguest/Markdown-Parser)：一个纯 Markdown 解析器。

#### SQL 解析器

- [SQL::Parser](https://github.com/perl5-dbi/SQL-Statement)：SQL 解析和处理引擎。

#### 其他

- [HTML::TreeBuilder::XPath](https://metacpan.org/pod/HTML::TreeBuilder::XPath)：为 HTML::TreeBuilder 添加 XPath 支持的库。
- [HTML::TreeBuilder::LibXML]：一个与 HTML::TreeBuilder 及 XPath 兼容的接口，基于 libxml。
- [WWW::RobotRules](https://github.com/gisle/www-robotrules)：一个模块，可根据 “[A Standard for Robot Exclusion](http://www.robotstxt.org/wc/norobots.html)” 中的规定解析 robots.txt 文件。
- [XML::RSS::LibXML](https://github.com/lestrrat-p5/XML-RSS-LibXML)：使用 XML::LibXML（libxml2）解析 RSS 的库。
- [WWW::Sitemap::XML](https://github.com/ajgb/www-sitemap-xml)：读写符合 Sitemaps.org 协议的 XML 网站地图的库。

### 网络爬取

#### 框架

- [Scrappy](https://metacpan.org/pod/Scrappy)：一个强大的网络蜘蛛、抓取、爬行框架。
- [Web::Query](https://github.com/tokuhirom/Web-Query)：类似 jQuery 的另一个 Perl 抓取库。
- [WWW::Scraper](https://metacpan.org/pod/WWW::Scraper)：一个框架，用于从搜索引擎抓取结果。

#### 代理集成

- [Bright Data的代理服务](https://bright.cn/proxy-types)：一个拥有7200万以上 IP 的代理网络，提供高级住宅、数据中心、移动和 ISP 代理，可按州、国家、ZIP、ASN 等级别定位，覆盖195个国家，适用于任意 HTTP 客户端或抓取库 [**Bright Data 的解决方案**]  
- [HTTP::Proxy](https://github.com/book/HTTP-Proxy)：一个纯 Perl 的 HTTP 代理。
- [Net::Proxy](https://github.com/book/Net-Proxy)：一个可多方式代理网络连接的框架。

#### CAPTCHA 解决

- [CAPTCHA Solver](https://bright.cn/products/web-unlocker/captcha-solver)：一个快速、自动化的CAPTCHA解决工具，可解决 reCAPTCHA、hCaptcha、px_captcha、SimpleCaptcha、GeeTest 等 [**Bright Data 的解决方案**]。

### 网络自动化

#### 浏览器自动化框架

- [WWW::Mechanize::Chrome](https://github.com/Corion/WWW-Mechanize-Chrome)：一个用于自动化Chrome浏览器的库。
- [Playwright](https://github.com/teodesian/playwright-perl)：[Playwright](https://playwright.dev/) 的 Perl 绑定。
- [Selenium::Edge](https://github.com/teodesian/Selenium-Remote-Driver)：Selenium Webdriver 服务器的 Perl 绑定，用于 Edge。
- [Firefox::Marionette](https://github.com/david-dick/firefox-marionette)：一个使用 Marionette 协议自动化 Firefox 的库。
- [WWW::Selenium](https://github.com/lukec/cpan-selenium-rc-perl)：Selenium Remote Control 测试工具的 Perl 客户端。

#### 工具和插件

- [Firefox::Marionette::Extension::Stealth]()：一个针对 Firefox::Marionette 的 Stealth 扩展。

#### 其他

- [Chrome::DevToolsProtocol](Chrome::DevToolsProtocol)：一个 DevTools 协议的异步调度程序。
- [JavaScript::SpiderMonkey](https://github.com/thomasbusch/perl-javascript-spidermonkey)：[SpiderMonkey](https://spidermonkey.dev/) JavaScript 引擎的 Perl 接口。

### 数据导出

#### JSON

- [JSON](https://github.com/makamaka/JSON)：Perl 版 JSON 编码/解码库。
- [JSON:PP](https://github.com/makamaka/JSON-PP)：纯 Perl 实现的 JSON 编解码器。
- [JSON::XS](https://metacpan.org/pod/JSON::XS)：正确且快速地执行 JSON 序列化/反序列化。
- [Geo::JSON](https://github.com/mjemmeson/Geo-JSON)：一个适用于 GeoJSON 的 Perl 面向对象接口。
- [JSON::Syck](https://metacpan.org/pod/JSON::Syck)：基于 YAML 的 JSON 解析和生成实现。

#### CSV

- [Text::CSV](https://github.com/makamaka/Text-CSV)：用于逗号分隔值的处理器（可使用 XS 或 PurePerl）。

#### YAML

- [YAML::XS](https://github.com/ingydotnet/yaml-libyaml-pm)：使用 XS 与 [libyaml](https://github.com/yaml/libyaml) 的 Perl YAML 序列化模块。
- [YAML](https://github.com/ingydotnet/yaml-pm)：一个 Perl YAML 模块。
- [YAML::PP](https://github.com/perlpunk/YAML-PP-p5)：Perl 中 YAML 1.2 处理器。
- [YAML::Syck](https://metacpan.org/pod/YAML::Syck)：一个快速且轻量的 YAML 加载和转储器。
- [YAML::Tiny](https://github.com/Perl-Toolchain-Gang/YAML-Tiny)：极少代码即可读写 YAML 文件的库。

#### 其他

- [Excel::Writer::XLSX](https://github.com/jmcnamara/excel-writer-xlsx)：一个 Perl 模块，用于创建 Excel XLSX 文件。
- [Pod::Markdown](https://github.com/rwstauner/Pod-Markdown)：一个将 POD 转换为 Markdown 的库。

### 数据处理

#### 字符编码

- [PerlIO::encoding](https://metacpan.org/pod/PerlIO::encoding)：一个内置库，可在文件句柄上开启透明编码过滤器。
- [Encoding::FixLatin](https://github.com/grantm/encoding-fixlatin)：将混合编码输入转换为 UTF-8 输出的库。

#### 日期和时间

- [DateTime](https://github.com/houseabsolute/DateTime.pm)：Perl 的日期与时间对象。
- [Mojo::Date](https://metacpan.org/pod/Mojo::Date)：实现基于 RFC 7230、RFC 7231 和 RFC 3339 的 HTTP 日期与时间函数的库。
- [HTTP::Date](https://github.com/libwww-perl/HTTP-Date)：提供处理 HTTP 协议中日期格式的函数。
- [Date::Manip::Date](https://github.com/SBECK-github/Date-Manip)：为处理日期提供多种方法的库。
- [APR::Date](https://metacpan.org/dist/mod_perl/view/docs/api/APR/Date.pod)：Perl 对 APR 日期操作函数的 API。
- [Date::Calc](https://metacpan.org/dist/Date-Calc/view/lib/Date/Calc.pod)：一个执行公历日期计算的库。

#### 度量单位

- [Class::Measure::Length](https://github.com/bluefeet/Class-Measure)：一个可创建、比较和转换测量单位的库。

#### 电话号码

- [Number::Phone](https://github.com/DrHyde/perl-modules-Number-Phone)：一组大型的 Perl 模块，用于解析和处理电话号码。

#### URL 和网络地址

- [Mojo::URL](https://github.com/mojolicious/mojo)：实现了 RFC 3986、RFC 3987 以及 URL Living Standard 的子集，并支持 IDNA 和 IRI 的库。
- [URI](https://github.com/libwww-perl/URI)：用于统一资源标识符（绝对/相对）的库。
- [URI::XS](https://metacpan.org/dist/URI-XS/view/lib/URI/XS.pod)：一个快速的 URI 框架，与经典 URI 兼容并拥有 C++ 接口。
- [URL::Encode](https://github.com/chansen/p5-url-encode)：编码/解码 `application/x-www-form-urlencoded` 编码的库。

#### 语言

- [Text::Unaccent](https://metacpan.org/pod/Text::Unaccent)：一个从字符串中移除重音符号的库。

### 其他

#### 多进程

- [MCE](https://github.com/marioroy/mce-perl)：提供多核并行处理能力的 Perl 引擎。
- [Parallel::ForkManager](https://github.com/dluxhu/perl-parallel-forkmanager)：一个简单的并行处理 fork 管理器。
- [Parallel::Runner](https://github.com/exodist/Parallel-Runner)：一个对象，可管理并行进程的运行。

#### 任务调度

- [Schedule::Cron](https://github.com/NicholasBHubbard/schedule-cron)：一个类似 cron 的调度器，可用于 Perl 子程序。

## 常用网络爬虫技术栈

### 静态网页

#### HTTP 客户端 + HTML 解析器

- **HTTP 客户端**：LWP::UserAgent、HTTP::Tiny、Mojo::UserAgent 或 WWW::Mechanize
- **HTML 解析器**：HTML::TreeBuilder、HTML::Parser 或 Mojo::DOM

#### 一体化网络爬取框架

- Scrappy 或 Web::Query

### 动态网页

#### 一体化浏览器自动化框架

- WWW::Mechanize::Chrome、Playwright 或 Firefox::Marionette

## 指南和教程

- [使用 Perl 进行网页抓取 - 分步指南](https://bright.cn/blog/web-data/web-scraping-with-perl)
