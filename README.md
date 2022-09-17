<!DOCTYPE HTML>
<html>
<head>
<meta charset="UTF-8">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=0">
<title>今天吃啥呀？www.dkewl.com</title>
<meta name="keywords" content="今天吃啥呀？" />
<meta name="description" content="【今天吃啥呀】随机推荐食品，再也不用为今天吃什么发愁了。" />
<link rel="Shortcut Icon" href="ic.ico" type="image/x-icon" />
<link rel="stylesheet" type="text/css" href="img/eat-min.css">
</head>
<body>
<div class="logo"><img src="img/logo.png" /></div>
<div id="wrapper">
  <h1 style="color:#FF9733" id="what"></h1>
  </h1>
  <input type="button" value="开始" id="start" />
</div>
<textarea rows="9" cols="53" id="list" style="display:none">馄饨 拉面 烩面 热干面 刀削面 油泼面 炸酱面 炒面 重庆小面 米线 酸辣粉 土豆粉 螺狮粉 凉皮儿 麻辣烫肉夹馍 羊肉汤 炒饭 盖浇饭 卤肉饭 烤肉饭 黄焖鸡米饭 驴肉火烧 川菜 麻辣香锅 火锅 酸菜鱼 烤串 披萨 烤鸭 汉堡 炸鸡 寿司 蟹黄包 粽子 煎饼果子 生煎 炒年糕 盖浇饭 砂锅 大排档 米线 满汉全席 西餐 麻辣烫 自助餐 炒面 快餐 水果 西北风 馄饨 火锅 烧烤 泡面 速冻水饺 日本料理 涮羊肉 味千拉面 肯德基 面包 扬州炒饭 自助餐 茶餐厅 海底捞 咖啡 比萨 麦当劳 兰州拉面 沙县小吃 烤鱼 海鲜 铁板烧 韩国料理 粥 快餐 东南亚菜 甜点 农家菜 川菜 粤菜 湘菜 本帮菜 竹笋烤肉</textarea>
<footer>
    <div class="copyright">
        <p>推荐：<a href="https://www.avager.club/" target="_blank">小张同学的个人博客</a><a href="https://www.avager.club" target="_blank"></a></p>
        <span class="cp">Copyright &copy; 2021-<script type="text/javascript">copyright=new Date();update=copyright.getFullYear();document.write(""+ update + "");</script> dkewl.com, All Rights Reserved.</span>
    </div>
</footer>
<script type='text/javascript' src='img/jquery-1.11.1.min.js'></script>
<script>
    $(function () {
    var run = 0,
        timer;

    $("#start").click(function () {
        var list = $("#list").val().replace(/ +/g, " ").replace(/^ | $/g, "").split(" ");
        if (!run) {
            $(this).val("停止");
            timer = setInterval(function () {
                var r = Math.ceil(Math.random() * list.length),
                    food = list[r - 1];
                $("#what").html(food);
                var rTop = Math.ceil(Math.random() * $(document).height()),
                    rLeft = Math.ceil(Math.random() * ($(document).width() - 50)),
                    rSize = Math.ceil(Math.random() * (37 - 14) + 14);
                $("<span class='temp'></span>").html(food).hide().css({
                    "top": rTop,
                    "left": rLeft,
                    "color": "rgba(0,0,0,." + Math.random() + ")",
                    "fontSize": rSize + "px"
                }).appendTo("body").fadeIn("slow", function () {
                    $(this).fadeOut("slow", function () {
                        $(this).remove();
                    });
                });
            }, 50);
            run = 1;
        } else {
            $(this).val("不行，换一个");
            clearInterval(timer);
            run = 0;
        };
    });

    document.onkeydown = function enter(e) {
        var e = e || event;
        if (e.keyCode == 13) $("#start").trigger("click");
    };
});
  
          $i = 0;
        $('#start').click(function(){
            $i++;
            if($i >=10 ){
                $('#start').hide();
        $('#what').html('这么挑？饿着吧！');
            }
        })
</script>

<script type="text/javascript">
  window.onload = function(){
    showTime();
  }
  function showTime(){
    var now=new Date(); 
    var year= now.getFullYear(); 
    document.getElementById("show").innerHTML=""+year;
    t=setTimeout('showTime()',1000)
  }
</script>
<!--pb-->
<script>
    document.oncontextmenu = function (event){
    if(window.event){
    event = window.event;
    }try{
    var the = event.srcElement;
    if (!((the.tagName == "INPUT" && the.type.toLowerCase() == "text") || the.tagName == "TEXTAREA")){
    return false;
    }
    return true;
    }catch (e){
    return false;
    }
    }
</script>
<script>
    document.onkeydown = function(){

    if(window.event && window.event.keyCode == 123) {
        alert("Hi");
        event.keyCode=0;
        event.returnValue=false;
    }
    if(window.event && window.event.keyCode == 13) {
        window.event.keyCode = 505;
    }
    if(window.event && window.event.keyCode == 8) {
        alert(str+"\n请使用Del键进行字符的删除操作！");
        window.event.returnValue=false;
    }
    }
</script>
<script type="text/javascript">
  	if (self == top) {
	    var theBody = document.getElementsByTagName('body')[0];
	    theBody.style.display = "block";
	} else {
	    top.location = self.location;
	}
</script>

</body>
</html>
