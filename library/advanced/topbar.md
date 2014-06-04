# 顶部功能条 #
> fab专用，可以直接复制整段代码后改样式即可，请滚动看效果，代码添加在最外层


----------
## 输出效果 ##

<iframe src="http://jsbin.com/nofor/1/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>


## html ##

    <div id="ScrollTopBar">
    <a id="ScrollTopLogo" href="http://xy2.163.com" target="_blank">新大话2西游2</a>
    <a class="ScrollTopBtn" href="javascript:void(0)"  id="ScrollTopBtn1">快速注册赢取好金蛋</a>
    <a class="ScrollTopBtn" href="javascript:void(0)"  id="ScrollTopBtn2">立即领取龙马特权礼包</a>	
	</div>

## css ##
    #ScrollTopBar{width: 100%;position: fixed;height: 97px;background: #fdef6c;top: -97px;z-index: 9999;_position:absolute}
    #ScrollTopBar a{display: block;text-indent: -9999px;position: absolute}
    #ScrollTopLogo{width: 225px;height: 90px;background: url(http://res.nie.netease.com/xy2/gw/13v2/images/SrcollTop/xy2TopLogo.jpg) no-repeat;top: 2px;left: 10px}
    .ScrollTopBtn{width: 186px;height: 62px;top: 10px}
    #ScrollTopBtn1{background: url(http://res.nie.netease.com/xy2/gw/13v2/images/SrcollTop/xy2TopBtn1.jpg) no-repeat;right: 10px}
    #ScrollTopBtn2{background:url(http://res.nie.netease.com/xy2/gw/13v2/images/SrcollTop/xy2TopBtn2.jpg) no-repeat;right: 214px }

## Javascript ##
> 需要注意的是添加监测代码  
> **nie.config.stats.url.add('PM单号/trace_添加时间.html?action=click&btn=任意名字','任意名字')**

	$(function(){
        $('#ScrollTopBtn2').click(function(){
            openD('#booktc')
			//添加监测代码
            nie.config.stats.url.add('5280/trace_0121.html?action=click&btn=fastreg','快速注册')
        })
        $('#ScrollTopBtn1').click(function(){
            $("html, body").stop().animate({scrollTop : 140});
            $("#reg1").find('.qr-m_username-inp').focus().css('border','2px solid red');
			//添加监测代码
            nie.config.stats.url.add('5280/trace_0121.html?action=click&btn=lqlb','领取礼包')
        })
        //基本滚动代码
        ScrollTopBar({
            topBarWrap:'#ScrollTopBar',//顶部条的id
            speed:300,//顶部条显示速度
            distance:200 //滚动多少距离后顶部条才显示
        });
    })

    function ScrollTopBar(opt){
        var settings = {
                    topBarWrap:'',//顶部条的id
                    speed:200,//顶部条显示速度
                    distance:0 //滚动多少距离后顶部条才显示
                },
                opt = opt || {};
        settings = $.extend(settings, opt);
        var topBar = $(settings.topBarWrap),h = $(settings.topBarWrap).height();
        $(window).scroll(function(){
            if($.browser.msie && $.browser.version =='6.0'){
                $(window).scrollTop() > settings.distance? topBar.stop().animate({'top':$(window).scrollTop()},settings.speed):topBar.stop().animate({'top':'-'+h+'px'},settings.speed);
            }else{
                $(window).scrollTop() > settings.distance? topBar.stop().animate({'top':0},settings.speed):topBar.stop().animate({'top':'-'+h+'px'},settings.speed);
            }

        })
    }

