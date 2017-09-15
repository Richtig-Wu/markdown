
## 1、url打开后过程（输入url发生类什么）
   * ①进行DNC域名解释，找到对应的主机ip
   * ②在浏览器和主机之间，建立网络类连接
   * ③浏览器给主机发送http请求
   * ④服务器接收请求，并根据请求查找相关资源，并返回给浏览器结果
   * ⑤浏览器接受服务器接受的响应，根据响应内容进行渲染，将网页显示在浏览器中

2、语义化的意思和用处(语义化定义和手段)
①语义化：就是根据网页的内容和结构，选择对应的语义化标签。可以使页面在没有css的情况下
仍然能做到结构清晰，组织有序，偏于搜索引擎优化，有利于其他设备进行解析。
②手段：尽量选择语义化的标签

3、描述优先css算法、掌握css属性
CSS优先级：important》style》  id》class》标签》继承》浏览器的默认值
混合使用：css的优先级 默认为0
出现一次id+100;class+10;标签+1;
	 优先级相同：后来据上
4、块元素、行元素
^
嵌套基本原则：块级元素可以包含行元素，但是行元素不能包含块级元素
块级元素之间的嵌套大部分是可以的

交集选择器：选择器同时满足多个条件，可以精确的改变元素的样式
例：
div.p{}
div#id{}
并集选择器：选择器以逗号作为分隔符

伪类：{ Link：标签原本的样式
	hover：鼠标悬停的样式
	visited:标签被访问后的样式
	active：鼠标点击时}
style：样式标签嵌套样式   
	行内样式：  
	引用外部样式表：<link rel="stylesheet" href="css路径" type="text/css">




day03
1、搞清楚进制


line-height:1.5 <1.5没有单位，表示一个行高因子。后代元素只会继承该行高因子，不会继承祖先的行高>


day06
1、什么是精灵图
  答：由多张小图组成的图片
2、为什么要用精灵图
  答：减少http请求，降低服务端的压力，提高用户的体验

day07
1、选择器的解析使从样式右边开始解译
2、z-index的设置必须有定位的情况下才生效（如：position）层级
3、opacity:(0-1)：设整个元素的透明度   加上postion:fixed;(固定在可视窗口上)

outline:none (取消点击input时的边框)

isply:block;显示  none:让元素彻底消失，不占用任何页面位置（没有该节点）
opacity:应用到整个元素，元素后代都会受到影响（无法改变）
background:rgba(xxx,xxx,xxx,0.5);:只会影响选中的元素，不会影响父类
～～～～～～～～～～～～～～～～～～～～～
js

标识符：
1、第一个字符必须使字母、下划线或$。
2、不推荐使用符号
3、建议用驼峰法
4、标识符不允许和关键字相同


typeof：关键字测试变量的数据类型。（永远都不会报错）
typeof NaN:得出的值为number
函数：不依赖与对象的独立集合
方法：依赖于对象的集合
07day问题
js的数据类型有哪些？？
全局作用域和局部作用域的区分？？
函数的声明提升？？
进制写法和科学技术法？？
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
!--jQuery--!什么是jQuery??
jQuery:一个高效、精简并功能丰富的js工具库.提供的API易于使用兼容众多浏览器.


jQuery的优点是什么??jQuery能干什么??
1:简化js任务（DOM操作、AJAX调用和事件处理）;
2:快速获取文档元素
3:创建AJAX无刷新网页
4:提供对javascript语言的增强
5:增强事件处理
6:修改页面内容
7、提供页面动态效果													
注 意 ： 外部js要单独引用和使用,不能嵌套



