---
title: 读书笔记：JavaScript高级程序设计02（第3版）
date: 2019-11-09 15:45:40
tags: 读书笔记
categories: 前端理论
top: 665
---

（注1：现在是2020年10月27日，我下载了《JavaScript高级程序设计》第四版的电子书，后面第8章以后的我基本没看的内容以后就看第四版了吧。）

（注2：不然我再单独开辟一个博文写《JavaScript高级程序设计》第四版的笔记？？等到时候再看看吧。大体看了一下，感觉确实新增加了挺多东西的。）

（注3：我还是新增一篇博文写吧，那这一篇博文算是废弃了吧，第8章以后看最新版的《JavaScript高级程序设计》了吧）

# 第9章：客户端检测（先略，没看）

浏览器提供商虽然在实现公共接口方面投入了很多精力，但结果仍然是每一种浏览器都有各自的长处，也都有各自的缺点。即使是那些跨平台的浏览器，虽然从技术上看版本相同，也照样存在不一致性问题。面对普遍存在的不一致性问题，开发人员要么采取迁就各方的“最小公分母”策略，要么（也是更常见的）就得利用各种客户端检测方法，来突破或者规避种种局限性。

迄今为止，客户端检测仍然是Web开发领域中一个饱受争议的话题。一谈到这个话题，人们总会不约而同地提到浏览器应该支持一组最常用的公共功能。在理想状态下，确实应该如此。但是，在现实当中，浏览器之间的差异以及不同浏览器的“怪癖”（quirk），多得简直不胜枚举。因此，客户端检测除了是一种补救措施之外，更是一种行之有效的开发策略。

检测Web客户端的手段很多，而且各有利弊。但最重要的还是要知道，不到万不得已，就不要使用客户端检测。只要能找到更通用的方法，就应该优先采用更通用的方法。一言以蔽之，先设计最通用的方案，然后再使用特定于浏览器的技术增强该方案。

## 能力检测

最常用也最为人们广泛接受的客户端检测形式是能力检测（又称特性检测）。能力检测的目标不是识别特定的浏览器，而是识别浏览器的能力。采用这种方式不必顾及特定的浏览器如何如何，只要确定浏览器支持特定的能力，就可以给出解决方案。能力检测的基本模式如下：

# 第10章：DOM(看的不细，很多不懂)

**DOM(文档对象模型)是针对HTML和XML文档的一个API(应用程序编程接口)。**DOM描述了一个**层次化的节点树**，允许开发人员添加、移除或修改页面的某一部分。DOM脱胎于Netscape及微软公司创始的DHTML(动态HTML),但现在它已经成为表现和操作页面标记的真正的**跨平台、语言中立**的方式。

1998年10月DOM1级规范成为W3C的推荐标准，为基本的**文档结构及查询**提供了**接口**。本章主要讨论与浏览器中的HTML页面相关的**DOM1级**的特性和应用，以及JavaScript对DOM1级的实现。
IE、Firefox、Safari、Chrome和Opera都非常完善地实现了DOM。

> 注意，IE中的所有DOM对象都是以COM对象的形式实现的。这意味着IE中的DOM对象与原生JavaScript对象的行为或活动特点并不一致。本章将较多地谈及这些差异。

