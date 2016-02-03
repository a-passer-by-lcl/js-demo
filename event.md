#event对象
* 当触发某个事件时，会产生一个事件对象event，此对象包含所有与事件有关的信息
* 即包括导致事件的元素、事件的类型、以及其他特定事件相关的信息
* DOM中的事件对象
* CAPTURING-PHASE---------------------当前事件阶段为捕获阶段(3)1
* AT-TARGET---------------------------当前事件是目标阶段,在评估目标事件(1)
* BUBBLING-PHASE----------------------当前的事件为冒泡阶段 ()3

####event属性
* event.type----------------------------返回触发事件的类型(string)（只读）
* event.target--------------------------返回触发事件的元素(element)（只读）
* event.bubbles-------------------------返回布尔值，表明事件是否冒泡(Boolean)（只读）
* event.cancelable----------------------返回布尔值，表明是否可以取消事件的默认行为(Boolean)（只读）
* event.detail--------------------------与事件相关的细节信息（只读）
* event.eventPhase----------------------调用事件处理程序的阶段：1、表示捕获阶段；2、表示处于目标阶段；3、表示冒泡阶段（只读）
* event.view----------------------------返回事件关联的抽象视图，等同于发生事件的Window对象（只读）
* event.trusted-------------------------当为ture时，表示事件是浏览器生成的，当为false表示事件是由开发人员通过javascript创建的（DOM新增）（Boolean）（只读）
* event.currentTarget-------------------其事件处理程序当前正在处理事件的那个元素（element）（只读）
* event.defaultPrevented----------------当返回ture时，表示已经调用了preventDefault()方法（Boolean）（只读）
* event.currentTarget-------------------返回其事件监听器触发该事件的元素
* event.eventPhase----------------------返回事件传播的当前阶段
* event.timeStamp-----------------------返回事件生成的日期和时间
* event.Location------------------------返回按键在设备上的位置3
* event.button--------------------------返回当事件被触发时，哪个鼠标按钮被点击
* event.charCode------------------------返回onkeypress事件触发键值的字母代码
* event.key-----------------------------在按下按键时返回按键的标识符3
* event.keyCode-------------------------回onkeypress事件触发的键的值的字符代码，或者 onkeydown 或 onkeyup 事件的键的代码
* event.which---------------------------返回onkeypress事件触发的键的值的字符代码，或者 onkeydown 或 onkeyup

* event.altKey--------------------------返回当事件被触发时，"ALT" 键是否被按下
* event.ctrlKey-------------------------返回当事件被触发时，"CTRL" 键是否被按下
* event.metaKey-------------------------返回当事件被触发时，"meta" 键是否被按下
* event.shiftKey------------------------返回当事件被触发时，"SHIFT" 键是否被按下

* event.pageX---------------------------返回当事件被触发时，鼠标指针相对于浏览器页面的水平坐标
* event.pageY---------------------------返回当事件被触发时，鼠标指针相对于浏览器页面的垂直坐标
* event.clientX-------------------------返回当事件被触发时，鼠标指针相对于浏览器视口的水平坐标
* event.clientY-------------------------返回当事件被触发时，鼠标指针相对于浏览器视口的垂直坐标
* event.screenX-------------------------返回当事件被触发时，鼠标指针相对于电脑屏幕的水平坐标
* event.screenY-------------------------返回当事件被触发时，鼠标指针相对于电脑屏幕的垂直坐标

####事件的键的代码
* event.relatedTarget-------------------返回与事件的目标节点相关的节点
* event.initMouseEvent()----------------初始化鼠标事件对象的值
* event.initKeyboardEvent()-------------初始化键盘事件对象的值
* event.relatedTarget-------------------返回与事件的目标节点相关的节点

####event方法
* document.createEvent(type)------------创建一个新的事件，随之必须调用自身的 init 方法进行初始化（只读）
* Event.initEvent()---------------------用于初始化事件创建使用的价值（只读）
* event.stopPropagetion()---------------取消事件的进一步捕获或冒泡，如果bubbles为 true，则使用此方法（只读）
* event.preventDefalt()-----------------取消事件的默认行为，如果cancelables是 true，则可以用此方法（只读）
* event.stopImmediatePropagation()------取消事件的进一步捕获或冒泡，同时阻止任何事件处理程序被调用（DOM3新增）（只读）
* 在事件处理程序内部，this始终等于currentTarget的值，target则包含事件的实际目标
* 如果直接将事件处理程序指定给目标元素，则this，currentTarget,target包含相同的值
* event.initEvent()---------------------初始化新创建的 Event 对象的属性
* event.preventDefault()----------------通知浏览器不要执行与事件关联的默认动作
* event.stopPropagation()---------------不再派发事件

