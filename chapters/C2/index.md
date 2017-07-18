## 简单的http协议

- 通信是从客户端开始建立的，客户端向服务端发送请求，服务端响应请求并且返回数据。那么就是**通过请求和响应的交换达成通信**。
- 客户端发送请求的例子：
  ``` 
    GET /index.html HTTP/1.1
    HOST: hackr.jp
  ```
  GET表示请求的方式、方法（method），/index.html表示请求指定资源，称为URI（request-URI），最后HTTP/1.1表示客户端使用的协议版本。

  请求报文是由*请求方法*、*请求 URI*、*协议版本*、*可选的请求首部字段*和*内容实体*构成的。
- 服务器响应的例子：
  ```
  HTTP/1.1 200 ok
  Date: Tue, 10 Jul 2012 06:50:15 GMT
  Content-Length: 363
  Content-Type: text/html

  <html>
  ...
  ```
  HTTP/1.1： 服务器的协议版本  
  200 ok： 响应的状态码和原因短语（简短的解释）  
  Date: Tue, 10 Jul 2012 06:50:15 GMT： 创建响应的时间  
  下面就是首部字段，然后空一行就是内容实体。  

