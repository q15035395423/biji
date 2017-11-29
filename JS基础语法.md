## 网页的组成（3部分）    
* 结构层（HyperText Markup Language）
* 表现层（Cascading Style Sheets）
* 行为层（JavaScript）

计算机语言发展阶段：二进制语言、汇编语言、高级语言（c\c++\java\php...）

##什么是程序？
（炒菜的过程是流程，把炒菜的过程写成菜谱是程序，记录炒菜的过程就是编程。）
为了实现某个功能或某个目的，通过计算机语言写的指令序列的集合。

流程：一个逻辑思维,

需求

程序：记录过程媒介

编程

##JavaScript    Java
* 公司：Java——sun公司  JS——网景公司
* 语言：Java是强类型的语言  JS是弱类型的语言
       Java:int a=10;           JS:var a = 10;var a = 10.3;
            float b=2.3;
            string c='ddd';        var = 'ddd';
* 特点：Java是纯面向对象的（封装、继承、多态） 
   JS是基于对象（内置对象：日期、数组...）
* 执行方式：Java是编译（解析成计算机能识别的代码）的类型;JS是解释型的

# JavaScript 

##JS作用

* 给页面添加动效
* 实现数据验证
* 操作HTML、CSS
* 制作游戏【最新】
* 单页面应用（谷歌在线的Word、Excel等在线编辑器;各大平台的云;）【最新】
* 服务器端的应用（node.js）【最新】
* cookie：存储小型数据【最新】
  ...

##JS是什么
JS是运行在浏览器的一个脚本语言（脚本语言可以直接在浏览器中解析执行，无需编译，从上到下直接解析，没有生命周期）
JS是基于对象和事件驱动的解释型的松散型语言。（JS特点）
* 基于对象（具体的、抽象的）：本身有自己内置对象
* 事件驱动：对浏览器和用户的行为进行响应
* 解释型：浏览器直接解释，无需编译
* 松散型（弱类型）：声明变量无需分开，直接一个var就可以声明变量;
  ​                 可以不用写分号，但为了规范，写上为好

JS组成部分：ECMAScript（基础语法、基本对象）、DOM（文档对象模型）、BOM（浏览器对象模型）

##JS语言
### 如何执行？

代码从上到下解析但不是一行一行去解析，而是一条语句一条语句去解析。

### HTML如何引入JS？

**注意：**  多个script块之间会相互影响；按加载顺序从上到下一条语句一条语句进行加载。

* 引入外部文件  <script src=""></script>

​       **注意 ：** 引入外部文件的时候，不能在标签中间写入内容

~~~html
 <script src="lianxi.js"></script>
~~~

* 嵌入式  <script>alert(1);</script>

  **注意 ：**  引入嵌入式的时候，不能在写地址

  ~~~html
   <script>alert(1);</script>
  ~~~

* 在超链接或者重定向里面写入  <a href="javascript:alert(1)">超链接</a>

  * 超链接：<a href="javascript:alert(1)">超链接</a>

  * 重定向

    ~~~html
    <form action="javascript:alert(1)" method="">
      <input type="submit">
    </form>
    ~~~

* 在事件之后调用

  ~~~html
  <div onclick="alert(1)">点击我</div>
  ~~~

~~~html
超链接的表现形式（常用有4种）：
1.普通链接：<a href="http://www.baidu.com">百度</a>
2.写入JS代码，会屏蔽href属性
<a href="javascript:alert(1)">超链接</a>
<a href="javascript:void(0)">超链接</a>
3.若实现资源下载，默认只能是压缩过的文件
<a href="1.zip"></a>
4.空链接，实现的是返回页面顶部
<a href=""></a>
5.邮件地址
...
~~~

### 如何输出？

#### 一、JS输出工具

* 把想要展示的数据输出至页面
* 调试

1.alert();在页面中弹出一个框。

 **注意：** alert会阻止后面代码的执行

2.console.log();将数据内容输出至控制台

3.document.write();将数据内容输出至页面中

4.confirm();在页面中弹出一个带确定和取消按钮的弹出框

**注意：** 识别标签和行内样式

5.prompt('请输入你的名字');页面中弹出一个带提示信息和输入框的弹出框

~~~html
<script>
	alert(1);
  	console.log(2);
  	document.write('<div style="color:red;">html</div>');
    confirm(0);
  	prompt('请输入你的名字');
</script>
~~~

#### 二、注释标签

### 声明变量

#### 一、变量命名规范：

> 1、变量名必须以字母、下划线_或 $ 开头，后面的部分可以跟任意的字母、数字、下划线 或美元符
>
> 2、不能使用关键字（JS自定义的 var）或者是保留字（为以后扩展用）命名
>
> 3、JavaScript有自己的命名习惯
>
> - 驼峰命名法：getElementByld
> - 首字母大写法：Object
>
> 4、变量名区分大小写
>
> 5、命名一定要有意义，提高代码可读性

#### 二、什么是变量

> 变量就是存储数据的容器。
>
> 内存就是一个盒子，每次声明一个变量，它都会在内存中开辟一段空间进行保存。保存起来后，当我们需要用的时候，会从内存中获取相应的数据。
>
> **注意：** 如果浏览器关闭，内存会释放空间，方便下次使用。
>
> 计算机内存的模块：依据数据类型不同放在不同区域，栈区（初始数据类型）堆区（引用数据类型）、代码块

#### 三、声明变量（通过关键字）：

##### var

##### let（Es6）

- let的用法类似于var

- let不存在变量提升现象（不可以在声明之前进行调用）

- let不能重新声明      报错：该变量已经存在

- let存在块级作用域（es6）   

  **注：** 块级作用域：es6 if switch function for

  use  script用来区分es5与es6

##### const（Es6）

* const声明的是一个常量
* const只能声明的同时进行赋值（单个/多个变量都可以）
* const不存在变量提升现象
* const不能重新声明      报错：该变量已经存在

#### 四、变量的赋值情况【针对var】

>* 声明变量的同时进行赋值（单个变量）
>
>* 声明之后赋值（单个变量）
>
>* 声明多个变量并同时进行赋值
>
>**注意：** 多个变量之间用逗号隔开
>
>* 声明多个变量，之后赋值
>
>~~~html
><script>
>var num=10;
>console.log(num);
>
>var num1;
>num1 = 'hello';
>console.log(num1);
>
>var num2= 20,num3= 30;
>console.log(num2,num3);
>
>var num4,num5;
>num4 = 40;
>num5 = 50;
>console.log(num4,num5);
></script>
>~~~
>
>

#### 五、注意【针对var】

>* 在变量声明之前进行调用，不会报错，只会返回undefined（与代码预解析顺序有关）【变量提升现象：变量声明之前进行调用】
>* 不通过关键字声明的变量，但是赋值了，他会返回对应的值（不通过关键字声明的变量是全局变量）
>* 不通过关键字声明的变量，但是没有赋值，会报错
>* 对变量重新赋值，会发生覆盖，遵循就近原则
>* 对变量重新声明并赋值，会发生覆盖
>
>~~~html
><script> 
>console.log(num);
>var num=10;
>
>num1 = 'hello';
>console.log(num1);
>
>num2;
>console.log(num2);
>
>var num4=40;
>num4 = 50;
>console.log(num4);
>
>var num4=40;
>var num4 = 50;
>console.log(num4);
></script>
>~~~
>

###### JS关键字

| break |    case    |  catch  | continue | default  | delete |
| :---: | :--------: | :-----: | :------: | :------: | :----: |
|  do   |    else    | finally |   for    | function |   if   |
|  in   | instanceof |   new   |  return  |  switch  |  this  |
| throw |    try     | typeof  |   var    |   void   | while  |
| with  |            |         |          |          |        |

