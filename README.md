jetpl.js
=======
# 快速上手

* [查看模板详细API](http://www.jayui.com/jetpl/)  

**编写模板**

使用一个``type="text/html"``的``script``标签存放模板：

    <script id="test" type="text/html">
    {% if (title){ %}
        {% for (var i=0;i<list.length;i++) { %}
            <div>{%= i %}. {%= list[i].user %}</div>
        {%}%>
        {%= name||"name is not found !" %}
    {% } %}
    </script>


**渲染模板**

      var data = {
          title: '标签',
          list: ['文艺', '博客', '摄影', '电影', '民谣', '旅行', '吉他']
      };
      var gethtml = document.getElementById('test').innerHTML
      
      jetpl(gethtml).render(data, function(html){
          document.getElementById('testid').innerHTML = html
      });
============
**查看演示**

* [查看模板演示](http://singod.github.io/jetpl/)   

**下载**

* [jetpl.js](https://github.com/singod/jetpl/blob/gh-pages/js/jetpl.js) *(原生语法, 2.7kb)*


============


