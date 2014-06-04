# 搜索模块 #
> 简单的搜索模块，要用js是因为要转码，你懂的


----------
## 输出效果 ##

<iframe src="http://jsbin.com/vetun/1/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>


## html ##

    <div class="fSearch" id="search0">
	    <form id="search">
	        <input type="text" onblur="if(this.value==''){this.value='官网搜索全面升级  欢迎使用';this.style.color='#676767'};" onfocus="this.value=this.value=='官网搜索全面升级  欢迎使用'?'':this.value;this.style.color='#676767';" value="官网搜索全面升级  欢迎使用" class="inpTxt" name="qs" id="searchKeyWords1" style="color: rgb(103, 103, 103);">
	        <input type="submit" class="inpBut" value="搜索">
	    </form>
	</div>

## css ##
	/*搜索版块*/
	.fSearch {width: 392px;height: 31px;padding: 14px; margin: 0 auto;background: url(http://res.nie.netease.com/xy2/gw/13v2/images/schbg.jpg) no-repeat;}
	.fSearch .inpTxt {width: 301px;height: 29px;background: #f3eee5;font-size: 12px;line-height: 29px;color: #b2866b;padding-left: 10px;}
	.fSearch .inpBut {float: right;width: 68px;height: 30px;overflow: hidden;border: 0;text-indent: -9999px;cursor: pointer;background: none}

## Javascript ##
	//    搜索版块
    $('.fSearch').find('.inpBut').click(function(){
        var val = $("#searchKeyWords1").val();
        window.open(encodeURI("http://so.xy2.163.com/search?qs="+val));
    })

