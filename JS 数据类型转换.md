# JS 数据类型转换

# 1. 强制转换

- Number()
  + undefined ==> NaN
  + null ==> NaN
  + boolean: true ==> 1 / false ==> 0
  + number: 简单的传入传出
  + string: '' ==> 0 / '数值' ==> 数值 / 其他 ==> NaN (八进制忽略前导0,十六进制转为十进制)
  + 对象:
    * 先调用对象的valueOf()方法，结果是基本数据类型，则转换为数值
    * 否则调用对象的头String()方法，结果是基本数据类型，则转换为数值
    * 否则，抛出一个错误。

- String()
  + underfined ==> 'underfined'
  + null ==> 'null'
  + boolean : true ==> 'true' / false ==> 'false'
  + 数值 ==> '数值'
  + string ==> string
  + 对象：
    * 先调用对象的toString() 方法，若返回原始类型的值，则对该值使用String() 方法
    * 否则调用valueOf() 方法，如果返回原始类型的值，则对该值使用 String() 方法
    * 否则，抛出一个错误

	```JavaScript
	String({a:1})   //'[object object]'
	String[1,2,3]   // '1,2,3'
	```

- Boolean()
  + undefined / null / false / 0 (包括+0和-0)/ NaN / '' ==> false
  + 其他为 true


# 2. 自动转换
	> 预期什么类型的值，就调用该类型的转换函数。

- 自动转换为布尔值

- 自动转换为字符串
  > 常发生在加法运算时

- 自动转换为数值
  > 除加法运算符外，其他数值都会把运算子转换为数值。（一元运算符也会运算子转换为数值）


