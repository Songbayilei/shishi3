# shishi3
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
    
    <style type="text/css">
        .newStyle1 {
            font-family: Algerian;
        }
        .auto-style1 {
            font-family: "Bell MT";
            font-weight: bold;
            font-size: large;
        }
        </style>

</head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    <title>倒计时</title>
    <link rel="stylesheet" href="style.css" />

<body>
    <form id="form2" runat="server">
        <div>
            <asp:Label ID="Label1" runat="server" Text="Label"></asp:Label>
        </div>
    </form>
    <div class="time">We have been together for <span id="LeftTime"></span></div>
    <script>
    function FreshTime() {
        var endtime = new Date("2019/6/1"); //结束时间
        var nowtime = new Date(); //当前时间
        var lefttime = parseInt((nowtime.getTime() - endtime.getTime()) / 1000);
        d = parseInt(lefttime / 3600 / 24);
        h = parseInt((lefttime / 3600) % 24);
        m = parseInt((lefttime / 60) % 60);
        s = parseInt(lefttime % 60);
        document.getElementById("LeftTime").innerHTML = d + " days!";
    }
    FreshTime()
    var sh;
    sh = setInterval(FreshTime, 1000);
    </script>
</body>
</html>
