<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>聚光灯效果</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }

        body {
            background-color: #222;
            /* 弹性布局  水平居中 垂直居中 */
            display: flex;
            justify-content: center;
            align-items: center;
            /* 100%窗口高度 */
            height: 100vh;
        }

        h1 {
            color: #333;
            /* 转换为大写 */
            text-transform: uppercase;
            font-size: 112px;
            /* 相对定位 */
            position: relative;
        }

        h1::after {
            content: 'hello world';
            /* 颜色更改为透明 */
            color: transparent;
            position: absolute;
            top: 0;
            left: 0;
            background: linear-gradient(to right, #ff59b3, #fe0000, #ffff01, #40e1d2, #6435f8);
            background-clip: text;
            -webkit-background-clip: text;
            clip-path: circle(100px at 0% 50%);
            animation: light 5s infinite;
        }
        
        @keyframes light {
            0% {
                clip-path: circle(100px at 0% 50%);
            }
            50% {
                clip-path: circle(100px at 100% 50%);
            }
            100% {
                clip-path: circle(100px at 0% 50%);
            }
        }
    </style>
</head>

<body>
    <h1>hello world</h1>
</body>

</html>
