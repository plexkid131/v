<!DOCTYPE html>
<html>
<head>
    <title>Simple Block Game</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: #d0e7f9;
        }
        #game {
            width: 600px;
            height: 400px;
            position: relative;
            border: 2px solid #333;
            background: #87ceeb;
        }
        .block {
            width: 40px;
            height: 40px;
            background: #8b4513;
            position: absolute;
        }
    </style>
</head>
<body>
    <div id="game"></div>
    <script>
        document.getElementById('game').addEventListener('click', function(event) {
            let block = document.createElement('div');
            block.classList.add('block');
            block.style.left = event.clientX - (event.clientX % 40) + 'px';
            block.style.top = event.clientY - (event.clientY % 40) + 'px';
            document.getElementById('game').appendChild(block);
        });
    </script>
</body>
</html>
