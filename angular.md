## angular
### 1.controller  
#### 1). conttroller使用过程的注意点
> 不要试图去复用controller一个控制器一般只负责一小块视图  
> 不要在控制器中操作dom，这不是控制器的职责  
> 不要再controller里面做数据格式化，ng有很好的表单控件  
> 不要在controller里面做数据过滤操作，ng有$filter服务  
> 一般来说controller是不会互相调用的，控制器之间会通过事件实现交互