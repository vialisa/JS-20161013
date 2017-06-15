# JS BOM对象

- windowd 对象 (窗口)
  > 顶层对象 （所有的 BOM 对象都在 window 里面操作）

  + 方法
    * 弹出框 alert()
    * 确认框 confirm()
    * 输入框 prompt()
    * open() / close() : 打开一个新窗口/ 关闭当前窗口
    * 定时器
      1. setInterval("js代码",毫秒数) / clearInterval()  不停执行
      2. setTimeout("js代码",毫秒数) / clearTimeout()  执行一次

- screen 对象
  > 获取屏幕的信息

- navigator 对象
  > 获取客户机的信息（浏览器）

- location 对象
  > 请求 url 地址

  + href属性
    * 获取请求的 url 地址
      `document.write(location.href);`
    * 设置 url 地址 （绑定一个事件） `location.href=" url 地址";`

- history 对象
  > 请求 url 的历史记录

  + history.back() ： 访问的上一个页面 / history.go(-1);
  + histoty.forward() ： 访问的下一个页面 / history.go(1);
