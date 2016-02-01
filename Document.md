#Document
javascript通过Document类型操作文档，document对象是HTMLDocument的一个实例，表示整个页面。

####document属性
* document.documentElement--------------------返回文档的根节点(即html节点)，包含所有内容(node)
* document.doctype----------------------------返回文档类型声明 (DTD)(node)
* document.title------------------------------返回当前文档的标题(node)
* document.body-------------------------------返回body节点，包含所有内容(node)
* document.URL--------------------------------返回文档完整的URL
* document.domain-----------------------------返回当前文档的域名
* document.referrer---------------------------返回载入当前文档的文档的 URL
* document.baseURI----------------------------返回文档的绝对基础 URI
* document.domConfig--------------------------返回normalizeDocument()被调用时所使用的配置
* document.activeElement----------------------返回当前获取焦点元素
* document.documentURI------------------------设置或返回文档的位置
* document.cookie-----------------------------设置或返回与当前文档有关的所有 cookie
* document.charset----------------------------设置或返回charset（当前文档的字符集）
* document.defaultCharset---------------------根据默认浏览器或系统设置，当前文档默认的字符集是什么

####document方法
* document.addEventListener()-----------------向文档添加句柄
* document.adoptNode(node)--------------------从另外一个文档返回 adapded 节点到当前文档
* document.implementation---------------------返回处理该文档的 DOMImplementation 对象
* document.importNode()-----------------------把一个节点从另一个文档复制到该文档以便应用
* document.documentMode-----------------------返回用于通过浏览器渲染文档的模式
* document.inputEncoding----------------------返回用于文档的编码方式（在解析时）
* document.lastModified-----------------------返回文档被最后修改的日期和时间
* document.readyState-------------------------返回文档状态 (载入中……)
* document.strictErrorChecking----------------设置或返回是否强制进行错误检查
* document.removeEventListener()--------------移除文档中的事件句柄(由 addEventListener() 方法添加)
* document.renameNode()-----------------------重命名元素或者属性节点


* 获取节点
* document.querySelector()--------------------返回文档中匹配指定的CSS选择器的第一元素
* document.querySelectorAll()-----------------返回文档中匹配的CSS选择器的所有元素节点列表
* document.getElementById(id)-----------------返回指定结点，包含所有内容(node)
* document.getElementsByName()----------------返回带有指定名称的对象集合(nodeList)
* document.getElementsByTagName(name)---------返回文档中所有匹配的元素的集合(nodeList)
* document.getElementsByClassName(className)--返回文档中所有匹配的类的集合(nodeList)


* 创建节点
* document.createElement(name)----------------创建标签节点(node)
* document.createAttribute()------------------创建属性节点(node)
* document.createTextNode(text)---------------创建文本结点(node)
* document.createComment()--------------------创建注释节点(node)
* document.createDocumentFragment()-----------创建空的 DocumentFragment 对象，并返回此对象
* document.normalize()------------------------删除空文本节点，并连接相邻节点


* 对象集合
* document.anchors----------------------------返回文档中所有带name的<a>元素
* document.links------------------------------返回文档中所有带herf的<a>元素以及<area>元素
* document.forms------------------------------返回文档中所有的<form>元素
* document.images-----------------------------返回文档中所有的<img>元素
* document.scripts----------------------------返回页面中所有脚本的集合
* document.applets---------------------------返回对文档中所有 Applet 对象的引用
* document.embeds-----------------------------返回文档中所有嵌入的内容（embed）集合


* document.open()----------------------------打开一个流，以收集来自任何 document.write() 或 documentwriteln() 方法的输出
* document.close()---------------------------关闭用 document.open() 方法打开的输出流，并显示选定的数据

###HTML5新加API
* document.getElementsByClassName()--------------用class类获取元素，用这个方法可以查询任何带有class属性且带有符合该class参数值的元素和Document对象（例如：SVG和MathML）
* document.innerHTML------------------------------一种解析和序列化HTML/XML文档的方式，该属性在以前版本的浏览器里只支持HTMLElement并且没有标准化，现在已经支持HTMLDocument了
* document.activeElement-------------------------声明哪个元素是当前的焦点元素
	* 默认情况下，该API中保存的是document.body元素的引用
	* 文档加载期间，该API的值是null
* document.hasFocus------------------------------该Document是否有各自的焦点
* document.hasFocus()----------------------------检测文档或元素是否获取了焦点
