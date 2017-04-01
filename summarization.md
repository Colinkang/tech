技术总结
   JavaScript
   1.基本数据类型
   2.语句  
   3.数组
   4.静态方法
   5.函数
   6.标准输入输出
   7.数据抽象
   8.Promise

   Json
   Object
1.
   Number
   String
   Boolean
   Undefined
   Null
   Symbol
Number -> Number
Math.round() 四舍五入
Math.ceil() 向上舍入
Math.floor() 向下舍入

Number -> String
Number.toString() 或者 String(Number)

Number -> Boolean
!Number !!Number

String -> Number
Number(String) parseInt(String) parseFloat(String)

String -> Boolean
!String !!String

String -> Json
JSON.parse('{"ck":"clarekang"}')  =>属性名也需要引号，否则会报错

Boolean -> Number
Number(false) Number(true)

Json -> String
JSON.stringify({'ck':'clarekang'})
2.
声明 var let const
赋值
条件  if switch
循环  while for
调用  
返回 return  break