###### JS保留字

| abstract | boolean |    byte    |     char     |   class   |   const   |
| :------: | :-----: | :--------: | :----------: | :-------: | :-------: |
| debugger | double  |    enum    |    export    |  extends  |   final   |
|  float   |  goto   | implements |    import    |    int    | interface |
|   long   | native  |  package   |   private    | protected |   publi   |
|  short   | static  |   super    | synchronized |  throws   | transient |
| volatile |         |            |              |           |           |

### 数据类型

#### 一、什么是数据类型：

> 能够表达或操作值的类型，称为数据类型。

#### 二、为何要划分数据类型：

* 需求不同
* 在内存中存储的位置不一样

#### 三、数据类型（两大类）

##### 1、初始类型（存放在栈区，内存比较小，但访问速度快）

* undefined：

  可能的情况：声明变量并未赋值，返回undefined；

  ​                      声明变量之前进行访问，返回undefined。

  返回的值：undefined

  返回值的类型：undefined

  ~~~html
  <script> 
       console.log(num);
       var num=10;
       console.log(num);
       console.log(typeof num);判断返回值的类型
  </script>
  ~~~

* null（空，占位符）：

  可能的值：null

  返回的值：null

  返回值的类型：object

  ~~~html
  <script> 
       console.log(num);
       var num=null;
       console.log(num);
  </script>
  ~~~

* number（数值类型）：

  可能的值：整型、浮点型、二进制、十进制、八进制、十六进制、科学计数法（最大值、最小值）

  返回的值：对应的数值

  返回值的类型：number

  ~~~html
  <script> 
      console.log(Number.MAX_VALUE);
      console.log(Number.MIN_VALUE);
  </script>
  ~~~

* string(字符串类型)：通过引号引起来

  可能的值：通过引号引起来的

  返回的值：对应的字符串

  返回值的类型：string

  ~~~html
  <script> 
      var str1="HELLO";
      console.log(str1);
  </script>
  ~~~

* boolean（布尔类型）：true  false

  可能的值：true  false

  返回的值：true  false

  返回值的类型：boolean

  ~~~html
  <script> 
      var str1="true";
      console.log(str1);
  </script>
  ~~~

* symol（ES6）

##### 2、引用类型（存放在堆区，内存比较大，但访问速度慢）

​	object（数组、函数...）



### 运算符

#### 一、算术运算（+ - * /  % ++ --）

##### 加号 + ：

**注意：** 加、减、乘、除、取余相同

* 进行加法运算
  * 如果两个操作数都是number，最终得到number
  * 如果其中一个操作数是undefined，最终得到NaN（not a number，是number类型的一个状态）
  * 如果其中一个操作数是null，会转换成对应的值进行计算，最终得到number的值
  * 如果其中一个操作数是boolean，会转换成对应的值进行计算，最终得到number
* 字符串连接
  * 如果其中一个操作数是string
    - 是数值的话：会隐式转换，等到number
    - 是字母的话：NaN
  * 如果两个操作数都是string，
    - 是数值的话：会隐式转换，等到number
    - 是字母的话：NaN

~~~html
<script>
	var num1 = 30;
  	var num2 = 2.4;
  	var sum = num1 + num2;
  	console.log(sum);
  	console.log(typeof sum);
</script>

<script>
	var num1 = 30;
  	var num2 = 'aaa';
  	var sum = num1 + num2;
  	console.log(sum);
  	console.log(typeof sum);
</script>

<script>
	var num1 = 30;
  	var num2 = '';
  	var sum = num1 + num2;
  	console.log(sum);
  	console.log(typeof sum);
</script>

<script>
	var num1 = 30;
  	var num2 = null;
  	var sum = num1 + num2;
  	console.log(sum);
  	console.log(typeof sum);
</script>

<script>
	var num1 = 30;
  	var num2 = true;
  	var sum = num1 + num2;
  	console.log(sum);
  	console.log(typeof sum);
</script>
~~~

##### 减号 - ：

* 如果两个操作数都是number，最终得到number
* 如果其中一个操作数是undefined，最终得到NaN
* 如果其中一个操作数是null，会转换成对应的值进行计算，最终得到number的值
* 如果其中一个操作数是boolean，会转换成对应的值进行计算，最终得到number
* 如果其中一个操作数是string
  * 是数值的话：会隐式转换，等到number
  * 是字母的话：NaN
* 如果两个操作数都是string，
  * 是数值的话：会隐式转换，等到number
  * 是字母的话：NaN

##### 乘法 * ：

* 特殊用法：进行幂运算，用两个乘号

##### 自增 ++：

* num++ ：先运行再自增1；
* ++num：先自增1再运行；

##### 自减 -- ：

- num-- ：先运行再自减1；
- --num：先自减1再运行；

#### 二、比较运算符（> < == ===【判断类型】 >= <= !=）

* 如果操作数是string类型，会先进行隐式转换，转换成功进行正常运算（true或false），转换不成功，永远返回false。

* null == 0，进行比较最终返回false

* undefined == null，进行比较最终返回true

  ~~~html
  <script>
  	var num1 = null;
    	var num2 = 0;
    	console.log( num1 == num2 );
  </script>

  <script>
  	var num1 = '';
    	var num2 = null;
    	console.log( num1 == num2 );
  </script>
  ~~~

#### 三、赋值运算符（=  +=  -=  *=  /=  %=）

~~~html
<script>
	var num1 = 20;
  	mun1 += 2;    //num1 = mun1 + 2;
  	console.log( num1 );
</script>
~~~

#### 四、逻辑运算符（&&与   ||或    !非）

* 可以操作任何类型的数据。

* **注意 :** 数字0，false，undefined，null，NaN，空字符串会转换为false

* ##### &&：同真为真，其余全为假

  | num1  | mun2  | result |  结果  |
  | :---: | :---: | :----: | :--: |
  | true  | true  |  true  | num2 |
  | true  | false | false  | num2 |
  | false | true  | false  | num1 |
  | false | false | false  | num1 |

  **注意：** 如果第一个操作数为假，发生短路原则，对第二个数不会进行操作，并返回假值。

  ~~~html
  <script>
  	var num1 = 20;
  	var num2 = 10; 
    	console.log(num1 && num2);
  </script>     结果：10
  ~~~

* ##### ||：同假为假，其余全为真

  | num1  | num2  | result |  结果  |
  | :---: | :---: | :----: | :--: |
  | true  | true  | false  | num1 |
  | true  | false | falae  | num1 |
  | false | true  | false  | num2 |
  | false | false |  true  | num2 |

  **注意：** 如果第一个操作数为真，发生短路原则，对第二个数不会进行操作，并返回真值。

  ~~~html
  <script>
  	var num1 = 20;
  	var num2 = 10; 
    	console.log(num1 || num2);
  </script>     结果：20
  ~~~

* ##### !非：

  ~~~html
  <script>
  	var num1 = 20;
  	var num2 = 10; 
    	console.log(!num2);
  </script>     结果：false
  ~~~

#### 五、其他运算符

##### 1.一元运算符

> typeof
>
> ++  --
>
> +（正号）-（负号）
>
> delete（删除一个对象）
>
> new

##### 2.三元运算符

> 一个条件表达式?为真的值:为假的值
>
> ~~~html
> <script>
> 	console.log(3 > 5?'真的':'假的');
> </script>
> ~~~

#### 六、特殊运算符()

>作用：提高优先级

#### 七、模板字符串（ES6）

