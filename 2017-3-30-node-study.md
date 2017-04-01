1.nvm  npm nrm  
（nvm首先安装，利用nvm安装node，同时会带有npm，然后利用npm安装nrm）
nvm 用来控制版本
npm 用来管理各种包
nrm 用来管理源
可以使用yarn来替代npm，主要优点在于版本的锁定  
2.require exports module.exports
require用来引入包
module.exports导出包
3.测试用例
mocha ava 测试框架
should expect 断言库
istanbul  覆盖率测试
4.异步控制
回调函数
promise(bluebird)
generator(co自动执行)
async/await
5.框架
Express
koa
6.supertest可以参照superagent的API
对app的接口进行测试
var app = express();
var request = require('supertest')(app);
request.get('/path')
7.benchmark
用来测试性能
8.mongodb 与 mongoose
nosql数据库
9.cookie和session
http协议是无状态的(也就是不记录用户信息),所以客户端每次发出请求时，下一次请求
无法得知上一次请求所包含的状态数据，如何能把一个用户的状态数据关联起来？
所以服务器端给浏览器发送cookie(包括用户的基本信息并存储在浏览器端)，
每次请求时，把cookie信息发送给服务器端，服务器端便能识别用户信息。
后来发现cookie有一个很大的弊端，cookie中所有数据在客户端可以被修改，数据很容易被伪造
而且数据字段太多会影响传输效率
所以我们有了session(session存储在服务器端)
我们在cookie中存储session_id,每次发送session_id,服务器端检查cookie中保存的session_id
并通过这个session_id与服务器端的session data关联起来，进行数据的保存和修改。
