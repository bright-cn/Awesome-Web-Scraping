# JavaScript 网络爬取

本文档列出了用于JavaScript网络爬取的库和资源。

## 目录

- [库](#库)
  - [网络](#网络)
    - [HTTP客户端](#http客户端)
    - [WebSocket](#websocket)
    - [低级网络](#低级网络)
    - [其他](#其他)
  - [解析器](#解析器)
    - [HTML/XML解析器](#htmlxml解析器)
    - [URL解析器](#url解析器)
    - [CSV解析器](#csv解析器)
    - [PDF解析器](#pdf解析器)
    - [HTTP解析器](#http解析器)
    - [电子邮件解析器](#电子邮件解析器)
    - [Markdown解析器](#markdown解析器)
    - [YAML解析器](#yaml解析器)
    - [SQL解析器](#sql解析器)
    - [Office文件解析器](#office文件解析器)
    - [其他解析器](#其他解析器)
  - [网络爬取](#网络爬取)
    - [框架](#框架)
    - [反机器人检测](#反机器人检测)
    - [代理集成](#代理集成)
    - [验证码解决方案](#验证码解决方案)
    - [用户代理伪装](#用户代理伪装)
  - [网络自动化](#网络自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
    - [工具和插件](#工具和插件)
    - [其他工具](#其他工具)
  - [数据导出](#数据导出)
    - [JSON](#json)
    - [CSV](#csv)
    - [其他导出](#其他导出)
  - [数据处理](#数据处理)
    - [字符编码](#字符编码)
    - [日期和时间处理](#日期和时间处理)
    - [价格处理](#价格处理)
    - [电话号码处理](#电话号码处理)
    - [Slug生成](#slug生成)
    - [语言处理](#语言处理)
  - [其他功能](#其他功能)
    - [任务调度](#任务调度)
- [常用网络爬取技术栈](#常用网络爬取技术栈)
  - [静态网页](#静态网页)
    - [HTTP客户端+HTML解析器](#http客户端html解析器)
    - [一体化网络爬取框架](#一体化网络爬取框架)
  - [动态网页](#动态网页)
- [指南和教程](#指南和教程)
  - [通用指南](#通用指南)
  - [代理教程](#代理教程)
  - [用户代理设置](#用户代理设置)
  - [反机器人检测](#反机器人检测-1)
  - [对比分析](#对比分析)

## 库

### 网络

#### HTTP客户端

- **[fetch](https://nodejs.org/dist/latest/docs/api/globals.html#fetch)**：Node.js内置的与浏览器兼容的[`fetch()`](https://developer.mozilla.org/zh-CN/docs/Web/API/Window/fetch)函数实现。
- **[axios](https://github.com/axios/axios)**：一个基于`Promise`的浏览器和Node.js HTTP客户端 [**[Axios代理集成](https://brightdata.com/blog/how-tos/axios-proxy)**]。
- **[node-fetch](https://github.com/bitinn/node-fetch)**：一个轻量级模块，将Fetch API带到Node.js [**[node-fetch代理集成](https://brightdata.com/blog/proxy-101/proxy-in-node-fetch)**]。
- **[got](https://github.com/sindresorhus/got)**：一个人性化且强大的Node.js HTTP请求库。

#### WebSocket

- **[ws](https://github.com/websockets/ws)**：一个简单、快速且经过严格测试的Node.js WebSocket客户端和服务器。

#### 低级网络

- **[node:net](https://nodejs.org/api/net.html)**：Node.js内置模块，提供创建基于TCP或IPC服务器和客户端的异步网络API。

### 解析器

#### HTML/XML解析器

- **[cheerio](https://github.com/cheeriojs/cheerio)**：一个快速、灵活且优雅的HTML和XML解析与操作库。

#### CSV解析器

- **[csv-parse](https://github.com/adaltas/node-csv/tree/master/packages/csv-parse)**：一个将CSV文本输入解析为数组或对象的解析器。

#### JSON解析器

- **[JSON](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/JSON)**：JavaScript内置的JSON解析与转换工具。

### 网络爬取

#### 框架

- **[crawlee](https://github.com/apify/crawlee)**：Node.js的网络爬取和浏览器自动化库，用于构建可靠的爬虫。支持Puppeteer、Playwright、Cheerio等。

#### 反机器人检测

- **[cloudflare-scraper](https://github.com/JimmyLaurent/cloudflare-scraper)**：绕过Cloudflare保护的库。
- **[unblocker](https://github.com/nfriedly/node-unblocker)**：一个用于规避互联网审查的网络代理工具。

#### 代理集成

- **[Bright Data代理服务](https://brightdata.com/proxy-types)**：提供超过7200万个IP的代理网络，支持高精度地理定位 [**Bright Data解决方案**]。

#### 验证码解决方案

- **[CAPTCHA Solver](https://brightdata.com/products/web-unlocker/captcha-solver)**：快速、自动化的验证码解决方案。

#### 用户代理伪装

- **[user-agents](https://github.com/intoli/user-agents)**：一个JavaScript库，用于生成随机用户代理。

### 网络自动化

#### 浏览器自动化框架

- **[puppeteer](https://github.com/GoogleChrome/puppeteer)**：用于通过DevTools Protocol控制Chrome或Firefox的JavaScript库 [**[Puppeteer代理集成](https://brightdata.com/integration/puppeteer)**]。
- **[playwright](https://github.com/microsoft/playwright)**：跨浏览器自动化框架，支持测试Chromium、Firefox和WebKit [**[Playwright代理集成](https://brightdata.com/integration/playwright)**]。
- **[selenium](https://github.com/SeleniumHQ/selenium)**：浏览器自动化框架和生态系统 [**[Selenium代理集成](https://brightdata.com/integration/selenium)**]。

## 常用网络爬取技术栈

### 静态网页

#### HTTP客户端+HTML解析器

- **HTTP客户端**：推荐Axios、node-fetch或SuperAgent。
- **HTML解析器**：推荐Cheerio。

#### 一体化网络爬取框架

- **Crawlee**

### 动态网页

- 推荐使用Playwright、Puppeteer或Selenium。

## 指南和教程

### 通用指南

- [JavaScript和Node.js网络爬取指南](https://brightdata.com/blog/how-tos/web-scraping-with-node-js)
- [使用Crawlee进行网络爬取：分步教程](https://brightdata.com/blog/web-data/web-scraping-with-crawlee)
- [Puppeteer网络爬取 - 2024指南](https://brightdata.com/blog/how-tos/web-scraping-puppeteer)

### 代理教程

- [如何在Axios中设置代理](https://brightdata.com/blog/how-tos/axios-proxy)
- [在Node.js中使用代理服务器](https://brightdata.com/blog/how-tos/nodejs-proxy-servers)

### 用户代理设置

- [Puppeteer用户代理指南](https://brightdata.com/blog/web-data/puppeteer-user-agent)

### 反机器人检测

- [使用Playwright Stealth避免机器人检测](https://brightdata.com/blog/how-tos/avoid-bot-detection-with-playwright-stealth)

### 对比分析

- [JavaScript与Python网络爬取对比](https://brightdata.com/blog/web-data/javascript-vs-python)
- [Puppeteer与Selenium对比](https://brightdata.com/blog/proxy-101/puppeteer-vs-selenium)