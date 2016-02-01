#element方法

####Node的属性
* element.nodeType----------------显示节点的类型(String)
* element.nodeName----------------显示节点的名称(String)
* element.nodeValue---------------显示节点的值(String)
* element.childNodes--------------表示该节点的所有子节点(NodeList)
* element.parentNode--------------表示所在节点的父节点(node)
* element.firstChild--------------表示某一节点的第一个节点(node)
* element.lastChild---------------表示某一节点的最后一个子节点(node)
* element.nextSibling-------------紧挨着当前节点的下一个节点(node)
* element.previousSibling---------紧挨着当前节点的上一个节点(node)
* element.nextSibling-------------如果节点是兄弟节点，该值为null
* element.previousSibling---------如果节点是兄弟节点，该值为null
* element.childNodes.length-------查看长度
	* 每个节点都有一个childNodes属性，它保存有NodeList对象(类似于数组对象)，用于保存一组有序节点

####node方法
* element.childNodes.item(index)--------------访问节点位置
* element.hasChildNodes()---------------------判断节点是否有子节点,返回布尔值
* element.appendChild(child)------------------节点末尾添加子节点
* element.insertBefore(newChild,refChild)-----在指定节点之前插入子节点
* element.replaceChild(newChild,oldChild)-----替换指定结点的子结点
* element.removeChild(child)------------------移除指定结点的子结点
* element.cloneNode()-------------------------复制节点
	* 当参数为true时，复制整个节点以及子节点树，当无参时，只复制节点本身
* element.normalize()-------------------------使得此成为一个"normal"的形式
	* 其中只有结构（如元素，注释，处理指令，CDATA节和实体引用）隔开Text节点，即元素（包括属性）下面的所有文本节点，既没有相邻的文本节点也没有空的文本节点


####Attribute方法
* element.hasAttribute(attributeName)-------------若元素中有指定的属性返回true，否则false(Boolean)
* element.hasAttributes(node)---------------------如果元素有属性返回ture，否则false(Boolean)
* element.getAttribute(attributeName)-------------返回指定属性的值(String)
* element.setAttribute(attributeName,value)-------添加或者改变属性的属性值(String)
* element.removeAttribute(attributeName)----------移除指定属性和属性值(String)
* element.getAttributeNode(attributeName)---------返回指定属性节点(Attr object)
* element.setAttributeNode(attributenode)---------设置或改变指定属性节点(Attr object)
* element.removeAttributeNode(attributenode)------删除指定属性节点并返回移除后的节点(Attr object)

* element.attributes------------------------------返回指定节点的属性数组(nodeMap)
* element.attributes.length-----------------------返回集合中节点的数量
	* Node 对象的属性是 NamedNodeMap 对象的实例
* element.attributes[index].isId------------------若属性是 id 类型，则返回 true，否则返回 false
* element.attributes[index].specified-------------若已指定属性，则返回 true，否则返回 false
	* 如果已创建该属性但尚未添加到元素中，也会返回 true；否则返回 false

* element.attributes[index]-----------------------返回指定节点该索引下的属性以及属性值(String)
	* item() 方法以 Node 对象返回 namedNodeMap 中位于指定索引的节点
* element.attributes.item(index)------------------返回指定节点该索引下的属性以及属性值(node)
* element.attributes[index].value-----------------返回指定节点该索引下的属性值(String)
* element.attributes.item(index).value------------返回指定节点该索引下的属性值(node)
* element.attributes[index].name------------------返回指定节点该索引下的name属性名称(String)
* element.attributes.item(index).name-------------返回指定节点该索引下的name属性名称(node)
* element.attributes.getNamedItem(node)-----------返回指定节点中具有指定名称的属性节点(node)
* element.attributes.removeNamedItem(node)--------返回指定节点中带有指定名称的节点(node)
* element.attributes.setNamedItem(node)-----------设置指定节点中指定的属性节点(node)


