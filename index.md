##事件
    (~~~)
    oBtn.onclick = function(e){
        //获取事件的兼容性写法  e 标准浏览器  window.event ie浏览器
            e = e || window.event;  
        console.log('hahah');
        //阻止默认行为 
            e.preventDefault();  //标准浏览器
            e.returnValue = false;  //ie浏览器
        return false;
    }
    (~~~)
    事件绑定方式:内联绑定 onclick=XXX
                js内绑定
                (~~~)
                XXX.addEventListener{'click',function(){
                    console.log(");
                },false}
                (~~~)
                内联绑定多个事件会被覆盖
                js内可以绑定多个事件不被覆盖

                冒泡与捕获
                    若最后参数为false则为冒泡   文档流由子向父
                    若最后参数为true则为捕获    文档流由父向子

    阻止事件冒泡  标准浏览器
        ~e.stopPropagation();~
    IE浏览器
        ~e.cancelBubble = true;~