[DOM之元素与节点的区别](<https://blog.csdn.net/caseywei/article/details/81368531>)

> 元素(element)一定是节点，但节点(Node)不一定是元素。
>
> node(节点)是相对Tree这种数据结构而言的。Tree就是由Node(节点)组成。
>
> element则是XML里面的概念，< xxx>就是元素，是XML中数据的组成部分之一。
>
> 一个元素是由开始标签、结束标签以及标签之间的数据构成的

[认识DOM的三大节点：元素节点，文本节点，属性节点以及nodeName,nodeType,nodeValue的区别](<https://blog.csdn.net/u010792238/article/details/23533801>)

[DOM里面的Node对象和Element对象的区别](https://segmentfault.com/a/1190000016224547)

## 节点层次(看完，挺重要)

DOM可以**将任何HTML或XML文档描绘成一个由多层节点构成的结构**。**节点**分为几种不同的类型，**每种类型分别表示文档中不同的信息及（或）标记**。**每个节点都拥有各自的特点、数据和方法**，另外也与其他节点存在某种关系。**节点之间的关系构成了层次**，而**所有页面标记则表现为一个以特定节点为根节点的树形结构**。

以下面的HTML为例：

~~~javascript
<html>
  <head>
    <title>Sample Page</title>
  </head>
  <body>
    <p>Hello World!</p>
  </body>
</html>
~~~

可以将这个简单的**HTML文档**表示为一个层次结构，如图10-1所示。

**文档节点**是每个文档的**根节点**。

在这个例子中，**文档节点只有一个子节点，即\<html>元素，我们称之为文档元素。**文档元素是文档的**最外层元素**，文档中的其他所有元素都包含在文档元素中。**每个文档只能有一个文档元素**。**在HTML页面中，文档元素始终都是\<html>元素**。**在XML中，没有预定义的元素，因此任何元素都可能成为文档元素。**（XML不太熟）

> 在DOM中，每个部分都是节点（Node）
>
> * 文档本身是文档节点
> * 所有 HTML 元素是元素节点
> * 所有 HTML 属性是属性节点
> * HTML 元素内的文本是文本节点 （包括回车符也是属于文本节点）
> * 注释是注释节点
>
> Element 对象可以拥有类型为元素节点、文本节点、注释节点的子节点。
>
>  NodeList 对象表示节点列表，比如 HTML 元素的子节点集合。
>
> 元素也可以拥有属性。属性是属性节点。
>
> 总结1：元素是元素节点，是节点中的一种，但元素节点中可以包含很多的节点。
>
> 总结2：元素一定是节点，但节点不一定是元素。

每一段**标记**都可以通过树中的一个节点来表示：**HTML元素通过元素节点表示，特性（attribute）**
**通过特性节点表示，文档类型通过文档类型节点表示，而注释则通过注释节点表示。**总共有**12种**节点**类型**，这些类型都继承自一个基类型。

![](读书笔记：JavaScript高级程序设计02(第3版)/98.png)

### Node类型（看完，不太熟）

DOM1级定义了一个Node接口，**该接口将由DOM中的所有节点类型实现**。这个Node接口在JavaScript中是作为Node类型实现的；**除了IE之外**，在其他所有浏览器中都可以访问到这个类型。
**JavaScript中的所有节点类型都继承自Node类型，因此所有节点类型都共享着相同的基本属性和方法。**

每个节点都有一个**nodeType属性**，用于**表明节点的类型**。**节点类型**由在Node类型中定义的下列**12个数值常量**来表示，任何节点类型必居其一：

| 常量值 | 节点类型                         |
| ------ | -------------------------------- |
| 1      | Node.ELEMENT_NODE                |
| 2      | Node.ATTRIBUTE_NODE              |
| 3      | Node.TEXT_NODE                   |
| 4      | Node.CDATA_SECTION_NODE          |
| 5      | Node.ENTITY_REFERENCE_NODE       |
| 6      | Node.ENTITY_NODE                 |
| 7      | Node.PROCESSING_INSTRUCTION_NODE |
| 8      | Node.COMMENT_NODE                |
| 9      | Node.DOCUMENT_NODE               |
| 10     | Node.DOCUMENT_TYPE_NODE          |
| 11     | Node.DOCUMENT_FRAGMENT_NODE      |
| 12     | Node.NOTATION_NODE               |


> 这12个节点类型完全不知道是啥意思
>
> 现在懂一点了-2020.04.15

这12种类型中，有些节点可以包含子节点，有些没有子节点，详细如下：

| 常量值 | 节点类型              | 描述                                             | 子节点                                                       |
| :----: | --------------------- | ------------------------------------------------ | ------------------------------------------------------------ |
|   1    | Element               | 代表元素                                         | Element, Text, Comment, ProcessingInstruction, CDATASection, EntityReference |
|   2    | Attr                  | 代表属性                                         | Text, EntityReference                                        |
|   3    | Text                  | 代表元素或属性中的文本内容。                     | None                                                         |
|   4    | CDATASection          | 代表文档中的 CDATA 部 （不会由解析器解析的文本） | None                                                         |
|   5    | EntityReference       | 代表实体引用。                                   | Element, ProcessingInstruction, Comment, Text, CDATASection, EntityReference |
|   6    | Entity                | 代表实体。                                       | Element, ProcessingInstruction, Comment, Text, CDATASection, EntityReference |
|   7    | ProcessingInstruction | 代表处理指令。                                   | None                                                         |
|   8    | Comment               | 代表注释。                                       | None                                                         |
|   9    | Document              | 代表整个文档（DOM 树的根节点）。                 | Element, ProcessingInstruction, Comment, DocumentType        |
|   10   | DocumentType          | 向为文档定义的实体提供接口                       | None                                                         |
|   11   | DocumentFragment      | 代表轻量级的 Document 对象 （文档的某个部分）    | Element, ProcessingInstruction, Comment, Text, CDATASection, EntityReference |
|   12   | Notation              | 代表 DTD 中声明的符号。                          | None                                                         |

[JavaScript HTML DOM节点类型之Node类型介绍](<https://itbilu.com/javascript/js/Ny3B0ddWg.html>)

通过比较上面这些**常量**，可以很容易地确定节点的类型，例如：

~~~javascript
if(someNode.nodeType == Node.ELEMENT_NODE){		//在IE中无效
    alert（"Node is an element."）;
}
~~~

这个例子比较了someNode.nodeType与Node.ELEMENT_NODE常量。**如果二者相等，则意味着someNode确实是一个元素。**然而，由于IE没有公开Node类型的构造函数，因此上面的代码在E中会导致错误。为了确保跨浏览器兼容，**最好还是将nodeType属性与数字值进行比较**，如下所示：

~~~javascript
if(someNode.nodeType == 1){		//适用于所有的浏览器
    alert（"Node is an element."）;
}
~~~

并不是所有节点类型都受到Web浏览器的支持。开发人员最常用的就是**元素和文本节点**。本章后面将详细讨论每个节点类型的受支持情况及使用方法。

1. **nodeName和nodeValue属性**

   要了解节点的具体信息，可以使用 nodeName和nodeValue这两个属性。这两个属性的值完全取决于节点的类型。在使用这两个值以前，最好是像下面这样先检测一下节点的类型。

   ~~~javascript
   if(someNode.nodeType == 1){		
      value = someNode.nodeName;		//nodename的值是元素的标签名
   }
   ~~~
   在这个例子中，首先检查节点类型，**看它是不是一个元素**。如果是，则取得并保存nodeName的值。**对于元素节点，nodeName中保存的始终都是元素的标签名，而nodeValue的值则始终为null。**

   > `nodeName`属性用于返回指定节点的节点名，节点名会以大写形式返回。
   >
   > `nodeValue`属性用于返回或设置给定节点的节点值

   12种节点类型nodeValue和nodeName的返回值如下：

   | 常量值 | 节点类型              | nodeName 返回值 | nodeValue 返回值 |
   | ------ | --------------------- | --------------- | ---------------- |
   | 1      | Element               | 元素名          | null             |
   | 2      | Attr                  | 属性名称        | 属性值           |
   | 3      | Text                  | #text           | 节点的内容       |
   | 4      | CDATASection          | #cdata-section  | 节点的内容       |
   | 5      | EntityReference       | 实体引用名称    | null             |
   | 6      | Entity                | 实体名称        | null             |
   | 7      | ProcessingInstruction | target          | 节点的内容       |
   | 8      | Comment               | #comment        | 注释文本         |
   | 9      | Document              | #document       | null             |
   | 10     | DocumentType          | 文档类型名称    | null             |
   | 11     | DocumentFragment      | #document 片段  | null             |
   | 12     | Notation              | 符号名称        | null             |

2. **节点关系**（看完）

   文档中所有的节点之间都存在这样或那样的关系。**节点间的各种关系可以用传统的家族关系来描述，相当于把文档树比喻成家谱。**在HTML中，可以将\<body>元素看成是\<html>元素的**子元素**；相应地，也就可以将\<html>元素看成是\<body>元素的**父元素**。而< head>元素，则可以看成是\<body>元素的**同胞元素**，因为它们都是同一个父元素\<html>的直接子元素。

   **每个节点都有一个childNodes属性，其中保存着一个NodeList对象**。NodeList是一种类数组对象，用于保存一组有序的节点，可以通过位置来访问这些节点。请注意，虽然可以通过**方括号语法**来访问NodeList的值，而且**这个对象也有length属性，但它并不是Array的实例**。NodeList对象的独特之处在于，它实际上是基于DOM结构动态执行查询的结果，因此DOM结构的变化能够自动反映在NodeList对象中。我们常说，**NodeList是有生命、有呼吸的对象，而不是在我们第一次访问它们的某个瞬间拍摄下来的一张快照。**

   下面的例子展示了如何访问保存在NodeList中的节点——**可以通过方括号，也可以使用item（）方法。**

   ~~~javascript
   var firstChild = someNode.childNodes[0]; 
   var secondchild = someNode.childNodes.item(1); 
   var count = someNode.childNodes.1ength;
   ~~~
   **无论使用方括号还是使用item（）方法都没有问题，但使用方括号语法看起来与访问数组相似，因此颇受一些开发人员的青睐。**另外，要注意**length属性表示的是访问NodeList的那一刻，其中包含的节点数量。**我们在本书前面介绍过，**对arguments对象使用Array.prototype.slice（）方法可以将其转换为数组。而采用同样的方法，也可以将NodeList对象转换为数组。**来看下面的例子：

   ~~~javascript
   //在IE8及之前版本中无效
   var arrayOfNodes=Array.prototype.slice.ca11（someNode.childNodes，0）;
   ~~~

   除IE8及更早版本之外，这行代码能在任何浏览器中运行。由于IE8及更早版本将NodeList实现为一个COM对象，而我们不能像使用JScript对象那样使用这种对象，因此上面的代码会导致错误。要想在IE中将NodeList转换为数组，必须**手动枚举所有成员**。下列代码在所有浏览器中都可以运行：

   ~~~javascript
   function convertToArray（nodes）{
   		var array = null;
       try{
   			array = Array.prototype.slice.call（nodes，0）; 	//针对非E浏览器）
       }catch（ex）{
   		array = new Array（）;
           for（var i = 0，len = nodes.length;i< len；i++）{
   						array.push（nodes[i]）;
           }
        }
       return array;
   }
   ~~~

   这个convertToArray（）函数首先尝试了创建数组的最简单方式。如果导致了错误（说明是在IE8及更早版本中），则**通过try-catch块来捕获错误，然后手动创建数组。这是另一种检测怪癖的形式**。

   **每个节点都有一个parentNode属性，该属性指向文档树中的父节点。包含在childNodes列表中的所有节点都具有相同的父节点，因此它们的 parentNode属性都指向同一个节点。**此外，包含在childNodes列表中的每个节点相互之间都是同胞节点。通过使用列表中每个节点的**previousSibling和nextSibling属性，可以访问同一列表中的其他节点**。列表中**第一个节点的previousSibling属性值为null，而列表中最后一个节点的nextSibling属性的值同样也为null**，如下面的例子所示：

   ~~~javascript
   if(someNode.nextSibling === null){
   		alert("Last node in the parent's childNodes list.");
   ) else if (someNode.previousSibling === null){
   	alert("First node in the parent's childNodes list.");
   }
   ~~~

   **当然，如果列表中只有一个节点，那么该节点的nextSibling和previousSibling都为null。**

   父节点与其第一个和最后一个子节点之间也存在特殊关系。**父节点的firstChild和lastChild属性分别指向其 childNodes列表中的第一个和最后一个节点。**

   > 不太懂什么意思

   其中，**someNode.firstChild的值始终等于someNode.childNodes[0]，而someNode.lastChild的值始终等于someNode.**
   **childNodes[someNode.childNodes.length-1]**。在只有一个子节点的情况下，firstChild和lastChi1d 指向同一个节点。如果没有子节点，那么firstchild和lastchild的值均为null。**明确这些关系能够对我们查找和访问文档结构中的节点提供极大的便利。**图10-2形象地展示了上述关系。

   ![](读书笔记：JavaScript高级程序设计02(第3版)/103.png)

   在反映这些关系的所有属性当中，childNodes属性与其他属性相比更方便一些，因为只须使用简单的关系指针，就可以通过它访问文档树中的任何节点。另外，**haschildNodes（）**也是一个非常有用的方法，这个方法在节点包含一或多个子节点的情况下返回true；应该说，这是比查询 childNodes列表的length属性更简单的方法。

   **所有节点都有的最后一个属性是ownerDocument**，该属性指向表示整个文档的文档节点。这种关系表示的是**任何节点都属于它所在的文档，任何节点都不能同时存在于两个或更多个文档中。通过这个属性，我们可以不必在节点层次中通过层层回溯到达顶端，而是可以直接访问文档节点。**

   > 虽然所有节点类型都继承自Node，但并不是每种节点都有子节点。本章后面将会讨论不同节点类型之间的差异。

3. **操作节点**(没看)

   因为关系指针都是只读的，所以DOM提供了一些操作节点的方法。其中，最常用的方法是appendchild（），用于向childNodes列表的末尾添加一个节点。添加节点后，childNodes的新增节点、父节点及以前的最后一个子节点的关系指针都会相应地得到更新。更新完成后，appendchild（）返回新增的节点。来看下面的例子：

   ~~~javascript
   var returnedNode = someNode. appendchild(newNode); 
   alert(returnedNode == newNode);//true
   alert(someNode. lastChild == newNode);//true
   ~~~

   如果传入到appendchild（）中的节点已经是文档的一部分了，那结果就是将该节点从原来的位置转移到新位置。即使可以将DOM树看成是由一系列指针连接起来的，但任何DOM节点也不能同时出现在文档中的多个位置上。因此，如果在调用appendchi1d（）时传人了父节点的第一个子节点，那么该节点就会成为父节点的最后一个子节点，如下面的例子所示。

   ~~~javascript
   //someNode有多个子节点
   var returnedNode = someNode.appendChild（someNode.firstChild）;
   alert（returnedNode == someNode.firstChild）; //false 
   alert（returnedNode == someNode.lastChild）;//true
   ~~~

   如果需要把节点放在childNodes列表中某个特定的位置上，而不是放在末尾，那么可以使用insertBefore（）方法。这个方法接受两个参数：要插入的节点和作为参照的节点。插入节点后，被插入的节点会变成参照节点的前一个同胞节点（previoussibling），同时被方法返回。如果参照节点是nu11，则insertBefore（）与appendchild（）执行相同的操作，如下面的例子所示。

   ~~~javascript
   //插入后成为最后一个子节点
   returnedNode=someNode.insertBefore（newNode，null）;
   alert（newNode == someNode.lastChild）；//true
   
   //插入后成为第一个子节点
   var returnedNode a someNode.insertBefore（newNode，someNode.firstChild）；alert（returnedNode == newNode）;//true 
   alert（newNode == someNode.firstChild）;//true
   
   //插入到最后一个子节点前面
   returnedNode = someNode.insertBefore（newNode，someNode.lastChild）;
   alert（newNode == someNode.childNodes[someNode.childNodes.length-2]）；//true
   ~~~

   前面介绍的appendchi1d（）和insertBefore（）方法都只插入节点，不会移除节点。而下面要介绍的replaceChi1d（）方法接受的两个参数是：要插入的节点和要替换的节点。要替换的节点将由这个方法返回并从文档树中被移除，同时由要插入的节点占据其位置。来看下面的例子。

   ~~~javascript
   //替换第一个子节点
   var returnedNode=someNode.replacechi1d（newNode，someNode.firstchild）;
   
   //替换最后一个子节点
   returnedNode =someNode.replaceChild（newNode，someNode.lastChild）;
   ~~~

   在使用replacechild（）插入一个节点时，该节点的所有关系指针都会从被它替换的节点复制过来。尽管从技术上讲，被替换的节点仍然还在文档中，但它在文档中已经没有了自己的位置。

   如果只想移除而非替换节点，可以使用removeChild（）方法。这个方法接受一个参数，即要移除的节点。被移除的节点将成为方法的返回值，如下面的例子所示。

   ~~~javascript
   //移除第一个子节点
   var formerFirstchild=someNode.removeChi1d（someNode.firstChild）;
   
   //移除最后一个子节点
   var formerLastChild=someNode.removeChi1d（someNode.lastChild）;
   ~~~

   与使用replaceChi1d（）方法一样，通过removeChild（）移除的节点仍然为文档所有，只不过在文档中已经没有了自己的位置。

   前面介绍的四个方法操作的都是某个节点的子节点，也就是说，要使用这几个方法必须先取得父节点（使用parentNode属性）。另外，并不是所有类型的节点都有子节点，如果在不支持子节点的节点上调用了这些方法，将会导致错误发生。

4. **其他方法**

   有两个方法是所有类型的节点都有的。第一个就是cloneNode（），用于创建调用这个方法的节点的一个完全相同的副本。cloneNode（）方法接受一个布尔值参数，表示是否执行深复制。在参数为true的情况下，执行深复制，也就是复制节点及其整个子节点树；在参数为false的情况下，执行浅复制，即只复制节点本身。复制后返回的节点副本属于文档所有，但并没有为它指定父节点。因此，这个节点副本就成为了一个“孤儿”，除非通过appendchi1d（）、insertBefore（）或replacechild（）将它添加到文档中。例如，假设有下面的HTML代码。

   ~~~javascript
   <ul>
     <li>item 1</li>
     <li>item 1</li>
     <li>item 1</li>
   </ul>
   ~~~

   如果我们已经将< u1>元素的引用保存在了变量myList中，那么通常下列代码就可以看出使用cloneNode（）方法的两种模式。

   ~~~javascript
   var deepList = myList.cloneNode（true）；alert（deepList.childNodes.1ength）；//3（IE<9）或7（其他浏览器）
   
   var shallowList = myList.cloneNode（false）；alert（shallowList.childNodes.length）；//0
   ~~~

   在这个例子中，deepList中保存着一个对myList执行深复制得到的副本。因此，deepList中包含3个列表项，每个列表项中都包含文本。而变量shallowList中保存着对myList执行浅复制得到的副本，因此它不包含子节点。deepList.childNodes.1ength中的差异主要是因为IE8及更早版本与其他浏览器处理空白字符的方式不一样。IE9之前的版本不会为空白符创建节点。

   > cloneNode（）方法不会复制添加到DOM节点中的JavaScript属性，例如事件处理程序等。这个方法只复制特性、（在明确指定的情况下也复制）子节点，其他一切都不会复制。IE在此存在一个bug，即它会复制事件处理程序，所以我们建议在复制之前最好先移除事件处理程序。

   我们要介绍的最后一个方法是normalize（），这个方法唯一的作用就是处理文档树中的文本节点。
   由于解析器的实现或DOM操作等原因，可能会出现文本节点不包含文本，或者接连出现两个文本节点的情况。当在某个节点上调用这个方法时，就会在该节点的后代节点中查找上述两种情况。如果找到了空文本节点，则删除它；如果找到相邻的文本节点，则将它们合并为一个文本节点。本章后面还将进一步讨论这个方法。

### Document类型

**JavaScript通过Document类型表示文档。在浏览器中，document对象是HTMLDocument（继承自Document类型）的一个实例，表示整个HTML页面。而且，document对象是window对象的一个属性，因此可以将其作为全局对象来访问。**Document节点具有下列特征：

~~~javascript
nodeType的值为9；

nodeName的值为“#document";

nodeValue的值为nu11;

parentNode的值为nul1;

owmerDocument的值为nul1;

其子节点可能是一个DocumentType（最多一个）、Element（最多一个）、processingInstruction或Comment。
~~~

Document类型可以表示HTML页面或者其他基于XML的文档。不过，最常见的应用还是作为HTML.Document实例的document对象。通过这个文档对象，不仅可以取得与页面有关的信息，而且还能操作页面的外观及其底层结构。

> 在Firefox、Safari、Chrome和Opera中，可以通过脚本访问Document类型的构造函数和原型。但在所有浏览器中都可以访问HTMLDocument类型的构造函教和原型，包括IE8及后续版本。

1. 文档的子节点

   虽然DOM标准规定Document节点的子节点可以是DocumentType、Element、ProcessingInstructior或Comment，但还有两个内置的访问其子节点的快捷方式。第一个就是documentElement属性，该属性始终指向HTML页面中的< html>元素。另一个就是通过childNodes列表访问文档元素，但通过documentElement属性则能更快捷、更直接地访问该元素。以下面这个简单的页面为例。

   ~~~javascript
   <html>
       <body>
       
       </body>
   </html>
   ~~~

   这个页面在经过浏览器解析后，其文档中只包含一个子节点，即< html>元素。可以通过documentElement或childNodes列表来访问这个元素，如下所示。

   ~~~javascript
   var html=document.documentElement；		//取得对<html>的引用alert（html===document.childNodes[0]）；	 //true alert（html===document.firstchild）；    //true
   ~~~

   这个例子说明，documentElement、firstchild和childNodes[0]的值相同，都指向< html>
   元素。

   作为HIMLDocument的实例，document对象还有一个body 属性，直接指向< body>元素。因为开发人员经常要使用这个元素，所以document.body在JavaScript代码中出现的频率非常高，其用法如下。

   ~~~javascript
   var body = document.body;		//取得对<body>的引用
   ~~~

   所有浏览器都支持document.documentE1ement和document.body属性。

   Document另一个可能的子节点是DocumentType。通常将<!DOCTYPE>标签看成一个与文档其他部分不同的实体，可以通过doctype属性（在浏览器中是document.doctype）来访问它的信息。

   ~~~
   var doctype=document.doctype；//取得对<!DOCTYPE>的引用
   ~~~

   浏览器对document.doctype的支持差别很大，可以给出如下总结。

   > IE8及之前版本：如果存在文档类型声明，会将其错误地解释为一个注释并把它当作Comment节点；而document.doctype的值始终为nul1。
   >
   > IE9+及Firefox：如果存在文档类型声明，则将其作为文档的第一个子节点；document.doctype是一个DocumentType节点，也可以通过document.firstchi1d或document.childNodes[0]
   > 访问同一个节点。
   >
   > Safari、Chrome 和Opera：如果存在文档类型声明，则将其解析，但不作为文档的子节点。docu-
   > ment.doctype是一个DocumentType节点，但该节点不会出现在document.childNodes中。

   由于浏览器对document.doctype的支持不一致，因此这个属性的用处很有限。

   从技术上说，出现在< html>元素外部的注释应该算是文档的子节点。然而，不同的浏览器在是否解析这些注释以及能否正确处理它们等方面，也存在很大差异。以下面简单的HTML页面为例。

   ~~~javascript
   <！--第一条注释-->
   <htm1>
      <body>
       
      </body>
   </html>
   <！--第二条注释-->
   ~~~

   看起来这个页面应该有3个子节点：注释、< html>元素、注释。从逻辑上讲，我们会认为document.childNodes中应该包含与这3个节点对应的3项。但是，现实中的浏览器在处理位于
   < htm1>外部的注释方面存在如下差异。

   > IE8及之前版本、Safari3.1及更高版本、Opera和Chrome只为第一条注释创建节点，不为第二条注释创建节点。结果，第一条注释就会成为document.childNodes中的第一个子节点。
   >
   > IE9及更高版本会将第一条注释创建为document.childNodes中的一个注释节点，也会将第二条注释创建为document.childNodes中的注释子节点。
   >
   > Firefox以及Safari3.1之前的版本会完全忽略这两条注释。

   同样，浏览器间的这种不一致性也导致了位于< html>元素外部的注释没有什么用处。

   多数情况下，我们都用不着在document 对象上调用appendchi1d（）、removechild（）和replacechild（）方法，因为文档类型（如果存在的话）是只读的，而且它只能有一个元素子节点（该节点通常早就已经存在了）。

2. 文档信息

   作为HTMLDocument的一个实例，document对象还有一些标准的Document对象所没有的属性。这些属性提供了document对象所表现的网页的一些信息。其中第一个属性就是tit1e，包含着< title>元素中的文本——显示在浏览器窗口的标题栏或标签页上。通过这个属性可以取得当前页面的标题，也可以修改当前页面的标题并反映在浏览器的标题栏中。修改tit1e属性的值不会改变< title>元素。来看下面的例子。

   ~~~javascript
   //取得文档标题
   var originalTitle=document.title；
   
   //设置文档标题
   document.title="New page title"；
   ~~~

   接下来要介绍的3个属性都与对网页的请求有关，它们是URL、domain和referrer。URL属性中包含页面完整的URL（即地址栏中显示的URL），domain属性中只包含页面的域名，而 referrer属性中则保存着链接到当前页面的那个页面的URL。在没有来源页面的情况下，referrer属性中可能会包含空字符串。所有这些信息都存在于请求的HTTP头部，只不过是通过这些属性让我们能够在JavaScrip中访问它们而已，如下面的例子所示。

   ~~~javascript
   //取得完整的URL 
   var url=document.URL；
   
   //取得域名
   var domain=document.domain；
   
   //取得来源页面的URL 
   var referrer =document.referrer；
   ~~~

   URL与domain属性是相互关联的。例如，如果document.URL等于http:/www.wrox.com/WileyCDA/，那么document.domain就等于www.wrox.com。

   在这3个属性中，只有domain是可以设置的。但由于安全方面的限制，也并非可以给domain设置任何值。如果URL中包含一个子域名，例如p2p.wrox.com，那么就只能将domain 设置为“wrox.com·
   （URL中包含“www”，如www.wrox.com时，也是如此）。不能将这个属性设置为URL中不包含的域，如下面的例子所示。

   ~~~javascript
   //假设页面来自p2p.wrox.com域
   document.domain="wrox.com"；//成功
   document.domain="nczonline.net"；//出错！
   ~~~

   所有浏览器中都存在这个限制，但IE8是实现这一限制的最早的E版本。

3. 查找元素

   说到最常见的DOM应用，恐怕就要数取得特定的某个或某组元素的引用，然后再执行一些操作了。
   取得元素的操作可以使用document对象的几个方法来完成。其中，Document类型为此提供了两个方法：getElementById（）和getElementsByTagName（）。

   第一个方法，getElementById（），接收一个参数：要取得的元素的ID。如果找到相应的元素则返回该元素，如果不存在带有相应ID的元素，则返回nu11。注意，这里的ID必须与页面中元素的id特性（attribute）严格匹配，包括大小写。以下面的元素为例。

   ~~~javascript
   <div id='myDiv'>Some text</div>
   ~~~
   可是使用下面的代码取得这个元素：

   ~~~javascript
   var div = document.getElementById("myDiv");
   ~~~

   但是，下面的代码在除IE7及更早版本之外的所有浏览器中都将返回null。

   ~~~javascript
   var div = document.getElementById("mydiv");		//无效的ID(在IE7及更早版本中可以)
   ~~~

   IE8及较低版本不区分ID的大小写，因此“myDiv“和“mydiv“会被当作相同的元素ID。

   如果页面中多个元素的ID值相同，getElementById（）只返回文档中第一次出现的元素。IE7及较低版本还为此方法添加了一个有意思的“怪癖”：name特性与给定ID匹配的表单元素（< input>、< textarea>、< button>及< select>）也会被该方法返回。如果有哪个表单元素的name特性等于指定的ID，而且该元素在文档中位于带有给定ID的元素前面，那么正就会返回那个表单元素。来看下面的例子。

   ~~~javascript
   <input type="text" name="myElement" value="Text field">
   <div id="myElement">A div</div>
   ~~~

   基于这段HTML代码，在IE7中调用document.getElementById（"myElement"），结果会返回< input>元素；而在其他所有浏览器中，都会返回对< div>元素的引用。为了避免IE中存在的这个问题，最好的办法是不让表单字段的name 特性与其他元素的ID相同。

   另一个常用于取得元素引用的方法是getElementsByTagName（）。这个方法接受一个参数，即要取得元素的标签名，而返回的是包含零或多个元素的NodeList。在HTML文档中，这个方法会返回一个HTMLCo1lection对象，作为一个“动态”集合，该对象与Nodetist非常类似。例如，下列代码会取得页面中所有的< img>元素，并返回一个HTMLCollection。

   ~~~javascript
   var images = document.getElementByTagName('img')
   ~~~

   这行代码会将一个HTMLCo1lection对象保存在images变量中。与NodeList对象类似，可以使用方括号语法或item（）方法来访问HTML.Co1lection对象中的项。而这个对象中元素的数量则可以通过其1ength属性取得，如下面的例子所示。

   ~~~javascript
   alert{images.1ength）；//输出图像的数量
   alert（images[0].src）；//输出第一个图像元素的srC特性
   alert（images.item（0）.src）；//输出第一个图像元素的src特性
   ~~~

   HTMLCollection对象还有一个方法，叫做namedItem（），使用这个方法可以通过元素的 name特性取得集合中的项。例如，假设上面提到的页面中包含如下< img>元素：

   ~~~javascript
   <img src = "myimage.gif"name="myImage">
   ~~~

   那么就可以通过如下方式从images变量中取得这个< img>元素：

   ~~~javascript
   var myImage=images.namedItem("my Image");
   ~~~

   在提供按索引访问项的基础上，HTMLCo1lection还支持按名称访问项，这就为我们取得实际想要的元素提供了便利。而且，对命名的项也可以使用方括号语法来访问，如下所示：

   ~~~javascript
   var myImage = imagest"myImage"];
   ~~~

   对HTMLCollection而言，我们可以向方括号中传人数值或字符串形式的索引值。在后台，对数值索引就会调用item（），而对字符串索引就会调用namedrtem（）。

   要想取得文档中的所有元素，可以向 getslementsBy TagName（）中传人”*”。在JavaScript及CSS中，星号（ *）通常表示“全部”。下面看一个例子。

   ~~~javascript
   var allElements = document. getElementsBy TagName("*");
   ~~~

   仅此一行代码返回的HTMLCo11ection中，就包含了整个页面中的所有元素——按照它们出现的先后顺序。换句话说，第一项是< htm1>元素，第二项是< head>元素，以此类推。由于IE将注释（Comment）实现为元素（Element），因此在IE中调用getE1ementsBy TagName（"*"）将会返回所有注释节点。

   > 虽然标准规定标签名需要区分大小写，但为了最大限度地与既有HTML页面兼容，传给getElementsByTagName（）的标签名是不需要区分大小写的。但对于XML页面而言（包括XHTML），getElementsByTagName（）方法就会区分大小写。

   第三个方法，也是只有HMLDocument类型才有的方法，是getE1ementsByName（）。顾名思义，这个方法会返回带有给定name 特性的所有元素。最常使用getElementsByName（）方法的情况是取得单选按钮；为了确保发送给浏览器的值正确无误，所有单选按钮必须具有相同的name特性，如下面的例子所示。

   ![](读书笔记：JavaScript高级程序设计(第3版)/109.png)

   如这个例子所示，其中所有单选按钮的name特性值都是“color”，但它们的ID可以不同。ID的作用在于将<1abe1>元素应用到每个单选按钮，而name 特性则用以确保三个值中只有一个被发送给浏览器。这样，我们就可以使用如下代码取得所有单选按钮：

   ~~~javascript
   var radios = document. getElementsByName("color");
   ~~~

   与getElementsBy TagName（）类似，getElementsByName（）方法也会返回一个HmMLCollectioin。
   但是，对于这里的单选按钮来说，namedrtem（）方法则只会取得第一项（因为每一项的name特性都相同）。

4. 特殊集合

   除了属性和方法，document对象还有一些特殊的集合。这些集合都是HTMLCo11ection对象，为访问文档常用的部分提供了快捷方式，包括：

   ~~~javascript
   document.anchors，包含文档中所有带 name 特性的<a>元素；
   document.applets，包含文档中所有的<applet>元素，因为不再推荐使用<applet>元素，所以这个集合已经不建议使用了；
   document.forms，包含文档中所有的<forms元素，与document.getElementsByTagName（“form*）得到的结果相同；
   document.images，包含文档中所有的<img>元素，与document.getElementsByTagName
   （“img")得到的结果相同；
   document.1inks，包含文档中所有带href 特性的<a>元素。
   ~~~

   这个特殊集合始终都可以通过HTMLDocument对象访问到，而且，与HTMLCollection对象类似，集合中的项也会随着当前文档内容的更新而更新。

5. 一致性检测

   由于DOM分为多个级别，也包含多个部分，因此检测浏览器实现了DOM的哪些部分就十分必要了。document.implementation属性就是为此提供相应信息和功能的对象，与浏览器对DOM的实现直接对应。DOMI级只为document.implementation规定了一个方法，即hasFeature（）。这个方法接受两个参数：要检测的DOM功能的名称及版本号。如果浏览器支持给定名称和版本的功能，则该方法返回true，如下面的例子所示：

   ~~~javascript
   var hasxmlDom=document.implementation.hasFeature（"XML"，“1.0"）;
   ~~~
   下表列出了可以检测的不同的值及版本号。

   ![](读书笔记：JavaScript高级程序设计(第3版)/113.png)

   尽管使用hasFeature（）确实方便，但也有缺点。因为实现者可以自行决定是否与DOM规范的不同部分保持一致。事实上，要想让hasFearture（）方法针对所有值都返回true很容易，但返回true有时候也不意味着实现与规范一致。例如，Safari2x及更早版本会在没有完全实现某些DOM功能的情况下也返回true。为此，我们建议多数情况下，在使用DOM的某些特殊的功能之前，最好除了检测hasFeature（）之外，还同时使用能力检测。

6. 文档写入

   有一个document对象的功能已经存在很多年了，那就是将输出流写人到网页中的能力。这个能力体现在下列4个方法中：write（）、writeln（）、open（）和close（）。其中，write（）和writeln（）方法都接受一个字符串参数，即要写入到输出流中的文本。write（）会原样写入，而writeln（）则会在字符串的末尾添加一个换行符（\n）。在页面被加载的过程中，可以使用这两个方法向页面中动态地加入内容，如下面的例子所示。

   ~~~javascript
   <!DOCTYPE html>
   <html>
   <head>
       <title>document.write() Example</title>
   </head>
   <body>
       <p>The current date and time is:
       <script type="text/javascript">
           document.write("<strong>" + (new Date()).toString() + "</strong>");
       </script>
       </p>
   </body>
   </html>
   ~~~

   这个例子展示了在页面加载过程中输出当前日期和时间的代码。其中，日期被包含在一个< strong>
   元素中，就像在HTML页面中包含普通的文本一样。这样做会创建一个DOM元素，而且可以在将来访问该元素。通过write（）和writeln（）输出的任何HTML代码都将如此处理。
   此外，还可以使用write（）和writeln（）方法动态地包含外部资源，例如JavaScript文件等。在包含JavaScript文件时，必须注意不能像下面的例子那样直接包含字符串"< /script>”，因为这会导致该字符串被解释为脚本块的结束，它后面的代码将无法执行。

   ~~~javascript
   <!DOCTYPE html>
   <html>
   <head>
       <title>document.write() Example 2</title>
   </head>
   <body>
       <script type="text/javascript">
           document.write("<script type=\"text\javascript\" src=\"file.js\">" +   
               "</script>");
       </script>
   </body>
   </html>
   ~~~

   即使这个文件看起来没错，但字符串“< /script>“将被解释为与外部的< script>标签匹配，结果文本“）；将会出现在页面中。为避免这个问题，只需把这个字符串分开写即可；第2章也曾经提及这个问题，解决方案如下。

   ~~~javascript
   <!DOCTYPE html>
   <html>
   <head>
       <title>document.write() Example 3</title>
   </head>
   <body>
       <script type="text/javascript">
           document.write("<script type=\"text\javascript\" src=\"file.js\">" +   
               "<\/script>");
       </script>
   </body>
   </html>
   
   ~~~

   字符串<\/script>不会被当作外部< script>标签的关闭标签，因而页面中也就不会出现多余的内容了。
   前面的例子使用document.write（）在页面被呈现的过程中直接向其中输出了内容。如果在文档加载结束后再调用document.write（），那么输出的内容将会重写整个页面，如下面的例子所示：

   ~~~javascript
   <!DOCTYPE html>
   <html>
   <head>
       <title>document.write() Example 4</title>
   </head>
   <body>
       <p>This is some content that you won't get to see because it will be overwritten.</p>
       <script type="text/javascript">
           window.onload = function(){
               document.write("Hello world!");
           };
       </script>
   </body>
   </html>
   ~~~

   在这个例子中，我们使用了**window.onload事件处理程序**（事件将在第13章讨论），等到页面完全加载之后延迟执行函数。函数执行之后，字符串“Hello world！“会重写整个页面内容。

   方法open（）和close（）分别用于打开和关闭网页的输出流。如果是在页面加载期间使用write（）或writeln（）方法，则不需要用到这两个方法。

   > 严格型XIHTML文档不支持文档写入。对于那些按照application/xml+xhtml内容类型提供的页面，这两个方法也同样无效。

### Element类型

除了Document类型之外，Element类型就要算是Web编程中最常用的类型了。Element类型用于表现XML或HTML元素，提供了对元素标签名、子节点及特性的访问。Element节点具有以下特征：

~~~javascript
nodeType的值为1；

nodeName的值为元素的标签名；

nodeValue的值为nu11；

parentNode可能是Document或Element；

其子节点可能是Element、Text、Comment、ProcessingInstruction、cDATASection或EntityReference。
~~~

要访问元素的标签名，可以使用nodeName属性，也可以使用tagName属性；这两个属性会返回相同的值（使用后者主要是为了清晰起见）。以下面的元素为例：

~~~javascript
<div id='myDiv'></div>
~~~

可以像下面这样取得这个元素及其标签名：

~~~javascript
var div = document. getElementById("myDiv"); 
alert(div.tagName);		//"DIV"
alert(div.tagName == div.nodeName);		//true
~~~

这里的元素标签名是div，它拥有一个值为“myDiv的ID。可是，div.tagName实际上输出的是"DIV而非·div"。在HTML中，标签名始终都以全部大写表示；而在XML（有时候也包括XHTML）中，标签名则始终会与源代码中的保持一致。假如你不确定自己的脚本将会在HTML还是XML文档中执行，最好是在比较之前将标签名转换为相同的大小写形式，如下面的例子所示：

~~~javascript
if（element.tagName == “div“）{	//不能这样比较，很容易出错！
//在此执行某些操作
}

if（element.tagName.tolowerCase（）==“div"）（	//这样最好（适用于任何文档）
//在此执行某些操作
}
~~~

这个例子展示了围绕tagName属性的两次比较操作。第一次比较非常容易出错，因为其代码在HTML文档中不管用。第二次比较将标签名转换成了全部小写，是我们推荐的做法，因为这种做法适用于HTML文档，也适用于XML文档。

> 可以在任何浏览器中通过脚本访问Element类型的构造函数及原型，包括I正8及之前版本。在Safari2之前版本和Opera8之前的版本中，不能访问Element类型的构造函数。

1. HTML元素

   所有HTML元素都由HTML.Element类型表示，不是直接通过这个类型，也是通过它的子类型来表示。HTMLElement类型直接继承自Element并添加了一些属性。添加的这些属性分别对应于每个HTML元素中都存在的下列标准特性。

   ~~~javascript
   id，元素在文档中的唯一标识符。
   title，有关元素的附加说明信息，一般通过工具提示条显示出来。
   1ang，元素内容的语言代码，很少使用。
   dir，语言的方向，值为“1tr”（left-to-right，从左至右）或“rt1"（right-to-left，从右至左），也很少使用。
   className，与元素的class特性对应，即为元素指定的CSS类。没有将这个属性命名为class，是因为c1ass是ECMAScript的保留字（有关保留字的信息，请参见第1章）。
   ~~~

   上述这些属性都可以用来取得或修改相应的特性值。以下面的HTML元素为例：

   ~~~javascript
   <div id="myDiv" class="bd" title="Body text" lang="en" dir="ltr"></div>
   ~~~

   元素中指定的所有信息，都可以通过下列JavaScript代码取得：

   ~~~javascript
   var div = document.getElementById("myDiv");
   alert(div.id);         //"myDiv"
   alert(div.className);  //"bd"
   alert(div.title);      //"Body text"
   alert(div.lang);       //"en"
   alert(div.dir);        //"ltr"
   ~~~

   当然，像下面这样通过为每个属性赋予新的值，也可以修改对应的每个特性：

   ~~~javascript
    div.id = "someOtherId";
    div.className = "ft";
    div.title = "Some other text";
    div.lang = "fr";
    div.dir ="rtl";        
   ~~~

   并不是对所有属性的修改都会在页面中直观地表现出来。对id或1ang的修改对用户而言是透明不可见的（假设没有基于它们的值设置的CSS样式），而对tit1e的修改则只会在鼠标移动到这个元素之上时才会显示出来。对dir的修改会在属性被重写的那一刻，立即影响页面中文本的左、右对齐方式。
   修改className时，如果新类关联了与此前不同的CSS样式，那么就会立即应用新的样式。

   前面提到过，所有HTML元素都是由HTMLElement或者其更具体的子类型来表示的。下表列出了所有HTML元素以及与之关联的类型（以斜体印刷的元素表示已经不推荐使用了）。注意，表中的这些类型在Opera、Safari、Chrome和Firefox中都可以通过JavaScript访问，但在IE8之前的版本中不能通过JavaScript访问。

   ![](读书笔记：JavaScript高级程序设计(第3版)/114.png)

   表中的每一种类型都有与之相关的特性和方法。本书将会讨论其中很多类型。

2. 取得特性

   每个元素都有一或多个特性，这些特性的用途是给出相应元素或其内容的附加信息。操作特性的DOM方法主要有三个，分别是getAttribute（）、setAttribute（）和removeAttribute（）。这三个方法可以针对任何特性使用，包括那些以HIMLElement类型属性的形式定义的特性。来看下面的例子：

   ~~~javascript
   var div = document.getElementById("myDiv");
   alert(div.getAttribute("id"));         //"myDiv"
   alert(div.getAttribute("class"));      //"bd"
   alert(div.getAttribute("title"));      //"Body text"
   alert(div.getAttribute("lang"));       //"en"
   alert(div.getAttribute("dir"));        //"ltr"
   ~~~

   注意，传递给 getattribute（）的特性名与实际的特性名相同。因此要想得到class特性值，应该传入“class"而不是“className”，后者只有在通过对象属性访问特性时才用。如果给定名称的特性不存在，getAttribute（）返回nul1。

   通过 getAttribute（）方法也可以取得自定义特性（即标准HTML语言中没有的特性）的值，以下面的元素为例：

   ~~~javascript
   <div id="myDiv" my_special_attribute="hello!"></div>
   ~~~

   这个元素包含一个名为my_special_attribute的自定义特性，它的值是“he11o！。可以像取得其他特性一样取得这个值，如下所示：

   ~~~javascript
   var value = div.getAttribute("my_special_attribute");
   ~~~

   不过，特性的名称是不区分大小写的，即ID“和“id“代表的都是同一个特性。另外也要注意，根据HTML5规范，自定义特性应该加上data-前缀以便验证。

   任何元素的所有特性，也都可以通过DOM元素本身的属性来访问。当然，HTMLElement也会有5个属性与相应的特性一一对应。不过，只有公认的（非自定义的）特性才会以属性的形式添加到DOM对象中。以下面的元素为例：

   ~~~javascript
    <div id="myDiv" align="left" my_special_attribute="hello!"></div>
   ~~~

   因为id和align在HTML中是< div>的公认特性，因此该元素的DOM对象中也将存在对应的属性。不过，自定义特性my_special_attribute在Safari、Opera、Chrome及Firefox中是不存在的；但I正却会为自定义特性也创建属性，如下面的例子所示：

   ~~~javascript
    alert(div.id);                     //"myDiv"
    alert(div.my_special_attribute);   //"hello!" (IE除外)
    alert(div.align);                  //"left"
   ~~~

   有两类特殊的特性，它们虽然有对应的属性名，但属性的值与通过getAttribute（）返回的值并不相同。第一类特性就是sty1e，用于通过CSS为元素指定样式。在通过getAttribute（）访问时，返回的sty1e特性值中包含的是CSS文本，而通过属性来访问它则会返回一个对象。由于style属性是用于以编程方式访问元素样式的（本章后面讨论），因此并没有直接映射到sty1e特性。

   第二类与众不同的特性是onclick这样的事件处理程序。当在元素上使用时，onclick特性中包含的是JavaScript代码，如果通过getAttribute（）访问，则会返回相应代码的字符串。而在访问onclick 属性时，则会返回一个JavaScript函数（如果未在元素中指定相应特性，则返回nu11）。这是因为onclick及其他事件处理程序属性本身就应该被赋予函数值。

   由于存在这些差别，在通过JavaScript以编程方式操作DOM时，开发人员经常不使用getAttribute（），而是只使用对象的属性。只有在取得自定义特性值的情况下，才会使用getAttribute（）方法。

   > 在IE7及以前版本中，通过getAttribute（）方法访问style特性或onclick这样的事件处理特性时，返回的值与属性的值相同。换句话说，getAttribute（"style"）返回一个对象，而getAttribute（"onclick”）返回一个函数。虽然IE8已经修复了这个bug，但不同E版本间的不一致性，也是导致开发人员不使用getAttribute（）访问HTML特性的一个原因。

3. 设置特性

   与getAttribute（）对应的方法是setAttribute（），这个方法接受两个参数：要设置的特性名和值。如果特性已经存在，setAttribute（）会以指定的值替换现有的值；如果特性不存在，setAttribute（）则创建该属性并设置相应的值。来看下面的例子：

   ~~~javascript
    div.setAttribute("id", "someOtherId");
    div.setAttribute("class", "ft");
    div.setAttribute("title", "Some other text");
    div.setAttribute("lang","fr");
    div.setAttribute("dir", "rtl");        
   ~~~

   通过setAttribute（）方法既可以操作HTML特性也可以操作自定义特性。通过这个方法设置的特性名会被统一转换为小写形式，即"ID最终会变成“id"。
   因为所有特性都是属性，所以直接给属性赋值可以设置特性的值，如下所示。

   ~~~javascript
   div.id = 'someOtherId';
   div.align = 'left';
   ~~~

   不过，像下面这样为DOM元素添加一个自定义的属性，该属性不会自动成为元素的特性。

   ~~~javascript
   div.mycolor="red"；
   alert（div.getAttribute（"mycolor"））；//nul1（IE除外）
   ~~~

   这个例子添加了一个名为mycolor的属性并将它的值设置为“red“。在大多数浏览器中，这个属性都不会自动变成元素的特性，因此想通过getAttribute（）取得同名特性的值，结果会返回nul1。
   可是，自定义属性在E中会被当作元素的特性，反之亦然。

   > 在IE7及以前版本中，setAttribute（）存在一些异常行为。通过这个方法设置class和style特性，没有任何效果，而使用这个方法设置事件处理程序特性时也一样。尽管到了IE8才解决这些问题，但我们还是推荐通过属性来设置特性。

   要介绍的最后一个方法是removeAttribute（），这个方法用于彻底删除元素的特性。调用这个方法不仅会清除特性的值，而且也会从元素中完全删除特性，如下所示：

   ~~~javascript
   div.removeAttribute("class");
   ~~~

   这个方法并不常用，但在序列化DOM元素时，可以通过它来确切地指定要包含哪些特性。

   > IE6及以前版本不支持removeAttribute（）。

4. attributes属性

   Element类型是使用attributes属性的唯一一个DOM节点类型。attributes属性中包含一个NamedNodeMap，与NodeList类似，也是一个“动态”的集合。元素的每一个特性都由一个Attr节点表示，每个节点都保存在NamedNodeMap对象中。NamedNodeMap对象拥有下列方法。

   ~~~javascript
   getNamedItem（name）：返回 nodeName 属性等于name的节点；
   removeNamedItem（name）：从列表中移除nodeName属性等于name的节点；
   setNamedItem（node）：向列表中添加节点，以节点的nodeName属性为索引；
   item（pos）：返回位于数字pos位置处的节点。
   ~~~

   attributes属性中包含一系列节点，每个节点的nodeName就是特性的名称，而节点的nodeValue就是特性的值。要取得元素的id特性，可以使用以下代码。

   ~~~javascript
   var id = element. attributes. getNamedItem("id"). nodeValue;
   ~~~

   以下是使用方括号语法通过特性名称访问节点的简写方式。

   ~~~javascript
   var id = element.attributes["id"].nodeValue;
   ~~~

   也可以使用这种语法来设置特性的值，即先取得特性节点，然后再将其nodeValue设置为新值，如下所示。

   ~~~javascript
   element.attributes["id"].nodeValue="someotherId";
   ~~~

   调用removeNamedrtem（）方法与在元素上调用removeAttribute（）方法的效果相同——直接删除具有给定名称的特性。下面的例子展示了两个方法间唯一的区别，即removeNamedrtem（）返回表示被删除特性的Attr节点。

   ~~~javascript
   var oldAttr = element.attributes.removeNamedrtem("id");
   ~~~

   最后，setNamedrtem（）是一个很不常用的方法，通过这个方法可以为元素添加一个新特性，为此需要为它传人一个特性节点，如下所示。

   ~~~javascript
   element.attributes.setNamedItem(newAttr);
   ~~~

   一般来说，由于前面介绍的attributes的方法不够方便，因此开发人员更多的会使用getAttribute（）、removeAttribute（）和setAttribute（）方法。

   不过，如果想要遍历元素的特性，attributes属性倒是可以派上用场。在需要将DOM结构序列化为XML或HTML字符串时，多数都会涉及遍历元素特性。以下代码展示了如何迭代元素的每一个特性，然后将它们构造成name="value”name="value“这样的字符申格式。

   ~~~javascript
    function outputAttributes(element){
         var pairs = new Array(),
               attrName,
               attrValue,
               i,
               len;
   
          for (i=0, len=element.attributes.length; i < len; i++){
               attrName = element.attributes[i].nodeName;
               attrValue = element.attributes[i].nodeValue;
               if (element.attributes[i].specified){
                    pairs.push(attrName + "=\"" + attrValue + "\"");
                }
          }
          return pairs.join(" ");
   }
   ~~~

   这个经过改进的函数可以确保即使在IE7及更早的版本中，也会只返回指定的特性。

5. 创建元素

   使用document.createElement（）方法可以创建新元素。这个方法只接受一个参数，即要创建元素的标签名。这个标签名在HTML文档中不区分大小写，而在XML（包括XHTML）文档中，则是区分大小写的。例如，使用下面的代码可以创建一个< div>元素。

   ~~~javascript
   var div = document. createElement("div");
   ~~~

   在使用createlement（）方法创建新元素的同时，也为新元素设置了ownerDocuemnt属性。此时，还可以操作元素的特性，为它添加更多子节点，以及执行其他操作。来看下面的例子。

   ~~~javascript
   div.id="myNewDiv"; 
   div.className="box";
   ~~~

   在新元素上设置这些特性只是给它们赋予了相应的信息。由于新元素尚未被添加到文档树中，因此设置这些特性不会影响浏览器的显示。要把新元素添加到文档树，可以使用appendchi1d（）、inser-
   tBefore（）或replacechi1d（）方法。下面的代码会把新创建的元素添加到文档的< body>元素中。

   ~~~javascript
   document.body.appendChild(div);
   ~~~

   一旦将元素添加到文档树中，浏览器就会立即呈现该元素。此后，对这个元素所作的任何修改都会实时反映在浏览器中。

   在IE中可以以另一种方式使用createElement（），即为这个方法传人完整的元素标签，也可以包含属性，如下面的例子所示。

   ~~~javascript
   var div = document. createElement("<div id=\"myNewDiv\"class=\"box\"></div>");
   ~~~

   这种方式有助于避开在IE7及更早版本中动态创建元素的某些问题。下面是已知的一些这类问题。

   ~~~javascript
   不能设置动态创建的<iframe>元素的name特性。
   
   不能通过表单的reset（）方法重设动态创建的<input>元素（第13章将讨论reset（）方法）。
   
   动态创建的type 特性值为“reset"的<button>元素重设不了表单。
   
   动态创建的一批name相同的单选按钮彼此毫无关系。name值相同的一组单选按钮本来应该用于表示同一选项的不同值，但动态创建的一批这种单选按钮之间却没有这种关系。
   ~~~
   上述所有问题都可以通过在createElement（）中指定完整的HTML标签来解决，如下面的例子所示。

   ~~~javascript
   if（client.browser.ie&&client.browser.ie<=7）{
       
   //创建一个带name特性的iframe元素
   var iframe = document.createElement（"<iframe name=\"my frame\"></iframe>"）;
       
   //创建input元素
   var input = document.createElement（"<input type=\"checkbox\">"）;
       
   //创建button元素
   var button = document.createElement（"<button type=\"reset\"></button>"）;
       
   //创建单选按钮
   var radiol = document.createElement（"<input type=\"radio\"name=\"choice\""+
   “value=\“1\">"）；
   var radio2 = document.createElement（"<ingut type=\"radio\"name=\"choice\*"+
   “value=\"2\">"）;
   ~~~

   与使用createElement（）的惯常方式一样，这样的用法也会返回一个DOM元素的引用。可以将这个引用添加到文档中，也可以对其加以增强。但是，由于这样的用法要求使用浏览器检测，因此我们建议只在需要避开IE及更早版本中上述某个问题的情况下使用。其他浏览器都不支持这种用法。

6. 元素的子节点

   元素可以有任意数目的子节点和后代节点，因为元素可以是其他元素的子节点。元素的childNodes属性中包含了它的所有子节点，这些子节点有可能是元素、文本节点、注释或处理指令。
   不同浏览器在看待这些节点方面存在显著的不同，以下面的代码为例。

   ~~~javascript
    <ul id="myList">
          <li>Item1</li>
          <li>Item2</li>
          <li>Item3</li>
    </ul>
   ~~~

   如果是E来解析这些代码，那么< ul>元素会有3个子节点，分别是3个<1i>元素。但如果是在其他浏览器中，   < u1>元素都会有7个元素，包括3个<1i>元素和4个文本节点（表示<1i>元素之间的空白符）。如果像下面这样将元素间的空白符删除，那么所有浏览器都会返回相同数目的子节点。

   ~~~javascript
   <ul id="myList"><li>Item 1</li><li>rtem 2</li><li>Item 3</li></ul>
   ~~~

   对于这段代码，<u1>元素在任何浏览器中都会包含3个子节点。如果需要通过childNodes属性遍历子节点，那么一定不要忘记浏览器间的这一差别。这意味着在执行某项操作以前，通常都要先检查一下noderpye属性，如下面的例子所示。

   ~~~javascript
   for（var i=0，len=element.childNodes.length；i< len；i++）{
   	if（element.childNodes[i].nodeType == 1）{
   	//执行某些操作
       }
   }
   ~~~

   这个例子会循环遍历特定元素的每一个子节点，然后只在子节点的nodeType等于1（表示是元素节点）的情况下，才会执行某些操作。

   如果想通过某个特定的标签名取得子节点或后代节点该怎么办呢？实际上，元素也支持getElementsByTagName（）方法。在通过元素调用这个方法时，除了搜索起点是当前元素之外，其他方面都跟通过document调用这个方法相同，因此结果只会返回当前元素的后代。例如，要想取得前面
   ​      < u1>元素中包含的所有<1i>元素，可以使用下列代码。

   ~~~javascript
   var ul = document. getElementById("myList"); 
   var items = ul.getElementsByTagName("1i");
   ~~~

   要注意的是，这里< u1>的后代中只包含直接子元素。不过，如果它包含更多层次的后代元素，那么各个层次中包含的<1i>元素也都会返回。

### Text类型

文本节点由Text类型表示，包含的是可以照字面解释的纯文本内容。纯文本中可以包含转义后的HTML字符，但不能包含HTML代码。Text节点具有以下特征：

~~~javascript
nodeType的值为3；
nodeName的值为“#text";
nodeValue的值为节点所包含的文本；
parentNode是一个Element；
不支持（没有）子节点。
~~~

可以通过nodeValue属性或data属性访问Text节点中包含的文本，这两个属性中包含的值相同。对nodeValue的修改也会通过data反映出来，反之亦然。使用下列方法可以操作节点中的文本。

~~~javascript
appendData（text）：将text添加到节点的末尾。
deleteData（offset，count）：从offset指定的位置开始删除count个字符。
insertData（offset，text）：在 offset 指定的位置插入text。
replaceData（offset，count，text）：用text 替换从offset 指定的位置开始到offset+
count为止处的文本。
splitText（offset）：从offset指定的位置将当前文本节点分成两个文本节点。
subatringData（offset，count）：提取从offset 指定的位置开始到offset+count为止处的字符串。
~~~

除了这些方法之外，文本节点还有一个1ength属性，保存着节点中字符的数目。而且，nodeValue.length和data.1ength中也保存着同样的值。

在默认情况下，每个可以包含内容的元素最多只能有一个文本节点，而且必须确实有内容存在。来看几个例子。

~~~javascript
<！--没有内容，也就没有文本节点-->
<div></div>

<！--有空格，因而有一个丈本节点-->
<div> </div>

<！--有内容，因而有一个文本节点-->
<div>Hello world！</div>
~~~

上面代码给出的第一个< div>元素没有内容，因此也就不存在文本节点。开始与结束标签之间只要存在内容，就会创建一个文本节点。因此，第二个 < div>元素中虽然只包含一个空格，但仍然有一个文本子节点；文本节点的nodeValue值是一个空格。第三个< div>也有一个文本节点，其nodeValue的值为“He11o World！"。可以使用以下代码来访问这些文本子节点。

~~~javascript
var textNode = div.firstChild；			//或者div.childNodes[0]
~~~

在取得了文本节点的引用后，就可以像下面这样来修改它了。

~~~javascript
div.firstChild.nodeValue = "Some other message";
~~~

如果这个文本节点当前存在于文档树中，那么修改文本节点的结果就会立即得到反映。另外，在修改文本节点时还要注意，此时的字符串会经过HTML（或XML，取决于文档类型）编码。换句话说，小于号、大于号或引号都会像下面的例子一样被转义。

~~~javascript
//输出结果是“Some &lt；strong&gt；other&lt；/strong&gt；message"
div.firstChild.nodeValue = "Some <strong>other</strong> message";
~~~

应该说，这是在向DOM文档中插入文本之前，先对其进行HTML编码的一种有效方式。

> 在IE8、Firefox、Safari、Chrome和Opera中，可以通过脚本访问Text类型的构造函数和原型。

1. 创建文本节点

   可以使用document.createTextNode（）创建新文本节点，这个方法接受一个参数——要插入节点中的文本。与设置已有文本节点的值一样，作为参数的文本也将按照HTML或XML的格式进行编码。

   ~~~javascript
   var textNode = document.createTextNode("<strong>Hello</strong>world!");
   ~~~

   在创建新文本节点的同时，也会为其设置ownerDocument属性。不过，除非把新节点添加到文档树中已经存在的节点中，否则我们不会在浏览器窗口中看到新节点。下面的代码会创建一个< div>元素并向其中添加一条消息。

   ~~~javascript
   var element = document.createElement("div");
   element.className = "message";
               
   var textNode = document.createTextNode("Hello world!");
   element.appendChild(textNode);
               
   document.body.appendChild(element);
   ~~~

   这个例子创建了一个新cdiv>元素并为它指定了值为“message”的class特性。然后，又创建了一个文本节点，并将其添加到前面创建的元素中。最后一步，就是将这个元素添加到了文档的<body>
   元素中，这样就可以在浏览器中看到新创建的元素和文本节点了。

   一般情况下，每个元素只有一个文本子节点。不过，在某些情况下也可能包含多个文本子节点，如下面的例子所示。

   ~~~javascript
    var element = document.createElement("div");
    element.className = "message";
               
    var textNode = document.createTextNode("Hello world!");
    element.appendChild(textNode);
               
    var anotherTextNode = document.createTextNode("Yippee!");
    element.appendChild(anotherTextNode);
               
    document.body.appendChild(element);
   ~~~

   如果两个文本节点是相邻的同胞节点，那么这两个节点中的文本就会连起来显示，中间不会有空格。

2. 规范化文本节点

   DOM文档中存在相邻的同胞文本节点很容易导致混乱，因为分不清哪个文本节点表示哪个字符串。另外，DOM文档中出现相邻文本节点的情况也不在少数，于是就催生了一个能够将相邻文本节点合并的方法。这个方法是由Node类型定义的（因而在所有节点类型中都存在），名叫normalize（）。如果在一个包含两个或多个文本节点的父元素上调用normalize（）方法，则会将所有文本节点合并成一个节点，结果节点的nodeValue等于将合并前每个文本节点的nodeValue值拼接起来的值。来看一个例子。

   ~~~javascript
   var element = document.createElement("div");
   element.className = "message";
               
   var textNode = document.createTextNode("Hello world!");
   element.appendChild(textNode);
               
   var anotherTextNode = document.createTextNode("Yippee!");
   element.appendChild(anotherTextNode);
               
   document.body.appendChild(element);
               
   alert(element.childNodes.length);  //2
               
   element.normalize();
   alert(element.childNodes.length);  //1
   alert(element.firstChild.nodeValue);  //"Hello World!Yippee!"
   ~~~

   浏览器在解析文档时永远不会创建相邻的文本节点。这种情况只会作为执行DOM操作的结果出现。

   > 在某些情况下，执行normalize（）方法会导致IE6崩渍。不过，在IE6后来的补丁中，可能已经修复了这个问题（未经证实）。IE7及更高版本中不存在这个问题。

3. 分割文本节点

   Text类型提供了一个作用与normalize（）相反的方法：splitText（）。这个方法会将一个文本节点分成两个文本节点，即按照指定的位置分割nodeValue值。原来的文本节点将包含从开始到指定位置之前的内容，新文本节点将包含剩下的文本。这个方法会返回一个新文本节点，该节点与原节点的parentNode 相同。来看下面的例子。

   ~~~javascript
   var element = document.createElement("div");
   element.className = "message";
               
   var textNode = document.createTextNode("Hello world!");
   element.appendChild(textNode);
               
   document.body.appendChild(element);
               
   var newNode = element.firstChild.splitText(5);
   alert(element.firstChild.nodeValue);  //"Hello"
   alert(newNode.nodeValue);             //" world!"
   alert(element.childNodes.length);     //2
   ~~~

   在这个例子中，包含“He11o world！“的文本节点被分割为两个文本节点，从位置5开始。位置5是“He11o“和“wor1d:“之间的空格，因此原来的文本节点将包含字符串“He11o*，而新文本节点将包含文本"wor1d！”（包含空格）。

   分割文本节点是从文本节点中提取数据的一种常用DOM解析技术。

### Comment类型

注释在DOM中是通过comment类型来表示的。Comment节点具有下列特征：

~~~javascript
nodeType的值为8；
nodeName的值为“#comment"；
nodeValue的值是注释的内容；
parentNode 可能是Document或Element；
不支持（没有）子节点。
~~~

Comment类型与Text类型继承自相同的基类，因此它拥有除splitText（）之外的所有字符串操作方法。与Text类型相似，也可以通过nodeValue或data属性来取得注释的内容。

注释节点可以通过其父节点来访问，以下面的代码为例。

~~~javascript
<div id="myDiv"><!--A comment--></div>
~~~

在此，注释节点是< div>元素的一个子节点，因此可以通过下面的代码来访问它。

~~~javascript
var div = document.getElementById("myDiv");
var comment = div.firstChild;
alert(comment.data);
~~~

另外，使用document.createcomnent（）并为其传递注释文本也可以创建注释节点，如下面的例子所示。

~~~javascript
var comment = document. createComment("A comment ");
~~~

显然，开发人员很少会创建和访问注释节点，因为注释节点对算法鲜有影响。此外，浏览器也不会识别位于          < /htm1>标签后面的注释。如果要访问注释节点，一定要保证它们是< html>元素的后代（即位于< htm1>和       < /html>之间）。

> 在Firefox、Safari、Chrome和Opera中，可以访问Comment类型的构造函数和原型。在IE8中，注释节点被视作标签名为“！”的元素。也就是说，使用getElementsByTagName（）可以取得注释节点。尽管IE9没有把注释当成元素，但它仍然通过一个名为HTML.CommentElement的构造函数来表示注释。

### CDATASection类型

cDATASection类型只针对基于XML的文档，表示的是CDATA区域。与comment类似，cDATASection 类型继承自Text类型，因此拥有除splitText（）之外的所有字符串操作方法。
CDATASection节点具有下列特征：

~~~javascript
noderype的值为4；
nodeName的值为“#cdata-section"；
nodeValue的值是CDATA区域中的内容；
parentNode可能是Document或Element；
不支持（没有）子节点。
~~~

CDATA区域只会出现在XML文档中，因此多数浏览器都会把CDATA区域错误地解析为comment或Element。以下面的代码为例：

~~~javascript
<div id="myDiv"><![CDATA[ This is some content.]]></div>
~~~

这个例子中的< div>元素应该包含一个CDATASection节点。可是，四大主流浏览器无一能够这样解析它。即使对于有效的XHTML页面，浏览器也没有正确地支持嵌入的CDATA区域。

在真正的XML文档中，可以使用document.createCDataSection（）来创建CDATA区域，只需为其传入节点的内容即可。

> 在Firefox、Safari、Chrome和Opera中，可以访问 cDAASection类型的构造函数和原型。IE9及之前版本不支持这个类型。

### DocumentType类型

DocumentType 类型在Web浏览器中并不常用，仅有Firefox、Safari和Opera支持它。DocumentType 包含着与文档的doctype有关的所有信息，它具有下列特征：

~~~javascript
nodeType的值为10；
nodeName的值为doctype的名称；
nodeValue的值为nul1；
parentNode是Document；
不支持（没有）子节点。
~~~

在DOM1级中，DocumenType对象不能动态创建，而只能通过解析文档代码的方式来创建。支持它的浏览器会把DocumentType对象保存在document.doctype中。DOM1级描述了DocumentType 对象的3个属性：name、entities和notations。其中，name表示文档类型的名称；entities 是由文档类型描述的实体的NamedNodeMap 对象；notations是由文档类型描述的符号的NamedNodeMap对象。通常，浏览器中的文档使用的都是HTML或XHTML文档类型，因而entities和notations都是空列表（列表中的项来自行内文档类型声明）。但不管怎样，只有name属性是有用的。这个属性中保存的是文档类型的名称，也就是出现在<!DOCTYPE之后的文本。以下面严格型 HTML
4.01的文档类型声明为例：

~~~javascript
<！DOCTYPE HTML PUBLIC"-//W3C//DTD HTML 4.01//EN"
"http://www.w3.org/TR/html4/strict.dtd">
    
DocumentType的 name属性中保存的就是“HTML"：
alert（document.doctype.name）；	//“HTML"
~~~

IE及更早版本不支持Documentrype，因此document.doctype的值始终都等于nu11。可是，这些浏览器会把文档类型声明错误地解释为注释，并且为它创建一个注释节点。IE9会给document.doctype 赋正确的对象，但仍然不支持访问DocumentType类型。

### DocumentFragment类型

在所有节点类型中，只有DocumentFragment在文档中没有对应的标记。DOM规定文档片段（document fragment）是一种“轻量级”的文档，可以包含和控制节点，但不会像完整的文档那样占用额外的资源。DocumentFragment节点具有下列特征：

~~~javascript
noderype的值为11；
nodeName的值为“#document-fragment"；
nodeValue的值为nu11；
parentNode的值为nu11；
子节点可以是Element、ProcessingInstruction、Comment、Text、CDATASection或EntityReference。
~~~

虽然不能把文档片段直接添加到文档中，但可以将它作为一个“仓库”来使用，即可以在里面保存将来可能会添加到文档中的节点。要创建文档片段，可以使用document.createDocumentFragment（）方法，如下所示：

~~~javascript
var fragment = document. createDocumentFragment();
~~~

文档片段继承了Node的所有方法，通常用于执行那些针对文档的DOM操作。如果将文档中的节点添加到文档片段中，就会从文档树中移除该节点，也不会从浏览器中再看到该节点。添加到文档片段中的新节点同样也不属于文档树。可以通过appendchild（）或insertBefore（）将文档片段中内容添加到文档中。在将文档片段作为参数传递给这两个方法时，实际上只会将文档片段的所有子节点添加到相应位置上；文档片段本身永远不会成为文档树的一部分。来看下面的HTML示例代码：

~~~javascript
<ul id="myList"></ul>
~~~

假设我们想为这个< u1>元素添加3个列表项。如果逐个地添加列表项，将会导致浏览器反复渲染（呈现）新信息。为避免这个问题，可以像下面这样使用一个文档片段来保存创建的列表项，然后再一次性将它们添加到文档中。

~~~javascript
 var fragment = document.createDocumentFragment();
 var ul = document.getElementById("myList");
 var li = null;
            
 for (var i=0; i < 3; i++){
      li = document.createElement("li");
      li.appendChild(document.createTextNode("Item " + (i+1)));
           fragment.appendChild(li);
      }
            
ul.appendChild(fragment);  
~~~

在这个例子中，我们先创建一个文档片段并取得了对<u1>元素的引用。然后，通过for 循环创建3个列表项，并通过文本表示它们的顺序。为此，需要分别创建<1i>元素、创建文本节点，再把文本节点添加到<1i>元素。接着使用appendchild（）将<1i>元素添加到文档片段中。循环结束后，再调用appendchild（）并传入文档片段，将所有列表项添加到< ul>元素中。此时，文档片段的所有子节点都被删除并转移到了< u1>元素中。

### Attr类型

元素的特性在DOM中以Attr类型来表示。在所有浏览器中（包括IE8），都可以访问Attr类型的构造函数和原型。从技术角度讲，特性就是存在于元素的attributes属性中的节点。特性节点具有下列特征：

~~~
noderype的值为11；
nodeName的值是特性的名称；
nodeValue的值是特性的值；
parentNode的值为nul1；
在HTML中不支持（没有）子节点；
在XML中子节点可以是Text或EntityReference。
~~~

尽管它们也是节点，但特性却不被认为是DOM文档树的一部分。开发人员最常使用的是getAt-
tribute（）、setAttribute（）和remveAttribute（）方法，很少直接引用特性节点。

Attr对象有3个属性：name、value和specified。其中，name是特性名称（与nodeName的值相同），value是特性的值（与nodeValue的值相同），而specified是一个布尔值，用以区别特性是在代码中指定的，还是默认的。

使用document.createAttribute（）并传入特性的名称可以创建新的特性节点。例如，要为元素添加align特性，可以使用下列代码：

~~~javascript
var attr = document.createAttribute("align");
attr.value = "left";
element.setAttributeNode(attr);
            
alert(element.attributes["align"].value);       //"left"
alert(element.getAttributeNode("align").value); //"left"
alert(element.getAttribute("align"));           //"left"
~~~

这个例子创建了一个新的特性节点。由于在调用createAttribute（）时已经为name属性赋了值，所以后面就不必给它赋值了。之后，又把value属性的值设置为“1eft”。为了将新创建的特性添加到元素中，必须使用元素的 setAttributeNode（）方法。添加特性之后，可以通过下列任何方式访问该特性：attributes属性、getAttributeNode（）方法以及 getAttribute（）方法。其中，attributes和getAttributeNode（）都会返回对应特性的Attr节点，而getAttribute（）则只返回特性的值。

> 我们并不建议直接访问特性节点。实际上，使用getAttribute（）、setAttribute（）和removeAttribute（）方法远比操作特性节点更为方便。

## DOM操作技术

很多时候，DOM操作都比较简明，因此用JavaScript生成那些通常原本是用HTML代码生成的内容并不麻烦。不过，也有一些时候，操作DOM并不像表面上看起来那么简单。由于浏览器中充斥着隐藏的陷阱和不兼容问题，用JavaScript代码处理DOM的某些部分要比处理其他部分更复杂一些。不过，也有一些时候，操作DOM并不像表面上看起来那么简单。

### 动态脚本

使用< script>元素可以向页面中插入JavaScript代码，一种方式是通过其src特性包含外部文件，另一种方式就是用这个元素本身来包含代码。而这一节要讨论的动态脚本，指的是在页面加载时不存在，但将来的某一时刻通过修改DOM动态添加的脚本。跟操作HTML元素一样，创建动态脚本也有两种方式：插入外部文件和直接插入JavaScript代码。

动态加载的外部JavaScript文件能够立即运行，比如下面的< script>元素：

~~~javascript
<script type="text/javascript" src="client.js"></script>
~~~

这个< script>元素包含了第9章的客户端检测脚本。而创建这个节点的DOM代码如下所示：

~~~javascript
var script = document. createElement ("script"); 
script. type = "text/javascript";
script. src = "client. js"; 
document.body.appendchild(script);
~~~

显然，这里的DOM代码如实反映了相应的HTML代码。不过，在执行最后一行代码把< script>元素添加到页面中之前，是不会下载外部文件的。也可以把这个元素添加到head>元素中，效果相同。
整个过程可以使用下面的函数来封装：

~~~javascript
function loadscript (url){
	var script = document. createElement ("script");
    script.type = "text/javascript"; 
    script.src = url;
    document.body.appendChild (script);
}
~~~

然后，就可以通过调用这个函数来加载外部的JavaScript文件了：

~~~javascript
loadscript ("client. js");
~~~

加载完成后，就可以在页面中的其他地方使用这个脚本了。问题只有一个：怎么知道脚本加载完成呢？遗憾的是，并没有什么标准方式来探知这一点。不过，与此相关的一些事件倒是可以派上用场，但要取决于所用的浏览器，详细讨论请见第13章。

另一种指定JavaScript代码的方式是行内方式，如下面的例子所示：

~~~javascript
<script type="text/javascript">
	function sayHi(){
		alert ("hi");
</script>
~~~

从逻辑上讲，下面的DOM代码是有效的：

~~~javascript
var script = document. createElement ("script");
script.type = "text/javascript"; 
script. appendChild (document. createTextNode ("function sayHi() {alert(' hi');}")); document.body.appendChild(script);
~~~

在Firefox，Safari、Chrome和Opera中，这些DOM代码可以正常运行。但在IE中，则会导致错误。
IE将< script>视为一个特殊的元素，不允许DOM访问其子节点。不过，可以使用< script>元素的text属性来指定JavasScript代码，像下面的例子这样：

~~~javascript
var script = document.createElement("script");
script.type = "text/javascript";
script.text = "function sayHi(){alert('hi');}";
document.body.appendChild(script);
~~~

经过这样修改之后的代码可以在IE，Firefox，Opera和Safari 3及之后版本中运行。Safari 3.0之前的版本虽然不能正确地支持text属性，但却允许使用文本节点技术来指定代码。如果需要兼容早期版本的Safari，可以使用下列代码：

~~~javascript
var script = document.createElement("script");
script.type = "text/javascript";
script.text = "function sayHi(){alert('hi');}";
try {
       script.appendChild(document.createTextNode(code));
} catch (ex){
       script.text = code;
}
 document.body.appendChild(script);
~~~

这里，首先尝试标准的DOM文本节点方法，因为除了E（在IE中会导致抛出错误），所有浏览器都支持这种方式。如果这行代码抛出了错误，那么说明是E，于是就必须使用text属性了。整个过程可以用以下函数来表示：

~~~javascript
function loadScriptString(code){
     var script = document.createElement("script");
     script.type = "text/javascript";
     try {
           script.appendChild(document.createTextNode(code));
     } catch (ex){
           script.text = code;
     }
     document.body.appendChild(script);
}
~~~

下面是调用这个函数的示例：

~~~javascript
loadScriptString("function sayHi(){alert('hi');}");
~~~

以这种方式加载的代码会在全局作用域中执行，而且当脚本执行后将立即可用。实际上，这样执行代码与在全局作用域中把相同的字符串传递给eval（）是一样的。

### 动态样式

能够把CSS样式包含到HTML页面中的元素有两个。其中，< link>元素用于包含来自外部的文件，而< style>元素用于指定嵌入的样式。与动态脚本类似，所谓动态样式是指在页面刚加载时不存在的样式；动态样式是在页面加载完成后动态添加到页面中的。

我们以下面这个典型的< link>元素为例：

~~~javascript
<link rel="stylesheet" types"text/css" href="styles.css">
~~~

使用DOM代码可以很容易地动态创建出这个元素：

~~~javascript
var link = document. createElement ("link");
1ink.rel = "stylesheet";
1ink.type = "text/css";
link.href = "style. css"; 
var head = document.getElementsByTagNane ("head")[0];
head. appendchild (1ink);
~~~

以上代码在所有主流浏览器中都可以正常运行。需要注意的是，必须将< link>元素添加到head>
而不是< body>元素，才能保证在所有浏览器中的行为一致。整个过程可以用以下函数来表示：

~~~css
function loadstyles(url) {
var link = document. createElement ("link");
1ink.rel = "stylesheet";
1ink.type = "text/css";
link.href = "style. css"; 
var head = document.getElementsByTagNane ("head")[0];
head. appendchild (1ink);
}    
~~~

调用loadstyles（）函数的代码如下所示：

~~~javascript
loadstyles ("styles.css");
~~~

加载外部样式文件的过程是异步的，也就是加载样式与执行JavaScript代码的过程没有固定的次序。
一般来说，知不知道样式已经加载完成并不重要；不过，也存在几种利用事件来检测这个过程是否完成的技术，这些技术将在第13章讨论。

另一种定义样式的方式是使用< style>元素来包含嵌入式css，如下所示：

~~~javascript
<style type-"text/css">
body {
      background-color: red;
}
</style>
~~~

按照相同的逻辑，下列DOM代码应该是有效的：

~~~javascript
function addStyle(){
    var style = document.createElement("style");
    style.type = "text/css";
    style.appendChild(document.createTextNode("body{background-color:red}"));  
    var head = document.getElementsByTagName("head")[0];
    head.appendChild(style);
}
~~~

以上代码可以在Firefox，Safari，Chrome和Opera中运行，在IE中则会报错。IE将< style>视为一个特殊的、与< script>类似的节点，不允许访问其子节点。事实上，IE此时抛出的错误与向< script>
元素添加子节点时抛出的错误相同。解决IE中这个问题的办法，就是访问元素的stylesheet属性，该属性又有一个cssText属性，可以接受CSS代码（第13章将进一步讨论这两个属性），如下面的例子所示。

~~~javascript
var style = document. createElement ("style"); 
style. type = "text/css";
tryt {
    style. appendChild (document. createrextNode ("body (background-color: red}"));
} catch (ex){
	Btyle. atylesheet. ceBText -"body (background-color: red)";
}
var head = document. getElenentsByTagName ("head") [0]; 
head. appendchild(styie);
~~~

与动态添加嵌入式脚本类似，重写后的代码使用了try-catch语句来捕获IE抛出的错误，然后再使用针对IE的特殊方式来设置样式。因此，通用的解决方案如下。

~~~javascript
function loadStyleString(css){
    var style = document.createElement("style");
    style.type = "text/css";
    try{
         style.appendChild(document.createTextNode(css));
    } catch (ex){
         style.styleSheet.cssText = css;
    }
    var head = document.getElementsByTagName("head")[0];
    head.appendChild(style);
}  
~~~

调用这个函数的示例如下：

~~~javascript
loadStyleString ("body (background-color:red} ");
~~~

这种方式会实时地向页面中添加样式，因此能够马上看到变化。

> 如果专门针对IE编写代码，务必小心使用styleSheet.cssText属性。在重用同一个< style>元素并再次设置这个属性时，有可能会导致浏览器崩溃。同样，将CSSText属性设置为空字符串也可能导致浏览器崩溃。我们希望IE中的这个bug能够在将来被修复。

### 操作表格

<table>元素是HTML中最复杂的结构之一。要想创建表格，一般都必须涉及表示表格行、单元格、表头等方面的标签。由于涉及的标签多，因而使用核心DOM方法创建和修改表格往往都免不了要编写大量的代码。假设我们要使用DOM来创建下面的HTML表格。

  ~~~javascript
<table border="1" width="100%">
	<tbody>
		<tr>
			<td>Cell 1,1</td>
			<td>Cell 2,1</td>
		</tr>
		<tr>
			<td>Cell 1,2</td>
			<td>Cell 2,2</td>
		</tr>
	</tbody>
</table>
  ~~~

要使用核心DOM方法创建这些元素，得需要像下面这么多的代码：

~~~javascript
//创建table 
var table = document.createtlement（"table"）；
table.border = 1；
table.width ="100%";

//创建tbody 
var tbody = document.createElement（"tbody"）;
table.appendchild（tbody）；

//创建第一行
var rowl = document.createElement（"tr"）；
tbody.appendchild（row1）；
var cel11_1 = document.createElement（"td"）；cel11_1.appendchild（document.createrextNode（"Cell 1，1"））；row1.appendchild（cell1_1.）;
var cel12_1 = document.createElement（"td"）；cel12_1.appendchild（document.createTextNode（"Cell 2，1"））;
rowl.appendChild（cel12_1）；

//创建第二行
var row2 = document.createElement（"tr"）;
tbody.appendchild（row2）;
var cell1_2 = document.createElement（"td"）;
cel11_2.appendChild（document.createTextNode（"Cell 1.2"））;
row2.appendchild（cell1_2）;
var cell2_2 = document.createElement（"td"）;
cel12_2.appendchild（document.createTextNode（"Cell 2，2"））;
row2.appendchild（cel12_2）;

//将表格添加到文档主体中
document.body.appendchild（table）；
~~~

显然，DOM代码很长，还有点不太好懂。为了方便构建表格，HTMLDOM还为< table>、< tbody>
和< tr>元素添加了一些属性和方法。

为< table>元素添加的属性和方法如下。

![](读书笔记：JavaScript高级程序设计(第3版)/115.png)

在这次的代码中，创建< table>和< tbody>的代码没有变化。不同的是创建两行的部分，其中使用了HTML DOM定义的表格属性和方法。在创建第一行时，通过< tbody>元素调用了insertRow（）方法，传入了参数0--表示应该将插入的行放在什么位置上。执行这一行代码后，就会自动创建一行并将其插入到< tbody>元素的位置0上，因此就可以马上通过tbody.rows[01来引用新插入的行。

创建单元格的方式也十分相似，即通过< tr>元素调用insertCell（）方法并传入放置单元格的位置。然后，就可以通过tbody.rows [0].cells [0]来引用新插入的单元格，因为新创建的单元格被插人到了这一行的位置0上。

总之，使用这些属性和方法创建表格的逻辑性更强，也更容易看懂，尽管技术上这两套代码都是正确的。

### 使用NodeList

**理解NodeList及其“近亲"NamedNodeMap和HTMLcollection，是从整体上透彻理解DOM的关键所在。**这三个集合都是“动态的"；换句话说，每当文档结构发生变化时，它们都会得到更新。因此，它们始终都会保存着最新、最准确的信息。从本质上说，所有NodeList对象都是在访问DOM文档时实时运行的查询。例如，下列代码会导致无限循环：

~~~javascript
var divs = document. getElementsByTagName ("div"),
i,
div;

for (i=0: i < divs. length; i++){
	div = document. createElement ("div"); 
    document.body.appendchild(div);
}
~~~

第一行代码会取得文档中所有< div>元素的HTMLCollection。由于这个集合是“动态的"，因此只要有新< div>元素被添加到页面中，这个元素也会被添加到该集合中。浏览器不会将创建的所有集合都保存在一个列表中，而是在下一次访问集合时再更新集合。结果，在遇到上例中所示的循环代码时，就会导致一个有趣的问题。每次循环都要对条件i < divs.length求值，意味着会运行取得所有< div>元素的查询。考虑到循环体每次都会创建一个新<div元素并将其添加到文档中，因此divs.length的值在每次循环后都会递增。既然i和divs.length每次都会同时递增，结果它们的值永远也不会相等。

如果想要迭代一个NodeList，最好是使用length属性初始化第二个变量，然后将迭代器与该变量进行比较，如下面的例子所示：

~~~javascript
var divs = document. getElementsByTagNane ("div"), 
    i, 
    len,
    div; 
for (i=0, len=divs.length; i<len; i++){
    div = document. createElement ("div");
    document. body. appendchild(div);
}
~~~

这个例子中初始化了第二个变量len。由于len中保存着对divs.length在循环开始时的一个快照，因此就会避免上一个例子中出现的无限循环问题。在本章演示迭代NodeList对象的例子中，使用的都是这种更为保险的方式。

一般来说，应该尽量减少访问NodeList的次数。因为每次访问NodeList，都会运行一次基于文档的查询。所以，可以考虑将从NodeList中取得的值缓存起来。

## 小结

![](读书笔记：JavaScript高级程序设计(第3版)/116.png)

# 第11章：DOM扩展(复习)

尽管DOM**作为API**已经非常完善了，但为了实现更多的功能，仍然会有**一些标准或专有的扩展**。2008年之前，浏览器中几乎所有的DOM扩展都是专有的。此后，W3C着手**将一些已经成为事实标准的专有扩展标准化并写入规范当中。**

对DOM的**两个主要的扩展是Selectors API（选择符API）和HTML5**，这两个扩展都源自开发社区，而将某些常见做法及AP1标准化一直是众望所归。此外，还有一个不那么引人瞩目的**Element Traversal**
**（元素遍历）规范**，为DOM添加了一些属性。虽然前述两个主要规范（特别是HTML5）已经涵盖了大量的DOM扩展，但专有扩展依然存在。本章也会介绍专有的DOM扩展。

## 选择符API

众多JavaScript库中最常用的一项功能，就是根据CSS选择符选择与某个模式匹配的DOM元素。
实际上，**jQuery（www.jquery.com）的核心就是通过CSS选择符查询DOM文档取得元素的引用，从而抛开了getElementById（）和getElementsByTagName（）。**

Selectors API（www.w3.org/TR/selectors-api/）是由w3C发起制定的一个标准，**致力于让浏览器原生支持CSS查询。所有实现这一功能的JavaScript库都会写一个基础的CSS解析器，然后再使用已有的DOM方法查询文档并找到匹配的节点。**尽管库开发人员在不知疲倦地改进这一过程的性能，但到头来都只能通过运行JavaScript代码来完成查询操作。**而把这个功能变成变成原生API之后，解析和树查询操作可以在浏览器内部通过编译后的代码来完成，极大地改善了性能。**

Selectors API Level 1的核心是两个方法：**querySelector（）和querySelectorAll（）**。在兼容的浏览器中，可以通过Document及Element类型的实例调用它们。目前已完全支持Selectors API Level 1的浏览器有IE 8+、Firefox 3.5+、Safari 3.1+、Chrome和Opera 10+。

### querySelector()方法

querySelector（）方法接收一个CSS选择符，返回与该模式匹配的**第一个元素**，如果没有找到四配的元素，返回**null**。请看下面的例子。

~~~css
 //取得body元素
 var body = document.querySelector("body");
 
 //取得ID为 "myDiv"的元素
 var myDiv = document.querySelector("#myDiv");
                              
//取得类名为 "selected"的第一个元素
var selected = document.querySelector(".selected");
                               
//取得类为 "button"的第一个图像元素
 var img = document.body.querySelector("img.button");
~~~

**通过Document类型调用queryselector（）方法时，会在文档元素的范围内查找匹配的元素。而通过Element类型调用queryselector（）方法时，只会在该元素后代元素的范围内查找匹配的元素。**

CSS选择符可以简单也可以复杂，视情况而定。如果传入了不被支持的选择符，querySelector（）会抛出错误。

### querySelectorAll()方法

querySelectorAll（）方法接收的参数与querySelector（）方法一样，都是一个CSS选择符，但**返回的是所有匹配的元素而不仅仅是一个元素。这个方法返回的是一个NodeList的实例。**

具体来说，**返回的值实际上是带有所有属性和方法的NodeList，而其底层实现则类似于一组元素的快照，而非不断对文档进行搜索的动态查询。**这样实现可以避免使用NodeList对象通常会引起的大多数性能问题。

只要传给querySelectorAl1（）方法的CSS选择符有效，该方法都会返回一个NodeList**对象**，而不管找到多少匹配的元素。如果没有找到匹配的元素，NodeList就是空的。

与querySelector（）类似，能够调用querySelectorAll（）方法的类型包括Document 、DocumentFragment和Element。下面是几个例子。

~~~css
//取得某<div>中的所有<em>元素（类似于getElementsByTagName（"em"））
var ems = document.getElementById（"myDiv"）.querySelectorAl1（"em"）；

//取得类为"selected"的所有元素
var selecteds = document.queryselectorAll（".selected"）;

//取得所有<p>元素中的所有<strong>元素
var strongs = document.queryselectorAll（"p strong"）;
~~~

要取得返回的NodeList中的每一个元素，可以使用**item()方法**，也可以使用**方括号语法**，比如：

~~~javascript
var i，len，strong；
for（i=0,len=strongs.length;i<len；i++）{
	strong = strongs[i];	//或者strongs.item（i）
	strong.className ="important"；
}
~~~

同样与querySelector（）类似，如果传入了浏览器不支持的选择符或者选择符中有语法错误，queryselectorAll（）会抛出错误。

### matchesSelector（）方法

Selectors API Level 2规范为Element类型新增了一个方法matchesselector（）。这个方法接收一个参数，即CSS选择符，如果调用元素与该选择符匹配，返回true；否则，返回false。看例子。

~~~css
if (document.body.matchesSelector {"body . pagel")){
    //true
    }
~~~

在取得某个元素引用的情况下，使用这个方法能够方便地检测它是否会被queryselector（）或queryselectorAl1（）方法返回。

截至2011年年中，还没有浏览器支持matchesSelector（）方法；不过，也有一些实验性的实现。
IE 9+通过msMatchesSelector（）支持该方法，Firefox 3.6+通过mozMatchesselector（）支持该方法，Safari 5+和Chrome通过webkitMatchesselector支持该方法。因此，如果你想使用这个方法，最好是编写一个包装函数。

~~~css
 function matchesSelector(element, selector){
      if (element.matchesSelector){
           return element.matchesSelector(selector);
      } else if (element.msMatchesSelector){
           return element.msMatchesSelector(selector);
      } else if (element.mozMatchesSelector){
           return element.mozMatchesSelector(selector);
      } else if (element.webkitMatchesSelector){
           return element.webkitMatchesSelector(selector);
      } else {
           throw new Error("Not supported.");
      }
 }
        
if (matchesSelector(document.body, "body.page1")){
       //执行操作
 }
~~~

## 元素遍历

对于元素间的空格，IE9及之前版本不会返回文本节点，而其他所有浏览器都会返回文本节点。这样，就导致了在使用chilaNodes和firstChila等属性时的行为不一致。为了弥补这一差异，而同时又保持DOM规范不变，Element Traversal规范（www.w3.org/TR/ElementTraversal/）新定义了一组属性。
Element Traversal API为DOM元素添加了以下5个属性。

~~~
childElementCount：返回子元素（不包括文本节点和注释）的个数。
firstElementChild：指向第一个子元素；firstChild的元素版。
lastElementChild：指向最后一个子元素；lastChila的元素版。
previousElementSibling：指向前一个同辈元素；previousSibling的元素版。
nextElementSibling：指向后一个同辈元素；nextSibling的元素版。
~~~

支持的浏览器为DOM元素添加了这些属性，利用这些元素不必担心空白文本节点，从而可以更方便地查找DOM元素了。

下面来看一个例子。过去，要跨浏览器遍历某元素的所有子元素，需要像下面这样写代码。

~~~javascript
var i，
	1en, 
    child = element.firstChild；
while（child ！= element.lastChild(){
	if（child.nodeType ==1）（ //检查是不是元素
    	processChild（child）;
	}
	child = child.nextSibling；
}
~~~

而使用Element Traversal新增的元素，代码会更简洁。

~~~javascript
var i，
	1en, 
    child = element.firstElementChild；
while（child ！= element.lastElementChild(){
    	processChild（child）;	//已知其是元素
	   child = child.nextElementSibling；
}
~~~

支持Element Traversal规范的浏览器有IE 9+，Firefox 3.5+，Safari 4+，、Chrome和Opera 10+。

## HTML5（看了一点）

对于传统HTML而言，HTMLS是一个**叛逆**。所有之前的版本对JavaScript接口的描述都不过三言两语，**主要篇幅都用于定义标记**，与JavaScript相关的内容一概交由DOM规范去定义。

而HTMLS规范则围绕**如何使用新增标记**定义了大量JavaScript API，**其中一些API与DOM重叠**，定义了浏览器应该支持的DOM扩展。

> 因为HTML5涉及的面非常广，本节只讨论与**DOM节点**相关的内容。HTML5的其他相关内容将在本书其他章节中穿插介绍。

### 与类相关的补充

HTML4在Web开发领域得到广泛采用后导致了一个很大的变化，即**class属性用得越来越多**，**一方面可以通过它为元素添加样式，另一方面还可以用它表示元素的语义。**于是，自然就有很多JavaScript代码会来操作CSS类，比如动态修改类或者搜索文档中具有给定类或给定的一组类的元素，等等。为了让开发人员适应并增加对class属性的新认识，**HTML5新增了很多API，致力于简化CSS类的用法**。

1. **getElementsByClassName（）方法**

   HTML5添加的getElementsByClassName（）方法是最受人欢迎的一个方法，**可以通过document对象及所有HTML元素调用该方法。**这个方法最早出现在JavaScript库中，是通过既有的DOM功能实现的，而**原生的实现具有极大的性能优势。**

   getElementsByClassName（）方法**接收一个参数，即一个包含一或多个类名的字符串，返回带有指定类的所有元素的NodeList。传入多个类名时，类名的先后顺序不重要。**来看下面的例子。

   ~~~javascript
   //取得所有类中包含"username"和"current"的元素，类名的先后顺序无所谓
   var allcurrentUsernames = document.getElementsByClassName（"username current"）；
   
   //取得ID为"myDiv"的元素中带有类名"selected"的所有元素
   var selected =document.getElementById（"myDiv"）.getElementsByClassName（"selected"）
   ~~~

   调用这个方法时，只有位于调用元素**子树**中的元素才会返回。在**document对象上**调用getElementsByClassName（）始终会返回与类名匹配的**所有元素**，在**元素上**调用该方法就只会返回**后代元素中匹配的元素**。

   > 在document对象上调用和元素上调用getElementsByClassName()方法返回的元素是不一样的

   [Document.getElementsByClassName()方法API介绍](<https://developer.mozilla.org/zh-CN/docs/Web/API/Document/getElementsByClassName>)

   使用这个方法可以**更方便地为带有某些类的元素添加事件处理程序，从而不必再局限于使用ID或标签名**。不过别忘了，因为**返回的对象是NodeList**，所以使用这个方法与使用getElementsByTagName（）
   以及其他返回NodeList的DOM方法都具有同样的性能问题。

   支持getElementsByClassName（）方法的浏览器有IE 9+，Firefox 3+、Safari 3.1+，Chrome和Opera 9.5+。

2. **classList属性**（没看）

   在操作类名时，需要通过className属性添加、删除和替换类名。因为className中是一个字符串，所以即使只修改字符串一部分，也必须每次都设置整个字符串值。比如，以下面的HTML代码为例。

   ~~~javascript
   <div class="bd user disabled">...</div>
   ~~~

   这个< div>元素一共有三个类名。要从中删除一个类名，需要把这三个类名拆开，删除不想要的那个，然后再把其他类名拼成一个新字符串。请看下面的例子。

   ~~~javascript
   //删除"user"类
   
   //首先，取得类名字符串并拆分成数组
   var classNames = div.className.split（/\s+/）；
   
   //找到要删的类名
   var pos = -1，
   	i,
   	len;
   for（i=0，len=classNames.length;i < len；i++）{
   	if（classNames[i]=="user"）{
   		pos =i；
           break；
       }
   }
   //删除类名
   classNames.splice（i，1）；
   
   //把剩下的类名耕成字符串并重新设置
   div.className = classNames.join（""）；
   ~~~

   为了从< div>元素的class属性中删除"user"，以上这些代码都是必需的。必须得通过类似的算法替换类名并确认元素中是否包含该类名。添加类名可以通过拼接字符串完成，但必须要通过检测确定不会多次添加相同的类名。很多JavaScript库都实现了这个方法，以简化这些操作。

   HTML5新增了一种操作类名的方式，可以让操作更简单也更安全，那就是为所有元素添加classList属性。这个classList属性是新集合类型DOMTokenList的实例。与其他DOM集合类似，DOMTokenList有一个表示自己包含多少元素的length属性，而要取得每个元素可以使用item（）方法，也可以使用方括号语法。此外，这个新类型还定义如下方法。

   ~~~javascript
   adda（value）：将给定的字符串值添加到列表中。如果值已经存在，就不添加了。
   contains（value）：表示列表中是否存在给定的值，如果存在则返回true，否则返回false remove（value）：从列表中删除给定的字符串。
   toggle（va lue）：如果列表中已经存在给定的值，删除它；如果列表中没有给定的值，添加它。
   ~~~

   这样，前面那么多行代码用下面这一行代码就可以代替了：

   ~~~javascript
   div.classList.remove ("user");
   ~~~

   以上代码能够确保其他类名不受此次修改的影响。其他方法也能极大地减少类似基本操作的复杂性，如下面的例子所示。

   ~~~javascript
   //删除"disabied"类
   div.classList.remove（"disabled"）;
   
   //添加“current"类
   div.classList.add（"current"）；
   
   //切换"user"类
   div.classList.toggle（"user"）；
   
   //确定元素中是否包含既定的类名
   if（div.classList.contains（"bd"）&& !div.classList.contains（"disabled")){
   	//执行操价
   }
       //速代类名
   for（var i=o，len=div.classList.length;i < len；i++）{
   	dosomething（div.classList[i]）；
   }
   ~~~

   有了classList属性，除非你需要全部删除所有类名，或者完全重写元素的class属性，否则也就用不到className属性了。

   支持classList属性的浏览器有Firefox 3.6+和Chrome。

### 焦点管理

   HTMLS也添加了辅助管理DOM焦点的功能。首先就是document.activeElement属性，这个属性始终会引用DOM中当前获得了焦点的元素。元素获得焦点的方式有页面加载、用户输入（通常是通过按Tab键）和在代码中调用focus（）方法。来看几个例子。

   ~~~javascript
   var button = document. getElementById ("myButton");
   button.focus();
   alert (document.activeElement === button); //true
   ~~~

   默认情况下，文档刚刚加载完成时，document.activeBlement中保存的是document.body元素的引用。文档加载期间，document.activeElement的值为null。

   另外就是新增了document.hasFocus（）方法，这个方法用于确定文档是否获得了焦点。

   ~~~javascript
   var button = document.getElementById("myButton");
   button.focus (); 
   alert (document.hasFocus ()); //true
   ~~~

   通过检测文档是否获得了焦点，可以知道用户是不是正在与页面交互。

   查询文档获知哪个元素获得了焦点，以及确定文档是否获得了焦点，这两个功能最重要的用途是提高Web应用的无障碍性。无障碍web应用的一个主要标志就是恰当的焦点管理，而确切地知道哪个元素获得了焦点是一个极大的进步，至少我们不用再像过去那样靠猜测了。

   实现了这两个属性的浏览器的包括1E 4+，Firefox 3+，Safari 4+、Chrome和Opera 8+。

### HTMLDocument的变化

HTMLS扩展了HTMLDocument，增加了新的功能。与HTML5中新增的其他DOM扩展类似，这些变化同样基于那些已经得到很多浏览器完美支持的专有扩展。所以，尽管这些扩展被写人标准的时间相对不长，但很多浏览器很早就已经支持这些功能了。

1. readyState属性

   1E4最早为document对象引入了readystate属性。然后，其他浏览器也都陆续添加这个属性，最终HTMLS把这个属性纳入了标准当中。Document的readystate属性有两个可能的值：

   ~~~
   loading，正在加载文档；
   complete，已经加载完文档。
   ~~~

   使用document.readystate的最恰当方式，就是通过它来实现一个指示文档已经加载完成的指示器。在这个属性得到广泛支持之前，要实现这样一个指示器，必须借助onload事件处理程序设置一个标签，表明文档已经加载完毕。document.readyState属性的基本用法如下。

   ~~~javascript
   if（document.readystate =="complete"）{
   	//执行操作
   }
   ~~~

   支持readystate属性的浏览器有IE4+，Firefox 3.6t，Safari，Chrome和Opera 9+。

2. 兼容模式

   自从IE6开始区分渲染页面的模式是标准的还是混杂的，检测页面的兼容模式就成为浏览器的必要功能。IE为此给document添加了一个名为compatMode的属性，这个属性就是为了告诉开发人员浏览器采用了哪种渲染模式。就像下面例子中所展示的那样，在标准模式下，document.compatMode的值等于"CSS1compat"，而在混杂模式下，document.compatMode的值等于"BackCompat"。

   ~~~javascript
   if (document.compatMode ="CSS1Compat"){
   	alert ("Standards mode");
   } else {
   	alert ("ouirks mode");
   }
   ~~~

   后来，陆续实现这个属性的浏览器有Firefox，Safari 3.1+，Opera和Chrome，最终，HTML5也把这个属性纳入标准，对其实现做出了明确规定。

3. head属性

   作为对document.body引用文档的< body>元素的补充，HTML5新增了document.head属性，引用文档的< head>元素。要引用文档的< head>元素，可以结合使用这个属性和另一种后备方法。

   ~~~javascript
   var head = document.head || document . getElementsByTagName ("head") [0];
   ~~~

   如果可用，就使用document.head，否则仍然使用getElementsByTagName（）方法。

   实现document.head属性的浏览器包括Chrome和Safari 5。

### 字符集属性

HTMLS新增了几个与文档字符集有关的属性。其中，charset属性表示文档中实际使用的字符集，也可以用来指定新字符集。默认情况下，这个属性的值为"UTF-16"，但可以通过<meta>元素、响应头部或直接设置charset属性修改这个值。来看一个例子。

~~~javascript
alert (document. charset); //"UTF-16"
document. charset = "UTF-8";
~~~

另一个属性是defaultCharset，表示根据默认浏览器及操作系统的设置，当前文档默认的字符集应该是什么。如果文档没有使用默认的字符集，那charset和defaultCharset属性的值可能会不一样，例如：

~~~javascript
if (document.charset != document.defaultCharset){
	alert ("Custom character set being used.");
}
~~~

通过这两个属性可以得到文档使用的字符编码的具体信息，也能对字符编码进行准确地控制。运行适当的情况下，可以保证用户正常查看页面或使用应用。

支持document.charset属性的浏览器有IE、Firefox.Safari、Opera和Chrome。支持document.defaultCharset属性的浏览器有1E，Safari和Chrome。

### 自定义数据属性

HTML5规定可以为元素添加非标准的属性，但要添加前缀data-，目的是为元素提供与渲染无关的信息，或者提供语义信息。这些属性可以任意添加、随便命名，只要以data-开头即可。来看一个例子。

~~~javascript
<div id="myDiv" data-appld="12345" data-myname="Nicholas"></div>
~~~

添加了自定义属性之后，可以通过元素的dataset属性来访问自定义属性的值。dataset属性的值是DOMStringMap的一个实例，也就是一个名值对儿的映射。在这个映射中，每个data-name形式的属性都会有一个对应的属性，只不过属性名没有data-前缀（比如，自定义属性是data-myname，那映射中对应的属性就是myname），还是看一个例子吧。

~~~javascript
//本例中使用的方法仅用于演示

var div = document.getElementById（"myDiv"）;

//取得自定义属性的值
var appId = div.dataset.appId;
var myName  div.dataset.myName;

//设置值
div.dataset.appId = 23456；
div.dataset.myname ="Michael";

//没有"myname"值呢？
if（div.dataset.myname）{
    alert ("Hello, "+ div. dataset.myname);
}
~~~

如果需要给元素添加一些不可见的数据以便进行其他处理，那就要用到自定义数据属性。在跟踪链接或混搭应用中，通过自定义数据属性能方便地知道点击来自页面中的哪个部分。
在编写本书时，支持自定义数据属性的浏览器有Firefox 6+和Chrome。

### 插入标记(看完)

虽然DOM为操作节点提供了细致入微的控制手段，但在**需要给文档插入大量新HTML标记的情况下，通过DOM操作仍然非常麻烦，因为不仅要创建一系列DOM节点，而且还要小心地按照正确的顺序把它们连接起来**。相对而言，**使用插入标记的技术，直接插入HTML字符串不仅更简单，速度也更快**。以下与插入标记相关的DOM扩展已经纳入了HTML5规范。

1. **innerHTML属性**

   在**读模式**下，innerHTML属性返回与调用元素的所有子节点（包括元素、注释和文本节点）对应的HTML标记。在**写模式**下，innerHTML会根据指定的值创建新的DOM树，然后用这个DOM树完全替换调用元素原先的所有子节点。下面是一个例子。

   ~~~javascript
   <div id="content">
   	<p>This is a <strong>paragraph</strong> with a list following it.</p>
   	<ul>
   		<li>item 1</li>
   		<li>iter 2</1i>
   		<li>iten 3</1i>
   	</ul>
   </div>
   ~~~

   对于上面的< div>元素来说，它的innerHTML属性会返回如下字符串。

   ~~~javascript
   <p>This is a <strong>paragraph</strong> with a list following it.</p>
   	<ul>
   		<li>item 1</li>
   		<li>iter 2</1i>
   		<li>iten 3</1i>
   	</ul>
   ~~~
   但是，不同浏览器返回的文本格式会有所不同。IE和Opera会将所有标签转换为大写形式，而Safari、Chrome和Firefox则会原原本本地按照原先文档中（或指定这些标签时）的格式返回HTML，包括空格和缩进。不要指望所有浏览器返回的innerHTML值完全相同。

   在写模式下，innerHTML的值会被解析为DOM子树，替换调用元素原来的所有子节点。因为它的值被认为是HTML，所以其中的所有标签都会按照浏览器处理HTML的标准方式转换为元素（同样，这里的转换结果也因浏览器而异），如果设置的值仅是文本而没有HTML标签，那么结果就是设置纯文本，如下所示。

   ~~~javascript
   div.innerHTML = "Hello world!";
   ~~~

   为innerHTML设置的包含HTML的字符串值与解析后innerHTML的值大不相同。来看下面的例子。

   ~~~javascript
   div. innerHTML = "Hello & welcome, <b>\"reader\"!</b>";
   ~~~

   以上操作得到的结果如下：

   ~~~javascript
   <div id="content">Hello &amp; welcome, <b>&quot;reader&quot;!</b></div>
   ~~~

   设置了innerHTML之后，可以像访问文档中的其他节点一样访问新创建的节点。

   > 为innerHTML设置HTML字符串后，浏览器会将这个字符串解析为相应的DOM树。因此设置了innerHTML之后，再从中读取HTML字符串，会得到与设置时不一样的结果。原因在于返回的字符串是根据原始HTML字符串创建的DOM树经过序列化之后的结果。

   使用innerHTML属性也有一些限制。比如，在大多数浏览器中，通过innerHTML，插入< script>
   元素并不会执行其中的脚本。IE8及更早版本是唯一能在这种情况下执行脚本的浏览器，但必须满足一些条件。一是必须为< script>元素指定defer属性，二是< script>元素必须位于（微软所谓的）“有作用域的元素”（scoped element）之后。< script>元素被认为是“无作用域的元素”（NoScope element），也就是在页面中看不到的元素，与< style>元素或注释类似。如果通过innerHTML插入的字符串开头就是一个“无作用域的元素”，那么IE会在解析这个字符串前先删除该元素。换句话说，以下代码达不到目的：

   ~~~javascript
   div.innerHTML ="<script defer>alert（'hi'）;<\/script>"；//无效
   ~~~

   此时，innerHTML字符串一开始（而且整个）就是一个“无作用域的元素”，所以这个字符串会变成空字符串。如果想插人这段脚本，必须在前面添加一个“有作用域的元素”，可以是一个文本节点，也可以是一个没有结束标签的元素如< input>。例如，下面这几行代码都可以正常执行：

   ~~~javascript
   div.innerHTML  = "_<script defer>alert (' hi');<\/script>"; 
   div.innerHTMI  = "<div>& nbsp;</div><script defer>alert (' hi');<\/script>"; 
   div.innerHTML  = "<input type=\"hidden\"><script defer>alert ('hi');<\/script>";
   ~~~

   第一行代码会在< script>元素前插入一个文本节点。事后，为了不影响页面显示，你可能需要移除这个文本节点。第二行代码采用的方法类似，只不过使用的是一个包含非换行空格的<div元素。如果仅仅插入一个空的< div>元素，还是不行；必须要包含一点儿内容，浏览器才会创建文本节点。同样，为了不影响页面布局，恐怕还得移除这个节点。第三行代码使用的是一个隐藏的< input>域，也能达到相同的效果。不过，由于隐藏的< input>域不影响页面布局，因此这种方式在大多数情况下都是首选。

   大多数浏览器都支持以直观的方式通过innerHTML插入< style>元素，例如：

   ~~~javascript
   div.innerHTML = "<style type=\"text/css\">body (background-color: red; )</style>";
   ~~~

   但在IE8及更早版本中，< style>也是一个“没有作用域的元素”，因此必须像下面这样给它前置一个“有作用域的元素"：

   ~~~javascript
   div.innerHML ="<style type-\"text/css\">body [ background-color: red; )</style>"; div.removechild(div. firstchila);
   ~~~

   **并不是所有元素都支持innerHTML属性**。不支持innerHTML的元素有：< col>、< colgroup>、< frameset>、< head>、< html>、< style>、< table>、< tbody>、< thead>、< tfoot>和< tr>。此外，在1E8及更早版本中，< title>元素也没有innerHTML属性。

   > Firefox对在内容类型为application/xhtmi+xml的XHTML文档中设置innerHTML有严格的限制。在XHTML文档中使用innerHTML时，XHTML代码必须完全符合要求。如果代码格式不正确，设置innerHTML将会静默地失败。

   无论什么时候，只要使用innerHTML从外部插入HTML，都应该首先以可靠的方式处理HTML
   。IE8为此提供了window.tostaticHTML（）方法，这个方法接收一个参数，即一个HTML字符串；返回一个经过无害处理后的版本-从源HTML中删除所有脚本节点和事件处理程序属性。下面就是一个例子：

   ~~~javascript
   var text = "<a href=\"#\"onclick=\"alert (' hi')\">Click Me</a>"; 
   var sanitized = window. tostaticHTML (text);//Internet Explorer 8 only 
   alert (sanitized); 	//"<a href=\"#\">Click Me</a>"
   ~~~

   这个例子将一个HTML链接字符申传给了tostaticHTML（1）方法，得到的无害版本中去掉了onclick属性。虽然目前只有1E8原生支持这个方法，但我们还是建议读者在通过innerHTM插入代码之前，尽可能先手工检查一下其中的文本内容。

2. outerHTML属性

   在读模式下，outerHTML返回调用它的元素及所有子节点的HTML标签。在写模式F，outerHTML会根据指定的HTML字符串创建新的DOM子树，然后用这个DOM子树完全替换调用元素。下面是一个例子。

   ~~~javascript
   <div id="content">
        <p>This is a <strong>paragraph</strong> with a list following it.</p>
        <ul>
               <li>Item 1</li>
               <li>Item 2</li>
               <li>Item 3</li>
        </ul>
   </div>
   ~~~

   如果在< div>元素上调用outerHTML，会返回与上面相同的代码，包括< div>本身。不过，由于浏览器解析和解释HTML标记的不同，结果也可能会有所不同。（这里的不同与使用innerHTML属性时存在的差异性质是一样的。）

   使用outerHTML属性以下面这种方式设置值：

   ~~~javascript
   div.outerHTML = "<p>This is a paragraph.</p>";
   ~~~

   这行代码完成的操作与下面这些DOM脚本代码一样：

   ~~~javascript
   var p = document.createElement ("p");
   p.appendChild (document.createTextNode ("This is a paragraph.")); 
   div.parentNode.replacechild(p, div);
   ~~~

   结果，就是新创建的< p>元素会取代DOM树中的< div>元素。

   支持outerHTMr，属性的浏览器有IE4+、Safari 4+、Chrome和Opera 8+，Firefox 7及之前版本都不支持outerHTML属性。

3. insertAdjacentHTML()方法

   插入标记的最后一个新增方式是insertAdjacentHTML（）方法。这个方法最早也是在1E中出现的，它接收两个参数：插入位置和要插入的HTML文本。第一个参数必须是下列值之一：

   ~~~javascript
   "beforebegin"，在当前元素之前插入一个紧邻的同辈元素；
   "afterbegin"，在当前元素之下插入一个新的子元素或在第一个子元素之前再插入新的子元素；
   "beforeen"，在当前元素之下插入一个新的子元素或在最后一个子元素之后再插入新的子元素；
   "afterend"，在当前元素之后插入一个紧邻的同辈元素。
   ~~~

   注意，这些值都必须是小写形式。第二一HTML串（与innerHTML和outerHTM的值相同），如果浏览器无法解析该字符串，就会抛出错误。以下是这个方法的基本用法示例。

   ~~~javascript
   //作为前一个同單元素插入
   element.insertAdjacentHTML（"beforebegin"，"<p>Hello world！</p>"）；
   
   //作为第一个子元素插入
   element.insertAdjacentHTML（"afterbegin"，"<p>Hel1o world！</p>"）；
   
   //作为最后一个子元素插入
   element.insertAdjacentHTML（"beforeend"，"<p>Hello world！</p>"）；
   
   //作为后一个同辈元素插入
   element.insertAdjacentHTML（"afterend"，"<p>Hel1o world！</p>"）；
   ~~~

   支持insertAdjacentHTML（）方法的浏览器有IE，Firefox 8+，Safari，Opera和Chrome。

4. 内存与性能问题

   使用本节介绍的方法替换子节点可能会导致浏览器的内存占用问题，尤其是在IE中，问题更加明显。在删除带有事件处理程序或引用了其他JavaScript对象子树时，就有可能导致内存占用问题。假设某个元素有一个事件处理程序（或者引用了一个Javascript对象作为属性），在使用前述某个属性将该元素从文档树中删除后，元素与事件处理程序（或JavaScript对象）之间的绑定关系在内存中并没有一并删除。如果这种情况频繁出现，页面占用的内存数量就会明显增加。因此，在使用innerHTML outerHTML属性和insertAdjacentHML（）方法时，最好先手工删除要被替换的元素的所有事件处理程序和JavaScript对象属性（第13章将进一步讨论事件处理程序）
   。

   不过，使用这几个属性-特别是使用innerHTML，仍然还是可以为我们提供很多便利的。一般来说，在插入大量新HTML标记时，使用innerHTML属性与通过多次DOM操作先创建节点再指定它们之间的关系相比，效率要高得多。这是因为在设置innerHTML或outerHTML时，就会创建一个HTML解析器。这个解析器是在浏览器级别的代码（通常是C+编写的）基础上运行的，因此比执行JavaScript快得多。不可避免地，创建和销毁HTML解析器也会带来性能损失，所以最好能够将设置innerHTMI或outerHTML的次数控制在合理的范围内。例如，下列代码使用innerHTML，创建了很多列表项：

   ~~~javascript
   for（var i=0，len=values.length；i < len；i++）{
   	ul.innerHTML +="<ii>"+ values[i]+"</li>"；//要避免这种频繁操作！！
   }
   ~~~

   这种每次循环都设置一次innerHTME的做法效率很低。而且，每次循环还要从innerHTML中读取一次信息，就意味着每次循环要访问两次innerHTML，最好的做法是单独构建字符串，然后再一次性地将结果字符串赋值给innerHTML，像下面这样：

   ~~~javascript
   var itemsHtml = ";
   for (var i=0, len-values. length; i s len; i++)
   	itemHtml += "<1i>"+ values[1] +"</1i>"
   ul. innerHML = itemaHtml;
   ~~~

   这个例子的效率要高得多，因为它只对innerHTML执行了一次赋值操作。

### scrollIntoView（）方法

如何滚动页面也是DOM规范没有解决的一个问题。为了解决这个问题，浏览器实现了一些方法，以方便开发人员更好地控制页面滚动。在各种专有方法中，HTMLS最终选择了scrollIntoView（）作为标准方法。

scroll IntoView（）可以在所有HTML元素上调用，通过滚动浏览器窗口或某个容器元素，调用元素就可以出现在视口中。如果给这个方法传入true作为参数，或者不传入任何参数，那么窗口滚动之后会让调用元素的顶部与视口顶部尽可能平齐。如果传入false作为参数，调用元素会尽可能全部出现在视口中，（可能的话，调用元素的底部会与视口顶部平齐。）不过顶部不一定平齐，例如：

~~~javascript
//让元素可见
document.forms[0].scrollIntoview（）；
~~~

当页面发生变化时，一般会用这个方法来吸引用户的注意力。实际上，为某个元素设置焦点也会导致浏览器滚动并显示出获得焦点的元素。

支持scrollIntoview（）方法的浏览器有IE、Firefox、Safari和Opera。

## 专有扩展

虽然所有浏览器开发商都知晓坚持标准的重要性，但在发现某项功能缺失时，这些开发商都会一如既往地向DOM中添加专有扩展，以弥补功能上的不足。表面上看，这种各行其事的做法似乎不太好，但实际上专有扩展为Web开发领域提供了很多重要的功能，这些功能最终都在HTMLS规范中得到了标准化。

即便如此，仍然还有大量专有的DOM扩展没有成为标准。但这并不是说它们将来不会被写进标准，而只是说在编写本书的时候，它们还是专有功能，而且只得到了少数浏览器的支持。

### 文档模式

IE8引入了一个新的概念叫“文档模式"（document mode）。页面的文档模式决定了可以使用什么功能。换句话说，文档模式决定了你可以使用哪个级别的css，可以在Javascript中使用哪些API，以及如何对待文档类型（doctype），到了IE9，总共有以下4种文档模式。

~~~javascript
IE5：以混杂模式渲染页面（IE5的默认模式就是混杂模式），1E8及更高版本中的新功能都无法使用。
1E7：以1E7标准模式渲染页面。IE8及更高版本中的新功能都无法使用。
1E8：以1E8标准模式渲染页面。1E8中的新功能都可以使用，因此可以使用Selectors AP1、更多Css2级选择符和某些CSs3功能，还有一些HTMLS的功能。不过1E9中的新功能无法使用。
1E9：以IE9标准模式渲染页面。IE9中的新功能都可以使用，比如ECMAScript5、完整的Css3以及更多HTMLS功能。这个文档模式是最高级的模式。
~~~

要理解IE8及更高版本的工作原理，必须理解文档模式。

要强制浏览器以某种模式渲染页面，可以使用HTTP头部信息x-UA-Compatible，或通过等价的< meta>标签来设置：

~~~javascript
<meta http-equivy="x-UA-Compatible" content="IE-IEVersion">
~~~

注意，这里IE的版本（IEVersion）有以下一些不同的值，而且这些值并不一定与上述4种文档模式对应。

~~~javascript
Edge：始终以最新的文档模式来渲染页面。忽略文档类型声明。对于1E8，始终保持以1E8标准模式渲染页面。对于1E9，则以IE9标准模式渲染页面。
Emulate1E9：如果有文档类型声明，则以IE9标准模式渲染页面，否则将文档模式设置为IE5
Emulate1E8：如果有文档类型声明，则以IE8标准模式渲染页面，否则将文档模式设置为IE5
Emulate1E7：如果有文档类型声明，则以IE7标准模式渲染页面，否则将文档模式设置为IE5
9：强制以IE9标准模式渲染页面，忽略文档类型声明。
8：强制以IE8标准模式渲染页面，忽略文档类型声明。
7：强制以1E7标准模式渲染页面，忽略文档类型声明。
5：强制将文档模式设置为IE5，忽略文档类型声明。
~~~

比如，要想让文档模式像在IE7中一样，可以使用下面这行代码：

~~~javascript
<meta http-equiv-"x-UA-Compatible" content="IE-EmulatelE7>
~~~

如果不打算考虑文档类型声明，而直接使用1E7标准模式，那么可以使用下面这行代码：

~~~javascript
<meta http-equiv="X-UA-Compatible" content="IE=7">
~~~

没有规定说必须在页面中设置X-UA-Compatible。默认情况下，浏览器会通过文档类型声明来确定是使用最佳的可用文档模式，还是使用混杂模式。

通过document.documentMode属性可以知道给定页面使用的是什么文档模式。这个属性是1E8中新增的，它会返回使用的文档模式的版本号（在IE9中，可能返回的版本号为5，7，8、9）：

~~~javascript
var mode = document.documentMode;
~~~

知道页面采用的是什么文档模式，有助于理解页面的行为方式。无论在什么文档模式下，都可以访问这个属性。

### children属性

由于1E9之前的版本与其他浏览器在处理文本节点中的空白符时有差异，因此就出现了children属性。这个属性是HTMLCollection的实例，只包含元素中同样还是元素的子节点。除此之外，children属性与childNodes没有什么区别，即在元素只包含元素子节点时，这两个属性的值相同。
下面是访问children属性的示例代码：

~~~javascript
var childcount = element.children.length; 
var firstChild = element.children[0];
~~~

支持children属性的浏览器有IES，Firefox 3.5，Safari 2（但有bug），Safari 3（完全支持）、Opera8和Chrome（所有版本），1E8及更早版本的children属性中也会包含注释节点，但IE9之后的版本则只返回元素节点。

### contains()方法

在实际开发中，经常需要知道某个节点是不是另一个节点的后代。IE为此率先引入了contains（）
方法，以便不通过在DOM文档树中查找即可获得这个信息。调用contains（）方法的应该是祖先节点，也就是搜索开始的节点，这个方法接收一个参数，即要检测的后代节点。如果被检测的节点是后代节点，该方法返回true；否则，返回false。以下是一个例子：

~~~~jinja2
alert {document.documentElement.contains (document.body)};  //true
~~~~

使用DOM Level 3 compareDocumentPosition（）也能够确定节点间的关系。支持这个方法的浏览器有IE9+.Firefox.Safari.Opera 9.5+和Chrome。如前所述，这个方法用于确定两个节点间的关系，返回一个表示该关系的位掩码（bitmask），下表列出了这个位掩码的值。

![](读书笔记：JavaScript高级程序设计(第3版)/117.png)

为模仿contains（）方法，应该关注的是掩码16，可以对compareDocumentPosition（）的结果执行按位与，以确定参考节点（调用compareDocument Position（）方法的当前节点）是否包含给定的节点（传入的节点），来看下面的例子：

~~~javascript
var result = document. documentElement.compareDocumentPosition (document.body); alert(!! (result & 16));
~~~

执行上面的代码后，结果会变成20（表示“居后”的4加上表示“被包含”的16）。对掩码16执行按位操作会返同一个非零数值，而两个逻辑非操作符会将该数值转换成布尔值。

使用一些浏览器及能力检测，就可以写出如下所示的一个通用的contains函数：

~~~javascript
function contains(refNode, otherNode){
      if (typeof refNode.contains == "function" && 
             (!client.engine.webkit || client.engine.webkit >= 522)){
           return refNode.contains(otherNode);
      } else if (typeof refNode.compareDocumentPosition == "function"){
           return !!(refNode.compareDocumentPosition(otherNode) & 16);
      } else {
            var node = otherNode.parentNode;
              do {
                  if (node === refNode){
                     return true;
                  } else {
                      node = node.parentNode;
                  }
              } while (node !== null);
                return false;
       }
}
~~~

这个函数组合使用了三种方式来确定一个节点是不是另一个节点的后代。两数的第一个参数是参考节点，第二个参数是要检查的节点。在函数体内，首先检测refNode中是否存在contains（）方法（能力检测）。这一部分代码还检查了当前浏览器所用的Webkit版本号。如果方法存在而且不是webKit
（！client.engine.webkit），则继续执行代码。否则，如果浏览器是Webkit且至少是Safari 3（WebKit版本号为522或更高），那么也可以继续执行代码。在webkit版本号小于522的Safari浏览器中，contains（）方法不能正常使用。

接下来检查是否存在compareDocument Position（）方法，而函数的最后一步则是自otherNode开始向上遍历DOM结构，以递归方式取得parentNode，并检查其是否与refNode相等。在文档树的顶端，parentNode的值等于null，于是循环结束。这是针对旧版本Safari设计的一个后备策略。

### 插入文本（复习）

前面介绍过，**IE原来专有的插入标记的属性innerHTML和outerHTML已经被HTML5纳入规范**。
但另外两个插入文本的专有属性则没有这么好的运气。**这两个没有被HTML5看中的属性是innerText和outerText**。

1. **innerText属性**（看完）

   通过innertText属性可以操作元素中包含的所有**文本内容**，**包括子文档树中的文本**。在通过innerText读取值时，它会按照**由浅入深**的顺序，将子文档树中的所有文本拼接起来。在通过innerText**写入值**时，**结果会删除元素的所有子节点，插人包含相应文本值的文本节点**。来看下面这个HTML代码示例。

   ~~~javascript
   <div id="content">
           <p>This is a <strong>paragraph</strong> with a list following it.</p>
           <ul>
               <li>Item 1</li>
               <li>Item 2</li>
               <li>Item 3</li>
           </ul>
       </div>
   ~~~

   对于这个例子中的<div元素而言，其innerText属性会返回下列字符串：

   ~~~javascript
   This is a paragraph with a list following it.
   Item 1
   Item 2
   Item 3
   ~~~

   由于不同浏览器处理空白符的方式不同，因此输出的文本可能会也可能不会包含原始HTML代码中的缩进。

   使用innerText属性设置这个< div>元素的内容，则只需一行代码：

   ~~~javascript
   div.innerText = "Hello World!"
   ~~~

   执行这行代码后，页面的HTML代码就会变成如下所示。

   ~~~javascript
   <div id="content ">Hello world!</div>
   ~~~

   **设置innerText属性移除了先前存在的所有子节点，完全改变了DOM子树**。此外，**设置innerText属性的同时，也对文本中存在的HTML语法字符（小于号、大于号、引号及和号）进行了编码**。再看一个例子。

   ~~~javascript
   div.innerText = "Hello & welcome, <b>\"reader\"!</b>";
   ~~~

   运行以上代码之后，会得到如下所示的结果。

   ~~~javascript
   <div id="content ">Hello &amp; welcome, &lt;b&gt;&quot;reader&quot;!&lt;/b&gt;</div>
   ~~~

   **设置innerText永远只会生成当前节点的一个子文本节点，而为了确保只生成一个子文本节点，就必须要对文本进行HTML编码。**利用这一点，**可以通过innerText属性过滤掉HTML标签**。方法是将innerText设置为等于innerText,**这样就可以去掉所有HTML标签**，比如：

   ~~~javascript
   div.innerText = div.innerText;
   ~~~

   > 这个小技巧不太熟

   **执行这行代码后，就用原来的文本内容替换了容器元素中的所有内容（包括子节点，因而也就去掉了HTML标签）**
   。

   支持innerText属性的浏览器包括IE4+，Safari 3+、Opera 8+和Chrome，**Firefox虽然不支持inner Text，但支持作用类似的textContent属性**。textContent是DOM Level3规定的一个属性，其他支持textContent属性的浏览器还有1E9+，Safari 3+，Opera 10+和Chrome。为了确保跨浏览器兼容，有必要编写一个类似于下面的函数来**检测**可以使用哪个属性。

   ~~~javascript
   function getInnerText(element){
               return (typeof element.textContent == "string") ? 
                   element.textContent : element.innerText;
           }
           
           function setInnerText(element, text){
               if (typeof element.textContent == "string"){
                   element.textContent = text;
               } else {
                   element.innerText = text;
               }
           }
   ~~~

   > 调试浏览器兼容性是真的麻烦
   >
   > get和set方法现在还是不熟

   这两个函数都接收一个元素作为参数，然后检查这个元素是不是有textContent属性。如果有，那么typeof element.textContent应该是"string"；如果没有，那么这两个函数就会改为使用innerText。可以像下面这样调用这两个函数。

   ~~~javascript
   setInnerText (div，"Hello world!");
   alert (getInnerText (div)); 	//"Hello world!"
   ~~~

   > 实际上，innerText与textContent返回的内容并不完全一样。比如，innerText会忽略行内的样式和脚本，而textContent则会像返回其他文本一样返回行内的样式和脚本代码。避免跨浏览器兼容问题的最佳途径，就是从不包含行内样式或行内脚本的DOM子树副本或DOM片段中读取文本。

2. outerText属性

   除了作用范围扩大到了包含调用它的节点之外，outerText与innermext基本上没有多大区别。
   在读取文本值时，outerText与innerText的结果完全一样。但在写模式下，outerText就完全不同了：outerrext不只是替换调用它的元素的子节点，而是会替换整个元素（包括子节点）。比如：

   ~~~javascript
   div.outerText = "Hello world!";
   ~~~

   这行代码实际上相当于如下两行代码：

   ~~~javascript
   var text = document. createTextNode ("Hello worlq!"); 
   div.parentNode.replaceChild(text, div);
   ~~~

   本质上，新的文本节点会完全取代调用outerText的元素。此后，该元素就从文档中被删除，无法访问。
   支持outerText属性的浏览器有IE4+，Safari 3+、Opera 8+和Chrome。由于这个属性会导致调用它的元素不存在，因此并不常用。我们也建议读者尽可能不要使用这个属性。

### 滚动

如前所述，HTML5之前的规范并没有就与页面滚动相关的API做出任何规定。但HTML5在将scroll Intoview（）纳入规范之后，仍然还有其他几个专有方法可以在不同的浏览器中使用。下面列出的几个方法都是对HTMLElement类型的扩展，因此在所有元素中都可以调用。

~~~javascript
scroll IntoviewIfNeeded（alignCenter）：只在当前元素在视口中不可见的情况下，才滚动浏览器窗口或容器元素，最终让它可见。如果当前元素在视口中可见，这个方法什么也不做。如果将可选的alignCenter参数设置为true，则表示尽量将元素显示在视口中部（垂直方向）。Safari和Chrome实现了这个方法。

scro1l ByLines（lineCount）：将元素的内容滚动指定的行高，lineCount值可以是正值，也可以是负值。Safari和Chrome实现了这个方法。

scrol1ByPages（pageCount）：将元素的内容滚动指定的页面高度，具体高度由元素的高度决定。Safari和Chrome实现了这个方法。
~~~

希望大家要注意的是，scroll Intoview（）和scro1l IntoviewIfNeeded（）的作用对象是元素的容器，而scrollByLines（）和scrol1ByPages（）影响的则是元素自身。下面还是来看几个示例吧。

~~~javascript
//将页面主体滚动5行
document.body.scrollBylines（5）；

//在当前元素不可见的时候，让它进入浏览器的视口
document.images[0].scro11IntoviewI fNeeded（）;

//将页面主体往回滚动1页
document.body.scrollByPages（-1）；
~~~

由于scroll IntoView（）是唯一一个所有浏览器都支持的方法，因此还是这个方法最常用。

## 小结

虽然DOM为与XML及HTML文档交互制定了一系列核心API，但仍然有几个规范对标准的DOM进行了扩展。这些扩展中有很多原来是浏览器专有的，但后来成为了事实标准，于是其他浏览器也都提供了相同的实现。本章介绍的三个这方面的规范如下。

~~~javascript
Selectors API，定义了两个方法，让开发人员能够基于CSS选择符从DOM中取得元素，这两个方法是queryselector（）和queryselectorAl1（）。

Element Traversal，为DOM元素定义了额外的属性，让开发人员能够更方便地从一个元素跳到另一个元素。之所以会出现这个扩展，是因为浏览器处理DOM元素间空白符的方式不一样。

HTML5，为标准的DOM定义了很多扩展功能。其中包括在innerHTML属性这样的事实标准基础上提供的标准定义，以及为管理焦点、设置字符集、滚动页面而规定的扩展API
~~~

虽然目前DOM扩展的数量还不多，但随着Web技术的发展，相信一定还会涌现出更多扩展来。很多湖览器都在试验专有的扩展，而这些扩展一旦获得认可，就能成为“伪”标准，甚至会被收录到规范的更新版本中。

# 第12章：DOM2和DOM3(先略，不熟)

DOM1级主要定义的是HTML和XML文档的底层结构。DOM2和DOM3级则在这个结构的基础上引入了更多的交互能力，也支持了更高级的XML特性。为此，DOM2和DOM3级分为许多模块（模块之间具有某种关联），分别描述了DOM的某个非常具体的子集。这些模块如下。

~~~javascript
DOM2级核心（DOM Level 2 Core）：在1级核心基础上构建，为节点添加了更多方法和属性。
DOM2级视图（DOM Level 2 Views）：为文档定义了基于样式信息的不同视图。
DOM2级事件（DOM Level 2 Events）：说明了如何使用事件与DOM文档交互。
DOM2级样式（DOM Level 2 Style）：定义了如何以编程方式来访问和改变Css样式信息。
DOM2级遍历和范围（DOM Level 2 Traversal and Range）：引人了遍历DOM文档和选择其特定部分的新接口。
DOM2级HTML（DOM Level 2 HTML）：在1级HTML基础上构建，添加了更多属性、方法和新接口。
~~~

本章探讨除"DOM2级事件”之外的所有模块，"DOM2级事件”模块将在第13章进行全面讲解。

> DOM3级又增加了"XPath"模块和“加载与保存"（Load and Save）模块。这些模块将在第18章讨论。

## DOM变化

DOM2级和3级的目的在于扩展DOM API，以满足操作XML的所有需求，同时提供更好的错误处理及特性检测能力。从某种意义上讲，实现这一目的很大程度意味着对命名空间的支持。"DOM2级核心”没有引人新类型，它只是在DOM1级的基础上通过增加新方法和新属性来增强了既有类型。"DOM3级核心”同样增强了既有类型，但也引人了一些新类型。

类似地，"DOM2级视图”和"DOM2级HTML"模块也增强了DOM接口，提供了新的属性和方法。由于这两个模块很小，因此我们将把它们与"DOM2级核心”放在一起，讨论基本JavaScript对象的变化。可以通过下列代码来确定浏览器是否支持这些DOM模块。

~~~javascript
var supportsDOM2Core = document . implementation. hasFeature ("Core". "2.0"); 
var supportsDOM3Core = document.implementation. hasFeature ("Core", "3.0"); 
var supportsDOM2HTML= document.implementation. hasFeature ("HTML", "2.0"); 
var supportsDOM2Views = document.implementation. hasFeature("views". "2.0"): 
var supportsDOM2XML = document.implementation. hasFeature ("XML", "2.0");
~~~

> 本章只讨论那些已经有浏览器实现的部分，任何浏览器都没有实现的部分将不作讨论。

### 针对XML命名空间的变化




# 第13章：事件(复习)

**JavaScript与HTML之间**的交互是通过**事件**实现的。**事件，就是文档或浏览器窗口中发生的一些特定的交互瞬间。可以使用侦听器（或处理程序）来预定事件，以便事件发生时执行相应的代码。**这种在传统软件工程中被称为**观察员模式的模型**，**支持页面的行为（JavaScript代码）与页面的外观（HTML和CSS代码）之间的松散耦合。**

事件最早是在IE3和Netscape Navigator2中出现的，当时是作为分担服务器运算负载的一种手段。在IE4和Navigator4发布时，这两种浏览器都提供了相似但不相同的API，这些API并存经过了好几个主要版本。DOM2级规范开始尝试以一种符合逻辑的方式来标准化DOM事件。IE9、Firefox、Opera、Safari和 Chrome全都已经实现了“DOM2级事件”模块的核心部分。**IE8是最后一个仍然使用其专有事件系统的主要浏览器。**

浏览器的事件系统相对比较复杂。尽管所有主要浏览器已经实现了“DOM2级事件”，但这个规范本身并没有涵盖所有事件类型。浏览器对象模型（BOM）也支持一些事件，这些事件与文档对象模型（DOM）事件之间的关系并不十分清晰，因为BOM事件长期没有规范可以遵循（HTML5后来给出了详细的说明）。**随着DOM3级的出现，增强后的DOM事件API变得更加繁琐。使用事件有时相对简单，有时则非常复杂，难易程度会因你的需求而不同。**不过，有关事件的一些核心概念是一定要理解的。

## 事件流(复习完)

当浏览器发展到第四代时（IE4及Netscape Communicator4），浏览器开发团队遇到了一个很有意思的问题：页面的哪一部分会拥有某个特定的事件？要明白这个问题问的是什么，可以**想象画在一张纸上的一组同心圆。如果你把手指放在圆心上，那么你的手指指向的不是一个圆，而是纸上的所有圆。**两家公司的浏览器开发团队在看待浏览器事件方面还是一致的。如果你单击了某个按钮，他们都认为单击事件不仅仅发生在按钮上。**换句话说，在单击按钮的同时，你也单击了按钮的容器元素，甚至也单击了整个页面。**

**事件流描述的是从页面中接收事件的顺序**。但有意思的是，IE和Netscape开发团队居然提出了差不多是完全相反的事件流的概念。**IE的事件流是事件冒泡流，而Netscape Communicator的事件流是事件捕获流。**

### 事件冒泡（IE:从下往上冒泡）

**IE的事件流叫做事件冒泡（event bubbling），即事件开始时由最具体的元素（文档中嵌套层次最深的那个节点）接收，然后逐级向上传播到较为不具体的节点（文档）。**以下面的HTML页面为例：

~~~javascript
<html>
  <head>
    <title>事件冒泡举例</title>
  </head>
  <body>
    <div id="myDiv">点击我</div>
  </body>
</html>
~~~

如果你单击了页面中的\<div>元素，那么这个click事件会按照如下顺序传播：

~~~javascript
（1）<div>
（2）<body>
（3）<html>
（4）document
~~~

也就是说，click事件首先在\<div>元素上发生，而这个元素就是我们单击的元素。然后，click事件沿DOM树向上传播，在每一级节点上都会发生，直至传播到document对象。图13-1展示了事件冒泡的过程。

![](读书笔记：JavaScript高级程序设计02(第3版)/104.png)

**所有现代浏览器都支持事件冒泡，但在具体实现上还是有一些差别**。IE5.5及更早版本中的事件冒泡会跳过\<htm1>元素（从\<body>直接跳到document）。**IE9、Firefox、Chrome和Safari则将事件一直冒泡到window对象。**

### 事件捕获(网景：从树上一跃而下捕获猎物)

Netscape Communicator团队提出的另一种事件流叫做**事件捕获**（event capturing）。事**件捕获的思想是不太具体的节点应该更早接收到事件，而最具体的节点应该最后接收到事件。**事件捕获的用意在于**在事件到达预定目标之前捕获它。**如果仍以前面的HTML页面作为演示事件捕获的例子，那么单击\<div>
元素就会以下列顺序触发click事件。

~~~javascript
（1）document
（2）<html>
（3）<body>
（4）<div>
~~~

在事件捕获过程中，document对象首先接收到click事件，然后**事件沿DOM树依次向下，一直传播到事件的实际目标，即\<div>元素**。图13-2展示了事件捕获的过程。

![](读书笔记：JavaScript高级程序设计02(第3版)/105.png)

虽然事件捕获是Netscape Communicator唯一支持的事件流模型，但IE9、Safari、Chrome、Opera和Firefox目前也都支持这种事件流模型。尽管**“DOM2级事件”规范**要求事件应该从**document对象**开始传播，但这些浏览器都是从**window对象**开始捕获事件的。

**由于老版本的浏览器不支持，因此很少有人使用事件捕获。我们也建议读者放心地使用事件冒泡，在有特殊需要时再使用事件捕获。**

> IE胜利，网景失败

### DOM事件流

“DOM2级事件”规定的**事件流包括三个阶段**：**事件捕获阶段、处于目标阶段和事件冒泡阶段**。**首先发生的是事件捕获，为截获事件提供了机会。然后是实际的目标接收到事件。最后一个阶段是冒泡阶段，可以在这个阶段对事件做出响应。**以前面简单的HTML页面为例，单击< div>元素会按照图13-3所示顺序触发事件。

![](读书笔记：JavaScript高级程序设计(第3版)02/110.png)

在DOM事件流中，实际的目标(< div>元素)**在捕获阶段不会接收到事件**。这意味着在捕获阶段，事件从document到< htm1>再到< body>后就停止了。下一个阶段是“处于目标”阶段，于是事件在< div>
上发生，并在事件处理（后面将会讨论这个概念）中被看成冒泡阶段的一部分。然后，冒泡阶段发生，事件又传播回文档。

多数支持DOM事件流的浏览器都实现了一种特定的行为；**即使“DOM2级事件”规范明确要求捕获阶段不会涉及事件目标，但IE9、Safari、Chrome、Firefox和Opera9.5及更高版本都会在捕获阶段触发事件对象上的事件。结果，就是有两个机会在目标对象上面操作事件。**

> IE9、Opera、Firefox、Chrome和Safari都支持DOM事件流；E8及更早版本不支持DOM事件流。

## 事件处理程序（响应事件的函数）

**事件就是用户或浏览器自身执行的某种动作。**诸如click、load和mouseover，都是事件的名字。
**而响应某个事件的函数就叫做事件处理程序（或事件侦听器）**。**事件处理程序的名字以“on“开头，因此click事件的事件处理程序就是onclick，load事件的事件处理程序就是onload。**为事件指定处理程序的方式有好几种。

### HTML事件处理程序(看完，后面看的不太懂)

> HTML事件处理程序用的不多，因为耦合度太高了，所以后面看不太懂也没什么大问题。

**某个元素支持的每种事件，都可以使用一个与相应事件处理程序同名的HTML特性来指定。这个特性的值应该是能够执行的JavaScript代码。**例如，要在按钮被单击时执行一些JavaScript，可以像下面这样编写代码：

~~~javascript
<input type="button" value="Click Me" onclick="alert('Clicked')">
~~~

当单击这个按钮时，就会显示一个警告框。**这个操作是通过指定onclick 特性并将一些JavaScript代码作为它的值来定义的。**由于这个值是JavaScript，因此**不能在其中使用未经转义的HTML语法字符**，例如和号（&）、双引号（”）、小于号（<）或大于号（>）。**为了避免使用HTML实体，这里使用了单引号。**如果想要使用双引号，那么就要将代码改写成如下所示：

~~~javascript
<input type="button" value="Click Me" onclick="alert(&quot;Clicked&quot;)">
~~~

**在HTML中定义的事件处理程序可以包含要执行的具体动作，也可以调用在页面其他地方定义的脚本**，如下面的例子所示：

~~~javascript
 <script type="text/javascript">
        function showMessage(){
            alert("Hello world!");
        }
 </script>
 <input type="button" value="Click Me" onclick="showMessage()" />
~~~

**在这个例子中，单击按钮就会调用showMessage（）函数**。**这个函数是在一个独立的< script>元素中定义的，当然也可以被包含在一个外部文件中**。**事件处理程序中的代码在执行时，有权访问全局作用域中的任何代码。**

**这样指定事件处理程序具有一些独到之处。首先，这样会创建一个封装着元素属性值的函数。这个函数中有一个局部变量event，也就是事件对象（本章稍后讨论）**：

~~~javascript
<!-- 输出"click" -->
<input type="button" value="Click Me" onclick="alert(event.type)">
~~~

**通过event变量，可以直接访问事件对象，你不用自己定义它，也不用从函数的参数列表中读取。**
**在这个函数内部，this值等于事件的目标元素**，例如：

~~~javascript
<!-- 输出"click Me" -->
<input type="button" value="Click Me" onclick="alert(this.type)">
~~~

关于这个动态创建的函数，另一个有意思的地方是**它扩展作用域的方式**。在这个函数内部，可以像访问局部变量一样访问 document及该元素本身的成员。这个函数使用with像下面这样扩展作用域：

~~~javascript
function(){
	with(document){
		with(this){
			//元素属性值
		}
	}
}
~~~

**如此一来，事件处理程序要访问自己的属性就简单多了。**下面这行代码与前面的例子效果相同：

~~~javascript
<!-- 输出"click Me" -->
<input type="button" value="Click Me" onclick="alert(value)">
~~~

如果当前元素是一个表单输入元素，则作用域中还会包含访问表单元素（父元素）的入口，这个函数就变成了如下所示：

~~~javascript
function(){
		with(document){
        with(this.form){
						with(this){
							//元素属性值
            }
        }
		}
}
~~~

**实际上，这样扩展作用域的方式，无非就是想让事件处理程序无需引用表单元素就能访问其他表单字段。例如：**

~~~javascript
<form method="post">
    <input type="text" name="username" value="enter username">
    <input type="button" value="Echo Username" onclick="alert(username.value)">
</form>
~~~

在这个例子中，单击按钮会显示文本框中的文本。值得注意的是，这里直接引用了username元素。

不过，在HTML中指定事件处理程序有两个缺点。**首先，存在一个时差问题。**因为用户可能会在HTML元素一出现在页面上就触发相应的事件，但当时的事件处理程序有可能尚不具备执行条件。以前面的例子来说明，假设 showMessage（）函数是在按钮下方、页面的最底部定义的。如果用户在页面解析 showMessage（）函数之前就单击了按钮，就会引发错误。为此，**很多HTML事件处理程序都会被封装在一个try-catch块中，以便错误不会浮出水面**，如下面的例子所示：

~~~javascript
<input type="button" value="Click Me" onclick="try{showMessage();}catch(ex){}" />
~~~

这样，如果在showMessage（）函数有定义之前单击了按钮，用户将不会看到JavaScript错误，因为在浏览器有机会处理错误之前，错误就被捕获了。

**另一个缺点是，这样扩展事件处理程序的作用域链在不同浏览器中会导致不同结果**。不同 JavaScript引擎遵循的标识符解析规则略有差异，很可能会在访问非限定对象成员时出错。

通过HTML指定事件处理程序的最后一个缺点是**HTML与JavaScript代码紧密耦合**。**如果要更换事件处理程序，就要改动两个地方：HTML代码和JavaScript代码。而这正是许多开发人员摒弃HTML事件处理程序，转而使用JavaScript指定事件处理程序的原因所在。**

### DOM0级事件处理程序（复习完）

**通过JavaScript**指定事件处理程序的传统方式，就是将一个**函数**赋值给一个事件处理程序**属性**。这种为事件处理程序赋值的方法是在第四代Web浏览器中出现的，而且至今仍然为所有现代浏览器所支持。**原因一是简单，二是具有跨浏览器的优势。要使用JavaScript指定事件处理程序，首先必须取得一个要操作的对象的引用。**

**每个元素（包括window和document）都有自己的事件处理程序属性，这些属性通常全部小写，例如onclick。将这种属性的值设置为一个函数，就可以指定事件处理程序**，如下所示：

~~~javascript
var btn = document.getElementById ("myBtn"); 
btn.onclick = function() {
	alert ("clicked");
};
~~~

在此，我们通过文档对象取得了一个按钮的引用，然后为它指定了onclick事件处理程序。但要注意，**在这些代码运行以前不会指定事件处理程序**，因此**如果这些代码在页面中位于按钮后面，就有可能在一段时间内怎么单击都没有反应。**

**使用DOMO级方法指定的事件处理程序被认为是元素的方法。**因此，这时候的事件处理程序是在元素的作用域中运行；换句话说，程序中的this引用当前元素。来看一个例子。

~~~javascript
var btn = document.getElementById("myBtn");
btn.onclick = function(){
     alert(this.id);	//"myBtn"
};
~~~

单击按钮显示的是元素的ID，这个ID是通过this.ia取得的。**不仅仅是ID，实际上可以在事件处理程序中通过this访问元素的任何属性和方法。**以这种方式添加的事件处理程序会在事件流的**冒泡阶段**被处理。

也可以删除通过DOMO级方法指定的事件处理程序，只要像下面这样将事件处理程序属性的值设置为null即可：

~~~javascript
btn.onclick = nul1；//删除事件处理程序
~~~

**将事件处理程序设置为null之后，再单击按钮将不会有任何动作发生。**

> 如果你使用HTML指定事件处理程序，那么onclick属性的值就是一个包含着在同名HTML特性中指定的代码的函数。而将相应的属性设置为null，也可以删除以这种方式指定的事件处理程序。

### DOM2级事件处理程序（看完）

"DOM2级事件”定义了两个方法，**用于处理指定和删除事件处理程序的操作：addEventListener（）和removeEventListener（）**。**所有DOM节点**中都包含这两个方法，并且**它们都接受3个参数**：**要处理的事件名、作为事件处理程序的函数和一个布尔值。最后这个布尔值参数如果是true，表示在捕获阶段调用事件处理程序；如果是false，表示在冒泡阶段调用事件处理程序。**

> true:捕获阶段      false:冒泡阶段

要在按钮上为click事件添加事件处理程序，可以使用下列代码：

~~~javascript
var btn = document. getElementById ("myBtn"); 
btn.addBventListener("click", function(){
	alert (this.id);
},false);
~~~

上面的代码为一个按钮添加了onclick事件处理程序，而且该事件会在冒泡阶段被触发（因为最后一个参数是false），**与DOM0级方法一样，这里添加的事件处理程序也是在其依附的元素的作用域中运行**。使用DOM2级方法添加事件处理程序的**主要好处是可以添加多个事件处理程序**。来看下面的例子。

~~~javascript
 var btn = document.getElementById("myBtn");
 btn.addEventListener("click", function(){
        alert(this.id);
 }, false);

 btn.addEventListener("click", function(){
        alert("Hello world!");
 }, false);
~~~

这里为按钮添加了两个事件处理程序。这两个事件处理程序会**按照添加它们的顺序触发**，因此首先会显示元素的ID，其次会显示"Hello world！"消息。

**通过addEventListener（）添加的事件处理程序只能使用removeEventListener（）来移除**；移除时传入的参数与添加处理程序时使用的参数相同。**这也意味着通过addEventListener（）添加的匿名函数将无法移除**，如下面的例子所示。

~~~javascript
 var btn = document.getElementById("myBtn");
 btn.addEventListener("click", function(){
        alert(this.id);
 }, false);

//这里省略了其他代码

btn.removeBventListener（"click"，function（）｛//没有用！
	alert（this.id）；
｝.false）；
~~~

在这个例子中，我们使用addEventListener（）添加了一个事件处理程序。虽然调用remove-EventListener（）时看似使用了相同的参数，**但实际上，第二个参数与传入addEventListener（）中的那一个是完全不同的函数。**而传入removeEventListener（）中的事件处理程序函数必须与传入addEventListener（）中的相同，如下面的例子所示。

~~~javascript
 var btn = document.getElementById("myBtn");
 var handler = function(){
        alert(this.id);
};
btn.addEventListener("click", handler, false); 

//这里省略了其他代码

btn.removeEventListener("click", handler, false);  //有效!
~~~

**重写后的这个例子没有问题，是因为在adaEventListener（）和removeEventListener（）中使用了相同的函数。**

**大多数情况下，都是将事件处理程序添加到事件流的冒泡阶段，这样可以最大限度地兼容各种浏览器。**

> 所以第3个参数基本上都是false

最好只在需要在事件到达目标之前截获它的时候将事件处理程序添加到捕获阶段。**如果不是特别需要，我们不建议在事件捕获阶段注册事件处理程序。**

> IE9，Firefox，Safari，Chrome和Opera支持DOM2级事件处理程序。

### IE事件处理程序（先不看）

IE实现了与DOM中类似的两个方法：attachEvent（）和detachEvent（）。这两个方法接受相同的两个参数：事件处理程序名称与事件处理程序函数。由于1E8及更早版本只支持事件冒泡，所以通过attachEvent（）添加的事件处理程序都会被添加到冒泡阶段。

要使用attachEvent()为按钮添加一个事件处理程序，可以使用以下代码。

~~~javascript
var btn = document.getElementById("myBtn");
btn.attachEvent("onclick", function(){
      alert("Clicked");
});
~~~

注意，attachEvent（）的第一个参数是"onclick"，而非DOM的addEventListener（）方法中的"click"。

在IE中使用attachEvent（）与使用DOMO级方法的主要区别在于事件处理程序的作用域。在使用DOMO级方法的情况下，事件处理程序会在其所属元素的作用域内运行；在使用attachEvent（）方法的情况下，事件处理程序会在全局作用域中运行，因此this等于window。来看下面的例子。

~~~javascript
var btn = document.getElementById("myBtn");
btn.attachEvent("onclick", function(){
      alert(this === window);		//true
});
~~~

在编写跨浏览器的代码时，牢记这一区别非常重要。

与addEventListener（）类似，attachEvent（）方法也可以用来为一个元素添加多个事件处理程序。来看下面的例子。

~~~javascript
 var btn = document.getElementById("myBtn");
 btn.attachEvent("onclick", function(){
        alert("Clicked");
 });

 btn.attachEvent("onclick", function(){
        alert("Hello world!");
 });
~~~

这里调用了两次attachEvent（），为同一个按钮添加了两个不同的事件处理程序。不过，与DOM方法不同的是，这些事件处理程序不是以添加它们的顺序执行，而是以相反的顺序被触发。单击这个例子中的按钮，首先看到的是"Hello world！"，然后才是"Clicked"。

使用attachEvent（）添加的事件可以通过detachEvent（）来移除，条件是必须提供相同的参数。
与DOM方法一样，这也意味着添加的匿名函数将不能被移除。不过，只要能够将对相同函数的引用传给detachEvent（），就可以移除相应的事件处理程序。例如：

~~~javascript
 var btn = document.getElementById("myBtn");
 var handler = function(){
       alert("Clicked");
 };

 btn.attachEvent("onclick", handler); 
//这里省略了其他代码

btn.detachEvent("onclick", handler); 
~~~

这个例子将保存在变量handler中的函数作为事件处理程序。因此，后面的detachEvent（）可以使用相同的函数来移除事件处理程序。

> 支持IE事件处理程序的浏览器有IE和Opera

### 跨浏览器的事件处理程序

为了以跨浏览器的方式处理事件，不少开发人员会使用能够隔离浏览器差异的Javascript库，还有一些开发人员会自己开发最合适的事件处理的方法。自己编写代码其实也不难，只要恰当地使用能力检测即可（能力检测在第9章介绍过），要保证处理事件的代码能在大多数浏览器下一致地运行，只需关注冒泡阶段。

第一个要创建的方法是adaHandler（），它的职责是视情况分别使用DOMO级方法、DOM2级方法或IE方法来添加事件。这个方法属于一个名叫EventUtil的对象，本书将使用这个对象来处理浏览器间的差异。adaHandler（1）方法接受3个参数：要操作的元素、事件名称和事件处理程序函数。

与addHandler（）对应的方法是removeHandler（），它也接受相同的参数。这个方法的职责是移除之前添加的事件处理程序-无论该事件处理程序是采取什么方式添加到元素中的，如果其他方法无效，默认采用DOMO级方法。

EventUtil的用法如下所示。

~~~javascript
var EventUtil = {

    addHandler: function(element, type, handler){
        if (element.addEventListener){
            element.addEventListener(type, handler, false);
        } else if (element.attachEvent){
            element.attachEvent("on" + type, handler);
        } else {
            element["on" + type] = handler;
        }
    },
    removeHandler; function (element, type, handler){
	    if (element.removeEvent Listener){
			element.removeEventListener (type. handler, false);
		} else if (elenent. detachEvent) (
			element. detachEvent ("on"+ type, handler);
            } else {
        	element ["on"+ type] = null;
        }
	}
};
~~~

这两个方法首先都会检测传入的元素中是否存在DOM2级方法。如果存在DOM2级方法，则使用该方法：传入事件类型、事件处理程序函数和第三个参数false（表示冒泡阶段），如果存在的是IE的方法，则采取第二种方案。注意，为了在1E8及更早版本中运行，此时的事件类型必须加上"on"前缀。
最后一种可能就是使用DOMO级方法（在现代浏览器中，应该不会执行这里的代码）。此时，我们使用的是方括号语法来将属性名指定为事件处理程序，或者将属性设置为null。

可以像下面这样使用EventUti1对象：

~~~javascript
 var btn = document.getElementById("myBtn");
 var handler = function(){
        alert("Clicked");
 };

 EventUtil.addHandler(btn, "click", handler); 
       
//这里省略了其他代码
 EventUtil.removeHandler(btn, "click", handler); 
~~~

adaHandler（）和removeHandler（）没有考虑到所有的浏览器问题，例如在IE中的作用域问题。
不过，使用它们添加和移除事件处理程序还是足够了。此外还要注意，DOMO级对每个事件只支持一个事件处理程序。好在，只支持DOMO级的浏览器已经没有那么多了，因此这对你而言应该不是什么问题。

## 事件对象

在触发DOM上的某个事件时，会产生一个**事件对象event**，**这个对象中包含着所有与事件有关的信息**。**包括导致事件的元素、事件的类型以及其他与特定事件相关的信息。**例如，鼠标操作导致的事件对象中，会包含鼠标位置的信息，而键盘操作导致的事件对象中，会包含与按下的键有关的信息。**所有浏览器都支持event对象，但支持方式不同。**

### DOM中的事件对象

兼容DOM的浏览器会将一个event对象传入到事件处理程序中。无论指定事件处理程序时使用什么方法（DOM0级或DOM2级），都会传入event对象。来看下面的例子。

~~~javascript
var btn = document. getElementById("myBtn"); 
btn.onclick = function (event){
    alert (event.type); //"click"
};

btn.addEventListener("click", function (event)(
	alert (event. type); //"click"
),false);
~~~

这个例子中的两个事件处理程序都会弹出一个警告框，显示由event.type属性表示的事件类型。
这个属性始终都会包含被触发的事件类型，例如"click"（与传入addEventListener（）和removeEventListener（）中的事件类型一致）。

在通过HTML特性指定事件处理程序时，变量event中保存着event对象。请看下面的例子。

~~~javascript
<input type="button" value="Click Me" onclick="alert(event.type)">
~~~

以这种方式提供event对象，可以让HTML特性事件处理程序与JavaScript函数执行相同的操作。

event对象包含与创建它的特定事件有关的属性和方法。触发的事件类型不一样，可用的属性和方法也不一样。不过，所有事件都会有下表列出的成员。

![](读书笔记：JavaScript高级程序设计02(第3版)/119.jpg)

# 第20章：JSON

曾经有一段时间，XML是互联网上传输结构化数据的事实标准。Web服务的第一次浪潮很大程度上都是建立在XML之上的，突出的特点是服务器与服务器间通信。然而，业界一直不乏质疑XML的声音。不少人认为XML过于烦琐、冗长。为解决这个问题，也涌现了一些方案。不过，Web的发展方向已经改变了。

2006年，Douglas Crockford把JSON（JavaScript Object Notation，JavaScript对象表示法）作为IETF RFC4627提交给IETF，而JSON的应用早在2001年就已经开始了。JSON是JavaScript的一个严格的子集，利用了JavaScript中的一些模式来表示结构化数据。Crockford认为与XML相比，JSON是在JavaScript中读写结构化数据的更好的方式。因为可以把JSON直接传给eva1（），而且不必创建DOM对象。

关于JSON，最重要的是要理解它是一种数据格式，不是一种编程语言。虽然具有相同的语法形式，但JSON并不从属于JavaScript。而且，并不是只有JavaScript才使用JSON，毕竟JSON只是一种数据格式。很多编程语言都有针对JSON的解析器和序列化器。

## 语法

![](读书笔记：JavaScript高级程序设计(第3版)/111.png)

### 简单值

最简单的JSON数据形式就是简单值。例如，下面这个值是有效的JSON数据：

~~~
5
~~~

这是JSON表示数值5的方式。类似地，下面是JSON表示字符串的方式：

~~~javascript
"Hello World!"
~~~

JavaScript字符串与JSON字符串的最大区别在于，JSON字符串必须使用双引号（单引号会导致语法错误）。
布尔值和nu11也是有效的JSON形式。但是，在实际应用中，JSON更多地用来表示更复杂的数据结构，而简单值只是整个数据结构中的一部分。

### 对象

JSON中的对象与JavaScript字面量稍微有一些不同。下面是一个JavaScript中的对象字面量：

~~~javascript
var person = {
  name: 'Nicholas',
  age: 29
};
~~~

这虽然是开发人员在JavaScript中创建对象字面量的标准方式，但JSON中的对象要求给属性加引号。实际上，在JavaScript中，前面的对象字面量完全可以写成下面这样：

~~~javascript
var object = {
  "name": 'Nicholas',
  "age": 29
};
~~~

JSON表示上述对象的方式如下：

~~~javascript
{
    "name": 'Nicholas',
    "age": 29 
}
~~~

与JavaScript的对象字面量相比，JSON对象有两个地方不一样。首先，没有声明变量（JSON中没有变量的概念）。其次，没有末尾的分号（因为这不是JavaScript语句，所以不需要分号）。再说一遍，对象的属性必须加双引号，这在JSON中是必需的。属性的值可以是简单值，也可以是复杂类型值，因此可以像下面这样在对象中嵌入对象：

~~~javascript
{
    "name": 'Nicholas',
    "age": 29,
        "school": {
           "name":"Merrimack College",
		   "location":"North Andover,MA"
        }
}
~~~

这个例子在顶级对象中嵌入了学校（“school*）信息。虽然有两个“name“属性，但由于它们分别属于不同的对象，因此这样完全没有问题。不过，同一个对象中绝对不应该出现两个同名属性。

与JavaScript不同，JSON中对象的属性名任何时候都必须加双引号。手工编写JSON时，忘了给对象属性名加双引号或者把双引号写成单引号都是常见的错误。

### 数组

JSON中的第二种复杂数据类型是数组。JSON数组采用的就是JavaScript中的数组字面量形式。例如，下面是JavaScript中的数组字面量：

~~~javascript
var value = [25,"hi",true];
~~~

在JSON中，可以采用同样的语法表示同一个数组：

~~~javascript
[25,"hi",true];
~~~

同样要注意，JSON数组也没有变量和分号。把数组和对象结合起来，可以构成更复杂的数据集合，例如：

![](读书笔记：JavaScript高级程序设计(第3版)/112.png)

这个数组中包含一些表示图书的对象。每个对象都有几个属性，其中一个属性是“authors*，这个属性的值又是一个数组。对象和数组通常是JSON数据结构的最外层形式（当然，这不是强制规定的），利用它们能够创造出各种各样的数据结构。

## 解析与序列化

JSON 之所以流行，拥有与JavaScript类似的语法并不是全部原因。更重要的一个原因是，可以把JSON数据结构解析为有用的JavaScript对象。与XML数据结构要解析成DOM文档而且从中提取数据极为麻烦相比，JSON可以解析为JavaScript对象的优势极其明显。就以上一节中包含一组图书的JSON数据结构为例，在解析为JavaScript对象后，只需要下面一行简单的代码就可以取得第三本书的书名：

~~~javascript
books[2].title
~~~

当然，这里是假设把解析后JSON数据结构得到的对象保存到了变量books中。再看看下面在DOM结构中查找数据的代码：

~~~javascript
doc.getElementsByTagName("book")[2].getAttribute("title")
~~~

看看这些多余的方法调用，就不难理解为什么JSON能得到JavaScript开发人员的热烈欢迎了。从此以后，JSON就成了Web服务开发中交换数据的事实标准。

### JSON对象

早期的JSON解析器基本上就是使用JavaScript的eval（）函数。由于JSON是JavaScript语法的子集，因此eval（）函数可以解析、解释并返回JavaScript对象和数组。ECMAScript 5对解析JSON的行为进行规范，定义了全局对象JsoN。支持这个对象的浏览器有IE8+、Firefox 3.5+、Safari4+、Chrome和Opera10.5+。对于较早版本的浏览器，可以使用一个shim:https://github.com/douglascrockford/JSON-js。
在旧版本的浏览器中，使用eva1（）对JSON数据结构求值存在风险，因为可能会执行一些恶意代码。
对于不能原生支持JSON解析的浏览器，使用这个shim是最佳选择。

JSON对象有两个方法：stringify（）和parse（）。在最简单的情况下，这两个方法分别用于把JavaScript对象序列化为JSON字符串和把JSON字符串解析为原生JavaScript值。例如：

~~~javascript
 var book = {
                  title: "Professional JavaScript",
                  authors: [
                       "Nicholas C. Zakas"
                   ],
                   edition: 3,
                   year: 2011
            };

var jsonText = JSON.stringify(book);
~~~

这个例子使用JsoN.stringify（）把一个JavaScript对象序列化为一个JSON字符串，然后将它保存在变量sonrext中。默认情况下，JsoN.stringify（）输出的JSON字符申不包含任何空格字符或缩进，因此保存在sonText中的字符串如下所示：

~~~javascript
{"title":"Professional JavaScript","authors":["Nicholas C. Zakas"],"edition":3,
"year":2011}
~~~

在序列化JavaScript对象时，所有函数及原型成员都会被有意忽略，不体现在结果中。此外，值为undefined的任何属性也都会被跳过。结果中最终都是值为有效JSON数据类型的实例属性。

将JSON字符串直接传递给JSON.parse（）就可以得到相应的JavaScript值。例如，使用下列代码就可以创建与book类似的对象：

~~~javascript
var bookCopy = JSON.parse(jsonText);
~~~

注意，虽然book与bookCopy具有相同的属性，但它们是两个独立的、没有任何关系的对象。

如果传给JSON.parse（）的字符串不是有效的JSON，该方法会抛出错误。

### 序列化选项

实际上，JsoN.stringify（）除了要序列化的JavaScript对象外，还可以接收另外两个参数，这两个参数用于指定以不同的方式序列化JavaScript对象。第一个参数是个过滤器，可以是一个数组，也可以是一个函数；第二个参数是一个选项，表示是否在JSON字符串中保留缩进。单独或组合使用这两个参数，可以更全面深入地控制JSON的序列化。

1. 过滤结果

   如果过滤器参数是数组，那么JsoN.stringify（）的结果中将只包含数组中列出的属性。来看下面的例子。

   ~~~javascript
   var book = {
               title: "Professional JavaScript",
               authors: [
                       "Nicholas C. Zakas"
                     	 ],
               edition: 3,
               year: 2011
             };
   var jsonText = JSON.stringify(book, ["title", "edition"]);
   ~~~

   JsoN.stringify（）的第二个参数是一个数组，其中包含两个字符申：“title“和edition"。这两个属性与将要序列化的对象中的属性是对应的，因此在返回的结果字符串中，就只会包含这两个属性：

   ~~~javascript
   {"title":"Professional JavaScript","edition":3}
   ~~~

   如果第二个参数是函数，行为会稍有不同。传人的函数接收两个参数，属性（键）名和属性值。根据属性（键）名可以知道应该如何处理要序列化的对象中的属性。属性名只能是字符串，而在值并非键值对儿结构的值时，键名可以是空字符串。

   为了改变序列化对象的结果，函数返回的值就是相应键的值。不过要注意，如果函数返回了undefined，那么相应的属性会被忽略。还是看一个例子吧。

   ~~~javascript
   var book = {
               title: "Professional JavaScript",
               authors: [
                       "Nicholas C. Zakas"
                ],
               edition: 3,
               year: 2011
              };
   
   var jsonText = JSON.stringify(book, function(key, value){
           switch(key){
               case "authors":
                   return value.join(",")
                    
               case "year":
                   return 5000;
                       
               case "edition":
                   return undefined;
                       
               default:
                  return value;
           }
   });
   ~~~
   这里，函数过滤器根据传入的键来决定结果。如果键为“authors”，就将数组连接为一个字符串；如果键为"year"，则将其值设置为5000；如果键为“edition"，通过返回undefined 删除该属性。
   最后，一定要提供default项，此时返回传人的值，以便其他值都能正常出现在结果中。实际上，第一次调用这个函数过滤器，传人的键是一个空字符串，而值就是book对象。序列化后的JSON字符串如下所示：

   ~~~javascript
   {"title":"Professional JavaScript","authors":"Nicholas C. Zakas","year":5000}
   ~~~

   要序列化的对象中的每一个对象都要经过过滤器，因此数组中的每个带有这些属性的对象经过过滤之后，每个对象都只会包含“tit1e"、“authors”和“year“属性。
   Firefox 3.5和3.6对JsoN.stringify（）的实现有一个bug，在将函数作为该方法的第二个参数时这个bug就会出现，即这个函数只能作为过滤器：返回undefined意味着要跳过某个属性，而返回其他任何值都会在结果中包含相应的属性。Firefox4修复了这个bug。

2. 字符串缩进

   JSON.stringify（）方法的第三个参数用于控制结果中的缩进和空白符。如果这个参数是一个数值，那它表示的是每个级别缩进的空格数。例如，要在每个级别缩进4个空格，可以这样写代码：

   ~~~javascript
   var book = {
                 title: "Professional JavaScript",
                 authors: [
                       "Nicholas C. Zakas"
                 ],
                 edition: 3,
                 year: 2011
                };
   
   var jsonText = JSON.stringify(book, null, 4);
   ~~~

   保存在jsonText中的字符串如下所示：

   ~~~javascript
   {
     " title": "Professional JavaScript",
      "authors": [
                "Nicholas C. Zakas"
       ],
       "edition": 3,
       "year": 2011
    }
   ~~~

   不知道读者注意到没有，JsON.stringify（）也在结果字符串中插入了换行符以提高可读性。只要传人有效的控制缩进的参数值，结果字符串就会包含换行符。（只缩进而不换行意义不大。）最大缩进空格数为10，所有大于10的值都会自动转换为10。

   如果缩进参数是一个字符串而非数值，则这个字符串将在JSON字符串中被用作缩进字符（不再使用空格）。在使用字符串的情况下，可以将缩进字符设置为制表符，或者两个短划线之类的任意字符。

   ~~~javascript
     var jsonText = JSON.stringify(book, null, "--");
   ~~~

   这样，sonText中的字符串将变成如下所示：

   ~~~javascript
   {
   --"title":"Professional JavaScript",
   --"authors":[
   ----"Nicholas C. Zakas"
   --],
   --"edition":3,
   --"year":2011
   }
   ~~~

   缩进字符串最长不能超过10个字符长。如果字符串长度超过了10个，结果中将只出现前10个字符。

3. toJSON()方法

   有时候，JSON.stringify（）还是不能满足对某些对象进行自定义序列化的需求。在这些情况下，可以通过对象上调用toJSON（）方法，返回其自身的JSON数据格式。原生Date对象有一个toJSON（）方法，能够将JavaScript的Date对象自动转换成ISO 8601 日期字符串（与在Date对象上调用toISOstring（）的结果完全一样）。

   可以为任何对象添加toJSON（）方法，比如：

   ~~~javascript
   var book = {
               "title": "Professional JavaScript",
               "authors": [
                      "Nicholas C. Zakas"
                ],
                edition: 3,
                year: 2011,
                toJSON: function(){
                       return this.title;
                }
   };
   
   var jsonText = JSON.stringify(book);
   ~~~

   以上代码在book对象上定义了一个toJsoN（）方法，该方法返回图书的书名。与Date对象类似，这个对象也将被序列化为一个简单的字符串而非对象。可以让toJsoN（）方法返回任何序列化的值，它都能正常工作。也可以让这个方法返回undefined，此时如果包含它的对象嵌入在另一个对象中，会导致该对象的值变成nu11，而如果包含它的对象是顶级对象，结果就是undefined。

   toJSON（）可以作为函数过滤器的补充，因此理解序列化的内部顺序十分重要。假设把一个对象传入JSON.stringify（），序列化该对象的顺序如下。

   （1）如果存在toJSON（）方法而且能通过它取得有效的值，则调用该方法。否则，按默认顺序执行序列化。
   （2）如果提供了第二个参数，应用这个函数过滤器。传入函数过滤器的值是第（1）步返回的值。

   （3）对第（2）步返回的每个值进行相应的序列化。

   （4）如果提供了第三个参数，执行相应的格式化。

   无论是考虑定义toJSON（）方法，还是考虑使用函数过滤器，亦或需要同时使用两者，理解这个顺序都是至关重要的。

### 解析选项

JSON.parse（）方法也可以接收另一个参数，该参数是一个函数，将在每个键值对儿上调用。为了区别JsoN.stringify（）接收的替换（过滤）函数（replacer），这个函数被称为还原函数（reviver），但实际上这两个函数的签名是相同的一—它们都接收两个参数，一个键和一个值，而且都需要返回一个值。

如果还原函数返回undefined，则表示要从结果中删除相应的键；如果返回其他值，则将该值插入到结果中。在将日期字符串转换为Date对象时，经常要用到还原函数。例如：

~~~javascript
var book = {
            "title": "Professional JavaScript",
            "authors": [
                  "Nicholas C. Zakas"
             ],
             edition: 3,
             year: 2011,
             releaseDate: new Date(2011, 11, 1)
          };

var jsonText = JSON.stringify(book);
        
var bookCopy = JSON.parse(jsonText, function(key, value){
      if (key == "releaseDate"){
           return undefined;
      } else {
           return value;
      }
});

alert(bookCopy.releaseDate.getFullYear());
~~~

以上代码先是为book对象新增了一个releasepate属性，该属性保存着一个Date对象。这个对象在经过序列化之后变成了有效的JSON字符串，然后经过解析又在bookCopy中还原为一个Date对象。还原函数在遇到“releasepate*键时，会基于相应的值创建一个新的pate对象。结果就是bookCopy.releaseDate属性中会保存一个Date对象。正因为如此，才能基于这个对象调用getFullyear（）方法。

## 小结

JSON是一个轻量级的数据格式，可以简化表示复杂数据结构的工作量。JSON使用JavaScript语法的子集表示对象、数组、字符串、数值、布尔值和nu11。即使XML也能表示同样复杂的数据结果，但JSON没有那么烦琐，而且在JavaScript中使用更便利。

ECMAScript5定义了一个原生的JsoN对象，可以用来将对象序列化为JSON字符串或者将JSON数据解析为JavaScript对象。JsoN.stringify（）和JsoN.parse（）方法分别用来实现上述两项功能。
这两个方法都有一些选项，通过它们可以改变过滤的方式，或者改变序列化的过程。

原生的JSON对象也得到了很多浏览器的支持，比如IE8+、Firefox 3.5+、Safari4+、Opera10.5和Chrome。

# 第21章：Ajax和Comet(Ajax很重要啊)

2005年，Jesse  Garrett发表了一篇在线文章，题为"Ajax：A new Approach to WebApplications"（http://www.adaptivepath.com/ideas/essays/archives/000385.php），他在这篇文章里介绍了一种技术，用他的话说，就叫Ajax，是对Asynchronous JavaScript + XML的简写。这一技术能够向服务器请求额外的数据而无须卸载页面，会带来更好的用户体验。Garrett还解释了怎样使用这一技术改变自从Web诞生以来就一直沿用的“单击，等待”的交互模式。

Ajax技术的核心是XMHttpRequest对象（简称XHR），这是由微软首先引入的一个特性，其他浏览器提供商后来都提供了相同的实现。在XHR出现之前，Ajax式的通信必须借助一些hack手段来实现，大多数是使用隐藏的框架或内嵌框架。XHR为向服务器发送请求和解析服务器响应提供了流畅的接口。能够以异步方式从服务器取得更多信息，意味着用户单击后，可以不必刷新页面也能取得新数据也就是说，可以使用XHR对象取得新数据，然后再通过DOM将新数据插入到页面中。另外，虽然名字中包含XML的成分，但Ajax通信与数据格式无关；这种技术就是无须刷新页面即可从服务器取得数据，但不一定是XML数据。

实际上，Garrett提到的这种技术已经存在很长时间了。在Garrett撰写那篇文章之前，人们通常将这种技术叫做远程脚本（remote scripting），而且早在1998年就有人采用不同的手段实现了这种浏览器与服务器的通信。再往前推，JavaScript需要通过Java applet或Flash电影等中间层向服务器发送请求。
而XHIR则将浏览器原生的通信能力提供给了开发人员，简化了实现同样操作的任务。

在重命名为Ajax之后，大约是2005年底2006年初，这种浏览器与服务器的通信技术可谓红极一时。人们对JavaScript和Web的全新认识，催生了很多使用原有特性的新技术和新模式。就目前来说，熟练使用XHR对象已经成为所有Web开发人员必须掌握的一种技能。

## XMLHttpRequest对象

IE5是第一款引入XHR对象的浏览器。在IES中，XHR对象是通过MSXML库中的一个Activex对象实现的。因此，在IE中可能会遇到三种不同版本的XHR对象，即MSXML2.XMLHttp.
MSXML2.XMLHttp.3.0和 MXSML2.XMLHttp.6.0，要使用MSXML库中的XHR对象，需要像第18章讨论创建XML文档时一样，编写一个函数，例如：

![](读书笔记：JavaScript高级程序设计02(第3版)/118.png)

这个函数会尽力根据IE中可用的MSXML库的情况创建最新版本的XHR对象。

IE7+，Firefox，Opera，Chrome和Sari都支持原生的XHR对象，在这些浏览器中创建XHR对象要像下面这样使用XMLHttpRequest构造函数。

~~~javascript
var xhr = new XMLHttpRequest();
~~~

假如你只想支持IE7及更高版本，那么大可丢掉前面定义的那个函数，而只用原生的XHR实现。
但是，如果你必须还要支持IE的早期版本，那么则可以在这个createxHR（）函中加入对原生XHR对象的支持。

~~~javascript
function createXHR(){
            if (typeof XMLHttpRequest != "undefined"){
                return new XMLHttpRequest();
            } else if (typeof ActiveXObject != "undefined"){
                if (typeof arguments.callee.activeXString != "string"){
                    var versions = ["MSXML2.XMLHttp.6.0", "MSXML2.XMLHttp.3.0",
                                    "MSXML2.XMLHttp"],
                        i, len;
            
                    for (i=0,len=versions.length; i < len; i++){
                        try {
                            new ActiveXObject(versions[i]);
                            arguments.callee.activeXString = versions[i];
                            break;
                        } catch (ex){
                            //跳过
                        }
                    }
                }
            
                return new ActiveXObject(arguments.callee.activeXString);
            } else {
                throw new Error("No XHR object available.");
            }
        }
~~~

这个函数中新增的代码首先检测原生XHR对象是否存在，如果存在则返回它的新实例。如果原生对象不存在，则检测Activex对象。如果这两种对象都不存在，就抛出一个错误。然后，就可以使用下面的代码在所有浏览器中创建XHR对象了。

~~~javascript
var xhr = createXHR();
~~~

由于其他浏览器中对XHR的实现与IE最早的实现是兼容的，因此就可以在所有浏览器中都以相同方式使用上面创建的xhr对象。

### XHR的用法

在使用XHR对象时，要调用的第一个方法是open（），它接受3个参数：要发送的请求的类型
（"get"、"post"等）、请求的URL和表示是否异步发送请求的布尔值。下面就是调用这个方法的例子。

~~~javascript
xhr.open("get","example.php",false);
~~~

这行代码会启动一个针对example.php的GET请求。有关这行代码，需要说明两点：一是URL相对于执行代码的当前页面（当然也可以使用绝对路径）；二是调用open（）方法并不会真正发送请求，而只是启动一个请求以备发送。

> 只能向同一个城中使用相同端口和协议的URL发送请求。如果URL与启动请求的页面有任何差别，都会引发安全错误。

要发送特定的请求，必须像下面这样调用send（）方法：

~~~javascript
xhr.open("get","example.php",false);
xhr.send(null);
~~~

这里的send（）方法接收一个参数，即要作为请求主体发送的数据。如果不需要通过请求主体发送数据，则必须传入null，因为这个参数对有些浏览器来说是必需的。调用send（）之后，请求就会被分派到服务器。

由于这次请求是同步的，JavaScript代码会等到服务器响应之后再继续执行。在收到响应后，响应的数据会自动填充XHR对象的属性，相关的属性简介如下。

* responseText：作为响应主体被返回的文本。
* responseXML：如果响应的内容类型是"text/xml"或"application/xml"，这个属性中将保存包含着响应数据的XML DOM文档。
*  status：响应的HTTP状态。
*  statusText：HTTP状态的说明。

在接收到响应后，第一步是检查status属性，以确定响应已经成功返回。一般来说，可以将HTTP状态代码为200作为成功的标志。此时，responseText属性的内容已经就绪，而且在内容类型正确的情况下，responsexML也应该能够访问了。此外，状态代码为304表示请求的资源并没有被修改，可以直接使用浏览器中缓存的版本；当然，也意味着响应是有效的。为确保接收到适当的响应，应该像下面这样检查上述这两种状态代码：

~~~javascript
xhr.open("get", "example.txt", false);
xhr.send(null);
        
if ((xhr.status >= 200 && xhr.status < 300) || xhr.status == 304){
        alert(xhr.responseText);
 } else {
        alert("Request was unsuccessful: " + xhr.status);
 }
~~~

根据返回的状态代码，这个例子可能会显示由服务器返回的内容，也可能会显示一条错误消息。我们建议读者要通过检测status来决定下一步的操作，不要依赖statusText，因为后者在跨浏览器使用时不太可靠。另外，无论内容类型是什么，响应主体的内容都会保存到responseText属性中；而对于非XML数据而言，responsexML属性的值将为null。

> 有的浏览器会错误地报告204状态代码。IE中XHR的Activex版本会将204设置为1223，而IE中原生的XHR则会将204规范化为200.Opera会在取得204时报告status的值为0。

像前面这样发送同步请求当然没有问题，但多数情况下，我们还是要发送异步请求，才能让Javascript继续执行而不必等待响应。此时，可以检测XHR对象的readystate属性，该属性表示请求/响应过程的当前活动阶段。这个属性可取的值如下。

* 0：未初始化。尚未调用open（）方法。
* 1：启动。已经调用open（）方法，但尚未调用send（）方法。
* 2：发送。已经调用send（）方法，但尚未接收到响应。
* 3：接收。已经接收到部分响应数据。
* 4：完成。已经接收到全部响应数据，而且已经可以在客户端使用了。

只要readyState属性的值由一个值变成另一个值，都会触发一次readystatechange事件。可以利用这个事件来检测每次状态变化后readystate的值。通常，我们只对readystate值为4的阶段感兴趣，因为这时所有数据都已经就绪。不过，必须在调用open（）之前指定onreadystatechange事件处理程序才能确保跨浏览器兼容性。下面来看一个例子。

~~~javascript
 var xhr = createXHR();        
 xhr.onreadystatechange = function(event){
       if (xhr.readyState == 4){
             if ((xhr.status >= 200 && xhr.status < 300) || xhr.status == 304){
                 alert(xhr.responseText);
             } else {
                 alert("Request was unsuccessful: " + xhr.status);
             }
       }
 };
 xhr.open("get", "example.txt", true);
 xhr.send(null);
~~~

以上代码利用DOM0级方法为xHR对象添加了事件处理程序，原因是并非所有浏览器都支持DOM2级方法。与其他事件处理程序不同，这里没有向onreadystatechange事件处理程序中传递event对象；必须通过xHR对象本身来确定下一步该怎么做。

> 这个例子在onreadystatechange事件处理程序中使用了xhr对象，没有使用this对象，原因是onreadystatechange事件处理程序的作用域问题。如果使用this对象，在有的浏览器中会导致函数执行失败，或者导致错误发生。因此，使用实际的XHR对象实例变量是较为可靠的一种方式。

另外，在接收到响应之前还可以调用abort（）方法来取消异步请求，如下所示：

~~~javascript
xhr.abort();
~~~

调用这个方法后，xHR对象会停止触发事件，而且也不再允许访问任何与响应有关的对象属性。在终止请求之后，还应该对XHR对象进行解引用操作。由于内存原因，不建议重用xHR对象。

### HTTP头部信息

每个HTTP请求和响应都会带有相应的头部信息，其中有的对开发人员有用，有的也没有什么用。
xHR对象也提供了操作这两种头部（即请求头部和响应头部）信息的方法。

默认情况下，在发送xHR请求的同时，还会发送下列头部信息。

* Accept：浏览器能够处理的内容类型。
* Accept-Charset：浏览器能够显示的字符集。
* Accept-Encoding：浏览器能够处理的压缩编码。
* Accept-Language：浏览器当前设置的语言。
* Connection：浏览器与服务器之间连接的类型。
* Cookie：当前页面设置的任何Cookic 
* Host：发出请求的页面所在的域。
* Referer：发出请求的页面的URI。注意，HTTP规范将这个头部字段拼写错了，而为保证与规范一致，也只能将错就错了。（这个英文单词的正确拼法应该是referrer。）
* User-Agent：浏览器的用户代理字符串。

虽然不同浏览器实际发送的头部信息会有所不同，但以上列出的基本上是所有浏览器都会发送的。
使用setRequestHeader（）方法可以设置自定义的请求头部信息。这个方法接受两个参数：头部字段的名称和头部字段的值。要成功发送请求头部信息，必须在调用open（）方法之后且调用send（）方法之前调用setRequestHeader（），如下面的例子所示。

~~~javascript
var xhr = createXHR();        
xhr.onreadystatechange = function(){
    if (xhr.readyState == 4){
           if ((xhr.status >= 200 && xhr.status < 300) || xhr.status == 304){
                alert(xhr.responseText);
            } else {
                alert("Request was unsuccessful: " + xhr.status);
            }
    }
};
xhr.open("get", "example.php", true);
xhr.setRequestHeader("MyHeader", "MyValue");
xhr.send(null);
~~~

服务器在接收到这种自定义的头部信息之后，可以执行相应的后续操作。我们建议读者使用自定义的头部字段名称，不要使用浏览器正常发送的字段名称，否则有可能会影响服务器的响应。有的浏览器允许开发人员重写默认的头部信息，但有的浏览器则不允许这样做。

调用xHR对象的getResponseHeader（）方法并传入头部字段名称，可以取得相应的响应头部信息。而调用getAl1ResponseHeaders（）方法则可以取得一个包含所有头部信息的长字符串。来看下面的例子。

~~~javascript
var myHeader = xhr.getResponseHeader("MyHeader");
var allHeaders xhr.getAllResponseHeaders();
~~~

在服务器端，也可以利用头部信息向浏览器发送额外的、结构化的数据。在没有自定义信息的情况下，getAl1ResponseHeaders（）方法通常会返回如下所示的多行文本内容：

~~~
Date: Sun, 14 Nov 2004 18:04:03 GMT 
Server: Apache/1.3.29 (Unix)
vary: Accept x-Powered-By: PHP/4.3.8
Connection: close
Content-Type: text/html; charset=iso-8859-1
~~~

这种格式化的输出可以方便我们检查响应中所有头部字段的名称，而不必一个一个地检查某个字段是否存在。

### GET请求

GET是最常见的请求类型，最常用于向服务器查询某些信息。必要时，可以将查询字符串参数追加到URL的末尾，以便将信息发送给服务器。对XHR而言，位于传入open（）方法的URL末尾的查询字符串必须经过正确的编码才行。

使用GET请求经常会发生的一个错误，就是查询字符串的格式有问题。查询字符串中每个参数的名称和值都必须使用encodeURIComponent（）进行编码，然后才能放到URL的末尾；而且所有名值对儿都必须由和号（&）分隔，如下面的例子所示。

~~~javascript
xhr.open("get","example.php?name1=value1&name2=value2",true);
~~~

下面这个函数可以辅助向现有URL的末尾添加查询字符串参数：

~~~javascript
function addURLParam(url, name, value) {
		url += (url.indexOf("?") == -1 ? "?": "&");
  	url += encodeURIComponent (name) + "=" + encodeURIComponent (value) ;
  	return url;
}
~~~

这个addURLParam（）函数接受三个参数：要添加参数的URL、参数的名称和参数的值。这个函数首先检查URI.是否包含问号（以确定是否已经有参数存在），如果没有，就添加一个问号；否则，就添加一个和号。然后，将参数名称和值进行编码，再添加到URL的末尾。最后返回添加参数之后的URL。

下面是使用这个函数来构建请求URL的示例。

~~~javascript
var url ="example.php";

//添加参数
url = adduRLParan（url，"name"，"Nicholas"）;
url = adduRLParan（url，"book"，"Professional Javascript"）;

//初始化请求
xhr.open（"get"，url,false）;
~~~

在这里使用addURLParan（）函数可以确保查询字符串的格式良好，并可靠地用于XHR对象。

### POST请求

使用频率仅次于GET的是POST请求，通常用于向服务器发送应该被保存的数据。POsT请求应该把数据作为请求的主体提交，而CET请求传统上不是这样。PosT请求的主体可以包含非常多的数据，而且格式不限。在open（）方法第一个参数的位置传入"post"，就可以初始化一个POST请求，如下面的例子所示。

~~~javascript
xhr.open("post","example.php",true);
~~~

发送POST请求的第二步就是向send（）方法中传入某些数据。由于XHR最初的设计主要是为了处理XML，因此可以在此传入XML DOM文档，传入的文档经序列化之后将作为请求主体被提交到服务器。当然，也可以在此传入任何想发送到服务器的字符串。

默认情况下，服务器对POST请求和提交Web表单的请求并不会一视同仁。因此，服务器端必须有程序来读取发送过来的原始数据，并从中解析出有用的部分。不过，我们可以使用XHR来模仿表单提交：首先将content-Type头部信息设置为application/x-www-form-urlencoded，也就是表单提交时的内容类型，其次是以适当的格式创建一个字符串。第14章曾经讨论过，POST数据的格式与查询字符串格式相同。如果需要将页面中表单的数据进行序列化，然后再通过XHR发送到服务器，那么就可以使用第14章介绍的serialize（）函数来创建这个字符串：

~~~javascript
function submitData(){
     var xhr = createXHR();        
     xhr.onreadystatechange = function(event){
          if (xhr.readyState == 4){
               if ((xhr.status >= 200 && xhr.status < 300) || xhr.status == 304){
                    alert(xhr.responseText);
                } else {
                    alert("Request was unsuccessful: " + xhr.status);
           }
      }
};
            
xhr.open("post", "postexample.php", true);
xhr.setRequestHeader("Content-Type", "application/x-www-form-urlencoded");
var form = document.getElementById("user-info");            
xhr.send(serialize(form));
}
~~~

这个函数可以将ID为"user-info"的表单中的数据序列化之后发送给服务器。而下面的示例PHP文件postexample.php就可以通过s_posT取得提交的数据了：

~~~javascript
<?php
    header("Content-Type: text/plain");   
    echo <<<EOF
Name: {$_POST['user-name']}
Email: {$_POST['user-email']}
EOF;
?>
~~~

如果不设置Content-Type头部信息，那么发送给服务器的数据就不会出现在s-PoST超级全局变量中。这时候，要访问同样的数据，就必借助$HTTP_RAW_POST_DATA。

> 与GET请求相比，POST请求消耗的资源会更多一些。从性能角度来看，以发送相同的数据计，GET请求的速度最多可达到POST请求的两倍。

## XMLHttpRequest 2级

鉴于XHR已经得到广泛接受，成为了事实标准，w3C也着手制定相应的标准以规范其行为。
XMLHtpRequest 1级只是把已有的XHR对象的实现细节描述了出来。而XMILHtpRequest 2级则进一步发展了XHR，并非所有浏览器都完整地实现了XMLHtpRequest 2级规范，但所有浏览器都实现了它规定的部分内容。

### FormData

现代Web应用中频繁使用的一项功能就是表单数据的序列化，XMLHtpRequest 2级为此定义了FormData类型。FormData为序列化表单以及创建与表单格式相同的数据（用于通过XHR传输）提供了便利。下面的代码创建了一个Formbata对象，并向其中添加了一些数据。

~~~javascript
var data = new FormData();
data.append ("name", "Nicholas");
~~~

这个append（）方法接收两个参数：键和值，分别对应表单字段的名字和字段中包含的值。可以像这样添加任意多个键值对儿。而通过向FormData构造函数中传入表单元素，也可以用表单元素的数据预先向其中填入键值对儿：

~~~javascript
var data= new FormData (document.forms[0]);
~~~

创建了FormData的实例后，可以将它直接传给XHR的send（）方法，如下所示：

~~~javascript
var xhr = createXHR();        
xhr.onreadystatechange = function(event){
     if (xhr.readyState == 4){
            if ((xhr.status >= 200 && xhr.status < 300) || xhr.status == 304){
                  alert(xhr.responseText);
             } else {
                  alert("Request was unsuccessful: " + xhr.status);
             }
      }
};
           
xhr.open("post", "postexample.php", true);
var form = document.getElementById("user-info");            
xhr.send(new FormData(form));
~~~

使用FormData的方便之处体现在不必明确地在xHR对象上设置请求头部。XHR对象能够识别传人的数据类型是FormData的实例，并配置适当的头部信息。

支持FormData的浏览器有Firefox 4+，、Safari 5+，Chrome和Android 3+版Webkito。

### 超时设定
















