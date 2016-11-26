# 数组

- 定义 ： 按次序排列的一组值（0开始）
  + 定义时赋值
    var arr = ['a','b','c']

  + 先定义 后赋值

    ```
    var arr = []
    arr[0] = 'a';
    arr[1]= 'b';
    ```

  + 任何类型的数据，都可放入数组
  + 多维数组： 数组的元素是数组

- 数组的本质
  > 特殊的对象。typeof 运算符返回 "object"

  + ` Object.keys(arr) `  ==> 0,1,2,...
  + JavaScript 规定 所有的键名都是字符串。非字符串的键名会被转为字符串。

- length 属性
  + 将 length 设置为0，可将数组清空
  + length 属性可写。
  + length 属性的值等于最大的数字键加 1
  + for 循环 ： 遍历一个数组

    ```JavaScript
	for(var i=0;i<arr.length;i++) {
	alert(arr[i]);
	}
	```

- in 运算符
  > 检查某个键名是否存在，适用于对象，数组  ==> true / false

- for...in 循环和数组的遍历
  > 既遍历数字键，又遍历非数字键。（推荐用 for/ while 语句遍历）

- 数组的空位（hole)
  + 空位不影响 length 属性

    ```JavaScript
    var arr = [1,,2,3];
    arr.length; // 4
    ```

  + delete 命令删除数组一位成员形成 hole ,不影响length属性
