


1、如何解决跨域？有几种方式？

1>通过jsonp跨域
2>通过修改document.domain来跨子域
3>使用window.name来进行跨域
4>使用HTML5中新引进的window.postMessage方法来跨域传送数据

资料地址:http://www.cnblogs.com/2050/p/3191744.html

2、前端性能优化方法？
一种：
1、使用css sprites，可以有效的减少http请求数
2、使用缓存
3、压缩js，css文件，减小文件体积
4、使用cdn，减小服务器负担
5、懒加载图片
6、预加载css，js文件
7、避免dom结构的深层次嵌套
8、给DOM元素添加样式时，把样式放到类中，直接给元素添加类，减少重构，回流

链接：https://www.zhihu.com/question/41466747/answer/132562725

二种：
减少http请求次数、避免页面跳转、缓存ajax、延迟加载、提前加载、减少DOM元素数量、减少iframe数量、避免404、避免空的图片src、样式放头部、避免css表达式、用link代替@import、js放底部、使用外部css和js、压缩css和js、减少DOM操作、使用css sprite、ajax异步加载

资料地址：http://www.cnblogs.com/lei2007/archive/2013/08/16/3262897.html

js延迟加载的方式有哪些？
方法：defer （按顺序依次执行）、async （不能保证脚本会按顺序执行）、动态创建DOM方式、使用jQuery的getScript()方法。

3、样式导入link和@import的区别？
其实link和@import的最根本区别就是，link 是一个html 的一个标签 ，而@import 是css 的一个标签 ,避免使用@import的原因很简单，因为它相当于将css放在网页内容底部

4、html5 的新特性？如何区分html和html5?css3新特性？
html5:
绘画 canvas、localStorage、sessionStorage、用于媒介回放的 video和 audio 元素、语意化更好的内容元素，比如article、footer、header、nav、section;
     表单控件，calendar、date、time、email、url、search;新的技术web worker(专用线程)、web socket通信、 Geolocation 地理定位。
css3：
在项目开发中我们采用的CSS3新特性有 
1、CSS3的选择器
2、@Font-face 特性
3、圆角
4、阴影
5、渐变
6、css弹性盒子模型（display: -webkit-box; ）
7、 CSS3动画

如何区分HTML和HTML5：
文档申明
        html5的文档头部申明很简单<！doctype html>
利用标签区分
        有很多html新增标签，比如article、footer、header、nav、section

资料地址：http://blog.csdn.net/lxcao/article/details/52797914

5、cookies、sessionStorage、localStorage区别？
相同点：都存储在客户端
不同点：
1.存储大小
cookie数据大小不能超过4k。
sessionStorage和localStorage 虽然也有存储大小的限制，但比cookie大得多，可以达到5M或更大。
2.有效时间
localStorage 存储持久数据，浏览器关闭后数据不丢失除非主动删除数据；
sessionStorage 数据在当前浏览器窗口关闭后自动删除。
cookie 设置的cookie过期时间之前一直有效，即使窗口或浏览器关闭
3. 数据与服务器之间的交互方式
cookie的数据会自动的传递到服务器，服务器端也可以写cookie到客户端
sessionStorage和localStorage不会自动把数据发给服务器，仅在本地保存。
6、css优先级
!important>style>权重值（如果权重相同，则最后定义的样式起作用）

7、sass、less是什么？为什么用它？
sass和less都是一种动态样式语言，sass是运行在服务端的，而less是可在服务端和客户端运行。
作用：使CSS开发更灵活和更强大
8、css sprite的优缺点？
优点：减少http请求、提高页面性能
缺点：维护较麻烦

9、如何快速生成一段随机文本？
var a = 'asassdfeeqwrqwesdgqwerq2wdasrqew',b='';
for(var i=0;i<10;i++){
b+=a.charAt(Math.random()*a.length)
}
console.log(b)

10、web workers是什么？什么场景下用它？
web workers是一种运行在l浏览器后台的JavaScript多线程解决方案，不会影响页面性能。
应用场景：
对于图像、视频、音频的解析处理；
canvas 中的图像计算处理；
大量的 ajax 请求或者网络服务轮询；
大量数据的计算处理（排序、检索、过滤、分析…）；

11、什么是闭包？为什么要用它？
我个人理解，闭包是就是函数中的函数，里面的函数可以访问外面函数的变量，外面的变量的是这个内部函数的一部分。
作用：1.使用闭包可以访问函数中的变量。2.可以使变量长期保存在内存中，生命周期比较长。
注意：闭包不能滥用，否则会导致内存泄露，影响网页的性能。闭包使用完了后，要立即释放资源，将引用变量指向null。

12、移动端点击事件延迟是多少？为什么会有？怎么解决？
300ms;
原因：双击缩放 
解决方法：禁用缩放 、引入fastClickjs

13、nodejs了解吗？有过哪些应用？

14、使用过哪些前端框架？说出他们的优缺点？
bootstrap、jquery mobile、jquery ui、vue、angular

15、css 盒子模型？
盒子模型有两种，W3C和IE盒子模型
1、W3C定义的盒子模型包括margin、border、padding、content ，元素的width=content的宽度
2、IE盒子模型与W3C的盒子模型唯一区别就是元素的宽度，元素的width=content+padding+border

实例：我个人认为W3C定义盒子模型与IE定义的盒子模型，IE定义的比较合理，元素的宽度应该包含border（边框）和padding（填充），这个和我们现实生活的盒子是一样的，W3C也认识到自己的问题了，所以在CSS3中新增了一个样式box-sizing，包含两个属性content-box 和 border-box。

16、vue与angular区别？

17、angular依赖注入？
 
依赖注入（Dependency Injection，简称DI）是一种软件设计模式，在这种模式下，一个或更多的依赖（或服务）被注入（或者通过引用传递）到一个独立的对象（或客户端）中，然后成为了该客户端状态的一部分。
AngularJS 提供很好的依赖注入机制。以下5个核心组件用来作为依赖注入：
value
factory
service
provider
constant
18、vue 的核心是什么？
核心是：数据驱动、组件系统
