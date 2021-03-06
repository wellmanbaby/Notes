# HTTP状态码

维基百科：[HTTP状态码](https://zh.wikipedia.org/wiki/HTTP状态码)

## 1xx消息

这一类型的状态码，代表请求已被接受，需要继续处理。这类响应是临时响应，只包含状态行和某些可选的响应头信息，并以空行结束。由于HTTP/1.0协议中没有定义任何1xx状态码，所以除非在某些试验条件下，服务器禁止向此类客户端发送1xx响应。这些状态码代表的响应都是信息性的，标示客户应该采取的其他行动。

## 2xx成功

这一类型的状态码，代表请求已成功被服务器接收、理解、并接受。

## 3xx重定向

这类状态码代表需要客户端采取进一步的操作才能完成请求。通常，这些状态码用来重定向，后续的请求地址（重定向目标）在本次响应的Location域中指明。

当且仅当后续的请求所使用的方法是GET或者HEAD时，用户[浏览器](https://zh.wikipedia.org/wiki/浏览器)才可以在没有用户介入的情况下自动提交所需要的后续请求。客户端应当自动监测[无限循环](https://zh.wikipedia.org/wiki/死循環)重定向（例如：A→B→C→……→A或A→A），因为这会导致服务器和客户端大量不必要的资源消耗。按照HTTP/1.0版规范的建议，浏览器不应自动访问超过5次的重定向。

## 4xx客户端错误

这类的状态码代表了客户端看起来可能发生了错误，妨碍了服务器的处理。除非响应的是一个HEAD请求，否则服务器就应该返回一个解释当前错误状况的实体，以及这是临时的还是永久性的状况。这些状态码适用于任何请求方法。浏览器应当向用户显示任何包含在此类错误响应中的实体内容。[\[30\]](https://zh.wikipedia.org/wiki/HTTP状态码#cite_note-30)

如果错误发生时客户端正在传送数据，那么使用[TCP](https://zh.wikipedia.org/wiki/TCP)的服务器实现应当仔细确保在关闭客户端与服务器之间的连接之前，客户端已经收到了包含错误信息的[数据包](https://zh.wikipedia.org/wiki/数据包)。如果客户端在收到错误信息后继续向服务器发送数据，服务器的TCP栈将向客户端发送一个重置数据包，以清除该客户端所有还未识别的输入[缓冲](https://zh.wikipedia.org/w/index.php?title=缓冲&action=edit&redlink=1)，以免这些数据被服务器上的[应用程序](https://zh.wikipedia.org/wiki/应用程序)读取并干扰后者。

## 5xx服务器错误

表示服务器无法完成明显有效的请求。这类状态码代表了服务器在处理请求的过程中有错误或者异常状态发生，也有可能是服务器意识到以当前的软硬件资源无法完成对请求的处理。除非这是一个HEAD请求，否则服务器应当包含一个解释当前错误状态以及这个状况是临时的还是永久的解释信息实体。浏览器应当向用户展示任何在当前响应中被包含的实体。这些状态码适用于任何响应方法。

## 常见状态码

**1\*\***：信息性状态码  

**2\*\***：成功状态码  

200：OK 请求正常处理  

204：No Content请求处理成功，但没有资源可返回  

206：Partial Content对资源的某一部分的请求  

**3\*\***：重定向状态码  

301：Moved Permanently 永久重定向  

302：Found 临时性重定向  

304：Not Modified 缓存中读取  

**4\*\***：客户端错误状态码  

400：Bad Request 请求报文中存在语法错误  

401：Unauthorized需要有通过Http认证的认证信息  

403：Forbidden访问被拒绝  

404：Not Found无法找到请求资源  

**5\*\***：服务器错误状态码  

500：Internal Server Error 服务器端在执行时发生错误  

503：Service Unavailable 服务器处于超负载或者正在进行停机维护


