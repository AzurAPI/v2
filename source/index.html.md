---
title: Manual

language_tabs: # must be one of https://git.io/vQNgJ
  - javascript: Javascript
  - python: Python
  - csharp: C#
  - kotlin: Kotlin


toc_footers:
  - <a href='https://github.com/AzurAPI'>GitHub Organisation</a>
  - <a href='https://github.com/slatedocs/slate'>Powered by Slate</a>

includes:
  - database
  - ship
  - equipment
  - Voicelines
  - Barrage
  - Chapter
  - support

search: true

code_clipboard: true
---

# Introduction
> To install a library, please open your project in a terminal and use the following commands:

```javascript
npm install @azurapi/azurapi
//or
yarn add @azurapi/azurapi
```
```kotlin
//maven
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>
<dependency>
    <groupId>com.github.AzurAPI</groupId>
    <artifactId>AzurApi-Kotlin</artifactId>
    <version>Tag</version>
</dependency>
//gradle
repositories {
    maven(url = "https://jitpack.io")
}
dependencies {
    implementation("com.github.AzurAPI:AzurApi-Kotlin:Tag")
}
```
```python
pip install azurlane
```
```csharp
// dotnet add package AzurAPINet --version 2.0.0-preview1
//  - refer to https://www.nuget.org/packages/AzurAPINet/
```
Welcome to AzurAPI!
<aside class="notice">
This page is updated frequently according of our packages, please refer to this page to be keep up to date with the latest version of the libraries we've made.
</aside>

This project was made by a community of developers by developers who wanted to make a free database accessable to everyone for fetching any kind of data from Azur Lane's wiki. It can curate to web designers, bot developers, or mobile-based applications.

The documentation here states all functions avaliable to support you in development of the product you're trying to create. For starters, when fetching data, it returns a payload that is structured in JSON format, so keep that in mind of what library you're using. It's important to update the cache every once a while due to breaking changes of the API.

[![NPM](https://nodei.co/npm/@azurapi/azurapi.png?mini=true)](https://nodei.co/npm/@azurapi/azurapi/)
[![PyPI version](https://badge.fury.io/py/azurlane.svg)](https://badge.fury.io/py/azurlane)
[![Kotlin Version](https://jitpack.io/v/AzurAPI/AzurApi-Kotlin.svg?style=flat-square)](https://jitpack.io/#AzurAPI/AzurApi-Kotlin)
[![NuGet Preview Version](http://img.shields.io/nuget/vpre/AzurAPINet)](https://www.nuget.org/packages/AzurAPINet/)
