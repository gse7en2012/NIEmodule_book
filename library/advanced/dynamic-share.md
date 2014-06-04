# 动态输出分享信息 - by 范范 #
> 当分享内容需要用户自己来填写，并动态分享内容时的需求


----------
## 输出效果 ##

<iframe src="http://jsbin.com/saloy/1/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>


## html ##

    <!--form 范范-->
    <div class="edit">
        <p>请输入您的宣言（限140字）</p>
        <textarea>请在此输入您的宣言</textarea>
        <p>或者选择宣言模板</p>
        <div class="demon">我是电竞玩家，我要为中国电竞正名！中国电竞需要你我正确对待，星星之火
            可以燎原，让我们一起为中国电竞加油！#中国电竞被世界认可，WHY NOT！#</div>
        <div class="bshare">
        </div>
    </div>

## css ##
    /*动态输出分享内容*/
    .epic{float:left; margin:65px 0 0 45px; _margin-left:20px; width:325px; height:485px; border:5px solid #0082b8;}
    .edit{color:#000; font:14px "Microsoft Yahei"; font-weight:bold;}
    textarea{margin:10px 0 10px 0;  +margin-left:-40px; padding:10px; _padding:10px 20px 10px 40px; width:415px; height:160px; background:#1c1e20; border:none; color:#3cc7f5; font:12px "宋体"; line-height:25px; overflow:hidden;}
    .demon{margin:10px 0 0 0; padding:10px; width:415px; height:35px; border:2px solid #0082b8; background:#cecece; color:#363e4a; font:12px "宋体"; line-height:20px; cursor:pointer;}
    .check{background:url(http://res.nie.netease.com/yxsg/qt/13/0904_whynot/images/bingo.jpg) 415px 40px no-repeat #cecece;}
    .bshare{margin:25px 0 0 0; color:#b1ced2; font:20px "Microsoft Yahei"; width:437px; height:74px; background:url(http://res.nie.netease.com/yxsg/qt/13/0904_whynot/images/share.jpg) no-repeat;}
    .bshare .NIE-share-txt {display: none;}
    .bshare .NIE-share{margin:18px 0 0 146px; float:left;}
    .bshare .NIE-share-iconBtn a{margin-right:33px!important;}
    .bshare .NIE-share-more{display:none!important;}
    .bshare .NIE-share2 .NIE-share-iconBtn a img,.bshare .NIE-share2 .NIE-share-more em{background:none!important;}

## Javascript ##

	nie.use([,"util.share"], function () {
        //        动态输出分享内容
        var share3=nie.util.share({
            fat:".bshare",
            type:2,
            title:"#中国原创电竞被世界认可，WHYNOT！#我是中国玩家，我要为中国原创电竞正名！中国原创竞技大作《英雄三国》，更公平，告别4V5，告别挂机坑货。中国原创需要你我正确对待，星星之火可以燎原，让我们一起为中国原创电竞加油！",
            content:"#中国原创电竞被世界认可，WHYNOT！#我是中国玩家，我要为中国原创电竞正名！中国原创竞技大作《英雄三国》，更公平，告别4V5，告别挂机坑货。中国原创需要你我正确对待，星星之火可以燎原，让我们一起为中国原创电竞加油！",
            defShow: [5, 2, 3, 1],
            img: ""
        });
        var content="#中国原创电竞被世界认可，WHYNOT！#我是中国玩家，我要为中国原创电竞正名！中国原创竞技大作《英雄三国》，更公平，告别4V5，告别挂机坑货。中国原创需要你我正确对待，星星之火可以燎原，让我们一起为中国原创电竞加油！",choice=false;
        $(".demon").click(function(){
            if(choice==false){
                $("textarea").val("#中国原创电竞被世界认可，WHYNOT！#我是中国玩家，我要为中国原创电竞正名！中国原创竞技大作《英雄三国》，更公平，告别4V5，告别挂机坑货。中国原创需要你我正确对待，星星之火可以燎原，让我们一起为中国原创电竞加油！");
                $(this).addClass("check");
                choice=true;
            }else{
                $(this).removeClass("check");
                choice=false;
            }
        })
        $("textarea").focus(function(){
            if($("textarea").val()=="请在此输入您的宣言") $("textarea").val("");
            choice=false;
        }).blur(function(){
                    if($(this).val()!=content && $(this).val()!=""){
                        share3.args.title="#中国原创电竞被世界认可，WHYNOT！#"+$(this).val();
                        share3.args.content="#中国原创电竞被世界认可，WHYNOT！#"+$(this).val();
                        $(".demon").removeClass("check");
                        choice=false;
                    }else{
                        $(".demon").addClass("check");
                        choice=true;
                    }
                });
    })

