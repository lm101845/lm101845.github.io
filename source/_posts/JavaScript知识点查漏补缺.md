---
title: JavaScript知识点查漏补缺
date: 2020-03-02 21:34:39
tags: JavaScript
categories: 前端理论 
top: true
---

(注1：现在这段时间打算先停一下，把之前看尚学堂视频时学过的代码重新再看一遍，《JavaScript高级程序设计》也趁着这个机会从头梳理一下，争取这段时间把之前学习JavaScript时没有透彻理解的概念，比如原型链之类的彻底理解，这个一定要做的，基础不牢地动山摇啊！)

(注2：代码是尚学堂的教学代码)

(注3：现在是2020年9月15日，这篇博文搁置吧。)

(注4：现在是2021年1月13日，这篇博文重启，就当时系统复习一遍JavaScript吧，再重新体验一遍自己当初的学习经历吧。这是是我2019年9月份的时候开始学的。)

(注5：这个JavaScript基础复习大概1,2周应该可以复习完吧，到时候就立马开始进行JavaScript高级的复习，我的ES6视频还有一些没有看完，到时候要一起把它给看了啊。)

(注7:2021年2月1日复习完，结束。)

# JavaScript简介

## 什么是语言

![](JavaScript知识点查漏补缺/01.png)

## 起源

![](JavaScript知识点查漏补缺/02.png)

## 简史

![](JavaScript知识点查漏补缺/03.png)

## 时间表

![](JavaScript知识点查漏补缺/04.png)

## 实现

![](JavaScript知识点查漏补缺/05.png)

![](JavaScript知识点查漏补缺/06.png)

## 学习内容

![](JavaScript知识点查漏补缺/07.png)

## 特点

![](JavaScript知识点查漏补缺/08.png)

## 解释型语言

![](JavaScript知识点查漏补缺/09.png)

## 类似于C和Java的语法结构

![](JavaScript知识点查漏补缺/10.png)

## 动态语言

![](JavaScript知识点查漏补缺/11.png)

## 基于原型的面向对象

![](JavaScript知识点查漏补缺/12.png)

# 基本语法

## 编写位置

![](JavaScript知识点查漏补缺/13.png)

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<!-- 可以将JS代码编写到外部JS文件中，然后通过script标签引入
		 写到外部文件中可以在不同的页面中同时引用，同时也可以利用浏览器的缓存机制
		 推荐使用的方式
		 -->
			
		<script type="text/javascript" src="script.js">
			alert("我是内部的JS代码");  
		// alert这行执行不了，只能执行执行外部的script.js代码
		// script标签一旦用于引入外部文件了，就不能再编写代码了，即使编写了浏览器也会忽略
		// 如果需要则可以再创建一个新的script用于编写新的内部代码 
		</script>
		
		<script type="text/javascript">
			alert("我是内部的JS代码");
		</script>

		<!-- 可以将script代码写到script标签中
		<script type="text/javascript">
			alert("我是script标签中的代码！！");    
			//不要忘了加分号啊
			//这里的代码并没有执行
		</script> -->

	</head>
	<body>
		<!-- 可以将JS代码编写到标签的onclick属性中  
		当我们点击按钮时，JS代码才会执行
		虽然可以写在标签的属性中，但是他们属于结构和行为耦合，不方便维护，不推荐使用
		 -->
		 <!-- 外面是双引号，alert里面就是单引号了 -->
		<button onclick="alert('讨厌,你点我干嘛~~');">点我一下</button>  
		 
		 <!-- 可以将JS代码写在超链接的href属性中，这样当点击超链接时，会执行JS代码 -->
		<a href="javascript:alert('让你点你就点啊~~');">你也点我一下</a>
		
		<!-- 这个超链接点完以后没有反应 -->
		<a href="javascript:;">你也点我一下</a>

	</body>
</html>
~~~

## HelloWorld

![](JavaScript知识点查漏补缺/14.png)

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<!-- JS代码需要编写到Script标签中 -->
		 <script type="text/javascript">    
         //type="text/javascript"写不写都行,默认就是它
		 
		 //控制浏览器弹出一个警告框		
		//这句话要加一对双引号  指令结束要写分号
		alert("这是我的第一行JS代码") ;  
	    
	   // 让计算机在页面中输出一个内容
	   // document.write()可以向body中输出一个内容 
	   document.write("看我出不出来");
	   
	  // 向控制台输出一个内容
	  // console.log（）的作用是向控制台输出一个内容
	  console.log("你猜我在哪出来呢"); 	 				
		</script> 
	</head>
	<body>
	</body>
</html>
~~~

## 注释和严格区分大小写

![](JavaScript知识点查漏补缺/16.png)

![](JavaScript知识点查漏补缺/15.png)

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			/* 
			多行注释
			JS注释
			 多行注释，注释中的内容不会被执行，但是可以在源代码中被查看
			 要养成良好的编写注释的习惯，也可以通过注释来对代码进行一些简单的调试
			 */
			
			//单行注释
			//alert("hello");
			//document.write("hello");
			//console.log("hello");
			
			/* 
			 *1.JS中严格区分大小写（HTML里面不区分）
			 *2.JS中每一条语句以分号(;)结尾
			 * 	-如果不写分号，浏览器会自动添加，但是会消耗一些系统资源
			 * 	-而且有些时候，浏览器会加错分号，所以在开发中分号必须写
			 *3.JS会忽略多个空格和换行，所以我们可以利用空格和换行对代码进行格式调整
			 */
			Alert("hello");   
			//会报错,不认识Alert  Alert is not defined
		</script>
	</head>
	<body>
	</body>
</html>
~~~

## 标识符

![](JavaScript知识点查漏补缺/17.png)

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			/* 
			 *标识符
			 *  -在JS中所有的可以由我们自主命名的都可以称为是标识符
			 *  -例如：变量名、函数名、属性名都属于标识符
			 * 	-命名一个标识符时需要遵守如下的规则
			 * 	1.标识符中可以含有字母、数字、下划线（_）、dollor符号（$）
			 * 	2.标识符不能以数字开头
			 * 	3.标识符不能是ES中的关键字或保留字	
			 * 	4.标识符一般采用驼峰命名法
			 * 		-首字母小写，每个单词的开头字母大写，其余小写
			 * 		helloWorld
			 */
            
// 			var a_1_$ = 123;		
// 			console.log(a_1_$);
		</script>
	</head>
	<body>
	</body>
</html>
~~~

## 关键字和保留字符

![](JavaScript知识点查漏补缺/18.png)

## 其他不建议使用的标识符

![](JavaScript知识点查漏补缺/19.png)

## 变量和字面量

![](JavaScript知识点查漏补缺/20.png)

~~~javascript

<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			/* 
			 *字面量：都是一些不可改变的值（可以理解成常量）
			 * 	比如 1 2 3 4 5
			 * 	字面量都是可以直接使用的，但是我们一般不会直接使用字面量
			 * 	//alert(123123123);
			 * 
			 *变量：变量可以用来保存字面量，而且变量的值是可以任意改变的（变量像一个仓库）
			 * 	   变量可以更加方便使用，所以在开发中都是通过变量去保存一个字面量，而很少直接使用字面量
			 */  
			
			//声明变量
			//在JS中使用var关键字来声明一个变量
			var a;
			
			//为变量赋值
			a = 123;
			a = 456;
			
			//声明和赋值可以同时进行
			var b = 789;
			
			var age = 80;
			console.log(a);  //456
			console.log(b);  //789
		</script>
	</head>
	<body>
	</body>
</html>
~~~

## 数据类型

![](JavaScript知识点查漏补缺/21.png)

### String类型

![](JavaScript知识点查漏补缺/22.png)

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			/*  
			*数据类型指的就是字面量的类型
			* 在JS中一共有6中数据类型(首字母大写)
			* 		String 	字符串
			* 		Number 	数值
			* 		Boolean 布尔值
			* 		Null 	空值
			* 		Undefined 未定义
			* 		Object  对象
			 * 其中String 、Number、Boolean、Null、Undefined属于基本数据类型
			 * 而Object属于引用数据类型
			*/
		   
		   /* 
		   *String字符串
		   * 	-在JS中字符串需要使用引号引起来
		   * 	-使用双引号或单引号都可以，但是不要混着用
		   * 	-引号不能嵌套，双引号里面不能放双引号（但能放单引号），
		   		 单引号里面不能放单引号（但能放双引号）
		   */
		  
		  //var str = "hello";
		  //var str = 'hello'  和上面效果一样的
		  //str = "我说："今天天气真不错！"";  不可以这样
		  
		  
		  /* 
		  *在字符串中我们可以使用\作为转义字符，当表示一些特殊符号时可以使用\进行转义
		  * 比如：
		  * str = "我说：\"今天天气真不错！\"";   
		  * 用斜杠来表示转义，2个斜杠表示右边的双引号只是一个普通的双引号
		  * \" 可以用来表示一个双引号
		  * \' 可以用来表示一个单引号
		  * \n 可以用来表示一个换行
		  * \t 可以用来表示一个制表符
		  * \\表示一个\  (左边的斜杠是用来转义斜杠的)
		  */
            
		  //str = '我说："今天天气真不错！"'; 
          //这样是可以的
            
		  //srt = "我说：\"今天天气真不错！\"";
		  //str = "我说：\"今天\n天气真不错！\"";
		  //str = "我说：\"今天\t天气真不错！\"";
		  //str = "\\";
		  
		  //输出字面量字符串str--加上双引号就是字符串了
		  //alert("str");
		  
		  //输出变量str--变量的值是多少,它就输出多少
		  //alert(str);
		  
		  //var str2 = "hello";  
          //var只在声明变量的时候写 应用题只有在最开始的时候设x,往后就不用设了,直接拿来用了
		  
		  //str2 = "你好";  //第二次赋值,谁在下面谁有效
		  //str2 = 3;
		  
		  //var str3 = 8;  //声明新的变量str3,所以前面还得有var 
		</script>
	</head>
	<body>
	</body>
</html>
~~~

### Number类型

> 注意NaN、Infinity这些知识点。

![](JavaScript知识点查漏补缺/23.png)

~~~javascript
<!DOCTYPE html> 
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			/*  
			*在JS中所有的数值都是Number类型
			* 包括整数和浮点数（小数）
			*/
		   
		   
		   //数字123
		   var a = 123;
		   //a = 456.789;
		   
		   //字符串123
		   var b = "123";
		   
		   /* 
		   *可以使用一个运算符typeof来检查一个变量的类型
		   * 语法：typeof 变量
		   * 检查字符串时，会返回string（小写）
		   * 检查数值时，会返回number(小写)
		   * 使用typeof检查Infinity也会返回Number
		   * NaN是一个特殊的数字，表示Not a Number
		   * 使用typeof检查NaN也会返回一个number(小写)
		   */
		  console.log(Number.MAX_VALUE)  
		  //这是JS中可以表示的最大值   1.7976931348623157e+308
		  a = Number.MAX_VALUE*Number.MAX_VALUE     
		 //Infinity   正无穷大    -Infinity   负无穷大
		  //如果使用Number表示的数字超过了最大值,则会返回一个Infinity,超过最小值会返回-Infinity 
		  a = Infinity;
		  a = "abc" * "bcd";
		  a = NaN;
		  //console.log(typeof a)    //检查a的类型,并把结果显示在控制台上  
		  
		  a = Number.MIN_VALUE;
		  console.log(a);     
		 //返回的是0以上的最小值 5e-324   而不是-1.7976931348623157e+308
		  
		  //在JS中整数的运算可以基本保证精确	
		  var c = 123 + 456;
		  
		  //如果使用JS进行浮点运算,可能得到一个不精确的结果
		  //十进制里不能精确表示1/3,二进制里不能精确表示1/10  
		  // 计算机是离散的，所以无法十分准确的表示小数，只能保留小数点后一定位数，近似表示小数
		  //所有的语言都有这个问题,很多语言可以解决,但是JS很难解决
		  //所以千万不要使用JS进行对精确度要求比较高的运算(算钱）)
		  var c = 0.1 + 0.2;   //结果是0.30000000000000004
		  console.log(c);
		  
		  console.log(typeof b)
		   console.log(a);
		   console.log(b);
		</script>
	</head>
	<body>
	</body>
</html>
~~~

#### 其他进制的数字

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			var a = 123;
			/* 
			*在JS中，如果需要表示16进制的数字，则需要以0x开头
			* 		如果需要表示8进制的数字，则需要以0开头
			* 		如果需要表示2进制的数字，则需要以0b开头（但是不是所有的浏览器都支持）
			* 
			*/
		   
		   //十六进制
		   a = 0x10;
		   a = 0xff;
		   
		   //八进制
		   a = 050;
		   
		   //二进制--用的比较少
		   a = 0b10;
		   
		   //像"070"这种字符串,有些浏览器会当成8进制解析,有些会当成10进制解析
		   a = "070";
		   
		   a = "";	 //NaN
		   //可以在parseInt()中传递第二个参数,来指定数字的进制
		   a = parseInt(a,10);
		   console.log(typeof a)		   
		   console.log(a);  
		  //输出的时候都会转换成10进制输出
		</script>
	</head>
	<body>
	</body>
</html>
~~~

#### 强制类型转换(不熟了)

![](JavaScript知识点查漏补缺/24.png)

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			//方法   函数   参数		
			/* 
			 *强制类型转换
			 * 	-指将一个数据类型强制转换为其他的数据类型
			 * 	-类型转换主要指，将其他的数据类型，转换为
			 * 		String Number Boolean 
			 * 
			 */
			
			
			/*  
			*将其他的数据类型转换为String
			* 	方式1：
			* 		-调用被转换类型的toString()方法
			* 		-该方法不会影响到原变量，它会将转换的结果返回
			* 		-但是注意：null和undefined这两个值没有toString方法
			* 			如果调用他们的方法，会报错
			* 
			* 
			* 	方法2：
			* 		-调用String()函数，并将被转换的数据作为参数传递给函数    
			* 		 （函数不等于方法，函数没有点，方法有点!!!!!!!!!!!!!!!!!!!!!!）
			*  		-使用String()函数做强制类型转换：
			* 			对于Number和Boolean实际上就是调用的toString方法
			* 			对于null和undefined,就不会调用toString方法
			* 				它会将null直接转换为"null"
			* 				它会将undefined直接转换为"undefined"	
			*/
		   
			var a = 123;
			
			//调用a的toString（）方法
			//调用xxx的yyy方法,就是xxx.yyy()
			//var b = a.toString();   
			//方法都是有执行结果的，这个方法的作用是可以将a转换成字符串
			a = a.toString();  		 
			//将a原来的数据类型给覆盖掉了
			
			a = true;
			a = a.toString();
			
			a = null;
			//a = a.toString()   //报错
			
			a = undefined;
			//a = a.toString();  //报错
			
			//下面的是函数，上面的是方法（有点）
			a = 123;
			//调用String函数,来将a转换成字符串
			a = String(a);   
			//s是大写的,小括号里的是参数a,表示将a转换成字符串
			
			a = null;
			a = String(a);
			
			a = undefined;
			a = String(a);
			 
			console.log(typeof a);
			console.log(a);  	 
			
			//console.log(typeof b);
			//console.log(b);		//这是字符串123
		</script>
	</head>
	<body>
	</body>
</html>
~~~

### Boolean类型

![](JavaScript知识点查漏补缺/25.png)

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			/*  
			*Boolean 布尔值
			* 布尔值只有两个
			* true-表示逻辑上真
			* false-表示逻辑上假
			* 
			* 使用typeof检查一个布尔值，会返回boolean		
			*/
		   
		   var bool = true;
		   console.log(bool);
		   console.log(typeof bool);
		</script>
	</head>
	<body>
	</body>
</html>
~~~

### Undefined类型

![](JavaScript知识点查漏补缺/26.png)

### Null类型

