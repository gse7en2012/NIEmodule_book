# Banner切换 #
> Banner切换模块，包括两种，一种是switch，一种是click（也就是图片幻灯片）


----------

## 输出效果 ##

<iframe src="http://jsbin.com/rawop/1/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>


## html ##
    <!--Switch切换-->
    <section class="fSwitch">
        <div class="fSwitchPic">
            <a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/2/10/2014-02-10_417869.jpg" alt="哈哈哈哈啊"/></a>
            <a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/2/12/2014-02-12_418317.jpg" alt="哈哈哈哈啊"/></a>
            <a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/2/10/2014-02-10_417863.jpg" alt="哈哈哈哈啊"/></a>
            <a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/1/30/2014-01-30_417281.jpg" alt="哈哈哈哈啊"/></a>
        </div>
        <div class="fSwitchNav"></div>
    </section>

    <!--click切换-->
    <section id="slideShow">
        <div id="slideWrap">
            <ol class="g-clr">
                <li><a href="javascript:void(0)" class="current"></a></li>
                <li><a href="javascript:void(0)"></a></li>
                <li><a href="javascript:void(0)"></a></li>
                <li><a href="javascript:void(0)"></a></li>
                <li><a href="javascript:void(0)"></a></li>
            </ol>
            <ul class="g-clr">
                <li><img src="http://res.nie.netease.com/xy2/fab/13v3/images/slide1.jpg" alt="" data-pinit="registered"></li>
                <li><img src="http://res.nie.netease.com/xy2/fab/13v3/images/slide2.jpg" alt="" data-pinit="registered"></li>
                <li><img src="http://res.nie.netease.com/xy2/fab/13v3/images/slide3.jpg" alt="" data-pinit="registered"></li>
                <li><img src="http://res.nie.netease.com/xy2/fab/13v3/images/slide4.jpg" alt="" data-pinit="registered"></li>
                <li><img src="http://res.nie.netease.com/xy2/fab/13v3/images/slide5.jpg" alt="" data-pinit="registered"></li>
            </ul>
        </div>
        <div id="slideBtn">
            <a class="g-thide" id="prev">上一张</a>
            <a class="g-thide" id="next">下一张</a>
        </div>
    </section>

