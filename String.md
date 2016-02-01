#String对象
###String对象用于处理字符串
#####创建String对象的语法：
* new String(stringValue)
* String(stringValue)
* 创建一个String对象，语法：new String(stringValue)
* 该调用会将参数转换为字符串，并作为一个String对象
* 事实上任何一个字符串常量都是一个String对象，可以将其直接作为对象来使用
* 字符串常量和new String()的区别是：typeof的返回值不同，一个是“stirng"，另一个是"object"
* 当不用 new 运算符调用String() 时，它只把stringValue转换成原始的字符串，并返回转换后的值

###String 对象属性(String 即 String)
* String.constructor-------------------对创建该对象的函数的引用
* String.length------------------------字符串的长度
* String.prototype---------------------允许您向对象添加属性和方法

###String 对象方法(String 即 String)
* 字符串的方法包括：charAt()、charCodeAt()、concat()、indexOf()、lastIndexOf()、localeCompare()、match()、replace()、search()、slice()、split()、substr()、substring()、toLowerCase()、toString()、toUpperCase()、valueOf()

######charAt类方法
* String.charAt(index)-----------------返回指定位置的字符(即某个字或者字母)
	* 若超出有效范围的索引值返回空字符串
* String.charCodeAt(index)-------------返回指定位置的字符串的Unicode编码
	* 若指定位置没有字符，将返回NaN
* String.fromCharCode(numX)------------使用Unicode编码形式创建一个字符串(只能用String.方法名)

#####String对象HTML中应用
* String.blink()-----------------------显示闪动字符串
* String.sup()-------------------------让字符串显示为上标
* String.sub()-------------------------让字符串显示为下标
* String.bold()------------------------使用粗体显示字符串
* String.italics()---------------------使用斜体显示字符串
* String.strike()----------------------使用删除线显示字符串
* String.big()-------------------------使用大号字显示字符串
* String.small()-----------------------使用小字号显示字符串
* String.fixed()-----------------------打字机文本显示字符串
* String.fontcolor(color)--------------使用指定的颜色显示字符串
* String.fontsize(size)----------------使用指定的尺寸显示字符串(处于1-7之间的数字)
* String.link(URL)---------------------将字符串显示为链接(参数为链接的URL)
* String.anchor(anchorname)------------将字符串显示为锚点(参数为链接的name属性值)


#####String对象的大小写转换
* String.toLocaleLowerCase()-----------按照本地方式把字符串转换为小写
* String.toLocaleUpperCase()-----------按照本地方式把字符串转换为大写
* String.toLowerCase()-----------------把字符串转换为小写
* String.toUpperCase()-----------------把字符串转换为大写

#####String截取
* String.slice(start,end)--------------返回新的字符串来表示被截取部分
	* start--------截取开始,若是负数，规定的是从字符串的尾部开始算起的位置
	* end----------截取结束,若是负数，规定的是从字符串的尾部开始算起的位置
	* String.slice() 与 Array.slice() 相似

* String.substring(start,end)----------返回新的字符串来表示截取字符串中介于两个指定下标之间的字符
	* start--------开始，一个非负的整数，规定要提取的子串的第一个字符在String中的位置
	* end----------结束，一个非负的整数，比要提取的子串的最后一个字符在String中的位置多1
	* 若是负数，则不会报错,会返回原字符串
	* 若参数start与stop相等，该方法返回的就是一个空串(即长度为0的字符串)
	* 若参数start比stop大，该方法在截取子串之前会先交换这两个参数

* String.substr(start,length)----------从起始索引号截取字符串中指定数目的字符
	* start--------开始,必须是数值;若是负数，那么该参数声明从字符串的尾部开始算起的位置
	* length-------子串中的字符数,必须是数值
	* 若该参数为负数或0，都将返回空字符串
	* 重要事项：ECMAscript 没有对该方法进行标准化，因此反对使用它

* String.slice()、String.substring()、String.substr()比较或者区别
	* String.slice()、String.substring()与String.substr()方法若省略end或length参数，返回的子串会从start开始到字符串的结尾
	* String.slice()、String.substring()方法返回的子串包括start处的字符，但不包括end处的字符
	* String 对象的方法slice()、substring()和substr()(不建议使用)都可返回字符串的指定部分
	* slice()比substring()要灵活一些，因为它允许使用负数作为参数
	* slice()与substr()不同，因为它用两个字符的位置来指定子串,substr()则用字符位置和长度来指定子串


* String.concat(stringX)----------------用于连接两个或多个字符串(String本身并没有被更改)
	* 将把它的所有参数转换成字符串，然后按顺序连接到字符串String 的尾部，并返回连接后的字符串
	* 请注意，String 本身并没有被更改
	* String.concat()与Array.concat()很相似

* String.split(separator,howmany)------把字符串分割为字符串数组
	* separator------字符串或正则表达式，从该参数指定的地方分割String
	* howmany--------该参数可指定返回的数组的最大长度;若设置了该参数，返回的子串不会多于这个参数指定的数组;若没有设置该参数，整个字符串都会被分割，不考虑它的长度
	* 返回一个字符串数组，该数组是通过在 separator 指定的边界处将字符串 String 分割成子串创建的。返回的数组中的字串不包括separator 自身
	* 若 separator 是包含子表达式的正则表达式，那么返回的数组中包括与这些子表达式匹配的字串（但不包括与整个正则表达式匹配的文本）

