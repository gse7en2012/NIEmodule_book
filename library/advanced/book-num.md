# 动态输出分享信息 - by 范范 #
> 当分享内容需要用户自己来填写，并动态分享内容时的需求


----------
## 输出效果 ##

<iframe src="http://jsbin.com/toxoso/1/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>


## html ##

    <div class="wrap">
    <div class="g-clr">
        <p class="title">输入验证码：</p>
        <input type="text" id="token_value" class="token_value" />
        <img class="test token_img" id="token_img" onClick="get_token();" width="90" height="30" />
        <input type="button" id="getkey" class="getkey" value="" />
    </div>
    <div class="g-cr">
        <p class="title">序 列 号：</p>
        <input type="text" class="cdkey" id="cdkey" readonly value="直接输入验证码领取"/>
    </div>
	</div>

## css ##
    /*=reset Start*/
	body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,input,button,textarea,blockquote,th,td,p{margin:0;padding:0}
	input,button,select,textarea{outline:none}li{list-style:none}img{border:none}textarea{resize:none}
	body{color:#d00;word-break:break-all;word-wrap:break-word;line-height:18px;}
	body,input,textarea{font-size:14px;font-family:"宋体",Verdana,Arial;color: #f58750;}
	a{color:#d00;text-decoration:none;outline:none}
	a:hover{color:#f90}
	
	.g-clr{ zoom: 1; }
	.g-clr:after{ display: block; clear: both; height: 0; content: "\0020"; }
	.wrap{width: 350px;margin: 0 auto}
	input{border: 0}
	p{ height: auto; overflow: hidden; margin-bottom: 6px; }
	p img, p input{ display: inline; float: left; }
	.title{float: left;height: 30px;line-height: 30px;color: #5f0a03;font-size: 12px;margin-left: 8px;}
	.token_img{ margin:0 5px 0 0 ;}
	.token_value{ margin:0 10px 0 0; float:left;height: 30px;line-height: 30px; border:none; width: 119px; padding:0 5px; background: #5f0a03;color: #edd477 }
	.cdkey{  height: 30px;line-height: 30px; border:none; width: 159px; padding:0 5px; background: #5f0a03;color: #edd477;float: left;margin-left:12px;}
	.getkey{display: block;width: 170px;height: 46px;background: url(http://res.nie.netease.com/xy2/fab/13v3/images/btn.jpg) no-repeat;clear: left;margin: 10px 79px;cursor: pointer;}
	.getkey:hover{background: url(http://res.nie.netease.com/xy2/fab/13v3/images/btnhov.jpg)}

## Javascript ##
> 唯一要变的就是样式和product产品号，请让编辑和平台组**小坚**申请

	function giftByCtoken(args){
            var root='https://get-cdkey.webapp.163.com/',
                    product=args["product"],
                    tokenImg=args["tokenImg"],
                    tokenInput=args["tokenInput"],
                    getKeyBtn=args["getKeyBtn"],
                    successFunc=args["success"],
                    inputError=args["inputError"],
                    errorFunc=args["error"],
                    get_token=function(){
                        var imgsrc="http://get-cdkey.webapp.163.com/get_ctoken/?random="+Math.random();
                        $(tokenImg).attr("src",imgsrc);
                    }
            get_token();
            $(tokenImg).bind("click",get_token);
            $(getKeyBtn).bind("click",function(){
                var OK_STAT = 1;
                var INPUT_ERROR = 0;
                $.ajax({
                    "url": root+ "get_cdkey",
                    "dataType": "jsonp",
                    "data": {
                        "product": product,
                        "ctoken": $(tokenInput).val()
                    },
                    "success": function(data){
                        if(data.status === OK_STAT){
                            successFunc(data.cdkey);
                        }else if(data.status === INPUT_ERROR){
                            inputError(data.msg);
                        }else{
                            errorFunc(data.msg);
                        }
                    }
                });
            });
        }
        $(function(){
            giftByCtoken({
                product:292,//产品号
                tokenImg:"#token_img",//验证码图片id或者类名
                tokenInput:"#token_value",//填写验证码的容器的id或者类名
                getKeyBtn:"#getkey",//点击领取序列号的按钮的id或者类名
                success:function(key){//成功callback
                    $("#cdkey").val(key);
                },
                inputError:function(msg){//填写错误callback
                    alert(msg);
                },
                error:function(msg){//错误callback
                    alert(msg);
                }
            });

            nie.use(['util.clipBoard'], function(){
                $("#copykey").click(function(){
                    var cdkey = $.trim($('#cdkey').val());
                    if(cdkey != '上方输入框填写验证码，点击领取'){
                        $.clipBoard(cdkey,"复制成功！");
                    }else{
                        alert(cdkey);
                    }
                });
            });

            var loc = window.location.href
            if(loc.indexOf("fcreg") > -1){
                $("body").addClass("fcreg")
            }
        });

