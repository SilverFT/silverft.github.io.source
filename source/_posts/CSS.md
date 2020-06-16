---
title: CSS
copyright: true
date: 2019-06-05 23:26:22
tags: 前端
---



# CSS命名规范

## 常规命名

* 头：header
* 内容：content/container
* 尾：footer
* 导航：nav
* 侧栏：sidebar
* 栏目：column
* 页面外围控制整体布局宽度：wrapper
* 左右中：left right center
* 登录条：loginbar
* 标志：logo
* 广告：banner
* 页面主体：main
* 热点：hot
* 新闻：news
* 下载：download
* 子导航：subnav
* 菜单：menu
* 子菜单：submenu
* 搜索：search
* 友情链接：friendlink
* 页脚：footer
* 版权：copyright
* 滚动：scroll
* 内容：content
* 标签页：tab
* 文章列表：list
* 提示信息：msg
* 小技巧：tips
* 栏目标题：title
* 加入：joinus
* 指南：guild
* 服务：service
* 注册：regsiter
* 状态态：status
* 投票：vote
* 合作伙伴：partner

## 注释的写法

/* Footer */
内容区
/* End Footer */

## id的命名

* 容器: container
* 页头：header
* 内容：content/container
* 页面主体：main
* 页尾：footer
* 导航：nav
* 侧栏：sidebar
* 栏目：column
* 页面外围控制整体布局宽度：wrapper
* 左右中：left right center

## 页面结构

* 容器: container
* 页头：header
* 内容：content/container
* 页面主体：main
* 页尾：footer
* 导航：nav
* 侧栏：sidebar
* 栏目：column
* 页面外围控制整体布局宽度：wrapper
* 左右中：left right center

## 导航

* 导航：nav
* 主导航：mainbav
* 子导航：subnav
* 顶导航：topnav
* 边导航：sidebar
* 左导航：leftsidebar
* 右导航：rightsidebar
* 菜单：menu
* 子菜单：submenu
* 标题: title
* 摘要: summary

## 功能

* 标志：logo
* 广告：banner
* 登陆：login
* 登录条：loginbar
* 注册：regsiter
* 搜索：search
* 功能区：shop
* 标题：title
* 加入：joinus
* 状态：status
* 按钮：btn
* 滚动：scroll
* 标签页：tab
* 文章列表：list
* 提示信息：msg
* 当前的: current
* 小技巧：tips
* 图标: icon
* 注释：note
* 指南：guild
* 服务：service
* 热点：hot
* 新闻：news
* 下载：download
* 投票：vote
* 合作伙伴：partner
* 友情链接：link
* 版权：copyright

## class的命名

(1)颜色:使用颜色的名称或者16进制代码,如

```css
.red { color: red; }
.f60 { color: #f60; }
.ff8600 { color: #ff8600; }
```

(2)字体大小,直接使用"font+字体大小"作为名称,如

```css
.font12px { font-size: 12px; }
.font9pt {font-size: 9pt; }
```

(3)对齐样式,使用对齐目标的英文名称,如

```css
.left { float:left; }
.bottom { float:bottom; }
```

(4)标题栏样式,使用"类别+功能"的方式命名,如

```css
.barnews { }
.barproduct { }
```



## 注意事项

1.一律小写;
2.尽量用英文;
3.不加中杠和下划线;
4.尽量不缩写，除非一看就明白的单词.

* 主要的 master.css
* 模块 module.css
* 基本共用 base.css
* 布局，版面 layout.css
* 主题 themes.css
* 专栏 columns.css
* 文字 font.css
* 表单 forms.css
* 补丁 mend.css
* 打印 print.css

# CSS样式

## 字体样式

- font-family=“微软雅黑”;
  - 当指定多种字体时，用“，”分隔每种字体的名称
  - 当字体名称包含两个以上分开的单词是，用“”把该字体名称括起来。
  - 当样式规则外已经有“”时,用‘’代替“”。
- color=#ccc;
  - /*设置字体颜色*/
  - 16进制
  - RGBA
- text-decoration:underline;
  - /*字体加下划线*/
- text-decoration:none;
  - /*去下划线*/
- font-size:14px;
  - /*字体的大小*/
- font-style:
  - normal正常状态
  - italic斜体字
  - oblique 斜体和正常状态之间
- font-weight:
  - number(100～900) 
  - lighter（细体） 
  - bold(粗体)
  - bolder（特粗体）
