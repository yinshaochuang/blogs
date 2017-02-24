## 事件委派  
>事件委托的原理：
 事件委托是利用事件的冒泡原理来实现的，何为事件冒泡呢？  
 就是事件从最深的节点开始，然后逐步向上传播事件，  
 举个例子：页面上有这么一个节点树，div>ul>li>a;  
 比如给最里面的a加一个click点击事件，那么这个事件就会一层一层的往外执行，  
 执行顺序a>li>ul>div，有这样一个机制，那么我们给最外面的div加点击事件，  
 那么里面的ul，li，a做点击事件的时候，都会冒泡到最外层的div上，  
 所以都会触发，这就是事件委托，委托它们父级代为执行事件。  
 
>Event对象提供了一个属性叫target，可以返回事件的目标节点，我们成为事件源，  
也就是说，target就可以表示为当前的事件操作的dom，但是不是真正操作dom，  
当然，这个是有兼容性的，标准浏览器用e.target，IE浏览器用event.srcElement，  
此时只是获取了当前节点的位置，并不知道是什么节点名称，  
这里我们用nodeName来获取具体是什么标签名，这个返回的是一个大写的，  
我们需要转成小写再做比较（习惯问题）  
>`<ul>`
     `<li>1</li>`
     `<li>2</li>`
     `<li>3</li>`
     `<li>4</li>`
     `<li>5</li>`
` </ul>`
 
    var ul1 = document.querySelector("ul");
    ul1.onclick = function(e){
        var e = e || window.event;
        var target = e.target || e.srcElement;
        
        if(target.nodeName.toLowerCase() == "li"){
            alert(target.innerHTML);
        }
    }
 
 

 
 