# 滚动模块 #
> 滚动模块，横竖皆有，此模块用过多会影响页面效率，请慎用


----------
## 输出效果 ##

<iframe src="http://jsbin.com/gojic/1/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>

## html ##

    <!--竖版滚动-->
    <section class="fMarquee" id="marquee">
        <ul class="mar">
            <li>?下一个开放的合体的系是什么？</li>
            <li>?水生系、厉鬼系技能是否会调整？如何调整？</li>
            <li>?高等级化雪丹的投放途径和更多的聚能丹投放途径有怎样的规划？</li>
            <li>?铁血元魂珠定位问题。</li>
            <li>?尸兵合体是否会调整？</li>
            <li>?什么时候开放85级，经验槽已经满了好久了。</li>
            <li>?16、18钻翅膀能否回归成最原始的样子？</li>
        </ul>
    </section>

    <!--横版滚动-->
    <section class="fMarquee" id="marquee2">
        <ul class="mar g-clr">
            <li>?下一个开放的合体的系是什么？</li>
            <li>?水生系、厉鬼系技能是否会调整？如何调整？</li>
            <li>?高等级化雪丹的投放途径和更多的聚能丹投放途径有怎样的规划？</li>
            <li>?铁血元魂珠定位问题。</li>
            <li>?尸兵合体是否会调整？</li>
            <li>?什么时候开放85级，经验槽已经满了好久了。</li>
            <li>?16、18钻翅膀能否回归成最原始的样子？</li>
        </ul>
    </section>

## css ##
	/*滚动模块*/
    .fMarquee {position:relative;width:275px;height:158px;overflow:hidden;}
    .fMarquee .mar {position:relative;width:275px;}
    #marquee2{height: 30px}
    #marquee2 ul{width: 9999px}
    #marquee2 li{float: left}

## Javascript ##
> $.marquee2 ( dom , direction , [data] )  
**Parameters:**
dom <Jquery Object|String> 需要滚动的dom  
direction <String> 滚动方向："left","right","top","bottom"  
[data] <Object> 选填参数：有speed（速度 ms/px,移动每像素的毫秒数，默认值为**40**）  

	nie.use(["ui.marquee2"], function () {
        //        滚动模块
        if($("#marquee li").length > 3){
            $.marquee2("#marquee","top");
        }
        $.marquee2("#marquee2","left");
    })

