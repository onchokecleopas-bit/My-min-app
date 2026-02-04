<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Earn & Play</title>
    
    <script src="https://richinfo.co/richpartners/telegram/js/sdk.js"></script>
    
    <script>
        // Set the initial balance
        let balance = 0;

        // 1. Initialize the Ad Controller
        window.TelegramAdsController = new TelegramAdsController();
        window.TelegramAdsController.initialize({
            pubId: "1001227",
            appId: "5994",
        });

        // 2. Function to play ad and increase balance
        function playAd() {
            // Show the ad
            window.TelegramAdsController.showAd();
            
            // Logic to increase the number
            balance = balance + 1;
            
            // Update the number shown on the screen
            document.getElementById("balance-count").innerText = balance;
        }
    </script>

    <style>
        body { font-family: sans-serif; text-align: center; background: #1a1a1a; color: white; padding-top: 50px; }
        .balance-box { font-size: 24px; margin-bottom: 20px; background: #333; padding: 10px; border-radius: 10px; display: inline-block; }
        .btn { background: #0088cc; color: white; border: none; padding: 15px 30px; font-size: 18px; border-radius: 10px; cursor: pointer; }
    </style>
</head>
<body>

    <div class="balance-box">
        💰 Balance: <span id="balance-count">0</span>
    </div>

    <br>
    
    <button class="btn" onclick="playAd()">📺 Watch Ad (+1)</button>

</body>
</html>
