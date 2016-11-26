# JS Object对象

- # 概述

+ 生成新对象：` var o = new Object(); `
+ Object 作为构造函数使用时可以接受一个参数，如果该参数是一个对象，则返回这个对象，如果是原始类型的值，
则返回该值对应的包装对象。

+ 在Object 上部署方法
  * 部署在Object 对象本身

     ```JavaScript
     Object.print = function(){ console.log('hello')};

     var o = new Object();

     Object.print(o);    // hello
     ```

   * 部署在Object.prototype 对象
     > 所有构造器都有一个prototype 属性，指向一个原型对象。凡是定义在Object.prototype 对象上面的属性和方法，将被所有的实例对象共享。

     ```JavaScript
     Object.prototype.print = function() { console.log('hello')};

     var o = new Object();

	 // o 直接继承Object.prototype 的属性和方法
     o.print();      // hello
	 ```

- # Object()
  > 将任意值转为对象

  + 如果参数是原始类型的值, 返回对应的包装对象的实例。
  + 如果参数是对象，返回原对象。
  + 判断一个变量是否为对象的函数：

    ```JavaScript
    function isObject(value) {
    return value === Object(value);
    }

    isObject([])    // true
    isObject(true)    //false
    ```

- # Object 对象的静态方法
  > 部署在Object 对象自身的方法

  + Object.keys(), Object.getOwnPropertyNames()
    * 相同点
      1. 遍历对象的属性
      2. 都返回一个数组
      3. 该数组的成员都是对象自身的，而不是继承的所有属性。

    * 不同点
      1. Object.keys方法只返回可枚举的属性。
      2. Object.getOwnPropertyNames 方法还返回不可枚举的属性名。

      ```JavaScript
      var arr = ['a', 'b', 'c'];

      Object.keys(arr);     // ["1", "2", "3"]
      Object.getOwnPropertyNames(arr);      // ["1", "2", "3", "length"]
      ```