## CSS ##
    /*Banner切换*/
    /*--Switch切换*/
    .fSwitch {  width: 255px; height: 235px; overflow: hidden;position:relative;}
    .fSwitchPic { position: relative; width: 255px; height: 235px; }
    .fSwitchPic a { position: absolute; display: block; width:255px; height: 235px; }
    .fSwitchPic a:hover { text-decoration: none; }
    .fSwitchPic a img { display: block; width: 255px; height:235px; }
    .fSwitchPic a span { position: relative; display: block; height: 28px; padding: 0 5px; margin-top: -28px; background: #333; filter: Alpha(opacity=80); opacity: 0.8; color: #fff; line-height: 28px; }
    .fSwitchNav {position:absolute;right:0;bottom:0;height: 14px;padding-right:8px;padding-bottom:8px;z-index: 2; }
    .fSwitchNav a { display: inline-block;*display:inline;*zoom:1;margin-left:6px;width: 14px; height: 14px; background: #000; text-align: center; line-height: 14px; color: #fff; cursor: default;font-size:12px;}
    .fSwitchNav a:hover { background: #d00; }
    .fSwitchNav a.current { background: #d00; }
    /*--click切换*/
    #slideShow{width: 631px;height: 168px;position: relative;*zoom:1;}
    #slideWrap{width: 631px;height: 168px;position: relative;overflow:hidden}
    #slideBtn a{position: absolute;width: 28px;height: 28px;background: url(http://res.nie.netease.com/xy2/fab/13v3/images/slidebtn.png) no-repeat -9999px;z-index: 99;top:65px;cursor: pointer}
    #slideBtn #prev{background-position:0 0;left:-14px}
    #slideBtn #next{background-position:-27px 0;right:-14px}
    #slideShow ul{width: 9999px;position: absolute;top:0;left:0}
    #slideShow li{float: left;}
    #slideShow ul li{width: 631px;}
    #slideShow ul li img{display: block;width: 631px;height: 168px;}
    #slideShow ol{width:120px;position: absolute;bottom: 12px;left: 105px;z-index: 99}
    #slideShow ol li{margin-right: 2px}
    #slideShow ol li a{display: block;width: 10px;height: 10px;background: url(http://res.nie.netease.com/xy2/fab/13v3/images/slidenav.png) no-repeat -10px 0}
    #slideShow ol li a.current{background-position: 0 0}

## Javascript ##
> Switch组件介绍：  
**//简便方式**  
$.Switch("#switch-btn button","#switch-img a","#switch-con a");	  
**//简便方式（不需要内容切换）**  
$.Switch("#switch-btn button","#switch-img a");	     
**//全参数方式**  
//默认情况下  
{  
btnDoms:null,  
imgDoms: null,  
conDoms: null,  
btnEvent: "mouseover",  
"class": "current",  
time: 5000,  
index: 0,  
totalDom:0,  
speed:400  
}  
//btnDoms:按钮Doms，imgDoms：图片Doms，conDoms:其他内容Doms，btnEvent：按钮触发事件，class：全部doms激活的class，time：切换时间，index：默认激活doms索引  
$.Switch({btnDoms:[$("#switch-btn button")],imgDoms:[$("#switch-img a")],conDoms:[$("#switch-con span")]});
  
	$(function(){
	//    scroll
	    scrollPics_tab({
	        currentTarget:'#slideShow',
	        wrap: '#slideWrap',
	        tab: '#slideShow ol a'
	    });
	    nie.use([ 'ui.Switch'], function () {
	//        switch
	        for (var i = 0; i < $(".fSwitchPic a").length; i++) {
	            nums = i + 1;
	            $(".fSwitchNav").append("<a>" + nums + "</a>")
	        }
	        $.Switch(".fSwitchNav a", ".fSwitchPic a");
	    })
	})
	function scrollPics_tab(opt){
	    //只针对一个tab con
	    var settings = {
	                currentTarget: '',
	                autoplay : true,
	                minNum: 1,
	                time: 5000,
	                tab: ''
	            },
	            opt = opt || {};
	    settings = $.extend(settings, opt);
	
	    var $currentTarget = $(settings.currentTarget),
	            $wrap = $(settings.wrap),
	            ul = $wrap.find("ul"),
	            li_len = ul.find("li").length,
	            li_w = ul.find("li").width(),
	            left = $currentTarget.find("#prev"),
	            right = $currentTarget.find("#next"),
	            tab = $(settings.tab),
	            timer = null,
	            currentIndex = 0;
	    tab.eq(currentIndex).addClass('current');
	
	    if(li_len > settings.minNum){
	        right.click(function() {
	            currentIndex++;
	            if(currentIndex == li_len){
	                currentIndex = 0;
	            }
	            tab.removeClass('current').eq(currentIndex).addClass('current');
	
	            ul.stop().animate({
	                "left": -(li_w*currentIndex)
	            }, 300)
	        });
	        left.click(function() {
	            currentIndex--;
	            if(currentIndex < 0){
	                currentIndex = li_len - 1;
	            }
	            tab.removeClass('current').eq(currentIndex).addClass('current');
	
	            ul.stop().animate({
	                "left": -(li_w*currentIndex)
	            }, 300)
	        });
	        tab.click(function(){
	            currentIndex = $(this).index(settings.tab);
	            tab.removeClass('current').eq(currentIndex).addClass('current');
	            ul.stop().animate({
	                "left": -(li_w*currentIndex)
	            }, 300)
	        });
	        if (settings.autoplay) {
	            timer = setInterval(function() {
	                right.trigger("click");
	            }, settings.time);
	            $wrap.mouseenter(function() {
	                clearInterval(timer);
	            })
	            $wrap.mouseleave(function() {
	                clearInterval(timer);
	                timer = setInterval(function() {
	                    right.trigger("click");
	                }, settings.time);
	            })
	        };
	    }
	}
