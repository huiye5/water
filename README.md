# water - 笔记积累

##1.写一个事件添加器
```javascript
//拆分应用层逻辑
var MyApplication = {
    handleClick:function(event){
        this.showPopup(event);
    },
    
    showPopup:function(event){
        var popup = document.getElementById("popup");
        popup.style.left = event.clientX + "px";
        popup.style.top = event.clientY + "px";
    }
}
addEventListener(element, "click", function(){
    MyApplication.handleClick(event);
});
```