# 弹层合集（普通弹层、flash弹层、视频弹层） #
> 弹层插件，可以控制弹层的大小、传入flash地址，和flash的wmode，视频地址


----------
## 输出效果 ##


> jsbin不知道为啥不支持flash，大家可以直接下载temple试试看

<iframe src="http://jsbin.com/cuduk/2/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>

## html ##

	<!--普通弹层-->
	<div class="dTc" id="shareTc" style="display:none">
	    <h3 class="hide">分享赢龙马，送贴心防雾霭口罩</h3>
	    <a class="aCloseQ" href="javascript:void(0)"></a>
	</div>
	<!--flash弹层-->
	<div id="flashtc1" class="dTc" style="display:none">
	    <a href="javascript:void(0)" class="aCloseQ"></a>
	    <div id="flash-wrap"></div>
	</div>
	<!--视频弹层-->
	<div class="dTc videoBox" id="videoShow" style="display: none">
	    <a class="aCloseQ" title="关闭">关闭</a>
	    <div class="dialogCon">
	        <div class="dVideoBox"><div id="dVideo"></div></div>
	    </div>
	</div>

## css ##
    /*弹层蒙版*/
    .dTc{position:absolute;zoom:1;top:200px;z-index:999999}
    .aCloseQ{display:block;position:absolute;right:21px;top:27px;width:20px;height:20px;cursor:pointer;text-indent: -9999px}
    #NIE-overlayer{display:none;position:absolute;width:100%;height:100%;background:#000;filter:alpha(opacity=80);opacity:.8;top:0;left:0;z-index:99}
    /*视频弹层*/
    .videoBox {background: #000;}
    .videoBox .dialogCon {overflow: hidden;padding: 5px;}
    .videoBox .dVideoBox {border: 1px solid #999;padding: 4px;background: #666;}
    .videoBox .aCloseQ {position: absolute;width: 57px;height: 57px;display: block;right: -57px;top: 0;cursor: pointer;overflow: hidden;text-indent: -9999px;background: url(http://res.nie.netease.com/tx3/gw/13v1/images/close.jpg) no-repeat 0 0;}

## Javascript ##
1. 调用相关js  
<pre>
$(function(){
    //-----------以下为普通弹层示例
    $('#pop1').click(function(){
        openD({
            id: '#shareTc',//弹出的弹层id
            type : '1'//1为普通弹层，2为flash弹层，3为视频弹层
        })
    })
    //-----------以下为flash弹层示例
    $('#pop2').click(function(){
        openD({
            id: '#flashtc1',//弹出的弹层id
            type : '2',//1为普通弹层，2为flash弹层，3为视频弹层
            width: '960',//弹层宽度
            height: '600',//弹层高度
            flashurl:'http://res.nie.netease.com/xy2/qt/14/0109_biwu/pop.swf',//弹层所需的flash地址
            wmode: 'opaque'
        })
    })
    //-----------以下为视频弹层示例
    $('#pop3').click(function(){
        openD({
            id: '#videoShow',//弹出的弹层id
            type : '3',//1为普通弹层，2为flash弹层，3为视频弹层
            width: '800',//弹层宽度
            height: '450',//弹层高度
            videourl:'http://v.nie.netease.com/tx3/2013/1231/longwu.f4v'//弹层所需的flash地址
        })
    })

})
//flash自己内部调用的函数
var closeMe = function(){
    $("#NIE-overlayer").hide();
    $('.aCloseQ').show();
    $('#flashtc1').hide();
}
</pre>

2. 弹层封装好的js（会有些累赘，因为考虑到各种情况，可能官网类比较适用，而且还有可优化的地方）
<pre>
//弹层
//--这个函数是将三种基本弹层合在一体的，所以代码会比较长一些，可以根据需求自己独立出来相对应的弹层代码
function openD(opt){
//只针对一个tab con
var settings = {
            id: '',
            type : '',//1为普通弹层，2为flash弹层，3为视频弹层
            width: '',//2和3需要使用
            height: '',//2和3需要使用
            flashurl:'',//2需要使用，flash地址
            videourl:'',//3需要使用，视频地址
            wmode: '',//2和3可能需要使用
            startImg:''//3需要使用，视频截图
        },
        opt = opt || {};
settings = $.extend(settings, opt);

var popbg = $("#NIE-overlayer"),
        popid = $(settings.id),
        type = settings.type,
        w =parseInt(settings.width),
        h = parseInt(settings.height),
        vimg = settings.startImg,
        furl = settings.flashurl,
        vurl = settings.videourl,
        wmode = settings.wmode,
        dh = $(document).height(),
        wh = $(window).height(),
        ww = $(window).width(),
        st = $(window).scrollTop(),
        sl = $(window).scrollLeft();
// 蒙版弹出
popbg.css({"height":dh}).show();
// 弹层弹出
function posPop(idname){
    idname.height()>wh?idname.fadeIn().css({'top':st,'left':(ww-idname.width())/2+sl}):idname.fadeIn().css({'top':(wh-idname.outerHeight())/2+st,'left':(ww-idname.outerWidth())/2+sl});
}
//  弹层关闭
$('.aCloseQ').click(function(){
    $(this).parent().fadeOut();
    $("#NIE-overlayer").hide();
});
//判断弹层类别
switch (type){
    case '1':
        posPop(popid);
        break;
    case '2':
        $('#flash-wrap').html('');
        nie.use(["util.swfobject"], function () {
            $('#flash-wrap').flash({
                swf:furl,
                width:w,
                height:h,
                allowScriptAccess:'always',
                wmode:wmode
            });
        })
        var obj = $('#flashtc1');
        obj.css({'width':w,'height':h});
        $('.aCloseQ').hide();//flash本身有做关闭按钮
        posPop(popid);

        break;
    case '3':
        $('#dVideo').html('').css({'height':h+'px','width':w+'px'});
        popid.css({'height':h+22+'px','width':w+22+'px'});
        posPop(popid);
        nie.use(['nie.util.video'], function () {
            nie.util.video($('#dVideo'),{
                movieUrl:vurl,
                mp4_movieUrl:vurl.replace(/\.(flv|f4v)/,'.mp4'),
                width:w,
                height:h,
                startImg:vimg,
                bufferTime:5,
                loopTimes:0,
                wmode:"opaque",
                volume:0.8,
                autoPlay:true
            });
        })
        break;
    default :break;
}

}
</pre>