- text-transform:
  - uppercase 所有文字大写显示
  - lowercase:所有文字小写显示
  - capitalize 每个单词的头字母大写
  - none 不继承母体的文字变形参数
- text-decoration:
  - underline 为文字加下划线
  - overline 为文字加上划线
  - line-through 为文字加删除线
  - blink	使文字闪烁
  - none 不显示上叙任何效果
- 可以用font 属性全部定位
  - p{font:italic bold 12pt;}

## 边框与填充样式

- margin：
  - 外边距
  - 与边距的距离 
  - (margin-top margin-left margin-bottom margin-left)
  - 取值可以是：auto默认
  - 百分比或者具体的值：
  - 取值可以是一个或者两个或者三个或者四个（每个都具有不同的含义）。 
  - 4:上右下左
  - 3：上，左右，下
  - 2：上下，左右
- padding
  - 内边距
  - 复合属性填充（指用白值填充）
  - 和margin的用法一样。  
- border-style
  - border-top-style:上边框样式
  - border-right-style:右边框样式
  - border-bottom-style:底边框样式
  - border-left-style:左边框样式
  - 取值：
    - none	不现实边框，为默认值
    - dotted	点线（电线）
    - dashed	虚线，也称短线
    - solid	实线
    - double	双实线
    - groove	边框带有立体感的沟槽
    - ridge	边框成脊形
    - inset	使整个表框凹陷，即在边框内嵌入一个立体边框
    - outset	使整个边框凸起，即在边框外嵌入一个立体边框  
- border-color=“#ccc”;
  - /*设置边框颜色*/
- border-width：
  - border-top-width:上边框宽度
  - border-right-width:右边框宽度
  - border-bottom-width:底边框宽度
  - border-left-width:左边框宽度
  - 取值为：
    - medium 默认宽度
    - thin 细边框 
    - thick 粗边框  
- border:1px solid #999;
  - /*添加一条边框*/
  - border-top：上边框
  - border—right：右边框
  - border—bottom：底边框
  - border-left：左边框

## 背景样式

- background-color 
  - 背景颜色
- background-image 
  - 背景图片
- background-repeat:
  - repeat 表示图像从水平和垂直角度平铺
  - no-repeat 不重复平铺背景图片
  - repeat-x 使图片只在水平方向上平铺
  - repeat-y 使图片只在垂直方向上平铺
- background-attachment 参数
  - fixed 网页滚动时，背景图片相对浏览器而言固定不动
  - scroll 网页滚动时，背景图片相对浏览器而言一起滚动
- background-postion ：
  - （背景定位）
  - top 相对前景对象顶对齐
  - bottom 相对前景对象底对齐
  - left 相对前景对象左对齐
  - right 相对前景对象右对齐
  - center 相对前景对象中心对齐
