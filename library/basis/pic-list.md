# ͼƬ�б� #
> �򵥵�ͼƬ�б�ģ�飬���Ҷ���


----------
## ���Ч�� ##
> �����fpicList��һ��������ȣ�����margin-right����ֵ�Ϳ������Ҷ����ˣ�ԭ����ʹ����margin��ֵ


<iframe src="http://jsbin.com/fekuw/1/embed?output" class=" foo" id="" style="border: 1px solid rgb(170, 170, 170); width: 100%; min-height: 200px; height: 537px;"></iframe>


## html ##
    <section class="fpicList">
        <ul class="fpicListWrap g-clr">
            <li><a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/2/10/2014-02-10_417869.jpg" alt="����������"/><p>����������</p></a></li>
            <li><a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/2/10/2014-02-10_417869.jpg" alt="����������"/><p>����������</p></a></li>
            <li><a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/2/10/2014-02-10_417869.jpg" alt="����������"/><p>����������</p></a></li>
            <li><a href="#" target="_blank"><img src="http://img.nie.163.com/images/2014/2/10/2014-02-10_417869.jpg" alt="����������"/><p>����������</p></a></li>
        </ul>
    </section>

## css ##
    /*ͼƬ�б�*/
    .fpicList{overflow: hidden;}
    .fpicListWrap{zoom: 1;margin-right: -100px;}
    .fpicListWrap li{float: left;margin-right: 34px;text-align: center}
    .fpicListWrap li p{font-size: 16px}

