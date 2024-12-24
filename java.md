# Java网络爬取

本文档列出了用于Java网络爬取的库和资源。

## 目录

- [库](#库)
  - [网络](#网络)
    - [HTTP和WebSocket客户端](#http和websocket客户端)
    - [WebSocket](#websocket)
    - [低级网络](#低级网络)
  - [解析器](#解析器)
    - [通用解析器](#通用解析器)
    - [HTML解析器](#html解析器)
    - [XML解析器](#xml解析器)
    - [URL解析器](#url解析器)
    - [CSV解析器](#csv解析器)
    - [JSON解析器](#json解析器)
    - [电子邮件解析器](#电子邮件解析器)
    - [Markdown解析器](#markdown解析器)
    - [YAML解析器](#yaml解析器)
    - [SQL解析器](#sql解析器)
    - [Office文件解析器](#office文件解析器)
    - [其他解析器](#其他解析器)
  - [网络爬取](#网络爬取)
    - [框架](#框架)
    - [代理集成](#代理集成)
    - [验证码解决方案](#验证码解决方案)
  - [网络自动化](#网络自动化)
    - [浏览器自动化框架](#浏览器自动化框架)
    - [其他工具](#其他工具)
  - [数据处理](#数据处理)
    - [通用数据处理](#通用数据处理)
    - [字符编码](#字符编码)
    - [JSON处理](#json处理)
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
    - [一体化解决方案](#一体化解决方案)
  - [动态网页](#动态网页)
- [指南和教程](#指南和教程)
  - [通用指南](#通用指南)
  - [对比分析](#对比分析)

## 库

### 网络

#### HTTP和WebSocket客户端

- **[HttpClient](https://docs.oracle.com/en/java/javase/23/docs/api/java.net.http/java/net/http/HttpClient.html)**：Java 11内置的HTTP客户端，用于发送请求和接收响应。
- **[Apache HttpClient](https://github.com/apache/httpcomponents-client)**：适用于Java的同步HTTP和WebSocket客户端库。
- **[OkHttp](https://github.com/square/okhttp)**：适用于JVM和Android的高效HTTP客户端。

#### WebSocket

- **[Java-WebSocket](https://github.com/TooTallNate/Java-WebSocket)**：用Java编写的轻量级WebSocket客户端和服务器实现。

#### 低级网络

- **[pcap4j](https://github.com/kaitoy/pcap4j)**：Java库，用于捕获、构建和发送网络数据包。

### 解析器

#### HTML解析器

- **[Jsoup](https://github.com/jhy/jsoup)**：Java HTML解析器，用于HTML编辑、清理、爬取和安全性增强。

#### JSON解析器

- **[JSON Path](https://github.com/json-path/JsonPath)**：用于读取JSON文档的Java DSL。

### 网络爬取

#### 框架

- **[Apache Nutch](https://github.com/apache/nutch)**：可扩展的网络爬取框架。
- **[WebMagic](https://github.com/code4craft/webmagic)**：可扩展的Java网络爬取框架。

#### 代理集成

- **[Bright Data的代理服务](https://brightdata.com/proxy-types)**：提供7200万个IP的代理网络，支持高精度地理定位。

#### 验证码解决方案

- **[Bright Data验证码解决方案](https://brightdata.com/products/web-unlocker/captcha-solver)**：快速、自动化的验证码解决方案。

### 网络自动化

#### 浏览器自动化框架

- **[Selenium](https://github.com/SeleniumHQ/selenium)**：流行的浏览器自动化框架。
- **[Playwright](https://github.com/microsoft/playwright-java)**：跨浏览器自动化框架的Java版本。

### 数据处理

#### JSON处理

- **[Jackson](https://github.com/FasterXML/jackson)**：Java平台上强大的JSON解析和生成库。

#### 日期和时间处理

- **[Joda-Time](https://github.com/JodaOrg/joda-time)**：Java日期和时间处理的广泛使用替代库。

#### 电话号码处理

- **[libphonenumber](https://github.com/google/libphonenumber)**：国际电话号码解析和验证库。

## 常用网络爬取技术栈

### 静态网页

#### HTTP客户端+HTML解析器

- **HTTP客户端**：推荐HttpClient或Apache HttpClient。
- **HTML解析器**：推荐Jsoup。

#### 一体化解决方案

- **Jsoup**

### 动态网页

- 推荐使用**Selenium**或**Playwright**。

## 指南和教程

### 通用指南

- [Java网络爬取完整指南2024](https://brightdata.com/blog/how-tos/java-web-scraping)
- [使用Jsoup进行Java网络爬取：分步指南](https://brightdata.com/blog/how-tos/web-scraping-with-jsoup)

### 对比分析

- [Java与Python的对比指南](https://brightdata.com/blog/web-data/java-vs-python)
- [Playwright与Selenium对比分析2024](https://brightdata.com/blog/web-data/playwright-vs-selenium)