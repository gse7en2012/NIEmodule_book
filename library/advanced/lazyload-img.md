# ͼƬ�ӳټ��� #
> �ο���ַ��http://wh.163.com/index.html  
 ������ο���nie.util.pageLoad  
 ҳ���е�img��ǩ�е�ͼƬ��ַ����д��data-src�����м���

----------
 ```javascript
         nie.util.pageLoad=nie.util.pageLoad||function(e){$(function(){var g=$(window),f={},h={},i=window.location.hash,j=function(){var c=g.scrollTop()-50,a=c+g.height()+50,d;for(d in f){var b=f[d],e=!1;if(b.b){if(b.y>=c&&b.y<=a||b.b>=c&&b.b<=a)e=!0}else b.y>=c&&b.y<=a&&(e=!0);e&&b.dom.attr("src",b.src)}for(d in h)b=h[d],(b.top>=c&&b.top<=a||b.bot>=c&&b.bot<=a)&&b.dom.attr("style","background-image:url("+b.src+")")};e.bgSelector&&$(e.bgSelector).each(function(c){var a=$(this),d=a.attr("data-bgUrl");if(d!=
                 ""){var b=a.offset().top+parseInt($.browser.msie?a.css("background-position-y"):a.css("background-position").split(" ")[1]);h[c]={dom:a,src:d,top:b,bot:b+a.height()}}});e.imgSelector&&$(e.imgSelector).each(function(c){var a=$(this),d=a.attr("data-src");if(d!="")if(f[c]={dom:a,src:d,y:a.offset().top},a.css("height"))f[c].b=f[c].y+parseInt(a.css("height"));else if(a.attr("height"))f[c].b=f[c].y+parseInt(a.attr("height"))});g.scroll(j).resize(j);(i==""||$("a#"+i+"[name="+i+"]").length==0)&&j()})};
         setTimeout(function(){
             //�Ż�����
             new nie.util.pageLoad({
                 imgSelector:"img"
             });
         },0);

 ```
 ע������ͼƬ�϶��ҽϳ���ҳ�棬�����ڹ�����