- 可以直接用 background 复合属性来确定式样
  - 示例：
  - table{background:#001122 url(zhouliang.jpg) no-repeat bottom right}

## 文本样式

- word-spacing:
  - 英文单词间距 
  - 取值：normal或者是单位像素
- letter-spacing:
  - 英文字母间距 
  - 取值可以是：normal或者是单位像素
- line-height:
  - 行距 
  - 可以是精确的值，也可以是百分比
- text-aglin:
  - 文本水平排列
  - left: 左对齐 
  - right：右对齐 
  - center: 居中 
  - justify:相对左右对齐。
  - 注意到：text-aglin 是块级属性，只能用于p、blockquqte、ul、h1-h6等表示
- vertical-align:
  - 文本垂直排列 
  - top 顶对齐 bottom 底部对齐 text-top 相对文本顶对齐
  - text-bottom相对文本底对齐 baseline:基准线对齐 middle 中心线对齐
  - sub 以下标的形式对齐 sup 以上标的形式对齐,相对于元素行高属性的百分比
- text-indent：
  - 文本缩进 
  - 缩进距离必须是值或者百分比  
- white-space
  - normal：合并连续的多个空格
  - pre：保留原样式
  - nowrap：不换行，直到遇到br标签  
- text-decoraition
  - none :表示不对文本进行修饰，也是默认值，
  - underline:表示对文字添加下划线
  - overline:表示添加上划线
  - line-through:表示对文本添加删除线
  - blink:表示文字具有闪烁效果  
- text-transform：文本转换
  - none:表示原有值
  - capitalize:使每个字的第一个字母大写
  - uppercase:大写
  - lowercase:小写  

## 定位样式

- postion 
  - absolute	采用绝对定位（分别用四个边框来定位）
  - relative	采用相对定位（也得用四个边框来设定位置）
  - static	默认值  
- left/top/width/height
  - 设置值可以是  
- z-index
  - 也就是元素的堆叠,大的在上，小的在下。默认是按照先后顺序
  - 取值auto默认值，表示它遵循其父对象的定位属性
  - 如果设置为数字,必须是无单位的正整数，可以取负值，但是一般为正数,一般数字为1时间是最底层

## 布局样式

- visibility 可视性

  - inherit：表示对象继承父本的继承性。
  - visible:表示对象可见
  - hidden：表示对象隐藏  

- 视口

  - width=device-width ：表示宽度是设备屏幕的宽度
  - initial-scale=1.0：表示初始的缩放比例
  - minimum-scale=0.5：表示最小的缩放比例
  - maximum-scale=2.0：表示最大的缩放比例
  - user-scalable=yes：表示用户是否可以调整缩放比例

- display 

  - 设置或检索对象是否及如何显示
  - block、inline、list-item、none  

- clip 

  - 可视区域
  - auto表示对象不裁剪
  - rect(数值表示)(一般有四个设置值：方向定位于上右下左的顺序，一般以左上角(0,0)坐标计算4个偏移数值。其中 任何一个值都可以用auto代替)

- overflow

  - 超出范围
  - isible 扩大浏览器
  - hidden 裁剪掉多余的文本
  - scroll	滚动条
  - auto 当有多余的时候才显示滚动条

- ### ***float***	浮动属性

  - left表示文字浮在元素左侧
  - right 表示文字浮在元素右侧
  - none 默认值，表示不浮动。
  - ***重点***

- clear ：

  - 表示指定一个元素周围是都允许有其他元素漂浮在它的周围。
  - left ,right,none,both;指要清除本元素四周的浮动对象

- page-break-before 

  - always 是否强制分页

- page-break-after

  - always 打印后设置是否强制分页

- width和height 

  - 表示层的宽度与高度
  - 设置值为 auto|数值

## 列表样式

- list-style-type 
  - 指显示于列表项前的标识符号
  - none 表示不显示列表符号  
- list-style-postion 
  - 列表缩进 
  - inside 列表内容和列表标识符号处在不同垂直位置，在符号内侧
  - outside 列表内容和列表标识符号处在同一垂直位置 
- list-style-image
  - 用图片符号作为链接标题
  - none	表示不指定图像
  - url(网页地址)	指定图片位置
- list-style
  - 复合属性：实现以上三种

## 光标样式

- cursor 
  - 当点击某个内容时，鼠标显示其他的图形
  - style="cursor:hand" 手形
  - style="cursor:crosshair" 十字形



# CSS尺寸

## tips

**任意浏览器的默认字体高都是16px。所有未经调整的浏览器都符合:**
**1em=16px。那么12px=0.75em,10px=0.625em。为了简化font-size的换算，需要在css中的body选择器中声明Font-size=62.5%，这就使em值变为**
**16px*62.5%=10px, 这样12px=1.2em, 10px=1em, 也就是说只需要将你的原来的px数值除以10，然后换上em作为单位就行了**

## 绝对单位

* in

  * 英寸（Inch），绝对长度单位

* pt

  * 绝对长度单位。点（Point）。
  * 1in = 2.54cm = 25.4 mm = 72pt = 6pc

* pc

  * 绝对长度单位。派卡（Pica）。相当于我国新四号铅字的尺寸。

    ​    1in = 2.54cm = 25.4 mm = 72pt = 6pc

* cm

  * 绝对长度单位。厘米（Centimeter）。

    ​    1in = 2.54cm = 25.4 mm = 72pt = 6pc

* mm

  * 绝对长度单位。毫米（Millimeter）。

    ​    1in = 2.54cm = 25.4 mm = 72pt = 6pc

## 相对长度单位

* px
  * 相对长度单位。像素（Pixel）
* em
  * 相对长度单位。相对于当前对象内文本的字体尺寸
* ex
  * 相对长度单位。相对于字符“x”的高度。此高度通常为字体尺寸的一半。
  * 如当前对行内文本的字体尺寸未被人为设置，则相对于浏览器的默认字体尺寸。
* rem
  * 区别在于使用rem为元素设定字体大小时，仍然是相对大小，但相对的只是HTML根元素
  * **选择使用什么字体单位主要由你的项目来决定，如果你的用户群都使用最新版的浏览器，那推荐使用rem，如果要考虑兼容性，那就使用px,或者两者同时使用**

