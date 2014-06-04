# 手机端页面相关规范 #


----------

## 相关规范与结构 ##
> index.html  
> -img  
> -css  
> --page.css  
> -js  
> --page.js

### index.html ###
> 请记得修改相关的分享，易信的在html页面上改就行，微信的在js中改

	<!DOCTYPE HTML>
	<html>
	<head>
	<title>迷你西游之悟空上树节节高</title>
	<meta name="keywords" content="悟空上树节节高" />
	<meta name="description" content="悟空上树节节高" />
	<meta name="format-detection" content="telephone=no"/>
	<meta name="format-detection" content="address=no"/>
	<!--viewport 设置，如果页面实际情况不允许缩放请加上,user-scalable=no-->
	<meta content="target-densitydpi=device-dpi,width=640" name="viewport" />
	<!--项目meta信息，请编辑提供 start-->
	<meta name="author" content="网易，NetEase Inc." />
	<meta name="copyright" content="网易，NetEase Inc." />
	<meta name="pmid" content="276333" />
	<meta name="animator" content="KWG,hy,QC" />
	<!--项目meta信息，请编辑提供 end-->
	<!--易信分享配置 start-->
	<meta name='yixin-share-image' content='http://xym.163.com/share/0529/share.png' />
	<meta name='yixin-share-desc' content='悟空上树节节高' />
	<!--易信分享配置 end-->
	<meta charset="gb2312">
	<link rel="dns-prefetch" href="http://res.nie.netease.com">
	<link type="text/css" rel="stylesheet" href="css/index_m.css" media="all" />
	<script charset="gb2312" src="http://res.nie.netease.com/comm/js/jquery(mixNIE).last.js"></script>
	</head>
	<body>
	<div id="main">
	</div>
	<script charset="gb2312" src="js/index_m.js"></script>
	</body>
	</html>

### css ###
- page.css
<pre>
html{-ms-text-size-adjust:100%;-webkit-text-size-adjust:100%;}
ul,li,div,p,body{margin:0;padding:0;-webkit-user-select: none;-moz-user-select: none;-khtml-user-select: none;user-select: none;text-align:left;}
input{-webkit-appearance:button;}
li{list-style:none;}
a{text-decoration:none;}
.hide{display:none;}
body, html {background:#dbdbdb;text-align: left;height: 100%;width: 100%;font-family: "Microsoft YaHei","Helvetica Neue",Arial, HelveticaNeue, "Helvetica-Neue", Helvetica, "BBAlpha Sans", sans-serif;font-size: 24px;font-weight: normal;display: -webkit-box;-webkit-box-orient: vertical; -webkit-box-align: center;}
*{-webkit-tap-highlight-color:rgba(14,159,111,0.5);-webkit-touch-callout:none;}
body{opacity: 0;-webkit-transition:opacity 500ms ease-in;transition:opacity 500ms ease-in;}
#main{position:relative;width:640px;height:1037px;margin:0 auto;background:url('../images/bg.jpg') repeat-y;background-size:100%;overflow:hidden;display:none;}
</pre>

### js ###

	var shareTitle = '悟空上树节节高';
	var shareTxt = '悟空上树节节高';
	var shareUrl = 'http://xym.163.com/2014/wukong/';
	var sharePic = 'http://xym.163.com/share/0529/share.png';
	var winObj = $(window);
	var isAndroid = /android/i.test(navigator.userAgent.toLowerCase());
	var isWx = /micromessenger/i.test(navigator.userAgent.toLowerCase());
	var isYx = /yixin/i.test(navigator.userAgent.toLowerCase());
	
	$('#main').show();
	$('body').css({'opacity':1});
	
	//给易信设置分享文案
	function setYxShare() {
		var str = shareTxt;
		var meta = document.getElementsByTagName('meta');
		for(var i=0;i<meta.length;i++){
			if(meta[i].getAttribute('name') == "yixin-share-desc"){
				meta[i].setAttribute('content',str);
			}
		}
	}
	function is_weixin(){
		var ua = navigator.userAgent.toLowerCase();
		if(/micromessenger|yixin/i.test(ua)){
			return true;
	 	} else {
			return false;
		}
	}
	//给微信设置分享文案
	var onBridgeReady = function () {
		var appId = '';
		// 发送给好友;
		WeixinJSBridge.on('menu:share:appmessage', function(argv){
			var imgUrl = sharePic;
			var link = shareUrl;
			var title = shareTitle;
			var shareDesc = shareTxt;
			WeixinJSBridge.invoke('sendAppMessage',{
				'img_url' : imgUrl,
				'img_width' : '640',
				'img_height' : '640',
				'link' : link,
				'desc' : shareDesc,
				'title' : title
				}, function(res) {
	
			});
		});
		// 分享到朋友圈;
		WeixinJSBridge.on('menu:share:timeline', function(argv){
			var imgUrl = sharePic;
			var link = shareUrl;
			var title = shareTitle;
			var shareDesc = shareTxt;
			WeixinJSBridge.invoke('shareTimeline',{
			'img_url' : imgUrl,
			'img_width' : '640',
			'img_height' : '640',
			'link' : link,
			'desc' : shareDesc,
			'title' : shareDesc
			}, function(res) {
	
			});
		});
	};
	if(document.addEventListener){
		document.addEventListener('WeixinJSBridgeReady', onBridgeReady, false);
	} else if(document.attachEvent){
		document.attachEvent('WeixinJSBridgeReady' , onBridgeReady);
		document.attachEvent('onWeixinJSBridgeReady' , onBridgeReady);
	}
	//隐藏易信底部条
	document.addEventListener('YixinJSBridgeReady', function onBridgeReady() {
	    YixinJSBridge.call('hideToolbar');
	});