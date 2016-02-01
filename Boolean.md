#Boolean 对象
* Boolean 对象表示两个值："true" 或 "false"
###创建 Boolean 对象的语法
	```javascript
	var bl = new Boolean(value);
	var bl = Boolean(value);
	//参数 value 由布尔对象存放的值或者要转换成布尔值的值
	```
* 当作为一个构造函数（带有运算符 new）调用时，Boolean() 将把它的参数转换成一个布尔值，并且返回一个包含该值的 Boolean 对象
* 如果作为一个函数（不带有运算符 new）调用时，Boolean() 只将把它的参数转换成一个原始的布尔值，并且返回这个值
* 如果省略 value 参数，或者设置为 0、-0、null、""、false、undefined 或 NaN，则该对象设置为 false否则设置为 true（即使 value 参数是字符串 "false"）

###Boolean 对象属性
* Boolean.constructor-----------返回对创建此对象的 Boolean 函数的引用
* Boolean.prototype-------------向对象添加属性和方法

###Boolean 对象方法
* Boolean.toSource()------------返回该对象的源代码
* Boolean.toString()------------把逻辑值转换为字符串，并返回结果
* Boolean.valueOf()-------------返回 Boolean 对象的原始值