>作用：方便引入变量
>
>模板字符串要用反引号(`)括起来，如果需要引入变量通过${变量名}

~~~html
<script>
	var num1 = 20;
	var num2 = 10;
  	var sum = num1 + num2;
	console.log("这是num1 -- " + num1 + "和num2 -- " + num2 + "的和" + sum);
    console.log("这是num2 -- " + num2);
    console.log(`这是num1 -- ${num1}和num2 -- ${num2}的和${sum}`); 
    console.log(`这是num2 -- ${num2}`); 
</script>
~~~

### 流程控制

#### 一、流程

>程序代码的执行顺序
>
>**注意：** JS的执行是根据浏览器的解析从上到下，一条语句一条语句的执行，有且只有这一种方式。

#### 二、流程控制

> 通过规定的语句让程序代码有条件的按照一定的方式执行

#### 三、表达式

> 表达式一般由运算符或操作数构成，且有一定的值。（**注：** 已经有值或即将赋值的都是表达式）

~~~html
<script>
	var a = 20;
	var b = 2 * 3;
  	var c = a;
  	var d;
	d = 30;
</script>
~~~

#### 四、语句

>以分号为标识的为一条语句。
>
>* 声明语句 （声明一个变量、数组...）
>
>* 赋值语句 （对变量进行赋值）
>
>* 表达式语句（例如：console.log(typeof num1);）
>
>* 控制语句：if判断语句，switch条件语句，for循环语句等
>
>* 函数
>
>* 终止语句：
>
>break：跳出整个循环   
>
>​     **注意：** 每次只能跳出一层循环，若想一次跳出多层循环，在要跳出的那层循环前加一个标记，比如：'out:'，那么终止语句就是’break out;‘。
>
>continue：跳出本层循环
>
>​    **注意：** 最好用适当的语句代替continue语句，不要用continue语句

#### 五、三大流程控制

##### 1.顺序结构

> 是程序中最基本的流程控制。（默认从上到下一条语句一条语句执行）

##### 2.选择结构

> 让代码有条件的执行。

* 分支结构：有多个条件，且条件有范围（会隐式进行数据转换）

  if(条件表达式){执行的语句};

  if(){}else(){};

  if(){}else if(){}else(){};

  **注意：** 条件可以是表达式也可以是任何数据类型

  ~~~html
  <script>
  	var date = prompt('请输入日期');
    	console.log(typeof date);
      //if(date == '6' || date == '7'){
      //    alert('明天不用上课');
      //}
    
    	//if(date >= '6' && date <= '7'){
      //      alert('明天不用上课');
      //}else{
      //     alert('输入有误');
      //}
    
    	if(date >= '6' && date <= '7'){
            alert('明天不用上课');
      }else if(date > '0' && date < '6'){
           alert('明天正常上课');
      }else{
           alert('日期输入有误');
      }
  </script>
  //成绩等级查询：
  <script>
  	var sco = Number(prompt('请输入成绩'));
    	console.log(typeof sco);
    	if(sco >= 60 && sco <= 100){
            alert('成绩及格');
            if(sco >= 60 && sco < 80){
            	alert('成绩一般');
            }else if(sco >= 80 && sco < 90){
            	alert('成绩良好');
            }else{
            	alert('成绩优秀');
            }
      }else if(sco >= 0 && sco < 60){
           alert('成绩不合格');
           if(sco >= 0 && sco < 40){
            alert('没救了');
           }else{
            alert('争取及格');
           }
      }else{
           alert('成绩输入有误');
      }
  </script>
  ~~~

* 条件结构：只有一个条件，且条件没有范围（不会进行数据转换，是什么类型就写成什么类型）

  switch(表达式){

  ​       case 条件1:条件1成立执行的语句;

  ​       break;

  ​       case 条件2:条件2成立执行的语句;

  ​       break;

  ​       ...

  ​       default:条件都不满足执行的语句;

  }

  ~~~html
  <script>
    	var date = new Date();
    	date = =date.getDate();
   	console.log(date);
    
    //星期：
  	var date = prompt('请输入日期');
    	console.log(typeof date);
      switch(date){
          case '1':alert('周一');
          break;
          case '2':alert('周二');
          break;
          case '3':alert('周三');
          break;
          case '4':alert('周四');
          break;
          case '5':alert('周五');
          break;
          case '6':alert('周六');
          break;
          case '7':alert('周日');
          break;
          default:alert('输入有误');
      }
    
    //四则运算：
    	var num1 = Number(prompt('请输入第一个值'));     //注意：数据类型
  	if(isNaN(num1)){
  		alert('请重新输入');
  	}
  	var num2 = Number(prompt('请输入第二个值'));
  	if(isNaN(num2)){
  		alert('请重新输入');
  	}
  	var symbol = prompt('请输入运算符');
  	switch(symbol){
  		case '+':alert(`${num1}+${num2}=${num1+num2}`);  注意“+”，容易出现字符串连接
  		break;
  		case '-':alert(`${num1}-${num2}=${num1-num2}`);
  		break;
  		case '*':alert(`${num1}*${num2}=${num1*num2}`);
  		break;
  		case '/':alert(`${num1}/${num2}=${num1/num2}`);
  		break;
  		case '%':alert(`${num1}%${num2}=${num1%num2}`);
  		break;
  		default:alert('请重新输入');
  	}
  </script>
  ~~~

##### 3.循环结构

当条件满足的时候，需要重复的执行一段代码。

一、for(初始化变量;条件表达式;步操作){执行的语句}

执行方式：先执行初始化变量，判断变量是否满足，满足执行，继续判断循环，不满足条件跳出循环

~~~html
<script>
	for(var a = 1;a <= 10;a++){
         alert(1);  
    }
  
    for(var i = 1;i <= 10;i++){
         if(i % 2 == 0){
              console.log(`100以内的偶数${i}`);
         }else if(i % 2 != 0){
              console.log(`100以内的奇数${i}`);
         }
    }
  
    for(var h = 1;h < 200;h++){
         if(h % 3 == 1 && h % 4 == 2 && h % 5 == 3){
              console.log(h);
         }
    }
  
  //水仙花【三位数】
  //【方法一】：
  for(var i = 1;i < 10;i++){
		for(var j = 0;j < 10;j++){
			for(var k = 0;k < 10;k++){
				if((i**3 + j**3 + k**3) == (i*100+j*10+k*1)){
					document.write(`水仙花数：${i*100+j*10+k*1}<br />`);
				}
			}
		}
	}
  //【方法二】：
  var g = 0,s = 0,b = 0;
	for(var shu = 100;shu < 1000;shu++){
		g = shu % 10;
		s = parseInt((shu / 10) % 10);
		b = parseInt(shu / 100);
		if(shu == (b**3 + s**3 + g**3)){
			document.write(`水仙花数：${shu}<br />`);
		}
	}
  
  //金字塔
 	for(var h = 1;h <= 6;h++){
    	for(var k = 1;k <= 6-h;k++){
        	document.write('&nbsp;');
    	}
    	for(var x = 1;x <= h;x++){
    		document.write('*&nbsp; ');
    	}
    document.write('<br />');
    }
  
  //十乘十表格
  //【无样式】
  	var tab = '<table width="600px" height="600px" border="1px" cellspacing="0">';
		for(var i = 0;i < 10;i++){
			tab += '<tr">';
			for(var j = 0;j < 10;j++){
				tab += '<td></td>';
			}
			tab += '</tr>';
		}
	tab += '</table>';
	document.write(tab);
  //【隔行换色】
  	var tab = '<table width="600px" height="600px" border="1px" cellspacing="0">';
		for(var i = 0;i < 10;i++){
			if(i % 2 == 0){
				tab += '<tr bgColor="pink">';
			}else{
				tab += '<tr bgColor="yellow">';
			}
			for(var j = 0;j < 10;j++){
				tab += '<td></td>';
			}
			tab += '</tr>';
		}
	tab += '</table>';
	document.write(tab);
  //【单个变色：四种颜色】
  	var tab1 = '<table width="600px" height="600px" border="1px" cellspacing="0">';
		for(var i = 0;i < 10;i++){
			tab1 += '<tr>';
			for(var j = 0;j < 10;j++){
				// tab1 += '<td bgColor="red"></td>';
				if((i % 2 == 1) && (j % 2 == 1)){
					tab1 += '<td bgColor="blue"></td>';
				}else if((i % 2 == 0) && (j % 2 == 0)){
					tab1 += '<td bgColor="red"></td>';
				}else if((i % 2 == 1) && (j % 2 == 0)){
					tab1 += '<td bgColor="yellow"></td>';
				}else{
					tab1 += '<td bgColor="green"></td>';
				}
			}
			tab1 +='</tr>'
		}
	tab1 += '</table>';
	document.write(tab1);
</script>
~~~

二、while(条件表达式){要执行的语句};

~~~html
<script>
var a = 1;                  //先声明赋值
while(a < 10){              //接着判断条件，条件满足继续执行
   doccument.write(a);      //继续执行语句
   a++;                     //最后进行步操作，当条件超出范围，退出循环
}
</script>
~~~



~~~html
<script>
  //九九乘法表
	var a=1;
    while(a < 10){
    var b=1;
    while(b <= a){
        document.write(`${a}*${b}=${a*b}`);
        document.write('&nbsp;');
        b++;
        }
    document.write('<br/>');
    a++;
    }
</script>
~~~

三、do{要执行的语句}while(条件表达式);

~~~html
<script>
	var b = 1;
	do{
      document.write('b');
	  b++;
	}while(b < 10);
</script>
~~~

总结：

while和do while的区别

>  while：满足条件才执行循环体
>
>  do while：限制性一次循环体，在进行判断

for和while的区别

> 循环次数确定时用for
>
> 循环次数不确定时用while

### 数组

#### 一、数组

变量：存储数据的容器

数组：存储一组或一系列相关数据的集合

#### 二、优势

> * 方便对数据进行管理
>
>
> * 可以保存大批量的数据

#### 三、创建方式

1.以快捷方式创建（json格式 ）：  var arr = [];

2.通过实例化对象的方式：var arr = new Array();

#### 四、赋值情况

1.声明的同时并赋值

​	var arr = [1,2,3,'a','b'];

2.声明之后再赋值

>  var arr = [];
>
>  arr[0] = 1;
>
>  arr[1] = 2;

#### 五、对数组的访问

以下标的形式进行访问

* length属性：统计数据的长度
* 访问数组的第一个元素：arr[0];
* 访问数组的最后一个元素：arr[arr.length-1];

#### 六、对数组的遍历

##### 1.for

for(初始化值;条件表达式;步操作){执行的语句;}

for遍历之后有顺序；

~~~html
<script>
  var arr = [18,24,3,56,68,'ds','gf'];
    for(var i = 0;i < arr.length;i++){
    	arr[i]*=2;
    }
  document.write(arr);
  
  var arr = [18,24,3,56,68,'ds','gf'];
    for(var i in arr){
    	arr[i];   //对应数组的每个元素
    }
  document.write(arr);
</script>
~~~

##### 2.for in【ES6】[一般用于数组和对象的遍历]

for(变量 in 对象){}

for in 最终遍历出来的是对象的属性，没有顺序

3.for      【ES6】

#### 七、 **注意：** 

>  数组默认的值是空【变量默认的值是undefined】；
>
>  数组的长度是可变的；
>
>  数组可以保存任何类型的数据；
>
>  ​数组下标是从0开始 
>
>  数组下标越界【提示undefined】

冒泡排序:

>  数字就如有气泡的海绵一样，数字大的浮上，数字小的下沉。

希尔排序、快速排序及区别

~~~html
<script>
	// 数组去空
    var a = [18,24,3,,68,'ds','gf',,85];
    var b = [];
    for(var i = 0;i < a.length;i++){
    	if(a[i] !== undefined){
    		b[b.length] = a[i];
    	}
    }
    console.log("数组去空后是：" + b);

    // 最大值
    var arr = [18,24,3,68,36,85];
    var max = arr[0];
    for(var i = 0;i < arr.length;i++){
    	if(max < arr[i]){
    		max = arr[i];
    	}
    }
    console.log("数组的最大值是：" + max);

    // 最小值
    var arr = [18,24,3,68,36,85];
    var min = arr[0];
    for(var i = 0;i < arr.length;i++){
    	if(min > arr[i]){
    		min = arr[i];
    	}
    }
    console.log("数组的最小值是：" + min);

    // 平均值
    var arr = [18,24,3,68,36,85];
    var sum = 0;
    for(var i = 0;i < arr.length;i++){
    	sum += arr[i];
    	}
    var ave = sum / arr.length;
    console.log("数组的平均数是：" + ave);

    // 数组排序：从大到小
    var arr = [18,24,3,68,36,85];
    for(var i = 0;i < arr.length-1;i++){
    	for(var j = 0;j < arr.length-1-i;j++){
    		if(arr[j] < arr[j+1]){
    			var xu = arr[j];  
                arr[j] = arr[j+1];  
                arr[j+1] = xu;
    		}
    	}
    }
    console.log("从大到小的排序："+ arr);

    // 数组排序：从小到大
    var arr = [18,24,3,68,36,85];
    for(var i = 0;i < arr.length-1;i++){
    	for(var j = 0;j < arr.length-1-i;j++){
    		if(arr[j] > arr[j+1]){
    			var xu = arr[j];  
                arr[j] = arr[j+1];  
                arr[j+1] = xu;
    		}
    	}
    }
    console.log("从小到大的排序："+ arr);

    var arr = [18,24,3,68,36,85];
    for(var i = 0;i < arr.length;i++){
    	for(var j = i + 1;j < arr.length;j++){
    		if(arr[i] > arr[j]){
    			var num = arr[i];
    			arr[i] = arr[j];
    			arr[j] = num;
    		}
    	}
    }
    console.log("从小到大的排序："+ arr);

    // 数组筛选数据类型
    var arr = [-1,32,,56,'a',93,0,-34];
    for(var i = 0; i < arr.length; i++) {
    	if(typeof arr[i] == 'number') {
        console.log("arr数组中是Number类型的有：" + arr[i]);
    	}
    }

    // 筛选数组中大于0的数
    var arr = [-1,32,56,'a',93,0,-34];
    for(var i = 0; i < arr.length; i++) {
    	if(arr[i] > 0) {
        console.log("arr数组中大于0的数有：" + arr[i]);
    	}
    }

    // 将数组里每个元素扩大二倍
    var arr = [18,24,3,56,68,'ds','gf'];
    for(var i = 0;i < arr.length;i++){
    	arr[i]*=2;
    }
	console.log("数组中每个元素扩大两倍后是："+ arr);

	// 反向输出数组中的各元素
	var arr = [8,24,3,56,68,1];
	var newArr = [];
	for(var i = arr.length - 1;i >= 0;i--){
		newArr[newArr.length] = arr[i];
	}
	console.log("反向输出数组元素是：" + newArr);

	// 数组合并
	var x = [8,24,3,56,68,1];
	var y = [18,24,3,,68,'ds','gf',,85];
	for(var i = 0;i < y.length;i++){
		x[x.length] = y[i];
	}
	console.log("数组合并后是：" + x);
</script>
~~~

#### 八、二维数组

每个数组元素的值，对应的又是一个数组。

##### 声明方式：

> * 声明的同时并赋值
> * 先声明之后再赋值
>
> ~~~html
> 声明的同时并赋值：
> var arr2 = [[3,4,7],[1,2,3],[534,32,83]];
> 先声明之后再赋值：
> var arr3 = [];
> arr3[0] = [43,1,62,32];
> arr3[1] = [63,28,16,24];
> ~~~

##### 访问方式：

> 通过双下标

##### 二维数组的遍历：双层for循环

~~~html
<script>
	var max = arr[][];
	for(var i = 0;i < arr3.length;i++){
  		for(var j = 0;j < arr3[i].length;i++){
  			if(max < arr3[i][j]){}
		}
	}
  //二维数组
	var arr = [[1,3,5],[5,735,32],[32,62,2]];
	var max = arr[0][0];
	for(var i = 0;i < arr.length;i++){
		for(var j = 0;j < arr[i].length;j++){
			if(arr[i][j] > max){
				max = arr[i][j];
			}
		}
	}
	console.log(max);
</script>
~~~

#### 浅拷贝和深拷贝

> 浅拷贝：传地址，会改变。指向的是赋值对象的引用。
>
> 深拷贝：传值，不会改变。指向的是赋值对象所有引用对象进行引用的全部赋值。
>
> ~~~html
> <script>
> //二维数组：浅拷贝
> 	var arr = [1,3,5];
> 	var newArr = arr;
> 	console.log(newArr);
> 	newArr[2] = 8;
> 	console.log(newArr);
> 	console.log(arr);
>
> //二维数组：深拷贝
> 	var arr1 = [1,3,5];
> 	var newArr1 = [];
> 	for(var i = 0;i <arr1.length;i++){
> 		newArr1[newArr1.length] = arr1[i]; 
> 	}
> 	console.log(newArr1);
> </script>
> ~~~

### 函数

#### 一、函数

> 函数就是将能够实现某一特定功能的代码块封装起来，方便重复调用。

#### 二、特点

> 特许会更加简洁，维护起来会更容易

#### 三、函数声明（三种方式）

##### 1.通过关键字

~~~html
<script>
	function 函数名([参数1],[参数2],[参数3]...){
  		函数体;
	}
</script>
~~~

~~~html
<script>
	function al(){
  		alert(1);
	}
  
  	function tx(){
  		document.write('<h1>你好</h1>');
	}
</script>
~~~

##### 2.通过字面量的方式

~~~html
<script>
  	var 变量名 = function([参数1],[参数2],[参数3]...){
  		函数体;
	}
</script>
~~~

~~~html
<script>
	var al =function(){alert(1)};	
    var al =function(){document.write('<h1>你好</h1>'};
</script>
~~~

##### 3.通过实例化对象的方式

~~~html
<script>
  	var 变量名 = new Function();
</script>
~~~

#### 四、函数调用

##### 1.函数名/变量名 + ()

~~~html
al();
tx();
~~~

##### 2.函数自调用：

(函数)();

> **注意：**  函数自调用的时候，无论之前是什么，必须加分号
>
> 

##### 3.在事件之后调用

> 只需要写函数名

~~~html
<body>
	<div>点击事件</div>
</body>
<script>
  	function al(){
  		alert(1);
	}
    var div = document.queryAlector('div');
    div.onlick = al;
</script>
~~~

#### 五、注意事项

> * 函数名重复会发生覆盖
> * 函数自调用时要加分号
> * 通过关键字声明的函数可以在声明之前进行访问【预解析:碰见var、function会提前解析】；而通过字面量声明的函数只有在解析到它的时候，才会进行赋值
> * 预解析顺序  见函数十六
> * 代码从上到下一条语句一条语句解析执行。多个script块之间由于解析环境一样，它们之间相互影响，调用不同块之间函数需要注意：一定要先声明再调用。

#### 六、参数

##### 1.形参

> 声明函数时小括号里传的是参数
>
> 作用：接受实参

##### 2.实参

> 调用函数时小括号里传的是参数
>
> 作用：传递给形参

##### 3.概念、作用

> 动态改变函数体内对应的数据类型与值

~~~html
function all(num){
  alert(num);
}

var txt = function(txt){
  	document.write('<h1> + txt + </h1>');
}

function al(num，num1){
  console.log(num,num1);
}

all('字符串');
txt('实参');
al(2,3);
al();
al(23,65,432,64,21);
~~~

#### 七、有关参数的个数

> * 实参和形参一一对应
> * 实参个数 < 形参：多余的形参返回undefined
> * 实参个数 >  形参：只返回形参相对应的值
>
> ~~~html
> function al(num，num1){
> console.log(num,num1);
> }
> al(2,3);
> al();
> al(23,65,432,64,21);
> ~~~

#### 八、多余实参的接收

##### 1.reset参数

reset接受剩余参数的时候，作为一个数组进行处理，本质是一个数组。

**注意：** 形参...reset是运算符   

~~~html
<script>
  function al(num，num1,...reset){
  	console.log(num,num1,reset);
  }
  function al(num，num1,...reset){
 	console.log(num,num1,reset);
	for(var i = 0;i < reset.length;i++){
   		console.log(reset[i]);
	}
  }
  al(23,56,74,34,234,32,94);
</script>
~~~

##### 2.arguments对象

当我们创建一个函数时，默认会创建一个arguments对象。

在arguments对象身上，保存了所有参数的信息。

argunments.callee指向函数自身

属性、方法：length、c

~~~html
<script>
  function al(){
  	console.log(arguments);
  }
  
  function al(num,num1){
  	console.log(num,num1,arguments[2],arguments[3],arguments[4]);
  }
  
  al(23,56,74,34,234,32,94);
</script>
~~~

#### 九、默认参数

##### 1.直接在形参后进行设置

**注意：** 默认参数位置一定放在最后，要不然参数会进行一一对应，出现覆盖

~~~html
<script>
  function al(num=29){
  	console.log(num);
  }
  al();
  
  function al(num=29,num1){
  console.log(num,num1);
  }
  al(23);   23 undefined
  
  function al(num,num1=29){
  console.log(num,num1);
  }
  al(23);   23 29
</script>
~~~

##### 2.通过三元运算符

条件表达式?为真的值:为假的值;

~~~html
<script>
  function al(num){
    num ===undefined?20:num;
  	console.log(num);
  }
  al();
</script>
~~~

##### 3.逻辑或||

~~~html
<script>
  function al(num){
    num = num || 30;
  	console.log(num);
  }
  al('sdsd');
</script>
~~~

#### 十、返回值

##### return

* ###### 在函数调用的地方，返回一个值

  **注意：** (1)如果return后没有值，则返回undefined；

​                    (2)return只返回一个值，如果在return后跟多个值，会发生覆盖，最后返回最后一个值

​                    (3)一个return中有多个语句，但只返回一条语句

​			停止return之后的语句

* ###### 终止函数执行，return之后的语句都将不再执行

~~~html
<script>
  function al(num,num1){
    var sum = num + num1;
    return sum;
  }
  console.log(al('20,3'));
  
  
  function jia(num,num1){
    var sum = num + num1;
    return sum;
  }
  function jian(num,num1){
    var sum = num - num1;
    return sum;
  }
  console.log(jian(jia('20,3'),6));  17
  
  
  function jia(num,num1){
    var sum = num + num1;
    return sum;
  }
  function jian(num,num1){
    var sum = num - num1;
    return;
  }
  console.log(jian(jia('20,3'),6));  undefined
  
  
  function jia(num,num1){
    var sum = num + num1;
    return sum;
  }
  function jian(num,num1){
    var sum = num - num1;
    return num,sum,num1;
  }
  console.log(jian(jia('20,3'),6));    6
  
  
  function jia3(num,fn){
    var sum = num + fn;
    return;
  }
  console.log(65,jia(3,6));
</script>
~~~

#### 十一、作用域

##### 环境：

> 宿主环境：浏览器
>
> 执行环境：决定了变量和函数的访问权限
>
> * 全局环境
> * 函数环境

##### 作用域：

>  有关变量和函数的访问范围
>
>  分类：
>
>  * 全局变量（全局作用域）：在任何地方都可以访问的变量
>  * 通过关键字var声明的变量【在全局环境】   <1>
>  * 在函数之外通过var声明的变量   <2>
>  * <1>+<2>  可合并为：在函数外部声明的变量
>  * 没有通过关键字声明的变量并且同时赋值【全局变量】    <3>
>  * window对象，window.name,window.top,window.local也拥有全局作用域
>
>
>  * 局部变量（局部作用域）：在规定的代码块内能够访问的变量（函数中的形参、var声明变量）
>  * 块级作用域（用{}括起来的）：es6（'use strict'声明环境es6） if switch for 
>  * 作用域链：作用域链的存在造成了闭包函数的产生

~~~html
<script>
  var a = 10;   //全局变量   <1>
  function aa(){
  	var b = 20;   //局部变量
  	c = 30;    //全局变量     <3>
  	function bb(){
  		var d = 40;  //局部变量
  		console.log('这是函数bb' + b);    <2>
  	}
  	bb();
  	console.log('这是函数bb' + b);
  	console.log('这是函数aa' + c);
  }
  aa();
  console.log('这是函数a' + a);
    
    
    'use strict'   //es6严格模式
    let i = 10;
    console.log(i);
    function aa(){
  		alert(1);
	}
</script>
~~~

#### 十二、闭包函数

- 闭包函数（一般在有局部变量的时候用）

- 函数作用域作用域链，在函数中的变量保存在对应的作用域中，这样的特性，称为闭包。函数中存在作用域链，函数中的变量全部保存在作用域链中，这样的特性，称为闭包。（在函数中再嵌套一个函数，当我们调用这个函数时，就行成能了闭包。）

- 作用：保存局部变量；在函数外部访问局部变量。

  ~~~html
  <script>
  	//闭包函数
    function aa(){
    	var a = 10;
    	function bb(){
    		return a;
    	}
    	return bb;
    }
    console.log(aa());
    var c = aa();
    console.log(c());
  </script>
  ~~~

  ​

#### 十三、回调函数

##### 概念：

把一个函数的指针（直接写函数名），作为参数传递给另一个函数，这个函数就叫回调函数。

##### 传参方式：

###### 1.通过函数的指针

###### 2.把整个函数传进去

~~~html
<script>
  function jia(num,num1){
  return num + num1;
  }
  function jian(num,num1){
  return num - num1;
  }
  function math(num fn){
  	return num * fn
  }
  console.log(marth(23,jia(12,43)));
  math(3,function jian()){
  	return 33 - 3;
  }
</script>
~~~

#### 十四、递归函数

在函数内部直接调用自己或者间接调用自身

**注意：** 如果逻辑处理不当，就会造成无限地柜，从而引起堆栈溢出，且每个地柜函数里必定会有终止条件。

阶乘：n! = n * (n-1)!

~~~
0！ = 1;
1! = 1 * 1
2! = 2 * 1
3! = 3 * 2 * 1
~~~

~~~html
<script>
  	function dg(num){
		if(num < 0){
			return false;
		}else if(num == 0 || num == 1){
			return 1;
		}else{
			return num * dg(num-1);
          	//return num * argyments.callee(num - 1);
		}
	}
	console.log(dg(4));   24
</script>
~~~

~~~html
月：  0  1  2  3  4  5  6   7
兔对：1  1  2  3  5  8  13  15
<script>
	function tu(num){
  		if(num == 0 || num == 1){
  			return 1;
		}else{
  			return arguments.callee(num-1) + argunments.callee(num-2);
		}
	}
  	consloe.log(tu());
</script>
~~~

#### 十五、模拟函数重载（arguments）

* 概念：同一个函数因为传入的参数的类型或个数不同，可以对应多个函数的实现，而且每种实现对应一个函数体

  ​


* 重载函数常用来实现功能类型而所处理的数据类型不同的问题。

#### 十六、预解析顺序

1.按照<script></script> 块来解析，有多个 <script></script> 对时，按块解析，先解析第一个 <script></script> 中的代码

2.按环境来解析

3.遇到关键字var和function时（即以关键字创建的函数），提前解析到内存中（相对应的环境里）。即可在声明前调用。

4.若还有 <script></script> ，在按照上面的顺序进行解析

#### 十七、内置顶层函数

##### 1.概念

内置顶层函数就是，ECM。

内置：ECMAScript   顶层：页面中任何地方都可以调用

##### 2.编码解码

* escape();对字符串进行编码

对非字母、数字、特殊标点符号（@ + - . / * 。 ）的字符串进行编码，最终得到十六进制的转义序列。也就是将机器不识别的编码方式以识别的。

* unescape(str);对编码的字符串解码

  ~~~html
  <script>
    console.log(escape('WUIF1709班级'));            字符串编码
    console.log(unescape(WUIF1709%u73ED%u7EA7));    字符串解码
  </script>
  ~~~

##### 3.有关数据类型转换的：

###### （1）Number();将任何数据类型转换为数值类型

如果是布尔值，true为1，false为0；

如果是数值，转换为本身，会将无意义的后导零与前导零去掉；

如果为null，转换为0；

如果是undefined，转换为NaN not a number；

如果是字符串：

* 如果是字符串中只有数字，则转换为数字（10进制）会忽略前导零和后导零；
* 如果是规范的浮点数，则转换为浮点数，会忽略前导零和后导零
* 如果是空字符串或为空，会转换为0；
* 如果是其他值，转换为NaN

~~~html
<script>
  var a = Number(null);     //清空对象时会用null
  var a = Number(undefined);
  var a = Number(23);   var a = Number(023);   var a = Number (23.0);
  var a = Number('aaa');    //比较时才会进行隐式转化为ascall码值
  var a = Number(true);     //true > 0,     true
  console.log(a);
 
</script>
~~~

###### （2）parseInt();将任何数据类型转换为整数

如果一个字符串中只包含数字，转换为十进制数；

如果有多个空格，会先找到第一个非空的值进行转换，直到非数值时结束；【字符串类型】

**如果第一个值不是以数字、空格开头的，一定转换为NaN；** 

有两个参数是，第一个参数表示要转换的值，第二个参数表示几进制，返回值是一个十进制的数字；

* 第一个参数从最高位开始计算，只要有一位数可以识别为第二个参数传入的进制，则可以实现转化；

* 第二个参数可以传入的值为2-36；

  ~~~html
  <script>
    var a = parseInt(3434,16);    如果符合进制规范转换成十进制，不符合规范输出NaN
    console.log(a);
    
    var b = parseInt('  34 a');
  </script>
  ~~~

###### （3）parseFloat();将任何数据类型转换为浮点数并返回

只有一个点起作用，其他无效；

如果字符串是一个有效的整数，他返回的是整数，不会返回浮点数；

###### （4）String();将任何数据类型转换为字符串

如果是null，undefined，转换为字符串“null”“undefined”；

如果是数值类型，转换为本身的字符串，123转换为“123”；

如果是布尔类型，true为“true”，false为”false“。

###### （5）Boolean();把任何数据类型转换为布尔型

**转换为假：""（空串），null，undefined，0，false，NaN；** 其他都为真。

###### （6）isNaN();

判断一个数据能否转换为数值；

如果能转换成数值返回假，不能返回为真。

###### （7）eval();

将符合js语法规范的 **字符串**转换成 **JavaScript命令** 执行**（必须在一行）** 

~~~html
<script>
  var a = Boolean(0);
  eval('console.log(a);alert(2)');
</script>
~~~

###### （8）toString();

将对象以字符串的方式来表示，都是通过对象的方式来调用的

> 格式：对象.toString();

* 数组 分割的字符串

* 布尔

* 字符串（还是本身）

* 数值类型

* null与undefined没有toString()方法

  ~~~html
  <script>
    var a = [1,2,3];
    eval(a.toString());
    
    var b = 6;
    eval(b.toString());
  </script>
  ~~~


#### 十八、构造函数与函数的区别

>  构造函数首字母大写

#### 十九、封装函数

~~~html
<script>
	四则运算
  //   function a(num1,num2,num){       
  //   switch(num){
  //    case "+":console.log(`${num1}+${num2}=(${num1+num2})`);
  //    break;
  //    case "-":console.log(`${num1}-${num2}=(${num1-num2})`);
  //    break;
  //    case "*":console.log(`${num1}*${num2}=(${num1*num2})`);
  //    break;
  //    case "/":console.log(`${num1}/${num2}=(${num1/num2})`);
  //    break;
  //    case "%":console.log(`${num1}%${num2}=(${num1%num2})`);
  //    break;
  //   }     
  // }
  // a(2,2,'%');
</script>

<script>
	 // 99乘法表
  //  function a(num){
  //  for(var i = 1;i<num;i++){
  //   for(var j = 1;j <= i;j++){
  //     document.write(`${i} * ${j} = ${i*j}`);
  //     document.write(`&nbsp;`)
  //   }
  //   document.write(`<br>`);     
  //  }
  // }
  //  a(20);    
</script>

<script>
	金字塔
  // function a(num){       
  // for(var i =0;i < num;i++){
  //     for(var j = 0;j < num-1 - i;j++){
  //       document.write('&nbsp;');
  //     }
  //    for(var k =0;k < i + 1;k++){
  //      document.write('*&nbsp;');
  //     }
  //     document.write('<br>');
  //    }
  //   }  
  //   a(6); 
</script>

<script>
	               // 十乘十表格
   //  function a(num){              
   //   var tab= '<table width="600px" height="600px" border="1px" cellspacing="0">';
   //   for(var i = 0;i < num;i++){
   //    tab += '<tr>';
   //    for(var j = 0;j < num;j++){
   //    tab += '<th> </th>';
   //  }
   //  tab += '</tr>'; 
   // }
   // tab += '</table>';
   // document.write(tab);
   // }
   // a(6);
</script>

<script>
	// 数组去空
  /*function a(d){
    var c =[];
    for(b = 0; b < d.length;b++){
      if (d[b] != undefined){
        c[c.length]=d[b];
      }
    }
    console.log(c);
  }
  var d=[2,3,,5,,7,,,9,10,,]; 
  a(d);
</script>

<script>
	// 封装数组求最大值
  /*function a(d){
    max = d[0];
    for(var b = 0;b < d.length;b++){
      if(max < d[b]){
        max = d[b];
      }
    }
    console.log(max);
  }
  var d = [3,8,1,6,9,10,5];
  a(d);*/
</script>

<script>
	/* 封装数组求最小值*/
  /*function a(d){
    min = d[0];
    for(var b = 0;b < d.length;b++){
      if(min > d[b]){
        min = d[b];
      }
    }
    console.log(min);
  }
  var d = [5,3,8,2,6,9,10,5];
  a(d);*/
</script>

<script>
	// 封装数组平均值
  /*var a =function (d){
    sum = 0;
    for(var b = 0; b < d.length;b++){
      sum = sum + d[b];  
    }
    var sum1 = sum /= d.length;
    console.log(sum1);
    
  }
  var d =[5,2,3,5,5]
  a(d);*/
</script>

<script>
	// 封装数组从大到小排
  
  /*var a = function (d){
    for(var b = 0;b < d.length;b++){
      for(var c = b+1; c < d.length;c++){
        if( d[b] < d[c]){
          var e;
          e = d[b];
          d[b] = d[c];
          d[c] = e;
        }
      }
    }
    console.log(d);
  }
  var d = [5,3,8,2,6,9,10,5];
  a(d);*/
</script>

<script>
	 // 封装数组从小到大排
  
  /*var a = function (d){
    for(var b = 0;b < d.length;b++){
      for(var c = b+1; c < d.length;c++){
        if( d[b] > d[c]){
          var e;
          e = d[b];
          d[b] = d[c];
          d[c] = e;
        }
      }
    }
    console.log(d);
  }


  var d = [5,3,8,2,6,9,10,5];
  a(d);*/
</script>

<script>
	// 封装数组筛选数据类型
	function SX(arr){
    	for(var i = 0; i < arr.length; i++) {
    		if(typeof arr[i] == 'number') {
        	console.log("arr数组中是Number类型的有：" + arr[i]);
    		}
   		}
	}
	SX([18,,24,'a',68,36,152])
</script>

<script>
	// 封装大于0的数
  /*function a(d){
    var c =[];
    for(var b = 0; b < d.length;b++){
      if( d[b] > 0){
        c[c.length] = d[b];
      }
    }
    console.log(c);
  }
  var d = [5,3,-8,2,-1,9,-5,-5];
  a(d);
*/
</script>

<script>
	// 封装数组元素扩大2倍
  /*function a(d){
    var c = [];
    for(var b = 0; b < d.length;b++){
      c[c.length] = d[b] *2 
    }
    console.log(c);
  }
  var d = [5,3,-8,2,-1,9,-5,-5];
  a(d);*/
</script>

<script>
	// 反向输出数组中的各个元素
  /*function a(d){
    var c =[];
    for(var b = d.length-1; b >= 0; b--){
      c[c.length] = d[b];
    }
    console.log(c);
  }
  var d =[1,2,3,4,5,6];
  a(d);*/
</script>

<script>
	// 数组合并
  /*function a(d,e){
    for(var b = 0; b < e.length;b++){
      d[d.length] = e[b];
    }
    console.log(d);
  }
  var d =[1,2,3,4,5];
  var e =[6,7,8,9,10];function aa(){
        return rr;
      }
  a(d,e);*/
  // function jc(num){
  //   if(num < 0){
  //     return false;
  //   }else if(num == 0 || num == 1){
  //     return 1;
  //   }else{
  //     return num * arguments.callee(num-1);
  //   }
  // }
  // console.log(jc());
</script>

<script>
	// 找出数组中是否包含某个元素，包含返回true，不包含返回false
   //var arr = [342,'df',456,8,9,2];
 //   var num = 8;
 //   function contain(arr,num){
 //       for(var i = 0;i < arr.length;i++){
 //           if(arr[i] == num){
 //                return true;
 //           }
 //       }
 //       return false;
 //  }
 //   console.log(contain(arr,num));
</script>

<script>
	//数组查找，查找数组中是否包含a元素，包含则返回此元素的下标，不包含则返回-1
	// function Index(arr,num){
  //      for(var i = 0;i < arr.length;i++){
  //          if(arr[i] == num){
  //               return i;
  //          }
  //      }
  //      return -1;
  // }
  //  console.log(contain(arr,num));
</script>

<script>
	//将数组转换为字符串，默认用-链接
	// function link(arr){
 //     var newArr = '';
 //     for(var i = 0;i < arr.length;i++){
 //         str = str + arr[i] + '-';
 //     }else{
 //         str = str + arr[i] + '-';
 //     }
 //     return str;
 // }
 // console.log(link(arr));
</script>

<script>
	//实现数组元素去重
   //  function qc(arr){
 //      var newArr [];      
 //      for(var i = 0;i <  arr.length;i++){
 //          var flag = true;
 //          for(var j = i+1;j < arr.length;j++){
 //              if(arr[i] !== arr[j]){
 //                  flag = false;
 //              }
 //          }
 //          if(flag == true){
 //               newArr[newArr.length] = arr[i];
 //          }
 //      }
 //      return newArr;
 //  }
 //  console.log(qc(arr));
</script>
~~~



### 对象

#### 一、对象

面向过程：按照流程一步一步进行操作

面向对象：不管中间环节具体实现，只要结果

对象：一切皆对象，即对象指的就是人们所能接触到的所有的事物，有抽象的，也有具体的。

​	对象：是属性和行为的无序集合。

​		属性：描述对象特征的数据

​		行为：操作对象方法的数据

​	类：具有相同属性和行为的对象的抽象。

​	类是对象的抽象，对象是类的实例化。

#### 二、声明一个对象

1、实例化

2、字面量

3、构造函数（通过构造函数来实现类）**注意：** 必须结合new

~~~html
<script>
实例化：
    var Preson = new Object();
字面量：
    var Preson1 = {};
构造函数：
    function Preson(){};   
  
实例化添加/访问：属性、方法
 	var lisi = new Object();
  	lisi.nwme = '李四';
  	lisi['age'] = 20;
  	lisi.sex = '男';
  	lisi.say = function(){
  		alert('会说话');
	}
    lisi.run = function(){
  		alert('会跑');
	}
    consol.log(lisi);
    consol.log(lisi['name']);
   	consol.log(lisi.age);
    consol.log(lisi['say']);
   	consol.log(lisi.run);
  
 字面量添加/访问：属性、方法
 	var lisi = {
  		name:'张三',
      	age:20,
      	sex:'男';
      	say:function(){
  			alert('speak');
		}
    	run:function(){
  			alert('run');
		}
	};
   	consol.log(lisi.run());
  
  构造函数：
  function Person(name,age){
  this.name = name;
  this.age = age;
  this.say = function(){
  		alert('说话');
	}   	
  }
  var ll = new Person('李丽',20);
  delete ll.age;   //delete删除属性和方法
  ll=null;   //清空对象
  console.log(ll);
  
</script>
~~~

#### 三、添加属性、方法

属性：对象.属性名 = 属性值

​	   对象['属性名‘] = 属性值

方法：对象.方法名 = function(){}

​	   对象['方法名‘] = function(){}

#### 四、访问属性、方法

属性：对象.属性名

​	   对象['属性名‘]

方法：对象.方法名

​	   对象['方法名‘]

#### 五、删除属性、方法

​	delete

#### 六、清空对象

​	null

#### 七、for in

对象中：i ->属性名/方法名

​		对象名[i] - 属性值/方法

数组中：i ->下标

​		数组[i] - 元素

#### 八、对象的封装（三种方式）

##### 1.概念

>  将对象的所有组成部分全部组合起来，并对部分细节进行隐蔽，使其受到保护，只留下接口和外界进行交流。

##### 2.方法

###### 2.1工厂函数

>  不推荐：即使方便维护，节省内存，但是代码不规范

~~~html
 <script> 
   function myPhone(color){
     var phone = {};
     phone.color = color;
     phone.size = 543;
     phone.cailioao = '塑料';
     phone.say = function(){
       alert('打电话');
     }
     return phone;      //不加return或只加return没有加值都只会返回undefined
   }
   let iphone1 = myPhone('red');
   console.log(iphone1);     //输出：Object {color: "red", size: 543, cailioao: "塑料"}
   
   let iphone2 = mtPhone('blue'); 
   console.log(iphone2);     //输出：Object {color: "blue", size: 543, cailioao: "塑料"}
</script>
~~~

###### 2.2构造函数

> 浪费内存，占空间

~~~html
<script> 
   function Animal(name,weight){
     	this.name = name;
     	this.weight = weight;
     	this.sing = function(){
       		alert('会唱歌');
     	}
     	this.fly = function(){
       		alert('会飞');
     	}     
   }
   var greens = new Animal('小绿',40);
   console.log(greens);
   greens.fly();
  
   var reds = new Animal('小红',50);
   console.log(reds);
</script>
~~~

###### 2.3原型

内存：栈区、堆区、代码块（原型数据保存在代码块中）、静态

* 2.3.1.概念：

  原型也是一个对象。在JS中，每一个对象都会继承另一个对象所有的属性和方法，被继承的这个对象就是原型。


* 2.3.2

  * 2.3.2.1对象：[[prototype]]

    p[[prototype]]是对象内部的一个属性，但是我们不能直接访问。FF和chrome提供了‘poto’访问器，ECM提供了Object.getPrototype(object)访问器。指向给对象的原型。

    “__proto__ ”是访问器，prototype是对象内部的一个属性

  * 2.3.3.2函数：prototype

    保存的是该函数的原型对象

    当一个函数作为构造函数来使用时，会把该函数的prototype属性作为原型赋值给所有通过该构造函数实例化的对象的原型

  * 2.3.3.3原型对象：constructor

    指向的是实例化的构造函数

    函数对象和原型对象通过prototype和constructor实现相互关联

    通过prototype可以实现代码共享：实现继承

~~~html
<script> 
   function Ani(name,weight){
     	this.name = name;
     	this.weight = weight;
    }
    Ani.prototype = {
  		sing:function(){
       		alert('会唱歌');
     	},
     	fly:function(){
      		alert('会飞');
     	}  
	}
   	var greens = new Ani('小绿',40);
   	console.log(greens);
  
   	var reds = new Ani('小红',50);
   	console.log(reds);
  

  
  	function Person(name,age){
     	this.name = name;
     	this.age = age;
      	this.say = function(){
  			document.write(`我是${this.name}`);
		}
   	}
  	var lisi = new Person('李四',50);
  	console.log(lisi);
  	console.log(lisi.__proto__);  //lisi的原型对象
  	console.log(lisi.__proto__.constructor);
  	console.log(lisi.constructor);   //lisi并没有constructor属性，会去原型链上找lisi的原型对象
  	console.log(lisi.__proto__.constructor  === lisi.constructor);
  	console.log(Person.prototype);
  	console.log(Person.prototype === lisi.__proto__); 
当一个函数作为构造函数来使用时，会把该函数的prototype属性作为原型值赋值给所有通过该构造函数实例化的对象的原型
</script>
~~~

四、构造函数结合原型

> 构造函数中一般放属性，原型中一般放方法

~~~html
<script>
	 function Ani(name,color){
     	this.name = name;
     	this.color = color;
   	}
   	Ani.prototype = {
  		sing:function(){
      		alert('会唱歌');
     	},
     	fly:function(){
       		alert('会飞');
     	},
     	aaa:{color:"red"}
	}
   	var greens = new Ani('小绿',40);
   	console.log(greens);
   	var reds = new Ani('小红',50);
  	console.log(reds);
  	reds.aaa.color = 'yellow';
  	console.log(reds.aaa.color);
  	console.log(greens.aaa.color);
</script>
~~~