DOM/元素/标签/节点  基本可以认为一样
！！DOM操作：！！
1.创建标签：$("<标签名>")
内部添加方法:append;（在目标里面最后一个元素后面添加）
	    preoend;(在目标里面最前一个元素前面添加）
	    .html(可以改面页面的内容)
	    .text（可以改变文本内容）
外部添加方法：after;(在目标外面指定位置添加).

删除：remover(不添加指定目标则全部清除;有则清除指定目标内所有内容)
	empty(可以删除所有内容，但能保存删除的内容供以后使用)
$("div").remove(li.eq(1));



函数声明的提升！！！！？？？
函数声明语句会被提升到外部函数作用域的顶部

变量声明提升！！！！？？？
变量的声明被提升到当前作用域的顶部，但赋值并没有提升
注意： 变量和函数同名时：
			变量没有赋值时，变量在最顶部，显示函数结果；
 			变量有赋值，函数在最顶部，显示变量结果



～～～ js基础进阶 ～～～
一、
遍历：  var e = new Array(10)
	  for (var i = 0; i < e.length; i++) {
		e[i] = i;
		console.log(e[i]);
	      }
1、push()方法将一个或多个元素添加到数组的末尾，并返回添加后的长度
例：<变量>.push();
2、pop()方法从数组中删除最后一个元素，并返回删除的值
例：<变量>.pop();
3、unshift()方法将一个或多个元素添加到数组的开头，并返回添加元素后的长度
例：<变量>.unshift([元素或数组])；
4、shift（）方法从数组中删除第一个元素，并返回删除元素的值
例：<变量>.shift();
5、join()方法将数组(或一个类数组对象)的所有元素连接到一个字符串中
例：<变量>.join(["连接符号"]);
6、reverse()方法将数组中元素的位置颠倒
例：<变量>.reverse();
7、sort()方法会默认按照字符编码进行排序，并返会数组
   sort(compareFunction)指定顺序进行排列
例：  var e = [10, 20, 3, 4, 22];
      function compareFunction(a, b)
	{ return a - b;//升序  }
      e.sort(compareFunction);
      console.log(e);
8、concat()方法用于合并两个或多个数组。合并后不会改变原有数组，会返会一个新数组
例：var nums = num1.concat(num2, num3, 10, 11, 12);
9、slice()方法返会一个从开始到结束(不包括结束)选择的数组的一部分浅拷贝到一个新数组对象，原始数组会被修改。如果参数为负数，则表示他在原数组的倒数第几个元素结束抽取。
9.1、深拷贝指的是对象属性所引用的对象全部进行新建对象复制，以保证深复制的对象的引用图不包含任何原有对象或对象图上的任何对象，隔离出两个完全不同的对象图。

10、splice()方法通过删除现有元素和/或添加新元素来更改一个数组的内容。
例：  var removed = myFish.splice([添加的位置], [移除的索引], "[添加的内容]");
11、forEach()方法对数组的每个元素执行一次提供的函数。
 例：array.forEach([当前值],[索引])
12、map()方法创建一个新数组，其结果是该数组中的每个元素都调用一个提供的函数后返回的结果
例：var b = [1, 2, 3, 4, 5];
      var ret = b.map(function(elem, index, array) {
	  return elem * elem;
	      });
	  console.log(ret);
13、filter() 方法创建一个新数组, 其包含通过所提供函数实现的测试的所有元素。（过滤）
例：b = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
      ret = b.filter(function(elem, index, array) {
         return   elem % 2 === 0 ? true : false;  });
      	 console.log(ret);
14、reduce() 方法对累加器和数组中的每个元素 (从左到右)应用一个函数，将其减少为单个值。
例：array.reduce(function(prev, 元素, 索引, array), <初始值>)//reduce的回调函数必须有返回值，该值会作为下一次prev
15、indexOf()方法返回在数组中可以找到一个给定元素的第一个索引，如果不存在，则返回-1。
例：  b = ['hello', 'world', 'abc', 'abc', 'efg', 'ghgjgjkgj', "skgjkjg"];
      ret = b.indexOf('abc', 3);
      console.log(ret);

～～～～～～原生代码～～～～～～～
DOM0的事件添加方式： DOM0 无法指定多个处理函数(移除处理函数:(对象).(事件)=null)
DOM2级的事件处理方式（事件冒泡：事件由内向外进行传递、 事件捕获：事件由外向内传递!!!!!）
1、添加移除事件：
 标准版本：
添加：addEventListener('<事件>',函数名,布尔类型);
移除：removeEventListener('<事件>',函数名,布尔类型);
停止事件传播:stopProPagation();
阻止默认事件：preventDefault();
tihs:注册该事件处理函数的元素
currentTarget:等价于this
target:触发事件的源头元素
 兼容版本(ie)：
添加：attachEvent()
移除：datachEvent()
2、获取坐标：
 整个页面：pageX、pageY
 整个屏幕：screenX、screenY
 浏览器可视窗口：clientX、clientY
3、鼠标和键盘事件
  console.log("click",e.button); （e.button可以知道那个键被按下）
  contextmenu：鼠标右键被点击时事件被触发(显示菜单之前)
  keyup(mouseup)：当松开按键时，keyup事件被触发
  keydown(mousedown)：当按下按键时，keydown事件被触发
  keypress:当一个键按下事件被触发，该事件通常产生一个字符值
~~~~~day24~~~~~
1、ie事件对象:
   ①console.log(window);(window就是在浏览器端的javascript中的全局变量)
   ②ie中的事件对象是window.event，不需要给处理函数传递
 var event = window.event;
   ③阻止事件传播：even.cancelBubble=true;
   ④阻止默认行为：window.event.returnValue  = false;
   ⑤alert(window.event.srcElement);//和event.target的作用一样
2、兼容event对象(判断浏览器是标准版本还是兼容IE版本)
   	 btn.onclick = function  (e) {
var event = e || window.event;
   };

3、使用原生方法添加单击事件
for（var i=0 ; i<lists.length; i++){
方法一：lists[i].onclick = function(){
       			 console.log(i);
    			  }
  	方法二：(function(i){
        lists[i].onclick = function(){
         console.log(i); }   
   })(i);
  方法三：lists[i].index = i;
         lists[i].onclick = function(){
          console.log(this.index);
      }
}
4、节点
标签：btn.nodeType					文本:btn.nodeName
文档：document.nodetype;
5、节点查询
①在整个文档或指定范围中查找
document.getElementByTagName("div");
②在整个文档中查找
document.geiElementsByClassName("f");
③在指定范围中查找(指定位置)
content.getElementsByClassName("f");
6、节点操作
①找到父节点
son.parentNode
②获得下一个节点，只包含元素，文本也算
son.nextSibling
③获得下一个节点，只包含元素，文本不算
son.nextElementSibling / son.previousElementSibling
④查找子节点
包括空格和换行：ID第一个子节点：box1.firstChild			ID最后一个子节点：box1.lastChild
不包括空格和换行：			  firstElementChild			lastElementChild
⑤获得所有的子节点
id.childNodes  / id.childNodes[num]
⑥创建一个新节点：var node1 = document.createElement("<div>");
        添 加 节 点    ：xxx.appendChild(node1);
   var node2 = document.createElement("h1");
xxx.insertBefgore(node2,son); (第二个参数为null等价于appendChild)		
 删  除 节  点   ：var oldChild = id.removeChild(id,lastElementChild);
 替  换  节 点   ：id.replaceChild(oldChild,id.firstElementChild);
7、节点特性
var box  = document.getElementById("box");
①获得特性：box.getAttribute("id");
②设置特性：box.setAttribute("hello","world");
③删除特性：removeAttribute("hello");
8、原生方法操作css
var box = document.grtElementById("box");
综合设置:box.style.cssText = "color:pink";
 box.style.border = " 1px solid red";
df//使用.去访问叫属性  //id,class叫特性
box.id  /  box.className
box.className  =  "color-red big-siza";(样式类)
9、节点的克隆
var one  = document.getElementsByClassName('list')[0];
var two  =  one.cloneNode(teue);
document.body.appendChild(two);

~~~~~~~~~~day25~~~~~~~~~~
1、jQuery对象和DOM对象的转换
①jquery对象：var jq.Box   =  $("#box")
②DOM对象：var domBox  =  		document.getElementById("box")
③转换
dom   =====>  jquery  ： $(domBox).css("color" , "red");
jquery  =====>   dom  ：console.log(jqBox[0]);///.get(0)
2、string字符串
①字符串的定义方法：
var str = 'hellow';
var newStr = new String("hellow");
②字符串的各种方法：
1）获取字符串相应位置：charAt(index)
2）获取相应位置字符的编码：charCodeAt(index)
1)查找子串,返回第一次出现的位置 : str2.indexOf("google");
2)字符拼接 :  srt1.concat(str2);
3)切片  :  var  str4 = "red blue yellow".slice(0,10); 或 ------.substr(0,10);
4)将start , end调换位置  : .substring(10,1);
5)大小写转换 : .toLowerCase (大写--->小写 ) .toUpperCase(小写-->大写)
③字符串分割  :  var arr  =  " hello , world  , google  ,  android ".split(" , " , 2);
3、间隔定时器setInterval
定时器中的代码都会先放到事件执行队列中，之后到达队头时该代码才会执行。setInterval的功能是间隔一定时间之后将代码添加到队列中（重复添加）
例：var id1 ；
id1 = setInterval(function()){
console.log("填写需要重复的代码")//异步代码
}，1000）；
console.log("id1 = " , id);     //同步代码
取消间隔定时器：clearInterval(id1);
4、超时定时器setTimeout
①setTimeout在时间到达之后，只会执行一次，除非手动调用
例：var id1；
function start（）{...
(该代码可以保证只有以上代码执行完毕之后，才会向队列中添加下一次)
id1 = setTimeout(start,1000);  
}
②取消超时定时器：clearTimeout(id1);
③严格模式：'use strict';
例： 方法一： setTimeout(function handler() {
      console.log("调用匿名函数 xxxx");
      setTimeout(handler, 1000);
    }, 1000);   // handler();//定义在定时器中的局部函数，全局没有
  方法二：//arguments.callee就是函数本身,严格模式不让用
