<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pesan Cinta</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }
        
        .container {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            padding: 60px 40px;
            text-align: center;
            max-width: 500px;
            width: 90%;
            position: relative;
            backdrop-filter: blur(10px);
        }
        
        .tab {
            display: none;
            animation: fadeIn 0.8s ease-in-out;
        }
        
        .tab.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .welcome-title {
            font-size: 32px;
            font-weight: 700;
            color: #4a5568;
            margin-bottom: 20px;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        .love-message {
            font-size: 48px;
            font-weight: 600;
            color: #e53e3e;
            margin-bottom: 30px;
            text-shadow: 0 2px 8px rgba(229, 62, 62, 0.3);
            animation: heartbeat 2s ease-in-out infinite;
        }
        
        @keyframes heartbeat {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
        }
        
        .subtitle {
            font-size: 18px;
            color: #718096;
            margin-bottom: 40px;
            font-weight: 300;
        }
        
        .btn {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 18px;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 8px 20px rgba(102, 126, 234, 0.3);
            font-family: 'Poppins', sans-serif;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 25px rgba(102, 126, 234, 0.4);
        }
        
        .btn:active {
            transform: translateY(-1px);
        }
        
        .btn-success {
            background: linear-gradient(135deg, #48bb78 0%, #38a169 100%);
            box-shadow: 0 8px 20px rgba(72, 187, 120, 0.3);
        }
        
        .btn-success:hover {
            box-shadow: 0 12px 25px rgba(72, 187, 120, 0.4);
        }
        
        .btn-danger {
            background: linear-gradient(135deg, #f56565 0%, #e53e3e 100%);
            box-shadow: 0 8px 20px rgba(245, 101, 101, 0.3);
        }
        
        .btn-danger:hover {
            box-shadow: 0 12px 25px rgba(245, 101, 101, 0.4);
        }
        
        .heart-decoration {
            position: absolute;
            font-size: 20px;
            color: #e53e3e;
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-10px);
            }
        }
        
        .heart-1 {
            top: 20px;
            left: 30px;
            animation-delay: 0s;
        }
        
        .heart-2 {
            top: 30px;
            right: 40px;
            animation-delay: -1s;
        }
        
        .heart-3 {
            bottom: 40px;
            left: 40px;
            animation-delay: -2s;
        }
        
        .heart-4 {
            bottom: 30px;
            right: 30px;
            animation-delay: -0.5s;
        }
        
        .final-message {
            font-size: 24px;
            color: #4a5568;
            margin-bottom: 30px;
            font-weight: 400;
            line-height: 1.6;
        }
        
        .sparkle {
            display: inline-block;
            animation: sparkle 1.5s ease-in-out infinite;
        }
        
        @keyframes sparkle {
            0%, 100% {
                opacity: 1;
                transform: scale(1);
            }
            50% {
                opacity: 0.7;
                transform: scale(1.2);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Dekorasi hati -->
        <div class="heart-decoration heart-1">💖</div>
        <div class="heart-decoration heart-2">💕</div>
        <div class="heart-decoration heart-3">💗</div>
        <div class="heart-decoration heart-4">💝</div>
        
        <!-- Tab 1: Halaman Awal -->
        <div class="tab active" id="tab1">
            <h1 class="welcome-title">Pesan Spesial Untukmu</h1>
            <p class="subtitle">Ada sesuatu yang ingin kusampaikan...</p>
            <button class="btn" onclick="showTab('tab2')">Klik Disini 💕</button>
        </div>
        
        <!-- Tab 2: lanjut -->
        <div class="tab" id="tab2">
            <div class="love-message">lanjut</div>
            <p class="subtitle">Perasaan ini tulus dari hatiku yang paling dalam</p>
            <button class="btn btn-success" onclick="showTab('tab3')">Lanjut 💖</button>
        </div>
        
        <!-- Tab 3: ruslan suka rahma -->
        <div class="tab" id="tab3">
            <div class="love-message">ruslan suka rahma</div>
            <p class="subtitle">Kamu adalah segalanya bagiku</p>
            <button class="btn btn-danger" onclick="showTab('tab4')">Selesai ✨</button>
        </div>
        
        <!-- Tab 4: Pesan Akhir -->
        <div class="tab" id="tab4">
            <div class="final-message">
                <span class="sparkle">✨</span> 
                Terima kasih sudah membaca pesan cintaku 
                <span class="sparkle">✨</span>
            </div>
            <div class="love-message" style="font-size: 36px;">
                Semoga hari-harimu selalu bahagia! 🌟
            </div>
            <button class="btn" onclick="showTab('tab1')">Mulai Lagi 🔄</button>
        </div>
    </div>

    <script>
        function showTab(tabId) {
            // Sembunyikan semua tab
            const tabs = document.querySelectorAll('.tab');
            tabs.forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Tampilkan tab yang dipilih
            document.getElementById(tabId).classList.add('active');
        }
        
        // Efek tambahan untuk dekorasi hati
        document.addEventListener('DOMContentLoaded', function() {
            const hearts = document.querySelectorAll('.heart-decoration');
            hearts.forEach((heart, index) => {
                heart.style.animationDelay = `-${index * 0.5}s`;
            });
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'97cfee91f6605f5f',t:'MTc1NzUxNzg2My4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
