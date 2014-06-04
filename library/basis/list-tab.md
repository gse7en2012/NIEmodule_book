# 新闻列表 #
> 简单的新闻列表模块，包括栏目名称、新闻标题、发布时间


----------
## 输出效果 ##


<iframe src="http://jsbin.com/kukam/1/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>

## html ##

    <ul class="fTabNav">
        <li><a href="#">新闻</a></li>
        <li><a href="#">维护</a></li>
        <li><a href="#">公告</a></li>
        <li><a href="#">专题</a></li>
    </ul>
    <div class="fTabCont">
        <section class="ftxtList">
            <ul class="fListWrap">
                <li><span class="sChannel"><a href="/news/" target="_blank">新闻</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">新闻</a></span><span class="sTitle"><a href="#" target="_blank" class="tRed">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">新闻</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">新闻</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">新闻</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
            </ul>
        </section>
        <section class="ftxtList">
            <ul class="fListWrap">
                <li><span class="sChannel"><a href="/news/" target="_blank">维护</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">维护</a></span><span class="sTitle"><a href="#" target="_blank" class="tRed">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">维护</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">维护</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">维护</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
            </ul>
        </section>
        <section class="ftxtList">
            <ul class="fListWrap">
                <li><span class="sChannel"><a href="/news/" target="_blank">公告</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">公告</a></span><span class="sTitle"><a href="#" target="_blank" class="tRed">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">公告</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">公告</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">公告</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
            </ul>
        </section>
        <section class="ftxtList">
            <ul class="fListWrap">
                <li><span class="sChannel"><a href="/news/" target="_blank">专题</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">专题</a></span><span class="sTitle"><a href="#" target="_blank" class="tRed">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">专题</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">专题</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
                <li><span class="sChannel"><a href="/news/" target="_blank">专题</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
            </ul>
        </section>

## css ##
    /*新闻切换*/
	.fTabNav {height:29px;overflow:hidden;background:#23b0eb;}
	.fTabNav li {float:left;width:84px;height:29px;}
	.fTabNav li a {display:block;height:27px;border:2px solid #23b0eb;border-bottom:0;color:#fff;text-align:center;font-size:14px;line-height:27px;}
	.fTabNav li.current a {background:#dff1fb;color:#23b0eb;}
	.fTabCont .ftxtList{display: none}
	.fTabCont .current{display: block}

## Javascript ##
> $.tab ( btnObj , conObj , params )  
**Parameters**:  
btnObj <jquery Object||String> 按钮对象  
conObj <jquery Object||String||Array> 内容对象,如多个可为Array（如：["#more li","#con li"]）  
params <[Objecj]> 选填参数，（time，index，activeClass）。time：鼠标需要停留的时间然后激活（默认值为180毫秒）；index：先打开的索引值（默认值为0）；activeClass：激活按钮和内容的class（默认值为current）；  
**例子：**  
$.tab("#tab li","#con p");  
//鼠标需要停留2000毫秒，然后激活  
$.tab("#tab li","#con p",{time:2000});  
//鼠标需要停留2000毫秒，然后激活；默认激活第二个  
$.tab("#tab li","#con p",{time:2000,index:1});  
//鼠标需要停留2000毫秒，然后激活；默认激活第二个；激活按钮和内容的activeClass="on"  
$.tab("#tab li","#con p",{time:2000,index:1,activeClass:"on"});

	nie.use(["ui.tab"], function () {
	//tab
        $.tab(".fTabNav li", ".fTabCont .ftxtList");

    });

