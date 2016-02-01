#web storage
* 类似于之前的cookie，cookie却只有4K
* web storage 拥有本地5兆的容量可以存储
###web strange
* localstorage
* sessionstorage
* 本地数据库

* Web Storage 包含如下两种机制
	* sessionStorage 为每一个给定的源（given origin）维持一个独立的存储区域，该存储区域在页面会话期间可用（即只要浏览器处于打开状态，包括页面重新加载和恢复）
	* localStorage 同样的功能，但是在浏览器关闭，然后重新打开后数据仍然存在

####window.localstorage
* window.localStorage.length----------------------获取localStorage的长度
* window.localStorage.setItem(key,value)----------保存数据
* window.localStorage.getItem(key)----------------读取数据
* window.localStorage.removeItem(key)-------------接受一个键名作为参数，后将其该键名从存储中移除
* window.localStorage.clear()---------------------调用它会清空存储对象里所有的键值
* window.localStorage.key(index)------------------返回存储对象第n个数据项的键名

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<script src="http://cdn.bootcss.com/jquery/2.1.4/jquery.js"></script>
<body>
	<form id="demoForm">
		<p><label><span>姓名</span><input name="name"></label></p>
		<p><label><span>年龄</span><input name="age"></label></p>
		<p><label><span>学号</span><input name="number"></label></p>
		<p><label><span>地址</span><input name="address"></label></p>
		<p><label><span>爱好</span><input name="habit"></label></p>
		<p>
			<label>
				<span>其他</span>
				<textarea name="big" id="" cols="30" rows="10"></textarea>
			</label>
		</p>
		<p><input type="submit" value="提交"></p>
	</form>
<script type="text/javascript">
$(document).ready(function() {
	$.fn.getFormParam=function(){
		var serializeObj={};
		var array=this.serializeArray();
		var str=this.serialize();
		$(array).each(function(){
			if(serializeObj[this.name]){
				if($.isArray(serializeObj[this.name])){
					serializeObj[this.name].push(this.value);
				} else{
					serializeObj[this.name]=[serializeObj[this.name],this.value];
				}
				} else{
					serializeObj[this.name]=this.value;
				}
			});
			return serializeObj;
		};
		var storageFile =JSON.parse(window.localStorage.getItem('demo'));
		$.each(storageFile, function(i, val){
			$('#demoForm').find('[name="'+i+'"]').val(val);
		});
		$('#demoForm').find('[type="submit"]').on('click', function(){
			var data = $('#demoForm').getFormParam();
			window.localStorage.setItem('demo', JSON.stringify(data));
			return false;
		});
	});
});
</script>
</body>
</html>
```


###window.sessionStorage
* window.sessionStorage用法与localStorage用法相同
* window.sessionStorage在浏览器关闭网站时候就会清除
* 而window.localStorage会一直保存至浏览器中，二者酌情配合使用

###本地数据库
* 熟悉IOS/Android开发的同学，应该会对SQLite数据库比较熟悉
* 主要有openDatabase方法和transaction方法
* 用一个对象db来接收openDatabase创建的访问数据库的对象

```javascript
var db = openDatabase(databasename,version,description,size)
databasename-----------数据库名
version----------------数据库版本 可不填
desription-------------数据库描述
size-------------------数据库分配空间大小
//transaction方法用一个回调函数作为参数，在函数中执行具体的访问数据库的方法
db.transaction(function(tx)){
	tx.executeSql(sqlQuery,[value1,value2..],dataHandler,errorHandler)
});
//executeSql方法的四个参数
///sqlQuer---------------------需要具体执行的sql语句，create||select||update||delete
//[value1,value2..]-----------sql语句中所有使用到的参数的数组，在executeSql方法中，将sql语句中所要使用的参数先用“?”代替，然后依次将这些参数组成数组放在第二个参数中
//dataHandler-----------------执行成功回调函数
//errorHandler----------------执行失败回调函数
```
