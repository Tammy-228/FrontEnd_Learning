ECMAscript
• 核心（ECMAScript）
• 文档对象模型（DOM） Document object model (整合 js，css，html)
• 浏览器对象模型（BOM） Broswer object model（整合 js 和浏览器）

全栈开发架构：
• 前端：使用框架（如 React.js、Vue.js）构建用户界面。
• 后端：使用 Node.js 和 Express.js 处理服务器逻辑。
• 数据库：使用 JavaScript 驱动的数据库（如 MongoDB）管理数据。

JS 基础： 1. 引入：
a. 直接引入
<script> alert('hello yuan') </script>
b. 文件引入 <script src="hello.js"></script> 2. 变量、常量、标识符
a. 用 var 来表示 var a;<br>a=3;
b. 同一行可以是不同的变量，可以是不同的类型 var name="yuan", age=20, job="lecturer";
c. 声明变量时 可以不用 var. 如果不用 var 那么它是全局变量
d. 变量命名,首字符只能是字母,下划线,$美元符 三选一；区分大小写。
e. 标识符与常量：
i. 常量就是直接在程序中出现的数据值
ii. 标识符是通用的概念，指代代码中所有“有名字的东西” 1) 当用来储存数据时，它是‘变量’ 2) 当用来表示类、方法、对象时，它是它自己特定的类型。 3. JS 的数据类型：
a. number ----- 数值
boolean ----- 布尔值
string ----- 字符串
undefined ----- undefined
null ----- null  
 b. number：不区分整数和小数：
i. 所有数字都采用 64 位浮点格式存储，相当于 Java 和 C 语言中的 double 格式。
ii. 16 进制数据前面加上 0x，八进制前面加 0;16 进制数是由 0-9,A-F 等 16 个字符组成;8 进制数由 0-7 等 8 个数字组成
C. 字符串：
是由 Unicode 字符、数字、标点符号组成的序列；字符串常量首尾由单引号或双引号括起；JavaScript 中没有字符类型；常用特殊字符在字符串中的表达；
字符串中部分特殊字符必须加上右划线；常用的转义字符 \n:换行 ':单引号 ":双引号 \:右划线
D. boolean： true=1,false=0
E. Null 和 undefined： undefined 是声明了变量但未对其初始化时赋予该变量的值，null 则用于表示尚未存在的对象 4. 运算：
A. 算式运算：
i. 注意：在 js 中，一元加号 会尝试将后面的值转换为数字。D = +d
□ 如果字符串是有效的数字格式（例如 "123" 或 "3.14"），会成功转换为数字。
□ 如果字符串不是有效的数字格式（例如 "yuan"），转换失败，结果是 NaN。
B. 比较运算：
i. 相等、全等运算符 1) == 是相等 === 全等 （值和类型都要相等，不进行类型转换） 2) ！= 值是否不相等，！== 值和类型是否都不相等
a) console.log(2 !== "2"); // true，因为虽然值相等，但类型不同
ii. 字符串和数字对比：如果一个是数字类型,一个是其他类型,会将其类型转换成数字类型. 1) var bResult = "Blue" < "alpha";
alert(bResult); // 输出 true 　字母 B 的字符代码是 66，字母 a 的字符代码是 97。 2) var bResult = "25" < "3";
alert(bResult); //输出 "true" 两个运算数都是字符串，所以比较的是它们的字符代码（"2" 的字符代码是 50，"3" 的字符代码是 51） 3) var bResult = "25" < 3;
alert(bResult); //输出 "false" 字符串 "25" 将被转换成数字 25，然后与数字 3 进行比较，结果不出所料
C. 逻辑运算：&& || ！
D. 赋值运算：= += -= \*= /=
NaN 是 JavaScript 中一个特殊的值，它表示“不是一个数字（Not-a-Number）”。NaN 通常出现在将非数字转换为数字失败，或者运算无法产生有效数字结果的情况下。
而 Nah 的类型属于 number.
alert() 是一个 内置函数，用于向用户显示一个简单的弹窗对话框。这种对话框一般是用来显示信息或者调试代码。Console.log() 是 JavaScript 提供的一个 内置函数，用于在浏览器的开发者工具（DevTools）的 控制台（Console） 中输出信息
var d="yuan";
d=+d;
alert(d);//NaN:属于 Number 类型的一个特殊值,当遇到将字符串转成数字无效时,就会得到一个 NaN 数据
alert(typeof(d));//Number
//NaN 特点:
var n=NaN;
alert(n>3); // false
alert(n<3); //false
alert(n==3); // false
alert(n==NaN); // false
alert(n!=NaN);//. True.  
 - 如何检测 NaN 呢？
