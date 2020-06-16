---
title: JavaScript
copyright: true
date: 2019-07-07 20:48:28
tags: 前端
---

# 基础知识



# TIPS

## js实现继承的几种方式(https://www.cnblogs.com/chaixiaozhi/p/8515087.html)

### 1、原型链继承

* 核心：*将父类的实例作为子类的原型*
* 缺点：*父类新增原型方法/原型属性，子类都能访问到，父类一变其他的都变了*



```javascript
function Person(name){
    this name = name;
};

Person prototype.getName = function(){//对原型进行扩展
    return this.name;
};

function Parent(age){
    this.age = age;
};

Parent.prototype = new Person('老明');//关键//通过构造器函数创建出一个新对象，把老对象的东西拿过来

Parent.prototype.getAge = function(){
    return this.age;
};

//Parent.prototype.getName = function(){   
//可以重写父类继承来的方法，会优先调用自己的
//   console.log(222);
//};

var result = new Parent(22);
console.log(result.getName());//老明//调用了从Person原型中继承来的方法(继承到了当前对象的原型中)
	console.log(result.getAge());//22//调用了从Parent原型中扩展来的方法
}
```

### 2、构造继承

* 基本思想
  * 借用构造函数的基本思想就是利用call或者apply把父类中通过this指定的属性和方法复制(借用)到子类创建的实例中
  * 因为this对象是运行时基于函数的执行环境绑定的。也就是说，在全局中，this等于Windows，而当函数被作为某个对象的方法调用时，this等于那个对象
  * call、apply方法可将与一个函数的对象上下文从初始的上下文改变为由 thisObj 指定的新对象
  * 所以，这个借用构造函数就是，new对象的时候(new创建的时候，this指向创建的这个实例)，