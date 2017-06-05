# f2e-server
f2e-server 2.0

## Install
`npm i -g shy2850/f2e-server`

## Options
- `f2e start`
- `f2e -h`
- `f2e start -h`

## Config
在启动目录的配置文件 `.f2econfig.js`
支持接入 [Koa](http://koajs.com/) 以及 [express](https://expressjs.com/)

```
const Koa = require('koa')
const app = new Koa()

app.use(ctx => {
	ctx.body = __dirname
})


const express = require('express')
const app1 = express()

app1.get('/', function (req, res) {
  	res.send(__dirname)
})

app1.use(express.static('lib'))

module.exports = {
	// app: app.callback(),
	app: app1
}
```