* String.localeCompare(target)---------用本地特定的顺序来比较两个字符串
	* 若 String 小于 target，则localeCompare()返回小于 0 的数
	* 若 String 大于 target，则该方法返回大于 0 的数
	* 若两个字符串相等，或根据本地排序规则没有区别，该方法返回 0

* String.toString()---------------------返回字符串
	* string的原始字符串值，一般不会调用该方法
	* 当调用该方法的对象不是 String 时抛出 TypeError 异常

* String.valueOf()----------------------返回 String 对象的原始值
	* 原始值是由从 String 对象下来的所有对象继承的
	* valueOf() 方法通常由 JavaScript 在后台自动进行调用，而不是显式地处于代码中

* String.indexOf(search,index)----------检索字符串，返回指定的字符串值在字符串中首次出现的位置
	* search--------规定需检索的字符串值
	* index---------可选的整数参数,该整数值指在字符串中开始检索的位置,如省略该参数，则将从字符串的首字符开始检索
	* 该方法将从头到尾地检索字符串 string，看它是否含有子串 search
	* 开始检索的位置在字符串的 index 处或字符串的开头（没有指定 index 时）
	* 若找到一个 search，则返回 search 的第一次出现的位置
	* 说明 indexOf 方法返回一个整数值，指出 String 对象内子字符串的开始位置
	* indexOf() 方法对大小写敏感
	* 若要检索的字符串值没有出现，则该方法返回 -1

* String.lastIndexOf(search,index)-----------------返回指定的字符串值最后出现的位置，从右向左查找
	* lastIndexOf() 方法对大小写敏感
	* 若要检索的字符串值没有出现，则该方法返回 -1
	* search--------规定需检索的字符串值
	* index---------规定在字符串中开始检索的位置；如省略该参数，则将从字符串的最后一个字符处开始检索
	* 该方法将从尾到头地检索字符串 String，看它是否含有子串 search
	* 开始检索的位置在字符串的 index 处或字符串的结尾（没有指定 index 时）
	* 若找到一个 search，则返回 search 的第一个字符在 String 中的位置
	* String 中的字符位置是从 0 开始的

#####替换和匹配字符串
* String.match()------------------------在字符串内检索指定的值，或找到一个或多个正则表达式的匹配
	* 它返回指定的值
	* String.match(search)-----search-------规定要检索的字符串值
	* String.match(regexp)-----regexp-------规定要匹配的模式的 RegExp 对象
	* 若该参数不是 RegExp 对象，则需要首先把它传递给 RegExp 构造函数，将其转换为 RegExp 对象
	* 存放匹配结果的数组,该数组的内容依赖于 regexp 是否具有全局标志 g
	* 若 regexp 没有标志 g，那么 match() 方法就只能在 String 中执行一次匹配
	* 若没有找到任何匹配的文本， match() 将返回 null
	* 否则，它将返回一个数组，其中存放了与它找到的匹配文本有关的信息
	* 该数组的第 0 个元素存放的是匹配文本，而其余的元素存放的是与正则表达式的子表达式匹配的文本
	* 返回的数组还含有两个对象属性
	* index 属性声明的是匹配文本的起始字符在 String 中的位置
	* input 属性声明的是对 String 的引用
	* 若 regexp 具有标志 g，则 match() 方法将执行全局检索，找到 String 中的所有匹配子字符串
	* 若没有找到任何匹配的子串，则返回 null
	* 若找到了一个或多个匹配子串，则返回一个数组
	* 不过全局匹配返回的数组的内容与前者大不相同，它的数组元素中存放的是String中所有的匹配子串，没有 index 属性或 input 属性
	* 在全局检索模式下，match() 即不提供与子表达式匹配的文本的信息，也不声明每个匹配子串的位置
	* 若您需要这些全局检索的信息，可以使用 RegExp.exec()

* String.replace(regexp/substr,replacement)
	* 在字符串中用一些字符替换另一些字符，或替换一个与正则表达式匹配的子串
	* regexp/substr-------规定子字符串或要替换的模式的 RegExp 对象
		* 若该值是一个字符串，则将它作为要检索的直接量文本模式，而不是首先被转换为 RegExp 对象
	* replacement---------一个字符串值，规定了替换文本或生成替换文本的函数
	* 返回一个新的字符串，是用 replacement 替换了 regexp 的第一次匹配或所有匹配之后得到的

	* 字符串 String 的 replace() 方法执行的是查找并替换的操作
	* 它将在 String 中查找与 regexp 相匹配的子字符串，然后用 replacement 来替换这些子串
	* 若 regexp 具有全局标志 g，那么 replace() 方法将替换所有匹配的子串
	* 否则，它只替换第一个匹配子串
	* replacement 可以是字符串，也可以是函数
	* 若它是字符串，那么每个匹配都将由字符串替换
	* 但是 replacement 中的 $ 字符具有特定的含义，它说明从模式匹配得到的字符串将用于替换

	* 注意：ECMAScript v3 规定，replace() 方法的参数 replacement 可以是函数而不是字符串
	* 在这种情况下，每个匹配都调用该函数，它返回的字符串将作为替换文本使用
	* 该函数的第一个参数是匹配模式的字符串。接下来的参数是与模式中的子表达式匹配的字符串，可以有 0 个或多个这样的参数
	* 接下来的参数是一个整数，声明了匹配在 String 中出现的位置。最后一个参数是 String 本身

