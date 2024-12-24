# R 网络爬取

本文档列出了用于 R 语言进行网络爬取的库和资源。

## 目录

- [库](#库)
  - [网络](#网络)
    - [HTTP 客户端](#http-客户端)
    - [WebSockets](#websockets)
    - [其他](#其他)
  - [解析器](#解析器)
    - [HTML/XML 解析器](#htmlxml-解析器)
    - [URL 解析器](#url-解析器)
    - [CSV 解析器](#csv-解析器)
    - [日期和时间解析器](#日期和时间解析器)
    - [PDF 解析器](#pdf-解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [YAML 解析器](#yaml-解析器)
    - [SQL 解析器](#sql-解析器)
    - [Office 文件解析器](#office-文件解析器)
    - [其他](#其他-1)
  - [网络爬取](#网络爬取)
    - [框架](#框架)
    - [工具和插件](#工具和插件)
    - [代理集成](#代理集成)
    - [验证码解决](#验证码解决)
    - [用户代理伪装](#用户代理伪装)
    - [其他](#其他-2)
  - [网络自动化](#网络自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
    - [工具和插件](#工具和插件-1)
    - [其他](#其他-3)
  - [数据导出](#数据导出)
    - [JSON](#json)
    - [CSV](#csv)
    - [其他](#其他-4)
  - [数据处理](#数据处理)
    - [通用](#通用)
    - [表格数据](#表格数据)
    - [字符编码](#字符编码)
    - [日期和时间](#日期和时间)
    - [电话号码](#电话号码)
    - [其他](#其他-5)
  - [其他](#其他-6)
    - [多进程](#多进程)
    - [任务调度](#任务调度)
- [热门网络爬取技术栈](#热门网络爬取技术栈)
  - [静态网页](#静态网页)
    - [HTTP 客户端 + HTML 解析器](#http-客户端-html-解析器)
    - [一体化网络爬取框架](#一体化网络爬取框架)
  - [动态网页](#动态网页)
    - [一体化浏览器自动化框架](#一体化浏览器自动化框架)
- [指南和教程](#指南和教程)

## 库

**注意**：以下列出的库均为活跃维护或广泛使用的项目。

### 网络

#### HTTP 客户端

- [httr2](https://github.com/r-lib/httr2)：一个 R 库，用于发起 HTTP 请求并处理响应，是 `httr` 的现代重新设计。
- [crul](https://github.com/ropensci/crul)：基于 [R6](https://r6.r-lib.org/) 的 R HTTP 客户端，适合开发者使用。
- [RCurl](https://cran.r-project.org/web/packages/RCurl/index.html)：[libcurl](https://curl.se/libcurl/) 的 R 封装。
- [request](https://github.com/sckott/request)：一个用于 HTTP 请求的 R 语言 DSL。
- [httpRequest](https://cran.r-project.org/web/packages/httpRequest/index.html)：提供 R 中 GET、POST 和多部分 POST 请求协议。
- [routr](https://github.com/thomasp85/routr)：一个用于 R 的 Web 请求路由包。

#### WebSockets

- [websocket](https://github.com/rstudio/websocket)：R 的 WebSocket 客户端。
- [httpuv](https://github.com/rstudio/httpuv)：为 R 提供 HTTP 和 WebSocket 服务器功能的包。

#### 其他

- [fauxpas](https://sckott.github.io/fauxpas/)：R 的 HTTP 错误帮助工具。
- [reqres](https://github.com/thomasp85/reqres)：提供 HTTP 请求和响应强大类的包。
- [tryr](https://github.com/analythium/tryr)：用于 HTTP API 的客户端/服务器错误处理库。
- [base64url](https://github.com/mllg/base64url)：一个快速且 URL 安全的 R Base64 编解码器。

### 解析器

#### HTML/XML 解析器

- [xml2](https://github.com/r-lib/xml2)：[libxml2](https://gitlab.gnome.org/GNOME/libxml2) 的 R 绑定。
- [XiMpLe](https://cran.r-project.org/web/packages/XiMpLe/index.html)：一个简单的 R XML 树解析器/生成器。
- [XML](https://cran.r-project.org/web/packages/XML/index.html)：用于 R 的 XML 解析和生成工具。
- [xml2relational](https://github.com/jsugarelli/xml2relational/)：将 XML 文档转换为关系数据模型的库。
- [xmlconvert](https://github.com/jsugarelli/xmlconvert/)：轻松将 XML 文档转换为数据框，反之亦然。
- [xmlr](https://github.com/Alipsa/xmlr)：类似于 [jdom](https://github.com/hunterhacker/jdom) 的 XML DOM 包，使用 R 的 [参考类](http://adv-r.had.co.nz/R5.html) 实现。


#### URL 解析器

- [adaR](https://github.com/gesistsa/adaR)：一个 [ada-url](https://github.com/ada-url/ada) 的封装器，是一个符合 WHATWG 标准的快速 URL 解析器，使用现代 C++ 编写。

#### CSV 解析器

- [csvread](https://github.com/jabiru/csvread)：一个快速且专用的 CSV 文件加载器。
- [easycsv](https://github.com/bogind/easycsv)：一个 R 包，用于轻松从多个表格加载数据。

#### 日期和时间解析器

- [parsedate](https://github.com/gaborcsardi/parsedate)：一个 R 包，用于解析任意格式的日期。

#### PDF 解析器

- [pdfsearch](https://github.com/lebebr01/pdfsearch)：一个库，用于在 PDF 文件中搜索关键字。
- [pdftools](https://github.com/ropensci/pdftools)：提供文本提取、渲染和 PDF 文档转换的工具。
- [tabulapdf](https://github.com/ropensci/tabulapdf/)：R 对 [Tabula](https://github.com/tabulapdf/tabula) PDF 表格提取库的绑定。
- [pdf](https://github.com/expersso/pdftables)：一个 R 库，用于以编程方式转换 PDF 表格。
- [Rpoppler](https://cran.r-project.org/web/packages/Rpoppler/index.html)：基于 [Poppler](https://poppler.freedesktop.org/) 的 PDF 工具。
- [staplr](https://cran.r-project.org/web/packages/staplr/index.html)：一个 PDF 工具包，提供操作 PDF 文件的功能。
- [pdfminer](https://cran.r-project.org/web/packages/pdfminer/index.html)：一个 R 库，为 [PDFMiner](https://github.com/pdfminer/pdfminer.six) 提供接口，该工具为 Python 提供从 PDF 文件中提取信息的功能。

#### Markdown 解析器

- [marquee](https://github.com/r-lib/marquee)：一个用于 R 图形的 Markdown 解析和渲染器。
- [parsemd](https://github.com/rundel/parsermd)：一个库，用于提取 R Markdown 文件的内容，允许以编程方式与文档内容交互。
- [md4r](https://cran.r-project.org/web/packages/md4r/index.html)：一个使用 [MD4C](https://github.com/mity/md4c) 库实现的 Markdown 解析器。

#### YAML 解析器

- [yum](https://gitlab.com/r-packages/yum)：用于提取和处理 YAML 片段的工具。

#### SQL 解析器

- [RSqlParser](https://cran.r-project.org/web/packages/RSqlParser/index.html)：一个用于解析 SQL 语句的工具。
- [queryparser](https://github.com/ianmcook/queryparser)：一个库，用于将 SQL 查询翻译为 R 表达式。
- [sqlparseR]：对 Python 模块 [sqlparse](https://github.com/andialbrecht/sqlparse) 的封装。

#### Office 文件解析器

- [readxl](https://github.com/tidyverse/readxl)：一个库，用于读取 Excel 文件（.xls 和 .xlsx）到 R 中。
- [readxlsb](https://github.com/velofrog/readxlsb)：一个库，用于导入 Excel 二进制文件（.xlsb）到 R 中。
- [exceldata](https://cran.r-project.org/web/packages/exceldata/index.html)：一个库，用于简化从 Excel 导入、清理和重新编码数据的流程。
- [modgetxl](https://cran.r-project.org/web/packages/modgetxl/index.html)：一个用于读取 Excel 表的 Shiny 模块。

#### 其他

- [humaniformat](https://github.com/ironholds/humaniformat/)：一个人名解析器。
- [parcr](https://github.com/SystemsBioinformatics/parcr)：用于在 R 中构建解析器组合器的工具。
- [qmrparser](https://cran.r-project.org/web/packages/qmrparser/index.html)：一个 R 解析器组合器，提供构建解析器的基本函数。
- [robotstxt](https://github.com/ropensci/robotstxt)：一个 R 库，用于解析和检查 robots.txt 文件。
- [r-optparse](https://github.com/trevorld/r-optparse)：一个命令行可选参数解析器。
- [configr](https://github.com/Miachol/configr)：一个实现 JSON、INI、YAML 和 TOML 解析器的库。
- [xmlparsedata](https://github.com/r-lib/xmlparsedata)：以 XML 树形式解析 R 代码数据的工具。

### 网络爬取

#### 框架

- [rvest](https://github.com/tidyverse/rvest)：用于 R 的简单网络爬取工具。
- [Rcrawler](https://github.com/salimk/Rcrawler/)：一个 R 的网络爬取和爬虫工具。
- [ralger](https://github.com/feddelegrand7/ralger)：一个易于抓取网站的库，基于 rvest 和 xml2。
- [scrapeR](https://cran.r-project.org/web/packages/scrapeR/index.html)：用于提取指定网页文本内容的函数。

#### 工具和插件

- [scraEP](https://cran.r-project.org/web/packages/scraEP/index.html)：用于从网页和其他 XML 内容中抓取信息的工具，支持使用 XPath 或 CSS 选择器。

#### 代理集成

- [Bright Data 的代理服务](https://brightdata.com/proxy-types)：提供超过 7200 万个 IP 的代理网络，包括高级住宅、数据中心、移动和 ISP 代理。支持按州、国家、邮政编码和 ASN 级别的定位，覆盖 195 个国家。适用于任何 HTTP 客户端或抓取库 [**Bright Data 的解决方案**]。
- [getProxy](https://github.com/selesnow/getProxy)：一个 R 库，用于在 R 中获取免费的代理 IP 和端口。
- [ip2proxy](https://cran.r-project.org/web/packages/ip2proxy/index.html)：一个 R 库，帮助用户识别被用作 VPN 匿名器、开放代理、网络代理和 Tor 出口的 IP 地址。
- [r.proxy](https://github.com/xiayh17/r.proxy)：一个库，用于在 R 控制台中设置代理。

#### 验证码破解

- [CAPTCHA Solver](https://brightdata.com/products/web-unlocker/captcha-solver)：一个快速自动化的验证码破解工具，可以解决 reCAPTCHA、hCaptcha、px_captcha、SimpleCaptcha、GeeTest CAPTCHA 等挑战 [**Bright Data 的解决方案**]。

#### 用户代理伪装

- [Randomuseragent](https://cran.r-project.org/web/packages/Randomuseragent/index.html)：用于筛选和随机抽样真实 User-Agent 字符串的库。

#### 其他

- [heapsofpapers](https://github.com/RohanAlexander/heapsofpapers)：一个库，可轻松下载大量 PDF 和 CSV 文件。
- [antiword](https://cran.r-project.org/web/packages/antiword/index.html)：一个用于从 Microsoft Word 文档中提取文本的库。
- [tidyrss](https://github.com/RobertMyles/tidyrss)：一个 R 包，用于从 RSS、Atom 和 JSON 提要中提取整洁的数据框。
- [getwiki](https://cran.r-project.org/web/packages/getwiki/index.html)：一个 R 包装器，用于获取 Wikipedia 数据。
- [tidywikidatar](https://github.com/EDJNet/tidywikidatar)：一个库，通过整洁的数据框探索 Wikidata。

### 网络自动化

#### 浏览器自动化框架

- [RSelenium](https://docs.ropensci.org/RSelenium/)：R 对 [Selenium WebDriver](https://www.selenium.dev/) 的绑定。
- [chromote](https://github.com/rstudio/chromote)：R 的 Chrome 远程接口。
- [hayalbaz](https://github.com/rundel/hayalbaz)：一个 R 包，提供类似 puppeteer 的界面，通过 chromote 使用 Chrome 开发工具协议。
- [selenium-r](https://github.com/ashbythorpe/selenium-r)：一个低级浏览器自动化接口。

#### 工具和插件

- [parsel](https://github.com/till-tietz/parsel)：用于并行执行 RSelenium 的工具。


#### 其他

- [selenider](https://github.com/ashbythorpe/selenider)：一个为 chromote 和 selenium 提供简洁、惰性和可靠包装的工具。

### 数据导出

#### JSON

- [jsonlite](https://github.com/jeroen/jsonlite)：一个强大且高性能的 JSON 解析器和生成器。
- [geojson](https://github.com/ropensci/geojson)：R 的 GeoJSON 类。
- [yyjsonr](https://github.com/coolbutuseless/yyjsonr)：R 的一个快速 JSON 包。
- [rapidjsonr](https://cran.r-project.org/web/packages/rapidjsonr/index.html)：通过 [Rapidjson](https://github.com/Tencent/rapidjson/) C++ 库提供 JSON 解析功能的 R 包。
- [RJSONIO](https://cran.r-project.org/web/packages/RJSONIO/index.html)：支持将数据与 JSON 格式相互转换的包。
- [rjson](https://cran.r-project.org/web/packages/rjson/index.html)：用于将 R 对象与 JSON 对象相互转换的库。

#### CSV

- [csv](https://cran.r-project.org/web/packages/csv/index.html)：支持特定约定的 CSV 文件读写工具。
- [csvwr](https://github.com/Robsteranium/csvwr)：支持读写 CSVW（即 CSV 表格及其 JSON 元数据）的库。
- [csvy](https://github.com/leeper/csvy)：提供 CSVY 文件格式导入和导出的库。

#### 其他

- [cleanrmd](https://github.com/gadenbuie/cleanrmd)：清理无类的 R Markdown HTML 文档。
- [r-yaml](https://github.com/vubiostat/r-yaml/)：一个支持 R 对象与 YAML 格式相互转换的包。
- [df2yaml](https://cran.r-project.org/web/packages/df2yaml/index.html)：将数据框转换为 YAML 的工具。
- [xlsx](https://github.com/colearendt/xlsx)：通过 [Apache POI Java](https://poi.apache.org/) 库与 Excel 文件交互的 R 包。
- [writexl](https://cran.r-project.org/web/packages/writexl/index.html)：基于 [libxlsxwriter](https://libxlsxwriter.github.io) 的零依赖数据框到 xlsx 导出工具。

### 数据处理

#### 通用

- [tidyverse](https://github.com/tidyverse/tidyverse)：轻松安装并加载 tidyverse 中的包。

#### 表格数据

- [tinytable](https://github.com/vincentarelbundock/tinytable)：R 中简单且可定制的表格工具。

#### 字符编码

- [utf8](https://cran.r-project.org/web/packages/utf8/index.html)：处理和打印 UTF-8 编码国际文本的库。
- [base64](https://cran.r-project.org/web/packages/base64/index.html)：一个 Base64 编码和解码器。

#### 日期和时间

- [lubridate](https://github.com/tidyverse/lubridate)：简化日期操作的库。
- [date](https://cran.r-project.org/web/packages/date/index.html)：处理日期的函数。
- [datefixR](https://github.com/ropensci/datefixR)：一个标准化各种格式或缺失数据的日期工具。

#### 电话号码

- [dialr](https://github.com/socialresearchcentre/dialr)：解析、格式化和验证国际电话号码的库。

#### 其他

- [geojsonR](https://github.com/mlampros/geojsonR)：一个 GeoJSON 处理工具包。
- [jsonStrings](https://github.com/stla/jsonStrings)：R 中用于操作 JSON 字符串的库。
- [excel.link](https://github.com/gdemin/excel.link)：一个用于在 R 和 Microsoft Excel 之间便捷数据交换的工具。
- [officer](https://github.com/davidgohel/officer)：让 R 用户操作 Word (.docx) 和 PowerPoint (.pptx) 文档的包。

### 其他

#### 多进程

- [parallel](https://www.rdocumentation.org/packages/parallel/versions/3.6.2)：R 内置支持并行计算的库，包括通过分叉（取自 multicore 包）、套接字（取自 snow 包）和随机数生成。
- [parallelly](https://github.com/HenrikBengtsson/parallelly)：增强 parallel 包功能的库。
- [RcppThread](https://github.com/tnagler/RcppThread)：提供 C++11 风格的线程类和线程池，可安全地从 R 中中断。

#### 任务调度

- [cronR](https://github.com/bnosac/cronR)：管理 cron 任务的简单 R 包。
- [later](https://github.com/r-lib/later)：调度 R 函数或公式在指定时间段后运行的库。
- [taskscheduleR](https://github.com/bnosac/taskscheduleR)：使用 Windows 任务计划程序调度 R 脚本/进程的工具。
- [sched](https://gitlab.com/cnrgh/databases/r-sched)：提供类和函数，以在符合站点规则的前提下联系 Web 服务器的库。

## 常见网页抓取技术栈

### 静态网页

#### HTTP 客户端 + HTML 解析器

- **HTTP 客户端**：httr2 或 RCurl
- **HTML 解析器**：xml2

#### 一体化网页抓取框架


- rvest or Rcrawler

### Dynamic Web Pages

#### All-In-One Browser Automation Framework

- RSelenium

## Guides and Tutorials

- [A Hands-On Guide to Web Scraping in R](https://brightdata.com/blog/how-tos/web-scraping-with-r)
