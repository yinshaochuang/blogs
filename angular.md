## angular
### 1.controller  
#### 1). conttroller使用过程的注意点
> 不要试图去复用controller一个控制器一般只负责一小块视图  
> 不要在控制器中操作dom，这不是控制器的职责  
> 不要再controller里面做数据格式化，ng有很好的表单控件  
> 不要在controller里面做数据过滤操作，ng有$filter服务  
> 一般来说controller是不会互相调用的，控制器之间会通过事件实现交互  

### 2. angual四大核心特性  
#### 1). [mvc](https://github.com/yinshaochuang/blogs/blob/master/mvc.md)  
#### 2). 模块化和依赖注入  
#### 3). 双向数据绑定  
#### 4). 指令  
> angular内置的指令
>> 1 restrict -- 匹配模式
E ---- 元素  
A ---- 属性  
C ---- class（类名）  
M ---- 注释  
推荐使用元素和属性的方式使用指令  
>> 2 template -- 模版  
templateUrl  
templateCache
replace
transclude