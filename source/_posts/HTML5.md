---
title: HTML5笔记
copyright: true
date: 2019-05-19 17:20:48
tags: 前端
---

# HEAD

## meta标记

* meta标记用来描述网页，有利于搜索引擎快速找到网站并正确分类

* **注意：**对于中文网页需要使用 meta charset="utf-8"声明编码，否则会出现乱码。
* 有些浏览器(如 360 浏览器)会设置 GBK 为默认编码，则你需要设置为meta charset="gbk"

* SEO（Search Engine Optimization）搜索引擎优化
  * 开发后上线=》发布=》用户就可以找到你的网站（网址、去搜索）
  *  记得网站要去做收录（各大搜索网站收录的地址）
  * 收录后，搜索引擎（蜘蛛程序）去爬你的网站
  * 目的：记录你的网页内容：title标签、alt、title属性、keywords、description

# STYLE / CSS

## 选择器

### 七种选择器

- ID 选择器， 如 #id{}
- 类选择器， 如 .class{}
- 属性选择器， 如 a[href="segmentfault.com"]{}
- 伪类选择器， 如 :hover{}
- 伪元素选择器， 如 ::before{}
- 标签选择器， 如 span{}
- 通配选择器， 如 *{}



### 关系选择符

* E   F：包含选择符
  * 选择所有被E元素包含的F元素
* E>F：子选择符
  * 选择所有作为E元素的子元素F
* E+F：相邻选择符
  * 选择紧贴在E元素之后的F元素
* E~F：兄弟选择符
  * 选择E元素所有兄弟元素F



### 伪类选择符

* 常用
  * ：hover
    
    * 设置元素在其鼠标悬停时的样式。
    
  * ：active
    
    * 设置元素在被用户激活
    
      (在鼠标点击与释放之间发生的事件)时的样式
    
  * ：focus
  
    * 设置元素在成为输入焦点
  
      (该元素的onfocus事件发生)时的样式
  
  * E：not（s)
  
    * 匹配不含有s选择符的元素E
  
  * ：first-child
  
    * 匹配第一个子元素
  
  * ：last-child
  
    * 匹配最后一个子元素
  
  * ：nth-child（n）
  
    * 匹配第n个子元素





