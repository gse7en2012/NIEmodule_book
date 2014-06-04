# 图片列表 #
> 简单的图片列表模块，左右对齐


----------
## 输出效果 ##
> 给外层fpicList定一个基本宽度，和算margin-right的数值就可以左右对齐了，原理是使用了margin负值


<iframe src="http://jsbin.com/fekuw/1/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>


## html ##
    <section class="fpicList">
        <ul class="fpicListWrap g-clr">
            <li><a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/2/10/2014-02-10_417869.jpg" alt="哈哈哈哈啊"/><p>哈哈哈哈哈</p></a></li>
            <li><a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/2/10/2014-02-10_417869.jpg" alt="哈哈哈哈啊"/><p>哈哈哈哈哈</p></a></li>
            <li><a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/2/10/2014-02-10_417869.jpg" alt="哈哈哈哈啊"/><p>哈哈哈哈哈</p></a></li>
            <li><a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/2/10/2014-02-10_417869.jpg" alt="哈哈哈哈啊"/><p>哈哈哈哈哈</p></a></li>
        </ul>
    </section>

## css ##
    /*图片列表*/
    .fpicList{overflow: hidden;}
    .fpicListWrap{zoom: 1;margin-right: -100px;}
    .fpicListWrap li{float: left;margin-right: 34px;text-align: center}
    .fpicListWrap li p{font-size: 16px}

