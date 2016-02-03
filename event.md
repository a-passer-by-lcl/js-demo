#event对象
* CAPTURING-PHASE---------------------当前事件阶段为捕获阶段(3)1
* AT-TARGET---------------------------当前事件是目标阶段,在评估目标事件(1)
* BUBBLING-PHASE----------------------当前的事件为冒泡阶段 ()3

* event.bubbles---------------------返回布尔值，指示事件是否是起泡事件类型
* event.cancelable------------------返回布尔值，指示事件是否可拥可取消的默认动作
* event.currentTarget---------------返回其事件监听器触发该事件的元素
* event.eventPhase------------------返回事件传播的当前阶段
* event.target----------------------返回触发此事件的元素（事件的目标节点）
* event.timeStamp-------------------返回事件生成的日期和时间
* event.type------------------------返回当前 Event 对象表示的事件的名称

####标准 Event 方法
* 下面列出了 2 级 DOM 事件标准定义的方法
* IE 的事件模型不支持这些方法
* event.initEvent()-----------------初始化新创建的 Event 对象的属性
* event.preventDefault()------------通知浏览器不要执行与事件关联的默认动作
* event.stopPropagation()-----------不再派发事件

目标事件对象
* event.addEventListener()----------允许在目标事件中注册监听事件(IE8 = attachEvent())
* event.dispatchEvent()-------------允许发送事件到监听器上 (IE8 = fireEvent())
* event.removeEventListener()-------运行一次注册在事件目标上的监听事件(IE8 = detachEvent())

事件监听对象
* event.handleEvent()---------------把任意对象注册为事件处理程序
文档事件对象
* event.createEvent()

鼠标/键盘事件对象
* event.altKey----------------------返回当事件被触发时，"ALT" 键是否被按下
* event.ctrlKey---------------------返回当事件被触发时，"CTRL" 键是否被按下
* event.metaKey---------------------返回当事件被触发时，"meta" 键是否被按下
* event.shiftKey--------------------返回当事件被触发时，"SHIFT" 键是否被按下

* event.button----------------------返回当事件被触发时，哪个鼠标按钮被点击

* event.pageX-----------------------返回当事件被触发时，鼠标指针相对于浏览器页面的水平坐标
* event.pageY-----------------------返回当事件被触发时，鼠标指针相对于浏览器页面的垂直坐标
* event.clientX---------------------返回当事件被触发时，鼠标指针相对于浏览器视口的水平坐标
* event.clientY---------------------返回当事件被触发时，鼠标指针相对于浏览器视口的垂直坐标
* event.screenX---------------------返回当事件被触发时，鼠标指针相对于电脑屏幕的水平坐标
* event.screenY---------------------返回当事件被触发时，鼠标指针相对于电脑屏幕的垂直坐标

* event.Location--------------------返回按键在设备上的位置3
* event.charCode--------------------返回onkeypress事件触发键值的字母代码
* event.key-------------------------在按下按键时返回按键的标识符3
* event.keyCode---------------------回onkeypress事件触发的键的值的字符代码，或者 onkeydown 或 onkeyup 事件的键的代码
* event.which-----------------------返回onkeypress事件触发的键的值的字符代码，或者 onkeydown 或 onkeyup

事件的键的代码
* event.relatedTarget---------------返回与事件的目标节点相关的节点
* event.initMouseEvent()------------初始化鼠标事件对象的值
* event.initKeyboardEvent()---------初始化键盘事件对象的值
* event.relatedTarget---------------返回与事件的目标节点相关的节点

####IE浏览器支持的属性
* event.cancelBubble----------------如果事件句柄想阻止事件传播到包容对象，必须把该属性设为 true
* event.keyCode---------------------该属性声明了被敲击的键生成的 Unicode 字符码
* event.offsetX---------------------发生事件的地点在事件源元素的坐标系统中的 x 坐标
* event.offsetY---------------------发生事件的地点在事件源元素的坐标系统中的 y 坐标
* event.returnValue-----------------如果设置了该属性，它的值比事件句柄的返回值优先级高把这个属性设置为fasle，可以取消发生事件的源元素的默认动作
* event.srcElement------------------对于生成事件的 Window 对象、Document 对象或 Element 对象的引用
* event.fromElement-----------------保存了 mouseover 事件的相关元素，获取获得焦点的相关元素
* event.toElement-------------------保存了 mouseout 事件的相关元素，获取失去焦点的相关元素
* event.x---------------------------事件发生的位置的 x 坐标
* event.y---------------------------事件发生的位置的 y 坐标
