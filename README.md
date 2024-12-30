<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>You've Been Hacked</title>
    <style>
        body {
            margin: 0;
            padding: 5vh 5vw;
            background: black;
            overflow:hidden;
            color: red;
            font-family: 'Courier New', Courier, monospace;
            animation: glitch 1s infinite;
        }
        * {
            box-sizing: border-box;
        }
        p {
            font-family: monospace;
            font-weight: bold;
            font-size: 4.1vh;
            margin: 0;
            padding: 0;
            line-height: 1;
            color: limegreen;
            text-shadow: 0px 0px 10px limegreen;
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
        .msg {
            font-family: monospace;
            font-weight: bold;
            text-transform: uppercase;
            font-size: 5vh;
            padding-top: 5vh;
            background: red;
            box-shadow: 0 0 30px red;
            text-shadow: 0 0 20px white;
            color: white;
            width: 20vw;
            height: 15vh;
            position: absolute;
            left: 50%;
            margin-left: -10vw;
            top: 50%;
            margin-top: -5vh;
            text-align: center;
            min-width: 200px;
            animation-name: blink;
            animation-duration: 0.6s;
            animation-iteration-count: infinite;
            animation-direction: alternate;
            animation-timing-function: linear;
        }
        @keyframes blink {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
        #console {
            margin-top: 10vh;
        }
    </style>
</head>
<body>
    <div class="hacked">
        🚨 YOU HAVE BEEN HACKED BY DEDCROWD 🚨
    </div>
    <div class="msg">Scanning</div>
    <div id="console"></div>

    <script>
        alert('🚨 SYSTEM BREACH DETECTED 🚨');
        alert('💀 ALL YOUR DATA BELONG TO US 💀');
        alert('Send BTC to: 1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa');

        var intervalID = window.setInterval(updateScreen, 200);
        var c = document.getElementById("console");

        var txt = [
          "FORCE: XX0022. ENCYPT://000.222.2345",
          "TRYPASS: ********* AUTH CODE: ALPHA GAMMA: 1___ PRIORITY 1",
          "RETRY: REINDEER FLOTILLA",
          "Z:> /FALKEN/GAMES/TICTACTOE/ EXECUTE -PLAYERS 0",
          "================================================",
          "Priority 1 // local / scanning...",
          "scanning ports...",
          "BACKDOOR FOUND (23.45.23.12.00000000)",
          "BACKDOOR FOUND (13.66.23.12.00110000)",
          "BACKDOOR FOUND (13.66.23.12.00110044)",
          "...",
          "...",
          "BRUTE.EXE -r -z",
          "...locating vulnerabilities...",
          "...vulnerabilities found...",
          "MCP/> DEPLOY CLU",
          "SCAN: __ 0100.0000.0554.0080",
          "SCAN: __ 0020.0000.0553.0080",
        ];

        var docfrag = document.createDocumentFragment();

        function updateScreen() {
          txt.push(txt.shift());
          txt.forEach(function(e) {
            var p = document.createElement("p");
            p.textContent = e;
            docfrag.appendChild(p);
          });
          while (c.firstChild) {
            c.removeChild(c.firstChild);
          }
          c.appendChild(docfrag);
        }
    </script>
</body>
</html>
