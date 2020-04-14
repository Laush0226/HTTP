## Http协议与Fiddler抓包
### 1.1 HTTP
1. HTTP协议原理
    - URL -> HTTPRequest -> web服务器
    - web服务器 -> HTTPResponse ->浏览器
* TCP/IP 协议使用Wireshark抓包
### 1.2 HTTP+TLS/SSL
1. HTTPS就是加密过的HTTP
2. 通过CA在浏览器请求前会与服务器有`握手验证`
    >查看CA *win+R cmd certmgr.msc*
3. Tunnel 是Client和Server间建立的通信隧道，也就是握手验证中的请求。
    >*Rules-Hide CONNECTs* 可以屏蔽握手请求。
### 1.3 Fiddler
1. 主菜单栏
2. 工具栏
3. web Sessions list
    - #:ID
    - Result:`响应状态码`
    - Protocol:使用的协议Http/Https
    - Host:服务器主机名或端口号
    - URL(uniform resource locator)：请求路径
    - Body：HttpResponse的字节数
    - Caching:缓存的字节数
    - Content-Type：相应中内容类型 
    - process：对应的本地进程
4. 功能面板
    - Inspectors
5. QuickExec
    - alt+Q
    - cls：清空面板
6. 状态栏：Fiddler的配置信息
### HTTP请求的方法
1. 常见的Method
    - GET
        GET可以带参数在URL中
        >`?`请求 `key=value` `&`分隔
    - POST
    - PATCH
    - PUT 
    - DELETE
2. 常见相应状态码

| **状态码** | **已定义范围** | **分类**        |
|:-------:|:---------:|:-------------:|
| 1XX     | 100~101   | 请求已经成功接收，继续处理 |
| 2XX     |           |               |
| 3XX     |           |               |
| 4XX     |           |               |
| 5XX     |           |               |