# Array对象

- 构造函数
  > Array 是 JavaScript 内置对象，同时也是一个构造函数。

  + ` var arr = new Array(1,2); ` 等同于 ` var arr = [1, 2] `(建议用后者创建)
  + ` var arr = new Array(); ` 的参数如果是一个正整数，返回数组的成员都是空的，可以读取数组的length 属性，但是不能读取数组的键值。

- Array.isArray()
  > 判断一个值是否为数组。

    ```JavaScript
    var arr = [1, 2, 3];

    typeOf a   // "object"
    Array.isArray(a)   // true
    ```

- Array实例的方法
  + ` valueOf() ` 返回数组本身

    ```JavaScript
    var a = [1, 2, 3]
    a.valueOf()   // [1, 2, 3]
    ```

  + ` toString() ` 返回数组的字符串形式

    ```JavaScript
    var a = [1, 2, 3]
    a.toString()    // "1, 2, 3"
    ```

  + push()
   > 在数组的末端添加一个或多个元素，并返回日添加新元素后的数组长度。

    * 合并两个数组

      ```
      var a = [1, 2];
      var b = [3, 4];
      Array.propotype.push.apply(a,b)
      // 或者
      a.push.apply(a,b)
      ```

    * push 方法还可用于向对象添加元素，新加入的元素的键对应数组的索引，有 length 属性。

  + pop()
    > 删除数组的最后一个元素，并返回改数组。

  + join()
    > 以参数作为分隔符，将所有的数组成员组成一个字符串返回。默认逗号分隔。

    * 数组成员是 undefined / null ,转成空字符串。
    * 通过call 方法, 这个方法也可以用于字符串
      ` Array.prototype.join.call('hello', '-') `

  + concat()
    > 合并多个数组，将新数组的成员连接到原数组的尾部，返回一个新数组。

    * 参数也可以是其他类型
      ` [1, 2].concat(4,5,6)  // [1, 2, 3, 4, 5, 6] `

    * 借助call 可以把对象添加进数组
      ` [].concat.call({a:1},{b:2})    // [{a;1}, {b:2}] `

  + shift()
    > 删除数组的第一个元素，并返回该元素

  + unshift()
    > 在数组的第一个位置添加元素，并返回添加后数组长度。

  + reverse()
    > 颠倒数组元素的顺序, 返回改变后的数组。

  + slice()
    >






