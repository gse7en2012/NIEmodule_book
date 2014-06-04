# 新闻列表 #
> 简单的新闻列表模块，包括栏目名称、新闻标题、发布时间


----------
## 输出效果 ##
> 非响应式，后期可以做优化

<iframe src="http://jsbin.com/papek/2/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>


## html ##

    <section class="ftxtList">
        <ul class="fListWrap">
            <li><span class="sChannel"><a href="/news/" target="_blank">新闻</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
            <li><span class="sChannel"><a href="/news/" target="_blank">新闻</a></span><span class="sTitle"><a href="#" target="_blank" class="tRed">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
            <li><span class="sChannel"><a href="/news/" target="_blank">新闻</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
            <li><span class="sChannel"><a href="/news/" target="_blank">新闻</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
            <li><span class="sChannel"><a href="/news/" target="_blank">新闻</a></span><span class="sTitle"><a href="#" target="_blank">金钱产出增加新途径 大话2游戏处处有钱拿</a></span>[01-27]</li>
        </ul>
    </section>

## css ##
    /*新闻列表*/
    .ftxtList{overflow: hidden}
    .fListWrap{margin-bottom: -1px}
    .fListWrap li{height: 20px;padding: 5px 10px 4px 0;border-bottom: 1px dotted #7d858a;line-height: 20px;text-align: right;}
    .fListWrap li span {float: left;display: block;height: 20px;overflow: hidden;}
    .fListWrap li .sChannel{width: 66px;margin-right: 35px;background: #72a547;text-align: center;}
    .fListWrap li .sChannel a{color: #fff}
    .fListWrap li .sTitle {width: 260px;text-align: left;}

