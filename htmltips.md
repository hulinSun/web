#前段小贴士


### 字符集（charset）

*字库规模：  UTF-8（字全） > gb2312（只有汉字）*
*UTF-8里面存储一个汉字3个字节。而gb2312中存储一个汉字2个字节。*

### 关键字和页面描述
在meta里面做seo搜索引擎优化
![](/Users/Hony/Desktop/Githup/web/someImages/屏幕快照 2017-02-14 下午6.06.23.png)

### img alt 属性
![](/Users/Hony/Desktop/Githup/web/someImages/8B7943B7-18C3-40D4-A81E-C269782EBC2E.png
)

### 网页中99%需要换行的时候，是因为另起了一个段落，所以要用p，不要用br br是英语break打断的意思。
### a标签的属性
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170214-0@2x.png)

### ul 标签里面只能放 li 标签，不能放别的东西 li是容器级标签，里面什么都能放。可以用来写tableviewCell

### DL
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-1@2x.png)
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-0@2x.png)

### span 是文本级标签
*span里面只能放置文字、图片、表单元素。 span里面不能放p、h、ul、dl、ol、div。*

### 表单
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-2@2x.png)

### 输入框
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-3@2x.png
)

### 下拉列表
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-4@2x.png)

### 三种按钮
普通按钮 button 
提交按钮 submit (按钮不需要写value自动就有“提交”文字。)
重置按钮 reset
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-5@2x.png)

### 字符实体
<  == &lt; (less than)
>  == &gt; (greater than)
c  == &copy;
   == &nbsp; 空格
   
###写css的地方是style标签，就是“样式”的意思，写在head里面
css对换行不敏感，对空格也不敏感。但是一定要有标准的语法。冒号，分号都不能省略。

html负责结构，css负责样式，js负责行为。

### 选择器
* 标签选择器
* id 选择器(不能相同，字母开头，可以有数字下划线) #lj{}
* 类选择器(.)  class属性可以重复，比如，页面上可能有很多标签都有t这个类,  .t{}  ![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-6@2x.png)  ![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-7@2x.png)
*  后代选择器![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-8@2x.png)
*  交集选择器 ![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-9@2x.png) 交集选择器，我们一般都是以标签名开头，比如div.haha  比如p.special 最好不要连续交。查找耗费性能
*  并集选择器 ![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-10@2x.png)
*  儿子选择器 ![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-11@2x.png)
*  序选择器 ![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-13@2x.png)
*  下一个兄弟选择器 ![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-12@2x.png)


### CSS属性的继承性与层叠性
有一些属性，当给自己设置的时候，自己的后代都继承上了，这个就是继承性。
哪些属性能继承？
color、 text-开头的、line-开头的、font-开头的。



**这些关于文字样式的，都能够继承； 所有关于盒子的、定位的、布局的属性都不能继承。**
层叠性：就是css处理冲突的能力。 所有的权重计算，没有任何兼容问题！

![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-14@2x.png)

真实项目中，你设置了某个属性。但是显示别的。这时候要考虑注意权重的问题了 权重比不过人家 0，1，0  < 0,1,1 如果这个时候考虑补全权重就可以了
通过继承来的属性，权重为0 (选中与没选中)

!important标记 权重无限大![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-15@2x.png)

!importtant 提升的是一个属性，而不是一个选择器 （字体颜色是red听inportant 但字号是50px）

!importtant  无法提升继承的权重
!importtant 不影响就近原则

### 权重计算总结
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-16@2x.png)

### 盒子模型
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-17@2x.png)
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-18@2x.png)

一般写法理解
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-19@2x.png
)

不能把小属性写在大属性前面，所以一般都是小属性层叠大属性![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-20@2x.png)

### border
三要素： 粗细 线型 颜色（默认为黑） 
border: 1px dashed red; // 一个都不能少 
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-21@2x.png)

### 块级元素和行内元素
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-22@2x.png)

块级元素可以设置为行内元素 ，行内元素可以设置为块级元素
修改display属性的值即可，inline行内。 block 块  display属性优先卸载样式表前面
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-23@2x.png)

浮动这个东西，我们在初期一定要遵循一个原则：永远不是一个东西单独浮动，浮动都是一起浮动，要浮动，大家都浮动。
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170215-24@2x.png)

浮动的性质： 脱标  贴边 字围 收缩(一个浮动的元素，如果没有设置width，那么将自动收缩为文字的宽度)

###清除浮动
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-0@2x.png)
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-1@2x.png)

![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-2@2x.png)
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-3@2x.png)
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-4@2x.png)

### margin 塌陷现象
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-5@2x.png)

盒子居中 margin: 0 auto;![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-6@2x.png)

### 善于使用父亲的padding 而不是儿子的，margin (父子之间不谈marign ，多用padding)

### 单行文本垂直居中（注意是单行）
行高=盒子高
如果想让多行文本垂直居中，设置盒子的padding

### font 属性 (字号 行高 字体)
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-7@2x.png)
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-8@2x.png)
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-9@2x.png)

### 伪类
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-10@2x.png)
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-11@2x.png)
必须按照固定的顺序写,否则将失效 love hate
所有的a不继承text、font这些东西。因为a自己有一个伪类的权重。


###background
![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-12@2x.png)

![](/Users/Hony/Desktop/Githup/web/someImages/QQ20170216-13@2x.png)

### 行内块元素和行内块元素拼接是有问题的(京东的搜索框) 后面的盒子会掉下来，最简单的处理方式是浮动

### 因为z-index 有从父现象。所以一般情况下调父亲的z-index 比较好。
只有定位的盒子才有z-index。如果一个盒子没有定位，但是又想让他不被其他盒子盖住，那么这时候给这个盒子定位，那么就不会被盖住，但是如果都有了定位，那么调整z-index 的层级就行。
定位的盒子如果想铺满整个屏幕，一定要写100%，否则会和内容一样宽(123123)

### 行高一定在字号的后面

### js 的变量作用域
 1. 在最外层声明的变量。
 2. 在函数体内部，但是没有声明var 的变量也是全局变量

### 事件三要素
事件源    事件    事件处理程序  
button.onclick = function(){}

### 让盒子隐藏
 Display: none  / display: block ;  显示的意思 
 Visibility: hidden; / visibility: visible  显示的意思
 Display  隐藏不占位置
 Visibility:hidden 隐藏占有位置   停职留薪
 Overflow:hidden;   隐藏超出的部分。
 
###DOM 做动态添加节点的时候，一般都是先写好css样式，然后给其赋类名的方法做样式的调整，而不是一个属性一个属性的搞
 
###双标签改变内容用innerHTML。单标签用value

### 九宫格布局， 浮动的盒子如果长度长度不够会掉下来，但是如果你不想让他掉下来，那么你要在这浮动的盒子里包一层定宽的div，那样就不会掉下来了

### 要做动画，一般要加定位，通过left top 等这些值改变位置 嘻嘻