setTimeout(arguments.callee, 1000);
5、使用console测试代码的运行时间
例：  console.time("start");
      for (var i = 0; i < 10000; i++) {
        console.log(i);
      }
    console.timeEnd("start");
6、 1）获得时间
①年：.getFullYear(); ②月：.getMonth()+1  ③日：.getDate()  ④时： .getHours()
⑤分0：.getMinutes();  ⑥秒： .getSeconds()  ⑦毫秒：.getMilliseconds();  
⑧返 回累计毫秒(1970/1/1午夜起 ) ：.getTime()   ⑨星期：getDay();
   例：var d = new Date();                                                                                                                                                
2）设置时间：setFullYear(自定义年)    setMonth(从0开始自定义月)
3）格式：toTimeString()：显示时：分：秒和区时
  toDateString()：显示星期几、月、日和年
～～～～～day26～～～～～
(っ°Д °;)っ
1、闭包：有权访问另一个函数作用域中的变量的函数
①创建闭包：
在一个函数A中返回一个函数，并且返回这个函数中引用到了A函数中的变量，返回的函数就是闭包（引用到A中的a变量，那么a变量在A函数调用完毕之后不会销毁，仍然在内存中）
(全局变量容易被修改，没有办法保护;而且全局资源有限，需要尽可能减少全局变量的定义)
②闭包的优点：
1、减少全局变量的定义，实现变量的私有化
2、可以根据不同参数动态生成一些值(每个闭包都有自己的变量，相互之间没有任何关联)
     缺点：私有变量会常驻内存，直到该变量使用完毕，会增加内存消耗
