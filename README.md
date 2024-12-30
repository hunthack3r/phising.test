
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>You've Been Hacked</title>
    <style>
        body {
            background-color: black;
            color: red;
            font-family: 'Courier New', Courier, monospace;
            overflow: hidden;
        }
        .hacked {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 3rem;
            text-align: center;
        }
        .skulls {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }
        .skull {
            position: absolute;
            font-size: 5rem;
            animation: float 5s infinite;
        }
        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); }
        }
        .hidden-link {
            position: absolute;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            color: black;
            font-size: 0.8rem;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="hacked">
        🚨 YOU HAVE BEEN HACKED BY DEDCROWD 🚨
    </div>
    <div class="skulls">
        <div class="skull" style="top: 10%; left: 20%;">💀</div>
        <div class="skull" style="top: 40%; left: 50%;">💀</div>
        <div class="skull" style="top: 70%; left: 80%;">💀</div>
    </div>
    <div class="hidden-link" onclick="showLog()">
        Company 2024
    </div>

    <script>
        function showLog() {
            window.location.href = '/log'; // Burada sunucuda log sayfasına yönlendirme yapılabilir.
        }
    </script>
</body>
</html>