§ isNaN(value) console.log(isNaN("yuan")); // 输出 true
§ Number.isNaN() 只检测值是否是严格的 NaN，不会对非数字类型进行隐式转换。
□ console.log(Number.isNaN("yuan")); // 输出 false 5. 逻辑顺序结构：
A. 分支：
i. If-else
ii. If-elif-else
iii. Switch-case
B. 循环：
i. For
ii. While  
 C. 异常处理：
i. Try - catch - finally 6. 对象：
<script language="javascript">
var aa=Number.MAX_VALUE;
//利用数字对象获取可表示最大数
var bb=new String("hello JavaScript");
//创建字符串对象
var cc=new Date();
//创建日期对象
var dd=new Array("星期一","星期二","星期三","星期四");
//数组对象
</script> 1. 字符串对象：
① 变量 = “字符串”
② 字串对象名称 = new String (字符串)
var str1="hello world";
var str1= new String("hello word");
x.toLowerCase() －－－－转为小写
x.toUpperCase() －－－－转为大写
x.trim() －－－－去除字符串两边空格  

x.charAt(index) －－－－str1.charAt(index);－－－－获取指定位置字符，其中 index 为要获取的字符索引
x.indexOf(findstr,index)－－－－查询字符串位置
x.lastIndexOf(findstr)  
 x.match(regexp) －－－－match 返回匹配字符串的数组，如果没有匹配则返回 null