2、面向对象：
定义：所有操作都是以对象为中心，围绕对象展开，对象拥有的属性和方法都是对象的附属。
特点：封装、继承、多态
①创建对象的方式：
1)使用已有的类创建						1.1)创建空对像：var obj =new Object()
    var date = new Date();  //object类型
2)直接赋值
var stu = {};
stu.age=10;//属性
stu.play = function(){};//方法
stu.play();//对象都是由key:var组成，键值对
(;´༎ຶД༎ຶ`)注意：使用.访问属性时不可以有引号，使用者[ ]访问属性使则要引号。
/*属性名加不加引号都可以 */
2.1)对象遍历: for (var pro in person){//此处用[ ]访问属性值}
/*只要使对象，就可以添加属性和方法*/
 3)自定义构造函数，通过new来创建对象，构造函数的名字首字母要大写
function Dog(type , color){
this.type = type;(;´༎ຶД༎ຶ`)创建属性
this.eat = function(){};	(;´༎ຶД༎ຶ`)创建方法}									
	/*直接调用构造函数，其中内部的this === window*/
  4)使用new关键词用构造函数时，函数中的this就是创建的对象本身。不需要return,this会自动返回this
~~~~~day27~~~~~
1、原型 prototype：
1)任何函数都有 prototype属性，而且该属性是个对象
2）想要所有对象共享的属性和方法，要在prototype上写
3)修改一个对象属性，没有影响其他对象，因为当修改和prototype同名的属性或者方法时，对象会在本身上重新添加同名属性，但是保留prototype，但是访问的时候自己属性优先级高于prototype。
4)直接修改构造函数上的prototype，会影响其他所有的对象
 	    任何对象都有__proto__属性，该属性指向自己的构造函数的prototype
例：one.__proto__.mao = false
5)①直接给prototype赋值就是添加自己的属性；②直接在已有的基础上修改，修改的是原型
例：原：aaa.prototype.hobby=[2,2,2]
  ①赋：one.hobby=[1,1,1]			②one.hobby.push(20);
6)constructor(构造器)：用来表示该对象使由那个构造器产生的
2、继承：原型链继承
function Person (name,age){
this.name = name;
this.age = age;
Person.prototype.aaa=function(){};
}
function Student(name,age,score){
this.name = name;
this.age = age;
this.score = score;
}
//仍然继承重复的name，age，而且将来Studen又会覆盖掉name，age吧
Student.prototype = new Person() ; //name,age,aaa 显示的构造函数是Person
//指定自己的constructor，因为上一步被覆盖了
Student.prototype.constuctor = Student;//显示的构造函数是Student
/*原型链继承的问题：继承了原型上的方法，但是同时也继承了Person对象中的属性(不需要的属性)*/
3、继承：借用构造函数实现继承
借用Person构造函数，只能继承构造函数内部的属性，但是原型的属性和方法无法实现继承
function Student (name,age,score){
Person.call(this.name,age);
this.score = score;
}
4、apply、call方法
var value = 0;
function fun() {
}
fun();
//直接调用时，fun内部的this === window  , 所以this.value === window.value === value
/*apply指定fun函数内部的this为obj，也就是函数内部this已经变成obj对象。不是window。
call的作用就是改变函数中的this。其余的参数都是传递给fun函数*/
fun.call(obj,1,1,2,3);//使用arguments可以传递数组
fun.apply(null,[1,2,3,3]);//自动将数组拆分为单个参数   null === window
call：调用，可以传递任何参数
apply：调用，只能传递一个数组或null
5、继承：组合继承 = 原型链继承(方法)+ 借用构造函数继承(属性)
1）例：function Person (name , age){
this.name = name ;
this.age = age;
}
Person.prototype.sayHellow = function (){}
function Student (name , age , score){
Person.call(this,name,age);
this.score = score;
}
  Student.prototype = new Person();
  Student.prototype.constructor = Student;
  Student.prototype.exam = function () {
      console.log("exam ...");
    };
var one = new Student('lisi', 22, 60);
   	var two = new Student('zhangsan', 20, 68);
  	  console.log(one,two);
2）Student.prototype = Person.prototype; //此种方式会导致两个构造函数的原型一样(执行同一个内存地址)，会导致相互影响。
3）功能：实现原型链继承，并且只继承原型方法，不会继承其他
（@sup,父类构造函数/@sub,子类构造函数）
例：function inherit(sup,sub){
function Fun() {};
Fun.prototype = sup.prototype;
sud.prototype = new Fun();
sud.prototype.constructor = sub;
}
～～～～～day28～～～～～
1、json的操作(json数据本质就是js对象)
例：var stu = {
"name"："lisi", "age"：15
};
2、json序列化，将json对象变为字符串:stringify
例：var str = JSON.stringify(stu,function(k,v){
if(k === 'age') {
return v + 20;
}else
return v;
});
3、json的解析，将字符串变为json对象
例：console.log(JSON.parse(str));
注意：要解析的字符串必须使json格式的字符串//反例：console.log(JSON。parse("hello"));
4、parse可以传递第二个参数为(函数),用于对返回的对象进行修改
 例：var ret = JSON.parse(str,function(key,value){
if(key === 'age'){
return value + 10;
}else{
return value;
}
});
5、xml的解析
⑴ 例:var xmlStr =`
<rss version = '2.0'>
<naem>lisi</name>
<age>10</age>
</rss>`;
 ⑵使用jQuer.parseXML();
例：var ret = $parseXML(xmlStr);//结果使DOM对象
//获取值:①$(ret).find("name").html();
  ~~~~~~~~~~~~~~~②.eq(0).html();//eq(x)得到这的是jQuery对象
  ~~~~~~~~~~~~~~~③[0].innerHTML;//[x]得到的是Dom对象
6、原生方法解析XML(domparser/实验中的功能)
var xmlStr =`
<stu>
<naem>lisi</name>
<age>10</age>
</rstu>`;
var ret = parser.parseFromString(str,"application/xml");
console.log(ret.getElementsByTagName("name")[0].innerHTML);//原生方法解析
7、正则表达式(g:全局)
①直接赋值的方式使用/pattern/
例:var pattern = /d{2,5}/g;
②使用new构造
pattern1 =  new RegExp(/hello/,'g');
③符号:取非(没有这个值)
/[^abc]/.test("abcaaa") //false
/[^abc]/.test("1") //true
④^,$是整行匹配
/^word$/.test("helloworld")  //false
/^word$/.test("word")  //ture
/^word/.test("wordaaaa")//ture
//word$/.test("aaaword")//ture
⑤连续数字"-"(一个范围)
/[1-5]/.test("1") //ture
⑥\b 用于匹配单词边界
/\bhello\b/.test("xxxx   hello  xxxhelloyyy")
⑦元字符
/zo*/.test("z"));//true

⑧"\"表示转义字符，就是转换字符的含义
/zo\*/.test("zo*")
⑨+:匹配前面一个表达式1或者多次。等价{1，}
/a+/
⑩？:匹配0次或者1次，等价于{0，1}
⑾{}匹配一个范围（里面的数字是出现的次数）
/\d{4,5}/.test("12");false   ("12345");ture
⑿()：一个整体
⒀|：或，整体出现
⒁*:默认使贪婪匹配
*后边携带？用于最短匹配，取消贪婪匹配，进行最短匹配
8、exec使用g时，需要多次调用
例： while ((result) = re. exec(str)) ! ==null{
console.log(result);
console.log(re.lastIndex);
}
9、m标志用于多行匹配
例：rest = str.match(/^hello world hehe!$/mg);
 console.log(rest);
～～～～～day029～～～～～
1、replace(regexp | substr, newSubStr | function)
第一个参数填写正则表达式或字符串，第二个参数填写替换正则表达式能匹配的字符串或函数
例：var result = "hello xxxx".replace(/x/g , "X");
 console.log("match = ", match);//匹配值
        console.log("p1= ", p1);//捕获（必须和获得的次数一致）
      	console.log("offset = ", offset);//偏移值？？？
        console.log("str = ", str);//原来的值（result）
        return "hehe"; //替换整个正则表达式能匹配的部分
2、.toUpperCase();将匹配到的小写字母转换成大写字母（str）
.toLowerCase();将匹配到的大写字母转换成小写字母（str）
 例：ret = "xxxx".replace(/([a-z])/g , function(match , a1){
return a1.tpUpperCase();
});
3、contenteditable :用于实现文本输入区域
例:<div contenteditable = "true"></div>
4、bind()：创建一个新的函数，第一个参数使thisarg，第二个是参数序列
~~~~~~~~~day30~~~~~~~~~
1、函数柯里化：和函数绑定差不多，使用一个闭包返回一个函数，第一个参数为null
2、高阶函数：对已有的函数进行加工，返回一个具有特定功能的函数
3、定时器节流：防止代码连续不间断的运行
4、jQuery获取高度:
  $(".f").height();(内容高度) 	
  $(".f").innerHeight();(padding+content）
  $(".f").outerHeight();(border+padding+content)
  $(window).height();/$(doucument).height();(浏览器窗口高度)
5、原生js获取
 1、offset
var f = document.getElementById("f"); //获取id
var s = f.children[0]; //f子类的第一个
//行内样式设置和获得
f.style.backgroundColor = "red";
//只读属性，无法修改
f.offsetWidth(content + padding +border)
f.offsetHeight(content + padding +border)
s.offsetLeft;(获得left的距离)
s.offsetTop;(获得top的距离)
//相对于那个元素定位
s.offsetParent;
s.style.left = "300px"; 通过style 修改
2、client
f.clientWidth;(padding  + content)
f.clientHeight;(padding  + content)
document.documentElement.clientHeight;(返回文档对象根元素的只读属性)
3、window.getComputedStyle
例：var styles = window.getComputedStyle(f);
styles.height;//内容高度,content
styles.getPropertyValue("height");//内容高度,content
6、scroll用法
scrollHright:(实际内容的高度)
scrollWidth:(实际内容的宽度)
//通过父元素获得滚动条滚出的距离
例:console.log(f.scrollLeft)；
 	   console.log(f.scrollTop);
7、监听scroll的滚动
window.onscoll = function(){
var d = getScroll().top;//获得滚动条离页面顶部的距离
if(d >=200){
如果滚动条离顶部距离大于或等于200的执行代码
}
else{}
}
back.onclick = function(){
window.scrollTo(0,0);//滚动条的坐标横向不变，纵向为初始位置！！！
//方法二:document.documentElement.scrollTop = 0; (将滚动条离顶部的距离设置为0)
}


～～～～～～day31～～～～～～
canvas:h5的新标签，可通过js绘制图片（h5游戏使用较多）
特点：1、一个矩形区域的画布，可用js绘画，控制每个像素。
     2、本身不具备绘图功能。
     3、拥有多种绘制路径、矩形、圆形、字符以及添加图片的方法。
1、canvas绘制的步骤：
获得画布上下文(对象.getContext("2d")//表示当前画布支持2d)---开始绘制(brginPath)--
结束绘画(closePath())
2、重新创建起始点：moveTo(x,y）
3、绘制直线：lineTo(x,y)  /   
4、strokeStyle:设置描边颜色   /  strokey();描边
5、fill();填充 / fillStyle()="red";设置填充颜色  
fillRect(x,y,x1,y1):填充矩形xy为位置，x1y1为矩形宽高
6、重新设置宽高可以清除整个画布
7、绘制圆弧:arc(x,y,r,sAngle,eAngle,count)//xy是圆心坐标，r是半径，
s是开始弧度，e是借宿弧度，count默认false，为顺时针
8、设置线的宽度:lineWidth=num;
9、字体：font ="100px 宋体"; /  strokeText("输入文字", x,y);xy是文字位置
10、绘制图片：var img=document.getElementsByTagName('img')[0];(图片Dom对象)
img.onload =function(){ //给图片DOM对象注册onload事件，图片加载成功后触发
aaa.drawImage(img,x,y,w,h);  //w，h为宽高
}
11、设置阴影
aaa.shadowColor="颜色"		aaa.shadowOffsetX=偏移值；
aaa.shadowBlur = 0;(模糊度)	aaa.shadowOffsetY=偏移值；
12、创建线性渐变对象：var xxx=aaa.createLinearGradient(x,y,x1,y1)
//xy是起始坐标，结束的坐标
xxx.addColorStop(0, "red");//指定渐变颜色位置
注：绘制形状必须在线性渐变的坐标范围内
13、径向渐变：var xxx=aaa.createLinearGradient(x,y,x1,y1)
aaa.fillRect(x,y,x1,y1)
aaa.arc(x,y,r,s,e,false);\
14、放大缩小：aaa.scale(2,2)//设置完之后会影响后面绘制
15、aaa.save();//变化之前保存当前状态
  aaa.restore();恢复变化之前保存的状态
16、透明度:aaa.globalAlpha=(0-1);
17、贝赛尔曲线

～～～～day33～～～～
1、全屏API
～～～day34～～～
BOM：浏览器对象模型
1、浏览器内置对象:location,navigator,history
#location对象:最有用的DOM对象之一，提供了与当前窗口加载的文档有关的信息，还提供例一些导航功能。
属性： 1)hashk：可读写，返回URL的hash 格式:#开头，如URL不包含散列(hash)则返回空字符串
 	    2)host:返回服务器名称和端口号（如果有）
      3)href:返回当前加载页面的完整URL                                                                
      4)pathnamr:获取文档目录名
5)port:返回URL指定的端口，如过没有则返回空字符串
6)search:返回URL查询字符，截取"?"后面的字符串
方法：  location.assign();跳转页面，参数为URL;
      location.reload();重新加载当前URL，参数为true/false；
location.replace();替换当前页面，不可后退，无历史记录；
  #navigator对象:识别客户端浏览器的事实标
*navigator.userAgent:浏览器代理
*navigator.userLanguage:用户默认语言
*navigator.platform:操作系统平台
*navigator.vendor:浏览器厂商
运用:检测浏览器插件:var a = navigator.plugins;
for(var i = 0 ; i<a.length ; i++){
console.log(a[i].name);
}
#history对象:保存着用户上网的历史记录
*history.go();参数为正前进或参数为负后退
*history.back()；后退
*history.forward();前进
2、错误处理函数:
#try{可能出现的错误代码}catch(){检查到错误后执行的代码}finally{无论是否有错误，都会执行};
注意：一但某处出现错误，那么try中的其他代码将不再执行；可以嵌套tey，如果没有catch，那么错误会向外传递，直到遇到一个catch为止！！
*throw (str自定义错误);抛出异常
#本地储存：DOM存储的机制是通过存储字符串类型的键值对，提供一种安全的存取方式。附加功能的目标使提供一个全面的，可以用来创建交互式应用程序的方法(包括那些高级功能，如可离线工作)
##sessionStorage对象：存储在sessionStorage中的数据可以跨越页面刷新而存在
属性:
*sessionStorage.setItem();写入数据，参数是键和值一对，将键值添加到存储中
*sessionStorage.getltem();接受键名作为参数，返回键名对应值
*sessionStorage.clear();清除
##localStorage对象:可将数据存储到客户端本地,除非手动清除.要访问同一个localStorage对象，页面必须来自同一个域名(子域名无效)协议,在同一个端口上
*localStorage.setItem();写入数据，参数是键和值一对
*localStorage.getltem();接受键名作为参数，返回键名对应值
*localStoragr.clear();手动清除
3、Web Worker:线程
#创建线程：var aaa=new Worker();参数使外部js，线程创建成功后立即开始运行
#postMessage();用于给线程发送输数据
#.onmessage:接收子线程发来的数据
#.terminate();结束/终止一个线程，无参数
importScripts(路径),引入外部文件，多则以逗号分隔开