[javascript中的null，对象系统还是非对象系统？](https://www.cnblogs.com/ChengWuyi/p/8648164.html)

![](JavaScript知识点查漏补缺/27.png)

> null 有时会被当作一种对象类型，但是这其实只是语言本身的一个 bug，即对 null 执行 typeof null 时会返回字符串 "object"。实际上，null 本身是基本类型。

~~~javascript

<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			/*  
			*Null(空值)类型的值只有一个，就是null
			* null这个值专门用来表示一个为空的对象----对象！！！！！！！！！(其实不是)
			* 使用typeof检查一个null时，会返回object
			* 这个是语言的一个bug，专门有面试题问null是不是一个对象，其实是不是的。
			* 
			* undefined（未定义）类型的值只有一个，就是undefined
			* 当声明一个变量，但是并不给变量赋值时，它的值就是underfined
			* 声明了！！！但是没有赋值
			* 使用typeof检查一个undefined时也会返回undefined
			*/
		   
		   var a = null;
		   
		   var b;
		   var b = undefined; //也行
		   
		   console.log(typeof a);	//object
		   console.log(typeof b);	//undefined
		   console.log(null == undefined);  //true
		</script>
	</head>
	<body>
	</body>
</html>
~~~

## 运算符

![](JavaScript知识点查漏补缺/28.png)

### 算数运算符

![](JavaScript知识点查漏补缺/29.png)

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			/*  
			*运算符也叫操作符，通过运算符可以对一个或多个值进行运算,并获取运算结果
			* 比如：typeof就是运算符，可以来获得一个值的类型
			* 		它会将该值的类型以字符串的形式返回
			* 		number string boolean undefined object
			* 
			* 算术运算符
			* 		当对非Number类型的值进行运算时，会将这些值转换为Number,然后再进行计算
			* 		任何值对NaN做运算，都得NaN (NaN就是一个黑洞)
			* 		+ ：
			* 			可以对两个值进行加法运算，并将结果返回
			* 			如果对两个字符串进行加法运算，则会做拼串（将两个字符串拼接成一个字符串，并返回）
			* 		    任何值和字符串做加法运算，都会先转换为字符串，然后再和字符串做拼串的操作
			* 
			* 		- :
			* 			可以对两个值进行减法运算，并将结果返回
			* 		* ：
			* 			可以对两个值进行乘运算，并将结果返回
			* 		/ ：
			*			可以对两个值进行除法运算，并将结果返回
			* 		% ：
			* 			%取模运算（取余数）
			*/
            
		   var a = 123;
		
		   var result = typeof a;
		   console.log(result);   	//number
		   console.log(typeof a);	//number
		   console.log(typeof result);	
		  //typeof的返回类型是一个字符串 string   它会将该值的类型以字符串的形式返回
		   
		   resule = a + 1;  //a还是123,不变,result是124,结果是result
		   console.log(result)
		   
		   a = a + 1;
		   console.log(a)  //如果希望a的值变,那么设a = a+1 即可
		   
		   result = true + 1;		//2
		   result = true + false;	//1
		   result = 2 + null;		//2
		   result = 2 + NaN;        //NaN
			 
		   result = "123" + "456";		
		  //两个字符串相加的结果是把两个字符串拼在了一起，俗称拼串  123456
		   result = "你好" + "世界";
			 
		   var str = "锄禾日当午,"  +      
           //双引号必须在同一行,不能换行,否则会报错 用加号连接起来就可以换行了
			"汗滴禾下土," +			
           //写一些比较长的字符串的时候,可以使用加号来给他们拼到一起,这样结构可以更加清楚一些
			"谁知盘中餐," +
			"粒粒皆辛苦";
			 console.log(str);		
					 
			 result = 123 + "1";		//1231
			 result = true + "hello";   //truehello
			 
			 //任何值和字符串相加都会转换为字符串,并作拼串操作

			 /* 
			 *我们可以利用这一特点，来将一个任意的数据类型转换为String
			 * 	我们只需要为任意的数据类型 + 一个""即将其转换为String
			 * 	这是一种隐式的类型转换，由浏览器自动完成，实际上它也是调用String()函数
			 */
			 var c = 123;
			 //c = string(c);
			 c = c + "";  //和上面的效果一样,也可以把c变成字符串
			 //console.log(typeof c);
			 //console.log("c = "+ c );
			 
			 //console.log(typeof result);  //两个字符串相加的类型还是字符串 string
		    //console.log(result);   
			
			result = 1 + 2 + "3";		//33
			result = "1" + 2 + 3;  //123
			
			result = 100 - "1";		//99  这里的字符串1转换成number1了
			
			result = 2 * "8";			//16
			
			result = 2 * undefined;		//NaN
			
			result = 2 * null;			//0
			
			result = 3 / 2 ; 			//1.5
			
			/*  
			*任何值做-  * / 运算时，都会自动转换为Number(可以利用这个做类型转换)
			* 	我们可以利用这一特点做隐式的类型转换
			* 	可以通过为一个值-0 *1 /1来将其转换为Number(注：+0不行！！！！！！！！！会拼串)
			* 	原理和Number()函数一样，但是使用起来更加简单
			*/

		  	var d = "123";
			//d = Number(b);
			d = d - 0;  //和上面的效果一样,也可以把d变成数字
			console.log(typeof d);
			console.log(d);
			
			
			result = 9 % 3;		  //0
			result = 9 % 4;			//1
			result = 9 % 5;			//4
			result = 9 % 15;	  //9
			console.log("result = " + result);
		</script>
	</head>
	<body>
	</body>
</html>
~~~

#### 一元运算符

~~~javascript

<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			/*  
			*一元运算符，只需要一个操作数
			* 	+  正号  正号不会对数字产生任何影响
			* 		
			* 	-  负号  负号可以对数字进行符号取反
			* 
			* 	对于非Number类型的值,
			* 		它会将先转换为Number,然后再运算
			* 		可以对一个其他的数据类型使用 + ，来将其转换为Number	（比-0 ，*1 ，/1 还简单）
			* 		它的原理和Number()函数一样
			* 
			*/
		   
		   var a = 123;
		   //a = +a;
		   //a = -a;
		   
		   a = true;
		   a = -a;
		   
		   a = "18";
		   a = -a;
		   a = +a;
		   console.log("a=" + a);
		   console.log(typeof a);
		   
		   
		   var result = 1 + "2" + 3   //123
		   var result = 1 + +"2" + 3  //6  在字符串2前面加一个正号会将字符串2转换为数字2

		   console.log("result=" + result);
		   
		</script>
	</head>
	<body>
	</body>
</html>
~~~

### 自增和自减

[javascript中的自增自减运算?](https://segmentfault.com/q/1010000018458245)

![](JavaScript知识点查漏补缺/30.png)

![](JavaScript知识点查漏补缺/31.png)

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			/*  
			*自增++
			* 		-通过自增可以使变量在自身的基础上增加1	
			* 		-对于一个变量自增以后，原变量的值会立即自增1（这是少数几个会影响到原变量的运算符）
			* 		-自增分成两种：后++（a++） 和 前++（++a）
			* 			无论是a++ 还是++a,都会立即使原变量的值自增1（对原变量来说是没区别的）
			* 				不同的是a++ 和++a 的值不同
			* 			a++的值等于原变量的值（自增以前的值）
			* 			++a的值等于原变量的新值（自增以后的值）
			* 
			* 自减--
			* 		-通过自减可以使变量在原来的基础上减1
			* 		-自减分成两种：后--（a--） 和 前--（--a）
			* 			无论是a--还是--a,都会立即使原变量的值自减1
			* 				不同的是a-- 和--a 的值不同
			* 			a--是变量的原值（自减以前的值）
			* 			--a是变量的新值（自减以后的值）
			* 
			* 			
			*/
		   
		   var a = 1;
		   //a = a + 1;
	
		   //使a自增1
		   //a++;		//++写在a的后面,和上面的a = a+1 效果一样
		   //a++;		//每调用一次,加一个1
		   
		   //++a;		//++a和a++的效果一样
		   console.log("a++=" + a++);		//a++ 为1 (是自增以前的旧a的值)
		   console.log("++a=" + ++a)		//++a 为2 (是自增以后的新a的值)
		   console.log("a ="+ a);	//a 为  2
		   
		   var c = 10;
		   //使c自增1
		   //第一次c++,是在10的基础上自增		
			
		   console.log(c++);	//10  第一次自增,在10的基础上自增
				 
		   c++;					//第二次自增,在11的基础上自增
		   console.log(c++);	//12

		   //第二次c++,是在11的基础上自增
		   c++;		   
		   console.log(c++);	//14 
		   
		   
		   var d = 20;
		   console.log(++d);		//21
		   console.log(++d);		//22
		   
		   //20 + 22 +  22(e自增了2次)
		   //var e = 20;
		   //var result = e++ + ++e + e;			//从左到右执行
		   //console.log("result=" + result);		//41
		   
		   var e = 20;
		   e = e++;		
		   /* 
		   *e = e++ 等价于
		   * var f = e++;
		   * 	e = f;
		   */
		   console.log(e);		
		 //20  e++为20,e为21,又把e++(20)赋值给e,则e又变成了20(20-->21-->20--又回到了起点)
		   
		   var num = 10;
		   //num--;
		   //--num;
		   //console.log(num--);		//10
		   console.log(--num);			//9(前提是上面的一行注释掉）
		   console.log("num=" + num);	//9

		</script>
	</head>
	<body>
	</body>
</html>
~~~

### 逻辑操作符

![](JavaScript知识点查漏补缺/32.png)

#### 非

![](JavaScript知识点查漏补缺/33.png)

#### 与

![](JavaScript知识点查漏补缺/34.png)

~~~javascript

<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			
			/*
			 * && || !布尔值的情况
			 * 	-对于非布尔值进行与或运算时，
			 * 		会先将其转换为布尔值， 然后再运算,并且返回原值
			 * 	-与运算：--（返回的是原值，而不是true或者false）
			 * 		如果第一个值为true,则必然返回第二个值
			 * 		如果第一个值为false,则必然返回第一个值
			 * 
			 * 	-或运算
			 * 		如果第一个值为true,则必然返回第一个值
			 * 		如果第一个值为false,则必然返回第二个值
			 */
			//true && true 
			//与运算,如果两个值都为true,则返回后面的(后面的！！！！！！)
			var  result = 1 && 2;  //2
				 result = 2 && 1;  //1
			
			
			//与运算,如果两个值中有false,则返回靠前的false
			//false && true	 
				 result = 0 && 2;   //0
				 result = 2 && 0;   //0
				 
			//false && false
				 result = NaN && 0;   //NaN
				 result = 0 && NaN;   //0
				
				//true || true
				//如果第一个值为true,则直接返回第一个值
			    result = 5 || 2;   		//5
				
				//如果第一个值是false,则直接返回 第二个值
				result = NaN || 1;     // 1
				result = NaN || 0;     // 0
				
				result = "" || "hello";  //hello  ""是false
				result = -1 ||0;      //-1
			
				
			console.log("result=" + result);  
		</script>
	</head>
	<body>
	</body>
</html>
~~~

#### 或

![](JavaScript知识点查漏补缺/35.png)

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<script type="text/javascript">
			/*  
			 *JS中为我们提供了3种逻辑运算符  
			 * &&  与
			 * 		 -&&可以对符号两侧的值进行与运算并返回结果
			 * 		 -运算规则
			 * 			-两个值中只要有一个值为false就返回false
			 * 				只有两个值都为true时才返回true
			 * 
			 * 		-JS中的"与"属于短路的与,
			 * 				如果第一个值为false,则不会看第二个值
			 * 
			 * ||  或
			 * 		-||可以对符号两侧的值进行或运算并返回结果
			 * 		-运算规则：
			 * 			-两个值中只要有一个true,就返回true
			 * 				如果两个值都为false,才返回false
			 * 		-JS中的"或"属于短路的或	
			 * 				如果第一个值为true,则不会看第二个值
			 * 
			 * ！  非
			 * 		 -！可以对一个值进行非运算
			 * 		 -所谓非运算就是值对一个布尔值进行取反操作
			 * 				true变false    false 变 true
			 * 		 -如果对一个值进行两次取反，它不会变化
			 * 		 -如果对非布尔值进行运算，则会将其转换成布尔值，然后再对其进行取反
			 * 			所以我们可以利用该特点，来将一个其他的数据类型转换为布尔值
			 * 			可以为一个任意数据类型取两次反，来将其转换为布尔值
			 * 			原理和Boolean()函数一样
			 */
			
			var a = true;
			//对a进行非运算
			a = !a;
			a = !!a; //两次取反还是原值
			console.log("a=" + a);
			
			var b = 10;
			b = !b;
			
			console.log("b=" + b);  //false
			console.log(typeof b);
			
			//只要有一个false,就返回false
			var result = true && false;   //true
			var result = true && false;   //false
			var result = false && false;   //false

			console.log("result=" + result);
			
			//第一个值为true会检查第二个值
			true&&alert("看我出不出来");  //可以出来
			
			//第一个值为false,不会检查第二个值
			false&&alert("看我出不出来");  //出不来
			
			
			//两个都是false,则返回false
			result = false || false;		//false
			
			result = true || false;			//true
			
			result = false || true;			//true
			
			result = true || true;      //true
			console.log("result=" + result);
			
			
			//第一个值为false,则会检查第二个值
			false || alert("123");   //123出来了
			
			//第一个值为true,则不再检查第二个值
			true || alert("123");	
		</script>
	</head>
	<body>
	</body>
</html>
~~~

### 赋值运算符

![](JavaScript知识点查漏补缺/36.png)

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 *  =:
		 *  	可以将符号右侧的值赋值给符号左侧的变量
		 *  +=:
		 *  	a = a + 5; 等价于a += 5;
		 *  -=:
		 *  	a = a - 5; 等价于a -= 5;
		 *  *=:
		 *  	a = a * 5; 等价于a *= 5;
		 *
		 *  \=:
		 *  	a = a \ 5; 等价于a \= 5;
		 *
		 *  %=:
		 *  	a = a % 5; 等价于a %= 5;
		 */
		var a = 10;	
		a = a + 5;   //等价于a+=5;
		console.log("a = " + a);					
	</script>
</head>
<body>
	
</body>
</html>
~~~

### 关系运算符

![](JavaScript知识点查漏补缺/37.png)

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 通过关系运算符可以比较两个值之间的大小关系
		 * 如果关系成立它会返回true,否则返回false
		 *
		 * 非数值的情况
		 * 	-对于非数值进行比较时，会将其转换为数字,然后再比较
		 */
		console.log(1 >= true);   //true
		console.log(1 > "0");	  //true
		console.log(10 > null);	  //true 
		console.log(10 > NaN);	  //false   任何值和NaN做任何比较都是false
		console.log(10 > "hello");	  //false 
		console.log(true > false);   //true

		//比较两个字符串时，比较的是字符编码
		console.log("a" < "b");   //true

		//比较字符串编码是一位一位进行比较，如果两位一样，则比较下一位
		console.log("abc" < "b");   //true

		//比较中文没有意义
		console.log("我" > "你");  //true

		//如果比较两个字符串类型的数字，可能得到不可预期的效果
		//注意，在比较两个字符串型的数字时，一定要转型
		console.log("111111454444" < "5");  //true

	</script>
</head>
<body>
	
</body>
</html>
~~~

### 相等

![](JavaScript知识点查漏补缺/38.png)

### 全等

![](JavaScript知识点查漏补缺/39.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 相等运算符用来表示两个值是否相等
		 * 		相等则返回true,否则false
		 *
		 * 使用==来比较两个值时，如果值的类型不同，
		 * 		则会自动进行类型转换(大部分情况转换成数字)，将其转换为相同的类型
		 *
		 * undefined衍生自null,
		 * 	所以这两个值做相等判断时，会返回true
		 *
		 * NaN不和任何值相等,包括他本身
		 *
		 * 不相等：
		 * 	!=
		 * 	不相等也会对变量进行自动类型转换
		 *
		 * 全等：
		 * 	===
		 * 	用来判断两个值是否全等，它和相等类似，不同的是它不会做自动类型转换
		 * 		如果两个类型不同，直接返回false
		 */
		
		var a = 10;
		console.log(a == 10);  //true
		console.log("1" == 1);  //true
		console.log(true == "1");  //true
		console.log(null == "0");  //false  此处null没有转换成number
		console.log(null == undefined);  //true
		console.log(NaN == undefined);   //false
		console.log(NaN == NaN);   //false

		var b = NaN;
		console.log(b == NaN);  //false

		//可以通过isNaN()函数判断一个值是否是NaN
		//	如果该值是NaN,则返回true,否则返回false
		console.log(isNaN(b));   //true

		console.log("1" != 1);  //false

		console.log("123"==123);  //true
		console.log("123"===123); //false  类型不一样，直接返回false

		console.log(null == undefined);  //true
		console.log(null === undefined);  //false
	</script>
</head>
<body>
	
</body>
</html>
~~~

### 逗号

![](JavaScript知识点查漏补缺/40.png)

### 条件运算符

![](JavaScript知识点查漏补缺/41.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 条件运算符也叫三元运算符
		 * 	语法：
		 * 		条件表达式？语句1：语句2；
		 * 	-执行的流程	
		 * 		条件运算符在执行时，首先对条件表达式进行求值
		 * 			如果该值是true,则执行语句1，并返回执行结果
		 * 			如果该值是false,则执行语句2，并返回执行结果
		 *
		 * 	如果条件表达式的结果是一个非布尔值，
		 * 		会将其转换为布尔值，然后再将其运算
		 */ 
		
		//true?alert("语句1")：alert("语句2");
		
		var a = 10;
		var b = 20;
		var c = 30;
		a > b ? alert("a大"):alert("b大");

		//获取a和b中的最大值
		var max = a > b ? a : b;
		console.log("max = " + max);

		//获取a,b,c中的最大值
		max = max > c ? max : c;
		console.log("max = " + max);

		//不推荐使用这种写法，不方便阅读
		var max = a > b ? (a > c ? a : c ): (b > c ? b :c);
		console.log("max = " + max);

		"hello" ? alert("语句1")：alert("语句2");

		
	</script>
</head>
<body>
	
</body>
</html>
~~~

### 运算符的优先级

![](JavaScript知识点查漏补缺/42.png)

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 *  ,运算符
		 *  使用逗号可以分割多个语句，一般可以在声明多个变量时使用，
		 *
		 * 就和数学中一样，在JS中也有优先级
		 * 		比如：先乘除，后加减
		 *
		 * 在JS中有个符号优先级的表，在表中位置越靠上优先级越高，优先级越高越优先计算
		 * 如果优先级一样，则从左往右计算
		 *
		 * 如果碰到拿不准的优先级，可以添加一个括号提高优先级
		 */
		
		//使用,运算符可以同时声明多个变量
		var a , b , c ;
		//var a ;
		//var b ;
		//var c ;
		alert(b);

		//可以同时声明多个变量并赋值
		var a = 1 , b = 2 ,c = 3;
		alert(c);

		var result = 1 + 2 * 3;

		/**
		 * 如果||或的优先级高，或者两个一样高，则应该返回3
		 * 如果&与的优先级高，则应该返回1
		 * 
		 */
		var result = 1 || 2 && 3;
		console.log("result = " + result);   //1
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 语句

![](JavaScript知识点查漏补缺/43.png)

### 代码块

![](JavaScript知识点查漏补缺/44.png)

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 我们的程序是由一条一条语句构成的
		 * 	语句是按照自上向下的顺序一条一条执行的
		 * 	在JS中使用｛｝来为语句分组
		 * 		同一个｛｝中的语句我们称为是一组语句
		 * 		它们要么都执行，要么都不执行
		 * 		一个｛｝中的语句我们也称为一个代码块
		 * 		在代码块的后面就不用再编写分号了
		 *
		 * JS中的代码块只具有分组的作用，没有其他的用途(不会隔离)
		 * 		代码块内部的内容在外部是完全可见的
		 */
		{	
			var a  = 10;
			alert("hello");

			console.log("你好");

			document.write("语句");
		}


		console.log("a = " + a);   //会显示出来，不会因为代码块的存在而隔离
		{
			alert("hello");

			console.log("你好");

			document.write("语句");
		}


		{
			alert("hello");

			console.log("你好");

			document.write("语句");
		}

	</script>
</head>
<body>
	
</body>
</html>
~~~

### 条件语句

![](JavaScript知识点查漏补缺/45.png)

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 流程控制语句
		 * 	 -JS中的程序是从上到下一行一行执行的
		 * 	 -通过流程控制语句可以控制程序执行流程
		 * 	 	使程序可以根据一定的条件来选择执行 
		 * 	 -语句的分类：
		 * 	 	1.条件判断语句
		 * 	 	2.条件分支语句
		 * 	 	3.循环语句
		 *
		 *
		 * 条件判断语句：
		 * 	-使用条件判断语句可以在执行某个程序之前进行判断 
		 * 		如果条件成立才会执行语句，条件不成立则语句不执行
		 * 		
		 * 	-if语句
		 * 	-语法一：
		 * 		if(条件表达式)
		 * 			语句
		 *
		 * 		if语句在执行时，会先对条件表达式进行求值判断，
		 * 		如果条件表达式的值为true,则执行if后的语句，
		 * 		如果条件表达式的值为false,则不会执行if后的语句
		 *
		 * 			if语句只能控制紧随其后的那个语句
		 * 				如果希望if语句可以控制多条语句
		 * 				可以将这些语句统一放到代码块中
		 * 			if语句后的代码块不是必须的，是在开发中尽量写上代码块，即使if后只有一条语句
		 * 	 
		 * 	 				 		 
		 */
		
		var a = 8;

		if(a > 10){
			alert("a比10大");
			alert("谁也管不了我");     //因为没有{}就管不了,有{}就可以管
		}

		var b = 15;

		if(b > 10 && b <= 20){
			alert("b大于10，并且b小于等于20");
		}

	</script>
</head>
<body>
	
</body>
</html>
~~~

#### if...else语句

![](JavaScript知识点查漏补缺/46.png)

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * if语句
		 * 	 语法二:
		 * 	 	if(条件表达式){
		 * 	 		语句...
		 * 	 	}else{
		 * 	 		语句...
		 * 	 	}
		 *
		 * if...else...语句
		 * 		当该语句执行时，会先对if后的条件表达式进行求值判断，
		 * 			如果该值为true,则执行if后的语句
		 * 			如果该值为false,则执行else后的语句
		 *
		 *
		 * 	 语法三：
		 * 	 	if(条件表达式){
		 * 	 		语句...
		 * 	 	}else if(条件表达式){
		 * 	 		语句...
		 * 	 	}else if(条件表达式){
		 * 	 		语句...
		 * 	 	}else{
		 * 	 		语句...
		 * 	 	}
		 *
		 * if...else if...else
		 * 		当该语句执行时会从上而下对条件表达式进行判断 
		 * 		如果值为true,则执行当前的语句。
		 * 		如果值为false,则继续向下判断
		 * 		如果所有的条件都不满足，则执行最后的else语句
		 * 		该语句中只会有一个代码块被执行，一旦有一个被执行，其余的都不会执行
		 * 	 
		 */
		
		var age = 60;

		if (age >= 60){
			alert("你已经退休了");
		}else{
			alert("你还没退休");
		}

		var age1 = 200;
		if(age1 > 100){
			alert("活着挺没意思的");
		}else if(age1 > 80){
			alert("你也老大不小了");
		}else if(age1 > 60){
			alert("你也退休了");
		}else if (age1 > 30){
			alert("你已经中年了");
		}else if(age1 > 17){
			alert("你已经成年了");
		}else{
			alert("你还是个小孩子");
		}

		var age2 = 18;
		if(age2 > 17 && age <= 30){
			alert("你已经成年了");
		}else if(age2 > 30 && age2 <= 60){
			alert("你已经中年了");
		}else{
			alert("你年龄挺大了");
		}

	</script>
</head>
<body>
	
</body>
</html>
~~~

##### if语句例子

![](JavaScript知识点查漏补缺/47.png)

#### switch...case语句

![](JavaScript知识点查漏补缺/48.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 条件分支语句也叫switch语句	
		 * 	语法：
		 * 		switch(条件表达式1){
		 * 			case 条件表达式2:
		 * 				语句...:
		 * 				break;
		 *
		 * 			case 条件表达式2:
		 * 				语句...:
		 * 				break;
		 * 				
		 * 			case 条件表达式2:
		 * 				语句...:
		 * 				break;
		 *
		 * 			default:
		 * 				语句...:
		 * 				break;
		 * 		}
		 *
		 * 执行流程：
		 * 			switch...case...语句
		 * 			在执行时会依次将case后的表达式2和switch后的条件表达式1的值进行全等(===)比较，
		 * 				如果比较结果为true,则从当前case处开始执行代码。
		 * 					当前case后的所有代码都会执行，我们可以在case的后面跟着一个break
		 * 					这样可以确保只会执行当前case后的语句，而不会执行其他的case
		 * 					
		 * 				如果比较结果为false,则继续向下比较
		 *
		 * 				如果所有的比较结果都为false,则只执行default后的语句
		 * 				（相当于if...else的else）
		 *
		 * switch语句和if语句的功能实际上有重复的，使用switch可以实现if的功能，
		 * 		同样使用if也可以实现switch的功能，所以我们使用时，可以根据自己的习惯使用
		 * 		（实际中if用的多一些，switch的条件比较清楚）
		 * 				
		 */
		
		//根据number的值，输出对应的中文
		var num = 1;
		switch(num){
			case 1:
			console.log("壹");
			break;    //使用break可以来退出switch语句，当前case后的所有代码就不会都执行了

			case 2:
			console.log("贰");
			break;

			case 3:
			console.log("叁");
			break;

			case 4:
			console.log("肆");
			break;

			case 5:
			console.log("伍");
			break;

			case 6:
			console.log("陆");
			break;

			case 7:
			console.log("柒");
			break;   

			default:
			console.log("非法数字");
			break;  //最后一个case,写不写都行，但还是尽量给它写上比较好
		}
	</script>
</head>
<body>
	
</body>
</html>
~~~

### 循环语句

![](JavaScript知识点查漏补缺/49.png)

#### while

![](JavaScript知识点查漏补缺/50.png)

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 假如投资的年利率为5%，试求从1000块增长到5000块，需要花费多少年

		 */
		
		//先定义一个变量来表示当前的钱数
		var money = 1000;

		//定义一个计数器
		var count = 0;
		//定义一个while循环来计算每年的钱数		
		while(money < 5000){
			money = money * 1.05
			count++;
		}
		/*第一年的钱数
		money = money * 1.05;

		//第二年的钱数
		money = money * 1.05;*/
		console.log("一共需要" + count + "年");
	</script>
</head>
<body>
	
</body>
</html>
~~~

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title>if练习1</title>
		<script type="text/javascript">
			/*
			 * 	从键盘输入小明的期末成绩:
			 *	当成绩为100时，'奖励一辆BMW'
			 *	当成绩为[80-99]时，'奖励一台iphone15s'
			 *	当成绩为[60-80]时，'奖励一本参考书'
			 *	其他时，什么奖励也没有
			 */
			
			/*
			 * prompt()可以弹出一个提示框，该提示框中会带有一个文本框，
			 * 	用户可以在文本框中输入一段内容，该函数需要一个字符串作为参数，
			 * 	该字符串将会作为提示框的提示文字
			 * 
			 * 用户输入的内容将会作为函数的返回值返回，可以定义一个变量来接收该内容
			 */
			
			//将prompt放入到一个循环中
			
			while(true){
				//score就是小明的期末成绩
				var score = prompt("请输入小明的期末成绩(0-100分):");
				//判断用户输入的值是否合法
				if(score >= 0 && score <= 100){
					//满足该条件则证明用户的输入合法，退出循环
					break;
				}
				alert("请输入有效的分数")
			}
			

			//首先判断是否合法
			if(score > 100 || score < 0 || isNaN(score)){
				alert("无效成绩")
			}else{
			//根据score值来决定给小明什么奖励
				if(score == 100){
					alert("奖励一辆BMW");
				}else if(score >= 80){
					alert("奖励一台iphone15s");
				}else if(score >= 60){
					alert("奖励一本参考书");
				}else{
					alert("什么奖励都没有");
				}
			}									
		</script>
	</head>
	<body>
		
	</body>
</html>
~~~

#### do...while

![](JavaScript知识点查漏补缺/51.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 向页面中输出连续的数字
		 *
		 * 	var n = 1;
		 *	document.write(n++ + "<br />");
		 *	document.write(n++ + "<br />");
		 *	document.write(n++ + "<br />");
		 *
		 * 
		 */
		

		/**
		 * 循环语句：
		 * 	 通过循环语句可以反复执行一段代码多次
		 *
		 * while循环
		 * 	-语法：
		 * 		while(条件表达式){
		 * 			语句...
		 * 		}
		 * 	-while语句在执行时，
		 * 		先对条件表达式进行求值判断
		 * 			如果值为true,则执行循环体
		 * 				循环体执行完毕以后，继续对表达式进行判断
		 * 				如果为true，则继续执行循环体，以此类推
		 * 			如果值为false,则终止循环
		 *
		 *
		 * do...while循环
		 * 		-语法：
		 * 			do{
		 * 				语句...
		 * 			}while(条件表达式)
		 *
		 *  -执行流程
		 *  	do...while语句在执行时，会先执行循环体 
		 *  		循环体执行完毕以后，再对while后的条件表达式进行判断
		 *  		如果结果为true,则继续执行循环体，执行完毕继续判断，以此类推
		 *  		如果结果为false,则终止循环
		 *
		 * 	实际上这两个语句功能类似，不同的是while先判断再执行，
		 * 		而do...while是先执行再判断
		 *
		 * do...while可以保证循环体至少循环一次，而while不能
		 * 但是while用的多一些
		 * 				
		 */

		 var n = 1;

		 //像这种将条件表达式写死为true的循环，叫做死循环
		 //该循环不会停止，除非浏览器关闭，死循环在开发中慎用
		 //可以使用break来终止循环
		 /*while(true){
		 	alert(n++);

		 	//判断n是否是10
		 	if(n == 10){
		 		//退出循环
		 		break;
		 	}		 	
		 }
*/
		 //创建一个循环，往往需要三个步骤：
		 //1.初始化一个变量    var i = 0;
		 //2.在循环中设置一个条件表达式	while(i < 10){}
		 //3.定义一个更新表达式，每次更新初始化变量		i++
		 //
		 

		 //while循环
		 var i = 1;
		 while(i < 11){
		 	document.write(i++ + "<br />")
		 }

		 //do...while循环
		 var m = 1;
		 do{
		 	document.write(m++ + "<br />")
		 }while(m <= 10)

		 //试一试让浏览器死机
		 /*while(true){
		 	document.write("hello");
		 }*/
	</script>
</head>
<body>
	
</body>
</html>
~~~

#### for

![](JavaScript知识点查漏补缺/52.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * for语句，也是一个循环语句，也称为for循环
		 * 		在for循环中，为我们提供了专门的位置用来放三个表达式：
		 * 			1.初始化表达式
		 * 			2.条件表达式
		 * 			3.更新表达式
		 *
		 * 	for循环的语法：
		 * 			for(①初始化表达式;②条件表达式;④更新表达式){
		 * 				③语句...
		 * 			}
		 *
		 * 	for循环的执行流程：
		 * 			①执行初始化表达式，初始化变量（初始化表达式只会执行一次）
		 * 			②执行条件表达式，判断是否执行循环。
		 * 				如果为true,则执行循环③
		 * 				如果为false,则终止循环
		 * 			④执行更新表达式，更新表达式执行完毕之后继续重复②
		 * 			
		 */
		
		//创建一个执行10次的while循环
		//初始化表示 var i = 0;
		//创建一个循环，定义条件表达式  while(i < 10){}
		//设置更新表达式  alert(i++);		
		
		for (var i = 0;i < 10; i++){
			alert(i);
		}


		/**
		 * for循环中的三个部分都可以省略，也可以写在外部
		 */
		
		var i = 0;
		for(;i<10;){
			alert(i++);
		}

		//死循环
		//如果在for循环中	不写任何的表达式，只写两个; 此时循环是一个死循环，会一直执行下去
		//所以这个也要慎用
		//
		for(::){
			alert("hello");
		}
	</script>
</head>
<body>
	
</body>
</html>
~~~

##### for循环练习1

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 打印1-100之间所有奇数之和
		 */
		
		//创建一个变量，用来保存奇数之和
		var sum = 0;

		//打印1-100之间的数
		for(var i = 1; i <= 100; i++){
			//判断i是否是奇数
			//不能被2整除的数是奇数
			if(i%2 !== 0){
				//如果i除以2有余数，则证明i是奇数
				//console.log(i);
				sum = sum + i; 
			}			
		}

		console.log("奇数已和为" + sum);


		//我自己这样做的
		var sum = 0;
		for (var i = 1 ;i < 100;i = i+2){
			sum = sum + i
		}
		alert(sum);
	</script>
</head>
<body>
	
</body>
</html>
~~~

##### for循环练习2

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 *打印1-100之间所有的7的倍数的个数和总和
		 * 
		 */
		
		//定义一个变量来保存组合
		var sum = 0;

		//定义一个计数器，来记录数量
		var count = 0;

		//打印1-100之间所有的数
		for(var i = 1; i <=100; i++){

			//判断i是否是7的倍数
			if(i % 7 == 0){
				console.log(i);
				sum = sum + i;
				//使计数器自增1
				count++;
			}				
		}
			//输出总和
			console.log("总和为" + sum);		

			//输出总数
			console.log("总数量为" + count);
		/*var sum;
		for(var i = 1;  sum = 7 * i; i++){
			console.log(sum);
		}*/
	</script>
</head>
<body>
	
</body>
</html>
~~~

##### for循环练习3

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 水仙花数是指一个3位数，它的每个位上的数字的3次幂之和等于它本身。
		（例如：1^3 + 5^3 + 3^3 = 153）,请打印所有的水仙花数。
		 */
		for(var i = 100; i <1000; i++){
			//获取i的百位，十位，个位的数字
			
			//获取百位数字
			var bai = parseInt(i/100);

			//获取十位数字
			var shi = parseInt((i - bai*100)/10);

			//获取个位数字
			var ge = i % 10;
			
			//判断i是否是水仙花数
			if(bai*bai*bai + shi*shi*shi + ge*ge*ge == i){
				console.log(i);
			}	
		}
	</script>
</head>
<body>
	
</body>
</html>
~~~

##### for循环练习4

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 在页面中接收一个用户输入的数字，并判断该数是否是质数。
		 * 质数：只能被1和它自身整除的数，1不是质数也不是合数，质数必须是大于1的自然数。	
		 */
		
		var num = prompt("请输入一个数字"); 

		//判断这个值是否合法
			if(num <= 1){
				alert("该值不合法")
			}else{
				//创建一个变量来保存当前数的状态
				var flag = true;
				//判断num是否是质数
				//获取2-number之间的数
				for(var i = 2; i < num; i++){
					//console.log(i);
					//判断number是否能被ｉ整除
					if(num % i == 0){
						//如果num能被i整除，则说明num一定不是质数
						//设置flag为false
						flag = false;
					}					
				}

				//如果num是质数则输出
				if(flag){
					alert(num + "是质数");
				}else{
					alert(num + "不是质数")
				}
			}
	</script>
</head>
<body>
	
</body>
</html>
~~~

##### for循环练习5

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 		通过程序，在页面中输出如下图形
		 * 		*
		 * 		**
		 * 		***
		 * 		****
		 * 		*****
		 * 		******
		 *
		 * 		*****
		 * 		*****
		 * 		*****
		 * 		*****
		 * 		*****
		 */
		
		//向body中输出一个内容
		//document.write("*****<br />");
		
		//通过一个for循环来输出图形
		//这个for循环执行几次，图形的高度就是多少
		//它可以用来控制图形的高度
		
		
		/**
		 *		*****
		 * 		*****
		 * 		*****
		 * 		*****
		 * 		*****
		 * 
		 * 
		 */
		for(var i = 0; i < 10; i++){
			/**
			 * 在循环的内部再创建一个循环用来控制图形的宽度
			 * 目前我们的外部的for循环执行1次，我们内部的for循环就会执行5次
			 *
			 * 内层循环可以来决定图形的宽度，执行几次图形的宽度就是多少
			 */
			for(var j = 0;j < 10;j++){
				document.write("*&nbsp;&nbsp;");				
			}	

			//输出一个换行
			document.write("<br />")		
		}



		/**
		 * 		*
		 * 		**
		 * 		***
		 * 		****
		 * 		*****
		 * 		******
		 * 
		 *
		 */
		for(var i = 0; i < 10; i++){
			/**
			 * 在循环的内部再创建一个循环用来控制图形的宽度
			 * 目前我们的外部的for循环执行1次，我们内部的for循环就会执行5次
			 *
			 * 内层循环可以来决定图形的宽度，执行几次图形的宽度就是多少
			 */
			
			//for(var j = 10;j > i+1;j--)则是倒三角
			for(var j = 0;j < i+1;j++){
				document.write("*&nbsp;&nbsp;");				
			}	

			//输出一个换行
			document.write("<br />")		
		}
	</script>
</head>
<body>
	
</body>
</html>
~~~

##### for循环练习6

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 1.打印九九乘法表
		 * 2.打印出1-100之间所有的质数
		 */
		
		//创建外层循环，用来控制乘法表的高度
		for(var a = 1; a < 10; a++){
			for(var b = 1;b <= a; b++){			
				document.write(b + "*" + a + "=" + a * b + "&nbsp;&nbsp;");	

			}
			//输出一个换行
			document.write("<br />")	
		}
	</script>

	<!-- <style style="text/css">
		body{
			width: 2000px;
		}
		div{
			display: inline-block;
			width: 80px;
		}
	</style> -->
</head>
<body>
	
</body>
</html>
~~~

##### for循环练习7

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 打印出1-100之间所有的质数
		 */
		
		//打印2-100之间所有的数
		 for(var i = 2;i <= 100; i++){
		 	
		 	//创建一个布尔值，来保存结果，默认i是质数
			 var flag = true;	

		 	//判断i是否是质数，首先需要获取2-i之间所有的数
		 	for(var j = 2; j < i; j++){
		 	
		 		//证明num是质数比较麻烦，所以反着来，证明num不是质数		
		 		if(i % j == 0){	
		 			//如果进入判断，则证明i不是质数
		 			flag = false;
		 		}		 		
		 	}
		 	//如果是质数，则打印i的值
		 	if(flag){
		 		console.log(i);
		 	}		 			 
		 }


		/*var flag = true;
		if(var num < 2 || num >100){
			alert("数据溢出");
		}else{
			for(var i = 2; i < num; i++){
				if(num % i == 0){
					alert("num不是质数");
					flag = false;
				}
			}
		}*/
	</script>
</head>
<body>
	
</body>
</html>
~~~

### break和continue

![](JavaScript知识点查漏补缺/53.png)

### label

![](JavaScript知识点查漏补缺/54.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * break关键字可以用来退出switch或循环语句（不能用于if）
		 * 不能在if语句中使用break和continue
		 */
		
		for(var i = 0;i < 5; i++){
			document.write(i);
			if(i == 2){
				//这个break是对for起作用的，不是对if起作用的，所以可以使用
				//单独用不行，但是能在for循环里面用
				//break会立即终止离他最近的循环语句
				break;   
			}			
		}

		/**
		 * 可以为循环语句创建一个label,来标识当前的循环
		 * label:循环语句
		 * 使用break语句时，可以在break后跟着一个label,
		 * 	这样break将会结束指定的循环，而不是最近的
		 * 
		 */
		
		outer:
		for(var j = 0;j < 5; j++){
			console.log("外层循环" + j);
			for(var k = 0;k < 5; k++){
				//终止内层循环，不终止外层循环
				//如果加上outer标签则直接终止外层循环				
					break outer; 				
				console.log("内层循环" + k);
			}
		}

		//break不能用于if语句，会报错 Uncaught SyntaxError: Illegal break statement
		/*if(true){
			break;
			document.write("hello");
		}*/


		/**
		 * continue关键字可以用来跳过当次循环
		 * 同样continue也是默认只会对它最近的循环起作用
		 * 
		 */
		for(var i = 0;i < 5; i++){
			//console.log(i);
			if(i == 2){
				//当i等于2时跳过此次循环
				continue;
			}
			console.log(i);
		}

		for(var j = 0;j < 5; j++){
			console.log("外层循环" + j);
			for(var k = 0;k < 5; k++){
				if(k ==1){
					continue; 
				}				
				console.log("内层循环" + k);
			}
		}
	</script>
</head>
<body>
	
</body>
</html>
~~~

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>

		//测试如下程序的性能
		//在程序执行前，开启计时器
		//console.time("计时器的名字")可以用来开启一个计时器
		//它需要一个字符串作为参数，这个字符串将会作为计时器的标识
		console.time("test");				
		 for(var i = 2;i <= 100; i++){		 
			 var flag = true;			 	
		 	for(var j = 2; j <= Math.sqrt(i); j++){		 		
		 		if(i % j == 0){			 			
		 			flag = false;		 		
		 			break;
		 		}		 		
		 	}		 
		 	if(flag){
		 		console.log(i);
		 	}		 			 
		 }

		 //终止计时器
		 //console.timeend()
		 //不使用break 2.5ms
		 //使用break: 2.2ms
		 //修改成j <= Math.sqrt(i)，更快
		 console.timeEnd("test");

		 /**
		  * 可以通过Math.sqrt()对一个数进行开方
		  */
		 var result = Math.sqrt(4);
		 console.log("result = " + result);
	</script>
</head>
<body>
	
</body>
</html>
~~~

# 对象

![](JavaScript知识点查漏补缺/55.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 创建一个对象
		 */
		
		var obj = new Object();

		//向对象中添加属性
		obj.name = "孙悟空";
		obj.age = 500;

		//对象的属性值可以是任何的数据类型，也可以是个函数
		obj.sayName = function(){
			console.log(obj.name);
		};

		//console.log(obj.sayName);		//没加括号，打印的是对象
		//这个叫做调用方法
		obj.sayName();		//孙悟空   类似与console.log()前面是对象，后面是方法


		//这个叫做调用函数
		function fun(){
			console.log(obj.name);
		}

		fun();
		/**
		 * 函数也可以成为对象的属性
		 * 如果一个函数作为一个函数的属性保存，
		 * 那么我们称这个函数是这个对象的方法
		 * 调用函数就说调用对象的方法(method)
		 *
		 * 但是它只是名称上的区别，没有本质的差别
		 */
		

		var obj2 = {
			name:"猪八戒",
			age:500,
			sayName:function(){
				console.log(obj2.name);
			}
		}
		obj2.sayName();

	</script>
</head>
<body>
	
</body>
</html>
~~~

## 创建对象

![](JavaScript知识点查漏补缺/56.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 在JS中一共有6中数据类型(首字母大写)
			* 		String 	字符串
			* 		Number 	数值
			* 		Boolean 布尔值
			* 		Null 	空值
			* 		Undefined 未定义
			* 		Object  对象
			*   		
			* 		其中String 、Number、Boolean、Null、Undefined属于基本数据类型
			*	 	而Object属于引用数据类型
			*
			* 基本数据类型都是单一的值"hello" 123 true;
			* 值和值之间没有任何的联系
			*
			* 在JS中表示一个人的信息(name gender	age)
			* 	var name = "孙悟空";
			* 	var gender = "男";
			* 	var age = 500;
			*
			* 如果使用基本数据类型的数据，我们所创建的变量都是独立的，不能成为一个整体
			*
			* 对象属于复合的数据类型，在对象中可以保存多个不同数据类型的属性
			*
			* 对象的分类：
			* 	1.内建对象
			* 		-由ES标准中定义的对象，在任何的ES的实现中都可以使用
			* 		-比如:Math String Number Boolean Function Object
			*
			*	2.宿主对象
			*		-由JS的运行环境提供的对象，目前来讲主要由浏览器提供的对象
			*		-比如BOM DOM对象 (不是两个对象，里面由一大堆对象)
			*			console(控制台)  document 
			*
			*	3.自定义对象（最难）
			*		-由开发人员自己创建的对象
			*
			* 对象就像一个容器，可以去装不同的属性（变量名是矿泉水瓶，变量值是里面的水）
		 */
		
		//创建对象
		/**
		 * 使用new关键字调用的函数，是构造函数 constructor
		 * 		构造函数是专门用来创建对象的函数！！！！！！！！！！！！！
		 * 		使用typeof检查一个对象时，会返回object
		 */
		var obj = new Object();   //空的
		console.log(obj);
		console.log(typeof obj);

		/**
		 * 在对象中保存的值称为属性
		 * 向对象中添加属性
		 * 		语法：对象.属性 = 属性值;
		 */
		
		//向obj中添加一个	name属性
		obj.name = "孙悟空";
		//向obj中添加一个gender属性
		obj.gender = "男";
		//向obj中添加一个age属性
		obj.age = 500;
		console.log(obj);

		/**
		 * 读取对象中的属性
		 * 		语法：对象.属性名
		 *
		 * 如果读取对象中没有的属性，不会报错而是会返回undefined
		 */
		console.log(obj.name);   //obj.不能省
		console.log(obj.hello);  //undefined

		/**
		 * 修改对象的属性值
		 * 		语法：对象.属性名 = 新值（和添加一样的，只不过把之前的值给覆盖掉了）
		 */
		
		obj.name = "齐天大圣";
		console.log(obj.name);

		/**
		 * 删除对象的属性
		 * 		语法：delete 对象.属性名
		 */
		delete obj.name;
		console.log(obj.name);  //undefined
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 工厂函数创建对象

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 创建一个对象
		 */
		
		/*var obj = {
			name:"孙悟空",
			age: 500,
			gender:"男",
			sayName:function(){
				alert(this.name);
			}
		};*/

		/**
		 * 使用工厂方法创建对象
		 * 通过该方法可以大批量的创建对象
		 * 
		 */
		 function createPerson(name,age,gender){
		 		//创建一个新的对象
		 		var obj = new Object();

		 		//向对象中添加属性
		 		obj.name = name;
		 		obj.age = age;
		 		obj.gender = gender;
		 		obj.sayName = function(){
		 			alert(this.name);
		 		}

		 		//将新的对象返回
		 		return obj;
		 }

		 /**
		  * 用来创建狗的对象
		  * 
		  * 
		  * 
		  */
		 function createDog(name,age){
		 	var obj = new Object();
		 	obj.name = name;
		 	obj.age = age;
		 	obj.sayHello = function(){
		 		alert("汪汪");
		 	};
		 	//将新的对象返回
		 	return obj;
		 }

		 var obj2 = createPerson("孙悟空",500,"男");
		 var obj3 = createPerson("猪八戒",400,"男");
		 var obj4 = createPerson("沙和尚",300,"男");

		 console.log(obj2);
		 console.log(obj3);
		 console.log(obj4);

		 /**
		  * 使用工厂方法创建的对象，使用的构造函数都是object
		  * 	所以创建的对象都是object这个类型
		  * 	就导致我们无法区分多种不同类型的对象
		  */
		 //创建一个狗的对象
		 var dog = createDog("旺财",3);
		 dog.sayHello();

		 console.log(dog);
		 console.log(obj4);

		/*var obj2 = {
			name:"猪八戒",
			age: 400,
			gender:"男",
			sayName:function(){
				alert(this.name);
			}
		};

		var obj3 = {
			name:"沙和尚",
			age: 300,
			gender:"男",
			sayName:function(){
				alert(this.name);
			}
		};*/
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 对象属性的访问

![](JavaScript知识点查漏补缺/57.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>		
		var obj = new Object();
		/**
		 * 向对象中添加属性
		 * 		属性名：
		 * 			-对象的属性名不强制要求遵守标识符的规范
		 * 				什么乱七八糟的名字都可以使用
		 * 		  	-但是我们使用还是尽量按照标识符的规范去做
		 */
		obj.name = "孙悟空";
		obj.var = "hello";  //obj可以用
		/**
		 * 如果要使用特殊的属性名，不能采用.的方式来操作
		 * 		需要使用另一种方式：
		 * 			语法：对象["属性名"] = 属性值;
		 * 		读取时也需要采用这一种方式
		 *
		 * 使用[]这种形式去操作属性，更加的灵活
		 * 		在[]中可以直接传递一个变量(比如n)，这样变量值是多少就会读取哪个属性
		 * 		
		 */
		//obj.123 = 789;  //会报错
		obj["123"] = 789; //不会报错
		obj["nihao"] = "你好";

		console.log(obj.var);
		console.log(obj["123"]);

		var n = "123";
		console.log(obj["123"]);  	//789
		console.log(obj[n]);   		//789

		var n = "nihao";
		console.log(obj[n]);   		//你好
		
		/**
		 * 属性值
		 * 	JS对象的属性值，可以使任意的数据类型
		 * 	甚至也可以是一个对象(在容器里又装了一个容器)
		 */
		
		obj.test = "hello";
		obj.test = "true";
		obj.test = "null";
		obj.test = "undefined";
		console.log(obj.test);

		//创建一个对象
		var obj2 = new Object();
		obj2.name = "猪八戒";

		//将obj2设置为obj1的属性
		obj.test = obj2;        //对象计算机有一个属性时键盘，同时键盘也是一个对象
		console.log(obj.test);  
		console.log(obj.test.name);  

		/**
		 * in运算符
		 * 		-通过该运算符可以检查一个对象中是否含有指定的属性 
		 * 			如果有则返回true,否则返回false
		 *
		 * 		-语法：
		 * 			"属性名" in 对象
		 */
		
		//检查obj中是否有test2这一属性
		console.log("test2" in obj);	//false

	</script>
</head>
<body>
	
</body>
</html>
~~~

## 基本数据类型

![](JavaScript知识点查漏补缺/58.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 在JS中一共有6中数据类型(首字母大写)
			* 		String 	字符串
			* 		Number 	数值
			* 		Boolean 布尔值
			* 		Null 	空值
			* 		Undefined 未定义
			* 		Object  对象
			*   		
			* 		其中String 、Number、Boolean、Null、Undefined属于基本数据类型
			*	 	而Object属于引用数据类型
			*
		 * 		JS中的变量(名)（包括基本和引用）--矿泉水瓶-都是保存在栈内存中的
		 * 			基本数据类型的值（水）直接在栈内存中存储
		 * 			值与值之间是独立存在的，修改一个变量不会影响其他的变量
		 *
		 * 			对象是保存到堆内存中的（变量名和变量值[保存的是栈内存的内存地址]在栈内存中）
		 * 			每创建一个新的对象，就会在堆内存中开辟出一个新的空间
		 * 			
		 * 	        而变量保存的是对象的内存地址（对象的引用），如果两个对象保存的是同一个
		 * 	      	对象引用
		 */
		var a = 123;
		var b = a;
		a++;
		console.log("a = " + a);	//124
		console.log("b = " + b);	//123

		var obj = new Object();
		obj.name = "孙悟空";
		var obj2 = obj;

		//修改obj.name的属性
		obj.name = "猪八戒";
		console.log(obj.name);		//猪八戒
		console.log(obj2.name);		//猪八戒

		//设置obj2为null
		obj2 = null;
		console.log(obj);		//Object
		console.log(obj2);		//null  我不扎小人了，不代表别人不扎。obj2断开链接，不影响他人

		/**
		 * 当比较两个基本数据类型的值时，就是比较值
		 * 而比较两个引用数据类型时，它是比较的对象的内存地址
		 * 		如果两个对象是一模一样的，但是地址不同，它也会返回false
		 * 
		 */
		var c = 10;
		var d = 10;
		console.log(c == d);  //true

		var obj3 = new Object();
		var obj4 = new Object();
		obj3.name = "沙和尚";
		obj3.name = "沙和尚";
		console.log(obj3);
		console.log(obj4);
		console.log(obj3 == obj4);  //false
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 引用数据类型

![](JavaScript知识点查漏补缺/59.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		//创建一个对象
		//var obj = new Object();
		
		/**
		 * 使用对象字面量来创建一个对象
		 */
		var obj = {};
		console.log(typeof obj);  //object

		obj.name = "孙悟空";
		console.log(obj.name);

		/**
		 * 使用对象字面量可以在创建对象时，直接指定对象的属性
		 * 		语法：{属性名：属性值, 属性名:属性值...}
		 *
		 * 		对象字面量的属性名可以加引号也可以不加，建议不加
		 * 		如果要使用一些特殊的名字，则必须要加引号
		 *
		 * 属性名和属性值是一组一组的名值对结构
		 * 名和值之间使用:连接，多个名值对之间使用,隔开
		 * 如果一个属性之后没有其他的属性，就不要写，
		 */
		
		var obj2 = {
			name:"猪八戒",
			age :500,
			gender: "男",  
			test:{name:"沙和尚"}		
            //最后一对不要写逗号了
		};  //大括号后面是分号，各个属性之间用逗号
		console.log(obj2);
		console.log(obj2.test);
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 栈和堆

![](JavaScript知识点查漏补缺/60.png)

![](JavaScript知识点查漏补缺/61.png)

## 数组

![](JavaScript知识点查漏补缺/62.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 *
		 * 面向对象 1.找对象   2.搞对象
		 *
		 * 
		 * 内建对象
		 * 宿主对象
		 * 自定义对象
		 *
		 * 数组(Array)
		 * 	-数组也是一个对象
		 * 	-它和普通的对象功能类似，也是用来存储一些值的
		 * 	-不同的是普通对象是使用字符串作为属性名的
		 * 		而数组是使用数字来作为索引操作元素
		 *
		 * -索引：
		 * 		从0开始的整数就是索引
		 *
		 * -数组的存储性能比普通对象好，所以在开发中我们经常使用数组来存储一些数据
		 */
		
		//创建数组对象
		var arr = new Array();
		console.log(arr);  	//[]

		//使用typeof检查一个数组时，会返回object
		console.log(typeof arr);	//object

		/**
		 *向数组中添加元素（数组添加元素是通过索引来的，而不是通过属性名来的）
		 *	语法： 数组[索引] = 值;
		 * 
		 */
		arr[0] = 10;
		arr[1] = 33;
		arr[2] = 22;
		arr[10] = 88;
		arr[100] = 100;
		console.log(arr);  	//(101) [10, 33, 22, empty × 7, 88, empty × 89, 100]

		/**
		 * 读取数组中的元素
		 * 	语法：数组[索引]
		 * 	
		 */
		console.log(arr[0]);	//10

		//如果读取不存在的索引，它不会报错，而是返回undefined
		console.log(arr[3]);	//undefined

		/**
		 * 获取数组的长度
		 * 可以使用length属性来获取数组的长度(元素的个数)
		 * 语法： 数组.length
		 */
		
		/**
		 * 对于连续的数组，使用length可以获取到数组的长度(元素的个数)
		 * 对于非连续的数组，使用length会获取到数组的最大索引+1
		 * 		尽量不要创建非连续数组
		 */
		console.log(arr.length);	//101  虽然只有5个元素，但长度是101

		/**
		 * 修改length
		 * 		如果修改的length大于原长度，则多出部分会空出来
		 * 		如果修改的length小于原长度，则多出元素会被删除
		 */
		 arr.length = 10;
		 console.log(arr.length);		//10
		 console.log(arr);				//(10) [10, 33, 22, empty × 7]

		 //永远向数组的最后一个位置添加元素
		 //语法：数组[数组.length] = 值;
		 arr[arr.length] = 70;
		 arr[arr.length] = 80;
		 arr[arr.length] = 90;
		 console.log(arr);
	</script>
</head>
<body>
	
</body>
</html>
~~~

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		//创建一个数组
		var arr = new Array();

		arr[0] = 123;
		arr.hello = "abc";	//这样也行
		console.log(arr.hello);

		//使用字面量来创建数组
		//语法：[]
		var arr = [];
		console.log(arr);		//[]
		console.log(typeof arr);	//object

		//使用字面量创建数组时，可以在创建时就指定数组中的元素
		var arr = [1,2,3,4,5,10];
		console.log(arr);		//(6) [1, 2, 3, 4, 5, 10]
		console.log(arr.length);	//6

		//使用构造函数创建数组时，也可以同时添加元素，将要添加的元素作为构造函数的参数传递
		//元素之间使用逗号隔开
		var arr2 = new Array(10,20,30);
		console.log(arr2);		//(3) [10, 20, 30]

		//创建一个数组，数组中只有一个元素10
		arr = [10];
		console.log(arr[0]);  //10

		//表示创建一个长度为10的数组
		arr2 = new Array(10);
		console.log(arr2);		//(10) [empty × 10]
		console.log(arr2.length);		//10

		//数组中的元素可以是任意的数据类型
		arr = ["hello" , 1 , true , null , undefined];
		console.log(arr);   //(5) ["hello", 1, true, null, undefined]

		//也可以是对象
		var obj = {name:"孙悟空"};
		arr[arr.length] = obj;
		console.log(arr[5].name);		//孙悟空

		arr2 = [{name:"孙悟空"},{name:"猪八戒"},{name:"沙和尚"}]
		console.log(arr2);

		//也可以是一个函数
		arr3 = [function(){alert(1)} , function(){alert(2)}];
		console.log(arr3);	//(2) [ƒ, ƒ]
		arr3[1](); 	//会显示2


		//数组中也可以放数组，如下这种数组我们称为二维数组
		arr4 = [[1 ,2 , 3] ,[4 ,5 , 6] , [7 ,8 , 9]];
		console.log(arr4);		//(3) [Array(3), Array(3), Array(3)]
	</script>
</head>
<body>
	
</body>
</html>
~~~

###  数组的方法

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		//创建一个数组
		var arr = ["孙悟空" , "猪八戒" , "沙和尚"];
		/**
		 * push()——尾巴增加
		 * 	-该方法可以向数组的末尾添加一个或多个元素，并返回数组的新的长度
		 * 	-可以将要添加的元素作为方法的参数传递，
		 * 	 这样这些元素将会自动添加到元素末尾
		 *
		 * -该方法会将数组新的长度作为返回值返回
		 */
		
		arr.push("唐僧" , "观音大士");
		console.log(arr);		

		//var result = arr.push("唐僧" , "观音大士");
		//console.log("result =" + result);  //result =5，返回的是一个数字！！！
		
		/**
		 * pop()——尾巴删除
		 * 	-该方法可以删除数组的最后一个元素,并将被删除的元素作为返回值返回
		 * 
		 */
		arr.pop()
		console.log(arr);	

		result = arr.pop()
		console.log(arr);	
		console.log("result =" + result);	//result =唐僧

		/**
		 * unshift()
		 * 	-向数组开头添加一个或多个元素，并返回新的数组
		 * 	-向前边插入元素以后，其他的元素索引会依次调整
		 */

		 console.log(arr);		
		 arr.unshift("牛魔王","二郎神");
		 console.log(arr);		

		 /**
		  * shift()
		  * 	-可以删除数组的第一个元素，并将被删除的元素作为返回值返回
		  */
		 console.log(arr);		
		 arr.shift();
		 console.log(arr);		
		 result = arr.shift();
		 console.log(arr);	
		 console.log("result = " + result); 
	</script>
</head>
<body>
	
</body>
</html>
~~~

> 把数组顺时针转90度，更加直观。最上面是数组头部，最下面是数组尾部，加数都是从数组尾部开始加的。

![](JavaScript知识点查漏补缺/81.png)

### 数组的遍历

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		//创建一个数组
		var arr = ["孙悟空" , "猪八戒" , "沙和尚" , "唐僧"];

		//所谓的遍历数组，就是将数组中所有元素都取出来
		/*console.log(arr[0]);
		console.log(arr[1]);
		console.log(arr[2]);
		console.log(arr[3]);*/

		//i是index的首字母
		for (var i = 0;i < arr.length ; i++){
			console.log(arr[i]);
		}
	</script>
</head>
<body>
	
</body>
</html>
~~~

### 数组的foreach方法遍历

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 一般我们都是使用for循环去遍历数组
		 * 	JS中还为我们提供了一个方法，用来遍历数组
		 *
		 * forEach()
		 * 		-这个方法只指出IE8以上的浏览器
		 * 			IE8及以下的浏览器均不支持该方法，所以如果需要兼容IE8,则不要使用
		 * 			forEach,还是使用for循环来遍历
		 */
		
		//创建一个数组
		var arr = ["孙悟空" , "猪八戒" , "沙和尚" , "唐僧" ,"白骨精"];

		/**
		 * forEach()方法需要一个函数作为参数
		 * 		-像这种函数，由我们创建但是不由我们调用的，我们称为回调函数
		 * 		-数组中有几个元素函数就会执行几次,每次执行时，浏览器会将遍历到的
		 * 			元素以实参的形式传递进来，我们可以来定义形参来读取这些内容
		 * 		-浏览器会在回调函数中传递三个参数:
		 * 			第一个参数，就是当前正在遍历的元素
		 * 			第二个参数，就是当前正在遍历的元素的索引
		 * 			第三个参数，就是正在遍历的数组
		 */

		 arr.forEach(function(value , index, obj){
		 	console.log("value= " + value);
		 	console.log("index= " + index);
		 	console.log("obj= " + obj);
		 });
	</script>
</head>
<body>
	
</body>
</html>
~~~

### 数组的练习

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		function Person(name,age,gender){
			this.name = name;
			this.age  = age;
			this.gender = gender;
		}

		//修改Person原型的toString
		Person.prototype.toString = function(){
			return "Person[name=" + this.name + ",age=" + this.gender + "]";
		};

		//创建一个Person对象
		var per = new Person("孙悟空" ,500);
		var per2 = new Person("猪八戒" ,28);
		var per3 = new Person("红孩儿" ,8);
		var per4 = new Person("二郎神" ,38);
		var per5 = new Person("蜘蛛精" ,16);
		/**
		 * 将这些person对象放入到一个数组中
		 */
		var perArr = [per,per2,per3,per4,per5];
		console.log(perArr);
		//console.log(per);		
		//Person {name: "孙悟空", age: 18, gender: undefined}
		
		/**
		 * 创建一个函数，可将perArr中的满18岁的Person提取出来
		 * 	然后封装到一个新的数组中并返回
		 * 	arr
		 * 	 形参，要提取信息的数组
		 */
		
		function getAdult(arr){
			//创建一个新的数组
			var newArr = [];

			//遍历arr,获取arr中的Person对象
			for(var i = 0; i < arr.length; i++){
				var p = arr[i];
				//判断Person对象的age是否大于等于18
				if(p.age >= 18){
					//如果大于等于18，则将这个对象添加到newArr中
					newArr.push(p);
				}
			}		
			//将新的数组返回
			return newArr;
		}

		var result = getAdult(perArr);
		console.log(result);
	</script>
</head>
<body>
	
</body>
</html>
~~~

### 数组去重

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		//创建一个数组
		var arr = [1,2,3,2,2,1,3,4,2,5];

		//去除数组中重复的数字
		//获取数组中的每一个元素
		for(var i = 0 ; i < arr.length; i++){
			//console.log(arr[i]);
			//获取当前元素后的所有元素
			for(var j = i+1; j < arr.length;j++){
				//console.log("---->" + arr[j]);

				//判断两个元素的值是否相等
				if(arr[i] == arr[j]){
					//如果相等，则证明出现了重复的元素，则删除j对应的元素
					arr.splice(j,1);
					//当删除了当前j所在的元素，后面的元素会自动补位
					//此时将不会再比较这个元素吧，我需要再比较一次j所在位置的元素
					//使j自减
					j--;	//这个很关键，没有就不对
				}
			}
		}
		console.log(arr);
		//去除数组中重复的数字
	</script>
</head>
<body>
	
</body>
</html>
~~~

# 函数

![](JavaScript知识点查漏补缺/63.png)

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 函数
		 * 	-函数也是一个对象
		 * 	-普通对象只是一个容器，只能装东西
		 * 	-而函数中可以封装一些功能（代码），在需要时可以执行这些功能（代码）
		 * 	-函数中可以保存一些代码，在需要的时候调用
		 * 	-使用typeof检查一个函数对象时，会返回function
		 */
		
		//创建一个函数对象
		//var obj = new Object();
		
		//可以将要封装的代码以字符串的形式传递给构造函数	
		//我们在实际开发中很少使用构造函数来创建一个函数对象，下面这个不好
		var fun = new Function("console.log('hello 这是我的第一个函数');");
		console.log(fun);
		console.log(typeof fun);

		//封装到函数中的代码不会立即执行，仅仅是把它存起来了
		//函数中的代码会在函数调用的时候执行
		//调用函数语法：  函数对象()
		//当调用函数时，函数中封装的代码会按照顺序执行
		fun();			//hello 这是我的第一个函数
		fun();			//hello 这是我的第一个函数
		fun();			//hello 这是我的第一个函数

		/**中括号代表可选
		 * 使用函数声明来创建一个函数对象
		 * 		语法：
		 * 			function 函数名([形参1，形参2，...形参N])｛
		 * 				语句...
		 * 			｝
		 */
		
		function fun2(){		//形参先别管
			console.log("这是我的第二个函数~~");
			alert("哈哈哈");
			document.write("呜呜呜");
		}

		console.log(fun2);
		//调用fun2
		fun2();


		/**
		 * 使用函数表达式来创建函数
		 * 		var 函数名 = function([形参1，形参2，...形参N]){
		 * 			语句...	
		 * 		}
		 */
		

		//没有名字用不了
		/*function(){
			console.log("我是匿名函数中封装的代码");
		}*/


		var fun3 = function(){
			console.log("我是有名字函数中封装的代码");
		}

		fun3();
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 函数的声明

![](JavaScript知识点查漏补缺/64.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 在调用函数时，浏览器每次都会穿递进两个隐含的参数
		 * 1.函数的上下文对象this
		 * 2.封装实参的对象arguments
		 * 		-arguments是一个类数组对象,它也可以通过索引来操作数据，也可以获取长度
		 * 		-在调用函数时，我们所传递的实参都会在arguments中保存
		 * 		-arguments.length可以用来获取实参的长度
		 * 		-我们即使不定义形参，也可以通过arguments来使用实参
		 * 		只不过比较麻烦
		 *
		 * 		arguments[0]表示第一个实参...
		 * 		arguments[1]表示第二个实参...
		 *
		 * 		-它里面有一个属性叫做callee,
		 * 		这个属性对应一个函数对象，就是当前正在指向的函数的对象
		 */
		function fun(){
			console.log(arguments);
			console.log(arguments instanceof Array);  //false
			console.log(Array.isArray(arguments));		//false
			console.log(arguments.length);	//2
			console.log(arguments[0]);  //"hello"
			console.log(arguments.callee);
			console.log(arguments.callee == fun);  //true
		}
		//fun();
		fun("hello" , true);
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 函数的调用

![](JavaScript知识点查漏补缺/65.png)

## 函数的声明(二)

![](JavaScript知识点查漏补缺/66.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 定义一个用来求2个数和的函数
		 * 		可以在函数的()里来指定一个或多个形参（形式参数）
		 * 		多个形参之间使用逗号(,)隔开,声明形参就相当于在函数内部声明了对应的变量，
		 * 		但是并不赋值
		 */
		
		function sum(a,b){
			console.log(a + b);
		}

		/**
		 * 在调用函数时，可以在()中指定实参（实际参数）
		 */
		sum(1,2);
		/**
		 * 调用函数时解析器不会检查实参的类型 
		 * 所以要注意，是否有可能会接收到非法的数据，如果有可能则需要对参数进行类型的检查
		 */
		sum(123,"hello");		//123hello

		/**
		 * 调用函数时，解析器也不会检查函数的数量
		 * 多余的实参不会被赋值
		 * 如果实参的数量少于形参的数量，则没有对应实参的形参将是undefined
		 *
		 * 函数的实参可以使任意的数据类型
		 */
		
		sum(123,456,"hell0","world");  //579  后面的两个参数没有被用
		sum(123);	//null   123+undefined = null
	</script>
</head>
<body>
	
</body>
</html>
~~~

##  变量的提前声明

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 变量的声明提前
		 * 	-使用var关键字声明的变量，会在所有的代码执行之前被声明（但是不会赋值）
		 * 	 但是如果声明变量时不使用var关键字，则变量不会被提前声明
		 *
		 * 函数的声明提前
		 * 	-使用函数声明形式创建的函数function()函数{}
		 * 	 它会在所有的代码执行之前就被创建，所以我们可以在函数声明前调用函数
		 * 	使用函数表达式创建的函数，不会被提前声明，所以不能在声明前调用
		 */
		console.log("a = " + a);		//不写var 会报错 a is not undefined 写了就不会报错

		a = 123;		//不写var 相当于window.a

		fun();	//在函数声明之前调用的函数，没有报错
		fun2();	//报错了

		//函数声明会被提前创建
		function fun(){
			console.log("我是fun函数");
		}

		//函数表达式不会被提前创建，fun2会被提前声明，但是没有赋值，
	    //所以fun2是undefined,直到执行到28行才会赋值
		var fun2 = functon(){
			console.log("我是fun2函数");
		}
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 传递参数

![](JavaScript知识点查漏补缺/67.png)

## return返回值

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 创建一个函数，用来计算三个数的和
		 *
		 * 可以使用return来设置函数的返回值
		 * 		语法：
		 * 			return 值
		 *
		 * return后的值将会作为函数的执行结果返回
		 * 		可以定义一个变量，可以接收该结果
		 */
		function sum(a , b , c){
			//alert(a + b + c);
			var d = a + b + c;

			//return后面如果不跟值的话就相当于return undefined;
			//如果不写return也会返回undefined
			return d;

			//return后的语句都不会执行，这是死代码
			alert("hello");  

			//return后可以跟任意类型的值 
		}

		//调用函数
		//变量result的值就是函数的执行结果	
		//函数返回什么result的值就是什么  result 就是4+7+8的结果
		//sum(1,2,3);
		var result = sum(4 , 7 , 8);
		console.log("result = " + result);
	</script>
</head>
<body>
	
</body>
</html>
~~~

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		function fun(){
			alert("函数要执行了");
			for(var i = 0;i < 5;i++){
				console.log(i);
				if (i == 2){
					//使用break可以退出当前的循环
					//break;
					
					//continue用于跳过当次循环
					//continue;
					
					//使用return可以结束整个函数
					return;
				}
			}
			alert("函数执行完了");
        	//这行代码无法执行，因为前面有return。
		}
		fun();

		/**
		 * 返回值（return后面的东西）可以是任意的数据类型
		 * 	  也可以是对象，也可以是一个函数
		 * 
		 */
		function fun2(){
			//return 10;
			var obj = {name:"沙和尚"};		
			return obj;
		}

		var a = fun2();
		console.log("a=" + a);			//a=[object Object]
		console.log("a=" + a.name);		//a=沙和尚

		function fun3(){
			//在函数内部再声明一个函数
			function fun4(){
				alert("我是fun4");
			}

			//将fun4函数对象作为返回值返回
			return fun4();
		}

		a = fun3();
		console.log(a);		//undefined

		//a();
		//fun3()();
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 立即执行函数

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 下面这个函数直接写会报错
		 * 但是加个()表示是一个整体就不会报错了	
		 */
		
		//调用函数：函数对象()
		/**
		 * 立即执行函数
		 * 函数定义完，立即被调用，这种函数叫做立即执行函数
		 * 立即执行函数往往只会执行一次
		 */
		(function(){
			alert("我是匿名函数~~");
		})();

		(function(a,b){
			console.log("a=" + a);
			console.log("b=" + b);

		})(123,456);
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 函数练习

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 定义一个函数，判断一个数字是否是偶数，如果是返回true,	否则返回false
		 */
		
		/*function isou(a){
			if(a % 2 == 0){
				return true;
			}else{
				return false;
			}
		}

		var result = isou(45);
		console.log("result=" + result);
*/
		//简洁版
		function isou(num){
			return num % 2 == 0;
		}

		var result = isou(7);
		console.log("result=" + result);

		/**
		 * 定义一个函数，可以根据半径计算一个圆的面积并计算结果
		 */
		var PI = 3.1415926;
		function circle(r){
			var s = PI*r*r;
			return s;

			//或者直接return PI*r*r;
		}
		var result = circle(8);
		console.log("圆的面积是" + result);


		/**
		 * 创建一个函数，可以在控制台中输出一个人的信息
		 * 		可以输出人的name,age,gender,address
		 *
		 * 实参可以是任意数据类型，也可以是一个对象(当参数过多可以将参数封装到一个对象里更方便)
		 * 		-当我们的参数过多时，可以将参数封装到一个对象中，然后通过对象传递 
		 */
		
		function sayHello(name,age,gender,address){
			console.log(name + "今年" + age + "岁了，" + "性别" + gender + "，
                        家住" + address);
		};
		sayHello("孙悟空",500,"男","花果山");

		//创建一个对象
		var obj = {
			name:"孙悟空",
			age:"500",
			gender:"男",
			address:"花果山"
		};

		//简洁版
		function sayHello(o){	//o就是obj
			console.log(o.name + "今年" + o.age + "岁了，" + "性别" + o.gender + "，
                        家住" + 		o.address);
		};
		sayHello(obj);

		/**
		 * 实参可以使一个对象，也可以是一个函数
		 * 对象能干的事情，函数都能干
		 */
		function fun(a){
			console.log("a=" + a);
			a(obj);
		}

		fun(sayHello);

		//可以将一个匿名函数作为一个实参传递给一个函数
		fun(function(){alert("hello")});


		/**
		 * -circle()	冰淇淋
		 * 		调用函数
		 * 		相当于使用函数的返回值
		 * 		
		 * 	circle	冰淇淋机器
		 * 		函数对象
		 * 		相当于直接使用函数对象
		 */
	</script>
</head>
<body>
	
</body>
</html>
~~~



## 执行环境

![](JavaScript知识点查漏补缺/68.png)

## 枚举对象中的属性(for...in)

> in可以理解为index，如果是数组，就枚举数组的下标；如果是对象，就枚举对象的属性。
>
> fo可以理解为value，如果是数组，就枚举数组的值；如果是对象，也枚举对象的值。

[for in与for of用法及区别](https://www.jianshu.com/p/ee21c4c86d5d)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		var obj = {
			name:"孙悟空",
			age:18,
			gender:"男",
			address:"花果山"
		};

		//枚举对象中的属性
		//使用for...in 语句
		
		/**
		 * 语法：
		 * 		for(var 变量 in 对象){
		 * 		
		 * 		}
		 *
		 * for... in语句   对象中有几个属性，循环体就会执行几次
		 * 		每次执行时，会将对象中的一个属性的名字赋值给变量
		 */
		
		for(var n in obj){
			//console.log("hello");
			console.log("属性名：" + n);
			//console.log(obj.n);		
			/**
			 * 如果要使用特殊的属性名，不能采用.的方式来操作
		 * 		需要使用另一种方式：
		 * 			语法：对象["属性名"] = 属性值;
		 * 		读取时也需要采用这一种方式
		 *
		 * 		使用[]这种形式去操作属性，更加的灵活
		 * 		在[]中可以直接传递一个变量(比如n)，这样变量值是多少就会读取哪个属性
			 */
			console.log("属性值：" + obj[n]);
		}
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 函数内部属性

![](JavaScript知识点查漏补缺/69.png)

## this引用的规则

![](JavaScript知识点查漏补缺/70.png)

## 构造函数

![](JavaScript知识点查漏补缺/71.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 创建一个构造函数，专门用来创建Person对象的
		 * 		构造函数就是一个普通的函数，创建方式和普通函数没有区别
		 * 		不同的是构造函数习惯上首字母大写
		 *
		 * 构造函数和普通函数的区别就是调用方式的不同
		 * 		普通函数时直接调用，而构造函数需要使用new关键字来调用
		 *
		 * 构造函数的执行流程：
		 * 		1.立刻创建一个新的对象
		 * 		2.将新建的对象设置为函数中的this,在构造函数中可以使用this来引用新建的对象
		 * 		3.逐行执行函数中的代码
		 * 		4.将新建的对象作为返回值返回
		 *
		 * 		使用同一个构造函数创建的对象，我们称为一类对象，也将一个构造函数称为一个类
		 * 		我们将通过一个构造函数创建的对象，称为是该类的实例
		 *
		 *
		 * this的情况
		 * 	1.当以函数的形式调用时，this是window
		 * 	2.当以方法的形式调用时，谁调用方法this就是谁
		 * 	3.当以构造函数的形式调用时，this就是新创建的那个对象	
		 */
		function Person(name,age,gender){
			//alert("hello");
			//alert(this);   //this==新建的对象per  [object Object]
			this.name = name;
			this.age = age;
			this.gender = gender;
			this.sayName = function(){
				alert(this.name);
			};
		}

		function Dog(){

		}
		//这是普通函数
		//var person = Person();
		//console.log(per)    //undefined

		//这是构造函数
		var per = new Person("孙悟空",500,"男");
		var per2  = new Person("猪八戒",400,"男");
		//console.log(per.name);		//object
		
		var dog = new Dog();
		//console.log(dog);
		/**
		 * 使用instanceof可以检查一个对象是否是一个类的实例
		 * 	语法：
		 * 		对象instanceof 构造函数
		 * 			如果是，返回true，否则返回false
		 */
		console.log(per instanceof 	Person);		//true
		console.log(dog instanceof 	Person);		//false
		/**
		 * 所有的对象都是Object的后代
		 * 	所以任何对象和Object被instanceof检查时都会返回true
		 */
		console.log(per instanceof 	Object);		//true
		console.log(dog instanceof 	Object);		//true
	</script>
</head>
<body>
	
</body>
</html>
~~~

### 构造函数的修改

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 创建一个Person构造函数
		 * 	-在Person构造函数中，为每一个对象都添加了一个sayName方法
		 * 		目前我们的方法是在构造函数内部创建的，也就是说构造函数每执行一次
		 * 		就会创建一个新的sayName方法
		 * 	也就是所有实例的sayName都是唯一的
		 * 	这样就导致了构造函数执行一次就会创建一个新的方法
		 * 		执行10000此就会创建10000个新的方法，而10000个方法都是一模一样的
		 * 		这是完全没有必要的，完全可以使所有的对象共享同一个方法
		 */
		
		function Person(name,age,gender){
			this.name = name;
			this.age = age;
			this.gender = gender;

			//向对象中添加一个方法
			/*this.sayName = fun;*/
		}

		//将sayName方法在全局作用域中定义
		
		/**
		 * 将函数定义在全局作用域中，污染了全局作用域的命名空间
		 * 	而且定义在全局作用域中也很不安全	
		 * 
		 */
		/*function fun(){
				alert("hello,大家好。我是：" + this.name);
			}
		*/		
		//向原型中添加sayName方法
		Person.prototype.sayName = function(){
			alert("hello,大家好。我是：" + this.name);
		}
		//创建一个Person的实例
		var per = new Person("孙悟空",500,"男");
		var per2 = new Person("猪八戒",400,"男");
		per.sayName();
		per2.sayName();
		console.log(per.sayName == per2.sayName);  //true  
	</script>
</head>
<body>
	
</body>
</html>
~~~

## new关键字

![](JavaScript知识点查漏补缺/72.png)

## 属性的访问

![](JavaScript知识点查漏补缺/73.png)

## 作用域

~~~javascript
 <!DOCTYPE html>
 <html lang="en">
 <head>
 	<meta charset="UTF-8">
 	<title>Document</title>
 	<script>
		/**
		 * 作用域：
		 * 	-作用域指一个变量的作用范围
		 * 	-在JS中一共有两种作用域：
		 * 		1.全局作用域
		 * 			-直接编写在script标签中的JS代码，都在全局作用域
		 * 			-全局作用域在页面打开时创建，在页面关闭时销毁
		 * 			-在全局作用域中有一个全局对象window,
		 * 				它代表的是一个浏览器的窗口，它由浏览器创建，我们可以直接使用
		 * 			-在全局作用域中创建的变量都会作为window对象的属性保存
		 * 			-在全局作用域中创建的函数都会作为window对象的方法保存
		 *
		 * 			-全局作用域中的变量都是全局变量
		 * 				在页面的任意的部分都可以访问的到
		 * 					
		 *
		 * 		2.函数作用域
		 */
		
		function fun(){
			var a = 123;
		}

		fun();
		console.log(a);		//报错，a在外部看不见。a is not defined

		console.log(window);

		var a = 10;
		console.log(window.a);

		function fun(){
			console.log("我是fun函数");
		}

		fun();
		window.fun();

		alert("hello");
		window.alert("hello");
	</script>
 </head>
 <body>
 	
 </body>
 </html>
~~~

## debug

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>

		alert(d);		//undefined

		var a = 10;
		var b = "hell0";
		c = true;
		function fun(){
			alert("hello");
		}
		var d = 35;
	</script>
</head>
<body>
	
</body>
</html>
~~~

## toString

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		function Person(name,age,gender){
			this.name = name;
			this.age = age;
			this.gender = gender;
		}

		//创建一个Person实例
		var per = new Person("孙悟空",500,"男");

		//修改Person原型的toString
		Person.prototype.toString = function(){
			return "Person[name =" + this.name  + ",age = " + this.age +  
            ",gender =" + this.gender + "]";
		}
 		//当我们直接在页面中打印一个对象时，实际上输出的是对象的toString()方法的返回值
		//如果我们希望在输出对象时不输出[object Object]，可以为对象添加一个toString方法
		/*per.toString = function(){
			return "Person[name =" + this.name  + ",age = " + this.age + 
            ",gender =" + this.gender + "]";
		}*/
		console.log(per);
		var result = per.toString();
		console.log("result"+ result); 		//result[object Object]
		console.log(per.__proto__.__proto__.hasOwnProperty("toString"));  //true
		console.log(per);
	</script>
</head>
<body>
	
</body>
</html>
~~~

## this

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 解析器在调用函数时，每次都会向函数内部传递进一个隐含的参数
		 * 这个隐含的参数就是this,this是一个参数，和a,b没区别，只不过是浏览器传进来的
		 * this指向的是一个对象，这个对象我们称为函数执行的上下文对象
		 * 根据函数调用方式(非创建方式)的不同，this会指向不同的对象
		 * 	 1.以函数的形式调用时，this永远都是window
		 * 	 2.以方法的形式调用时，this就是调用方法的对象
		 */
		function fun(){
			//console.log();
			console.log(this.name);	
			//Window {parent: Window, postMessage: ƒ, blur: ƒ, focus: ƒ, close: ƒ, …}
		}
		fun();

		//创建一个对象
		var obj = {
			name:"孙悟空",
			sayName:fun
		}; 

		var obj2 = {
			name:"猪八戒",
			sayName:fun
		}; 

		console.log(obj.sayName == fun);  //true
		obj.sayName();  //孙悟空
		obj2.sayName();	//猪八戒	


		var name = "全局的name属性";
		//obj.sayName();
		//以函数的形式调用，this是window
		fun();   //等价于window.fun();

		//以方法的形式调用，this是调用方法的对象
		obj.sayName();  
		obj2.sayName();
	</script>
</head>
<body>
	
</body>
</html>
~~~

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>

		//创建一个name变量
		var name = "全局";

		//创建一个sayName()函数
		function fun(){
			console.log(this.name);		//如果没有this,则只能输出全局
		}

		//创建2个对象
		var obj = {
			name:"孙悟空",
			sayName:fun
		};

		var obj2 = {
			name:"猪八戒",
			sayName:fun
		};

		//我们希望调用obj.sayName()时可以输出obj的名字
		obj.sayName();
		obj2.sayName();
	</script>
</head>
<body>
	
</body>
</html>
~~~

# 垃圾回收

![](JavaScript知识点查漏补缺/74.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 垃圾回收（GC）
		 * 	-就像人生活的时间长了会产生垃圾一样，程序运行过程中也会产生垃圾
		 * 		这些垃圾积攒过多以后，会导致程序运行的速度过慢
		 * 		所以我们需要一个垃圾回收的机制，来处理程序运行过程中产生的垃圾
		 *
		 * -当一个对象没有任何的变量或属性对它进行引用，此时我们将永远无法操作该对象
		 * 		此时这种对象就是一个垃圾，这种对象过多就会占用大量的内存空间，导致程序运行变慢
		 * 	 	所以这种垃圾必须进行清理
		 *
		 * -在JS中拥有自动的垃圾回收机制，会自动的将这些垃圾对象从内存中销毁
		 * 		我们不需要也不能进行垃圾回收的操作
		 *
		 * -我们需要做的只是将不再使用的对象设置为null即可
		 *
		 * 
		 */
		
		var obj = new Object();

		//对对象进行各种操作
		
		obj = null;
	</script>
</head>
<body>
	
</body>
</html>
~~~

# 原型继承

![](JavaScript知识点查漏补缺/75.png)

![](JavaScript知识点查漏补缺/79.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 原型 prototype
		 *
		 * 我们所创建的每一个函数，解析器都会向函数中添加一个属性prototype
		 * 		这个属性定义着一个对象，这个对象就是我们所谓的原型对象
		 *
		 * 如果函数作为普通函数调用prototype没有任何作用
		 * 当函数以构造函数形式调用时，它所创建的对象都会有一个隐含的属性，
		 * 这个属性指向该构造函数的原型对象，我们可以通过_proto_来访问该属性
		 *
		 * 原型对象就相当于公共的区域，所有同一个类的实例都可以访问到这个原型对象
		 * 		我们可以将对象中共有的内容，同一设置到原型对象中
		 *
		 * 当我们访问一个对象的属性或方法时，会先在对象自身中寻找，如果有则直接使用
		 * 	如果没有则会去原型对象中寻找，如果找到则直接使用
		 *
		 * 以后我们创建构造函数时，可以将这些对象共有的属性和方法，同一添加到构造函数的原型对象中
		 * 这样不用分别为每一个对象添加，也不会影响到全局作用域，就可以使每个对象都具有这些属性和方法
		 *
		 * 原型对象也有原型
		 */
		
		function Person(){
        
		}

		function MyClass(){
            
		}

		//向MyClass的原型中添加属性a
		MyClass.prototype.a = 123;

		//向MyClass的原型中添加一个方法
		MyClass.prototype.sayHello = function(){
			alert("hell0");
		}


		var mc = new MyClass();
		var mc2 = new MyClass();
		console.log(Person.prototype == MyClass.prototype);  
		//false 每个函数都有它自己的prototype
		

		console.log(mc.__proto__);   //Object
		console.log(mc.__proto__ == MyClass.prototype);  //true
		console.log(mc2.__proto__ == MyClass.prototype);  //true

		//向mc中添加a属性
		//mc.a = "我是mc中的a";	//如果有这句话显示的就不是123了

		console.log(mc.a);		//123  此时mc中没有a,这个123是从原型对象里找的

		mc.sayHello();		//hello
		console.log(mc.__proto__ === MyClass.prototype);		//true
		
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 设置原型

[函数对象、对象、原型](https://juejin.cn/post/6844903793285398535)

![](JavaScript知识点查漏补缺/76.png)

## 获取原型对象的方法

![](JavaScript知识点查漏补缺/77.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 *创建一个构造函数
		 * 
		 */
		
		function MyClass(){

		}

		//向MyClass的原型中添加一个name属性
		MyClass.prototype.name = "我是原型中的名字";
		var mc = new MyClass();
		console.log(mc.name);			//"我是原型中的名字";

		//使用in检查对象中是否含有某个属性时，如果对象中没有但是原型中有，也会返回true
		console.log("name" in mc);		//true

		//可以使用对象的hasOwnProperty()来检查对象自身中是否含有该属性
		//使用该方法只有当对象自身含有该属性时，才会返回true
		console.log(mc.hasOwnProperty("name"));  //false
		console.log(mc.hasOwnProperty("hasOwnProperty"));  //false

		/**
		 * 原型对象也是对象，所以它也有原型
		 * 		当我们在使用一个对象的属性或方法时，会先在自身中寻找，
		 * 		自身中如果有，则直接使用
		 * 		如果没有则去原型对象中寻找，如果原型对象中有，则使用
		 * 		如果没有则去原型的原型中寻找，直到找到Object对象的原型
		 * 		（Object对象的原型没有原型，如果在Object中依然没有找到，则返回undefined）
		 */
		console.log(mc.__proto__.hasOwnProperty("hasOwnProperty")); 
		//false 原型里也没有
		console.log(mc.__proto__.__proto__.hasOwnProperty("hasOwnProperty")); 
		//true 原型的原型里有

	</script>
</head>
<body>
	
</body>
</html>
~~~

## 原型链

![](JavaScript知识点查漏补缺/78.png)

# instanceof

![](JavaScript知识点查漏补缺/80.png)

# 引用类型

![](JavaScript知识点查漏补缺/82.png)

## Object

![](JavaScript知识点查漏补缺/83.png)

## Array

![](JavaScript知识点查漏补缺/84.png)

### 数组方法1

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		var arr = ["孙悟空" , "猪八戒" , "沙和尚"];
		var arr2 = ["白骨精" , "蜘蛛精" , "玉兔精"];
		var arr3 = ["菩提老祖" , "太上老君" , "玉皇大帝"];
		/**
		 * concat可以连接两个或多个数组，并将新的数组返回
		 * 	-该方法不会对原数组产生影响
		 */
		
		var result = arr.concat(arr2);
		console.log(arr);
		console.log(arr2);
		console.log(result);

		var result2 = arr.concat(arr2,arr3,"牛魔王","铁扇公主");
		console.log(result2);

		/**
		 * join()
		 * 	-该方法可以将数组转换为一个字符串
		 * 	-该方法不会对原数组产生影响，而是将转换后的字符串作为结果返回
		 * 	-在join中可以指定一个字符串作为参数，这个字符串将会成为数组中元素的连接符
		 * 			如果不指定连接符，则默认使用，作为连接符
		 */
		var arr4 = ["小虎" , "小驴" , "小猫"];
		var result3 = arr4.join("-");
		console.log(typeof result3);	//string
		console.log(result3);		//小虎-小驴-小猫

		/**
		 * reverse()
		 * 	-该方法用来反转数组（前边的去后边，后边的去前边）
		 * 	-该方法会直接修改原数组
		 */
		arr.reverse();
		console.log(arr);		//["沙和尚", "猪八戒", "孙悟空"]

		/**
		 * sort()
		 * 	-可以用来对数组进行排序
		 * 	也会影响原数组
		 */
		arr5 = ["b" , "a" , "c" , "f" , "d"];
		arr5.sort();
		console.log(arr5);

		/**
		 * 即使对于纯数字的数组，使用sort()排序时，也会按照Unicode编码来排序
		 * 	所以对数字进行排序时，可能会得到错误的结果
		 * 
		 */
		
		arr6 = [1 , 8 , 6 , 7 , 2 , 11 , 4 , ]
		arr6.sort();
		console.log(arr6);	//[1, 11, 2, 4, 6, 7, 8] 这种排序是错误的

		/**
		 * 我们可以自己来指定排序的规则
		 * 	 我们可以在sort()中添加一个回调函数，来指定排序规则
		 * 	 回调函数中需定义两个形参
		 * 	 浏览器将会分别使用数组中的元素作为实参去调用回调函数
		 * 	 使用哪个元素调用不确定，但是肯定的是在数组中a肯定在b前面
		 *
		 * -浏览器会根据回调函数的返回值来决定元素的顺序
		 * 		如果返回一个大于0的值，则元素会交换位置
		 * 		如果返回一个小于0的值，则元素位置不变
		 * 		如果返回一个0，则认为两个元素相等，也不交换位置
		 */
		
		arr7 = [5 ,4 ,3,11 , 3 ,2 ,9];
		arr7.sort(function(a,b){
			/*if(a > b){
				return 1;
			}else if(a < b){
				return -1;
			}else{
				return 0;
			}
			return 1;*/

			//升序排列
			return a-b;

			//降序排序
			//return b-a;
			
			
			//console.log("a= " + a);
			//console.log("b= " + b);
		});
		console.log(arr7);
	</script>
</head>
<body>
	
</body>
</html>
~~~

### 数组方法2

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		//创建一个字符串
		var str = "Hello World";
		/**
		 * 在底层字符串是以字符数组的形式保存的
		 * ["H" ,"e", "l" , "l" ,"o","W","o","r","l","d"]
		 */
		
		/**
		 * length属性（一说属性，不用加括号）
		 * 	 -可以用来获取字符串的长度
		 */
		console.log(str.length);	//11
		console.log(str[0]);        //H

		/**
		 * charAt()
		 * 	-可以返回字符串指定位置的字符
		 * 	-根据索引获取指定的字符
		 */
		str = "Hello World";
		var result = str.charAt(0);  //等价于var result = str[0];
		console.log("result = " + result); //result= H
		console.log(str);

		/**
		 * charCodeAt()
		 * 返回在指定的位置的字符的 Unicode 编码。
		 */
		result = str.charCodeAt(0);
		console.log(result);	//72

		/**
		 * formCharCode()--和上面的是反向操作
		 * 	-可以根据字符编码去获取字符（从字符编码创建一个字符串。）
		 * 	这个方法是属于构造函数对象的，得通过构造函数的对象去调
		 */
		result = String.fromCharCode(72);
		console.log(result);   //H

		/**
		 * concat()
		 * 	-可以用来连接2个或多个字符串
		 * 	-作用和 + 一样
		 */
		result = str.concat("你好" , "再见");
		console.log(result);		//Hello World你好再见

		/**
		 * indexOf()
		 * 	-该方法可以检索一个字符串中是否含有指定内容
		 * 	-如果字符串中含有该内容，则会返回其第一次出现的索引（第二次出现不管）
		 * 		如果没有找到指定的内容，则返回-1
		 *
		 * -可以指定一个第二个参数，指定开始查找的位置
		 */
		
		str = "Hello Hey World";
		result1 = str.indexOf("h");		
		result2 = str.indexOf("H");		
		result3 = str.indexOf("H",4);	 //表示从位置4开始查找	
		console.log(result1);		//-1 表示没有
		console.log(result2);		//0 表示有，并且位置是0（即第一个）
		console.log(result3);		//6 表明在位置6

		/**
		 * lastIndexOf();
		 * 	-该方法的用法和indexOf()一样，
		 * 		不同的是indexOf是从前往后找
		 * 		而lastIndexOf是从后往前找
		 *
		 * -lastIndexOf()方法可返回一个指定字符串值最后出现的位置，在一个字符串中的指定位置从后向前搜索。
		 */
		str = "Hello Hey World";
		result3 = str.lastIndexOf("l",4);
		console.log(result3);	//3

		/**
		 * slice
		 * 	-可以从字符串中截取指定的内容
		 * 	-不会影响原字符串，而是将截取到的内容返回
		 * 	-参数：
		 * 		第一个，开始位置的索引（包括开始位置）
		 * 		第二个，结束位置的索引（不包括结束位置）
		 * 			-如果省略第二个参数，则会截取到后边所有的
		 * 		-也可以传递一个负数作为参数，负数的话将会从后边计算
		 */
		
		str = "abcdefghijk";
		result = str.slice(0,2);
		console.log(result);  //ab 

		/**
		 * substring()
		 * 	-可以用来截取一个字符串，和slice()类似
		 * 	-参数：
		 * 		第一个，开始位置的索引（包括开始位置）
		 * 		第二个，结束位置的索引（不包括结束位置）
		 * 		不同的是这个方法不能接收负值作为参数
		 * 			如果传递了一个负值，则默认使用0
		 * 		而且它会自动调整参数位置，如果第二个参数小于第一个，则自动交换	
		 * 		
		 */
		result = str.substring(0,2);  //写成result = str.substring(2,0);也行，会自动交换
		console.log(result);  //ab 

		/**
		 * substr()
		 * 	-用来截取字符串
		 * 	-参数
		 * 		第一个，截取开始位置的索引
		 * 		第二个，截取的长度
		 */
		str = "abcdefg";
		result = str.substr(3,2);
		console.log(result);	//de

		/**
		 * split()
		 * 	-可以将一个字符串拆分为一个数组
		 * 	-参数：
		 * 		-需要一个字符串作为参数，将会根据该字符串去拆分数组
		 * 		(拆完以后就变成数组了)
		 */
		str = "abc , bcd , efg";
		result = str.split(",");
		console.log(typeof result);   //object
		console.log(Array.isArray(result));  //true
		console.log(result[0]);   //abc
		console.log(result.length);  //4

		/**
		 * 如果传递一个空串作为参数，则会将每个字符都拆分为数组中的一个元素
		 * 
		 */
		str = "abcdefg";
		result = str.split("");	
		console.log(result);   //["a", "b", "c", "d", "e", "f", "g"]
		/**
		 * toUpperCase()
		 * 	-将一个字符串转换为大写并返回
		 */
		str = "abcdefg";
		result = str.toUpperCase();
		console.log(result); 	//ABCDEFG

		/**
		 * toLowerCase()
		 * 	-将一个字符串转换为小写并返回
		 */
		str = "ABCDEFG";
		result = str.toLowerCase();

	</script>
</head>
<body>
	
</body>
</html>
~~~

## Date

![](JavaScript知识点查漏补缺/85.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>	</title>
	<script>
		/**
		 * 	Date对象
		 * 	  -在JS中使用Date对象来表示时间
		 */
		
		//创建一个Date对象
		//如果直接使用构造函数创建一个Date对象，则会封装为当前代码执行的时间
		var d = new Date();
		console.log(d);

		//创建一个指定的时间对象
		//需要在构造函数中传递一个表示时间的字符串作为参数
		//日期的格式 月份/日/年 时：分：秒   （年份写完整的，避免歧义）
		var d2 = new Date("12/03/2006 11:10:30");
		console.log(d2);

		/**
		 * getDate()
		 * 	-从 Date 对象返回一个月中的某一天 (1 ~ 31)。
		 */
		var date = d2.getDate();
		console.log("date = " + date);  //13

		/**
		 * getDay()
		 * 	-从 Date 对象返回一周中的某一天 (0 ~ 6)。
		 * 	-会返回一个0-6的值（0表示周日）
		 */
		var day = d2.getDay();
		console.log("day = " + day);	//0

		/**
		 * getMonth()
		 *  -从 Date 对象返回月份 (0 ~ 11)。
		 *  -会返回0-11的值（0表示一月）
		 */
		var month = d2.getMonth();
		console.log("month =" + month);

		/**
		 * getFullYear()    -----getYear()方法废了，不用了
		 * 	-从 Date 对象以四位数字返回年份。
		 */
		var year = d2.getFullYear();
		console.log("year =" + year);

		/**
		 * getTime()--时间很乱，各种进制都有，所以统一转换为毫秒
		 * 	-获取当前日期对象的时间戳（返回 1970 年 1 月 1 日至今的毫秒数。）
		 * 	-时间戳，指的是从格林威治标准时间的1970年1月1日，0时0分0秒
		 * 		到当前日期所花费的毫秒数   1秒 = 1000毫秒
		 *
		 * -计算机底层在保存时间时使用的都是时间戳
		 */
		var time = d2.getTime();
		console.log("time =" + time);		//time =1165115430000

		var d3 = new Date("1/1/1970 0:0:0");  
		//这个写的时间时中国时间，和标准时间有8小时时间差
		time = d3.getTime();
		console.log(time);   //-28800000

		//获取当前的时间戳
		time = Date.now();
		console.log(time);	//1570626732516  当前时间

		//利用时间戳来测试代码执行的性能
		//在循环开始之前获取一个时间戳
		var start = Date.now();  
		for(var i = 0; i < 100; i++){
			console.log(i);
		}
		//在循环结束之后获取一个时间戳
		var end = Date.now();  

		console.log("执行了" + (end - start) + "毫秒");  //执行了2毫秒
	</script>
</head>
<body>
	
</body>
</html>
~~~

## Function

![](JavaScript知识点查漏补缺/86.png)

### 函数也可以作为参数

![](JavaScript知识点查漏补缺/87.png)

### 函数对象的方法

![](JavaScript知识点查漏补缺/88.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		function fun(){
			alert(this.name);
		}
		/**
		 * call()和apply()
		 * 	-这两个方法都是函数对象的方法，需要通过函数对象来调用
		 * 	-当对函数调用call()和apply()都会调用函数执行
		 * 	-在调用call()和apply()可以将一个对象指定为第一个参数
		 * 		此时这个对象将会称为函数执行时的this
		 *
		 * -call()方法可以将实参在对象之后依次传递
		 * -apply()方法可以将实参封装到数组中同一传递
		 *
		 * this的情况
		 * 		1.以函数的形式调用时，this永远都是window
		 * 		2.以方法的形式调用时，this是调用方法的对象
		 * 		3.以构造函数的形式调用时，this是新创建的那个对象
		 * 		4.使用call和apply调用时，this是指定的那个对象
		 */
		
		//fun.call();
		//fun.apply();
		
		fun.call(obj,2,3);
		fun.apply(obj,[2,3]);
		var obj = {
			name:"obj",
			sayName:function(){
				//alert(this.name);
				alert(this.name);
			}
		};
		var obj2 = {name:"obj2"};
		//fun.call(obj);  //[object Object]
		//fun.call(obj);	//[object Object]
		//fun();			//[object Window]

		obj.sayName.apply(obj2);
	</script>	
</head>
<body>
	
</body>
</html>
~~~

### 闭包(closure)

![](JavaScript知识点查漏补缺/89.png)

## 基本包装类型

![](JavaScript知识点查漏补缺/90.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 基本数据类型
		 * 	String 	字符串
		 * 	Number 	数值
		 * 	Boolean 布尔值
		 * 	Null 	空值
		 * 	Undefined 未定义
		 * 	Object  对象
		 * 		
		 * 引用数据类型
		 * Object
		 *
		 * 在JS中为我们提供了三个包装类，通过这三个包装类可以将基本数据类型的数据转换为对象
		 *(这三个首字母都大写，都是构造函数)
		 * 1.String()
		 * 		-可以将基本数据类型字符串转换为String对象
		 * 2.Number()
		 * 		-可以将基本数据类型数值转换为Number对象
		 * 3.Boolean()
		 * 		-可以将基本数据类型布尔值转换为Boolean对象
		 *
		 * 但是注意：我们在实际应用中不会使用基本数据类型的对象
		 * 		如果使用基本数据类型的对象，在做一些比较时，可能会带来一些不可预期的结果
		 */
		
		//var a = 123;
		//console.log(typeof a);		//number

		//创建一个Number类型的对象
		var num = new Number(3);
		var num2 = new Number(3);
		console.log(typeof num);	//object
		console.log(num == num2);	//false  两个对象，内存地址不一样

		var str = new String("hello");
		console.log(typeof str);	//object

		var bool = new Boolean(true);
		var bool2 = true;
		console.log(typeof bool);	//object
		console.log(bool == bool2); //true  自动进行类型转换了
		console.log(bool === bool2); //false  

		//向num中添加一个属性
		num.hello = "abcdefg";
		console.log(num.hello);		//abcdefg

		var b = new Boolean(false);		//布尔值false转换为对象变成true,所以会运行
			if(b){
				alert("我运行了");  
			}
		/**
		 * 方法和属性只能添加给对象，不能添加给基本数据类型
		 * 当我们对一些基本数据类型的值去调用属性和方法时，
		 * 		浏览器会临时使用包装类将其转换为对象，然后再调用对象的属性和方法
		 *   	调用完以后，再将其转换为基本数据类型
		 */
		var s = 123;
		s = s.toString();		
		//照理说基本数据类型没有方法，但是这里它没有报错。解析器临时将s包装成对象
		s.hello = "你好";
		console.log(s);			//"123"
		console.log(s.hello);			//undefined
		console.log(typeof s);	//string
	</script>
</head>
<body>
	
</body>
</html>
~~~

### Boolean

![](JavaScript知识点查漏补缺/91.png)

### Number

![](JavaScript知识点查漏补缺/92.png)

### String

![](JavaScript知识点查漏补缺/93.png)

## Math

[Math.random()](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/random)

![](JavaScript知识点查漏补缺/94.png)

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * Math
		 * 	-Math和其他的对象不同，它不是一个构造函数（虽然开头大写）
		 * 		它属于一个工具类不用创建对象，它里面封装了数学运算相关的属性和方法
		 * 	-比如
		 * 		Math.PI表示的圆周率
		 */
		console.log(Math.PI);		//3.141592653589793

		/**
		 * abs()可以用来计算一个数的绝对值
		 */
		console.log(Math.abs(-25));		//25

		/**
		 * Math.ceil()
		 * 		-可以对一个数进行向上取整：小数位只要有值就自动进1
		 * Math.floor()
		 * 		-可以对一个数进行向下取整,小数部分会被舍弃掉
		 *
		 * Math.round()
		 * 		-可以对一个数进行四舍五入取整
		 */
		console.log(Math.ceil(1.2));    //2
		console.log(Math.floor(1.99));  //1
		console.log(Math.round(1.52));  //2

		/**
		 * Math.random()
		 * 		-可以用来生成一个0-1之间的随机数
		 * 		-生成一个0-10的随机数
		 * 		-生成0-x之间的随机数 Math.round(Math.random()*x)
		 * 		-生成1-10  Math.round(Math.random()*9 + 1
		 * 		-生成x-y   Math.round(Math.random()*(y-x) + x)
		 */
		console.log(Math.random());  //0.33978771093767546  每次都不一样

		for(var i = 0; i < 10; i++){
			console.log(Math.round(Math.random()*10));
		}

		/**
		 * max(可以获取多个数中的最大值)  --不限制数量
		 * min(可以获取多个数中的最小值)
		 */
		var max = Math.max(10,20,30);
		console.log(max);		//30

		/**
		 * Math.pow(x,y)
		 * 返回x的y次幂
		 */
		console.log(Math.pow(2,4));		//16

		/**
		 * Math.sqrt()
		 * 用于对一个数进行开方运算
		 */
		console.log(Math.sqrt(4));		//2
	</script>
</head>
<body>
	
</body>
</html>
~~~



### Math对象的属性

![](JavaScript知识点查漏补缺/95.png)

### Math的方法

![](JavaScript知识点查漏补缺/96.png)



# 正则表达式

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 创建一个正则表达式检查一个字符串中是否含有aaaaaa
		 */
		
		/**
		 * 量词
		 * 	-通过量词可以设置一个内容出现的次数
		 * 	-量词只对它前边的一个内容起作用
		 * 	-{n} 正好出现n次
		 */
		
		//笨方法
		var reg = /aaaaaa/;
		console.log(reg.test("abc"));  //false
		console.log(reg.test("aaaaaabc"));  //true

		reg = /a{3}/;
		console.log(reg.test("aaabd"));  //true

		reg = /(ab){3}/;
		console.log(reg.test("abababdkldk"));  //true

		reg = /ab{3}c/;
		console.log(reg.test("abbbcde"));	//true

		reg = /b{3}/;
		console.log(reg.test("bbbb"));	//true  找是否有连续出现的三个b
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 示例1

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 正则表达式（是一个对象）
		 * 		-admin
		 * 		-admin@atguigu.com
		 * 		-admin@.com adminatguigu.com
		 * 		-abc@abc.com
		 * 		
		 * 		-邮件的规则	
		 * 		1.前面可以是×××乱七八糟
		 * 		2.跟着一个@
		 * 		3.后面可以是×××乱七八糟
		 * 		4. .com获取其他的乱七八糟
		 *
		 * -正则表达式用于定义一些字符串的规则
		 * 		计算机可以根据正则表达式，来检查一个字符串是否符合规则
		 * 		或者将字符串中符合规则的内容提取出来		
		 */
		//创建正则表达式的对象
		/**
		 * 语法：
		 * var 变量 = new RegExp("正则表达式" , "匹配模式");
		 * 使用typeof检查正则对象，会返回object
		 * 这个正则表达式可以用来检查一个字符串里是否含有a
		 *
		 * 在构造函数中，可以传递一个匹配模式作为第二个参数
		 * 		可以是
		 * 			 i 忽略大小写
		 * 			 g 全局匹配模式
		 */
		var reg1 = new RegExp("a");
		console.log(reg1);	// /a/
		console.log(typeof reg1);   //object

		var str = "abc";
		/**
		 * 正则表达式的方法：
		 *  test()
		 *   -使用这个方法可以用来检查一个字符串是否符合正则表达式的规则
		 *   	如果符合则返回true,否则返回false	
		 */
		var result = reg1.test(str);
		console.log(result);	//true
		console.log(reg1.test("Abcbc"));  //false 正则表达式严格区分大小写

		//var reg2 = new RegExp("a", "i");
		//console.log(reg2.test("Abcbc"));  	//true 忽略大小写
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 示例2

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 使用字面量来创建正则表达式
		 * 	 语法： var 变量 = /正则表达式/匹配模式
		 *
		 * 使用字面量的方式创建更加简单
		 * 	使用构造函数创建更加灵活
		 */
		var reg = /a/i;
		//var reg = new RegExp("a", "i");
		console.log(reg.test("abc"));  //true
		console.log(typeof reg);       //object

		//创建一个正则表达式，检查一个字符串中是否有a或b
		/**
		 * 使用竖线|表示或者的意思
		 * 
		 */
		reg = /a|b|c/;
		console.log(reg.test("acd"));  //true

		/**
		 * 创建一个正则表达式检查一个字符串中是否有字母
		 * []里的内容也是或的关系
		 * [ab] == a | b
		 * [a-z] 表示任意小写字母
		 * [A-Z] 表示任意大写字母
		 * [A-z] 表示任意字母
		 * [0-9] 表示任意数字
		 */
		reg = /[a-z]/
		console.log(reg.test("p"));  //true

		//检查一个字符串中是否含有abc 或adc 或aec
		//比较笨的写法
		reg = /abc|adc|aec/;

		//比较聪明的写法
		reg = /a[bde]c/;
		console.log(reg.test("aec"));  //true

		/**
		 * [^×] 除了×以外的东西
		 * 
		 */
		reg = /[^ab]/;
		console.log(reg.test("abc"));  //true  有除了ab以外的东西
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 示例3

[String.prototype.split()](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/split)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		var str = "1a2b3c4d5f6";
		/**
		 * split()
		 * 	-可以将一个字符串拆分为一个数组
		 * 	-方法中可以传递一个正则表达式作为参数，这样方法将会根据正则表达式去拆分字符串
		 * 	-这个方法即使不指定全局匹配，也会全部拆分
		 */
		/**
		 * 根据任意字母来将字符串拆分
		 * 
		 */
		var result = str.split(/[A-z]/);  //写不写g都行 
		console.log(result);	//["1", "2", "3", "4", "5", "6"]

		/**
		 * search()
		 * 	-可以搜索字符串中是否含有指定内容
		 * 	-如果搜索到指定内容，则会返回第一次出现的索引，如果没有搜索到则会返回-1
		 * 	-它可以接收一个正则表达式作为参数，然后会根据正则表达式去检索字符串
		 * 	-search()只会查找第一个，即使设置全局匹配也没用
		 */
		str = "hello abc hello aec afc";
		/**
		 * 搜索字符串中是否含有abc 或aec 或afc
		 * 
		 */
		result = str.search(/a[bef]c/);
		console.log(result);  //6  索引是6

		/**
		 * match()
		 * 	-可以根据正则表达式，从一个字符串中将符合条件的内容提取出来
		 * 	-默认情况下我们的match只会找到第一个符合要求的内容，找到以后就停止检索
		 * 		我们可以设置正则表达式为全局匹配模式，这样就会匹配到所有的内容
		 * 		可以为一个正则表达式设置多个匹配模式，且顺序无所谓
		 * 	-match()会将匹配到的内容封装到数组中返回，即使只查询到一个结果
		 */
		
		str2 = "1a2b3c4d5f6A7B8C9";
		result = str2.match(/[A-z]/gi);  //既全局匹配，又忽略大小写
		console.log(result);  //"a b c d e f A B C"
		console.log(typeof result);  //object
		console.log(Array.isArray(result));  //true 
		console.log(result[0]);  //a

		/**
		 * replace()
		 * 	-可以将字符串中指定内容替换为新的内容
		 * 	-参数
		 * 		1.被替换的内容，可以接收一个正则表达式接收参数
		 * 		2.新的内容
		 * 	-默认只会替换第一个
		 */
		result = str.replace(/[A-z]/ig , " ");   //1 2 3 4 5 6 7 8 9
		console.log(result);
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 示例4

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 创建一个正则表达式检查一个字符串中是否含有aaaaaa
		 */
		
		/**
		 * 量词
		 * 	-通过量词可以设置一个内容出现的次数
		 * 	-量词只对它前边的一个内容起作用
		 * 	-{n} 正好出现n次
		 * 	-{m,n} 出现m-n次
		 * 	-{m,} m次以上
		 * 	- + 至少一个，相当于{1,}
		 * 	- * 表示0个或多个，相当于{0,}
		 * 	- ? 表示0个或一个，相当于{0,1}
		 */
		
		//笨方法
		var reg = /aaaaaa/;
		console.log(reg.test("abc"));  //false
		console.log(reg.test("aaaaaabc"));  //true

		reg = /a{3}/;
		console.log(reg.test("aaabd"));  //true

		reg = /(ab){3}/;
		console.log(reg.test("abababdkldk"));  //true

		reg = /ab{3}c/;
		console.log(reg.test("abbbcde"));	//true

		reg = /b{3}/;
		console.log(reg.test("bbbb"));	//true  找是否有连续出现的三个b

		reg = /ab{1,3}c/;
		console.log(reg.test("abbc"));  //true

		reg = /ab+c/;
		console.log(reg.test("abbbbbc"));  //true

		reg = /ab*c/;
		console.log(reg.test("ac"));  //true

		reg = /ab?c/;
		console.log(reg.test("abbc"));  //false

		/**
		 * 检查一个字符串中是否以a开头
		 * ^表示开头([]里的^表示除了)
		 * $表示结尾
		 */
		reg = /^a/;
		console.log(reg.test("bcabc"));  //false

		reg = /a$/;
		console.log(reg.test("bcabca"));  //true

		/**
		 * 如果再正则表达式中同时使用^$则要求字符串必须完全符合正则表达式
		 * 
		 */
		reg = /^a$/   //a既是开头，又是结尾，即只有一个a
		console.log(reg.test("aaa"));  //false
		console.log(reg.test("a"));  //true

		reg = /^a|a$/  //表示以a开头或者以a结尾
		console.log(reg.test("abc"));  //true

		/**
		 * 创建一个正则表达式，用来检查一个字符串是否是一个手机号
		 * 
		 * 手机号的规则：
		 * 	18008814924(11位)
		 * 	
		 * 	1.以1开头
		 * 	2.第2位是3-9的任意数字
		 * 	3.三位以后任意数字9个
		 *
		 * ^1 [3-9] [0-9]{9}$
		 */
		var phoneStr = "18088149243";  //true 	

		var phoneReg = /^1[3-9][0-9]{9}$/
		console.log(phoneReg.test(phoneStr));
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 示例5

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 检查一个字符串中是否含有点(.)
		 * .属于元字符[(Metacharacter)是拥有特殊含义的字符],查找单个字符，除了换行和行结束符。
		 * 在正则表达式中使用\作为转义字符
		 * \.可以来表示.
		 * \\今天用来表示\
		 *
		 * 注意：使用构造函数时，由于它的参数是字符串，而\是字符串中的转义字符，
		 * 	如果要使用\,则需要使用\\来代替
		 */
		
		var reg = /./;
		console.log(reg.test("."));  //true
		console.log(reg.test("abcded"));  //true!!!!

		 reg = /\./;
		console.log(reg.test("abcded"));  //false  这下才能正确识别.

		reg = new RegExp("\\.");
		console.log(reg);  //  /\./

		/**
		 * \w  --任意字母、数字、下划线 相当于[A-z0-9]
		 * \W  --除了字母、数字、下划线 相当于[^A-z0-9]
		 * \s  --空格
		 * \S  --除了空格
		 * \D  --除了数字
		 * \d  --任意数字
		 * \b  --单词边界
		 * \B  --除了单词边界
		 */
		
		reg = /\w/;
		console.log(reg.test("e"));  //true

		/**
		 * 创建一个正则表达式检查一个字符串中是否含有单词child
		 */
		reg = /child/;
		console.log(reg.test("hello children"));  
		//true 检查是否有child，只要有child,无论它是否是个独立的单词，都行
		
		reg = /\bchild\b/;
		console.log(reg.test("hello children"));   //false
		console.log(reg.test("hello child"));		//true

		//接收一个用户的输入
		//var str = prompt("请输入你的用户名:");
		//console.log(str); 

		//去除掉字符串中前后的空格（中间的空格不管的）
		//去除空格就是使用""来替换空格
		var str = "           he       llo                ";
		//去除前面的(多个)空格
		str = str.replace(/^\s*/,"");
		console.log(str);

		//去除结尾的(多个)空格
		str = str.replace(/\s*$/,"");
		console.log(str);

		//同时去开头和结尾的多个空格
		str = str.replace(/^\s* | \s*$/g,"");
		console.log(str);
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 示例6

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 电子邮件
		 * 	hell0@abc.com.cn
		 * 	任意字母数字下划线 .任意字母数字下划线 @ 任意字母数字 .任意字母(2-5位).	.任意字母(2-5位)
		 *
		 * /^\w{3,}(\.\w+)*@[A-z0-9]+(\.[A-z]{2,5}){1,2}$/
		 */
		
		var emailReg = /^\w{3,}(\.\w+)*@[A-z0-9]+(\.[A-z]{2,5}){1,2}$/;
		var email = "abc.hello@163.com";
		console.log(emailReg.test(email));   //true
	</script>
</head>
<body>
	
</body>
</html>
~~~

# DOM

## 什么是DOM

![](JavaScript知识点查漏补缺/97.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	<button id="btn">我是一个按钮</button>
	<script>
		/**
		 * 浏览器已经为我们提供了文档节点对象，这个对象是window对象的属性
		 * 	可以在页面中直接使用，文档节点代表的是整个网页
		 * 	DOM中的对象和网页内容都是有一一对应关系的
		 */
		console.log(document);   //object HTMLDocument  document就代表整个网页

		//获取到button对象
		var btn = document.getElementById("btn");   //object HTMLButtonElement

		//修改按钮的文字
		console.log(btn.innerHTML);   //我是一个按钮
		btn.innerHTML = "I'am Button";
	</script>
</body>
</html>
~~~



## 页面加载

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * 浏览器在加载一个页面时是按照自上向下的顺序加载的
		 * 	读取到一行就运行一行，如果将script标签写到页面的上边
		 * 	在代码执行时，页面还没有加载，页面没有加载DOM对象也没有加载
		 * 	会导致无法获取到DOM对象
		 */
		
		/**
		 * 将js代码编写到页面的下部就是为了可以在页面加载完毕以后再执行js代码
		 */
				
		/**
		 * onload事件会在整个页面加载完成之后才触发
		 * 为window绑定一个onload事件
		 * 		该事件对应的响应函数将会在页面加载完成之后执行
		 * 		这样可以确保我们的代码执行时所有的DOOM对象已经加载完毕了
		 * 		
		 * 
		 */
		window.onload = function(){
			//获取id为btn的按钮
			var btn = document.getElementById("btn");

			//为按钮绑定一个单击响应函数
			btn.onclick = function(){
			alert("hello");
			};
		};
	</script>
</head>
<body>
	<button id="btn">点我一下</button>
</body>
</html>
~~~

## 模型

![](JavaScript知识点查漏补缺/98.png)

## 节点

![](JavaScript知识点查漏补缺/99.png)

~~~javascript
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
	<head>
		<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
		<title>Untitled Document</title>
		<link rel="stylesheet" type="text/css" href="style/css.css" />
		<script type="text/javascript">
			window.onload = function(){
				//为id为btn01的按钮绑定一个单击响应函数
				var btn01 = document.getElementById("btn01");
				btn01.onclick = function(){
					//查找#bj节点
					var bj = document.getElementById("bj");
					//打印bj
					//innerHTML 通过这个属性可以获取到元素内部的html代码
					alert(bj.innerHTML);
				};
				

				//为id为btn02的按钮绑定一个单击响应函数
				var btn02 = document.getElementById("btn02");
				btn02.onclick = function(){
					//查找所有li节点
					//getElementsByTagName()可以根据标签名来获取一组元素节点对象
					//这个方法会给我们返回一个类数组对象，所有查询到的元素都会封装到对象中
					//即使查询到的元素只有一个，也会封装到数组返回
					var list = document.getElementsByTagName("li");   //加s
					//打印list长度
					alert(list.length);

					//遍历list
					for(var i = 0; i < list.length; i++){
						alert(list[i].innerHTML);
					};
				};
				
				//为id为btn03的按钮绑定一个单击响应函数
				var btn03 = document.getElementById("btn03");
				btn03.onclick = function(){
					//查找name=gender的所有节点
					var inputs = document.getElementsByName("gender");
					//打印inputs长度
					alert(inputs.length);

					//遍历inputs
					for(var i = 0; i < inputs.length; i++){
						/**
						 * innerHTML用于获取元素内部的HTML代码
						 * 	对于字节数标签，这个属性没有意义
						 */
						
						//alert(inputs[i].innerHTML);  //没有意义
						
						/**
						 * 如果需要读取元素节点的属性，
						 * 		直接使用元素.属性名
						 * 			例子：元素.id  元素.name  元素.value
						 * 			注意：class属性不能采用这种方式
						 * 			读取class属性时需要使用元素.className
 						 */
						alert(inputs[i].value);
					};	
				};
				
				//查找#city下所有li节点
				//返回#city的所有子节点
				//返回#phone的第一个子节点
				//返回#bj的父节点
				//返回#android的前一个兄弟节点
				//读取#username的value属性值
				//设置#username的value属性值
				//返回#bj的文本值
			};
						
		</script>
	</head>
	<body>
		<div id="total">
			<div class="inner">
				<p>
					你喜欢哪个城市?
				</p>

				<ul id="city">
					<li id="bj">北京</li>
					<li>上海</li>
					<li>东京</li>
					<li>首尔</li>
				</ul>

				<br>
				<br>

				<p>
					你喜欢哪款单机游戏?
				</p>

				<ul id="game">
					<li id="rl">红警</li>
					<li>实况</li>
					<li>极品飞车</li>
					<li>魔兽</li>
				</ul>

				<br />
				<br />

				<p>
					你手机的操作系统是?
				</p>

				<ul id="phone">
					<li>IOS</li>
					<li id="android">Android</li>
					<li>Windows Phone</li>
				</ul>
			</div>

			<div class="inner">
				gender:
				<input type="radio" name="gender" value="male"/>
				Male
				<input type="radio" name="gender" value="female"/>
				Female
				<br>
				<br>
				name:
				<input type="text" name="name" id="username" value="abcde"/>
			</div>
		</div>
		<div id="btnList">
			<div><button id="btn01">查找#bj节点</button></div>
			<div><button id="btn02">查找所有li节点</button></div>
			<div><button id="btn03">查找name=gender的所有节点</button></div>
			<div><button id="btn04">查找#city下所有li节点</button></div>
			<div><button id="btn05">返回#city的所有子节点</button></div>
			<div><button id="btn06">返回#phone的第一个子节点</button></div>
			<div><button id="btn07">返回#bj的父节点</button></div>
			<div><button id="btn08">返回#android的前一个兄弟节点</button></div>
			<div><button id="btn09">返回#username的value属性值</button></div>
			<div><button id="btn10">设置#username的value属性值</button></div>
			<div><button id="btn11">返回#bj的文本值</button></div>
		</div>
	</body>
</html>
~~~

**style.css**

~~~css
@CHARSET "UTF-8";

body {
	width: 800px;
	margin-left: auto;
	margin-right: auto;
}

button {
	width: 300px;
	margin-bottom: 10px;
}

#btnList {
	float:left;
}

#total{
	width: 450px;
	float:left;
}

ul{
	list-style-type: none;
	margin: 0px;
	padding: 0px;
}

.inner li{
	border-style: solid;
	border-width: 1px;
	padding: 5px;
	margin: 5px;
	background-color: #99ff99;
	float:left;
}

.inner{
	width:400px;
	border-style: solid;
	border-width: 1px;
	margin-bottom: 10px;
	padding: 10px;
	float: left;
}
~~~



## 节点的属性

![](JavaScript知识点查漏补缺/101.png)

## 文档节点(document)

![](JavaScript知识点查漏补缺/102.png)

## 元素节点(element)

![](JavaScript知识点查漏补缺/103.png)

## 文本节点(text)

![](JavaScript知识点查漏补缺/104.png)

## 属性节点(Attr)

![](JavaScript知识点查漏补缺/105.png)

## 使用DOM操纵CSS

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#box1 {
		width: 200px;
		height: 200px;
		background-color: red;
	}
	</style>
	<script>
		window.onload = function(){
			/**
			 * 点击按钮以后，修改box1的大小
			 */
			//获取box1
			var box1 = document.getElementById("box1");
			//为按钮绑定单击响应函数
			var btn1 = document.getElementById("btn1");
			btn1.onclick = function(){
				//修改box1的宽度
				/**
				 * 通过JS修改元素的样式：
				 * 	语法：元素.style.样式名 = 样式值
				 *
				 * 注意：如果CSS的样式名中含有减号，这种名称在JS中是不合法的
				 * 需要将这种样式名修改为驼峰命名法：
				 * 		去掉减号，将减号后的字母大写
				 *
				 * 我们通过style属性设置的样式都是内联样式
				 * 		而内联样式具有较高的优先级，所以通过JS修改的样式往往会立即显示
				 *
				 * 但是如果在样式中写了!important,则此时样式会有最高的优先级，
				 * 		即使通过JS也不能覆盖该样式，此时会导致JS修改样式失效
				 * 		所以尽量不要为样式添加!important
				 *
				 * 通过style属性设置和读取的都是内联样式
				 * 		无法读取样式表中的样式
				 */
				box1.style.width ="500px";   //要是字符串
				box1.style.height ="500px";   //要是字符串
				box1.style.backgroundColor = "blue";  // background-color  错误！！！！
			};

			//点击按钮2以后，读取元素的样式
			var btn2 = document.getElementById("btn2");
			btn2.onclick = function(){
				//读取box1的样式
				/**
				 * 语法：
				 * 	元素.style.样式名
				 */
				alert(box1.style.width);
				alert(box1.style.backgroundColor);
			};
		};
	</script>
</head>
<body>
	<button id="btn1">点我一下</button>
	<button id="btn2">点我一下</button>
	<br /><br />
	<div id="box1"></div>
</html>
~~~

## 获取元素的样式

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#box1{
			width: 100px;
			height: 100px;
			background-color: yellow;
		}
	</style>
	<script>
		window.onload = function(){
			//点击按钮以后读取box1的样式
			var box1 = document.getElementById("box1");
			var btn01 = document.getElementById("btn01");
			btn01.onclick = function(){
				//读取box1的宽度
				//alert(box1.style.width);
				/**
				 * 获取元素的当前显示的样式
				 * 	语法：元素.currentStyle.样式名
				 * 	它可以用来读取当前元素正在显示的样式
				 * 		如果当前元素没有设置该样式，则获取它的默认值
				 *
				 * 缺点：currentStyle只有IE浏览器支持，其他浏览器都不支持
				 */
				//alert(box1.currentStyle.width);
				//alert(box1.currentStyle.backgroundColor);
				
				/**
				 * 在其他浏览器中可以使用
				 * 		getComputedStyle()这个方法来获取元素的当前样式
				 * 		这个方法是window的方法，可以直接使用
				 * 	需要两个参数
				 * 		第一个：要获取样式的元素
				 * 		第二个：可以传递一个伪元素，一般都传null
				 *
				 * 该方法会返回一个对象，对象中封装了当前元素对应的样式
				 * 	可以通过对象.样式名来读取样式
				 * 	如果获取的样式名没有设置，则会获取到真实的值，而不是默认值
				 * 		比如：没有设置width,它不会获取到auto,而是一个长度
				 *
				 * 但是该方法不支持IE8及以下的浏览器
				 *
				 * 通过currentStyle和getComputedStyle()读取到的样式都是只读的，
				 * 		不能修改，如果要修改必须要通过style属性
				 */
				//var obj = getComputedStyle(box1,null);
				//alert(getComputedStyle(box1,null).width);
				
				//正常浏览器的方式
				//alert(getComputedStyle(box1,null).backgroundColor);
				
				//IE8的方式
				//alert(box1.currentStyle.backgroundColor);
				
				var w = getStyle(box1,"width");
				alert(w);
			};
		};
		/**
		 * 定义一个函数，用来获取指定元素的当前的样式	
		 * 		参数：
		 * 			obj 要获取样式的元素
		 * 			name 要获取的样式名
		 */
		function getStyle(obj , name){
			if(window.getComputedStyle){
			//正常浏览器的方式
			return getComputedStyle(obj,null)[name];				
			}else{
			//IE8的方式
			return obj.currentStyle[name];				
			}
		}
	</script>
</head>
<body>
	<button id="btn01">点我一下</button>
	<br /><br />
	<div id="box1"></div>
</body>
</html>
~~~

# DOM具体实例

## 实例1

> 就像这样的让我手写我估计自己都写不出来。所以，还是要自己多手敲代码啊。

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			
			*{
				margin: 0;
				padding: 0;
			}
			
			#outer{
				width: 500px;
				margin: 50px auto;
				padding: 10px;
				background-color: greenyellow;
				/*设置文本居中*/
				text-align: center;
			}
		</style>
		
		<script type="text/javascript">
			window.onload = function(){
				
				/*
				 * 点击按钮切换图片
				 */
				
				//获取两个按钮
				var prev = document.getElementById("prev");
				var next = document.getElementById("next");
				
				/*
				 * 要切换图片就是要修改img标签的src属性
				 */
				
				//获取img标签
				var img = document.getElementsByTagName("img")[0];
				
				//创建一个数组，用来保存图片的路径
				var imgArr = ["img/1.jpg" , "img/2.jpg" , "img/3.jpg" ,
                              "img/4.jpg" ,"img/5.jpg"];
				
				//创建一个变量，来保存当前正在显示的图片的索引
				var index = 0;
				
				//获取id为info的p元素
				var info = document.getElementById("info");
				//设置提示文字
				info.innerHTML = "一共 "+imgArr.length+" 张图片，当前第 "+(index+1)+" 张";
				
				
				//分别为两个按钮绑定单击响应函数
				prev.onclick = function(){
					
					/*
					 * 切换到上一张，索引自减
					 */
					index--;
					
					//判断index是否小于0
					if(index < 0){
						index = imgArr.length - 1;
					}
					
					img.src = imgArr[index];
					
					//当点击按钮以后，重新设置信息
					info.innerHTML = "一共 "+imgArr.length+" 张图片，
                    当前第 "+(index+1)+" 张";
				};
				
				next.onclick = function(){
					/*
					 * 切换到下一张是index自增
					 */
					index++;
					
					if(index > imgArr.length - 1){
						index = 0;
					}
					
					//切换图片就是修改img的src属性
					//要修改一个元素的属性 元素.属性 = 属性值
					img.src = imgArr[index];
					
					//当点击按钮以后，重新设置信息
					info.innerHTML = "一共 "+imgArr.length+" 张图片，当前第 "+
                    (index+1)+" 张";
					
				};
			};
		</script>
	</head>
	<body>
		<div id="outer">
			<p id="info"></p>
			<img src="img/1.jpg" alt="冰棍" />
			<button id="prev">上一张</button>
			<button id="next">下一张</button>
		</div>
	</body>
</html>

~~~

## 实例2

[JavaScript split() 方法](https://www.w3school.com.cn/js/jsref_split.asp)

~~~javascript
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<title></title>
		<script type="text/javascript">
			
			var str = prompt("请输出任意的内容:");
			
			//var arr = str.split("");
			
			//arr.reverse();
			
			//str = arr.join("");
			
			str = str.split("").reverse().join("");
			
			alert(str);
			
		</script>
	</head>
	<body>
		
	</body>
</html>
~~~

## 实例3

~~~javascript

<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<title>全选练习</title>
<script type="text/javascript">

	window.onload = function(){
		//获取四个多选框items
		var items = document.getElementsByName("items");
		//获取全选/全不选的多选框
		var checkedAllBox = document.getElementById("checkedAllBox");
		
		/*
		 * 全选按钮
		 * 	- 点击按钮以后，四个多选框全都被选中
		 */
		
		//1.#checkedAllBtn
		//为id为checkedAllBtn的按钮绑定一个单击响应函数
		var checkedAllBtn = document.getElementById("checkedAllBtn");
		checkedAllBtn.onclick = function(){
			//遍历items
			for(var i=0 ; i<items.length ; i++){
				
				//通过多选框的checked属性可以来获取或设置多选框的选中状态
				//alert(items[i].checked);
				
				//设置四个多选框变成选中状态
				items[i].checked = true;
			}
			
			//将全选/全不选设置为选中
			checkedAllBox.checked = true;
			
			
		};
		
		/*
		 * 全不选按钮
		 * 	- 点击按钮以后，四个多选框都变成没选中的状态
		 */
		//2.#checkedNoBtn
		//为id为checkedNoBtn的按钮绑定一个单击响应函数
		var checkedNoBtn = document.getElementById("checkedNoBtn");
		checkedNoBtn.onclick = function(){
			
			for(var i=0; i<items.length ; i++){
				//将四个多选框设置为没选中的状态
				items[i].checked = false;
			}
			
			//将全选/全不选设置为不选中
			checkedAllBox.checked = false;
			
		};
		
		/*
		 * 反选按钮
		 * 	- 点击按钮以后，选中的变成没选中，没选中的变成选中
		 */
		//3.#checkedRevBtn
		var checkedRevBtn = document.getElementById("checkedRevBtn");
		checkedRevBtn.onclick = function(){
			
			//将checkedAllBox设置为选中状态
			checkedAllBox.checked = true;
			
			for(var i=0; i<items.length ; i++){
				
				//判断多选框状态
				/*if(items[i].checked){
					//证明多选框已选中，则设置为没选中状态
					items[i].checked = false;
				}else{
					//证明多选框没选中，则设置为选中状态
					items[i].checked = true;
				}*/
				
				items[i].checked = !items[i].checked;
				
				//判断四个多选框是否全选
				//只要有一个没选中则就不是全选
				if(!items[i].checked){
					//一旦进入判断，则证明不是全选状态
					//将checkedAllBox设置为没选中状态
					checkedAllBox.checked = false;
				}
			}
			
			//在反选时也需要判断四个多选框是否全都选中
			
			
			
		};
		
		/*
		 * 提交按钮：
		 * 	- 点击按钮以后，将所有选中的多选框的value属性值弹出
		 */
		//4.#sendBtn
		//为sendBtn绑定单击响应函数
		var sendBtn = document.getElementById("sendBtn");
		sendBtn.onclick = function(){
			//遍历items
			for(var i=0 ; i<items.length ; i++){
				//判断多选框是否选中
				if(items[i].checked){
					alert(items[i].value);
				}
			}
		};
		
		
		//5.#checkedAllBox
		/*
		 * 全选/全不选 多选框
		 * 	- 当它选中时，其余的也选中，当它取消时其余的也取消
		 * 
		 * 在事件的响应函数中，响应函数是给谁绑定的this就是谁
		 */
		//为checkedAllBox绑定单击响应函数
		var  checkedAllBox = document.getElementById("checkedAllBox");
		checkedAllBox.onclick = function(){
			
			//alert(this === checkedAllBox);
			
			//设置多选框的选中状态
			for(var i=0; i <items.length ; i++){
				items[i].checked = this.checked;
			}
			
		};
		
		//6.items
		/*
		 * 如果四个多选框全都选中，则checkedAllBox也应该选中
		 * 如果四个多选框没都选中，则checkedAllBox也不应该选中
		 */
		
		//为四个多选框分别绑定点击响应函数
		for(var i=0 ; i<items.length ; i++){
			items[i].onclick = function(){
				
				//将checkedAllBox设置为选中状态
				checkedAllBox.checked = true;
				
				for(var j=0 ; j<items.length ; j++){
					//判断四个多选框是否全选
					//只要有一个没选中则就不是全选
					if(!items[j].checked){
						//一旦进入判断，则证明不是全选状态
						//将checkedAllBox设置为没选中状态
						checkedAllBox.checked = false;
						//一旦进入判断，则已经得出结果，不用再继续执行循环
						break;
					}					
				}
												
			};
		}				
	};
	
</script>
</head>
<body>

	<form method="post" action="">
		你爱好的运动是？<input type="checkbox" id="checkedAllBox" />全选/全不选 
		
		<br />
		<input type="checkbox" name="items" value="足球" />足球
		<input type="checkbox" name="items" value="篮球" />篮球
		<input type="checkbox" name="items" value="羽毛球" />羽毛球
		<input type="checkbox" name="items" value="乒乓球" />乒乓球
		<br />
		<input type="button" id="checkedAllBtn" value="全　选" />
		<input type="button" id="checkedNoBtn" value="全不选" />
		<input type="button" id="checkedRevBtn" value="反　选" />
		<input type="button" id="sendBtn" value="提　交" />
	</form>
</body>
</html>
~~~

## 实例4

~~~javascript
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
	<head>
		<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
		<title>Untitled Document</title>
		<link rel="stylesheet" type="text/css" href="style/css.css" />
		<script type="text/javascript">
			/**
			 * 定义一个函数，专门用来为指定元素绑定单击响应函数
			 * 	参数：
			 * 		idStr 要绑定单击响应函数的对象的id属性值 
			 *   	fun   事件的回调函数，当单击元素时，该函数将会被触发
			 */
			 function myClick(idString,fun){
				var btn = document.getElementById(idStr);
				btn.onclick = fun();
				}
			 
			window.onload = function(){
				//为id为btn01的按钮绑定一个单击响应函数
				var btn01 = document.getElementById("btn01");
				btn01.onclick = function(){
					//查找#bj节点
					var bj = document.getElementById("bj");
					//打印bj
					//innerHTML 通过这个属性可以获取到元素内部的html代码
					alert(bj.innerHTML);
				};
				
				//为id为btn02的按钮绑定一个单击响应函数
				var btn02 = document.getElementById("btn02");
				btn02.onclick = function(){
					//查找所有li节点
					//getElementsByTagName()可以根据标签名来获取一组元素节点对象
					//这个方法会给我们返回一个类数组对象，所有查询到的元素都会封装到对象中
					//即使查询到的元素只有一个，也会封装到数组返回
					var list = document.getElementsByTagName("li");   //加s
					//打印list长度
					alert(list.length);

					//遍历list
					for(var i = 0; i < list.length; i++){
						alert(list[i].innerHTML);
					};
				};
				
				//为id为btn03的按钮绑定一个单击响应函数
				var btn03 = document.getElementById("btn03");
				btn03.onclick = function(){
					//查找name=gender的所有节点
					var inputs = document.getElementsByName("gender");
					//打印inputs长度
					alert(inputs.length);

					//遍历inputs
					for(var i = 0; i < inputs.length; i++){
						/**
						 * innerHTML用于获取元素内部的HTML代码
						 * 	对于字节数标签，这个属性没有意义
						 */
						
						//alert(inputs[i].innerHTML);  //没有意义
						
						/**
						 * 如果需要读取元素节点的属性，
						 * 		直接使用元素.属性名
						 * 			例子：元素.id  元素.name  元素.value
						 * 			注意：class属性不能采用这种方式
						 * 			读取class属性时需要使用元素.className
 						 */
						alert(inputs[i].value);
					};	
				};

				
				//为id为btn04的按钮绑定一个单击响应函数
				var btn04 = document.getElementById('btn04');
				btn04.onclick = function(){
					//获取id为city的元素
					var city = document.gentElementByID("city");
					//查找#city下所有li节点
					var lis = city.getElementsByTagName("li");
					for(var i = 0; i < lis.length; i++){
						alert(lis[i].innerHTML);
					}
				};
				
				//为id为btn05的按钮绑定一个单击响应函数
				var btn05 = document.getElementById('btn05');
				btn05.onclick = function(){
					//获取id为city的元素
					var city = document.gentElementByID("city");
					//返回#city的所有子节点
					/**
					 * childNodes属性会获取包括文本节点在内的所有子类
					 * 根据DOM标签间空白也会当成文本节点
					 * 注意：在IE8及以下的浏览器中，不会将空白文本当前子节点
					 *  所以该属性在IE8中会返回4个子元素，而其他浏览器是9个
					 */
					var cns = city.childNodes;
					alert(cns.length);
					/*for(var i = 0; i < cns.length; i++){
						alert(cns[i]);
					}*/
					/**
					 * children属性可以获取当前元素的所有子元素(不会包括空白文本)
					 * 
					 */
					var cns2 = city.children;
					alert(cns2.children);
				};
				
				//为id为btn06的按钮绑定一个单击响应函数
				var btn06 = document.getElementById("btn06");
				btn06.onclick = function(){
					//获取id为phone的元素
					  var phone = document.getElementById("phone");
					//返回#phone的第一个子节点
					//phone.childNodes[0];
					//firstChild可以获取到当前元素的第一个子节点(包括空白文本节点)
					var fir = phone.firstChild;
					alert(fir.innerHTML);
					//firstElementChild获取当前元素的第一个子元素
					/**
					 * firstElementChild不知处IE8及以下的浏览器
					 * 如果需要兼容他们尽量不要使用
					 */
					fir = phone.firstElementChild;
				}
				
				//为id为btn07的按钮绑定一个单击响应函数
				myClick("btn07" , function(){
					//获取id为bj的节点
					var bj = document.getElementById("bj");
					//返回#bj的父节点
					var pn = bj.parentNode;
					//alert(pn.innerHTML);
					/**
					 * innerText
					 * 		-该属性可以获取到元素内部的文本内容
					 * 		-它和innerHTML类似，不同的是它会自动将html去除
					 */
					alert(pn.innerText);
				});

				//为id为btn08的按钮绑定一个单击响应函数
				myClick("btn08" , function(){
					//获取id为android的元素
					var and = document.getElementById("android");
					//返回#android的前一个兄弟节点(也可能获取到空白的文本)
					var ps = and.previousSibling;

					//previousElementSibling获取前一个兄弟元素，不包括空白的文本，IE8即以下不支持
					var pe = and.previousElementSibling;
					alert(ps.innerHTML);
				});
				
				//读取#username的value属性值
				myClick("btn09" , function(){
					//获取id为username的元素
					var um = documnet.getElementById("username");
					//读取um的value属性值
					//文本框的value属性值就是文本框中填写的内容
					alert(um.value);
				});

				
				//设置#username的value属性值
				myClick("btn10" , function(){
					//获取id为username的元素
					var um = documnet.getElementById("username");
					um.value = "今天天气真不错";
				});
				
				
				//返回#bj的文本值
				myClick("btn11" , function(){
					//获取id为bj的元素
					var bj = document.getElementById("bj");
					alert(bj.innerHTML);

					//获取bj中的文本节点
					/*var fc = bj.firstChild;
					alert(fc.nodeValue);*/
					alert(bj.firstChild.nodeValue);
				});
			};
						
		</script>
	</head>
	<body>
		<div id="total">
			<div class="inner">
				<p>
					你喜欢哪个城市?
				</p>

				<ul id="city">
					<li id="bj">北京</li>
					<li>上海</li>
					<li>东京</li>
					<li>首尔</li>
				</ul>

				<br>
				<br>

				<p>
					你喜欢哪款单机游戏?
				</p>

				<ul id="game">
					<li id="rl">红警</li>
					<li>实况</li>
					<li>极品飞车</li>
					<li>魔兽</li>
				</ul>

				<br />
				<br />

				<p>
					你手机的操作系统是?
				</p>

				<ul id="phone">
					<li>IOS</li>
					<li id="android">Android</li>
					<li>Windows Phone</li>
				</ul>
			</div>

			<div class="inner">
				gender:
				<input type="radio" name="gender" value="male"/>
				Male
				<input type="radio" name="gender" value="female"/>
				Female
				<br>
				<br>
				name:
				<input type="text" name="name" id="username" value="abcde"/>
			</div>
		</div>
		<div id="btnList">
			<div><button id="btn01">查找#bj节点</button></div>
			<div><button id="btn02">查找所有li节点</button></div>
			<div><button id="btn03">查找name=gender的所有节点</button></div>
			<div><button id="btn04">查找#city下所有li节点</button></div>
			<div><button id="btn05">返回#city的所有子节点</button></div>
			<div><button id="btn06">返回#phone的第一个子节点</button></div>
			<div><button id="btn07">返回#bj的父节点</button></div>
			<div><button id="btn08">返回#android的前一个兄弟节点</button></div>
			<div><button id="btn09">返回#username的value属性值</button></div>
			<div><button id="btn10">设置#username的value属性值</button></div>
			<div><button id="btn11">返回#bj的文本值</button></div>
		</div>
	</body>
</html>

~~~

## 实例5

~~~javascript

<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<title>添加删除记录练习</title>
<link rel="stylesheet" type="text/css" href="ex_2_style/css.css" />
<script type="text/javascript">
	/**
	 * 删除tr的单击响应函数
	 *
	 */
	function delA(){
				
				//点击超链接以后需要删除超链接所在的那行
				//这里我们点击那个超链接this就是谁
				//获取当前tr
				var tr = this.parentNode.parentNode;
				
				//获取要删除的员工的名字
				//var name = tr.getElementsByTagName("td")[0].innerHTML;
				var name = tr.children[0].innerHTML;
				
				//删除之前弹出一个提示框
				/*
				 * confirm()用于弹出一个带有确认和取消按钮的提示框
				 * 	需要一个字符串作为参数，该字符串将会作为提示文字显示出来
				 * 如果用户点击确认则会返回true，如果点击取消则返回false
				 */
				var flag = confirm("确认删除"+name+"吗?");
				
				//如果用户点击确认
				if(flag){
					//删除tr
					tr.parentNode.removeChild(tr);
				}
				
				/*
				 * 点击超链接以后，超链接会跳转页面，这个是超链接的默认行为，
				 * 	但是此时我们不希望出现默认行为，可以通过在响应函数的最后return false来取消默认行为
				 */
				return false;
			};
	window.onload = function(){
		
		/*
		 * 点击超链接以后，删除一个员工的信息
		 */
		
		//获取所有额超链接
		var allA = document.getElementsByTagName("a");
		
		//为每个超链接都绑定一个单击响应函数
		for(var i=0 ; i < allA.length ; i++){
			allA[i].onclick = delA;   //不加括号
		}
		
		/**
		 * 添加员工的功能
		 * 	-点击按钮以后，将员工的信息添加到表格中
		 */
		//为提交按钮添加一个单击响应函数
		var addEmpButton = document.getElementById('addEmpButton');
		addEmpButton.onclick = function(){
			//获取用户添加的员工信息
			//获取员工的名字
			var name = document.getElementById('empName').value;
			//获取员工的email和salary
			var email = document.getElementById('email').value;
			var salary = document.getElementById('salary').value;

			/**
			 * <tr>
				<td>Tom</td>
				<td>tom@tom.com</td>
				<td>5000</td>
				<td><a href="javascript:;">Delete</a></td>
				</tr>
				需要将获取到的信息保存到tr中
			 */
			//创建一个tr
			var tr = document.createElement("tr");

			//创建四个td
			var nameTd = document.createElement("td");
			var emailTd = document.createElement("td");
			var salaryTd = document.createElement("td");
			var aTd = document.createElement("td");

			//创建a元素
			var a = document.createElement("a");

			//创建文本节点
			var nameText = document.createTextNode(name);
			var emailText = document.createTextNode(email);
			var salaryText = document.createTextNode(salary);
			var delText = document.createTextNode("Delete");

			//将文本添加到td中
			nameTd.appendChild(nameText);
			emailTd.appendChild(emailText);
			salaryTd.appendChild(salaryText);
			
			//向a中添加文本
			a.appendChild(delText);

			//将a添加到td中
			aTd.appendChild(a);

			//将td添加到tr中
			tr.appendChild(nameTd);
			tr.appendChild(emailTd);
			tr.appendChild(salaryTd);
			tr.appendChild(aTd);

			//向a中获取href属性
			a.href = "javascript:;"

			//为新添加的a再绑定一次单击响应函数
			a.onclick = delA;

			//获取table
			var employeeTable = document.getElementById("employeeTable");

			//获取employeeTable中的tbody
			var tbody = employeeTable.getElementsByTagName("tbody")[0];

			//将tr添加到tbody中
			tbody.appendChild(tr);
		};
	};

	
</script>
</head>
<body>

	<table id="employeeTable">
		<tr>
			<th>Name</th>
			<th>Email</th>
			<th>Salary</th>
			<th>&nbsp;</th>
		</tr>

		<tr>
			<td>Tom</td>
			<td>tom@tom.com</td>
			<td>5000</td>
			<td><a href="javascript:;">Delete</a></td>
		</tr>

		<tr>
			<td>Jerry</td>
			<td>jerry@sohu.com</td>
			<td>8000</td>
			<td><a href="deleteEmp?id=002">Delete</a></td>
		</tr>

		<tr>
			<td>Bob</td>
			<td>bob@tom.com</td>
			<td>10000</td>
			<td><a href="deleteEmp?id=003">Delete</a></td>
		</tr>
	</table>

	<div id="formDiv">
		<h4>添加新员工</h4>
		<table>
			<tr>
				<td class="word">name: </td>
				<td class="inp">
					<input type="text" name="empName" id="empName" />
				</td>
			</tr>

			<tr>
				<td class="word">email: </td>
				<td class="inp">
					<input type="text" name="email" id="email" />
				</td>
			</tr>

			<tr>
				<td class="word">salary: </td>
				<td class="inp">
					<input type="text" name="salary" id="salary" />
				</td>
			</tr>

			<tr>
				<td colspan="2" align="center">
					<button id="addEmpButton">
						Submit
					</button>
				</td>
			</tr>

		</table>
	</div>
</body>
</html>
~~~

**style.css**

~~~css
@CHARSET "UTF-8";
#total {
	width: 450px;
	margin-left: auto;
	margin-right: auto;
}

ul {
	list-style-type: none;
}

li {
	border-style: solid;
	border-width: 1px;
	padding: 5px;
	margin: 5px;
	background-color: #99ff99;
	float: left;
}

.inner {
	width: 400px;
	border-style: solid;
	border-width: 1px;
	margin: 10px;
	padding: 10px;
	float: left;
}

#employeeTable {
	border-spacing: 1px;
	background-color: black;
	margin: 80px auto 10px auto;
}

th,td {
	background-color: white;
}

#formDiv {
	width: 250px;
	border-style: solid;
	border-width: 1px;
	margin: 50px auto 10px auto;
	padding: 10px;
}

#formDiv input {
	width: 100%;
}

.word {
	width: 40px;
}

.inp {
	width: 200px;
}
~~~

##  实例6

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#info{
			width: 300px;
			height: 500px;
			background-color: #bfa;
			overflow: auto;
		}
	</style>

	<script>
		window.onload = function(){
			/**
			 * 当垂直滚动条滚动到底时使表单项可用
			 * onscroll
			 * 	-该事件会在元素的滚动条滚动时触发
			 */
			
			//获取id为info的p元素
			var info = document.getElementById('info');
			//获取两个表单项
			var inputs = document.getElementsByTagName("input"); 
			//为info绑定一个滚动的事件
			info.onscroll = function(){
				//检查垂直滚动条是否滚动到底
				if(info.scrollHeight - info.scrollTop == info.clientHeight){
					//滚动条滚动到底则使表单项可用
					/**
					 * disabled属性可以设置一个元素是否禁用
					 * 如果设置为true,则元素禁用；否则元素可用
					 */
					inputs[0].disabled = false;
					inputs[1].disabled = false;
				}
			};
		};
	</script>
</head>
<body>
	<h3>欢迎亲爱的用户注册</h3>
	<p id="info">
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
		亲爱的用户，请仔细阅读以下协议，如果你不仔细阅读，你就别注册
	</p>
	<!-- 如果为表单项添加disabled="disabled" 则表单项将变成不可用的状态 -->
	<input type="checkbox" disabled="disabled">我已仔细阅读协议，一定遵守
	<input type="submit" value="注册" disabled="disabled">
</body>
</html>
~~~

# 事件

![](JavaScript知识点查漏补缺/106.png)

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>

	<button id="btn">点我一下</button>
	<!-- 
		我们可以在事件对应的属性中设置一些js代码
			这样当我们事件被触发时这些代码将会被执行

		这种写法我们叫做结构和行为耦合，不方便维护，不推荐使用
	 -->
	<!-- <button id="btn01" onclick="alert('你点我干嘛~~');">我是一个按钮</button>
	<button id="btn02" ondblclick="alert('老铁双击666~~');">我是另一个按钮</button>
	<button id="btn03" onmousemove="alert('鼠标移动');">我是第三个按钮</button> -->
	<script>
		/**
		 * 事件，就是用户和浏览器之间的交互行为
		 * 		比如：点击按钮、鼠标移动、关闭窗口......
		 */
		
		// 获取按钮对象 				
		var btn = document.getElementById("btn"); 

		/**
		 * 可以为按钮的对应事件绑定处理函数的形式来响应事件
		 * 	这样当事件被触发时，其对应的函数将会被调用
		 */
		
		//绑定一个单击事件
		//像这种为单击事件绑定的函数，我们称为单击响应函数
		//属性等于一个函数
		btn.onclick = function(){
			alert("你点我干嘛");
		};
	</script>
</body>
</html>
~~~

## 获取元素节点

![](JavaScript知识点查漏补缺/107.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		window.onload = function(){
			//获取body标签
			//var body = document.getElementsByTagName("body");
			//console.log(body);    //HTMLCollection(1)
			
			//var body = document.getElementsByTagName("body")[0];
			//console.log(body);    //<body>  </body>
			

			/**
			 * 在document中有一个属性就叫body,它保存的是body的引用
			 */
			var body = document.body;
			console.log(body);		//<body>  </body>

			/**
			 * document.documentElement保存的是html根标签
			 * 
			 */
			var html = document.documentElement;
			console.log(html);	

			/**
			 * document.all代表页面中所有的元素
			 * 
			 */
			var all = document.all;
			for(var i = 0; i < all.length; i++){
				console.log(all[i]);
			}
			//console.log(all);	 //HTMLAllCollection(6)
			
			all = document.getElementsByTagName("*");
			console.log(all);    //也行

			/**
			 * 	根据元素的class属性值查询一组元素节点对象
			 * 	getElementByClassName()可以根据class属性值获取一组元素节点对象
			 * 	但是该方法不支持IE8及以下浏览器
			 */
			 var box1 = document.getElementsByClassName('box1');
			 console.log(box1.length);

			 //获取页面中所有的div
			 var divs = document.getElementsByTagName('div');

			 //获取class为box1中的所有的div
			 //.box1 div
			 
			 /**
			  *  document.querySelector()
         	  *	   -需要一个选择器的字符串作为参数，可以根据一个CSS选择器来查询一个元素节点对象
         	  *	   -虽然IE8中没有getElementsByClassName()但是可以使用querySelector()代替
         	  *	   -使用该方法总会返回唯一的一个元素，如果满足条件的元素有多个，它只会返回第一个
			  *  	
			  */
			 var div3 = document.querySelector(".box1 div");
			 console.log(div3.innerHTML);  //我是box1中的div

			 var box4 = document.querySelector(".box1");
			 console.log(box1);   //HTMLCollection [div.box1]

			 /**
			  * document.querySelectorAll()
			  *		  -该方法和document.querySelector()用法类似，不同的是它会将符合条件的元素封装
			  *	到数组中返回
			  *	-即使符合条件的元素只有一个，它也会返回数组
			  */
			 var box5 = document.querySelectorAll(".box1");
			 console.log(box5);  //NodeList(1)
		};
	</script>
</head>
<body>
	<div class="box1">
		<div>我是box1中的div</div>
	</div>

	<div></div>
</body>
</html>
~~~

## 获取元素节点的子节点

![](JavaScript知识点查漏补缺/108.png)

~~~javascript

<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<title>Insert title here</title>
<style type="text/css">

	#areaDiv {
		border: 1px solid black;
		width: 300px;
		height: 50px;
		margin-bottom: 10px;
	}
	
	#showMsg {
		border: 1px solid black;
		width: 300px;
		height: 30px;
	}

</style>
<script type="text/javascript">

	window.onload = function(){
		/*
		 * 当鼠标在areaDiv中移动时，在showMsg中来显示鼠标的坐标
		 */
		//获取两个div
		var areaDiv = document.getElementById("areaDiv");
		var showMsg = document.getElementById("showMsg");
		
		/*
		 * onmousemove
		 * 	- 该事件将会在鼠标在元素中移动时被触发
		 * 
		 * 事件对象
		 * 	- 当事件的响应函数被触发时，浏览器每次都会将一个事件对象作为实参传递进响应函数,
		 * 	  在事件对象中封装了当前事件相关的一切信息，比如：鼠标的坐标  键盘哪个按键被按下  
		 	  鼠标滚轮滚动的方向。。。
		 */
		 areaDiv.onmousemove = function(event){
			/**
			 * 在IE8中，响应函数被触发时，浏览器不会传递事件对象
			 * 	在IE8及以下的浏览器中，是将事件对象作为window对象的属性保存的
			 */
			
			/*if(!event){
				event = window.event;
			}*/

			//解决事件对象的兼容性问题
			event = event || window.event;  //比上面的if更简单一点
			/**
			 * clientX可以获取鼠标指针的水平坐标
			 * clientY可以获取鼠标指针的垂直坐标
			 */
			var x = window.event.clientX;
			var y = window.event.clientY;
			//alert("x=" + x + ",y=" + y);

			//在showMsg中显示鼠标的坐标
			showMsg.innerHTML = "x=" + x + ",y=" + y;
		};
	};
</script>
</head>
<body>
	<div id="areaDiv"></div>
	<div id="showMsg"></div>
</body>
</html>
~~~

## 获取父节点和兄弟节点

![](JavaScript知识点查漏补缺/109.png)

## 元素节点的属性

![](JavaScript知识点查漏补缺/110.png)

## 其他属性

![](JavaScript知识点查漏补缺/111.png)

## 使用CSS选择器进行查询

![](JavaScript知识点查漏补缺/112.png)

## 节点的修改

![](JavaScript知识点查漏补缺/113.png)

~~~javascript
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
	<head>
		<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
		<title>Untitled Document</title>
		<link rel="stylesheet" type="text/css" href="style/css.css" />
		<script type="text/javascript">
		
			window.onload = function() {
				
				//创建一个"广州"节点,添加到#city下
					myClick("btn01" , function(){
						//创建广州节点 <li>广州</li>
						//1.创建li元素节点
						
					 /*
					  * document.createElement()
					  * 	可以用于创建一个元素节点对象，
					  * 	它需要一个标签名作为参数，将会根据该标签名创建元素节点对象，
					  * 	并将创建好的对象作为返回值返回
					  */
						var li = document.createElement("li");

					//创建广州文本节点
					/*
					 * document.createTextNode()
					 * 	可以用来创建一个文本节点对象
					 *  需要一个文本内容作为参数，将会根据该内容创建文本节点，并将新的节点返回
					 */
					 var gzText = document.createTextNode("广州");
						//将gzText设置li的子节点
						/*
					     * appendChild()
					     * 	 - 向一个父节点中添加一个新的子节点
					     * 	 - 用法：父节点.appendChild(子节点);
					     */
					    li.appendChild(gzText);

					    //获取id为city的节点
					    var city = document.getElementById("city");

					    //将广州添加到city下
					    city.appendChild(li);
					});
																		
				
				//将"广州"节点插入到#bj前面
					myClick("btn02" , function(){
						//创建一个广州
						var li = document.createElement("li");
						var gzText = document.createTextNode("广州");
						li.appendChild(gzText);

						//获取id为bj的节点
						var bj = document.getElementById("bj");

						//获取city
						var city = document.getElementById('city');
						city.insertBefore(li , bj);
						/*
					 	* insertBefore()
					 	* 	- 可以在指定的子节点前插入新的子节点
					 	*  - 语法：
					 	* 		父节点.insertBefore(新节点,旧节点);
					 	*/
					});
					

				//使用"广州"节点替换#bj节点
				myClick("btn03",function(){
					//创建一个广州
					var li = document.createElement("li");
					var gzText = document.createTextNode("广州");
					li.appendChild(gzText);
					
					//获取id为bj的节点
					var bj = document.getElementById("bj");
					
					//获取city
					var city = document.getElementById("city");
					
					/*
					 * replaceChild()
					 * 	- 可以使用指定的子节点替换已有的子节点
					 * 	- 语法：父节点.replaceChild(新节点,旧节点);
					 */
					city.replaceChild(li , bj);
					
					
				});
				
				//删除#bj节点
				myClick("btn04",function(){
					//获取id为bj的节点
					var bj = document.getElementById("bj");
					//获取city
					var city = document.getElementById("city");
					
					/*
					 * removeChild()
					 * 	- 可以删除一个子节点
					 * 	- 语法：父节点.removeChild(子节点);
					 * 		
					 * 		子节点.parentNode.removeChild(子节点);
					 * 		这种方式更方便，不用再获取它的父节点了
					 */
					//city.removeChild(bj);
					
					bj.parentNode.removeChild(bj);
				});
				
				
				//读取#city内的HTML代码
				myClick("btn05",function(){
					//获取city
					var city = document.getElementById("city");
					
					alert(city.innerHTML);
				});
				
				//设置#bj内的HTML代码
				myClick("btn06" , function(){
					//获取bj
					var bj = document.getElementById("bj");
					bj.innerHTML = "昌平";
				});
				
				myClick("btn07",function(){
					
					//向city中添加广州
					var city = document.getElementById("city");
					
					/*
					 * 使用innerHTML也可以完成DOM的增删改的相关操作
					 * 一般我们会两种方式结合使用
					 */
					//city.innerHTML += "<li>广州</li>";
					
					//创建一个li
					var li = document.createElement("li");
					//向li中设置文本
					li.innerHTML = "广州";
					//将li添加到city中
					city.appendChild(li);
					
				});
				
				
			};
			
			function myClick(idStr, fun) {
				var btn = document.getElementById(idStr);
				btn.onclick = fun;
			}
			
		
		</script>
		
	</head>
	<body>
		<div id="total">
			<div class="inner">
				<p>
					你喜欢哪个城市?
				</p>

				<ul id="city">
					<li id="bj">北京</li>
					<li>上海</li>
					<li>东京</li>
					<li>首尔</li>
				</ul>
				
			</div>
		</div>
		<div id="btnList">
			<div><button id="btn01">创建一个"广州"节点,添加到#city下</button></div>
			<div><button id="btn02">将"广州"节点插入到#bj前面</button></div>
			<div><button id="btn03">使用"广州"节点替换#bj节点</button></div>
			<div><button id="btn04">删除#bj节点</button></div>
			<div><button id="btn05">读取#city内的HTML代码</button></div>
			<div><button id="btn06">设置#bj内的HTML代码</button></div>
			<div><button id="btn07">创建一个"广州"节点,添加到#city下</button></div>
		</div>
	</body>
</html>
~~~

## div跟鼠标移动

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#box1{
			width: 100px;
			height: 100px;
			background-color: blue;
			/**	
			 * 开启box1的绝对定位
			 */
			position:absolute;
		}
	</style>

	<script>
		window.onload = function(){
			/**
			 * 使div可以跟随鼠标移动
			 */
			
			//获取box1
			var box1 = document.getElementById("box1");
			//绑定鼠标移动事件
			document.onmousemove = function(event){
				//解决兼容的问题
				event = event || window.event;
				//获取滚动条滚动的距离
				/**
				 * chrome认为浏览器的滚动条是body的，可以通过body.scrollTop来获取
				 * 火狐等浏览器认为浏览器的滚动条是html的
				 */
				var st = document.body.scrollTop ||  document.documentElement.scrollTop;
				var sl = document.body.scrollLeft || document.documentElement.scrollLeft;
				//var st = document.documentElement.scrollTop;
				console.log(st);

				//获取到鼠标的坐标
				/**
				 * clientX和clientY
				 * 		用于获取鼠标在当前的可见窗口的坐标
				 * 		div的偏移量
				 *
				 * pageX和pageY可以获取鼠标相对于当前页面的坐标
				 * 	但是这两个属性在IE8中不支持，所以如果需要兼容IE8,则不要使用
				 */
				
				//var left = event.pageX;
				//var top = event.pageY;

				var left = event.clientX;
				var top = event.clientY;

				//设置div的偏移量
				box1.style.left = left + sl + "px";
				box1.style.top = top + st + "px";	 
			};
		};
	</script>
</head>
<body style="height: 1000px ;width: 5000px;">
	<div id="box1"></div>
</body>
</html>
~~~

## 事件冒泡

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#box1{
			width: 200px;
			height: 200px;
			background-color: yellowgreen;
		}

		#s1{
			background-color: yellow;
		}
	</style>

	<script>
		window.onload = function(){
			/**
			 * 事件的冒泡
			 * 	-所谓事件的冒泡指的就是事件的向上传导，当后代元素的事件被触发时，其祖先元素的相同
			 * 	事件也会被触发
			 * -在开发中大多数情况下冒泡是有用的，如果不希望发生事件冒泡可以通过事件对象来取消冒泡
			 * 
			 * 
			 */
			//为s1绑定一个单击响应函数
			var s1 = document.getElementById("s1");
			s1.onclick = function(event){
				event = event || window.event;
				alert("我是span的单击响应函数");

				//取消冒泡
				//可以将事件对象的cancelBubble设置为true,即可取消冒泡
				event.cancelBubble = true;
			};

			//为box1绑定一个单击响应函数
			var box1 = document.getElementById("box1");
			box1.onclick = function(event){
				alert("我是div的单击响应函数");
				event.cancelBubble = true;
			};

			//为body来绑定一个单击响应函数
			document.body.onclick =function(event){
				alert("我是body的单击响应函数");
				event.cancelBubble = true;
			};
		};
	</script>
</head>
<body>
	<div id="box1">
		我是box1
		<span id="s1">我是span</span>
	</div>
</body>
</html>
~~~

## 事件

![](JavaScript知识点查漏补缺/114.png)

## 事件处理程序

![](JavaScript知识点查漏补缺/115.png)

## 通过HTML标签的属性设置

![](JavaScript知识点查漏补缺/116.png)

## 通过DOM对象的属性绑定

![](JavaScript知识点查漏补缺/117.png)

## 设置事件监听器

![](JavaScript知识点查漏补缺/118.png)

## 事件处理中的this

![](JavaScript知识点查漏补缺/119.png)

## 事件对象

![](JavaScript知识点查漏补缺/120.png)

![](JavaScript知识点查漏补缺/121.png)

## Event对象的通用属性/方法

![](JavaScript知识点查漏补缺/122.png)

## IE中的事件对象

![](JavaScript知识点查漏补缺/123.png)

## Event对象的通用属性/方法（IE）

![](JavaScript知识点查漏补缺/124.png)

## 事件的触发

![](JavaScript知识点查漏补缺/125.png)

## 事件的传播

![](JavaScript知识点查漏补缺/126.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		window.onload = function(){
			//点击按钮以后，添加超链接
			var btn01 = document.getElementById("btn01");
			btn01.onclick = function(){
				//创建一个li
				var li = document.createElement("li");
				li.innerHTML = "<a href='javascript:;' class='link'>新建的超链接</a>";

				//将li添加到ul中
				ul.appendChild(li);  
			};
			/**
			 * 为每一个超链接都绑定一个单击响应函数
			 * 这里我们为每一个超链接都绑定了一个单击响应函数，这种操作比较麻烦
			 * 	而且这些操作只能为已有的超链接设置事件，而新添加的超链接必须重新绑定
			 */
			//获取所有的a
			var allA = document.getElementsByTagName("a");
			//遍历
			/*for(var i = 0; i < allA.length; i++){
				allA[i].onclick = function(){
					alert("我是a的单击响应函数");
				}
			}*/

			/**
			 * 我们希望，只绑定一次事件，即可应用到多个的元素上，即使元素是后添加的
			 * 我们可以尝试将其绑定给元素的共同的祖先元素
			 *
			 * 事件的委派
			 * 	-指将事件统一绑定给元素的共同的祖先元素，这样当后代元素上的事件触发时，会
			 * 	 一直冒泡到祖先元素，从而通过祖先元素的响应函数来处理事件
			 *
			 *  -事件委派是利用了冒泡，通过委派可以减少事件绑定的次数，提高程序的性能
			 */
			
			//为ul绑定一个单击响应函数
			ul.onclick = function(event){
				event = event || window.event;
				/**
				 * target
				 * 	-event中的target表示的触发事件的对象
				 */
				//alert(event.target);
				

				//alert(this);
				//如果触发事件的对象是期望的元素，则执行。否则不执行 
				if(event.target.className == "link"){
					alert("我是ul的单击响应函数");
				}
				
			};
		};
	</script>
</head>

<body>
	<button id="btn01">添加超链接</button>
	<ul id="ul" style="background-color: #bfa;">
		<li><a href="javascript:;" class="link">超链接1</a></li>
		<li><a href="javascript:;" class="link">超链接2</a></li>
		<li><a href="javascript:;" class="link">超链接3</a></li>
	</ul>
</body>
</html>
~~~

## 事件的传播流程

![](JavaScript知识点查漏补缺/127.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		window.onload = function(){
			/**
			 * 点击按钮以后随便弹出一个内容
			 */
			
			//获取按钮对象
			var btn01 = document.getElementById("btn01");

			/**
			 * 使用对象.事件 = 函数的形式绑定响应函数，
			 * 	它只能为一个元素的一个事件绑定一个响应函数
			 * 	不能绑定多个，如果绑定了多个，则后边会覆盖掉前面的
			 */
			//为btn01绑定一个单击响应函数
			/*btn01.onclick = function(){
				alert(1);
			};
*/
			//为btn01绑定第二个响应函数
			/*btn01.onclick = function(){
				alert(2);
			}; */

			/**增加事件监听器
			 * addEventListener()
			 * 	-通过这个方法也可以为元素绑定响应函数
			 * 	-参数：
			 * 		1.事件的字符串，不要on
			 * 		2.回调函数，当事件触发时，该函数会被调用
			 * 		3.是否在捕获阶段触发事件，需要一个布尔值，一般都传false
			 *
			 * 使用addEventListener()可以同时为一个元素的相同事件同时绑定多个响应函数
			 * 	这样当事件被触发时，响应函数将会按照函数的绑定顺序执行
			 *
			 * 这个方法不支持IE8及以下的浏览器
			 */
			/*btn01.addEventListener("click",function(){
				alert(1);
			},false);

			btn01.addEventListener("click",function(){
				alert(2);
			},false);

			btn01.addEventListener("click",function(){
				alert(3);
			},false);*/

			/**
			 * attachEvent()
			 * 	-在IE8中可以使用attachEvent()来绑定事件
			 * 	-参数：
			 * 		1.事件的字符串，要on
			 * 		2.回调函数
			 *
			 * -这个方法也可以同时为一个事件绑定多个处理函数
			 * 		不同的是它是后绑定先执行，执行顺序和addEventListener()相反
			 */
			/*btn01.attachEvent("onclick" , function(){
				alert(1);
			});

			btn01.attachEvent("onclick" , function(){
				alert(2);
			});

			btn01.attachEvent("onclick" , function(){
				alert(3);
			});*/
			bind(btn01 , "click" , function(){
				alert(1);
				alert(this);
			});

			bind(btn01 , "click" , function(){
				alert(2);
			});
		};

		//定义一个函数，用来为指定元素绑定响应函数
		/**
		 * addEventListener()中的this,是绑定事件的对象
		 * attachEvent()中的this,是window
		 * 需要两个统一方法this 	
		 */
		/**
		 * 参数：
		 * 	-obj 要绑定事件的对象
		 *  -eventStr 事件的字符串(不要on)
		 *  -callback 回调函数
		 */
		function bind(obj,eventStr,callback){
			if(obj.addEventListener){
				//大部分浏览器兼容的方式
				obj.addEventListener(eventStr , callback ,false);
			}else{
				/**
				 * this是谁由调用方式决定
				 * callback.call(obj)   call方法可以修改函数的this 
				 */
				//IE8及以下
				obj.attachEvent("on" + eventStr , function(){
					//在匿名函数中调用回调函数
					callback.call(obj);
				});
			}
						
		}
	</script>
</head>
<body>
	<button id="btn01">点我一下</button>
</body>
</html>
~~~

## 事件的传播

![](JavaScript知识点查漏补缺/128.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#box1{
			width: 300px;
			height: 300px;
			background-color: yellowgreen;
		}

		#box2{
			width: 200px;
			height: 200px;
			background-color: yellow;
		}

		#box3{
			width: 150px;
			height: 150px;
			background-color: skyblue;
		}
	</style>
	<script>
		window.onload = function(){
			/**
			 * 分别为三个div绑定单击响应函数
			 * 
			 */
			var box1 = document.getElementById("box1");
			var box2 = document.getElementById("box2");
			var box3 = document.getElementById("box3");
			/**
			 * 事件的传播
			 * 	-关于事件的传播 网景公司和微软公司有不同的理解
			 * 	-微软公司认为事件应该是由内向外传播的，也就是当事件触发时，应该先触发当前元素
			 * 	上的事件
			 * 		然后再向当前元素的祖先元素上传播。也就是说事件应该在冒泡阶段执行
			 *
			 * -网景公司认为事件应该是由外向内传播的，也就是当事件触发时，应该先触发当前元素的最
			 * 外层祖先元素的事件
			 * 		然后再向内传播给后代元素
			 *
			 * -W3C综合了两个公司的方案，将事件分成了三个阶段
			 * 		1.捕获阶段
			 * 			-在捕获阶段时从最外层的祖先元素向目标元素进行事件的捕获，但是默认此时
			 * 			不会触发事件
			 *
			 *		2.目标阶段
			 *			-事件捕获到目标元素，捕获结束。开始在目标元素上触发事件
			 *
			 * 		3.冒泡阶段
			 * 			-事件从目标元素向它的祖先元素传递，依次触发祖先元素上的事件
			 * 			
			 *    	-如果希望在捕获阶段就触发事件，可以在addEventListener()的第三个参数
			 *    	设置为true
			 *
			 * 		一般情况下我们不会希望在捕获阶段触发事件，所以这个参数一般都是false
			 *
			 * 		-IE8及以下的浏览器没有捕获阶段
			 */

			bind(box1 , "click" , function(){
				alert("我是box1的响应函数");
			});

			bind(box2 , "click" , function(){
				alert("我是box2的响应函数");
			});

			bind(box3 , "click" , function(){
				alert("我是box3的响应函数");
			});
		}

		function bind(obj,eventStr,callback){
			if(obj.addEventListener){
				//大部分浏览器兼容的方式
				obj.addEventListener(eventStr , callback ,false);
			}else{
				/**
				 * this是谁由调用方式决定
				 * callback.call(obj)   call方法可以修改函数的this 
				 */
				//IE8及以下
				obj.attachEvent("on" + eventStr , function(){
					//在匿名函数中调用回调函数
					callback.call(obj);
				});
			}				
		}
	</script>
</head>
<body>
	<div id="box1">
		<div id="box2">
			<div id="box3"></div>
		</div>
	</div>
</body>
</html>
~~~

## 取消事件传播

![](JavaScript知识点查漏补缺/129.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		window.onload = function(){
			/**
			 * 键盘事件
			 * onkeydown
			 * 		-按键被按下
			 * 		-对于onkeydown来说，如果
			 * 		-当onkeydown连续触发时，第一次和第二次之间会间隔的稍微的长一点，
			 * 		其他的会非常的快
			 * 		-这种设计是为了防止误操作的发生
			 * 	onkeyup
			 * 		-按键被松开
			 *
			 * 键盘事件一般都会绑定给一些可以获取到焦点的对象或者是document 
			 */
			
			document.onkeydown =function(event){
				event = event || window.event;
				/**
				 * 可以通过keyCode获取按键的编码
				 * 通过它可以判断哪个按键被按下
				 * 除了keyCode，事件对象中还提供了几个属性
				 * altKey
				 * ctrlKey
				 * shiftKey
				 * 	-这三个用来判断alt,ctrl,shift是否被按下
				 * 		如果按下则返回true,否则返回false
				 */
				
				//判断一个y是否被按下
				//判断y和ctrl是否同时被按下
				if(event.keyCode === 89 && event.ctrlKey){
					console.log('"ctrl和y"都被按下了');
				}
				//console.log(event.keyCode);
			};

			/*document.onkeyup =function(){
				console.log("按键松开了");
			};*/

			//获取input
			var input = document.getElementsByTagName("input")[0];
			input.onkeydown = function(event){
				event = event || window.event;

				//console.log(event.keyCode);
				//数字的keyCode是48-57
				//是文本框中不能输入数字
				if(event.keyCode >= 48 && event.keyCode <=57)
					//在文本框中输入文本内容属于onkeydown的默认行为
					//如果在onkeydown中取消了默认行为，则输入的内容，不会出现在文本框中
					return false;   //取消默认行为

				
			};
		};
	</script>
</head>
<body>
	<input type="text">
</body>
</html>
~~~

## 盒子移动

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#box1{
			width: 100px;
			height: 100px;
			background-color: red;
			position:absolute;
		}
	</style>
	<script>
		//使div可以根据不同的方向键向不同的方向移动
		/**
		 * 按左键，div向左移...
		 */
		window.onload = function(){
			//为document绑定一个按键按下的事件
			document.onkeydown = function(event){
				event = event || window.event;

				//定义一个变量，来表示移动的速度
				var speed = 10;

				//当用户按了ctrl以后，速度加快
				if(event.ctrlKey){
					speed = 500;
				}
				/**
				 * 37 左
				 * 38 上
				 * 39 右 
				 * 40 下
				 */
				switch(event.keyCode){
					case 37:
					//alert("向左");  left值减小
					box1.style.left = box1.offsetLeft - speed + "px";
					break;

					case 39:
					box1.style.left = box1.offsetLeft + speed + "px";
					//alert("向右");
					break;

					case 38:
					box1.style.top = box1.offsetTop - speed + "px";
					//alert("向上");
					break;

					case 40:
					box1.style.top = box1.offsetTop + speed + "px";
					//alert("向下");
					break;
				};
				//console.log(event.keyCode);
			};
		};
	</script>
</head>
<body>
	<div id="box1"></div>
</body>
</html>
~~~

# BOM

![](JavaScript知识点查漏补缺/130.png)

## window对象

![](JavaScript知识点查漏补缺/131.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * BOM
		 * 	-浏览器对象模型
		 * 	-BOM可以使我们通过JS来操作浏览器
		 * 	-在BOM中为我们提供了一组对象，用来完成对浏览器的操作
		 * 	-BOM对象
		 * 		Window
		 * 			-window代表的是整个浏览器的窗口，同时window也是网页中的全局对象
		 * 		Navigator
		 * 			-代表的当前浏览器的信息，通过该对象可以用来识别不同的浏览器
		 * 		Location
		 * 			-代表我们当前浏览器的地址栏信息，通过Location可以获取地址栏信息，
		 * 			或者操作浏览器跳转页面
		 * 		History
		 * 			-代表浏览器的历史记录，可以通过该对象来操作浏览器的历史记录
		 * 				由于隐私的原因，该对象不能获取到具体的历史记录，只能操作
		 * 				浏览器向前或向后翻页。而且该操作只在当次访问时有效
		 * 				
		 * 		Screen-用的不多（不说了）
		 * 			-代表用户的屏幕的信息，通过该对象可以获取到用户的显示器的相关信息
		 *
		 * 		这些BOM对象在浏览器中都是作为window对象的属性保存的，
		 * 			可以通过window对象来使用，也可以直接使用
		 */
		//console.log(window.navigator);  //直接写nagigator也行
		//console.log(location);
		//console.log(history);
		
		/**
		 * Navigator
		 * 	-代表的当前浏览器的信息，通过该对象可以用来识别不同的浏览器
		 * 	-由于历史原因，Navigator对象中的大部分属性都已经不能帮助我们识别浏览器了
		 * 	-一般我们只会使用userAgent来判断浏览器的信息
		 * 		userAgent是一个字符串，这个字符串中包含有用来描述浏览器信息的内容
		 * 		不同的浏览器有不同的userAgent
		 *
		 * 谷歌的userAgent
		 * Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, 
		 * like Gecko) Chrome/77.0.3865.120 Safari/537.36
		 */
		//console.log(navigator.appName);
		var ua = navigator.userAgent;
		console.log(ua);
		if(/firefox/i.test(ua)){
			alert("你是火狐浏览器");
		}else if(/chrome/i.test(ua)){
			alert("你是Chrome");
		}else if(/msie/i.test(ua)){
			alert("你是IE浏览器");
		}
		 else if("ActiveXObject" in window){
		 	alert("你是IE11,我要枪毙了你");
		 }
		
		/**
		 * 如果通过userAgent不能判断，还可以通过一些浏览器中特有的对象来判断浏览器的信息
		 * 比如：ActiveXObject(IE独有的东西，是一个构造函数)
		 * 但是微软把这个给屏蔽了
		 */
		/*if(window.ActiveXObject){
			alert("你是IE,我已经抓住你了");
		}else{
			alert("你不是IE");
		};*/
		
	</script>
</head>
<body>
	
</body>
</html>
~~~

## 窗口大小

![](JavaScript知识点查漏补缺/132.png)

## 打开窗口

![](JavaScript知识点查漏补缺/133.png)

## 拖拽1

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#box1{
			width: 100px;
			height: 100px;
			background-color: red;
			position:absolute;
		}

		#box2{
			width: 100px;
			height: 100px;
			background-color: yellow;
			position:absolute;
			left: 200px;
			top: 200px;
		}
	</style>
	<script>
		window.onload = function(){
			/**
			 * 拖拽box1元素
			 * 	-拖拽的流程
			 * 		1.当鼠标在被拖拽的元素上按下时，开始拖拽  onmousedown
			 * 		2.当鼠标移动时，被拖拽元素跟随鼠标移动	   onmousemove
			 * 		3.当鼠标松开时，被拖拽元素固定在当前位置   onmouseup
			 */
			
			//获取box1
			var box1 = document.getElementById("box1");
			//为box1绑定一个鼠标按下事件	
			//当鼠标在被拖拽的元素上按下时，开始拖拽  onmousedown
			box1.onmousedown = function(event){
				event = event || window.event
				//求出div的偏移量  鼠标.clientX - 元素.offsetLeft
				//求出div的偏移量  鼠标.clientY - 元素.offsetTop
				var ol = event.clientX - box1.offsetLeft;
				var ot = event.clientY - box1.offsetTop;
				//为document绑定一个onmousemove事件
				document.onmousemove = function(event){
					event = event || window.event; 
					//当鼠标移动时，被拖拽元素跟随鼠标移动	   onmousemove
					//获取鼠标的坐标
					var left = event.clientX - ol;
					var top  = event.clientY - ot;

					//修改box1的位置
					box1.style.left = left + "px"; 
					box1.style.top =  top + "px"; 
				};

				//为我们元素来绑定一个鼠标松开事件
				document.onmouseup = function(){
					//当鼠标松开时，被拖拽元素固定在当前位置   onmouseup
					
					//取消document的onmousemove事件
					document.onmousemove = null;

					//取消document的onmouseup事件
					document.onmouseup = null;
				};
			};
		}; 
	</script>
</head>
<body>
	<div id="box1"></div>
	<div id="box2"></div>
</body>
</html>
~~~

## 拖拽2

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#box1{
			width: 100px;
			height: 100px;
			background-color: red;
			position:absolute;
		}

		#box2{
			width: 100px;
			height: 100px;
			background-color: yellow;
			position:absolute;
			left: 200px;
			top: 200px;
		}
	</style>
	<script>
		window.onload = function(){
			/**
			 * 拖拽box1元素
			 * 	-拖拽的流程
			 * 		1.当鼠标在被拖拽的元素上按下时，开始拖拽  onmousedown
			 * 		2.当鼠标移动时，被拖拽元素跟随鼠标移动	   onmousemove
			 * 		3.当鼠标松开时，被拖拽元素固定在当前位置   onmouseup
			 */
			
			//获取box1
			var box1 = document.getElementById("box1");
			var box2 = document.getElementById("box2");
			var girl = document.getElementById("girl");

			//开启box1的拖拽
			drag(box1);

			//开启box2的拖拽
			drag(box2);

			drag(girl);
};
			//为obj绑定一个鼠标按下事件	
			
		/**
		 * 提取一个专门用来拖拽的函数
		 * 参数：开启拖拽的元素
		 */
		function drag(obj){
			//当鼠标在被拖拽的元素上按下时，开始拖拽  onmousedown
			obj.onmousedown = function(event){

				//设置obj捕获所有鼠标按下的事件
				/**
				 * setCapture()
				 * 		-只有IE支持，但是在火狐中调用时不会报错
				 * 			而如果使用chrome调用，会报错
				 */
				
				/*if(obj.setCapture){
					obj.setCapture();
				}*/
				
				obj.setCapture && obj.setCapture();

				event = event || window.event
				//求出div的偏移量  鼠标.clientX - 元素.offsetLeft
				//求出div的偏移量  鼠标.clientY - 元素.offsetTop
				var ol = event.clientX - obj.offsetLeft;
				var ot = event.clientY - obj.offsetTop;
				//为document绑定一个onmousemove事件
				document.onmousemove = function(event){
					event = event || window.event; 
					//当鼠标移动时，被拖拽元素跟随鼠标移动	   onmousemove
					//获取鼠标的坐标
					var left = event.clientX - ol;
					var top  = event.clientY - ot;

					//修改obj的位置
					obj.style.left = left + "px"; 
					obj.style.top =  top + "px"; 
				};

				
				//为我们元素来绑定一个鼠标松开事件
				document.onmouseup = function(){
					//当鼠标松开时，被拖拽元素固定在当前位置   onmouseup
					
					//取消document的onmousemove事件
					document.onmousemove = null;

					//取消document的onmouseup事件
					document.onmouseup = null;

					//当鼠标松开时，取消对事件的捕获
					obj.releasedCapture && obj.releasedCapture();
				};
				/**
				 * 当我们去拖拽一个网页中的内容时，浏览器会默认搜索引擎中搜索内容
				 * 此时会导致拖拽功能的异常，这个是浏览器提供的默认行为
				 * 如果不希望发生这个行为，则可以通过return false来取消默认行为
				 *
				 * 但是这招对IE8不起作用
				 */
				return false;
				};
			}; 
	</script>
</head>
<body>
	我是一段文字
	<div id="box1"></div>
	<div id="box2"></div>
	<img src="img/girl.jpg" alt="" id="girl" width="200px" height="200px" style="position:absolute;">
</body>
</html>
~~~

## 鼠标滚轮

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#box1{
			width: 100px;
			height: 100px;
			background-color: red;
		}
	</style>
	<script>
		window.onload = function(){
			/**
			 * 当鼠标滚轮向下滚动时，box1变长
			 * 当鼠标滚论向上滚动时，box1变短
			 */
			
			//获取id为box1的div
			var box1 = document.getElementById("box1");

			//为box1绑定一个鼠标滚轮滚动的事件
			/**
			 * onmousewheel鼠标滚轮滚动事件，会在滚轮滚动时触发
			 * 	但是火狐不支持该属性
			 *
			 * 在火狐中需要使用DOMMouseScroll来绑定滚动事件
			 * 	注意：该事件需要通过addEventListener()函数来绑定
			 */
			
			/*function fun(){
				alert("滚了");
			};*/

			box1.onmousewheel = function(event){
				event = event || window.event;
				//判断鼠标滚轮滚动的方向
				
				//event.wheelDelta 可以获取鼠标滚轮滚动的方向
				//向上滚150 向下滚-150
				//wheelDelta这个值不看大小，只看正负
				//wheelDelta这个属性火狐中不支持
				

				//在火狐中使用event.detail来获取滚动的方向
				//向上滚-3 向上滚3
				//alert(event.detail);
				//alert(event.wheelDelta);
				
				//判断鼠标滚轮滚动的方向
				if(event.wheelDelta > 0 || event.detail < 0){
					//当鼠标滚论向上滚动时，box1变短
					//alert("向上滚");
					box1.style.height = box1.clientHeight  - 10 + "px";
				}else{
					//当鼠标滚论向上滚动时，box1变短
					//alert("向下滚");
					box1.style.height = box1.clientHeight  + 10 + "px";
					
				}
				/**
				 * 当鼠标滚轮向下滚动时，box1变长
				 * 当鼠标滚轮向上滚动时，box1变短
				 */
				
				/**
				 *使用addEventListener()方法绑定响应函数，取消默认行为时不能使用return false
				 *
				 *需要使用event来取消默认行为 event.preventDefault();
				 *但是IE8不支持event.preventDefault();这个玩意，如果直接调用会报错
				 */
				event.preventDefault && event.preventDefault();
				
				/**
				 * 当滚轮滚动时，如果浏览器有滚动条，滚动条会随之滚动，
				 * 这是浏览器的默认行为，如果不希望发生，则可以取消默认行为
				 */
				return false;
			};

			//为火狐绑定滚轮事件
			bind(box1 , "DOMMouseScroll" , box1.onmousewheel);
		};

		function bind(obj,eventStr,callback){
			if(obj.addEventListener){
				//大部分浏览器兼容的方式
				obj.addEventListener(eventStr , callback ,false);
			}else{
				/**
				 * this是谁由调用方式决定
				 * callback.call(obj)   call方法可以修改函数的this 
				 */
				//IE8及以下
				obj.attachEvent("on" + eventStr , function(){
					//在匿名函数中调用回调函数
					callback.call(obj);
				});
			}
						
		}
	</script>
</head>
<body style="height: 2000px">
	<div id="box1"></div>
</body>
</html>
~~~

## 超时调用

![](JavaScript知识点查漏补缺/134.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>

		var num = 1;

		//开启一个定时器
		setInterval(function(){
			console.log(num++);
		},3000);


		/**
		 * 延时调用
		 * 		一个函数不马上执行，而是隔一段时间以后再执行
		 *   	而且只会执行一次
		 * 
		 * 延时调用和定时调用的区别：
		 * 定时调用会执行很多次，而延时调用只会执行一次
		 *
		 * 延时调用和定时调用实际上是可以互相代替的，在开发中可以根据自己的需要进行选择
		 */
		var timer = setTimeout(function(){
			console.log(num++);
		},3000);

		//使用clearTimeout()来关闭一个延时调用
		clearTimeout(timer);
	</script>
</head>
<body>
	
</body>
</html>
~~~

### 实例1

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		*{
			margin: 0;
			padding: 0;
		}

		#box1{
			width: 100px;
			height: 100px;
			background-color: red;
			position: absolute;
			left: 0;
		}
	</style>
	<script>
		window.onload = function(){
			//获取box1
			var box1 = document.getElementById("box1");

			//获取btn01
			var btn01 = document.getElementById("btn01");

			//定义一个变量，用来保存定时器的标识
			var timer;

			//点击按钮以后，使box1向右移动（left值增大）
			btn01.onclick = function(){
				//关闭上一个定时器
				clearInterval(timer);
				//box1.style.left = "200px";
												
				//alert(oldValue);

				//开启一个定时器来执行动画效果
				timer = setInterval(function(){	

					//获取box1原来的left值
					var oldValue = parseInt(getStyle(box1,"left"));

					//在旧值的基础上增加
					var newValue = oldValue + 1;

					//判断newValue是否大于800
					if(newValue > 800){
						newValue = 800;
					}
					//将新值设置给box1
					box1.style.left = newValue + "px";

					//当元素移动到800px时使其停止执行动画
					if(newValue == 800){
						//到达目标，关闭定时器
						clearInterval(timer);
					}
				},30);
			};
		};

		function getStyle(obj , name){
			if(window.getComputedStyle){
			//正常浏览器的方式
			return getComputedStyle(obj,null)[name];				
			}else{
			//IE8的方式
			return obj.currentStyle[name];				
			}
			
		}
	</script>
</head>
<body>
	<button id="btn01">点击按钮以后box1向右移动</button>
	<br><br>
	<div id="box1"></div>	
	<div style="width: 0; height: 1000px; border-left: 1px black solid; position: absolute; left: 800px; top: 0px;"></div>
</body>
</html>
~~~

### 实例2

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		*{
			margin: 0;
			padding: 0;
		}

		#box1{
			width: 100px;
			height: 100px;
			background-color: red;
			position: absolute;
			left: 0;
		}
	</style>
	<script>
		window.onload = function(){
			//获取box1
			var box1 = document.getElementById("box1");

			//获取btn01
			var btn01 = document.getElementById("btn01");

			//获取btn02
			var btn02 = document.getElementById("btn02");

			//点击按钮以后，使box1向右移动（left值增大）
			btn01.onclick = function(){
				move(box1,800,10);
			};

			//点击按钮以后，使box1向左移动（left值减小）
			btn02.onclick = function(){
				move(box1,0,10);
			};
		
};
		//定义一个变量，用来保存定时器的标识
			var timer;

		//尝试创建一个可以简单执行动画的函数
		/**
		 * 参数：
		 * 	obj:要执行动画的对象
		 *  speed:移动的速度（正数向右移动，负数向左移动）
		 */
		function move(obj , target , speed){
			//关闭上一个定时器
				clearInterval(timer);
				//box1.style.left = "200px";
				
				//获取元素目前的位置	
				var current = parseInt(getStyle(obj,"left"));							
				//判断速度的正负值
				//如果从0向800移动，则speed为正
				//如果从800向0移动，则speed为负
				if(current > target){
					//此时速度应为负值
					speed = -speed;
				}

				//开启一个定时器来执行动画效果
				timer = setInterval(function(){	

				//获取box1原来的left值
				var oldValue = parseInt(getStyle(obj,"left"));
				//在旧值的基础上增加
				var newValue = oldValue + speed;
				//获取元素目前的位置
				
				//判断newValue是否大于800
				//从800向0移动
				//向左移动时，需要判断newValue是否小于target
				//向右移动时，需要判断newValue是否大于target
				if((speed < 0 && newValue < target) ||(speed > 0 && newValue >target)){
					newValue = target;
				}
				//将新值设置给box1
				obj.style.left = newValue + "px";
				//当元素移动到800px时使其停止执行动画
				if(newValue == target){
					//到达目标，关闭定时器
					clearInterval(timer);
				}
			},30);
		}

		/**
		 * 定义一个函数，用来获取指定元素的当前的样式	
		 * 		参数：
		 * 			obj 要获取样式的元素
		 * 			name 要获取的样式名
		 * 			target 执行动画的目标位置
		 */
		function getStyle(obj ,name){
			if(window.getComputedStyle){
			//正常浏览器的方式
			return getComputedStyle(obj,null)[name];				
			}else{
			//IE8的方式
			return obj.currentStyle[name];				
			}
			
		}
	</script>
</head>
<body>
	<button id="btn01">点击按钮以后box1向右移动</button>
	<button id="btn02">点击按钮以后box1向左移动</button>
	<br><br>
	<div id="box1"></div>	
	<div style="width: 0; height: 1000px; border-left: 1px black solid; position: absolute; left: 800px; top: 0px;"></div>
</body>
</html>
~~~

### 实例3

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		*{
			margin: 0;
			padding: 0;
		}

		#box1{
			width: 100px;
			height: 100px;
			background-color: red;
			position: absolute;
			left: 0;
		}

		#box2{
			width: 100px;
			height: 100px;
			background-color: yellow;
			position: absolute;
			left: 0;
			top: 200px;
		}
	</style>
	<script src="js/tools.js"></script>
	<script>
		window.onload = function(){
			//获取box1
			var box1 = document.getElementById("box1");

			//获取btn01
			var btn01 = document.getElementById("btn01");

			//获取btn02
			var btn02 = document.getElementById("btn02");

			//点击按钮以后，使box1向右移动（left值增大）
			btn01.onclick = function(){
				move(box1,"left",800,10);
			};

			//点击按钮以后，使box1向左移动（left值减小）
			btn02.onclick = function(){
				move(box1,"left",0,10);
			};

			//获取btn03
			var btn03 = document.getElementById("btn03");
			btn03.onclick = function(){
				move(box2,"left",800,10);
			};

			//测试	
			var btn04 = document.getElementById("btn04");
			btn04.onclick = function(){
				//move(box2,"width",800,10);
				//move(box2,"top",800,10);
				move(box2,"width",800,10,function(){
					//alert("动画执行完毕了");
					move(box2,"height",400,10,function(){
						move(box2,"top",0,10,function(){
						
						});
					});
				});
			};
		};

		//定义一个变量，用来保存定时器的标识
		/**
		 * 目前我们定时器的标识由全局变量timer保存，
		 * 	所有的正在执行的定时器都在这个变量中保存
		 */
		
		//var timer;

		
	</script>
</head>
<body>
	<button id="btn01">点击按钮以后box1向右移动</button>
	<button id="btn02">点击按钮以后box1向左移动</button>
	<button id="btn03">点击按钮以后box2向右移动</button>
	<button id="btn04">测试按钮</button>
	<br><br>
	<div id="box1"></div>	
	<div id="box2"></div>	
	<div style="width: 0; height: 1000px; border-left: 1px black solid; position: absolute; left: 800px; top: 0px;"></div>
</body>
</html>
~~~

### 实例4：轮播图

~~~javascript

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		*{
			margin:  0;
			padding: 0;
		}

		/*
		 *设置outer的样式 
		 */
		#outer{
			width: 520px;
			height: 333px;
			margin: 50px auto;
			background-color: greenyellow;
			padding: 10px 0;
			position: relative;
			/*裁剪溢出的内容*/
			overflow: hidden;
		}

		#imgList{
			/*去除项目符号*/
			list-style: none;
			/*设置ul的宽度*/
			/*width: 2600px;*/
			/*开启绝对定位*/
			position: absolute;
			/*设置偏移量*/
			/*每向左移动520个像素，就会显示到下一张图片*/
			left :0px;
		}

		/*设置图片中的li*/
		#imgList li{
			/*设置浮动*/
			float: left;
			/*设置左右外边距*/
			margin: 0 10px;
		}
		/*设置导航按钮*/
		#navDiv{
			/*开启绝对定位*/
			position: absolute;
			/*设置位置*/
			bottom: 15px;
			/*设置left的值
			 *outer宽度520
			 *navDiv宽度25*5=125
			 *520-125=395/2=197.5
			 */
		/*left: 197px;   但是这样就写死了*/
		}

		#navDiv a{
			display: block;
			width: 15px;
			height: 15px;
			background-color: red;
			/*设置超链接浮动*/
			float: left;
			/*设置左右外边距*/
			margin: 0 5px;
			/*设置透明*/
			opacity: 0.5;
			/*兼容IE8透明*/
			filter: alpha(opacity = 50);
		}

		/*设置鼠标移入的效果*/
		#navDiv a:hover{
			background-color: black;
		}
	</style>

	<!-- 引入工具 -->
	<script src="js/tools.js"></script>
	<script>
		window.onload = function(){
			
			//获取imgList
			var imgList = document.getElementById("imgList");

			//获取页面中所有的img标签
			var imgArr = document.getElementsByTagName("img");

			//设置imgList的宽度
			imgList.style.width = 520*imgArr.length + "px";

			// 设置导航按钮居中
			
			//获取navDiv
			var navDiv = document.getElementById("navDiv");

			//获取outer
			var outer = document.getElementById("outer");

			//设置navDiv的left的值
			navDiv.style.left = (outer.offsetWidth - navDiv.offsetWidth)/2 + "px";

			//默认显示图片的索引
			var index = 0;

			//获取所有的a
			var allA = document.getElementsByTagName("a");

			//设置默认选中的效果
			allA[index].style.backgroundColor = "black";

			/**
			 * 点击超链接切换到指定图片
			 * 		点击第一个超链接，显示第一个图片
			 * 		点击第二个超链接，显示第二个图片...
			 */
			
			//为所有的超链接绑定一个单击响应函数
			for(var i = 0; i < allA.length; i++){

				//为每一个超链接都添加一个number属性
				allA[i].num = i;

				//为超链接绑定一个单击响应函数
				allA[i].onclick = function(){

					//获取点击超链接的索引,并将其设置为index
					index = this.num;
					//alert(this.num);
					
					//切换图片
					/**
					 * 第一张 索引0 left 0
					 * 第二张 索引1 left-520
					 * 第三张 索引2 left -1040
					 */
					
					//imgList.style.left = -520*index + "px";
					//设置选中的a

					//修改正在选中的a
					//allA[index].style.backgroundColor = "black"; 不行
					
					setA();
					//使用move()函数切换
					move(imgList , "left" , -520*index , 20 , function(){

					});
				};
			}

			//创建要给方法，用来设置选中的a
			function setA(){

				//遍历所有的a,并将他们的背景颜色设置为红色
				for(var i = 0 ; i < allA.length; i++){
					allA[i].style.backgroundColor = "";
				}

				//将选中的a设置为黑色
				allA[index].style.backgroundColor = "black"; 
			}
		};
	</script>
</head>
<body>
	<!-- 创建一个外部的div，来作为一个大的容器-->
	<div id="outer">
		<!-- 创建一个ul,用于放置图片 -->
		<ul id="imgList">
			<li><img src="img/1.jpg" alt=""></li>
			<li><img src="img/2.jpg" alt=""></li>
			<li><img src="img/3.jpg" alt=""></li>
			<li><img src="img/4.jpg" alt=""></li>
			<li><img src="img/5.jpg" alt=""></li>
		</ul>

		<!-- 创建导航按钮 -->
		<div id="navDiv">
			<a href="javascript:;"></a>
			<a href="javascript:;"></a>
			<a href="javascript:;"></a>
			<a href="javascript:;"></a>
			<a href="javascript:;"></a>
		</div>
	</div>
</body>
</html>
~~~

### 实例5

~~~javascript
<!DOCTYPE html>
<html>

	<head>
		<meta charset="UTF-8">
		<title>二级菜单</title>
		<style type="text/css">
			* {
				margin: 0;
				padding: 0;
				list-style-type: none;
			}
			
			a,img {
				border: 0;
				text-decoration: none;
			}
			
			body {
				font: 12px/180% Arial, Helvetica, sans-serif, "新宋体";
			}
		</style>

		<link rel="stylesheet" type="text/css" href="css/sdmenu.css" />
		
		<script src="js/tools.js"></script>
		<script type="text/javascript">
			window.onload = function(){
				/**
				 * 我们的每一个菜单都是一个div
				 * 		当div具有collapsed这个类时，div就是折叠的状态
				 * 		当div没有这个类时，div就是展开的状态
				 */
				
				/**
				 * 点击菜单，切换菜单的显示状态
				 */
				
				//获取所有的class为memuSpan的元素
				var menuSpan = document.querySelectorAll(".menuSpan");

				//定义一个变量来保存当前打开的菜单
				var openDiv = menuSpan[0].parentNode;

				//alert(menuSpan.length);
				
				//为span绑定单击响应函数
				for(var i = 0; i < menuSpan.length; i++){
					menuSpan[i].onclick = function(){
						  //alert("hello");
						  
						  //this代表我当前点击的span
						  //获取当前span的父元素						  
						  var parentDiv = this.parentNode;

						  //切换菜单的显示状态
						  toggleMenu(parentDiv);

						  //判断openDiv和parentDiv是否相同
						  if(openDiv != parentDiv  && !hasClass(openDiv , "collapsed")){
						  	//打开菜单以后，应该关闭之前打开的菜单
						  	/**
						  	 * 为了可以同一处理动画的过渡效果，我们希望在这
						  	 * 将addClass改为toggleClass
						  	 */
						  
						  	//addClass(openDiv , "collapsed");
						  	
						  	//此处toggleClass()不需要有移除的功能
						  	//切换菜单的显示状态
						  	//toggleClass(openDiv , "collapsed");
						  	toggleMenu(openDiv);
						  }
						  

						  //修改openDiv为当前打开的菜单
						  openDiv = parentDiv;
					};
				}

				function toggleMenu(obj){
					//在切换类之前，获取元素的高度
						  var begin = obj.offsetHeight;

						  //切换parentDiv的显示
						  toggleClass(obj  , "collapsed");

						  //在切换类之后获取一个高度
						  var end = obj.offsetHeight;

						  //console.log("begin=" + begin + "end=" + end);
						  //动画效果就是将高度从begin向end过渡
						  
						  //将元素的高度重置为begin
						 obj.style.height = begin + "px";

						  //执行动画，从begin向end过渡
						  move(obj , "height" , end , 10 , function(){
						  		//动画执行完毕，内联样式已经没有存在的意义了，删除之
						  		obj.style.height = "";
						  });
				}
			};
		</script>
		
	</head>

	<body>

		<div id="my_menu" class="sdmenu">
			<div>
				<span class="menuSpan">在线工具</span>
				<a href="#">图像优化</a>
				<a href="#">收藏夹图标生成器</a>
				<a href="#">邮件</a>
				<a href="#">htaccess密码</a>
				<a href="#">梯度图像</a>
				<a href="#">按钮生成器</a>
			</div>
			<div class="collapsed">
				<span class="menuSpan">支持我们</span>
				<a href="#">推荐我们</a>
				<a href="#">链接我们</a>
				<a href="#">网络资源</a>
			</div>
			<div class="collapsed">
				<span class="menuSpan">合作伙伴</span>
				<a href="#">JavaScript工具包</a>
				<a href="#">CSS驱动</a>
				<a href="#">CodingForums</a>
				<a href="#">CSS例子</a>
			</div>
			<div class="collapsed">
				<span class="menuSpan">测试电流</span>
				<a href="#">Current or not</a>
				<a href="#">Current or not</a>
				<a href="#">Current or not</a>
				<a href="#">Current or not</a>
			</div>
		</div>
	</body>
</html>
~~~

## 间歇调用

![](JavaScript知识点查漏补缺/135.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		window.onload = function(){
			//获取count
			var count = document.getElementById("count")

			//使count中的内容，自动切换
			/**
			 * JS程序执行的速度使非常快的
			 * 如果希望一段程序，可以每间隔一段时间执行一次，可以使用定时调用
			 * 
			 */
			/*for(var i = 0; i < 10; i++){
				count.innerHTML = i;

				alert("hello");
			}*/

			/*count.innerHTML = 2;
			count.innerHTML = 3;
			count.innerHTML = 4;
			count.innerHTML = 5;*/

			/**
			 * setInterval()
			 * 	-定时调用
			 * 	-可以将一个函数，每隔一段时间执行一次
			 * 	-参数：
			 * 		1.回调函数，该函数会每隔一段时间被调用一次
			 * 		2.每次调用间隔的时间，单位是毫秒
			 *
			 * -返回值
			 * 		返回一个Number类型的数据
			 * 		这个数字用来作为定时器的唯一标识
			 */
			var num = 1;
			var timer = setInterval(function(){
				count.innerHTML = num++;
				if(num == 11){
					//关闭计时器
					clearInterval(timer);
				}
			} , 1000);

			//console.log(timer);
			
			//clearInterval()可以用来关闭一个定时器
			//方法中需要一个定时器的标识作为参数，这样将关闭标识对应的计时器
			
		};
	</script>
</head>
<body>
	<h1 id="count">num</h1>
</body>
</html>
~~~

### 实例1

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		window.onload = function(){
			/**
			 * 使图片可以自动切换
			 */
			
			//获取img标签 
			var img1 = document.getElementById("img1");

			//创建一个数组来保存图片的路径
			var imgArr = ["img/1.jpg" , "img/2.jpg", "img/3.jpg" , "img/4.jpg" , "img/5.jpg"];

			//创建一个变量，用来保存当前图片的索引
			var index = 0;

			//定义一个变量，用来保存定时器的标识
			var timer;

			//为btn01绑定一个单击响应函数
			var btn01 = document.getElementById("btn01");
			btn01.onclick = function(){
				/**
				 * 目前：我们每点击一次按钮，就会开启一个定时器
				 * 		点击多次就会开启多个计时器，这就导致图片的切换速度过快
				 *
				 * 		并且我们只能关闭最后一次开启的计时器
				 */
				
				//在开启定时器之前，需要将当前元素上的其他定时器关闭
				clearInterval(timer);

				/**
			 * 开启一个定时器，来自动切换图片 
			 */
			 timer = setInterval(function(){

				//使索引自增
				index++;

				//判断索引是否超过最大索引
				/*if(index >= imgArr.length){
					//则将index设为0
					index = 0;
				}*/
				index = index % imgArr.length; 
				//修改img1的src属性
				img1.src = imgArr[index];
			} , 1000);
		};

		//为btn02绑定一个单击响应函数
		var btn02 = document.getElementById("btn02");
		btn02.onclick = function(){
			//点击按钮以后，停止图片的自动切换，关闭定时器
			/**
			 * clearInterval()可以接收任意的参数，如果参数是一个有效的定时器的标识，则停止
			 * 对应的计时器
			 *
			 * 如果参数不是一个有效的标识，则什么也不做
			 */
			clearInterval(timer);
		};
 	};
			
	</script>
</head>
<body>
	<img id="img1" src="img/1.jpg" alt="">
	<br><br>
	<button id="btn01">开始</button>
	<button id="btn02">停止</button>
</body>
</html>
~~~

### 实例2

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#box1{
			width: 100px;
			height: 100px;
			background-color: red;
			position:absolute;
		}
	</style>
	<script>
		//使div可以根据不同的方向键向不同的方向移动
		/**
		 * 按左键，div向左移...
		 */
		window.onload = function(){

			//定义一个变量，来表示移动的速度
				var speed = 10;

			//创建一个变量表示方向
			//通过修改dir来影响方向 
			var dir = 0;

			//开启一个定时器，来控制div的移动
			setInterval(function(){
               switch(dir){
					case 37:
					//alert("向左");  left值减小
					box1.style.left = box1.offsetLeft - speed + "px";
					break;

					case 39:
					box1.style.left = box1.offsetLeft + speed + "px";
					//alert("向右");
					break;

					case 38:
					box1.style.top = box1.offsetTop - speed + "px";
					//alert("向上");
					break;

					case 40:
					box1.style.top = box1.offsetTop + speed + "px";
					//alert("向下");
					break;
				};
				//console.log(event.keyCode);
			},30);

			//为document绑定一个按键按下的事件
			document.onkeydown = function(event){
				event = event || window.event;

				//当用户按了ctrl以后，速度加快
				if(event.ctrlKey){
					speed = 500;
				}else{
					speed = 10;
				}
				/**
				 * 37 左
				 * 38 上
				 * 39 右 
				 * 40 下
				 */
				
				//使dir等于按键的值
				dir = event.keyCode;
			};

			//当按键松开时，div不再移动
			document.onkeyup = function(){
				//设置方向为0
				dir = 0;
			};
		};
	</script>
</head>
<body>
	<div id="box1"></div>
</body>
</html>
~~~

## 系统对话框

![](JavaScript知识点查漏补缺/136.png)

## alert

![](JavaScript知识点查漏补缺/137.png)

## confirm

![](JavaScript知识点查漏补缺/138.png)

## prompt

![](JavaScript知识点查漏补缺/139.png)

## location对象

![](JavaScript知识点查漏补缺/140.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * Location
		 *  -该对象封装了浏览器的地址栏的信息
		 */
		window.onload = function(){

			//获取按钮对象
			var btn = document.getElementById("btn")
			btn.onclick = function(){
				//如果直接打印location,则可以获取到地址栏的信息（当前页面的完整的路径）
				//alert(location);
				/**
				 * 如果直接将location属性修改为一个完整的路径，或相对路径
				 * 	则我们页面会自动跳转到该路径，并且会生成相应的地址路径
				 * 
				 */
				//location = "http://www.baidu.com"
				
				/**
				 * assign()
				 * 	-用来跳转到其他的页面，作用和直接修改location一样
				 * 	
				 */
				//location.assign("http://www.baidu.com");
				
				/**
				 * reload()
				 * 	-用于重新加载当前页面，作用和刷新按钮一样
				 * 	-如果在方法中传递一个true作为参数，则会强制清空缓存刷新页面
				 */
				//location.reload(true);
				
				/**
				 * replace()
				 * 	-可以使用一个新的页面替换当前页面，调用完毕也会跳转界面
				 * 	-不能生成历史记录，不能使用回退按钮回退
				 */
				location.replace("01 BOM.html");
			};
		};
	</script>
</head>
<body>
	<button id="btn">点我一下</button>
	<h1>Location</h1>
	<input type="text">
	<a href="01 BOM.html">去BOM</a>
</body>
</html>
~~~



## navigator对象

![](JavaScript知识点查漏补缺/141.png)

## screen对象

![](JavaScript知识点查漏补缺/142.png)

## history对象

![](JavaScript知识点查漏补缺/143.png)

~~~javascript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script>
		/**
		 * History
		 * 	-对象可以用来操作浏览器向前或向后翻页
		 */
		
		/**
		 * length
		 * 	-属性，可以获取到当前访问的链接的数量
		 */
		//alert(history.length); 
		
		/**
		 * back()
		 * 	-可以用来回退到上一个页面，作用和浏览器的回退按钮一样
		 */
		//history.back();

		/**
		 * forward()
		 * 	-可以跳转到下一个界面，作用和浏览器的前进按钮一样
		 */
		//history.forward();
		
		/**
		 * go()
		 * 	-可以用来跳转到指定的页面
		 * 	-它需要一个整数作为参数
		 * 		1：表示向前跳转1个界面
		 * 		2：表示向前跳转2个界面
		 * 		-1:表示向后跳转1个界面
		 * 		-2：表示向后跳转2个界面
		 */
		history.go(1);
		history.go(-1);
		window.onload = function(){
			//获取按钮对象
			var btn = document.getElementById("btn")
			btn.onclick = function(){
			};
		};
	</script>
</head>
<body>
	<button id="btn">点我一下</button>
	<h1>History</h1>
	<a href="01 BOM.html">去BOM</a>
</body>
</html>
~~~

## document

![](JavaScript知识点查漏补缺/144.png)











