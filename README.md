
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
            animation: glitch 1s infinite;
        }
        .hacked {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 5rem;
            text-align: center;
            text-shadow: 0 0 20px red;
            animation: flicker 2s infinite;
        }
        .skulls {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }
        .skull {
            position: absolute;
            font-size: 8rem;
            color: red;
            animation: float 5s infinite, spin 3s linear infinite;
        }
        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-50px); }
            100% { transform: translateY(0); }
        }
        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        @keyframes glitch {
            0% { transform: skewX(0deg); }
            25% { transform: skewX(10deg); }
            50% { transform: skewX(0deg); }
            75% { transform: skewX(-10deg); }
            100% { transform: skewX(0deg); }
        }
        @keyframes flicker {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.3; }
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
        .btc-address {
            position: absolute;
            bottom: 50px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 1.5rem;
            color: lime;
            animation: flicker 1.5s infinite;
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
        <div class="skull" style="top: 30%; left: 70%;">💀</div>
    </div>
    <div class="hidden-link" onclick="showLog()">
        Company 2024
    </div>
    <div class="btc-address">
        Send BTC: 1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa
    </div>

    <script>
        alert('🚨 SYSTEM BREACH DETECTED 🚨');
        alert('💀 ALL YOUR DATA BELONG TO US 💀');
        alert('Send BTC to: 1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa');

        function showLog() {
            alert('Accessing log files...');
            window.location.href = '/log'; 
        }
    </script>
</body>
</html>