| 选择器                                                       | 示例                  | 示例说明                                       |
| ------------------------------------------------------------ | --------------------- | ---------------------------------------------- |
| [:checked](https://www.runoob.com/cssref/sel-checked.html)   | input:checked         | 选择所有选中的表单元素                         |
| [:disabled](https://www.runoob.com/css/cssref/sel-disabled.html) | input:disabled        | 选择所有禁用的表单元素                         |
| [:empty](https://www.runoob.com/cssref/sel-empty.html)       | p:empty               | 选择所有没有子元素的p元素                      |
| [:enabled](https://www.runoob.com/cssref/sel-enable.html)    | input:enabled         | 选择所有启用的表单元素                         |
| [:first-of-type](https://www.runoob.com/cssref/sel-first-of-type.html) | p:first-of-type       | 选择的每个 p 元素是其父元素的第一个 p 元素     |
| [:in-range](https://www.runoob.com/cssref/sel-in-range.html) | input:in-range        | 选择元素指定范围内的值                         |
| [:invalid](https://www.runoob.com/cssref/sel-invalid.html)   | input:invalid         | 选择所有无效的元素                             |
| [:last-child](https://www.runoob.com/cssref/sel-last-child.html) | p:last-child          | 选择所有p元素的最后一个子元素                  |
| [:last-of-type](https://www.runoob.com/cssref/sel-last-of-type.html) | p:last-of-type        | 选择每个p元素是其母元素的最后一个p元素         |
| [:not(selector)](https://www.runoob.com/cssref/sel-not.html) | :not(p)               | 选择所有p以外的元素                            |
| [:nth-child(n)](https://www.runoob.com/cssref/sel-nth-child.html) | p:nth-child(2)        | 选择所有 p 元素的父元素的第二个子元素          |
| [:nth-last-child(n)](https://www.runoob.com/cssref/sel-nth-last-child.html) | p:nth-last-child(2)   | 选择所有p元素倒数的第二个子元素                |
| [:nth-last-of-type(n)](https://www.runoob.com/cssref/sel-nth-last-of-type.html) | p:nth-last-of-type(2) | 选择所有p元素倒数的第二个为p的子元素           |
| [:nth-of-type(n)](https://www.runoob.com/cssref/sel-nth-of-type.html) | p:nth-of-type(2)      | 选择所有p元素第二个为p的子元素                 |
| [:only-of-type](https://www.runoob.com/cssref/sel-only-of-type.html) | p:only-of-type        | 选择所有仅有一个子元素为p的元素                |
| [:only-child](https://www.runoob.com/cssref/sel-only-child.html) | p:only-child          | 选择所有仅有一个子元素的p元素                  |
| [:optional](https://www.runoob.com/cssref/sel-optional.html) | input:optional        | 选择没有"required"的元素属性                   |
| [:out-of-range](https://www.runoob.com/cssref/sel-out-of-range.html) | input:out-of-range    | 选择指定范围以外的值的元素属性                 |
| [:read-only](https://www.runoob.com/cssref/sel-read-only.html) | input:read-only       | 选择只读属性的元素属性                         |
| [:read-write](https://www.runoob.com/cssref/sel-read-write.html) | input:read-write      | 选择没有只读属性的元素属性                     |
| [:required](https://www.runoob.com/cssref/sel-required.html) | input:required        | 选择有"required"属性指定的元素属性             |
| [:root](https://www.runoob.com/cssref/sel-root.html)         | root                  | 选择文档的根元素                               |
| [:target](https://www.runoob.com/cssref/sel-target.html)     | #news:target          | 选择当前活动#news元素(点击URL包含锚的名字)     |
| [:valid](https://www.runoob.com/cssref/sel-valid.html)       | input:valid           | 选择所有有效值的属性                           |
| [:link](https://www.runoob.com/cssref/sel-link.html)         | a:link                | 选择所有未访问链接                             |
| [:visited](https://www.runoob.com/cssref/sel-visited.html)   | a:visited             | 选择所有访问过的链接                           |
| [:active](https://www.runoob.com/cssref/sel-active.html)     | a:active              | 选择正在活动链接                               |
| [:hover](https://www.runoob.com/cssref/sel-hover.html)       | a:hover               | 把鼠标放在链接上的状态                         |
| [:focus](https://www.runoob.com/cssref/sel-focus.html)       | input:focus           | 选择元素输入后具有焦点                         |
| [:first-letter](https://www.runoob.com/cssref/sel-firstletter.html) | p:first-letter        | 选择每个<p 元素的第一个字母                    |
| [:first-line](https://www.runoob.com/cssref/sel-firstline.html) | p:first-line          | 选择每个<p 元素的第一行                        |
| [:first-child](https://www.runoob.com/cssref/sel-firstchild.html) | p:first-child         | 选择器匹配属于任意元素的第一个子元素的 p> 元素 |
| [:before](https://www.runoob.com/cssref/sel-before.html)     | p:before              | 在每个<p元素之前插入内容                       |
| [:after](https://www.runoob.com/cssref/sel-after.html)       | p:after               | 在每个<p元素之后插入内容                       |
| [:lang(*language*)](https://www.runoob.com/cssref/sel-lang.html) | p:lang(it)            | 为<p元素的lang属性选择一个开始值               |

### 属性选择符

* E[att]
  * 选择具有att属性的E元素
* E[att="val"]
  * 选择具有att属性且属性值等于val的E元素
* E[att~="val"]
  * 选择具有att属性且属性值为一用空格分隔的字词列表，其中一个等于val的E元素
* E[att^="val"]
  * 选择具有att属性且属性值为以val开头的字符串的E元素
* E[att$="val"]
  * 选择具有att属性且属性值为以val结尾的字符串的E元素
* E[att*="val"]
  * 选择具有att属性且属性值为包含val的字符串的E元素
* E[att|="val"]
  * 选择具有att属性且属性值为以val开头并用连接符"-"分隔的字符串的E元素



### 伪对象选择符

* E:first-letter/E::first-letter 
  * 设置对象内的第一个字符的样式
* E:first-line/E::first-line 
  * 设置对象内的第一行的样式
* E:before/E::before  
  * 设置在对象前（依据对象树的逻辑结构）发生的内容。
  * 用来和content属性一起使用 
* E:after/E::after
  * 设置在对象后（依据对象树的逻辑结构）发生的内容。
  * 用来和content属性一起使用 
* E::placeholder   
  * 设置对象文字占位符的样式
* E::selection
  * 设置对象被选择时的颜色



### tips

* CSS选择器的使用，应该尽量避免使用 !important 和 内联样式；
* id通常也是与class区分开使用，前者多用于JS中的结点定位，后者多用于CSS选择器。
* color尽量使用16进制或RGBA
* 字体：
  * 垂直居中：
    * lineheight与height相等
    * vertical-align:middle;
  * 文本居中（img未转换成块元素前同样适用）：
    * text-align: center



## 优先级

### 规则：就近原则

* 行内引用  > 页内引用  > 页外引用

* **CSS 优先规则1：** 最近的祖先样式比其他祖先样式优先级高。

  ```css
  <!-- 类名为 son 的 div 的 color 为 blue -->
  <div style="color: red">
      <div style="color: blue">
          <div class="son"></div>
      </div>
  </div>
  ```

  

* **CSS 优先规则2：**"直接样式"比"祖先样式"优先级高。

  ```css
  <!-- 类名为 son 的 div 的 color 为 blue -->
  <div style="color: red">
      <div class="son" style="color: blue"></div>
  </div>
  ```

  

* **CSS 优先规则3：**

  * 优先级关系：内联样式 > ID 选择器 > 类选择器 = 属性选择器 = 伪类选择器 > 标签选择器 = 伪元素选择器

* **CSS 优先规则4：**

  * 计算选择符中 ID 选择器的个数（a），计算选择符中类选择器、属性选择器以及伪类选择器的个数之和（b），计算选择符中标签选择器和伪元素选择器的个数之和（c）。
  * 按 a、b、c 的顺序依次比较大小，大的则优先级高，相等则比较下一个。若最后两个的选择符中 a、b、c 都相等，则按照"就近原则"来判断。

* **CSS 优先规则5：**

  * 属性后插有 **!important** 的属性拥有最高优先级。若同时插有 **!important**，则再利用规则 3、4 判断优先级
  
* ! important **（特殊情况使用）**

  * !important是CSS1就定义的语法，作用是提高指定样式规则的应用优先权。
    * 语法格式{ cssRule !important }，即写在定义的最后面，例如：
      * p{color:red !important;}
      * p{color:blue}

## tips

* #### 错误的说法

  * 在学习过程中，你可能发现给选择器加权值的说法，即 ID 选择器权值为 100，类选择器权值为 10，标签选择器权值为 1，当一个选择器由多个 ID 选择器、类选择器或标签选择器组成时，则将所有权值相加，然后再比较权值。这种说法其实是有问题的。比如一个由 11 个类选择器组成的选择器和一个由 1 个 ID 选择器组成的选择器指向同一个标签，按理说 110 > 100，应该应用前者的样式，然而事实是应用后者的样式。错误的原因是：**选择器的权值不能进位**。还是拿刚刚的例子说明。11 个类选择器组成的选择器的总权值为 110，但因为 11 个均为类选择器，所以其实总权值最多不能超过 100， 你可以理解为 99.99，所以最终应用后者样式。

* #### CSS 选择符组合方式：

  - 后代选择符： .father .child{}
  - 子选择符： .father > .child{}
  - 相邻选择符: .bro1 + .bro2{}

* #### 样式被应用的位置越在下面则优先级越高

* 清除CSS中select的下拉箭头样式

  * ```css
    select {
    /*Chrome和Firefox里面的边框是不一样的，所以复写了一下*/
    border: solid 1px #000;
    
    /*很关键：将默认的select选择框样式清除*/
    appearance:none;
    -moz-appearance:none;
    -webkit-appearance:none;
    
    /*在选择框的最右侧中间显示小箭头图片*/
    background: url("http://ourjs.github.io/static/2015/arrow.png") no-repeat scroll right center transparent;
    
    
    /*为下拉小箭头留出一点位置，避免被文字覆盖*/
    padding-right: 14px;
    }
    
    
    /*清除ie的默认选择框样式清除，隐藏下拉箭头*/
    select::-ms-expand { display: none; }
    ```

    







## other

* 在布局上面，一开始就要设置的，主要目的去除/初始化所有标签的样式

  ```css
  *{
              margin: 0;  /*去除默认的外边距*/
              padding: 0; /*去除默认的内边距*/
              font-size: 14px;    /*统一字体大小*/
              font-weight: normal;    /*都不加粗*/
   }
  ```

* id名，一般不用来加样式，一般是用于js添加动态效果

* id的优先级最高

* 长图片定位

  * ```css
    .img{
    	background:url(1.png) 0 0 no-repeat;
    	width:25px;
    	height:25px;
    }
    ```

    

# 布局

## display（元素显示模式）

* block
  * 块对象指的是元素显示为一个方块，默认显示状态下将占据整行，其它的元素只能另起一行显示
* inline
  * 行间对象与block刚好相反，它允许其它元素在同一行显示
* none
  * 隐藏对象
* inline-block

## float（元素的浮动）

* none
  * 不浮动
* right
  * 向右浮动
* left
  * 向左浮动
* 浮动的时候元素的显示属性也变化了变为 “行内元素”

## clear（清除浮动）

* none
  * 默认值
  * 允许两两边都可以有浮动对象
* left
  * 不允许左边有浮动对象
* right
  * 不允许右边有浮动对象
* both
  * 不允许有浮动对象

## position（元素的定位）

* static
  * 无定位
  * 默认值
* absolute
  * 绝对定位
  * tips：
    * 脱离文档流。
    * 通过 top,bottom,left,right 定位。
    * 如果父元素 position 为 static 时，将以body坐标原点进行定位。
    * 如果父元素 position 为 relative  时，将以父元素进行定位。
* relative
  * 相对定位
  * tips：
    * 相对定位（相对自己原来的位置而言）
    * 不脱离文档流
    * 参考自身静态位置通过 top,bottom,left,right 定位。
* fixed
  * 固定定位
  * tips
    * 固定定位实际上只是绝对定位的特殊形式；
    * 固定定位的元素是相对于浏览器窗口而固定，而不是相对于其包含元素；
    * 即使页面滚动了，它们仍然会处在浏览器窗口中跟原来完全一样的地方。 

## z-index（元素的层叠关系）

* auto
* number

## **reset.css**

```css
body,p,ul,ol,li,dl,dt,dd,h1,h2,h3,h4,h5,h6,form,fieldset,legend,input,select,textarea,button,th,td,menu{margin:0;padding:0;}
ul,dl,ol{list-style:none;}
img,fieldset,input[type="submit"]{border:0 none;}
em{font-style:normal;}
strong{font-weight:normal;}
table{border-collapse:collapse;border-spacing:0;}
button,input[type="button"]{cursor:pointer;border:0 none;}
a,button,input,img{-webkit-touch-callout:none;}
img{pointer-events:none;/*禁止图片的点击事件，例如长按保存图片*/}
input,select,textarea{outline:none;}
a{text-decoration:none;}
.fl{ float: left}
.fr{ float: right}
.clear{clear:both;} 
html,body{
/*禁止用户选择元素*/
-moz-user-select:none;
 -webkit-user-select: none;
-ms-user-select: none;
 -khtml-user-select:none; /*禁止元素点击出现半透明黑色背景*/
 -webkit-tap-highlight-color:rgba(0, 0, 0, 0); }
html {height: 100%;width: 100%;font-family: 'Heiti SC', 'Microsoft YaHei';outline: 0;-webkit-text-size-adjust:none;}
body {height: 100%;margin: 0;position: relative;}
```





# BODY



## 常见语义标记

```html
<article> 
    
<header>
	<h1>文章标题</h1>
	<p>发表时间：1999-01-01 <span>作者：佚名</span></p>
</header> 
    
<nav> 
	<a href="#">HTML</a> | 
	<a href="#">CSS</a> | 
	<a href="#">JavaScript</a> 
</nav>

<p>正文...</p>
    
<section>
  	<h1>稻草</h1>
  	<p>夏日的夕阳，激起了小溪的热情，染红了乡间的田野。</p>
</section>
<p>今天我们去星光电影城看了场电影</p> 
<aside> 
	<h4>星光电影城</h4> 
	<p>星光电影城是市内最大的电影城，里面不仅有舒服的观影体验，还有大量的娱乐设施，美食等...</p> 
</aside>



<footer> 
	<p>Posted by: hello world</p>
 	<p><time pubdate datetime="2012-03-01"></time></p> 
</footer>

</article>

```



| 标记       | 说明                                                         |
| ---------- | ------------------------------------------------------------ |
| header     | 显示网站名称、主题或者主要信息                               |
| nav        | 网站的连接菜单                                               |
| aside      | 用于侧边栏                                                   |
| article    | 用于定义主内容区                                             |
| section    | 用于章节或段落                                               |
| footer     | 位于页脚，用来放置版权声明、作者等信息                       |
| figure     | 独立的流内容（图像、图表、照片、代码等等）<br/>内容应该与主内容相关，但如果被删除，则不应对文档流产生影响。 |
| figcaption | 定义 figure>元素的标题.<br/>应该被置于 "figure"元素的第一个或最后一个子元素的位置 |
|            |                                                              |

* div：容器标签

* span：区块标签

* embed：定义了一个容器，用来嵌入外部应用或者互动程序（插件）

  * width、height：宽高

  * type：规定嵌入内容的MIME 类型，如视频，外部应用

    * 值：MIME_type

  * src：URL

  * ```html
    <embed src="flash.swf" >
    ```

* base：为页面上的所有链接规定默认地址或默认目标

  * base> 标签必须位于 head> 元素内部

  * base>标签是空标签，没有结束标签，XHTML中要求正确关闭 />

  * ```html
    <head>
    <meta charset="utf-8"> 
    <title>菜鸟教程(runoob.com)</title>
    	<base href="//www.runoob.com/images/">
    </head>
    <body>
    <p>
        <img src="logo.png"> - 注意这里我们设置了图片的相对地址。能正常显示是因为我们在 head 部分设置了 base 标签，该标签指定了页面上所有链接的默认 URL，所以该图片的访问地址为 "http://www.runoob.com/images/logo.png"
        </p>
    ```

* bdo：改变文字方向

  * 属性

    * ltr：left to right  ：→
    * rtl：right to left  ：←

  * ```html
    <bdo dir=“rtl”>文本将改变文本方向</bdo>
    ```

* canvas：图形的绘制

  * 通过脚本（通常是JS）来完成

  * canvas> 标签只是图形容器，您必须使用脚本来绘制图形

  * 默认情况下 canvas元素没有边框和内容，使用 style 属性来添加边框

  * ```html
    <canvas  id=“id名” width=“200” height=“100” style="border:1px solid #000;"></canvas>
    ```

* ```
  <tbody> 标签表格主体（正文）。该标签用于组合 HTML 表格的主体内容。
  tbody 元素应该与 thead 和 tfoot 元素结合起来使用。
  thead 元素用于对 HTML 表格中的表头内容进行分组，而 tfoot 元素用于对 HTML 表格中的表注（页脚）内容进行分组。
  注释：如果您使用 thead、tfoot 以及 tbody 元素，您就必须使用全部的元素。它们的出现次序是：thead、tfoot、tbody，这样浏览器就可以在收到所有数据前呈现页脚了。您必须在 table 元素内部使用这些标签。
  提示：在默认情况下这些元素不会影响到表格的布局。不过，您可以使用 CSS 使这些元素改变表格的外观。
  详细描述
  thead、tfoot 以及 tbody 元素使您有能力对表格中的行进行分组。当您创建某个表格时，您也许希望拥有一个标题行，一些带有数据的行，以及位于底部的一个总计行。这种划分使浏览器有能力支持独立于表格标题和页脚的表格正文滚动。当长的表格被打印时，表格的表头和页脚可被打印在包含表格数据的每张页面上。
  注释：<thead> 内部必须拥有 <tr> 标签！
  ```

  

## 标记

- 换行

```html
<br>
```

- 分割线

```html
<hr>
```

- 让文字按原始代码的排列方式进行显示

```html
<pre></pre>
```

- 表示引用文字，会将标记内的文字换行并缩进

```html
<blockquote></blockquote>
```

- 特殊符号表示

  &copy;  //  &copy+;

  <  //  &lt+;

  &gt;  //  &gt+;

  &  //   &amp+;

  "   //   &quot+;

  &reg;   //   &reg+;

  不换行空格  //  &nbsp+;

  半角空格  //  &ensp；
  
  全角空格  //  &emsp；
  
  窄空格  //   &thinsp；6/1



## a：链接

```css
a{
	text-decoration：none;	/*去除下划线*/
    text-decoration：underline;/*添加下划线*/
}
```

* 说明：
  * href：定义链接地址
  * title：链接提示信息
  * target：链接打开方式 
* 锚点标签用于使用户"跳"到文档的某个部分。
  * a href="#位置名"></a
  * a name="位置名"></a

* **提示：**如果没有使用 href 属性，则不能使用 hreflang、media、rel、target 以及 type 属性
* **提示：**通常在当前浏览器窗口中显示被链接页面，除非规定了其他 target
* **提示：**请使用 CSS 来改变链接的样式



## img：图像

* 转换为块元素：

  * ```css
    img{
    	display: block;
    }
    ```

* 说明：

  * src：定义图像的url
  * alt：定义图像的替代文本（即图像提示信息）
  * width：设置图像的宽度  
  * height：设置图像的高度

* 图像热区

  ```
  <img src="URL"  usemap="# map名称" />
  <map name="map名称">
  	<area shape="形状" coords="坐标值" href="URL" />
  </map>
  ```

  * 矩形：(左上角顶点坐标为(x1,y1)，右下角顶点坐标为(x2,y2)) 

  ```html
  <area shape="rect" coords="x1,y1,x2,y2" href=url>
  ```

  * 圆形：(圆心坐标为(X1,y1)，半径为r) 

  ```html
  <area shape="circle" coords="x1,y1,r" href=url>
  ```

  * 多边形：(各顶点坐标依次为(x1,y1)、(x2,y2)、(x3,y3) ......) 

  ```html
  <area shape="poly" coords="x1,y1,x2,y2 ......" href=url>
  ```

* float：浮动

  |   值    |                         描述                         |
  | :-----: | :--------------------------------------------------: |
  |  left   |                    元素向左浮动。                    |
  |  right  |                    元素向右浮动。                    |
  |  none   | 默认值。元素不浮动，并会显示在其在文本中出现的位置。 |
  | inherit |         规定应该从父元素继承 float 属性的值          |

  

## dl：定义列表

```html
<dl>
   <dt>计算机</dt>
   <dd>用来计算的仪器 ... ...</dd>
   <dt>显示器</dt>
   <dd>以视觉方式显示信息的装置 ... ...</dd>
</dl>
```

* 类似ul



## ul：无序列表

```css
ul,dl{
	float: left;	/*左浮动：从左到右并排显示*/
    list-style: none;/*去小圆圈*/
}
```

* 属性：Type
  * disc：实心圆（默认）
  * circle：空心圆
  * square：实心方框
* reversed：倒序



## ol：有序列表

* start：排序的起点数值
* type：用来设置项目前面的标记
  * 1：数字（默认）
  * a：小写字母
  * A：大写字母
  * i：小写希腊字母
  * I：大写希腊字母



## Audio、Video：媒体

```html
<audio width="320" height="240" controls="controls">
  <source src="song.ogg" type="audio/ogg">
  <source src="song.mp3" type="audio/mpeg">
  你的浏览器不支持<audio>标签
</audio >
```

* 音频属性

  * autoplay：自动播放
  * loop：循环播放
  * controls：显示控件
  * preload：预加载（若使用autoplay属性则自动忽略）

* 视频属性

  * 同上
  * muted：规定视频的音频输出应该被静音
  * poster[URL]：规定视频未播放时的图像
  * src[URL]：视频链接
  * width & height：宽高

  

## table：表格

-   **tr（行）、th（表头）、td（单元）、caption（标题）**
  - **th**   所标识的单元格文字会以**粗体**显示，通常当做表格第一行的标题
- 说明：
  - width、height：宽高
  - border：边框宽度
  - cellpadding：单元内边距
  - cellmargin：单元外边距
  - align：水平
    - left
    - right
    - center
  - valign：垂直
    - top
    - middle
    - bottom
  - colspan：合并左右列  
  - rowspan：合并上下行   
- 让单元格文字不换行  **nowrap**  例：【td   nowrap】
- 遇到空白单元格时的处理方式：
  - 在其中输入全角空格（&emsp；）或（&nbsp；）即可解决
- **高度=行高，文字会垂直居中**
- 图片默认根据宽度对表格进行调整，故时而其下会有间隙，遇此情况
  - IMG CSS : display : block  //  将图片改成块元素
  - IMG CSS : display : flex  // 弹性布局
  - float : left  //  浮动



## HTML背景

* 设置背景颜色  **body bgcolor="#000000">**

* 设置背景图片 **body background="bg.jpg">**

* 设置页面文字颜色  **body text="#cccccc">**

* 尽量使用十六进制以及RGBA或RGB，利于浏览器渲染

* 背景图CSS设置：

  * ```css
    body {
                  /* 图片地址 */
                  background-image: url(09.jpg);
        
                  /* 图片按屏幕大小显示 */
                  background-size: cover;
        
                  /* 指定一个固定的背景图片 */
                  background-attachment: fixed;
        
                  /* 图片不重复 */
                  background-repeat: no-repeat;
        
                  /* 图片显示位置水平居中垂直居中 */
                  background-position: center center;
              }
    ```

    

## iframe内嵌框架

```html
<iframe src="xxx.html" frameborder="0" id="iframe" 
```

- 说明：

  - scrolling：是否显示滚动条
    - yes
    - no
    - auto
  - frameborder：是否显示边框
    - 1
    - 0

- 样式

  ```css
  iframe {
              position: fixed;
              /*固定定位*/
              right: 0;
              bottom: 0;
          }
  ```

- JavaScript

  ```JavaScript
  scrolling="no"></iframe>
      <script language="javascript">
          var timeIframe;
          window.onload = function () {
              timeIframe = setTimeout(GetIframeStatus, 10);
          }
          function GetIframeStatus() {
              var iframe = document.getElementById("iframe");
              var iframeWindow = iframe.contentWindow;
              //内容是否加载完
              if (iframeWindow.document.readyState == "complete") {
                  var iframeWidth, iframeHeight;
                  //获取Iframe的内容实际宽度
                  iframeWidth = iframeWindow.document.documentElement.scrollWidth;
                  //获取Iframe的内容实际高度
                  iframeHeight = iframeWindow.document.documentElement.scrollHeight;
                  //设置Iframe的宽度
                  iframe.width = iframeWidth;
                  //设置Iframe的高度
                  iframe.height = iframeHeight;
              } else {
                  timeIframe = setTimeout(GetIframeStatus, 10);
              }
          }
      </script>
  ```



## form表单

```html
<form name="form1" action="URL" method="get">
	用户名：<input type="text" name="uname" />
	密 码：<input type="password" name="passwd" />
</form>

```



- method（设置发送数据的方式）：

  - post  和  get   
    - 使用get方式发送数据，数据会直接加载URL之后，安全性比较差，并且有255个字符的字数限制
    - post方式是将数据封装之后再发送，字符串长度没有限制，数据安全性比较高。对于需要保密的信息，通常会采用post方式进行发送

- action

  - 表单提交地址

- enctype：MIME方式

  - MIME：
    - Multipurpose Internet Mail Extensions
    - 多用途互联网邮件扩展类型
  - 表单发送的编码方式，只有method=“post”时才有效
  - enctype="application/x-www-form-urlencoded"：此为默认值，若enctype省略不写，则表示采取此种编码模式
  - enctype="multipart/form-data"：用于上传文件的时候
  - enctype="text/plain"：将表单属性发送到电子邮箱时，enctype的值必须设为"text/plain",否则将会出现乱码

- marquee：滚动内容（过时）

  - marquee元素已经 **过时**，请不要再使用。尽管一些浏览器仍然支持它，但它不是必须的。此外，使用这个元素基本上是你可以对你的用户做最糟糕的事情之一，所以请不要这样做。
  - direction ：滚动的方向
    - left（默认）
    - right
    - up
    - down
  - behavior ：滚动的方式
    - scroll：连续滚动
    - slide：滑动一次
    - alternate：来回滚动
  - loop ：循环的次数
    - 正整数
    - 默认为无限循环 
  - scrollamount ：运动速度
    - 正整数，默认为6 
  - scrolldelay ：停顿时间
    - 正整数，默认为0，单位是毫秒 
  - align ：元素的垂直对齐方式
    - top
    - middle（默认）
    - bottom
  - bgcolor ：运动区域的背景色
    - 16进制的RGB颜色，默认为白色
  - height、width：运动区域的高度和宽度
    - 正整数(单位是像素)
    - 百分数
    - 默认：width=100% height为**标签**内元素的高度。 
  - hspace、vspace ：元素到区域边界的水平距离和垂直距离
    - 正整数，单位是像素。 
  - onmouseover=this.stop() onmouseout=this.start() ：当鼠标以上区域的时候滚动停止，当鼠标移开的时候又继续滚动。 

- target（打开方式）

  - _blank：打开新窗口
  - _self ：当前的窗口
  - _parent：上一层窗口（父窗口）
  - _top：最上层窗口
  - 框架名称：直接指定窗口或框架名称

- novalidate：规定当提交表单时不对表单数据（输入）进行验证。

  - ```html
    <form action="demo_form.html" novalidate>
    E-mail: <input type="email" name="user_email">
    		<input type="submit">
    </form> 
    ```

- autocomplete：规定表单是否应该启用自动完成功能。

  - on：浏览器会基于用户之前键入的值自动完成值。
  - off：用户必须在每次使用时输入值到每个字段中，浏览器不会自动完成输入。

### input：输入框

- 说明

  - placeholder：显示在输入框的内容

  - readonly：是否只读

  - maxlength：输入字符的最大长度

  - disabled：是否禁用

  - value：输入框中填入的值

  - checkbox ：复选框   

    - 此时name属性应为xxx [ ]

  - selected ：下拉框默认选中

  - datalist：规定了 input> 元素可能的选项列表。

    - ```html
      <input list="browsers"> 
      <datalist id="browsers"> 
          <option value="Internet Explorer"> 
          <option value="Firefox"> 
          <option value="Chrome"> 
          <option value="Opera"> 
          <option value="Safari"> 
      </datalist>
      ```

    - 提供"自动完成"的特性。用户能看到一个下拉列表，里边的选项是预先定义好的，将作为用户的输入数据。

    - 使用 input> 元素的 list 属性来绑定 datalist> 元素。

  - output：作为计算结果输出显示(比如执行脚本的输出)。

    - ```html
      <form oninput=
      "x.value=parseInt(a.value)+parseInt(b.value)">
          0
        <input type="range" id="a" value="50">
          100+
        <input type="number" id="b" value="50">
        	=
        <output name="x" for="a b"></output>
      </form> 
      ```

  - hidden

    - hidden 属性规定对元素进行隐藏。
    - 隐藏的元素不会被显示。
    - 如果使用该属性，则会隐藏元素。
    - 可以对 hidden 属性进行设置，使用户在满足某些条件时才能看到某个元素（比如选中复选框，等等）。然后，可使用 JavaScript 来删除 hidden 属性，使该元素变得可见。

  - radio：单选   

    - name必须相同

      #### label：

      * 将输入项或选项及其标签文字关联起来

      - 使单选**文字**部分也具有点击效果

      ```html
      <p>
      	<!-- 状态的属性，写个名字就可以了 autoplay loop checked选中 required必填-->
      单选按钮：
      	<input type="radio" name="sex" value="男" id="nan">
      	<label for="nan">男生</label>
      	<input type="radio" name="sex" value="女" checked id="nv">
      <label for="nv">女生</label>
      </p>
      ```

  - autocomplete

    - 用来设置input组件是否使用自动完成功能
      - on
      - off 
    - 自动完成允许浏览器预测对字段的输入。当用户在字段开始键入时，浏览器基于之前键入过的值，应该显示出在字段中填写的选项。
    - 适用于 form>，以及下面的 input> 类型：
      - text, search, url, telephone, email, password, datepickers, range 以及 color

  - autofocus：当页面加载时 input> 元素应该自动获得焦点

    - ```html
      <form action="demo_form.html">
      	First name: 
      	<input type="text" name="fname" autofocus>
         	<br>
      	Last name: 
      	<input type="text" name="lname"><br>
      	<input type="submit">
      </form> 
      ```

  - form：input> 元素所属的一个或多个表单。

    - ```html
      <form action="demo-form.php" id="form1">
      	First name: 
          <input type="text" name="fname">
          <br>
      	<input type="submit" value="提交">
      </form>
      
      <p> 
          "Last name" 字段没有在 form 表单之内，
          但它也是 form 表单的一部分。
      </p>
      
      Last name: <input type="text" name="lname" form="form1">
      
      <p><b>注意:</b> IE 不支持 form 属性</p>
      ```

  - required ：必须在提交之前填写输入域（不能为空）。

    - ```html
      <form action="" method="post" enctype="" >
      	<label for="user">用户名：</label>
      	<input type="text" name="user" id="user" required>
          <br>
      	<label for="password">密　码：</label>
      	<input type="password" name="password" id="password" > 
          <input type="submit" name="" value="提交">
      </form> 
      ```

      

  - checked：状态属性

    - 默认选中

  - accept：用于指定文件类型

    - ```
      accept=".jpg,.jpeg,.png,.gif"
      ```

  - file：文件上传  

    - ```html
      <input type="file" name="pic2" accept="image/*">
      ```

    -  multiple：控制是否上传多文件

  - number  //  数字输入框

    - [max](https://www.runoob.com/tags/att-input-max.html) - 规定允许的最大值。
    - [min](https://www.runoob.com/tags/att-input-min.html) - 规定允许的最小值。
    - [step](https://www.runoob.com/tags/att-input-step.html) - 规定合法数字间隔。
    - [value](https://www.runoob.com/tags/att-input-value.html) - 规定默认值。

- 去除输入框得到焦点时，浏览器出现的蓝色带阴影的边框

  - ```css
    input{
    	outline: 0;
    }
    		OR	
    input{
    	focus:outline: none;
    }
    ```

- enctype="multipart/form-data"  

  - 指表单数据有多部分构成，既有文本数据，又有文件等二进制数据
  - 默认情况下，enctype的值是application/x-www-form-urlencoded，不能用于文件上传，只有使用了multipart/form-data，才能完整的传递文件数据。
  - application/x-www-form-urlencoded不是不能上传文件，是只能上传文本格式的文件，multipart/form-data是将文件以二进制的形式上传，这样可以实现多种类型的文件上传。



|         值          |                             描述                             |
| :-----------------: | :----------------------------------------------------------: |
|       button        |   定义可点击的按钮（通常与 JavaScript 一起使用来启动脚本）   |
|      checkbox       |                          定义复选框                          |
|        file         |        定义文件选择字段和 "浏览..." 按钮，供文件上传         |
|       hidden        |                       定义隐藏输入字段                       |
|        image        |                     定义图像作为提交按钮                     |
|      password       |             定义密码字段（字段中的字符会被遮蔽）             |
|        radio        |                         定义单选按钮                         |
|        reset        |           定义重置按钮（重置所有的表单值为默认值）           |
|       submit        |                         定义提交按钮                         |
|        text         |     默认。定义一个单行的文本字段（默认宽度为 20 个字符）     |
| color(以下为H5新增) |                          定义拾色器                          |
|        date         |         定义 date 控件（包括年、月、日，不包括时间）         |
|      datetime       | 定义 date 和 time 控件（包括年、月、日、时、分、秒、几分之一秒，基于 UTC 时区） |
|   datetime-local    | 定义 date 和 time 控件（包括年、月、日、时、分、秒、几分之一秒，不带时区） |
|        email        |                  定义用于 e-mail 地址的字段                  |
|        month        |             定义 month 和 year 控件（不带时区）              |
|       number        |                    定义用于输入数字的字段                    |
|        range        |   定义用于精确值不重要的输入数字的控件（比如 slider 控件）   |
|       search        |               定义用于输入搜索字符串的文本字段               |
|         tel         |                  定义用于输入电话号码的字段                  |
|        time         |              定义用于输入时间的控件（不带时区）              |
|         url         |                   定义用于输入 URL 的字段                    |
|        week         |              定义 week 和 year 控件（不带时区）              |



### **textarea**：定义一个多行的文本输入控件

```html
<textarea rows="10" cols="30">
我是一个文本框。
</textarea>
```

* 说明

  * autofocus：当页面加载时，文本区域自动获得焦点。

  * cols：文本区域内可见的宽度。

    * 值：数字

  * disabled：禁用文本区域。

  * form：文本区域所属的一个或多个表单。

    * ```html
      <form action="demo-form.php" id="usrform">
        	Name: 
          <input type="text" name="usrname">
        	<input type="submit">
      </form>
      <br>
      <textarea rows="4" cols="50" name="comment" form="usrform">
      输入内容...
      </textarea>
      <p>
          以上的表单在文本框之外，但是它仍是表单中的一部分。</p>
      <p>
          <b>注意：</b> 
          IE 不支持 form 属性。
      </p>
      ```

  * maxlength：文本区域允许的最大字符数。

    * 值：数字

  * name：文本区域的名称

  * placeholder：提示

  * readonly：规定文本区域为只读。

  * required：规定文本区域是必需的/必填的。

  * rows：规定文本区域内可见的行数。

    * 值：数字

  * wrap：当提交表单时，文本区域中的文本应该怎样换行。

    * soft：文本不换行（默认）
    * hard：文本换行（包含换行符）。当使用 "hard" 时，必须指定 cols 属性。



### select：下拉框

```html
<select name="city">
<option value="0">请选择</option
<option value="bj">北京</option>
<option value="gz">广州</option>
</select>
```

* 说明：
  * name：名称
  * size：下拉框显示的行数
  * multiple：是否多选
  * disabled：是否禁用
  * selected：是否默认选中
  * value：选项的值



### optgroup：下拉框分组

```html
<select name="city" multiple>
		<optgroup label="广东">
			<option value="1">广州</option>
			<option value="2">深圳</option>
		</optgroup>
		<optgroup label="其他">
			<option value="3">长沙</option>
			<option value="4">香港</option>
		</optgroup>
</select>
```



## 居中

* 行内元素：text-align：center；
* 定宽块元素：margin：0 auto；

* 居中的三个条件： 

  * 必须是块元素(不可以是行元素) 
  * 有明显的宽（width:xxpx） 
  * margin：0px auto；

* 文本属性居中

  * align:设置水平对齐方式（left/right/center/justify）
  * valign:设置垂直对齐方式（top/middle/bottom）
  * 上面的不常用，下面的常用
    * text-align:
      * 设置水平对齐方式
      * left/right/center/justify
    * vertial-align:
      * 设置垂直对齐方式
      * top/middle/bottom

  ### 水平居中：

* 给div设置一个宽度，然后添加margin:0 auto属性

  ```css
  div{
      width:200px;
      margin:0 auto;
    }
  ```

  

  * 让绝对定位的div居中

  ```css
  div {
      position: absolute;
      width: 300px;
      height: 300px;
      margin: auto;
      top: 0;
      left: 0;
      bottom: 0;
      right: 0;
      background-color: bule;
   }
  ```

  

  ### 水平垂直居中

  * 确定容器的宽高 宽500 高 300 的层 设置元素的外边距

  ```css
   div {
      position: relative;     /* 相对定位或绝对定位均可 */
      width:500px;
      height:300px;
      top: 50%;
      left: 50%;
      margin-top: -150px；
      margin-left:  -250px;       /* 外边距为自身宽高的一半 */
      //margin:-150px 0 0 -250px; /*一样*/
      background-color: blue; 
    }
  ```

  

  * 未知容器的宽高，利用 transform 属性

  ```css
  div {
      position: absolute;     /* 相对定位或绝对定位均可 */
      width:500px;
      height:300px;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background-color: blue;
   }
  ```

  

  * 利用 flex 布局

  ```css
  .container {
      display: flex;
      align-items: center;        /* 垂直居中 */
      justify-content: center;    /* 水平居中 */
   }
   .container div {
      width: 100px;
      height: 100px;
      background-color: blue; 
   }
  ```

  



##  HTML 文本格式化标签

|  标签  |              描述               |
| :----: | :-----------------------------: |
|   b    |          定义粗体文本           |
|   em   |          定义着重文本           |
|   i    |           定义斜体字            |
| small  |           定义小号字            |
| strong | 定义加重语气（HTML5  推荐粗体） |
|  sub   |           定义下标字            |
|  sup   |           定义上标字            |
|  ins   |           定义插入字            |
|  del   |           定义删除线            |

* 粗体、斜体、下划线（最好使用CSS语法代替）
* em/strong/:  我们并不反对使用这个标签，但是如果您只是为了达到某种视觉效果而使用这个标签的话，我们建议您使用 CSS ，这样可能会取得更丰富的效果。
* small  :  small 标签定义小型文本（和旁注）。
* del和ins  :  <del 和 <ins 一起使用，描述文档中的更新和修正。浏览器通常会在已删除文本上添加一条删除线，在新插入文本下添加一条下划线





##   HTML "计算机输出" 标签

| 标签 |        描述        |
| :--: | :----------------: |
| code |   定义计算机代码   |
| kbd  |     定义键盘码     |
| samp | 定义计算机代码样本 |
| var  |      定义变量      |
| pre  |   定义预格式文本   |

* kdb  :  kbd 标签定义键盘文本。

  **提示:** kbd标签已废弃，不推荐使用，但 是可以通过CSS实现丰富的效果

* code  :  code标签是一个短语标签，用来定义计算机代码文本

* samp标签是一个短语标签，用来定义计算机程序的样本文本。

* var标签是一个短语标签，用来定义变量。

* abbr 标签用来表示一个缩写词或者首字母缩略词，如"WWW"或者"NATO"
  通过对缩写词语进行标记，您就能够为浏览器、拼写检查程序、翻译系统以及搜索引擎分度器提供有用的信息。

* samp/var  :  我们并不反对使用这个标签，但是如果您只是为了达到某种视觉效果而使用这个标签的话，我们建议您使用 CSS ，这样可能会取得更丰富的效果。

## HTML 引文, 引用, 及标签定义

|    标签    |        描述        |
| :--------: | :----------------: |
|    abbr    |      定义缩写      |
|  address   |      定义地址      |
|    bdo     |    定义文字方向    |
| blockquote |    定义长的引用    |
|     q      |   定义短的引用语   |
|    cite    |   定义引用、引证   |
|    dfn     | 定义一个定义项目。 |

* address标签定义文档作者/所有者的联系信息如果 

  address元素位于 body元素内部，则它表示该文档作者/所有者的联系信息。

  如果 address元素位于 article 元素内部，则它表示该文章作者/所有者的联系信息。
  
  address 元素的文本通常呈现为斜体。大多数浏览器会在该元素的前后添加换行。
    **提示：**不应该使用 address 标签来描述邮政地址，除非这些信息是联系信息的组成部分。
  
    **提示：**address 元素通常被包含在footer元素的其他信息中。
  
* bdo 指的是 bidi 覆盖（Bi-Directional Override）。  [  ltr  :  left to right  /  rtl  :  right to left  ]

  bdo标签用来覆盖默认的文本方向。
  bdo元素一般用于把一段文本的方向规定为与周围文本的自然方向相反的方向。方向由**必需属性dir**指定。bdo元素很少使用，只用于某些**多语言文档**。在这种文档中，可能有某一段文本使用的语言的阅读方式与文档中其他部分使用的语言的阅读方式不同。

* blockquote> 标签定义摘自另一个源的块引用。

  浏览器通常会对 blockquote元素进行缩进。

  **提示：**如果标记是不需要段落分隔的短引用，请使用q

* q> 标签定义一个短的引用。

  浏览器经常会在这种引用的周围插入引号。

  **提示：**请使用blockquote来标记摘自另一个源的块引用。

* cite> 标签定义作品（比如书籍、歌曲、电影、电视节目、绘画、雕塑等等）的标题。

  **注释：**人名不属于作品的标题。

* dfn> 标签是一个短语标签，用来定义一个定义项目。

* dfn  :  我们并不反对使用这个标签，但是如果您只是为了达到某种视觉效果而使用这个标签的话，我们建议您使用 CSS ，这样可能会取得更丰富的效果。



## HTML元素分类：inline、inline-block、block

- - inline
    - textarea、span、a、img、input、select
    - 行内元素特征：
      - 设置宽高无效
      - 对margin仅设置左右方向有效，上下无效；padding设置上下左右都有效，即会撑大空间,行内元素尺寸 由内含的内容决定，盒模型中 padding, border 与块级元素并无差异，都是标准的盒模型，但是 margin 却只有水平方向的值，垂直方向并没有起作用。行内元素的水平方向的padding-left,padding-right,margin- left,margin-right 都产生边距效果，但是竖直方向的padding-top,padding-bottom,margin-top,margin-bottom都 不会产生边距效果。padding设置上下左右都有效，即会撑大空间但是不会产生边距效果。
      - 不会自动进行换行
      - 元素宽度在不设置的情况下，是它本身父容器的100%（和父元素的宽度一致），除非设定一个宽度。
  - inline-block
    - 行内块状元素特征：
      - 不自动换行
      - 能够识别宽高
      - 默认排列方式为从左到右
  - block
    - div、p、ul、h1等标题元素、ol、form、table
      块状元素特征：
      - 能够识别宽高
      - margin和padding的上下左右均对其有效
      - 可以自动换行
      - 多个块状元素标签写在一起，默认排列方式为从上至下

- inline-block和float的区别

  - 文档流（Document flow）:浮动元素会脱离文档流，并使得周围元素环绕这个元素。而inline-block元素仍在文档流内。因此设置inline-block不需要清除浮动。当然，周围元素不会环绕这个元素，你也不可能通过清除inline-block就让一个元素跑到下面去。
  - 水平位置（Horizontal position）：很明显你不能通过给父元素设置text-align:center让浮动元素居中。事实上定位类属性设置到父元素上，均不会影响父元素内浮动的元素。但是父元素内元素如果设置了display：inline-block，则对父元素设置一些定位属性会影响到子元素。（这还是因为浮动元素脱离文档流的关系）。
  - 垂直对齐（Vertical alignment）：inline-block元素沿着默认的基线对齐。浮动元素紧贴顶部。你可以通过vertical属性设置这个默认基线，但对浮动元素这种方法就不行了。这也是我倾向于inline-block的主要原因。
  - 空白（Whitespace）：inline-block包含html空白节点。如果你的html中一系列元素每个元素之间都换行了，当你对这些元素设置inline-block时，这些元素之间就会出现空白。而浮动元素会忽略空白节点，互相紧贴.
  - scrolling="no"
    隐藏滚动条

- html很多标签都有默认样式，因此最好在样式中一开始就给表单标签去除默认的样式问题

  ```html
  <style type="text/css">
        input,select,option,textarea{outline: none;}
  </style>
  ```

# TIPS

```
<body onload="init()">//打开页面的同时调用init
```



## OTHER（应合理分类并及时归类）

