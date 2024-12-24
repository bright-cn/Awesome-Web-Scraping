# JavaScript 网页抓取

本文档包含 JavaScript 中可用于网络爬取的库和资源列表。

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
    - [CSV 解析器](#csv-解析器)
    - [PDF 解析器](#pdf-解析器)
    - [HTTP 解析器](#http-解析器)
    - [邮件解析器](#邮件解析器)
    - [Markdown 解析器](#markdown-解析器)
    - [YAML 解析器](#yaml-解析器)
    - [SQL 解析器](#sql-解析器)
    - [Office 文件解析器](#office-文件解析器)
    - [其他](#其他-1)
  - [网络爬取](#网络爬取)
    - [框架](#框架)
    - [反机器人检测](#反机器人检测)
    - [代理集成](#代理集成)
    - [CAPTCHA 解决](#captcha-解决)
    - [用户代理伪装](#用户代理伪装)
  - [网络自动化](#网络自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
    - [工具和插件](#工具和插件)
    - [其他](#其他-2)
  - [数据导出](#数据导出)
    - [JSON](#json)
    - [CSV](#csv)
    - [其他](#其他-3)
  - [数据处理](#数据处理)
    - [字符编码](#字符编码)
    - [日期与时间](#日期与时间)
    - [价格](#价格)
    - [电话号码](#电话号码)
    - [Slugs](#slugs)
    - [语言](#语言)
  - [其他](#其他-4)
    - [任务调度](#任务调度)
- [常用网络爬虫技术栈](#常用网络爬虫技术栈)
  - [静态网页](#静态网页)
    - [HTTP 客户端 + HTML 解析器](#http-客户端-html-解析器)
    - [一体化网络爬取框架](#一体化网络爬取框架)
  - [动态网页](#动态网页)
- [指南和教程](#指南和教程)
  - [通用指南](#通用指南)
  - [代理](#代理)
  - [用户代理设置](#用户代理设置)
  - [反机器人绕过](#反机器人绕过)
  - [对比](#对比)

---

## 库

**注意**：以下列出的所有库都处于活跃维护状态。

### 网络

#### HTTP 客户端

- [fetch](https://nodejs.org/dist/latest/docs/api/globals.html#fetch)：Node.js 内置的、与浏览器兼容的 [`fetch()`](https://developer.mozilla.org/en-US/docs/Web/API/Window/fetch) 函数实现。
- [axios](https://github.com/axios/axios)：基于 `Promise` 的浏览器和 Node.js HTTP 客户端 [**[Axios 代理集成](https://bright.cn/blog/how-tos/axios-proxy)**]
- [node-fetch](https://github.com/bitinn/node-fetch)：将 Fetch API 带到 Node.js 的轻量级模块 [**[node-fetch 代理集成](https://bright.cn/blog/proxy-101/proxy-in-node-fetch)**]
- [undici](https://www.npmjs.com/package/undici)：为 Node.js 从零编写的 HTTP/1.1 客户端
- [superagent](https://github.com/visionmedia/superagent)：一个小巧、渐进式的客户端 HTTP 请求库，同时也是 Node.js 模块，提供大量高级 HTTP 客户端功能 [**[SuperAgent 代理集成](https://bright.cn/blog/how-tos/superagent-proxy)**]
- [urllib](https://github.com/node-modules/urllib)：在复杂网络环境中请求 HTTP(s) URL 的库
- [node-libcurl](https://github.com/JCMais/node-libcurl)：Node.js 对 [libcurl](https://curl.se/libcurl/) 的绑定
- [got](https://github.com/sindresorhus/got)：一个对人类友好且功能强大的 Node.js HTTP 请求库
- [bent](https://github.com/mikeal/bent)：一个基于 async/await 的函数式 Node.js HTTP 客户端
- [needle](https://github.com/tomas/needle)：一个灵活可流式的 Node.js HTTP 客户端，支持代理、iconv、cookie、deflate & multipart 等功能

#### WebSockets

- [ws](https://github.com/websockets/ws)：一个易用、高速并且经过全面测试的 Node.js WebSocket 客户端和服务器
- [WebScoket-Node](https://github.com/theturtle32/WebSocket-Node)：一个 Node.JS 的 WebSocket 实现（Draft -08 一直到最终的 RFC 6455）

#### 底层网络

- [node:net](https://nodejs.org/api/net.html)：Node.js 内置模块，提供基于流的 TCP 或 IPC 服务器和客户端的异步网络 API
- [multicast-dns](https://github.com/mafintosh/multicast-dns)：纯 JavaScript 的低级多播 DNS 实现
- [node-ip](https://github.com/indutny/node-ip)：Node.js 的 IP 地址工具

#### 其他

- [wreck](https://github.com/hapijs/wreck)：为 [hapi](https://hapi.dev/) Web 框架提供的 HTTP 客户端工具
- [proxy-chain](https://github.com/apify/proxy-chain)：Node.js 的代理服务器实现（类似 Squid），支持 SSL、身份验证和上游代理链

### 解析器

#### HTML/XML 解析器

- [cheerio](https://github.com/cheeriojs/cheerio)：一个快速、灵活且优雅的 HTML/XML 解析与操作库
- [fast-xml-parser](https://github.com/NaturalIntelligence/fast-xml-parser)：无需 C/C++ 库，无回调的快速 XML 验证、解析、构建库
- [node-html-parser](https://github.com/taoqf/node-html-parser)：一个非常快速的 HTML 解析器，生成简化的 DOM，并支持基础元素查询
- [html-dom-parser](https://github.com/remarkablemark/html-dom-parser)：将 HTML 转换为 DOM 的解析器
- [parse5](https://github.com/inikulin/parse5)：Node.js 的 HTML 解析/序列化工具集，符合 WHATWG HTML Living Standard
- [htmlparser2](https://github.com/fb55/htmlparser2)：一个快速且兼容性较好的 HTML 与 XML 解析器
- [sax-js](https://github.com/isaacs/sax-js)：JavaScript 的 SAX 风格解析器

#### URL 解析器

- [node:url](https://nodejs.org/api/url.html)：Node.js 内置模块，提供 URL 解析和解析功能
- [query-string](https://github.com/sindresorhus/query-string)：一个用于解析和字符串化 URL 查询字符串的库
- [URI.js](https://github.com/medialize/URI.js/)：一个 JavaScript 的 URL 变换库

#### CSV 解析器

- [csv-parse](https://github.com/adaltas/node-csv/tree/master/packages/csv-parse)：将 CSV 文本输入解析成数组或对象的解析器
- [fast-csv](https://github.com/C2FO/fast-csv)：Node.js 的 CSV 解析器和格式化程序

#### PDF 解析器

- [pdf-parse](https://gitlab.com/autokent/pdf-parse)：纯 JavaScript 的跨平台 PDF 文本提取模块
- [pdf2json](https://github.com/modesty/pdf2json)：将二进制 PDF 转换为 JSON 和文本的库，用于服务端 PDF 处理及命令行使用

#### HTTP 解析器

- [http-parser-js](https://github.com/creationix/http-parser-js)：一个纯 JavaScript 编写的 Node.js HTTP 解析器

#### 邮件解析器

- [email-reply-parser](https://github.com/crisp-oss/email-reply-parser)：一个 Node.js 库，用于解析纯文本电子邮件内容
- [email-forward-parser](https://github.com/crisp-oss/email-forward-parser)：解析转发邮件并提取原始内容的库
- [node-address-rfc2822](https://github.com/haraka/node-address-rfc2822)：一个解析 RFC2822（Header）格式邮件地址的工具
- [smtp-address-parser](https://github.com/gene-hightower/smtp-address-parser)：一个解析 SMTP（RFC-5321）地址的库

#### Markdown 解析器

- [markdown-it](https://github.com/markdown-it/markdown-it)：一个正确的Markdown解析器，100% CommonMark支持，扩展与插件、高速
- [marked](https://github.com/markedjs/marked)：一个 Markdown 解析器与编译器，追求高效
- [micromark](https://github.com/micromark/micromark/tree/main)：一个小巧、安全、兼容 CommonMark（可选 GFM）的 Markdown 解析器

#### YAML 解析器

- [yaml](https://github.com/eemeli/yaml)：一个 JavaScript 的 YAML 解析和字符串化库
- [js-yaml](https://github.com/nodeca/js-yaml)：JavaScript 实现的 YAML 解析与转储工具，非常快速
- [yaml-eslint-parser](https://github.com/ota-meshi/yaml-eslint-parser)：一个使输出与 ESLint 兼容的 YAML 解析器

#### SQL 解析器

- [node-sql-parser](https://github.com/taozhi8833998/node-sql-parser)：解析简单的SQL语句为AST（抽象语法树），并可逆转换回SQL
- [js-sql-parser](https://www.npmjs.com/package/js-sql-parser)：使用 [jison](https://github.com/zaach/jison) 编写的 SQL 解析器，可将 SQL 解析为 AST，再转换回 SQL

#### Office 文件解析器

- [xlsx](https://github.com/SheetJS/sheetjs)：一个用于解析和写入电子表格数据的库
- [exceljs](https://github.com/exceljs/exceljs)：可读写 XLSX 与 JSON，支持对数据及样式的处理
- [docx](https://github.com/dolanmiu/docx)：一个以 JS/TS 容易操作 .docx 文件的库，提供声明式 API，可在Node.js或浏览器中使用

#### 其他

- [robots-parser](https://github.com/samclarke/robots-parser)：支持通配符（\*）匹配的 Node.js robots.txt 解析器
- [sitemapper](https://github.com/seantomburke/sitemapper)：解析 XML Sitemaps，可搭配 robots.txt 与爬虫使用
- [ip-address](https://github.com/beaugunderson/ip-address)：解析并操作 IPv4 和 IPv6 地址的 JavaScript 库
- [feed-extractor](https://github.com/extractus/feed-extractor)：最简单方式读取并规范化 RSS/ATOM/JSON feed 数据
- [sanitize-html](https://github.com/apostrophecms/sanitize-html)：清理用户提交的HTML，根据白名单保留安全元素和属性，基于htmlparser2，高速且容错
- [parse-css](https://github.com/tabatkins/parse-css)：基于标准的 CSS 解析器
- [js-xss](https://github.com/leizongmin/js-xss)：一个通过白名单配置，清理不受信HTML（防XSS）的库

### 网络爬取

#### 框架

- [crawlee](https://github.com/apify/crawlee)：Node.js 的网络爬取和浏览器自动化库，支持 JavaScript 和 TypeScript。可提取数据（AI、LLM、RAG或GPT），支持下载 HTML、PDF、JPG、PNG 等文件。兼容 Puppeteer、Playwright、Cheerio、JSDOM、原生HTTP，支持有头和无头模式，并且带代理轮换功能
- [node-crawler](https://github.com/sylvinus/node-crawler)：一个 Node.js + 服务端 jQuery 的爬虫/蜘蛛
- [ayakashi](https://github.com/ayakashi-io/ayakashi)：下一代网络爬取框架
- [webster](https://github.com/zhuyingda/webster)：一个可靠的高级 Node.js 爬取与抓取框架

#### 反机器人检测

- [node-curl-impersonate](https://www.npmjs.com/package/node-curl-impersonate)：本地使用 [curl-impersonate](https://github.com/lwthiker/curl-impersonate) 的库
- [cloudflare-scraper](https://github.com/JimmyLaurent/cloudflare-scraper)：绕过 Cloudflare 防护的包
- [unblocker](https://github.com/nfriedly/node-unblocker)：一个网络代理，用于规避互联网审查和常规 Node.js 库，可对远程网页进行代理和重写

#### 代理集成

- [Bright Data的代理服务](https://bright.cn/proxy-types)：一个拥有超过7200万个 IP 的代理网络，提供高质量住宅、数据中心、移动、ISP 代理，支持州、国家、ZIP、ASN级别的定位，覆盖195个国家，适用于任意HTTP客户端或爬虫库 [**Bright Data 的解决方案**]

#### CAPTCHA 解决

- [CAPTCHA Solver](https://bright.cn/products/web-unlocker/captcha-solver)：一个快速、自动化的CAPTCHA解决方案，可处理reCAPTCHA、hCaptcha、px_captcha、SimpleCaptcha、GeeTest等 [**Bright Data的解决方案**]
- [nopecha-nodejs](https://github.com/NopeCHALLC/nopecha-nodejs)：Node.js 的自动化CAPTCHA解决方案
- [2captcha](https://github.com/Furry/2captcha)：对 2Captcha API 的封装
- [2captcha-javascript](2captcha-javascript)：一个 JavaScript 库，用于简单集成 2captcha 验证码解决服务，以绕过 reCAPTCHA、hCaptcha、FunCaptcha、Geetest 等

#### 用户代理伪装

- [user-agents](https://github.com/intoli/user-agents)：一个JavaScript库，生成随机用户代理，并每天更新数据

### 网络自动化

#### 浏览器自动化框架

- [puppeteer](https://github.com/GoogleChrome/puppeteer)：一个JavaScript库，提供高级API，通过[DevTools Protocol](https://chromedevtools.github.io/devtools-protocol/)或[WebDriver BiDi](https://pptr.dev/webdriver-bidi)控制Chrome或Firefox [**[Puppeteer 代理集成](https://bright.cn/integration/puppeteer)**]
- [playwright](https://github.com/microsoft/playwright)：一个用于Web测试与自动化的框架，可在 Chromium、Firefox、WebKit 上进行测试 [**[Playwright 代理集成](https://bright.cn/integration/playwright)**]
- [selenium](https://github.com/SeleniumHQ/selenium)：一个浏览器自动化框架与生态系统 [**[Selenium 代理集成](https://bright.cn/integration/selenium)**]
- [cypress](https://github.com/cypress-io/cypress)：一个快速、简单且可靠的前端测试工具，适合在浏览器中运行的一切
- [webdriverio](https://github.com/webdriverio/webdriverio)：面向Node.js的下一代浏览器和移动端自动化测试框架
- [wendigo](https://github.com/angrykoala/wendigo)：一个适用于前端自动化测试的强力“怪物”

#### 工具和插件

- [puppeteer-extra-plugin-stealth](https://github.com/berstend/puppeteer-extra/tree/master/packages/puppeteer-extra-plugin-stealth)：puppeteer-extra 和 playwright-extra 的防检测插件
- [puppeteer-extra-plugin-anonymize-ua](https://github.com/berstend/puppeteer-extra/tree/master/packages/puppeteer-extra-plugin-anonymize-ua)：puppeteer-extra 和 playwright-extra 的插件，用于在所有页面上匿名化 User-Agent
- [@extra/proxy-router](https://github.com/berstend/puppeteer-extra/tree/master/packages/plugin-proxy-router)：playwright-extra 和 puppeteer-extra 的插件，用于动态路由代理
- [puppeteer-extra-plugin-block-resources](https://github.com/berstend/puppeteer-extra/tree/master/packages/puppeteer-extra-plugin-block-resources)：playwright-extra 和 puppeteer-extra 的插件，用于阻止资源（图像、媒体、CSS 等）

#### 其他

- [playwright-extra](https://github.com/berstend/puppeteer-extra/tree/39248f1f5deeb21b1e7eb6ae07b8ef73f1231ab9/packages/playwright-extra)：Playwright的模块化插件框架，可通过干净的接口使用各种插件
- [puppeteer-extra](https://github.com/berstend/puppeteer-extra)：一个通过插件为 puppeteer 添加新功能的库

### 数据导出

#### JSON

- [JSON](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON)：JavaScript 内置的JSON命名空间，包含从JSON解析和将数据转换为JSON的方法

#### CSV

- [csv-generate](https://github.com/adaltas/node-csv/tree/master/packages/csv-generate)：实现 Node.js [`stream.Readable`](https://nodejs.org/api/stream.html#class-streamreadable) API 的随机CSV字符串和JS对象生成器

#### 其他

- [protobuf.js](https://github.com/protobufjs/protobuf.js)：JavaScript & TypeScript 的 Protocol Buffers 库
- [jBinary](https://github.com/jDataView/jBinary)：一个高层API，用于操作二进制数据

### 数据处理

#### 字符编码

- [encoding.js](https://github.com/polygonplanet/encoding.js)：一个将文本转换并检测字符编码的 JavaScript 库
- [chardet](https://github.com/runk/node-chardet)：Node.js 的字符编码检测工具
- [iconv-lite](https://github.com/ashtuchkin/iconv-lite)：纯JavaScript的字符编码转换库

#### 日期与时间

- [dayjs](https://github.com/iamkun/dayjs)：一个2kB大小、不可变的日期库，可替代 Moment.js，具有相同的现代API
- [date-fns](https://github.com/date-fns/date-fns)：一个现代的JavaScript日期实用程序库
- [luxon](https://github.com/moment/luxon)：用于在JS中处理日期与时间的库

#### 价格

- [money.js](https://github.com/openexchangerates/money.js)：一个体积小(1kb)的JS货币转换库，适用于Web & Node.js
- [currency.js](https://github.com/scurker/currency.js)：一个处理货币的JavaScript库

#### 电话号码

- [libphonenumber-js](https://gitlab.com/catamphetamine/libphonenumber-js)：Google Android libphonenumber简化与瘦身的JS重写
- [phone](https://github.com/aftership/phone)：验证并将移动电话号码转为E.164标准格式的库

#### Slugs

- [unique-slug](https://github.com/npm/unique-slug)：一个可对UTF-8字符进行slug化的库
- [unique-slug](https://github.com/npm/unique-slug)：（同名）生成适用于文件和URL的唯一字符串的库

#### 语言

- [remove-accents](https://github.com/tyxla/remove-accents)：从字符串中移除重音符号，转换成对应的非重音字符
- [nodejieba](https://github.com/yanyiwu/nodejieba)：Node.js 的中文分词库

### 其他

#### 任务调度

- [node-schedule](https://github.com/node-schedule/node-schedule)：一个与cron类似，且也可非cron形式运行的Node任务调度器
- [node-cron](https://github.com/node-cron/node-cron)：Node.js 的简易cron任务调度器
- [bree](https://github.com/breejs/bree)：基于worker threads、cron、Date和类人类语法的 Node.js/JavaScript任务调度器
- [cron](https://github.com/kelektiv/node-cron)：一个基于cron语法的强大任务调度工具，可定时运行函数或命令

## 常用网络爬虫技术栈

### 静态网页

#### HTTP 客户端 + HTML 解析器

- **HTTP 客户端**：Axios、node-fetch、fetch 或 SuperAgent
- **HTML 解析器**：Cheerio

#### 一体化网络爬取框架

- Crawlee

### 动态网页

- Playwright、Puppeteer、Selenium 或 Cypress

## 指南和教程

### 通用指南

- [使用 JavaScript 和 Node.js 进行网页抓取指南](https://bright.cn/blog/how-tos/web-scraping-with-node-js)
- [2024 年在 Next.JS 中进行网页抓取](https://bright.cn/blog/how-tos/web-scraping-with-next-js)
- [Crawlee 网页抓取：分步教程](https://bright.cn/blog/web-data/web-scraping-with-crawlee)
- [使用 Cheerio NPM 进行网页抓取](https://bright.cn/blog/how-tos/cheerio-npm-web-scraping)
- [Playwright 网页抓取 - 2024 指南](https://bright.cn/blog/how-tos/playwright-web-scraping)
- [Puppeteer 网页抓取 - 2024 指南](https://bright.cn/blog/how-tos/web-scraping-puppeteer)
- [在 Node.js 中使用 Fetch API 进行 HTTP 请求](https://bright.cn/blog/how-tos/fetch-api-nodejs)

### 代理

- [在 Axios 中设置代理：完整指南](https://bright.cn/blog/how-tos/axios-proxy)
- [在 SuperAgent 中设置代理](https://bright.cn/blog/how-tos/superagent-proxy)
- [在 Node-Fetch 中使用代理教程](https://bright.cn/blog/proxy-101/proxy-in-node-fetch)
- [在 Node.js 中使用代理服务器](https://bright.cn/blog/how-tos/nodejs-proxy-servers)

### 用户代理设置

- [Puppeteer 用户代理指南：设置和修改](https://bright.cn/blog/web-data/puppeteer-user-agent)
- [Node.js 用户代理指南：设置和修改](https://bright.cn/blog/web-data/node-js-user-agent)

### 反机器人绕过

- [使用 Playwright Stealth 避免被检测](https://bright.cn/blog/how-tos/avoid-bot-detection-with-playwright-stealth)
- [在 Puppeteer 中避免被屏蔽的隐身模式](https://bright.cn/blog/how-tos/avoid-getting-blocked-with-puppeteer-stealth)
- [如何用 Playwright 绕过 CAPTCHA](https://bright.cn/blog/web-data/bypass-captchas-with-playwright)
- [在网页抓取中使用 Node Unblocker](https://bright.cn/blog/how-tos/node-unblocker-web-scraping)

### 对比

- [JavaScript vs Python：网页抓取对比](https://bright.cn/blog/web-data/javascript-vs-python)
- [C# vs JavaScript：哪个更适合网络爬取？](https://bright.cn/blog/web-data/c-sharp-vs-javascript)
- [JavaScript vs Rust 网页抓取对比](https://bright.cn/blog/web-data/javascript-vs-rust-web-scraping)
- [Cheerio vs. Puppeteer：网页抓取对比](https://bright.cn/blog/web-data/cheerio-vs-puppeteer)
- [Puppeteer vs. Selenium - 如何选择？](https://bright.cn/blog/proxy-101/puppeteer-vs-selenium)
- [Scrapy vs Puppeteer：网页抓取对比](https://bright.cn/blog/web-data/scrapy-vs-puppeteer)
- [Playwright vs. Selenium 2024 对比](https://bright.cn/blog/web-data/playwright-vs-selenium)
- [Puppeteer vs Playwright：网页抓取对比](https://bright.cn/blog/web-data/puppeteer-vs-playwright)
