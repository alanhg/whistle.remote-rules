# whistle.remote-rules

> 面对云IDE开发场景下，CI会根据IDE地址动态下发whistle rule配置文件，因此需要实现点击文件地址，从而本地可以动态加载代理，这样开发者不再需要维护该文件

[![npm version](https://badge.fury.io/js/whistle.remote-rules.svg)](https://badge.fury.io/js/whistle.remote-rules)

## design

- 针对whistle web服务，增加remoteRules参数解析，支持URL值，URL协议为HTTP/HTTPS
- 插件解析该参数并下载该rule
- 调用whistle加载该rule

## docs

- https://github.com/orgs/whistle-plugins/repositories
- https://github.com/avwo/lack
- https://wproxy.org/whistle/plugins.html

## get started

```
$ npm i -g lack

$ npm run dev

$ npm link

$ w2 stop

# 开启调试模式
$ w2 run

```

## Usage

```shell

$ npm i whistle -g

$ npm i whistle.remote-rules -g 
# or

$ w2 i whistle.remote-rules

```
自动加载远程规则，地址模版如下

`http://local.whistlejs.com/whistle.remote-rules/?remoteRules={url}`

举个例子

`http://local.whistlejs.com/whistle.remote-rules/?remoteRules=https%3A%2F%2Fgist.githubusercontent.com%2Falanhg%2Fa950d216121002d5bb0fd1278789da75%2Fraw%2Fc8bdf23e05c9dc504ea393a0b373cb556df911d8%2Ftest-whistle.js`
