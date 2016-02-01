#HTML5新加API

###自定义数据属性
* data-name，目的是为元素提供与渲染无关的信息，或者提供语义信息，可以任意的添加，命名
* 若要访问自定义的属性，需通过dataset属性来进行访问自定义属性的值
* dataset属性的值是DOMStringMap的一个实例，即一个名值对的映射
* 在该映射中，每个data-name形式的属性都会有一个与之对应的属性值
* 语法: element.dataset.name(data-name中的name)

###Document
* document.getElementsByClassName()--------------用class类获取元素，用这个方法可以查询任何带有class属性且带有符合该class参数值的元素和Document对象（例如：SVG和MathML）
* document.activeElement-------------------------声明哪个元素是当前的焦点元素
	* 默认情况下，该API中保存的是document.body元素的引用
	* 文档加载期间，该API的值是null
* document.hasFocus------------------------------该Document是否有各自的焦点
* document.hasFocus()----------------------------检测文档或元素是否获取了焦点
* document.charset-------------------------------设置或返回charset（当前文档的字符集）
* document.defaultCharset-------------------------根据默认浏览器或系统设置，当前文档默认的字符集是什么

###Element
* element.childElementCount----------------------返回子元素的个数(不包括文本节点以及注释)
* element.firstElementChild----------------------返回第一个子元素
* element.lastElementChild-----------------------返回最后一个子元素
* element.nextSibling----------------------------指向前一个同辈元素
* element.previousSibling------------------------指向后一个同辈元素
* element.focus()--------------------------------设置文档或某元素获取焦点
* element.innerHTML------------------------------返回与调用元素的所有子节点对应的HTML标记(只读)
* element.innerHTML------------------------------根据指定的HTML字符串创建新的DOM子树，然后用这个DOM子树完全替换调用元素原先的所有子节点(可读写)
* element.outerHTML------------------------------返回调用该元素以及所有子节点的HTML标签(只读)
* element.outerHTML------------------------------根据指定的HTML字符串创建新的DOM子树，然后用这个DOM子树完全替换调用元素（可读写）

####element.insertAdjacentHTML属性
* element.insertAdjacentHTML("插入位置", "要插入的HTML代码");
* element.insertAdjacentHTML("beforebegin", "HTMLString")---在当前元素之前插入一个紧邻的同辈元素
* element.insertAdjacentHTML("afterbegin", "HTMLString")----在当前元素第一子元素之前插入新的子元素
* element.insertAdjacentHTML("beforeend", "HTMLString")-----在当前元素最后一子元素之前插入新的子元素
* element.insertAdjacentHTML("afterend", "HTMLString")------在当前元素之后插入一个紧邻的同辈元素

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

####滚动scrollIntoView方法
* element.scrollIntoView()------------------------可以在所有HTML元素上调用，通过滚动浏览器窗口或某个容器元素，调用元素就可以出现在视口中
* 如果给这个方法传入true作为参数，或者不传入任何参数，那么窗口滚动之后会让调用元素的顶部与视口顶部尽可能平
* 如果传入false作为参数，调用元素会尽可能全部出现在视口中，（可能的话，调用元素的底部会与视口顶部平齐）不过顶部不一定平齐
* element.scrollIntoViewIfNeeded(alignCentent)----只有当前在视口不可见的情况下，才滚动浏览器窗口或容器窗口，让其可见，若当前元素可见，则该方法无用，
* 若将aligncontent设置为true，则表示尽量将元素显示在视口垂直方向
* element.scrollByLines(lineCount)----------------将元素的内容滚动制定的行高，lineCount可正可负
* element.scrollByPages(pageCount)----------------将元素的内容滚动到指定页面的高度，具体高度由元素高度决定
