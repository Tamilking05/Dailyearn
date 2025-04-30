<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Earn Cash App</title>
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #333;
        }
        
        .container {
            max-width: 500px;
            margin: 0 auto;
            background: linear-gradient(135deg, #6e8efb, #a777e3);
            min-height: 100vh;
            padding: 20px;
            position: relative;
            overflow: hidden;
        }
        
        /* Header Styles */
        .header {
            text-align: center;
            padding: 30px 0 20px;
            color: white;
        }
        
        .header h1 {
            font-size: 28px;
            margin-bottom: 10px;
            font-weight: 700;
        }
        
        .header p {
            font-size: 16px;
            opacity: 0.9;
            margin-bottom: 20px;
        }
        
        .btn {
            background: #ff9500;
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 50px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(255,149,0,0.4);
            display: inline-block;
            margin: 10px 0;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255,149,0,0.5);
        }
        
        /* Dashboard Styles */
        .dashboard {
            background: white;
            border-radius: 20px;
            padding: 20px;
            margin-top: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .dashboard-title {
            text-align: center;
            font-size: 18px;
            margin-bottom: 20px;
            color: #6e8efb;
            font-weight: 600;
        }
        
        .options-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .option-card {
            background: #f8f9fa;
            border-radius: 15px;
            padding: 15px 10px;
            text-align: center;
            cursor: pointer;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .option-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .option-card img {
            width: 40px;
            height: 40px;
            margin-bottom: 10px;
        }
        
        .option-card h3 {
            font-size: 14px;
            color: #333;
        }
        
        /* Balance Card */
        .balance-card {
            background: linear-gradient(135deg, #4CAF50, #8BC34A);
            border-radius: 15px;
            padding: 20px;
            margin: 20px 0;
            color: white;
            text-align: center;
            box-shadow: 0 5px 15px rgba(76,175,80,0.3);
        }
        
        .balance-card h2 {
            font-size: 16px;
            margin-bottom: 10px;
            font-weight: 500;
        }
        
        .coin-balance {
            font-size: 36px;
            font-weight: bold;
            margin-bottom: 5px;
        }
        
        .money-value {
            font-size: 20px;
            font-weight: bold;
        }
        
        /* Activity Screens (hidden by default) */
        .activity-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.9);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            z-index: 100;
            display: none;
        }
        
        .activity-box {
            background: white;
            padding: 25px;
            border-radius: 20px;
            width: 90%;
            max-width: 350px;
            text-align: center;
            position: relative;
        }
        
        .close-btn {
            position: absolute;
            top: 15px;
            right: 15px;
            color: #777;
            font-size: 24px;
            cursor: pointer;
        }
        
        .activity-title {
            font-size: 22px;
            margin-bottom: 15px;
            color: #6e8efb;
        }
        
        .activity-desc {
            font-size: 16px;
            margin-bottom: 20px;
            color: #555;
        }
        
        /* Wheel Styles */
        .wheel {
            width: 250px;
            height: 250px;
            margin: 20px auto;
            position: relative;
            border-radius: 50%;
            overflow: hidden;
            border: 10px solid #ff9500;
            box-shadow: 0 0 0 5px #333, 0 0 0 15px #f5f5f5;
        }
        
        .wheel-item {
            position: absolute;
            width: 50%;
            height: 50%;
            transform-origin: 100% 100%;
            left: 0;
            top: 0;
            text-align: center;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: white;
        }
        
        /* Scratch Card Styles */
        .scratch-card {
            width: 280px;
            height: 180px;
            background: linear-gradient(135deg, #ff9500, #ff5e62);
            border-radius: 15px;
            position: relative;
            overflow: hidden;
            margin: 20px auto;
        }
        
        .scratch-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #ddd url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAUCAYAAACNiR0NAAAABmJLR0QA/wD/AP+gvaeTAAAA+UlEQVQ4y+3UMUoDQRTG8Z8psJBUKTyAR7ATvIBgKTYW1oKtnRewsbG0sbKQNFZCTCFiIYgQEEFEEBEFwWJfYV52Z3dDUvjBYJj5vvfezJsZ/qdGOMYz5rGCNl5wj0s8VK1QxwV2MZqRj2EfZ5jJq7CHY0xXqDqJfZxUqXqI8YrVx3CAo7KqR5ioUX0U+zgsqtrFdM3qI9jDQV7VHqYaVB/GLvbyqu5jpmH1IexiN6vqHmYHqD6IHexkVd3F3IDVB7CN7ayqO5gfovoAtrCVVXUbC0NWH8AmNrOqbmJxyOoD2MBGVtV1LI1QfQDrWM+quoZlD6j6GtaxllV1FSsjVh/AKlazqq5g1QOqPsAKVrKqLmPNA6o+wDJWs6ouYd0Dqj7AEjayqi5iwwOqPsAiNrOqLmDTA6o+wDw2s6rOYcsDqj7AHLayqs5i2wOqPsAMtrOqzmDHA6o+wDS2sqpOYdcDqj7AFLazqk5izwOqPsAkdrKqTmDfA6o+wDh2s6qOYc8Dqj7AGPayqo5i3wOqPsAI9rOqDuPAA6o+wBD2s6oO4tADqj7AAA6zqvbjyAOqPkAfjrKq9uLYA6o+QC+Os6r24MQDqj5AD06yqnbj1AOqPkAXTrOqduHMA6o+QCfOsqp24NwDqj5AO86zqrbhwgOqPkAbLrKqtuLSA6o+QCsus6q24MoDqj5AC66yqj7j2gOqPsATrrOqPuHGA6o+wCNusqo+4NYDqj7AA26zqt7jzgOqPsA97rOq3uHBA6o+wC3usqre4tEDqj7ADW6zql7jCQ+o+gBXeMqqeoVnPKDqA1zgOavqOV7wgKoPcIZzXOBV1Qd4xSuqPsApTnCCd1Uf4B3HOMIRPvCJz5KqX/jCF77xjR/8FFT9xS9+8Yc//OMf/wC2dXm5Xa4R5QAAAABJRU5ErkJggg==');
            cursor: grab;
        }
        
        .scratch-result {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 24px;
            font-weight: bold;
            color: white;
            display: none;
        }
        
        /* Withdraw Screen */
        .withdraw-options {
            margin: 20px 0;
        }
        
        .withdraw-option {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 10px;
            margin-bottom: 10px;
            cursor: pointer;
        }
        
        .withdraw-option.selected {
            border-color: #4CAF50;
            background-color: #f8fff8;
        }
        
        .withdraw-amount {
            font-weight: bold;
            color: #333;
        }
        
        .withdraw-value {
            color: #4CAF50;
            font-weight: bold;
        }
        
        .upi-input {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 10px;
            margin: 15px 0;
            font-size: 16px;
        }
        
        /* Referral Screen */
        .referral-code {
            background: #f0f0f0;
            padding: 15px;
            border-radius: 10px;
            margin: 20px 0;
            font-size: 18px;
            font-weight: bold;
            text-align: center;
            color: #6e8efb;
        }
        
        .social-share {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 20px 0;
        }
        
        .social-share img {
            width: 40px;
            height: 40px;
            cursor: pointer;
        }
        
        /* Notification */
        .notification {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            background: #4CAF50;
            color: white;
            padding: 15px 25px;
            border-radius: 50px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            z-index: 1000;
            display: none;
            animation: slideIn 0.5s, fadeOut 0.5s 2.5s forwards;
        }
        
        @keyframes slideIn {
            from { top: -50px; opacity: 0; }
            to { top: 20px; opacity: 1; }
        }
        
        @keyframes fadeOut {
            from { opacity: 1; }
            to { opacity: 0; }
        }
        
        /* Coin Chart */
        .coin-chart {
            margin: 20px 0;
            padding: 15px;
            background: #f0f0f0;
            border-radius: 10px;
        }
        
        .chart-row {
            display: flex;
            justify-content: space-between;
            padding: 8px 0;
            border-bottom: 1px solid #ddd;
        }
        
        .chart-row:last-child {
            border-bottom: none;
        }
    </style>
</head>
<body>
    <!-- Launch Screen -->
    <div class="container" id="launchScreen">
        <div class="header">
            <h1>Earn Cash App</h1>
            <p>Turn Your Free Time Into Real Cash! Start Earning Today!</p>
            <button class="btn" onclick="showDashboard()">Start Now</button>
        </div>
    </div>
    
    <!-- Dashboard Screen (hidden initially) -->
    <div class="container" id="dashboardScreen" style="display: none;">
        <div class="header">
            <h1>Earn Cash App</h1>
            <p>Collect Coins, Unlock Rewards, and Cash Out Instantly!</p>
        </div>
        
        <div class="dashboard">
            <div class="dashboard-title">Choose How You Want to Earn</div>
            
            <div class="options-grid">
                <div class="option-card" onclick="openWheel()">
                    <img src="https://cdn-icons-png.flaticon.com/512/3209/3209260.png" alt="Spin Wheel">
                    <h3>Spin Wheel</h3>
                </div>
                
                <div class="option-card" onclick="openVideo()">
                    <img src="https://cdn-icons-png.flaticon.com/512/3670/3670147.png" alt="Watch Videos">
                    <h3>Watch Videos</h3>
                </div>
                
                <div class="option-card" onclick="openScratch()">
                    <img src="https://cdn-icons-png.flaticon.com/512/1037/1037933.png" alt="Scratch & Win">
                    <h3>Scratch & Win</h3>
                </div>
                
                <div class="option-card" onclick="openWallet()">
                    <img src="https://cdn-icons-png.flaticon.com/512/3132/3132693.png" alt="Wallet">
                    <h3>Wallet</h3>
                </div>
                
                <div class="option-card" onclick="openWithdraw()">
                    <img src="https://cdn-icons-png.flaticon.com/512/159/159268.png" alt="Withdraw">
                    <h3>Withdraw</h3>
                </div>
                
                <div class="option-card" onclick="openReferral()">
                    <img src="https://cdn-icons-png.flaticon.com/512/3079/3079165.png" alt="Refer & Earn">
                    <h3>Refer & Earn</h3>
                </div>
            </div>
            
            <div class="balance-card">
                <h2>Your Current Balance</h2>
                <div class="coin-balance" id="coinBalance">0</div>
                <div class="money-value" id="moneyValue">₹0</div>
            </div>
        </div>
    </div>
    
    <!-- Spin Wheel Screen -->
    <div class="activity-screen" id="wheelScreen">
        <div class="activity-box">
            <span class="close-btn" onclick="closeWheel()">×</span>
            <h2 class="activity-title">Spin the Wheel</h2>
            <p class="activity-desc">Feeling Lucky? Spin Now and Win small!</p>
            
            <div class="wheel" id="wheel">
                <!-- Wheel segments will be added by JavaScript -->
            </div>
            
            <button class="btn" onclick="spinWheel()">SPIN NOW</button>
            <p style="margin-top: 15px; color: #777;">Or watch an ad for a free spin</p>
            <button class="btn" style="background: #6e8efb;" onclick="watchAdForFreeSpin()">WATCH AD</button>
        </div>
    </div>
    
    <!-- Watch Videos Screen -->
    <div class="activity-screen" id="videoScreen">
        <div class="activity-box">
            <span class="close-btn" onclick="closeVideo()">×</span>
            <h2 class="activity-title">Watch & Earn</h2>
            <p class="activity-desc">Watch & Earn! Every Second Counts!</p>
            
            <div style="background: #000; width: 100%; height: 200px; border-radius: 10px; margin: 20px 0; display: flex; justify-content: center; align-items: center; color: white;">
                [VIDEO AD WILL PLAY HERE]
            </div>
            
            <button class="btn" onclick="watchVideo()">WATCH VIDEO</button>
            <p style="margin-top: 15px; color: #777;">Earn 10-20 coins per video</p>
        </div>
    </div>
    
    <!-- Scratch & Win Screen -->
    <div class="activity-screen" id="scratchScreen">
        <div class="activity-box">
            <span class="close-btn" onclick="closeScratch()">×</span>
            <h2 class="activity-title">Scratch & Win</h2>
            <p class="activity-desc">Your Luck Is Waiting! Scratch to Reveal Your Prize.</p>
            
            <div class="scratch-card">
                <div class="scratch-overlay" id="scratchOverlay"></div>
                <div class="scratch-result" id="scratchResult">
                    You won 1,2,5,9,8,coins!
                </div>
            </div>
            
            <button class="btn" onclick="scratchAnother()">SCRATCH ANOTHER</button>
            <p style="margin-top: 15px; color: #777;">Costs 3 to 9 below coins per scratch</p>
        </div>
    </div>
    
    <!-- Wallet Screen -->
    <div class="activity-screen" id="walletScreen">
        <div class="activity-box">
            <span class="close-btn" onclick="closeWallet()">×</span>
            <h2 class="activity-title">Your Wallet</h2>
            <p class="activity-desc">Your Wallet, Your Power!</p>
            
            <div class="balance-card" style="margin: 20px auto;">
                <div class="coin-balance" id="walletCoinBalance">0</div>
                <div class="money-value" id="walletMoneyValue">₹0</div>
            </div>
            
            <div class="coin-chart">
                <div class="chart-row">
                    <span>1000 Coins</span>
                    <span>= ₹10</span>
                </div>
                <div class="chart-row">
                    <span>2000 Coins</span>
                    <span>= ₹20</span>
                </div>
                <div class="chart-row">
                    <span>5000 Coins</span>
                    <span>= ₹50</span>
                </div>
                <div class="chart-row">
                    <span>10000 Coins</span>
                    <span>= ₹100</span>
                </div>
            </div>
            
            <button class="btn" onclick="openWithdraw()">WITHDRAW NOW</button>
        </div>
    </div>
    
    <!-- Withdraw Screen -->
    <div class="activity-screen" id="withdrawScreen">
        <div class="activity-box">
            <span class="close-btn" onclick="closeWithdraw()">×</span>
            <h2 class="activity-title">Withdraw Earnings</h2>
            <p class="activity-desc">Ready to Cash Out? Transfer to Your UPI Account!</p>
            
            <div class="withdraw-options">
                <div class="withdraw-option" onclick="selectWithdraw(this, 1000)">
                    <span class="withdraw-amount">1000 Coins</span>
                    <span class="withdraw-value">₹10</span>
                </div>
                
                <div class="withdraw-option" onclick="selectWithdraw(this, 2000)">
                    <span class="withdraw-amount">2000 Coins</span>
                    <span class="withdraw-value">₹20</span>
                </div>
            </div>
            
            <input type="text" class="upi-input" id="upiId" placeholder="Enter your UPI ID">
            <button class="btn" onclick="processWithdrawal()">WITHDRAW</button>
            
            <p style="margin-top: 15px; color: #777; font-size: 14px;">Minimum withdrawal: 1000 coins (₹10)</p>
        </div>
    </div>
    
    <!-- Refer & Earn Screen -->
    <div class="activity-screen" id="referralScreen">
        <div class="activity-box">
            <span class="close-btn" onclick="closeReferral()">×</span>
            <h2 class="activity-title">Refer & Earn</h2>
            <p class="activity-desc">Invite, Earn, Repeat! Get 100 Coins for Every Friend Who Joins.</p>
            
            <div class="referral-code">
                Your Code: EARN100
            </div>
            
            <p style="margin: 15px 0; color: #555;">Share your referral code with friends and earn when they sign up and start earning!</p>
            
            <div class="social-share">
                <img src="https://cdn-icons-png.flaticon.com/512/3670/3670127.png" alt="WhatsApp" onclick="shareViaWhatsApp()">
                <img src="https://cdn-icons-png.flaticon.com/512/2111/2111463.png" alt="Instagram" onclick="shareViaInstagram()">
                <img src="https://cdn-icons-png.flaticon.com/512/733/733579.png" alt="Twitter" onclick="shareViaTwitter()">
                <img src="https://cdn-icons-png.flaticon.com/512/2111/2111370.png" alt="Telegram" onclick="shareViaTelegram()">
            </div>
            
            <button class="btn" style="background: #6e8efb;" onclick="copyReferralCode()">COPY REFERRAL CODE</button>
        </div>
    </div>
    
    <!-- Notification -->
    <div class="notification" id="notification">
        You earned 50 coins!
    </div>
    
    <script>
        // App Variables
        let coins = 300; // Starting coins
        let selectedWithdrawAmount = 0;
        
        // DOM Elements
        const launchScreen = document.getElementById('launchScreen');
        const dashboardScreen = document.getElementById('dashboardScreen');
        const coinBalanceEl = document.getElementById('coinBalance');
        const moneyValueEl = document.getElementById('moneyValue');
        const walletCoinBalanceEl = document.getElementById('walletCoinBalance');
        const walletMoneyValueEl = document.getElementById('walletMoneyValue');
        const notificationEl = document.getElementById('notification');
        
        // Activity Screens
        const wheelScreen = document.getElementById('wheelScreen');
        const videoScreen = document.getElementById('videoScreen');
        const scratchScreen = document.getElementById('scratchScreen');
        const walletScreen = document.getElementById('walletScreen');
        const withdrawScreen = document.getElementById('withdrawScreen');
        const referralScreen = document.getElementById('referralScreen');
        
        // Initialize the app
        function init() {
            updateBalance();
            createWheel();
            initScratchCard();
        }
        
        // Show dashboard screen
        function showDashboard() {
            launchScreen.style.display = 'none';
            dashboardScreen.style.display = 'block';
        }
        
        // Update balance display
        function updateBalance() {
            coinBalanceEl.textContent = coins;
            moneyValueEl.textContent = `₹${(coins / 100).toFixed(2)}`;
            walletCoinBalanceEl.textContent = coins;
            walletMoneyValueEl.textContent = `₹${(coins / 100).toFixed(2)}`;
        }
        
        // Show notification
        function showNotification(message) {
            notificationEl.textContent = message;
            notificationEl.style.display = 'block';
            setTimeout(() => {
                notificationEl.style.display = 'none';
            }, 3000);
        }
        
        // Wheel Functions
        function createWheel() {
            const wheel = document.getElementById('wheel');
            const prizes = [50, 100, 150, 200, 250, 300, 350, 500];
            const colors = ['#FF5252', '#FF4081', '#E040FB', '#7C4DFF', '#536DFE', '#448AFF', '#40C4FF', '#18FFFF'];
            
            wheel.innerHTML = '';
            
            prizes.forEach((prize, index) => {
                const segment = document.createElement('div');
                segment.className = 'wheel-item';
                segment.style.transform = `rotate(${index * 45}deg) skewY(-45deg)`;
                segment.style.backgroundColor = colors[index];
                segment.textContent = prize;
                wheel.appendChild(segment);
            });
        }
        
        function openWheel() {
            wheelScreen.style.display = 'flex';
        }
        
        function closeWheel() {
            wheelScreen.style.display = 'none';
        }
        
        function spinWheel() {
            if (coins < 50) {
                showNotification('You need at least 50 coins to spin!');
                return;
            }
            
            coins -= 50; // Deduct spin cost
            updateBalance();
            
            const wheel = document.getElementById('wheel');
            const spinBtn = document.querySelector('.spin-btn');
            
            spinBtn.disabled = true;
            
            // Random spin (3-8 full rotations plus segment)
            const segmentAngle = 45;
            const prizeIndex = Math.floor(Math.random() * 8);
            const extraRotations = Math.floor(Math.random() * 5) + 3;
            const totalRotation = 360 * extraRotations + (prizeIndex * segmentAngle);
            
            wheel.style.transition = 'transform 3s cubic-bezier(0.17, 0.67, 0.12, 0.99)';
            wheel.style.transform = `rotate(${-totalRotation}deg)`;
            
            setTimeout(() => {
                const prizes = [50, 100, 150, 200, 250, 300, 350, 500];
                const prize = prizes[prizeIndex];
                
                coins += prize;
                updateBalance();
                showNotification(`You won ${prize} coins! Keep Spinning to Win More.`);
                
                spinBtn.disabled = false;
                wheel.style.transition = 'none';
                wheel.style.transform = 'rotate(0deg)';
                setTimeout(() => {
                    wheel.style.transition = 'transform 3s cubic-bezier(0.17, 0.67, 0.12, 0.99)';
                }, 10);
            }, 3000);
        }
        
        function watchAdForFreeSpin() {
            showNotification('Playing ad for free spin...');
            setTimeout(() => {
                showNotification('You earned a free spin!');
                spinWheel();
            }, 2000);
        }
        
        // Video Functions
        function openVideo() {
            videoScreen.style.display = 'flex';
        }
        
        function closeVideo() {
            videoScreen.style.display = 'none';
        }
        
        function watchVideo() {
            showNotification('Playing video ad...');
            
            setTimeout(() => {
                const reward = Math.floor(Math.random() * 50) + 25; // 25-75 coins
                coins += reward;
                updateBalance();
                showNotification(`Awesome! You've earned ${reward} Coins for watching. Keep going!`);
            }, 3000);
        }
        
        // Scratch Card Functions
        function initScratchCard() {
            const overlay = document.getElementById('scratchOverlay');
            const result = document.getElementById('scratchResult');
            
            // Set up canvas
            overlay.width = overlay.offsetWidth;
            overlay.height = overlay.offsetHeight;
            
            let ctx = overlay.getContext('2d');
            ctx.fillStyle = '#ddd';
            ctx.fillRect(0, 0, overlay.width, overlay.height);
            ctx.globalCompositeOperation = 'destination-out';
            
            let isDrawing = false;
            
            overlay.addEventListener('mousedown', (e) => {
                isDrawing = true;
                const rect = overlay.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                ctx.beginPath();
                ctx.arc(x, y, 20, 0, Math.PI * 2);
                ctx.fill();
            });
            
            overlay.addEventListener('mousemove', (e) => {
                if (!isDrawing) return;
                const rect = overlay.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                ctx.beginPath();
                ctx.arc(x, y, 20, 0, Math.PI * 2);
                ctx.fill();
                
                // Check if enough area is scratched
                const imageData = ctx.getImageData(0, 0, overlay.width, overlay.height);
                const pixelData = imageData.data;
                let transparentPixels = 0;
                
                for (let i = 3; i < pixelData.length; i += 4) {
                    if (pixelData[i] === 0) {
                        transparentPixels++;
                    }
                }
                
                const scratchedPercent = (transparentPixels / (overlay.width * overlay.height)) * 100;
                
                if (scratchedPercent > 30) {
                    revealScratchResult();
                }
            });
            
            overlay.addEventListener('mouseup', () => {
                isDrawing = false;
            });
            
            overlay.addEventListener('mouseleave', () => {
                isDrawing = false;
            });
        }
        
        function revealScratchResult() {
            const overlay = document.getElementById('scratchOverlay');
            const result = document.getElementById('scratchResult');
            
            const prizes = [50, 75, 100, 150, 200];
            const prize = prizes[Math.floor(Math.random() * prizes.length)];
            
            overlay.style.display = 'none';
            result.style.display = 'flex';
            result.textContent = `You Won ${prize} Coins! Scratch Daily for More Surprises!`;
            
            setTimeout(() => {
                coins += prize;
                updateBalance();
            }, 500);
        }
        
        function openScratch() {
            if (coins < 30) {
                showNotification('You need at least 30 coins to scratch!');
                return;
            }
            
            coins -= 30; // Deduct scratch cost
            updateBalance();
            
            scratchScreen.style.display = 'flex';
            document.getElementById('scratchOverlay').style.display = 'block';
            document.getElementById('scratchResult').style.display = 'none';
            
            // Reset scratch overlay
            const overlay = document.getElementById('scratchOverlay');
            const ctx = overlay.getContext('2d');
            ctx.fillStyle = '#ddd';
            ctx.fillRect(0, 0, overlay.width, overlay.height);
            ctx.globalCompositeOperation = 'destination-out';
        }
        
        function closeScratch() {
            scratchScreen.style.display = 'none';
        }
        
        function scratchAnother() {
            openScratch();
        }
        
        // Wallet Functions
        function openWallet() {
            walletScreen.style.display = 'flex';
        }
        
        function closeWallet() {
            walletScreen.style.display = 'none';
        }
        
        // Withdraw Functions
        function openWithdraw() {
            if (coins < 1000) {
                showNotification('You need at least 1000 coins (₹10) to withdraw!');
                return;
            }
            
            withdrawScreen.style.display = 'flex';
            selectedWithdrawAmount = 0;
            
            // Reset selected option
            const options = document.querySelectorAll('.withdraw-option');
            options.forEach(option => {
                option.classList.remove('selected');
            });
        }
        
        function closeWithdraw() {
            withdrawScreen.style.display = 'none';
        }
        
        function selectWithdraw(element, amount) {
            selectedWithdrawAmount = amount;
            
            // Update UI
            const options = document.querySelectorAll('.withdraw-option');
            options.forEach(option => {
                option.classList.remove('selected');
            });
            
            element.classList.add('selected');
        }
        
        function processWithdrawal() {
            const upiId = document.getElementById('upiId').value;
            
            if (!selectedWithdrawAmount) {
                showNotification('Please select an amount to withdraw');
                return;
            }
            
            if (!upiId) {
                showNotification('Please enter your UPI ID');
                return;
            }
            
            if (coins < selectedWithdrawAmount) {
                showNotification(`You don't have enough coins for this withdrawal`);
                return;
            }
            
            // Process withdrawal
            coins -= selectedWithdrawAmount;
            updateBalance();
            
            showNotification(`Withdrawal successful! ₹${selectedWithdrawAmount/100} will be sent to ${upiId}`);
            closeWithdraw();
        }
        
        // Referral Functions
        function openReferral() {
            referralScreen.style.display = 'flex';
        }
        
        function closeReferral() {
            referralScreen.style.display = 'none';
        }
        
        function copyReferralCode() {
            navigator.clipboard.writeText('EARN100');
            showNotification('Referral code copied to clipboard!');
        }
        
        function shareViaWhatsApp() {
            showNotification('Sharing via WhatsApp...');
        }
        
        function shareViaInstagram() {
            showNotification('Sharing via Instagram...');
        }
        
        function shareViaTwitter() {
            showNotification('Sharing via Twitter...');
        }
        
        function shareViaTelegram() {
            showNotification('Sharing via Telegram...');
        }
        
        // Initialize the app when loaded
        window.onload = init;
    </script>
</body>
</html>