####目标事件对象
* event.addEventListener()--------------允许在目标事件中注册监听事件(IE8 = attachEvent())
* event.dispatchEvent()-----------------允许发送事件到监听器上 (IE8 = fireEvent())
* event.removeEventListener()-----------运行一次注册在事件目标上的监听事件(IE8 = detachEvent())

####事件监听对象
* event.handleEvent()-------------------把任意对象注册为事件处理程序
文档事件对象
* event.createEvent()

* IE中的方法与属性
* event.type----------------------------返回触发事件的类型（string）（只读）
* event.returnValue---------------------默认为true，将其设置为false则可以取消事件的默认行为（可读写）（==vent.stopPropagetion()）
* event.srcElement----------------------返回触发事件的元素(element)（只读）（==vent.stopPropagetion()）
* event.cancelBubble--------------------默认为true，将其设置为false则可以取消事件冒泡（知道）
* event.cancelBubble--------------------如果事件句柄想阻止事件传播到包容对象，必须把该属性设为 true
* event.keyCode-------------------------该属性声明了被敲击的键生成的 Unicode 字符码
* event.offsetX-------------------------发生事件的地点在事件源元素的坐标系统中的 x 坐标
* event.offsetY-------------------------发生事件的地点在事件源元素的坐标系统中的 y 坐标
* event.returnValue---------------------如果设置了该属性，它的值比事件句柄的返回值优先级高把这个属性设置为fasle，可以取消发生事件的源元素的默认动作
* event.srcElement----------------------对于生成事件的 Window 对象、Document 对象或 Element 对象的引用
* event.fromElement---------------------保存了 mouseover 事件的相关元素，获取获得焦点的相关元素
* event.toElement-----------------------保存了 mouseout 事件的相关元素，获取失去焦点的相关元素
* event.x-------------------------------事件发生的位置的 x 坐标
* event.y-------------------------------事件发生的位置的 y 坐标

####跨浏览器的事件对象
```javascript
(function(window, document) {
	'use strict';
	var EventUtil = {
		addHandler: function(element, type, handler){
			if (element.addEventListener){
				element.addEventListener(type, handler, false);
			} else if(element.attachEvent){
				element.attachEvent("on"+ type, handler);
			} else {
				element["on" +type] = handler;
			}
		},

		removeHandler: function(element, type, handler){
			if (element.removeEventListener){
				element.removeEventListener(type, handler, false);
			} else if(element.detachEvent){
				element.detachEvent("on"+ type, handler);
			} else {
				element["on" +type] = handler;
			}
		},
		//返回对event对象引用
		getEvent: function(event){
			return event ? event : window.event;
		},
		//返回事件的触发目标
		getTarget: function(event){
			return event.target || event.srcElement;
		},
		//取消事件的默认行为
		preventDefault： funtion(event){
			if (event.preventDefault){
				event.preventDefault();
			} else {
				event.returnValue = false;
			}
		},
		//立即停止事件在DOM中的传播
		stopPropagetion: function(event){
			if (event.stopPropagetion){
				event.stopPropagetion();
			} else {
				event.cancelBubble = true;
			}
		},
		//获取mouseover和mouseout相关元素
		getRelatedTarget:function(event){
		    if (event.relatedTarget){
		        return event.relatedTarget;
		    } else if(event.toElement){
		    	//兼容IE8-
		        return event.toElement;
		    } else if(event.formElement){
		        return event.formElement;
		   	} else{
		        return null;
		    }
		},
		//获取mousedown或mouseup按下或释放的按钮是鼠标中的哪一个
		getButton:function(event){
		    if (document.implementation.hasFeature("MouseEvents","2.0")){
		        return event.button;
		    }else{
		        switch(event.button){
		        //将IE模型下的button属性映射为DOM模型下的button属性
		        case 0:
		        case 1:
		        case 3:
		        case 5:
		        case 7:
		            return 0;
		            //按下的是鼠标主按钮（一般是左键）
		        case 2:
		        case 6:
		            return 2;
		            //按下的是中间的鼠标按钮
		        case 4:
		            return 1;
		            //鼠标次按钮（一般是右键）
		        }
		    }
		},
		//获取表示鼠标滚轮滚动方向的数值
		getWheelDelta:function(event){
		    if (event.wheelDelta){
		       	return event.wheelDelta;
		    } else{
		        return -event.detail*40;
		    }
		},
		//以跨浏览器取得相同的字符编码，需在keypress事件中使用
		getCharCode:function(event){
		    if (typeof event.charCode=="number"){
		        return event.charCode;
		    } else{
		        return event.keyCode;
		    }
		}
	};

	var btn = document.document.querySelector("#btn");

	var handler = function() {
		console.log("我是跨浏览器的事件处理程序");
		event = EventUtil.getEvent(event);      //只要使用跨浏览器的事件对象必须传入的该语句

		vat target = EventUtil.getTarget(event);
	};

	EventUtil.addHandler(btn, "click", handler);
})(window, window.document);
```
