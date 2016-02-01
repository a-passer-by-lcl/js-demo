#Math 对象
* Math 对象用于执行数学任务
* Math 对象并不像 Date 和 String 那样是对象的类，因此没有构造函数 Math()
* Math.sin() 这样的函数只是函数，不是某个对象的方法您无需创建它
* 通过把 Math 作为对象使用就可以调用其所有属性和方法

###Math 属性
* Math.E---------------------------------返回算术常量 e，即自然对数的底数(2.718281828459045)
* Math.LN2-------------------------------返回 2 的自然对数(0.6931471805599453)
* Math.LN10------------------------------返回 10 的自然对数(2.302585092994046)
* Math.LOG2E-----------------------------返回以 2 为底的 e 的对数(1.4426950408889634)
* Math.LOG10E----------------------------返回以 10 为底的 e 的对数(0.4342944819032518)
* Math.PI--------------------------------返回圆周率 π(3.141592653589793)
* Math.SQRT2-----------------------------返回 2 的平方根(1.4142135623730951)
* Math.SQRT1_2---------------------------返回返回 2 的平方根的倒数(0.7071067811865476)

###Math 方法
#####Math三角函数方法
* Math.sin(num)--------------------------返回 num 的正弦值
	* 一个以弧度表示的角,将角度乘以 0.017453293 （2PI/360）即可转换为弧度
	* 返回值----参数 num 的正弦值返回值---在 -1.0 到 1.0 之间

* Math.cos(num)--------------------------返回 num 的余弦值
	* 返回值---num 的余弦值返回的是 -1.0 到 1.0 之间的数

* Math.sqrt(num)-------------------------返回 num 的平方根
	* 必须是大于等于 0 的数
	* 返回值---参数 num 的平方根若 num 小于 0，则返回 NaN

* Math.tan(num)--------------------------返回 num 的正切值
	* 必需一个以弧度表示的角将角度乘以 0.017453293 （2PI/360）即可转换为弧度

* Math.acos(num)-------------------------返回 num 的反余弦值
	* 必须是 -1.0 ~ 1.0 之间的数
	* 返回值---num 的反余弦值返回的值是 0 到 PI 之间的弧度值
	* 若参数 num 超过了 -1.0 ~ 1.0 的范围，那么浏览器将返回 NaN
	* 若参数 num 取值 -1，那么将返回 PI

* Math.asin(num)-------------------------返回 num 的反正弦值
	* 必需必须是一个数值，该值介于 -1.0 ~ 1.0 之间
	* 返回值---num 的反正弦值返回的值是 -PI/2 到 PI/2 之间的弧度值
	* 若参数 num 超过了 -1.0 ~ 1.0 的范围，那么浏览器将返回 NaN
	* 若参数 num 取值 1，那么将返回 PI/2

* Math.atan(num)-------------------------返回 num 的反正切值
	* 返回值---num 的反正切值返回的值是 -PI/2 到 PI/2 之间的弧度值
	* 以介于 -PI/2 与 PI/2 弧度之间的数值来返回 num 的反正切值

* Math.atan2(y,x)------------------------返回从 num 轴到点 (x,y) 的角度
	* 介于 -PI/2 与 PI/2 弧度之间
	* 返回值---- -PI 到 PI 之间的值，是从 X 轴正向逆时针旋转到点 (x,y) 时经过的角度

#####Math算术方法
* Math.abs(num)--------------------------返回 num 的绝对值
* Math.enump(num)------------------------返回以自然数为底,num次幂的数
* Math.log(num)--------------------------返回 num 的自然对数
* Math.pow(x,y)------------------------  返回 num 的y次方的值
* Math.random()--------------------------返回0到1之间的一个随机数
* Math.max(num1,num2)------------------返回 num1 和 num2 中最高值
	* 参数中最大的值若没有参数，则返回 -Infinity若有某个参数为 NaN，或是不能转换成数字的非数字值，则返回 NaN
* Math.min(num1,num2)--------------------返回 num1 和 num2 中最小值
	* 参数中最小的值若没有参数，则返回 Infinity若有某个参数为 NaN，或是不能转换成数字的非数字值，则返回 NaN

#####Math取舍方法
* Math.round(num)------------------------返回 num 四舍五入后的值
* Math.ceil(num)-------------------------返回 num 的最接近的整数，即对数进行上舍入
* Math.floor(num)------------------------返回 num 的最接近的整数，即对数进行下舍入



* Math.toSource()------------------------代表对象的源代码
	* Math.toSource()方法在 Internet Enumplorer 中无效
* Math.valueOf()-------------------------返回某个 Math 对象的原始值
	* 该原始值由 Math 对象派生的所有对象继承
	* Math.valueOf()方法通常由 JavaScript 在后台自动调用，并不显式地出现在代码中

*　parseInt(num)-------------------------丢弃小数部分,保留整数部分

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script src="http://cdn.bootcss.com/jquery/2.1.4/jquery.js"></script>
</head>
<body>
<script type="text/javascript">
$(document).ready(function() {
console.log(Math.SQRT2);
console.log(Math.random());
var math10 = Math.random()*10
console.log(typeof math10 + " random");
console.log(typeof parseInt(math10) + " parseInt");
console.log(typeof Math.ceil(math10) + " ceil");
console.log(typeof Math.floor(math10) +" floor");
console.log(typeof Math.round(math10) + " round");
console.log(math10 + " random");
console.log(parseInt(math10) + " parseInt");
console.log(Math.ceil(math10) + " ceil");
console.log(Math.floor(math10) +" floor");
console.log(Math.round(math10) + " round");
console.log(Math.ceil(2.5222));
console.log(Math.floor(2.5222));
console.log(Math.round(2.5222));
});
</script>
</body>
</html>
```
