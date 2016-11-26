# JS 错误处理机制

- Error 对象
  + Error 构造函数

  ```
  var err = new Error('出错了');
  err.message // "出错了"
  ```

    * 参数：message (错误提示信息) / name (错误名称) / stack (错误的堆栈)

- JavaScript 原生错误类型
  + Error对象是最一般的错误类型
  + SyntaxError 语法错误
  + ReferenceError 引用一个不存在的变量
  + RangeError 一个值超出有效范围
  + TypeError 变量或参数不是预期类型
  + URIError URL相关函数的参数不正确
  + EvalError eval函数未被正确执行