* String.search(regexp)-------------------用于检索字符串中指定的子字符串，或检索与正则表达式相匹配的子字符串
	* regexp---------该参数可以是需要在 stringObject 中检索的子串，也可以是需要检索的 RegExp 对象
	* String.search() 对大小写敏感
	* 要执行忽略大小写的检索，请追加标志 i
	* 返回值string 中第一个与 regexp 相匹配的子串的起始位置
	* 若没有找到任何匹配的子串，则返回 -1
	* search() 方法不执行全局匹配，它将忽略标志 g
	* 它忽略 regexp 的 lastIndex 属性，并且总是从字符串的开始进行检索，意味着它总是返回 string 的第一个匹配的位置

###String 对象描述
* 字符串是 JavaScript 的一种基本的数据类型
* String对象的 length 属性声明了该字符串中的字符数
* String类定义了大量操作字符串的方法，例如从字符串中截取字符或子串，或者检索字符或子串
* 需要注意的是，JavaScript 的字符串是不可变的
* （immutable），String 类定义的方法都不能改变字符串的内容。像 String.toUpperCase() 这样的方法，返回的是全新的字符串，而不是修改原始字符串。
* 在较早的 Netscape 代码基的 JavaScript 实现中（例如 Firefox 实现中），字符串的行为就像只读的字符数组。例如，从字符串 s 中截取第三个字符，可以用 s[2] 代替更加标准的
* s.charAt(2)。此外，对字符串应用 for/in 循环时，它将枚举字符串中每个字符的数组下标（但要注意，ECMAScript 标准规定，不能枚举 length 属性）。因为字符串的数组行为不标准，所以应该避免使用它

#String.prototype使用

#####字符串-格式化
```javascript
String.prototype.format = function(){
    //获取函数传递参数数组,以便在replace回调函数内使用
	//匹配并捕获所有形如:{数字}字串
	//参数 = 匹配子串+第几次匹配+匹配字串位置+源字符串
	var args   = arguments;
	var regex = /\{(\d+)\}/g;
    return this.replace(regex,function(m,i){
	    return args[i];
	});
}
```

```javascript
//字符串去掉前后空白字符
String.prototype.trim = function(){
    return this.replace(/(^\s*)|(\s*$)/g,"");
}
```

```javascript
//去掉字符两端的空白字符
String.prototype.Trim = function () {
    return this.replace(/(^[/t/n/r]*)|([/t/n/r]*$)/g,'');
};
```
```javascript
//字符串-去掉前空白字符
String.prototype.nextTrim = function(){
    return this.replace(/(^\s*)/g,"");
}
```

```javascript
//字符串-去掉后空白字符
String.prototype.prevTrim = function(){
    return this.replace(/(\s*$)/g,"");
}
```

```javascript
//去掉字符左边的空白字符
String.prototype.leftTrim = function () {
    return this.replace(/^[/t/n/r]/g,'');
};
```

```javascript
//去掉字符右边的空白字符
String.prototype.rightTrim = function () {
    return this.replace(/[/t/n/r]*$/g,'');
};
```

```javascript
//字符串-获取以ASCII编码字节数英文占1字节中文占2字节
String.prototype.lenASCII = function(){
    return this.replace(/[^\x00-\xff]/g,'xx').length;
    //将所有非\x00-\xff字符换为xx两个字符,再计算字符串
}
```

```javascript
//字符串-获取以UNICODE编码字节数一个字符均占2个字节
String.prototype.lenUNICODE = function(){
    return this.length*2;
}
```

```javascript
//返回字符的长度，一个中文算2个
String.prototype.ChineseLength = function(){
    return this.replace(/[^/x00-/xff]/g,"**").length;
};
```

```javascript
//判断字符串是否以指定的字符串结束
String.prototype.EndsWith = function (A,B) {
	var C = this.length;
	var D = A.length;
	if( D > C){
	    return false;
	}
	if(B){
	   	var E = new RegExp(A+'$','i');
	       return E.test(this);
	} else {
	    return (D =  = 0||this.substr(C-D,D) =  = A);
	}
};
```
```javascript
//判断字符串是否以指定的字符串开始
String.prototype.StartsWith = function(str){
    return this.substr(0, str.length) = =  str;
};
```

```javascript
//字符串从哪开始多长字符去掉
String.prototype.Remove = function (A,B) {
	var s = '';
	if(A>0){
		s = this.substring(0,A);
	}
	if(A+B<this.length){
		s+ = this.substring(A+B,this.length);
	    return s;
	}
};
```
