<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>山陰吃貨修行隨身助手</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+JP:wght@400;700&family=Noto+Sans+TC:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Noto Sans TC', sans-serif;
            background-color: #F8F5F0;
            color: #333;
            -webkit-tap-highlight-color: transparent;
        }
        .serif { font-family: 'Noto Serif JP', serif; }
        .card {
            background: #FFFFFF;
            border-radius: 16px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.03);
            margin-bottom: 1rem;
            overflow: hidden;
            border: 1px solid #EAE2D6;
        }
        .nav-tab.active {
            color: #8C6A5E;
            border-bottom: 2px solid #8C6A5E;
        }
        .tag {
            padding: 2px 8px;
            border-radius: 4px;
            font-size: 0.7rem;
            font-weight: bold;
            display: inline-block;
            margin-bottom: 4px;
        }
        .tag-food { background: #FFE8E8; color: #D65A5A; }
        .tag-spot { background: #E8F5FF; color: #5A8BD6; }
        .tag-buy { background: #F0FFE8; color: #5AD677; }
        .glass-nav {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            border-top: 1px solid #EEE;
        }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
    </style>
</head>
<body class="pb-24">

    <!-- Header -->
    <header class="p-6 pt-10 bg-white border-b border-stone-100">
        <h1 class="serif text-2xl font-bold text-stone-800 tracking-tight">山陰 8 日吃貨修行旅</h1>
        <div class="flex items-center mt-2 text-stone-500 text-xs">
            <span class="mr-3">📅 2026.01.16 - 01.23</span>
            <span>🚗 自駕行程</span>
        </div>
    </header>

    <!-- Top Navigation -->
    <div class="sticky top-0 z-50 bg-white/80 backdrop-blur-md px-4 py-2 border-b border-stone-100">
        <div class="flex space-x-6 overflow-x-auto no-scrollbar text-sm font-medium text-stone-400">
            <button onclick="switchTab('itinerary')" id="tab-itinerary" class="nav-tab active pb-2 whitespace-nowrap">每日行程</button>
            <button onclick="switchTab('transport')" id="tab-transport" class="nav-tab pb-2 whitespace-nowrap">交通住宿</button>
            <button onclick="switchTab('finance')" id="tab-finance" class="nav-tab pb-2 whitespace-nowrap">預算開支</button>
            <button onclick="switchTab('sos')" id="tab-sos" class="nav-tab pb-2 whitespace-nowrap">緊急/攻略</button>
        </div>
    </div>

    <main id="app-content" class="p-4">
        
        <!-- Tab: Itinerary -->
        <div id="content-itinerary" class="tab-content">
            
            <!-- Day 1: 松江 -->
            <div class="mb-8">
                <div class="flex justify-between items-center mb-3">
                    <h2 class="serif text-xl font-bold text-stone-700">D1 松江・千鳥城之旅</h2>
                    <span class="text-xs text-stone-400">☀️ 18°C</span>
                </div>
                
                <div class="card p-4">
                    <div class="flex justify-between">
                        <div>
                            <span class="text-[10px] bg-stone-100 text-stone-500 px-2 py-0.5 rounded">12:00 - 14:00</span>
                            <h3 class="font-bold text-lg">美保飛行場 (米子機場)</h3>
                        </div>
                        <button onclick="openMap('米子機場')" class="bg-stone-800 text-white p-2 rounded-full h-10 w-10 flex items-center justify-center">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path></svg>
                        </button>
                    </div>
                    <div class="mt-3 text-sm space-y-2">
                        <p><span class="tag tag-spot">手續</span> 取車地點：ORIX 租車。請確認**預約編號**與**保險內容**。</p>
                        <p><span class="tag tag-food">吃貨</span> 機場內可買「大山白玫瑰牛乳」相關點心先行墊胃。</p>
                    </div>
                </div>

                <div class="card p-4">
                    <div class="flex justify-between">
                        <div>
                            <span class="text-[10px] bg-stone-100 text-stone-500 px-2 py-0.5 rounded">14:43 - 16:46</span>
                            <h3 class="font-bold text-lg">松江城 & 堀川遊覽船</h3>
                        </div>
                        <button onclick="openMap('松江城')" class="bg-stone-800 text-white p-2 rounded-full h-10 w-10 flex items-center justify-center">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path></svg>
                        </button>
                    </div>
                    <div class="mt-3 text-sm space-y-2">
                        <p><span class="tag tag-spot">攻略</span> 國寶 5 城之一。遊覽船冬季有「暖桌船」，一定要體驗。</p>
                    </div>
                </div>
            </div>

            <!-- Day 2: 出雲 -->
            <div class="mb-8">
                <div class="flex justify-between items-center mb-3">
                    <h2 class="serif text-xl font-bold text-stone-700">D2 出雲・結緣神之國</h2>
                    <span class="text-xs text-stone-400">☁️ 16°C</span>
                </div>
                <div class="card p-4">
                    <h3 class="font-bold text-lg">出雲大社</h3>
                    <div class="mt-3 text-sm space-y-2">
                        <p><span class="tag tag-spot">重點</span> 參拜方式為「二禮、四拍手、一禮」，與一般神社不同。</p>
                        <p><span class="tag tag-food">必吃</span> **出雲蕎麥麵 (割子蕎麥)**。推薦：田中屋或かねや。</p>
                        <p><span class="tag tag-buy">必買</span> 結緣御守、神在餅 (紅豆麻糬原型)。</p>
                    </div>
                    <button onclick="openMap('出雲大社')" class="mt-4 w-full bg-stone-100 text-stone-800 py-2 rounded-lg text-sm font-bold flex items-center justify-center">
                        導航至出雲大社 <svg class="ml-2 w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path></svg>
                    </button>
                </div>
            </div>

            <!-- Day 3-5: 足立 & 溫泉 (Summary based on PDF) -->
            <div class="mb-8">
                <h2 class="serif text-xl font-bold text-stone-700 mb-3">D3-D5 藝術與秘湯</h2>
                <div class="card p-4">
                    <h3 class="font-bold text-lg">足立美術館</h3>
                    <p class="text-sm text-stone-600 mt-1">連續 20 年日本第一庭園。</p>
                    <div class="mt-2 text-xs space-y-1">
                        <p>📍 導航地點：島根縣安來市古川町458</p>
                        <p>💡 攻略：從咖啡廳窗口看的庭園猶如「活的畫框」。</p>
                    </div>
                </div>
                <div class="card p-4">
                    <h3 class="font-bold text-lg">三朝溫泉修行</h3>
                    <p class="text-sm text-stone-600 mt-1">全球稀有的鐳溫泉，可「吸、喝、泡」。</p>
                    <div class="mt-2 flex space-x-2">
                        <span class="tag tag-food">必點：海鮮丼</span>
                        <span class="tag tag-food">必吃：二十世紀梨</span>
                    </div>
                </div>
            </div>

            <!-- Day 6-8: 鳥取 -->
            <div class="mb-8">
                <h2 class="serif text-xl font-bold text-stone-700 mb-3">D6-D8 鳥取砂丘・歸途</h2>
                <div class="card p-4 border-l-4 border-l-stone-800">
                    <h3 class="font-bold text-lg">鳥取砂丘 & 砂之美術館</h3>
                    <div class="mt-3 text-sm space-y-2">
                        <p><span class="tag tag-spot">攻略</span> 建議早上前往砂丘，才能看到未被腳印踩亂的「風紋」。</p>
                        <p><span class="tag tag-food">必吃</span> **松葉蟹 (冬限)** 或 **紅楚蟹**。地點：賀露市場。</p>
                        <p class="font-bold text-red-600 text-xs">❗ 重要：Day 8 須在 12:00 前回到米子機場還車。</p>
                    </div>
                    <button onclick="openMap('鳥取砂丘')" class="mt-4 w-full bg-stone-800 text-white py-2 rounded-lg text-sm">開啟導航</button>
                </div>
            </div>
        </div>

        <!-- Tab: Transport -->
        <div id="content-transport" class="tab-content hidden">
            <h2 class="serif text-2xl font-bold mb-6">交通與住宿資訊</h2>
            
            <div class="card p-5 bg-stone-50 border-none">
                <p class="text-[10px] uppercase tracking-widest text-stone-400">Flight Info</p>
                <div class="flex justify-between items-center mt-2">
                    <div class="text-center">
                        <p class="text-2xl font-bold">TPE</p>
                        <p class="text-[10px]">06:40</p>
                    </div>
                    <div class="flex-1 px-4 flex flex-col items-center">
                        <span class="text-[10px] text-stone-400">CX-511</span>
                        <div class="w-full h-[1px] bg-stone-300 relative">
                            <div class="absolute -top-1 right-0">✈️</div>
                        </div>
                    </div>
                    <div class="text-center">
                        <p class="text-2xl font-bold">YNJ</p>
                        <p class="text-[10px]">12:00</p>
                    </div>
                </div>
            </div>

            <div class="card p-5">
                <h3 class="font-bold text-lg mb-2">🚗 自駕備忘錄</h3>
                <div class="text-sm space-y-2">
                    <p class="flex justify-between"><span>業者:</span> <span class="font-medium">ORIX Rent-a-car</span></p>
                    <p class="flex justify-between"><span>預約號:</span> <span class="font-bold underline">#MC-8822931</span></p>
                    <p class="flex justify-between"><span>油費政策:</span> <span class="font-medium">滿油還車</span></p>
                </div>
            </div>

            <div class="card p-5">
                <h3 class="font-bold text-lg mb-2">🏨 住宿點</h3>
                <div class="space-y-4">
                    <div class="border-b border-stone-100 pb-2">
                        <p class="font-medium">三朝溫泉觀光案內所周邊</p>
                        <p class="text-xs text-stone-400">鳥取縣東伯郡三朝町三朝973-1</p>
                        <p class="text-xs text-stone-800 mt-1 font-bold">預約號：901123445</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Tab: Finance -->
        <div id="content-finance" class="tab-content hidden">
            <h2 class="serif text-2xl font-bold mb-4">修行開支</h2>
            <div class="grid grid-cols-2 gap-3 mb-6">
                <div class="bg-white p-4 rounded-xl border border-stone-200">
                    <p class="text-[10px] text-stone-400">今日花費</p>
                    <p class="text-lg font-bold">¥ 4,500</p>
                </div>
                <div class="bg-white p-4 rounded-xl border border-stone-200">
                    <p class="text-[10px] text-stone-400">總餘額</p>
                    <p class="text-lg font-bold text-green-600">¥ 82,000</p>
                </div>
            </div>
            
            <div id="expense-items" class="space-y-2">
                <!-- Items added dynamically -->
                <div class="flex justify-between text-sm p-2 bg-white rounded border border-stone-100">
                    <span>租車(預約)</span>
                    <span class="font-mono">¥ 28,000</span>
                </div>
                <div class="flex justify-between text-sm p-2 bg-white rounded border border-stone-100">
                    <span>松江城門票</span>
                    <span class="font-mono">¥ 680</span>
                </div>
            </div>
            <button onclick="addExp()" class="w-full mt-4 py-3 border-2 border-dashed border-stone-300 rounded-xl text-stone-400 text-sm">
                + 新增吃貨開支
            </button>
        </div>

        <!-- Tab: SOS -->
        <div id="content-sos" class="tab-content hidden">
            <h2 class="serif text-2xl font-bold mb-4 text-red-800">緊急聯絡 & 攻略</h2>
            <div class="space-y-3">
                <a href="tel:110" class="flex justify-between items-center p-4 bg-red-50 text-red-900 rounded-xl font-bold">
                    <span>警察報案</span>
                    <span>110</span>
                </a>
                <a href="tel:119" class="flex justify-between items-center p-4 bg-red-50 text-red-900 rounded-xl font-bold">
                    <span>火災/急救</span>
                    <span>119</span>
                </a>
                <div class="card p-4">
                    <h3 class="font-bold mb-2">💡 山陰自駕攻略</h3>
                    <ul class="text-sm list-disc ml-5 space-y-2 text-stone-600">
                        <li>**加油站：** 山陰鄉下路段加油站較少，油錶剩 1/3 請務必加滿。</li>
                        <li>**停車：** 景點多設有免費停車場，松江城附近則需收費。</li>
                        <li>**導航：** 車載導航建議使用 **MapCode**，輸入更精準。</li>
                        <li>**休息站 (Michi-no-Eki)：** 小農特產最豐富的地方，看到一定要停。</li>
                    </ul>
                </div>
            </div>
        </div>

    </main>

    <!-- Navigation -->
    <nav class="fixed bottom-0 left-0 right-0 glass-nav h-20 flex justify-around items-center px-6 z-50">
        <button onclick="switchTab('itinerary')" class="flex flex-col items-center space-y-1">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg>
            <span class="text-[9px]">行程</span>
        </button>
        <button onclick="switchTab('transport')" class="flex flex-col items-center space-y-1">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg>
            <span class="text-[9px]">宿/交</span>
        </button>
        <button onclick="switchTab('finance')" class="flex flex-col items-center space-y-1">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span class="text-[9px]">記帳</span>
        </button>
        <button onclick="switchTab('sos')" class="flex flex-col items-center space-y-1">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
            <span class="text-[9px]">救急</span>
        </button>
    </nav>

    <script>
        function switchTab(tabId) {
            document.querySelectorAll('.tab-content').forEach(c => c.classList.add('hidden'));
            document.getElementById('content-' + tabId).classList.remove('hidden');
            
            document.querySelectorAll('.nav-tab').forEach(t => t.classList.remove('active'));
            document.getElementById('tab-' + tabId).classList.add('active');
            
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function openMap(query) {
            const url = `https://www.google.com/maps/search/?api=1&query=${encodeURIComponent(query)}`;
            window.open(url, '_blank');
        }

        function addExp() {
            const amt = prompt("請輸入金額 (¥):");
            if (amt) {
                const note = prompt("項目名稱:");
                const container = document.getElementById('expense-items');
                const div = document.createElement('div');
                div.className = "flex justify-between text-sm p-2 bg-white rounded border border-stone-100 animate-slide-in";
                div.innerHTML = `<span>${note || '無標題'}</span><span class="font-mono font-bold">¥ ${amt}</span>`;
                container.prepend(div);
            }
        }
    </script>
</body>
</html>