x.search(regexp) －－－－search 返回匹配字符串的首字符位置索引
x.substr(start, length) －－－－start 表示开始位置，length 表示截取长度
x.substring(start, end) －－－－end 是结束位置
x.slice(start, end) －－－－切片操作字符串 2. 数组对象：
i. 数组创建： 1) var arrname = [元素 0,元素 1,….]; 2) var arrname = new Array(元素 0,元素 1,….); 3) 先初始创建一个长度为 7 的数组 var cnweek = new Array(7);
然后在给每一个对象进行赋值 cnweek[0]="星期日";
2D：
var cnweek=new Array(7);
for (var i=0;i<=6;i++){
cnweek[i]=new Array(2);
}
ii. 数组连接：
join：
var arr1=[1, 2, 3, 4, 5, 6, 7];
var str1=arr1.join("-");
alert(str1); //结果为"1-2-3-4-5-6-7"
concat：
var a = [1,2,3];
var b=a.concat(4,5) ;
alert(a.toString()); //返回结果为 1,2,3  
alert(b.toString()); //返回结果为 1,2,3,4,5
iii. 排序 1) 如果直接用 sort()函数进行排序，会按照 字符串的字典顺序排序 2) 但可以自定义 compare 函数，对其进行数字大小的排序。
a) function intSort(a,b){
if (a>b){
return 1;//-1
}
else if(a<b){
return -1;//1
}
else {
return 0
}
}
a - b 的值正好符合比较函数返回值的意义：
• 如果 a > b，a - b 为正数，表示 a 应排在 b 后面。
• 如果 a < b，a - b 为负数，表示 a 应排在 b 前面。
• 如果 a === b，a - b 为 0，表示顺序不变。 3) 删除子数组：
x. splice(start, deleteCount, value, ...
//x 代表数组对象
//splice 的主要用途是对数组指定位置进行删除和插入
//start 表示开始位置索引
//deleteCount 删除数组元素的个数
//value 表示在删除位置插入的数组元素
//value 参数可以省略

var a = [1,2,3,4,5,6,7,8];
a.splice(1,2);
alert(a.toString());//a 变为 [1,4,5,6,7,8]
a.splice(1,1);
alert(a.toString());//a 变为[1,5,6,7,8]
a.splice(1,0,2,3);
alert(a.toString());//a 变为[1,2,3,5,6,7,8] 4) 压栈和弹栈
push pop 这两个方法模拟的是一个栈操作
//x.push(value, ...) 压栈
//x.pop() 弹栈  
//x 代表数组对象
//value 可以为字符串、数字、数组等任何值
//push 是将 value 值添加到数组 x 的结尾
//pop 是将数组 x 的最后一个元素删除
Stack LIFO 5) Shift & unshift
//x.unshift(value,...)
//x.shift()
//x 代表数组对象
//value 可以为字符串、数字、数组等任何值
//unshift 是将 value 值插入到数组 x 的开始
//shift 是将数组 x 的第一个元素删除
var arr1=[1,2,3];
arr1.unshift(4,5);
alert(arr1); //结果为"4,5,1,2,3"
arr1. unshift([6,7]);
alert(arr1); //结果为"6,7,4,5,1,2,3"
arr1.shift();
alert(arr1); //结果为"4,5,1,2,3" 3. 日期对象：
i. 日期对象创建：var nowd1=new Date(); 1) 参数为日期字符串：var nowd2=new Date("2004/3/20 11:12"); 2) 参数为毫秒数：var nowd3=new Date(5000); 3) 参数为年月日小时分钟秒毫秒： var nowd4=new Date(2004,2,20,11,12,0,300);
ii. Date 对象的方法： 1) 获取日期和时间
getDate() 获取日
getDay () 获取星期
getMonth () 获取月（0-11）
getFullYear () 获取完整年份
getYear () 获取年
getHours () 获取小时
getMinutes () 获取分钟
getSeconds () 获取秒
getMilliseconds () 获取毫秒
getTime () 返回累计毫秒数(从 1970/1/1 午夜) 2) 设计日期和时间：
var x=new Date();
x.setFullYear (1997); //设置年 1997
x.setMonth(7); //设置月 7
x.setDate(1); //设置日 1
x.setHours(5); //设置小时 5
x.setMinutes(12); //设置分钟 12
x.setSeconds(54); //设置秒 54
x.setMilliseconds(230); //设置毫秒 230
document.write(x.toLocaleString( )+"<br>");
//返回 1997 年 8 月 1 日 5 点 12 分 54 秒
x.setTime(870409430000); //设置累计毫秒数
document.write(x.toLocaleString( )+"<br>");
//返回 1997 年 8 月 1 日 12 点 23 分 50 秒 4. Math 对象：
abs(x) 返回数的绝对值。
exp(x) 返回 e 的指数。
floor(x)对数进行下舍入。
log(x) 返回数的自然对数（底为 e）。
max(x,y) 返回 x 和 y 中的最高值。
min(x,y) 返回 x 和 y 中的最低值。
pow(x,y) 返回 x 的 y 次幂。
random() 返回 0 ~ 1 之间的随机数。
round(x) 把数四舍五入为最接近的整数。
sin(x) 返回数的正弦。
sqrt(x) 返回数的平方根。
tan(x) 返回角的正切。 5. 函数对象：
i. function 函数名 (参数){
<br> 函数体;
return 返回值;
}
可以使用变量、常量或表达式作为函数调用的参数
函数由关键字 function 定义
函数名的定义规则与标识符一致，大小写是敏感的
返回值必须使用 return
Function 类可以表示开发者定义的任何函数。
var 函数名 = new Function("参数 1","参数 n","function_body");
JS 是全部加载完才会执行，所以执行函数放在函数声明上面或下面都可以 6. Function 对象的属性：
i. 内置的 arguments：
在 JavaScript 中，arguments 是一个类似数组的对象，默认可用于所有函数。它包含了调用函数时传递的所有参数，无论函数的定义中是否声明了这些参数。
□ 类似数组，但不是数组：
® arguments 可以通过索引访问（如 arguments[0]），但它不是一个真正的数组，没有数组的方法（如 map()、forEach() 等）。
® 如果需要将它转换为数组，可以使用 Array.from(arguments) 或扩展运算符 [...]。
□ 动态捕获所有传递的参数：
® 无论函数定义了多少参数，arguments 都会捕获所有传递的参数，包括多余的参数。
□ 属性：
® arguments.length：
◊ 表示实际传递给函数的参数个数。
® arguments[i]：
◊ 表示第 i 个参数。
□ 只存在于常规函数中：
® 在箭头函数中，arguments 不存在。如果需要类似功能，可以使用剩余参数 ...args。
与 parameters 类似但不同，parameters 只表示函数定义中声明的变量。但 argument 能获所有实际传入的值（包括未声明的参数）。
典型用法： 1. 需要接受任意数量的参数时，可以使用 arguments 捕获所有传入的值
function sum() {
let total = 0;
for (let i = 0; i < arguments.length; i++) {
total += arguments[i]; // 累加所有传入的值
}
return total;
}
console.log(sum(1, 2, 3, 4)); // 输出 10
典型用法 2: 检查是否输入的参数满足预期
function multiply(a, b) {
if (arguments.length !== 2) {
throw new Error("This function requires exactly 2 arguments");
}
return a * b;
}
console.log(multiply(2, 3)); // 输出 6
multiply(2); // 抛出错误
典型用法 3: 动态绑定 实际传入的参数与 arguments 的值
function demo(a, b) {
console.log(arguments[0]); // 输出 1
a = 10; // 修改 a 的值
console.log(arguments[0]); // 输出 10，arguments[0] 与 a 绑定
}
demo(1, 2);
ii. 匿名函数：没有名称的函数，通常用来创建临时的、一次性的函数
用法 1: 匿名函数赋值给变量，用来定义临时逻辑或回调函数
var func = function(arg){
return "tony";
}
用法 2:IIFE（Immediately Invoked Function Expression，立即执行函数表达式
(function(){
alert("tony");
} )()
用法 3: 带参数的立即执行函数
(function(arg){
console.log(arg);
})('123')
常用场景： 1. 作为回调函数
匿名函数常被用作回调函数（callback），在事件处理或异步操作中非常常见: setTimeout 是一个异步函数，它接受一个回调函数和延迟时间（毫秒）。
setTimeout(
function() {
console.log("This is a callback function!");
}, 1000); 2. 创建私有作用域：防止变量污染全局命名空间。
(function() {
var privateVar = "I am private";
console.log(privateVar); // 输出 "I am private"
})();
console.log(privateVar); // 报错：privateVar 未定义 3. 初始化配置或运行代码：比如设置初始状态或加载模块。
(function() {
var config = {
apiKey: "12345",
apiUrl: "https://api.example.com"
};
console.log("Configuration initialized:", config);
})(); 4. 带参数的初始化：通过传递参数到 IIFE 中，可以动态配置行为
(function(apiUrl) {
console.log("API URL is:", apiUrl);
})("https://api.example.com");
BOM + DOM：  

