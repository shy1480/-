<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>canvas</title>
    <style>
        canvas{
            border:2px solid darkcyan;
            margin:40px auto;
            display: block;
        }
    </style>
</head>
<body>
    <canvas id="mycanvas" class="canvas" name="canvas" width="800" height="400">
        浏览器不知道canvas 标签 
    </canvas>
    <script>
        var mycanvas = document.getElementById("mycanvas")
        var mycanvas1 = document.getElementsByClassName("canvas")[0]
        var mycanvas2 = document.getElementsByName("canvas")[0]
        var mycanvas3 = document.getElementsByTagName('canvas')[0]
        var mycanvas4 = document.querySelectorAll("#mycanvas")[0]
        var mycanvas5 = document.querySelector(".canvas")

        console.log(mycanvas)


        var c = mycanvas.getContext("2d");

        c.beginPath();
        c.moveTo(50,50);
        c.lineTo(200,200);
        c.lineTo(350,50);
        c.lineTo(50,50);
        c.strokeStyle= "red";
        c.lineWidth = 8;
        c.stroke();
        c.fillStyle = "yellow";
        // c.fill();
        c.closePath();


        c.beginPath();
        c.moveTo(125,125);
        c.lineTo(200,50);
        c.lineTo(275,125);
        c.lineTo(200,200);
        c.stroke();
        c.fill();
        c.closePath();

        // 绘制矩形
        c.beginPath();
        c.rect(400,100,200,100);
        c.strokeStyle = "blue"
        c.stroke();
        c.fill();
        c.closePath();
        
        // fillRect(x,y,w,h)

        c.beginPath();
        c.fillRect(100,300,200,100);
        c.fill();
        c.closePath();

        // arc(x,y,r,sa,ea,true/false)
        var P =   Math.PI;   // π = 3.14159262426243247
        c.beginPath();
        c.arc(300,300,80,-P/2,P/2,false);
        c.fillStyle = "purple"
        c.fill();
        c.closePath();


        c.beginPath();
        c.arc(600,200,150,0,P*2,false);
        c.strokeStyle= "green";
        c.lineWidth = 10;
        c.stroke();
        c.closePath();
    </script>
</body>
</html>
