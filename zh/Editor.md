
# 如何配置相


## 1. 新建一个相


## 2. 填写应用信息

| 字段   | 说明 |
| ----- | ---- |
| 应用名字  | **必填** 网站的名字，将显示在 App 的标题栏中 | 
| 图标地址  | 网站的图表，不填将自动请求默认位置的 `favicon.ico` | 
| 起始地址  | 打开「相」时将自动请求该地址，可以是主域名，也可以是一个页面地址，比如 `/trending` 这种 | 
| UA      | 默认请求手机页面，如果您想针对网站版的结果，可以选择 `desktop` | 
| Encoding  | 网站编码，有些 gbk 编码的网站显示乱码的情况下可以在这儿选择 gbk | 
| 匹配域名   | 除 `起始地址` 域名之外，额外匹配这些域名，可以使用 `*` 通配符，比如 `*.google.com` |
| 搜索地址   | 用来注册新的搜索引擎，你可以使用 `{q}` 来作为搜索占位符，比如 `http://baidu.com/s?wd={q}` |
| 作者   | 您的名字将显示在应用信息里面 |
| 简单介绍   | 简单介绍下您的应用 |
| 联系方式   | 可以随便留下一段文本 |



## 相的匹配规则

无相在`应用模式`和`浏览器模式`遇到一个请求时会查找已启用的「相」的域名配置，如果有域名匹配会继续查找匹配的`页面`，
如果有的话就会自动启动应用模式。

1. 如果填了 `起始地址` 将匹配这个地址的域名
2. 匹配域名：你还可以在这里添加额外的域名，最常见的比如 `m.*.com` —— 网站的手机版，以及有些新闻网站会针对不同的版块启用不同的子域名，但是页面布局一样。



## 页面配置

### 页面匹配

在上一步，无相匹配到一个域名后，将会继续检查 `匹配 URL` 寻找组件信息。这里可以添加多个，并且可以使用 `*` 通配符。


需要注意的是， 一个 `*`  并不包括 `/`，两个 `**` 则可以。

- `/*.html` 只匹配 `/a.html` 而不能匹配 `/a/b.html`
- `/*/*/*.html` 只匹配 `/任意/任意/任意.html` 文件
- `/**/*.html` 匹配 `/a.html` 和 `/a/b.html`，但不能匹配 `/a.php`
- `/**` 匹配所有 url


### 页面组件 

页面组件