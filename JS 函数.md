# 函数

# 1. 概述
- 函数声明的三种方法
  + `function` 命令

    ```JavaScript
	function 函数名(ar) {
	// 函数体
	}
	```

  + 函数表达式

    ```JavaScript
    var 函数名 = function(ar) {
    // 函数体
    }
    ```

  + `Function` 构造函数

    ```JavaScript
    var add = new Function(
    'x',
	'y',
	'return (x + y)'
    );
    ```

	等同于：

	```JavaScript
	function add(x,y) {
	return (x+ y);
	}
	```

- 函数重复声明，后面的函数会覆盖前面的函数。

- 圆括号运算符，return 和 递归
  + 函数内的 return 表示返回， return 后面的表达式，就是函数返回的值
  + 函数调用自身，就是递归。

- 函数名的提升
  > 采用function 命令声明的函数，函数名会被提升到作用域的顶部

- 不能在条件语句中声明函数
  + 在条件语句中定义函数必须用函数表达式

    ```JavaScript
    if(false){
    	var x = function() {}
    }
    ```

# 2. 属性和方法

  - name 属性: 返回紧跟在function 关键字后面的函数名(匿名函数为空字符串)
  - length 属性: 定义时的参数个数。
  - toString() 方法: 返回函数的源码（包含注释）

# 3. 函数作用域 scope
  - 作用域: 指变量存在的范围  全局作用域 / 函数作用域

  - 全局变量 / 局部变量： 函数内部声明的变量

  - 函数内部的变量提升
    > var 声明的变量，变量声明会被提升到函数体的头部。

  - 函数本身的作用域
    > 声明时所在的作用域, 与运行时所在的作用域无关 。

# 4. 参数
  - 为函数参数设置默认值

    ```JavaScript
    function x(a) {
    (a !== undefined && a !== null) ? a = a : a = 1;
    return a;
    }
    ```

  - 传递方式
    + 函数参数类型如果是原始类型的值, 传递方式是传值传递。
    + 函数参数类型如果是符合类型的值，传递方式是传址传递。
  - 同名参数
    > 同名的参数，取最后出现的那个值。

  - arguments 对象
    > 包含了函数命名时的所有参数。只能在函数体内部使用。

    + arguments 可以读取参数（` arguments[0]... `)
    + arguments 可以为参数赋值（严格模式不允许）
    + arguments 的 length 属性，判断函数调用时带几个参数。

    + arguments对象 与 数组
      - 将 arguments 转为数组
        * 方法一: ` var args = Array.prototype.slice.call(arguments); `
        * 方法二:

          ```
          var args = [];
          for(var i = 0; i< arguments.length; i++){
          args.push(arguments[i]);
          }
          ```

   + callee 属性
     > 返回它所对应的原函数

# 5.其他
  - 闭包（closure）
    > 定义在一个函数内部的函数。子函数可以读取父函数定义的变量。

  - 立即调用函数表达式 IIFE
    + 以 function 为行首被解释成语句。

     ` (function(){ code }()); `
     ` (function({ code })(); `

  - eval 命令
    > 讲字符串当做语句执行

    + eval 没有自己的作用域，严格模式下，eval 内部定义的变量不会影响到外部。
    + 直接调用 eval: 当前作用域。间接调用: 全局作用域。


