---
title: Emmet
copyright: true
date: 2019-05-19 16:14:08
tags: blog
---

# html缩写



## id（#）,class（.）

id指令:   # 

class指令:   .

* div#test

```html
<div id="test"></div>
```
* div.test
```html
<div class="test"></div>
```



## 子节点（>），兄弟节点（+），上级节点（^）

子节点指令:   >  

兄弟节点指令:   + 

上级节点:   ^

* div>ul>li>p

```html
<div>
   <ul>
     <li>
       <p></p>
     </li>
   </ul>
 </div>
```


* div+ul+p

```html
<div></div>
<ul></ul>
<p></p>
```

* div>ul>li^div

 (这里的^是接在li后面所以在li的上一级，与ul成了兄弟关系,当然两个^^就是上上级）

```html
<div>
   <ul>
     <li></li>
   </ul>
   <div></div>
 </div>
```



## 重复（*）

重复指令：*

div*5（*号后面添加数字表示重复的元素个数）
```html
   <div></div>
   <div></div>
   <div></div>
   <div></div>
   <div></div>
```



## 分组（()）

分组指令：()

* div>(ul>li>a)+div>p
  （括号里面的内容为一个代码块，表示与括号内部嵌套和外面的的层级无关）

```html
<div>
   <ul>
     <li><a href=""></a></li>
   </ul>
   <div>
     <p></p>
   </div>
 </div>
```

解释：这里如果不加括号的话，猜想下，a+div这样div就是和a是兄弟关系了，会包含在li里面。懂了吧哈哈
```html
 <div>
   <ul>
     <li>
       <a href=""></a>
       <div>
         <p></p>
       </div>
     </li>
   </ul
```



## 属性（[attr]）——id，class都有怎么能少了属性呢

属性指令：[]

* a[href=’###’ name=‘xiaoA’] 

（中括号内填写属性键值对的形式，并且空格隔开）

```html
<a href="###" name="xiaoA"></a>
```


## 编号  $ 

* ul>li.test$*3

*（$代表一位数，后面更上*数字就代表从1递增到填写的数字）

```html
 <ul>
   <li class="test1"></li>
   <li class="test2"></li>
   <li class="test3"></li>
 </ul>
```

注意：

一个$ 代表一位数，
如果想自定义从几开始递增的话就利用：$@+数字数字

* ul>li.test$@33

```html
 <ul>
   <li class="test33"></li>
   <li class="test34"></li>
   <li class="test35"></li>
 </ul>
```


## 文本（{}）

文本指令：{}

* ul>li.test$*3{测试$} 

  （{里面填写内容，可以和$一起组合使用哦}）

```html
<ul>
  <li class="test1">测试1</li>
  <li class="test2">测试2</li>
  <li class="test3">测试3</li>
</ul>
```


## 隐式标签

这个标签没有指令，而是部分标签可以不使用输入标签，直接输入指令，即可识别父类标签。

例如：.test
```html
<div class="test"></div>
```


* ul>.test$*3

```html
 <ul>
   <li class="test1"></li>
   <li class="test2"></li>
   <li class="test3"></li>
 </ul>
```


* select>.test$*5

```html
<select name="" id="">
  <option class="test1"></option>
  <option class="test2"></option>
  <option class="test3"></option>
  <option class="test4"></option>
  <option class="test5"></option>
</select>
```



等等…
隐私标签有如下几个：

* li：用于 ul 和 ol 中
* tr：用于 table、tbody、thead 和 tfoot 中
* td：用于 tr 中
* option：用于 select 和 optgroup 中



# CSS缩写

## **值** 

比如要定义元素的宽度，只需输入w100，即可生成 

1. ```css
   width: 100px;  
   ```

   
   
   * width:30px==>w30+tab
   * Height:30px==>h30+tab
   * Margin:30px==>mg30+tab
   * Padding:30px==> pd30+tab
   * Line-height:12px==>lh12px+tab
   * Background==>bg+tab
   * Background-color==>bgc+tab

 

除了px，也可以生成其他单位，比如输入h10p+m5e，结果如下： 

1. ```css
   1. height: 10%;  
   2. margin: 5em;  
   ```

   

 

单位别名列表： 

- p 表示%
- e 表示 em
- x 表示 ex



##  **附加属性** 

可能你之前已经了解了一些缩写，比如 @f，可以生成：

1. ```css
   1. @font-face {  
   2.   font-family:;  
   3.   src:url();  
   4. }  
   ```

   


一些其他的属性，比如background-image、border-radius、font、@font-face,text-outline、text-shadow等额外的选项，可以通过“+”符号来生成，比如输入@f+，将生成： 

1. ```css
   1. @font-face {  
   2.   font-family: 'FontName';  
   3.   src: url('FileName.eot');  
   4.   src: url('FileName.eot?#iefix') format('embedded-opentype'),  
   5. ​     url('FileName.woff') format('woff'),  
   6. ​     url('FileName.ttf') format('truetype'),  
   7. ​     url('FileName.svg#FontName') format('svg');  
   8.   font-style: normal;  
   9.   font-weight: normal;  
   10. }  
   ```

   

 

## **模糊匹配** 

如果有些缩写你拿不准，Emmet会根据你的输入内容匹配最接近的语法，比如输入ov:h、ov-h、ovh和oh，生成的代码是相同的： 

1. ```css
   overflow: hidden;  
   ```

   

 

 

## **供应商前缀** 

如果输入非W3C标准的CSS属性，Emmet会自动加上供应商前缀，比如输入trs，则会生成： 

1. ```css
   1. -webkit-transform: ;  
   2. -moz-transform: ;  
   3. -ms-transform: ;  
   4. -o-transform: ;  
   5. transform: ;  
   ```

   

 

你也可以在任意属性前加上“-”符号，也可以为该属性加上前缀。比如输入-super-foo： 

1. ```css
   1. -webkit-super-foo: ;  
   2. -moz-super-foo: ;  
   3. -ms-super-foo: ;  
   4. -o-super-foo: ;  
   5. super-foo: ;  
   ```

   

   
   
   如果不希望加上所有前缀，可以使用缩写来指定，比如-wm-trf表示只加上-webkit和-moz前缀：

1. ```css
   1. -webkit-transform: ;  
   2. -moz-transform: ;  
   3. transform: ;  
   ```

   


前缀缩写如下： 

- w 表示 -webkit-
- m 表示 -moz-
- s 表示 -ms-
- o 表示 -o-



##  **渐变** 

输入lg(left, #fff 50%, #000)，会生成如下代码：


   1. ```css
      1. background-image: -webkit-gradient(linear, 0 0, 100% 0, color-stop(0.5, #fff), to(#000));  
      2. background-image: -webkit-linear-gradient(left, #fff 50%, #000);  
      3. background-image: -moz-linear-gradient(left, #fff 50%, #000);  
      4. background-image: -o-linear-gradient(left, #fff 50%, #000);  
      5. background-image: linear-gradient(left, #fff 50%, #000);  
      ```

      

## Tips



### 供给带有单位的值

默认地，当展开带有整数值的缩写时，Emmet 输出会带有 `px` 单位：`m10` →`margin: 10px;`。若是展开的缩写带有浮点娄，输出将带有 `em` 单位：`m1.5` →`margin: 1.5em;`。不过也可以经由过程在值的后面放置随便率性的字母来明白指定单位： `m1.5ex` → `margin: 1.5ex;`， `m10foo` → `margin: 10foo;`。

若是明白定义了单位，不须要应用连字符分隔各个值： `m10ex20em` →`margin: 10ex 20em;`， `m10ex-5` → `margin: 10ex -5px;`。



### 值别号

Emmet 有几个常用的别号：

- `p` → `％`
- `e` → `em`
- `x` → `ex`

可以用这些别号来庖代完全的单位：[·](http://caibaojian.com/emmet-doc-3.html)

- `w100p` → `width: 100％`
- `m10p30e5x` → `margin: 10％ 30em 5ex`



### 色彩值

Emmet 付出16进制地色彩值，例如： `c＃3` → `color: ＃333;`。`＃` 符号是值的分隔符，所以不须要应用连字符做分隔。例如 `bd5＃0s` 展开成 `border: 5px ＃000 solid`: 。`5` 被从色彩值的 `＃` 到 `s` （`solid `的别号）从色彩平分隔出来，因为 `s 不是16进制的字符，不须要用 ``-` 分隔符。

可以以 1个、2个、3个或者6个数字的情势书写色彩值：

- `＃1` → `＃111111`
- `＃e0` → `＃e0e0e0`
- `＃fc0` → `＃ffcc00`

当 `css.color.short` 引用 可用时（默认），类似 `＃ffcc00` 如许的值会主动简化成 `＃fc0`。也可以按照 `css.color.case` 引用主动改变大小写。



### 无单位的值

一些 CSS 属性被定义为无单位，例如 `lh2` → `line-height: 2;`，`fw400` → `font-weight: 400;`。

这些值是: `""z-index`、 `line-height`、 `opacity` 和 `font-weight` ，可以哄骗 `css.unitlessProperties` 引用来覆盖它们。



### !important 润饰符

可以在任何 CSS 缩写后面添加 `!` 下标来获得 `!important` 值：

```
p!+m10e!
```

 

将生成

```
padding:  !important;
margin: 10em !important;
```

 

### Vendor 前缀

CSS3 的新特点为 [web](http://caibaojian.com/c/web) 法度员带来了福音：很少的几行代码就能完成几年前近乎不成能实现的任务。但同时这些特点对带来了疾苦：必须为不合的浏览器编写多个雷同的属性。

Emmet 的 CSS 解析器有一个很奇妙的特点，可以明显进步编写 CSS3 的体验。每次在 CSS 属性或缩写前添加连字符，Emmet 就主动为每个属性创建带有 vendor 前缀的副本。例如，`-bdrs` 缩写将展开成：

```
//code from http://caibaojian.com/emmet-doc-3.html
-webkit-border-radius: ;
-moz-border-radius: ;
border-radius: ;
```

 

此外，在支撑 tabstop 的编辑器（例如 Eclipse、 Sublime Text 2、 Espresso 等）中，Emmet 将建树值占位符，法度员可以输入属性值并主动放到全部生成的属性中。



### 它如何工作？

展开前面带有连字符的缩写时，Emmet 删除连字符并在 `snippets.json` 查找残剩的缩写的片段定义。例如 `-bdrs` 缩写将会在 `snippet.json` 中查找 `bdrs` 定义，定义的内容如下：

```
"bdrs": "border-radius:|;"
```

 

也就是说 `bdrs` 将被展开成 `border-radius` 属性。若是定义没有找到，缩写本身将被当成 CSS 属性名。

经过 CSS 解析器策画出的属性将被输出，它将查找特定的在特定的 *vendor 分类*是否呈现。这些分类定义设置中的 `css.{vendor}Properties` 分支。 `{vendor}` 是浏览器的 vendor 前缀，例如 `webkit`、 `moz` 等。

若是扩大属性在这些分类中被找到，它们的 vendor 前缀将用作前导属性。不然，所有的前缀将被应用。

例如，`border-radius` 被定义在 `css.webkitProperties` 和 `css.mozProperties `中，所以这个属性的输出将带有 `webkit` 和 `moz` 前缀。另一种景象，`foo` 属性没有定义在任何 vendor 分类中，所以在展开 `-foo` 缩写时，将输出所有可用的前缀：： `webkit`， `moz`， `ms` and `o`.。它对眼下所实现的那些前沿的 CSS 属性希罕有效。

假设 Google Chrome 昨天方才实现了 `super-foo` ，而你如今就想在项目中应用它。可以应用 `-super-foo` 属性，展开成果如下：

```
-webkit-super-foo: ;
-moz-super-foo: ;
-ms-super-foo: ;
-o-super-foo: ;
super-foo: ;
```

 

### 默认添加前缀属性

在编写 CSS 文件时，也许要查找不带有 vendor 前缀变量的 CSS3 的 “clear” 属性。这会使编写类似 `-trf` （`trf` 是 `transform` 的别号） 如许带有前导连字符的缩写很难堪。

这也是为什么默认景象下 Emmet 会有 `css.autoInsertVendorPrefixes` 选项的原因。这个属性生效，所有定义在 vendor 分类中的 CSS 属性都将被主动供给匹配的 vendor 前缀变量。

这意味着，无需应用连字符来为已知的 CSS 属性获取有效的前缀变量，直接展开 `bdrs` 或 `trf` 缩写就可以获得有效的 vendor 前缀属性。



### 明白地 vendor 前缀

有时可能会想要输出仅带有指定 vendor 前缀属性的 CSS 属性。

假定想要输出仅带有 `webkit` 和 `moz` 前缀的 `transform` 属性，可以编写如下缩写：

```
-wm-trf
```

 

正如所见到的那样，我们经由过程添加一个字符前缀列表对缩写略作批改。在这种景象下，添加的是 `w` （`webkit`） 和 `m` （`moz`） 前缀。Emmet 的单字母前缀如下：

- `w`: `webkit`
- `m`: `moz`
- `s`: `ms`
- `o`: `o`

 

### 渐变

编写 CSS3 特点的另一个难点是渐变。必须为多个 vendor 前缀多次反复长长地渐变定义。同时，要想覆盖所有支撑渐变的浏览器，就必须应用三种不合的注解：旧的 Webkit，当前支撑 （`linear-gradient（top， ...）`） 和 W3C-推荐 （`linear-gradient（to bottom， ...）`）。

凡是，用户偏向于应用第三方 GUI 来生成渐变定义，然则在编辑器中做同样的工作会更快。

Emmet 的 CSS3 渐变生成器可以或许帮你分忧：

正像上方显现的那样，可以输入常规地渐变定义如 `lg（...）` （或 `linear-gradient（...）`） 函数，并算作一个缩写来展开。若是编写渐变定义来充当属性值，Emmet将解析它并应用它的名字作为新的 CSS 属性的引用。



### 备用值

在偏爱设置中，可以使 `css.gradient.fallback` 选项有效，当渐变定义 `background-*` CSS 属性展开时，产生一个备用的 `background-color `CSS 属性。这个备用属性将包含来自渐变定义的第一个色彩。

为个选项默认是封闭的，这是因为它所产生的 `background-color` 值几乎可以必然须要手动进级，以确保这个靠山的内容可读。若是确切不在乎旧浏览器，就可以打开这个选项。

 

### 模糊查找

若是查阅 总览表，就会发明有很多 CSS 片段要记忆。并且它们中的一项目组为了分隔逻辑变得很长。

为了使 CSS 的编写更简单，Emmet 为 CSS 片段实现了模糊查找逻辑：每次输入一个未知的缩写，Emmet 老是试图找到类似的片段定义。

例如，作为 `ov:h` （`overflow: hidden;`） 缩写的调换，可以输入 `ov-h、` `ovh` 或者干脆输入 `oh`。拜见下面的示例。演示了 `bxz:cb`、`ovx:h` 和 `pos:a` 片段的不合示例

模糊查找只针对预定义的片段名，不支撑片段值或 CSS 属性。这个成果更好猜测和把握匹配。记住 可以创建本身的片段或重定义已存在的片段 来调剂模糊查找的体验



# **生成Lorem ipsum文本** 

Lorem ipsum指一篇常用于排版设计领域的拉丁文文章，主要目的是测试文章或文字在不同字型、版型下看起来的效果。通过Emmet，你只需输入lorem 或 lipsum即可生成这些文字。还可以指定文字的个数，比如lorem10，将生成：

 

引用

```css
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Libero delectus.
```

 

# **定制** 

你还可以定制Emmet插件： 



- 添加新缩写或更新现有缩写，可修改[snippets.json](http://docs.emmet.io/customization/snippets/)文件
- 更改Emmet过滤器和操作的行为，可修改[preferences.json](http://docs.emmet.io/customization/preferences/)文件
- 定义如何生成HTML或XML代码，可修改[syntaxProfiles.json](http://docs.emmet.io/customization/syntax-profiles/)文件

 


