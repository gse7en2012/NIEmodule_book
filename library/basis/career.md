# 职业模块 #
> 职业模块切换基本结构，万变不离其中,运用了tab插件


----------
## 输出效果 ##

<iframe src="http://jsbin.com/moyof/1/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>

## html ##

    <div class="fplayer">
	    <div class="pnav">
	        <ul>
	            <li class="pmenu"><a id="pmenu1" href="javascript:void(0)" class="current">鬼族 攻守兼备</a></li>
	            <li class="pmenu"><a id="pmenu2" href="javascript:void(0)">仙族 输出至上</a></li>
	            <li class="pmenu"><a id="pmenu3" href="javascript:void(0)">魔族 重在辅助</a></li>
	            <li class="pmenu"><a id="pmenu4" href="javascript:void(0)">人族 控制为王</a></li>
	        </ul>
	    </div>
	    <div class="ptabs">
	    <div class="ptab ptab_1 current">
	        <div class="gnav gnav1"><ul>
	            <li class="gmenu1"><a id="gmenu1" href="javascript:void(0)" class="current">夜灵溪</a></li>
	            <li class="gmenu2"><a id="gmenu2" href="javascript:void(0)">幽梦影</a></li>
	            <li class="gmenu3"><a id="gmenu3" href="javascript:void(0)">祭剑魂</a></li>
	            <li class="gmenu4"><a id="gmenu4" href="javascript:void(0)">猎魂引</a></li>
	            <li class="gmenu5"><a id="gmenu5" href="javascript:void(0)">墨衣行</a></li>
	            <li class="gmenu6"><a id="gmenu6" href="javascript:void(0)">无涯子</a></li>
	        </ul>
	        </div>
	        <div class="gtabs gtabs1">
	            <div class="gtab gtab_1 current">
	                <div class="goods">
	                    <h4>夜灵溪</h4>
	                    <p>擅 长：辅助</p>
	                    <p>法术特点：群体回复5个单位（男鬼）<br>
	                        群体加防或群体控制7-8个单位（女鬼）</p>
	                </div>
	                <img class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role1/g1.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg" alt=""/>
	            </div>
	            <div class="gtab gtab_2">
	                <div class="goods">
	                    <h4>幽梦影</h4>
	                    <p>擅 长：辅助</p>
	                    <p>法术特点：群体回复5个单位（男鬼）<br>
	                        群体加防或群体控制7-8个单位（女鬼）</p>
	                </div>
	                <img class="gifs"  data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role1/g2.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_3">
	                <div class="goods">
	                    <h4>祭剑魂</h4>
	                    <p>擅 长：辅助</p>
	                    <p>法术特点：群体回复5个单位（男鬼）<br>
	                        群体加防或群体控制7-8个单位（女鬼）</p>
	                </div>
	                <img class="gifs"  data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role1/g3.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_4">
	                <div class="goods">
	                    <h4>猎魂引</h4>
	                    <p>擅 长：辅助</p>
	                    <p>法术特点：群体回复5个单位（男鬼）<br>
	                        群体加防或群体控制7-8个单位（女鬼）</p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role1/g4.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_5">
	                <div class="goods">
	                    <h4>墨衣行</h4>
	                    <p>擅 长：辅助</p>
	                    <p>法术特点：群体回复5个单位（男鬼）<br>
	                        群体加防或群体控制7-8个单位（女鬼）</p>
	                </div>
	                <img class="gifs"  data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role1/g5.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_6">
	                <div class="goods">
	                    <h4>无涯子</h4>
	                    <p>擅 长：辅助</p>
	                    <p>法术特点：群体回复5个单位（男鬼）<br>
	                        群体加防或群体控制7-8个单位（女鬼）</p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role1/g6.gif"  src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg" alt=""/>
	            </div>
	        </div>
	    </div>
	
	    <div class="ptab ptab_2">
	        <div class="gnav gnav2">
	            <ul>
	                <li class="gmenu21"><a id="gmenu21" href="javascript:void(0)" class="current">神天兵</a></li>
	                <li class="gmenu22"><a id="gmenu22" href="javascript:void(0)">舞天姬</a></li>
	                <li class="gmenu23"><a id="gmenu23" href="javascript:void(0)">智圣仙</a></li>
	                <li class="gmenu24"><a id="gmenu24" href="javascript:void(0)">精灵仙</a></li>
	                <li class="gmenu25"><a id="gmenu25" href="javascript:void(0)">龙战将</a></li>
	                <li class="gmenu26"><a id="gmenu26" href="javascript:void(0)">玄剑娥</a></li>
	            </ul>
	        </div>
	        <div class="gtabs gtabs2">
	            <div class="gtab gtab_21 current">
	                <div class="goods">
	                    <h4>神天兵</h4>
	                    <p>擅 长：法术输出</p> <p>法术特点：群体法术伤害可同时伤害5-6<br>个单位</p>
	                </div>
	                <img class="gifs"  data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role4/x1.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_22">
	                <div class="goods">
	                    <h4>舞天姬</h4>
	                    <p>擅 长：法术输出</p> <p>法术特点：群体法术伤害可同时伤害5-6<br>个单位</p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role4/x2.gif"  src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg" alt=""/>
	            </div>
	            <div class="gtab gtab_23">
	                <div class="goods">  <h4>智圣仙</h4>
	                    <p>擅 长：法术输出</p> <p>法术特点：群体法术伤害可同时伤害5-6<br>个单位</p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role4/x3.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_24">
	                <div class="goods">
	                    <h4>精灵仙</h4>
	                    <p>擅 长：法术输出</p> <p>法术特点：群体法术伤害可同时伤害5-6<br>个单位</p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role4/x4.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_25">
	                <div class="goods">
	                    <h4>龙战将</h4>
	                    <p>擅 长：法术输出</p> <p>法术特点：群体法术伤害可同时伤害5-6<br>个单位</p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role4/x5.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_26">
	                <div class="goods">
	                    <h4>玄剑娥</h4>
	                    <p>擅 长：法术输出</p> <p>法术特点：群体法术伤害可同时伤害5-6<br>个单位</p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role4/x6.gif"  src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg" alt=""/>
	            </div>
	        </div>
	    </div>
	
	    <div class="ptab ptab_3">
	        <div class="gnav gnav3">
	            <ul>
	                <li class="gmenu31"><a id="gmenu31" href="javascript:void(0)" class="current">夺命妖</a></li>
	                <li class="gmenu32"><a id="gmenu32" href="javascript:void(0)">狐美人</a></li>
	                <li class="gmenu33"><a id="gmenu33" href="javascript:void(0)">虎头怪</a></li>
	                <li class="gmenu34"><a id="gmenu34" href="javascript:void(0)">骨精灵</a></li>
	                <li class="gmenu35"><a id="gmenu35" href="javascript:void(0)">巨魔王</a></li>
	                <li class="gmenu36"><a id="gmenu36" href="javascript:void(0)">小蛮妖</a></li>
	            </ul>
	        </div>
	        <div class="gtabs gtabs3">
	            <div class="gtab gtab_31 current">
	                <div class="goods"> <h4>夺命妖</h4>
	                    <p>擅 长：物理攻击+辅助</p>
	                    <p>法术特点：可对7-8个单位造成50%左右的伤害</p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role3/m1.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_32">
	                <div class="goods">
	                    <h4>狐美人</h4>
	                    <p>擅 长：物理攻击+辅助</p>
	                    <p>法术特点：可对7-8个单位造成50%左右的伤害</p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role3/m2.gif"  src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg" alt=""/>
	            </div>
	            <div class="gtab gtab_33">
	                <div class="goods">
	                    <h4>虎头怪</h4>
	                    <p>擅 长：物理攻击+辅助</p>
	                    <p>法术特点：可对7-8个单位造成50%左右的伤害</p>
	                </div>
	                <img class="gifs"  data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role3/m3.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_34">
	                <div class="goods">
	                    <h4>骨精灵</h4>
	                    <p>擅 长：物理攻击+辅助</p>
	                    <p>法术特点：可对7-8个单位造成50%左右的伤害</p>
	                </div>
	                <img class="gifs"  data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role3/m4.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_35">
	                <div class="goods">
	                    <h4>巨魔王</h4>
	                    <p>擅 长：物理攻击+辅助</p>
	                    <p>法术特点：可对7-8个单位造成50%左右的伤害</p>
	                </div>
	                <img class="gifs"  data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role3/m5.gif"  src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg" alt=""/>
	            </div>
	            <div class="gtab gtab_36">
	                <div class="goods">
	                    <h4>小蛮妖</h4>
	                    <p>擅 长：物理攻击+辅助</p>
	                    <p>法术特点：可对7-8个单位造成50%左右的伤害</p>
	                </div>
	                <img class="gifs"  data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role3/m6.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg" alt=""/>
	            </div>
	        </div>
	    </div>
	
	    <div class="ptab ptab_4">
	        <div class="gnav gnav4">
	            <ul>
	                <li class="gmenu41"><a id="gmenu41" href="javascript:void(0)" class="current">飞燕女</a></li>
	                <li class="gmenu42"><a id="gmenu42" href="javascript:void(0)">逍遥生</a></li>
	                <li class="gmenu43"><a id="gmenu43" href="javascript:void(0)">英女侠</a></li>
	                <li class="gmenu44"><a id="gmenu44" href="javascript:void(0)">剑侠客</a></li>
	                <li class="gmenu45"><a id="gmenu45" href="javascript:void(0)">猛壮士</a></li>
	                <li class="gmenu46"><a id="gmenu46" href="javascript:void(0)">俏千金</a></li>
	            </ul>
	        </div>
	        <div class="gtabs gtabs4">
	            <div class="gtab gtab_41 current">
	                <div class="goods">
	                    <h4>飞燕女</h4>
	                    <p>擅 长：控制系法术</p>
	                    <p>法术特点：群体控制，可同时控制7-8个单位
	                    </p>
	                </div>
	                <img class="gifs"  data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role2/r1.gif"  src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg" alt=""/>
	            </div>
	            <div class="gtab gtab_42">
	                <div class="goods">
	                    <h4>逍遥生</h4>
	                    <p>擅 长：控制系法术</p>
	                    <p>法术特点：群体控制，可同时控制7-8个单位
	                    </p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role2/r2.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_43">
	                <div class="goods">
	                    <h4>英女侠</h4>
	                    <p>擅 长：控制系法术</p>
	                    <p>法术特点：群体控制，可同时控制7-8个单位
	                    </p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role2/r3.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_44">
	                <div class="goods">
	                    <h4>剑侠客</h4>
	                    <p>擅 长：控制系法术</p>
	                    <p>法术特点：群体控制，可同时控制7-8个单位
	                    </p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role2/r4.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_45">
	                <div class="goods">
	                    <h4>猛壮士</h4>
	                    <p>擅 长：控制系法术</p>
	                    <p>法术特点：群体控制，可同时控制7-8个单位
	                    </p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role2/r5.gif" src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg"  alt=""/>
	            </div>
	            <div class="gtab gtab_46">
	                <div class="goods">
	                    <h4>俏千金</h4>
	                    <p>擅 长：控制系法术</p>
	                    <p>法术特点：群体控制，可同时控制7-8个单位
	                    </p>
	                </div>
	                <img  class="gifs" data-src="http://res.nie.netease.com/xy2/fab/13v3/images/role2/r6.gif"  src="http://res.nie.netease.com/xy2/fab/13v3/images/gifshow.jpg" alt=""/>
	            </div>
	        </div>
	    </div>
	    </div>
	    </div>


