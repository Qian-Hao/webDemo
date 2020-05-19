## Dom

### 1.Dom简介

DOM（文档对象模型）是针对HTML和XML文档的一个API。DOM为文档提供了结构化表示，并定义了如何通过脚本来访问文档结构，DOM由节点组成。

**节点：** 节点是构成HTML网页的最基本单元，网页中的每一个部分都可以称为是一个节点，比如html标签、属性文本、注释、整个文档等都是一个节点。

常见节点分为以下四类：

- 文档节点（文档）：整个 HTML 文档。整个 HTML 文档就是一个文档节点。
- 元素节点（标签）：HTML标签。
- 属性节点（属性）：元素的属性。
- 文本节点（文本）：HTML标签中的文本内容（包括标签之间的空格、换行）。

DOM树的结构如下：

<img src="https://upload-images.jianshu.io/upload_images/16749538-64b1ae6106efded7.png?imageMogr2/auto-orient/strip|imageView2/2/w/486/format/webp" alt="img" style="zoom:150%;" />

**DOM的用途：**

- 找元素节点
- 设置元素的属性值
- 设置元素的样式
- 动态创建和删除元素
- 事件的触发响应

### 2.DOM操作

#### 2.1查找元素

##### 1.  getElementById()

通过元素ID查找，返回文档中第一次出现的元素。

```javascript
var div = document.getElementById("box1");
```

##### 2. getElementsByTagName()

通过标签名查找，返回一个NodeList。在HTML文档中，这个方法会返回一个HTMLCollection对象。

```javascript
var arr1 = document.getElementsByTagName("div");
```

取出保存在NodeList中元素的方法如下：

```javascript
arr1[0];
arr1.item(1);
```

##### 3. getElementsByClassName()

通过类名获取元素节点数组。

```
var arr2 = document.getElementsByClassName("hehe");
```

##### 4.querySelector()

querySelector()方法接受一个CSS选择符，返回与该模式匹配的第一个元素，如果没有找到匹配的元素，则返回null。

```JavaScript
//获取body元素
var body = document.querySelector("body");

//获取ID为"myDiv"的元素
var myDiv = document.querySelector("#myDiv");

//获取类为"box1"的第一个元素
var myDiv = document.querySelector(".box1")
```

##### 5.querySelectorAll()

querySelectorAll()与querySelector()类似，只是返回的是一个NodeList实例，包含所有匹配的元素。

```javascript
//获取所有<li>元素
var body = document.querySelectorAll("li");

//获取所有类为"box1"的元素
var myDiv = document.querySelectorAll(".box1")
```