####HTML元素
* element.tabIndex--------------------------------设置或返回元素的标签顺序
* element.id--------------------------------------设置或返回某元素的ID
* element.innerHTML-------------------------------设置或返回某元素的内容(html)
* element.textContent-----------------------------设置或返回某元素文本内容(text)
* element.title-----------------------------------设置或返回元素的title属性
* element.style.css属性---------------------------设置或返回元素的样式属性
* element.dir-------------------------------------设置或返回某元素中的文本方向
* element.lang------------------------------------设置或返回某元素的语言
* element.tagName---------------------------------返回以字符串形式表示的某个元素的大写标签名
* element.namespaceURI----------------------------返回命名空间的url
* element.contentEditable-------------------------设置或返回元素的内容是否可编辑
* element.accessKey-------------------------------设置或返回accesskey一个元素
* element.compareDocumentPosition()---------------比较两个元素的文档位置
* element.addEventListener()----------------------向指定元素添加事件句柄
* element.setUserData()---------------------------在元素中为指定键值关联对象
* element.removeEventListener()-------------------移除由addEventListener() 方法添加的事件句柄
* element.toString()------------------------------将一个元素转换成字符

* element.selectNodes-----------------------------对节点进行指定的匹配,并返回匹配节点列表
* element.selectSingleNode------------------------对节点进行指定的匹配,并返回第一个匹配节点
* element.transformNode---------------------------使用指定的样式表对节点及其后代进行转换
* element.transformNodeToObject-------------------使用指定的样式表将节点及其后代转换为对象
####宽高操作
* element.clientHeight----------------------------返回某元素的可视高度(content+padding)
* element.clientWidth-----------------------------返回某元素的可视高度(content+padding)
* element.clientLeft------------------------------返回某元素border宽度
* element.clientTop-------------------------------返回某元素border高度

* element.offsetParent----------------------------返回当前对象的上级层对象
* element.offsetLeft------------------------------返回某元素到其上级层左边的距离
* element.offsetTop-------------------------------返回某元素到其上级层顶部的距离
* element.offsetHeight----------------------------返回某元素的高度(content+padding+border)
* element.offsetWidth-----------------------------返回某元素的宽度(content+padding+border)

* element.scrollLeft------------------------------返回当前视图中的实际元素的左边缘和左边缘之间的距离
* element.scrollTop-------------------------------返回当前视图中的实际元素的顶部边缘和顶部边缘之间的距离
* element.scrollWidth-----------------------------返回元素的整个宽度（包括带滚动条的隐蔽的地方）
* element.scrollHeight----------------------------返回整个元素的高度（包括带滚动条的隐蔽的地方）

####判断
* element.isContentEditable-----------------------如果元素内容可编辑返回 true，否则返回false
* element.isDefaultNamespace()--------------------如果指定了namespaceURI 返回 true，否则返回 false
* element.isEqualNode()---------------------------检查两个元素是否相等
* element.isSameNode()----------------------------检查两个元素所有有相同节点
* element.isSupported()---------------------------如果在元素中支持指定特征返回 true
* element.setUserData()---------------------------在元素中为指定键值关联对象



###HTML5新加API
* element.childElementCount----------------------返回子元素的个数(不包括文本节点以及注释)
* element.firstElementChild----------------------返回第一个子元素
* element.lastElementChild-----------------------返回最后一个子元素
* element.nextSibling----------------------------指向前一个同辈元素
* element.previousSibling------------------------指向后一个同辈元素
* element.focus()--------------------------------设置文档或某元素获取焦点

####class方法与属性
* element.classList-------------------------------返回元素的类名(数组)
* element.className-------------------------------设置或返回元素的class属性
* element.classList.length------------------------返回类列表中类的数量
* element.classList.add(classN)-------------------在元素中添加N个类名
* element.classList.contains(class)---------------判断指定的类名是否存在
* element.classList.item(index)-------------------返回该索引值值下的类名
* element.classList.remove(classN)----------------移除元素中N个类名
* element.classList.toggle(class, Boolean)--------在元素中切换类名
	* 第一个参数为要在元素中移除的类名，并返回 false;
	* 如果该类名不存在则会在元素中添加类名，并返回 true
	* 第二个是可选参数，是个布尔值用于设置元素是否强制添加或移除类，不管该类名是否存在
	* 移除一个class: element.classList.toggle("classToRemove", false);
	* 添加一个class: element.classList.toggle("classToAdd", true);
