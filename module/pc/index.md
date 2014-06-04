# PC端页面相关规范 #

----------

## 注意事项 ##

1. 尽可能用语义化的html5标签
2. 原则上需要兼容IE6+，但是我们衷心地希望以后可以兼容IE8+
3. 网站组服务器为**gb2312**，只能有这个编码，其他编码会出现乱码问题，这个问题无解，请大家制作时注意
3. html框架和css reset都是写好的了，大家可以复用，后期希望可以用grunt输出模块，less/sass组织css
4. 对于第一次接触网站组页面的人来说，有几点是需要注意的
	- 所有网站组的游戏都在[http://nie.163.com/](http://nie.163.com/)，你可以先去了解一下产品
	- 所有网站的白色顶部条和底部版权信息是自动读取的，在html中插入结构即可，具体可以看看模板，顶部是**NIE-topBar**，底部是**NIE-copyRight**
	- 网站组的基本组件库是jquery的，所以你可以用jquery的一切语法，但是为了自我提高，请尽量学习原生js，不要过多地依赖组件库
5. 笔者在写这个文档的时候，网站组前端依然没有一个高效可行的规范，css、js等等，希望在日后通过大家的努力，可以构建相关的组内规范



----------

## 相关规范与结构 ##
> index.html  
> -img  
> -css  
> --page.css  
> -js  
> --page.js

### index.html ###
> wrap1\wrap2\...的作用是在大背景的时候，可以切成几块，控制background-posisiton

		<!DOCTYPE html>
		<html>
		<head>
		<title>新大话2新年惊喜季</title>
		<meta name="keywords" content="" />
		<meta name="description" content="" />
		<meta charset="gb2312">
		<!--项目meta信息，请编辑提供 start-->
		<meta name="author" content="网易，NetEase Inc." />
		<meta name="copyright" content="网易，NetEase Inc." />
		<meta name="pmid" content="274800" />
		<meta name="editor" content="Leon" />
		<meta name="designer" content="doudou,QQ,CP-D" />
		<meta name="front-end technicist" content="MrF" />
		<!--项目meta信息，请编辑提供 end-->
		<meta name="renderer" content="webkit">
		<link rel="dns-prefetch" href="http://res.nie.netease.com">
		<!-- jquery mix NIE (最新版本）-->
		<script charset="gb2312" src="http://res.nie.netease.com/comm/js/jquery(mixNIE).last.js"></script>
		<!--[if lt IE 9]>
		<script src="http://res.nie.netease.com/comm/html5/html5shiv.js"></script>
		<![endif]-->
		<link rel="stylesheet" href="css/page.css"/>
		<!--底部版权颜色变灰，如果正常，则去掉以下-->
		<script>nie.config.copyRight.setGray();</script>
		</head>
		<body>
		<!--SEO start-->
		<h1 class="hide">新大话2新年惊喜季</h1>
		<!--SEO start-->
		<!--Share text start-->
		<div class="sharetxt hide"></div>
		<div class="shareimg hide"></div>
		<!--Share text end-->
		<div id="NIE-topBar"></div>
		
		<div id="wrap">
		<div id="wrap1">
		    <div id="wrap2">
			    <div id="wrap3">
		        <!--尾部-->
		        <footer>
		            <div id="NIE-copyRight"></div>
		        </footer>
				</div>
			</div>
		</div>
		</div>
		
		<div id="NIE-overlayer"></div>
		<script type="text/javascript" src="js/page.js"></script>
		<!--[if IE 6]>
		<script type="text/javascript" src="http://res.nie.netease.com/comm/html5/fixPNG.js"></script>
		<script type="text/javascript">
		$(function(){
		    $.fixPNG.fix('.png64');
		})
		
		</script>
		<![endif]-->
		</body>
		</html>
### css ###
- page.css
<pre>
@charset "gb2312";
/* =s Reset (by YUI 3) */
html{color:#000;}
body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,input,textarea,p,blockquote,th,td{margin:0;padding:0;}
article,aside,audio,bdi,canvas,command,datalist,details,figcaption,figure,footer,header,hgroup,keygen,mark,meter,nav,output,progress,rp,rt,ruby,section,source,summary,time,track,video,title {display:block}
table{border-collapse:collapse;border-spacing:0;}
fieldset,img{border:0;}
address,caption,cite,code,dfn,em,strong,th,var{font-style:normal;font-weight:normal;}
li{list-style:none;}
caption,th{text-align:left;}
h1,h2,h3,h4,h5,h6{font-size:100%;font-weight:normal;}
q:before,q:after{content:'';}
abbr,acronym{border:0;font-variant:normal;}
sup{vertical-align:text-top;}
sub{vertical-align:text-bottom;}
input,textarea,select{font-family:inherit;font-size:inherit;font-weight:inherit;}
input,textarea,select{*font-size:100%;}
legend{color:#000;}
article a{transition:all .5s ease-in-out;-webkit-transition:all .5s ease-in-out;-moz-transition:all .5s ease-in-out;-o-transition:all .5s ease-in-out;-ms-transition:all .5s ease-in-out;}
/* =e Reset */
/* =s base */
html,body{height:100%;background-color: #07192b;margin: 0;padding: 0}
body{font-family:"Microsoft YaHei",simSun,"Lucida Grande","Lucida Sans Unicode",Arial;line-height:170%;font-size:12px;color:#000;}
i{font-style:normal;}
a{color:#000;text-decoration: none}
a:hover{text-decoration: underline}
a.under:link,a.under:active,a.under:visited,a.under:hover{text-decoration:underline;}
/* float*/
.fltL{float:left;}
.fltR{float:right;}
.fixR{position: absolute;top: 0px; right: 0px;}
.setCenter{margin:0 auto;}

/* clear */
.clrB{clear:both;}
.clrL{clear:left;}
.clrR{clear:right;}
.clrN{clear:none;}
.g-clr { zoom: 1; }
.g-clr:after { display: block; clear: both; height: 0; content: "\0020"; }
/* =e base */

/* =s Font */
/* font-weight [first-letter]*/
.b{font-weight:bold;}
.n{font-weight:normal;}
/* font-position [txt-P] */
.txtC{text-align:center;}
.g-thide { text-indent: -9999px; }
.tRed{color: #d50000}
.hide{display:none!important;}
/* wrap */
#wrap{position: relative;width: 100%;max-width:1920px;min-width:1000px;margin:0 auto;_width:expression((document.documentElement.clientWidth>1680||document.body.clientWidth>1680)?"1920px":"100%");height: auto;overflow: hidden;margin: 0 auto;}
/* wrapbackground*/
#wrap1,#wrap2{width: 100%}
#wrap1{background: url(../img/bg1.jpg) no-repeat  center 0;}
#wrap2{background: url(../img/bg2.jpg) no-repeat center 579px;}

#main{width: 1000px;margin: 0 auto;position: relative;zoom: 1}

/*弹层蒙版*/
#NIE-overlayer{display:none;position:absolute;width:100%;height:100%;background:#000;filter:alpha(opacity=80);opacity:.8;top:0;left:0;z-index:99}
footer{text-align:center;clear:both;height:66px;line-height:60px;position: relative;margin:0 auto;background: #070e1c;padding:10px 0}
footer{color: #ecbf71}
footer a{color:#ecbf71;text-decoration:none;}
footer a:hover{text-decoration:underline;}
#NIE-copyRight{z-index:99999}
</pre>