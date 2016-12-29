# 基本语法

# 1. 语句
  > statement 为了完成某种任务而进行的操作。

  - 表达式 expression 指一个为了得到返回值的计算式。
  - 区别：
    + statement 是为了进行某种操作，一般不需要返回值。以分号结尾。
    + expression 为了得到返回值，一定会返回一个值。

# 2. 变量
  - 概念
    + 变量是对'值'的引用
    + 声明和赋值是两个操作
    + JavaScript 是动态型语言，所以变量的值可以是任何类型
    + 声明未赋值的变量的值是 undefined
  - 变量提升
    + var 声明的变量提升到函数/全局作用域的顶部 hoisting

# 3. 标识符
  - identifier 命名规则
    + 第一个字符 ：任意字母/美元符/下划线
    + 后面的字符 ：字母/美元符/下划线/数字
  - 对大小写敏感

# 4. 注释
  - ` // 单行注释 `
  - ` /* 多行注释 */ `

# 5. 区块 block
  - 不构成单独的作用域
  - 常在for/if/while/function 语句使用

# 6. 条件语句
  - if 语句
    > 先判断一个表达式的布尔值，再根据 boolean 的真伪选择执行的语句。

    ```JavaScript
    if(expression){
    statement
    }
    ```
    
  - if...else
  > 多个if...else 可以连写在一起

    ```JavaScript
    if(expression){
    statement1
    } else{
    statement2
    }
    ```

  - switch 语句

    ```JavaScript
	switch(expression){
	case值1:
	statement 1
	break;
	case值2:
	statement 2
	break;
	case值1:
	statement n
	break;
	case值1:
	statement n
	break;
	default:
	statement
	}
    ```

  - 三元运算符
    + 语法:` (contidion)? expr1 : expr2 `

# 7. 循环语句
  > 用于重复执行某个操作

  - while 语句
    + 语法

    ```JavaScript
    while(expression){
    statement;
    }
    ```

    + 无限循环

    ```JavaScript
    while(true){
    statement;
    }
    ```

  - for 循环
    + 语法

    ```JavaScript
    for(initialize; test; increment){
    statement
    }
    ```

    + 括号里的三个表达式
      * 初始化表达式：确定循环的初始值，只在循环开始时执行一次
      * 测试表达式：检查循环条件，为真就进行后续操作
      * 递增表达式：完成后续操作，返回上一步，再次检查循环条件

    + 无限循环

      ```JavaScript
      for ( ; ; ){
        statement
      }
      ```

  - do...while 循环
    > 先运行一次循环体，再判断条件

      + 语法

      ```JavaScript
      do{
      statement
      }while(expression);
      ```

  - break语句 和 continue 语句
    + break 用于跳出代码块或循环
    + continue 立即终止本轮循环，返回循环结构的头部，进入下一轮循环

  - 标签 label
    > 通常与 break 语句和 continue 语句配合使用，用于跳出特定循环
