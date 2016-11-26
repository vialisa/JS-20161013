# 数据类型

# 1. 概述
  - 六类
    + undefined : 未定义或不存在
    + null : 有一个值，为空
    + boolean ：true/false
    + number : 整数和小数
    + string
    + object : 各种值组成的集合

  - JavaScript 确定一个值类型的三种方法
    + typeof 运算符
    + instanceof 运算符
    + Object.prototype.toString方法

  - typeof 运算符
    + 返回类型："undefined"/"object"/"boolean"/"number"/"string"/"object"
      * 函数返回 "function" / 数组返回对象

# 2. null 和 undefined
  - null 表示空值，undefined 表示未定义
  - null 和 undefined 在 if 语句自动转为 false

# 3. 布尔值
  - 返回布尔值的运算符: && / || / ! / == / === / != / !== / > / >= / < / <=
  - 转型函数Boolean()
    + 转为 false : undefined / null / false/ 0 / NaN / ""或''
    + 转为 true : true / 非零数字值 / 非空字符串 / 任何对象
    + 空数组、空对象 的转换布尔值为 true

# 4. 数值
  - 整点和浮点数
  - 数值精度
  - 数值范围
    + Number.MAX_VALUE
    + Number.MIN_VALUE

  - 数值的进制
    * 默认情况下，JavaScript内部会自动将八进制、十六进制、二进制转为十进制

  - 特殊的数值
    * 正零和负零

  - NaN
    > 非数字，主要出现在将字符串解析成数字出错的场合

    + NaN 不等于任何值，与任何值的运算都得到 NaN
    + isNaN() 对于数值以外的先转换为数值 值为true/false
    + 0 除以 0 得到 NaN

  - Infinity
    > 无穷大
	+ 规则
	    * 非零数值除以0, 得到 Infinity
	    * 非零正数除以 -0, 得到 -Infinity。负数除以 -0, 得到 Infinity
		* 0 乘以Infinity==>NaN / 0 除以 Infinity ==> 0 / Infinity 除以 0 ==> Infinity
		* Infinity 和 undefined 的运算返回的都是 NaN
		* Infinity 加/乘 Infinity  返回 Infinity
		* Infinity 减/除 Infinity  返回NaN

    + isFinite()
      > 返回一个布尔值，表示某个值是不是正常数值

  - 与数值相关的全局方法
    + parseInt()
      > 用于将字符串转换为整数

    + parseFloat()
      > 用于将一个字符串转为浮点数


# 5. 字符串
  - 概述
	  + 约定：JavaScript字符串 使用单引号
	    * 加号连接字符串
	  + 字符串与数组
	    > 字符串可视为成字符数组，因此可以用方括号运算符

		  ```
		  var x = 'hello';
		  x[1]  //e
		  ```
      + length 属性
        > 字符串的长度

        ```
        var x = 'hello';
        x.length;  //5
        ```

  - 字符集
    + JavaScript使用Unicode字符集

  - 转码
    + Base64转码
      * btoa()：字符串或二进制值转为Base64编码
      * atob()：Base64编码转为原来的编码


# 6. 对象
  > 无序的数据集合，由键值对(key:value)组成

- 概述
  + 对象生成方法
    * var o1 = {}
    * var o2 = new object()
    * var o3 = object.create(null)

  + 键名
    * > 对象的键名都是字符串，加不加引号都可。
	* >键名不符合表示名条件时加引号
	* JS保留字作键名可不加引号

  + 属性 property
    * 对象的每一个键名又称为属性，它的'键值'可以是任何数据类型。如果一个属性的值为函数,把这个属性称为'方法'。

	  ```
	  var o = {
	  m : 2,
	  n : function(){}
	  }
	  ```

    * 属性可以动态创建，不必声明时就指定。

      ```
      var 0bj = {};
      o.foo = 3;
      obj.foo  // 3
      ```

  + 对象的引用

  + 表达式/语句
    * JavaScript 规定行首是花括号 解释为语句 `{foo:123}`
    * 花括号前加圆括号,解释为表达式 `({foo:123})`

- 属性的操作
  + 读取属性： 点运算符 / 方括号运算符
    * obj.p / obj['p'] (方括号运算符内部可以使用表达式)

  + 浏览器环境下，所有的变量都是 window 对象的属性

  + Object.keys() 查看一个对象的所有属性。` Object.keys(obj) `

  + delete 命令 ： 删除对象属性( 不包含继承属性 )

  + in 运算符 ： 检查对象是否包含某个属性 ==> true / false (不识别对象继承属性)
    > 可用来检测一个全局变量是否存在 ` if('x' in window){...} `

  + for...in 循环 ： 遍历一个对象的所有属性。(包含继承属性)

    ```JavaScript
    var obj = {key1:1,key2:2,key3:3};
    for(var i in obj) {
    console.log(i);
    }
    ```

  + wich 语句 ： 操作同一个对象的多个属性