## css ##
	/*职业切换*/
        .ftab,.ptab,.gtab{display:none;}
        .fplayer .current{display:block;}
        .fplayer{ width: 632px; height: 479px;}
        .fplayer h4{ display: none}
        .pnav,.pnav ul{ width: 632px; height: 59px; }
        .pnav li,.pnav a{float:left; display:block; width:158px;height:59px; background:url(http://res.nie.netease.com/xy2/fab/13v3/images/tabshow.png) 0 -247px; text-indent:-9999px; cursor:default;}
        #pmenu2{ background-position:-158px -247px;}
        #pmenu3{background-position:-316px -247px;}
        #pmenu4{background-position:-474px -247px;}
        .current #pmenu1{background-position:0 -306px;}
        .current #pmenu2{background-position:-158px  -307px;}
        .current #pmenu3{background-position:-316px -307px;}
        .current #pmenu4{background-position:-474px -307px;}
        .ptab{ position: relative; width:632px; height: 391px; }
        .gtabs{position: relative;*zoom:1;z-index: 8}
        .gtab{ width:632px; height: 391px;}
        .goods{ width: 252px; font-size:14px; z-index: 6;color: #68eaff;position: absolute;right: -8px; top:69px;}
        .goods p{ height: 20px; line-height: 20px; color: #9c321d}
        .gifs{ position: absolute; width: 247px; height: 226px; cursor: pointer;right: 0;bottom: 20px;}
        .gifs img{display: block;width: 247px;height: 226px;}

        .gnav{ width: 60px; position: absolute; top: 12px; left: 15px; z-index: 99}
        .gnav li,.gnav a{display:block; height:53px; width:60px; background:url(http://res.nie.netease.com/xy2/fab/13v3/images/role.png) 0 0; text-indent:-9999px; cursor:default;}
        .gnav li{ padding-bottom:10px; background:none;}
        .gmenu1,#gmenu1{background-position:0 -312px;}
        .gmenu2,#gmenu2{background-position:0 -363px;}
        .gmenu3,#gmenu3{background-position:0 -415px;}
        .gmenu4,#gmenu4{background-position:0 -467px;}
        .gmenu5,#gmenu5{background-position:0 -519px;}
        .gmenu6,#gmenu6{background-position:0 -572px;}
        #gmenu1.current{background-position:0 0;}
        #gmenu2.current{background-position:0 -52px;}
        #gmenu3.current{background-position:0 -104px;}
        #gmenu4.current{background-position:0 -156px;}
        #gmenu5.current{background-position:0 -208px;}
        #gmenu6.current{background-position:0 -260px;}
        .gtab_1{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_1.jpg) no-repeat bottom right;}
        .gtab_2{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_2.jpg) no-repeat bottom right;}
        .gtab_3{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_3.jpg) no-repeat bottom right;}
        .gtab_4{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_4.jpg) no-repeat bottom right;}
        .gtab_5{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_5.jpg) no-repeat bottom right;}
        .gtab_6{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_6.jpg) no-repeat bottom right;}

        .gmenu21,#gmenu21{background-position:-180px -312px;}
        .gmenu22,#gmenu22{background-position:-180px -363px;}
        .gmenu23,#gmenu23{background-position:-180px -415px;}
        .gmenu24,#gmenu24{background-position:-180px -467px;}
        .gmenu25,#gmenu25{background-position:-180px -519px;}
        .gmenu26,#gmenu26{background-position:-180px -572px;}
        #gmenu21.current{background-position:-180px 0;}
        #gmenu22.current{background-position:-180px -52px;}
        #gmenu23.current{background-position:-180px -104px;}
        #gmenu24.current{background-position:-180px -156px;}
        #gmenu25.current{background-position:-180px -208px;}
        #gmenu26.current{background-position:-180px -260px;}
        .gtab_21{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_x1.jpg) no-repeat bottom right;}
        .gtab_22{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_x2.jpg) no-repeat bottom right;}
        .gtab_23{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_x3.jpg) no-repeat bottom right;}
        .gtab_24{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_x4.jpg) no-repeat bottom right;}
        .gtab_25{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_x5.jpg) no-repeat bottom right;}
        .gtab_26{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_x6.jpg) no-repeat bottom right;}

        .gmenu31,#gmenu31{background-position:-120px -312px;}
        .gmenu32,#gmenu32{background-position:-120px -363px;}
        .gmenu33,#gmenu33{background-position:-120px -415px;}
        .gmenu34,#gmenu34{background-position:-120px -467px;}
        .gmenu35,#gmenu35{background-position:-120px -519px;}
        .gmenu36,#gmenu36{background-position:-120px -572px;}
        #gmenu31.current{background-position:-120px 0;}
        #gmenu32.current{background-position:-120px -52px;}
        #gmenu33.current{background-position:-120px -104px;}
        #gmenu34.current{background-position:-120px -156px;}
        #gmenu35.current{background-position:-120px -208px;}
        #gmenu36.current{background-position:-120px -260px;}
        .gtab_31{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_m1.jpg) no-repeat bottom right;}
        .gtab_32{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_m2.jpg) no-repeat bottom right;}
        .gtab_33{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_m3.jpg) no-repeat bottom right;}
        .gtab_34{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_m4.jpg) no-repeat bottom right;}
        .gtab_35{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_m5.jpg) no-repeat bottom right;}
        .gtab_36{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_m6.jpg) no-repeat bottom right;}


        .gmenu41,#gmenu41{background-position:-60px -312px;}
        .gmenu44,#gmenu42{background-position:-60px -363px;}
        .gmenu43,#gmenu43{background-position:-60px -415px;}
        .gmenu44,#gmenu44{background-position:-60px -467px;}
        .gmenu45,#gmenu45{background-position:-60px -519px;}
        .gmenu46,#gmenu46{background-position:-60px -572px;}
        #gmenu41.current{background-position:-60px 0;}
        #gmenu42.current{background-position:-60px -52px;}
        #gmenu43.current{background-position:-60px -104px;}
        #gmenu44.current{background-position:-60px -156px;}
        #gmenu45.current{background-position:-60px -208px;}
        #gmenu46.current{background-position:-60px -260px;}
        .gtab_41{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_r1.jpg) no-repeat bottom right;}
        .gtab_42{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_r2.jpg) no-repeat bottom right;}
        .gtab_43{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_r3.jpg) no-repeat bottom right;}
        .gtab_44{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_r4.jpg) no-repeat bottom right;}
        .gtab_45{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_r5.jpg) no-repeat bottom right;}
        .gtab_46{ background:url(http://res.nie.netease.com/xy2/fab/13v3/images/gtab_r6.jpg) no-repeat bottom right;}

## Javascript ##
	nie.use(["ui.tab"], function () {
	//职业切换
        $.tab(".pnav li",".ptabs > div");
        $.tab(".gnav1 a",".gtabs1 > div");
        $.tab(".gnav2 a",".gtabs2 > div");
        $.tab(".gnav3 a",".gtabs3 > div");
        $.tab(".gnav4 a",".gtabs4 > div");
        $('.gifs').click(function(){
            var imgurl = $(this).attr('data-src');
            $(this).attr('src',imgurl);
        })
    })

