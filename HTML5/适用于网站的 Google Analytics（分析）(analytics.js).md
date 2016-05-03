适用于网站的 Google Analytics（分析）(analytics.js)

https://developers.google.com/analytics/devguides/collection/analyticsjs/#the_javascript_tracking_snippet

<!-- Google Analytics -->
<script>
(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
(i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
})(window,document,'script','//www.google-analytics.com/analytics.js','ga');

ga('create', 'UA-XXXXX-Y', 'auto');
ga('send', 'pageview');
</script>
<!-- End Google Analytics -->

以上代码进行了以下四项操作：

创建了一个 &lt;script&gt; 元素，并开始从 https://www.google-analytics.com/analytics.js 异步下载 analytics.js JavaScript 库。
初始化了一个全局函数 ga（也称为 ga() 命令队列），您可以通过该函数来安排要在 analytics.js 库加载完毕可供使用时执行的命令。
在 ga() 命令队列中添加一条命令，为通过 'UA-XXXXX-Y' 参数指定的媒体资源创建一个新的跟踪器对象。
在 ga() 命令队列中添加另一条命令，为当前页面向 Google Analytics（分析）发送网页浏览数据。
自定义实现时可能需要修改 JavaScript 跟踪代码段的最后两行（create 和 send 命令）或添加更多代码来跟踪更多互动。但不应该更改加载 analytics.js 库或初始化 ga() 命令队列函数的代码。




