• BOM 主要用于 控制浏览器的交互行为，如窗口弹窗、页面跳转、定时器、滚动等。
§ 核心是 window 对象，它表示浏览器窗口，包含浏览器相关的所有属性和方法。
• DOM 主要用于 编辑和操作网页内容，如修改 HTML 元素、改变样式、增删内容等。
§ DOM 的核心是 document 对象，它表示当前的 HTML 文档，包含页面内容的所有节点。
虽然 BOM 和 DOM 是两个独立的模型，但它们经常一起使用，因为浏览器交互和网页内容的动态修改通常是紧密结合的。
交互中的协同作用 1. 通过 BOM 触发交互：
○ 使用 alert() 提示用户。
○ 使用 confirm() 获取用户的确认信息。 2. 通过 DOM 修改内容：
○ 根据用户的输入（例如 prompt()）动态修改页面内容。
// 弹出对话框让用户输入内容
let userName = prompt("请输入你的名字：");
// 根据输入内容动态修改网页
if (userName) {
document.getElementById("welcome").textContent = `欢迎，${userName}！`;
} else {
alert("请输入有效的名字！");
} 7. BOM： 核心是 window
所有浏览器都支持 window 对象。
概念上讲.一个 html 文档对应一个 window 对象.
功能上讲: 控制浏览器窗口的.
使用上讲: window 对象不需要创建对象,直接使用即可. 1. Window 对象方法：
alert() 显示带有一段消息和一个确认按钮的警告框。
confirm() 显示带有一段消息以及确认按钮和取消按钮的对话框。
prompt() 显示可提示用户输入的对话框。
open() 打开一个新的浏览器窗口或查找一个已命名的窗口。
close() 关闭浏览器窗口。
setInterval() 按照指定的周期（以毫秒计）来调用函数或计算表达式。
clearInterval() 取消由 setInterval() 设置的 timeout。
setTimeout() 在指定的毫秒数后调用函数或计算表达式。
clearTimeout() 取消由 setTimeout() 方法设置的 timeout。
scrollTo() 把内容滚动到指定的坐标。 2. 示例方法 1: 1. //open 方法 打开和一个新的窗口 并 进入指定网址.参数 1 : 网址.
//调用方式 1
//open("http://www.baidu.com");
//参数 1 什么都不填 就是打开一个新窗口. 参数 2.填入新窗口的名字(一般可以不填). 参数 3: 新打开窗口的参数.
open('','','width=200,resizable=no,height=100'); // 新打开一个宽为 200 高为 100 的窗口
//close 方法 将当前文档窗口关闭.
//close();
var num = Math.round(Math.random()*100);
function acceptInput(){
//2.让用户输入(prompt) 并接受 用户输入结果
var userNum = prompt("请输入一个 0~100 之间的数字!","0");
//3.将用户输入的值与 随机数进行比较
if(isNaN(+userNum)){
//用户输入的无效(重复 2,3 步骤)
alert("请输入有效数字!");
acceptInput();
}
else if(userNum > num){
//大了==> 提示用户大了,让用户重新输入(重复 2,3 步骤)
alert("您输入的大了!");
acceptInput();
}else if(userNum < num){
//小了==> 提示用户小了,让用户重新输入(重复 2,3 步骤)
alert("您输入的小了!");
acceptInput();
}else{
//答对了==>提示用户答对了 , 询问用户是否继续游戏(confirm).
var result = confirm("恭喜您!答对了,是否继续游戏?");
if(result){
//是 ==> 重复 123 步骤.
num = Math.round(Math.random()\*100);
acceptInput();
}else{
//否==> 关闭窗口(close 方法).
close();
}
}
} 3. 示例方法 2: setInterval()
• setInterval() 是一个 BOM 的方法，用于按照指定的时间间隔 重复执行某段代码或调用某个函数。
• 它会一直重复调用，直到：
○ 手动调用 clearInterval() 停止。
○ 浏览器窗口被关闭。
• setInterval(function, milliseconds);
○ Function 是需要执行的代码
○ milliseconds 是 需要间隔多久进行执行
//XML:
<input id="ID1" type="text" onclick="begin()">
<button onclick="end()">停止</button>
<script>
function showTime(){
var nowd2=new Date().toLocaleString();
var temp=document.getElementById("ID1");
temp.value=nowd2;
}
var ID;
function begin(){ //开始之后，每隔 1 秒钟就会停止 showTime 一次，直到 button onclick 会导致整个的 end()
if (ID==undefined){
showTime();
ID=setInterval(showTime,1000);
}
}
function end(){
clearInterval(ID);
ID=undefined;
}
</script> 4. XML 常用于不同系统之间的数据交换; XML 是一种用于描述和传输数据的标记语言，强调数据的结构化和自描述性。

    	DOM：
    	HTML  Document Object Model（文档对象模型）
    	HTML DOM 定义了访问和操作HTML文档的标准方法
    	HTML DOM 把 HTML 文档呈现为带有元素、属性和文本的树结构（节点树)


    	DOM节点
    	节点类型
    	HTML 文档中的每个成分都是一个节点。
    	DOM 是这样规定的：
    	整个文档是一个文档节点
    	每个 HTML 标签是一个元素节点
    	包含在 HTML 元素中的文本是文本节点
    	每一个 HTML 属性是一个属性节点
    	其中，document与element节点是重点。

    	在节点树中，顶端节点被称为根（root）

每个节点都有父节点、除了根（它没有父节点）
一个节点可拥有任意数量的子
同胞是拥有相同父节点的节点
getElementByID(id)
document.getElementById(“idname”)
document.getElementsByTagName(“tagname”)
document.getElementsByName(“name”)
document.getElementsByClassName(“name”)
<div id="div1">
<div class="div2">i am div2</div>
<div name="yuan">i am div2</div>
<div id="div3">i am div2</div>
<p>hello p</p>
</div>
<script>
var div1=document.getElementById("div1");
////支持;
// var ele= div1.getElementsByTagName("p"); by TagName 和 byClassName 都可以在 div 上去找，但 byID 和 byName 都只能在全局 document 上找。
// alert(ele.length);
////支持
// var ele2=div1.getElementsByClassName("div2");
// alert(ele2.length);
////不支持
// var ele3=div1.getElementById("div3"); 只能在全局中去找，只能用于全局 document 对象。
// alert(ele3.length);
////不支持
// var ele4=div1.getElementsByName("yuan"); 只能用于全局 document 对象
// alert(ele4.length)
</script>
