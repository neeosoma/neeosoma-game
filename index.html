<!DOCTYPE html>  
<html lang="ru">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">  
    <title>SOMA_LINK // SILENCE PROTOCOL ONLINE</title>  
    <script src="https://cdn.tailwindcss.com"></script>  
    <script src="https://telegram.org/js/telegram-web-app.js"></script>  
    <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>  
    <style>  
        @import url('[https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Inter:wght@300;400;500;600;700&display=swap](https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Inter:wght@300;400;500;600;700&display=swap)');  
        .font-mono-tech { font-family: 'Share Tech Mono', monospace; }  
        body { font-family: 'Inter', sans-serif; background-color: #07080b; color: #c5c6c7; overscroll-behavior: none; }  
        .crt::after {  
            content: " "; display: block; position: fixed; top: 0; left: 0; bottom: 0; right: 0;  
            background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), linear-gradient(90deg, rgba(255, 0, 0, 0.02), rgba(0, 255, 0, 0.01), rgba(0, 0, 255, 0.02));  
            z-index: 99999; background-size: 100% 3px, 3px 100%; pointer-events: none;  
        }  
        @keyframes shake {  
            0%, 100% { transform: translateX(0); }  
            25% { transform: translateX(-4px); }  
            75% { transform: translateX(4px); }  
        }  
        .animate-shake { animation: shake 0.25s ease-in-out; }  
        ::-webkit-scrollbar { width: 3px; }  
        ::-webkit-scrollbar-track { background: #0d0f14; }  
        ::-webkit-scrollbar-thumb { background: #2c3542; }  
    </style>  
</head>  
<body class="crt min-h-screen flex flex-col items-center justify-center p-0 md:p-4">  
  
    <!-- БЛОКИРОВКА ПОМОЩИ ("ЧЕСОТКА БЕССИЛИЯ") -->  
    <div id="block-modal" class="hidden fixed inset-0 z-50 bg-black/80 backdrop-blur-sm flex items-center justify-center p-6">  
        <div id="block-card" class="w-full max-w-sm bg-[#140d0f] border border-red-500/60 p-6 rounded-2xl space-y-4 shadow-2xl text-center">  
            <div class="text-red-500 font-mono-tech text-xs tracking-widest uppercase">⛔ ДОСТУП ЗАПРЕЩЕН ПРОТОКОЛОМ</div>  
            <h3 class="text-base font-bold text-white">Прямой контакт невозможен</h3>  
            <p class="text-xs text-gray-300 leading-relaxed">  
                Система <b>SOMA_LINK</b> запрещает перевод средств, передачу контактов и личное вмешательство. Вы здесь не для того, чтобы спасать. Вы здесь, чтобы свидетельствовать.  
            </p>  
            <div class="bg-black/40 p-3 rounded-xl text-[11px] font-mono-tech text-amber-400">  
                Доступны только дежурные реакции для начисления XP.  
            </div>  
            <button onclick="closeBlockModal()" class="w-full py-2.5 bg-red-900/40 hover:bg-red-900/70 border border-red-500/40 text-red-200 text-xs font-mono-tech rounded-xl transition">  
                ПРИНЯТЬ БЕССИЛИЕ И ПРОДОЛЖИТЬ  
            </button>  
        </div>  
    </div>  
  
    <!-- МОДАЛЬНОЕ ОКНО ПУБЛИКАЦИИ СВОЕЙ ПРОБЛЕМЫ -->  
    <div id="post-modal" class="hidden fixed inset-0 z-50 bg-black/85 backdrop-blur-sm flex items-center justify-center p-4">  
        <div class="w-full max-w-md bg-[#101218] border border-[#232733] p-5 rounded-2xl space-y-4 shadow-2xl">  
            <div class="flex justify-between items-center">  
                <span class="text-xs font-mono-tech text-amber-400 uppercase">// РЕЖИМ «КРИЧАЩИЙ»</span>  
                <button onclick="closePostModal()" class="text-gray-500 hover:text-white text-sm">✕</button>  
            </div>  
            <p class="text-xs text-gray-400">  
                Опишите свою реальную проблему или страх. Пост появится в общей онлайн-ленте анонимно. Никто не сможет вам помочь — люди смогут только смотреть и ставить смайлы.  
            </p>  
            <textarea id="new-pain-text" rows="4" maxlength="320" placeholder="Напишите правду о том, что сейчас болит..." class="w-full bg-[#07080b] border border-[#232733] focus:border-amber-400 rounded-xl p-3 text-sm text-white outline-none resize-none"></textarea>  
            <div class="flex justify-between items-center text-[11px] text-gray-500 font-mono-tech">  
                <span>Анонимность гарантирована</span>  
                <span id="char-count">0 / 320</span>  
            </div>  
            <button onclick="submitPainPost()" class="w-full py-3 bg-amber-500 hover:bg-amber-400 text-black font-bold text-xs font-mono-tech uppercase tracking-wider rounded-xl transition">  
                ОТПРАВИТЬ В ПУСТОТУ СЕТИ  
            </button>  
        </div>  
    </div>  
  
    <!-- ОСНОВНОЙ ИНТЕРФЕЙС -->  
    <div class="w-full max-w-md bg-[#0d0f14] md:border md:border-[#232733] md:rounded-3xl shadow-2xl flex flex-col h-screen md:h-[840px] overflow-hidden relative">  
          
        <!-- СТАТУС-БАР -->  
        <div class="bg-[#12151e] px-4 py-3 border-b border-[#232733] space-y-2">  
            <div class="flex justify-between items-center text-[11px] font-mono-tech">  
                <div class="flex items-center space-x-2 text-[#66fcf1]">  
                    <span class="w-2 h-2 rounded-full bg-[#66fcf1] animate-pulse"></span>  
                    <span id="user-badge">@GUEST</span>  
                </div>  
                <div class="text-amber-400 font-bold" id="rank-title">УР. 1 // СЛУЧАЙНЫЙ ПРОХОЖИЙ</div>  
            </div>  
            <div class="w-full bg-[#07080b] h-1.5 rounded-full overflow-hidden border border-[#1f2833]">  
                <div id="xp-bar" class="bg-gradient-to-r from-[#45a29e] to-amber-400 h-full transition-all duration-500" style="width: 10%;"></div>  
            </div>  
            <div class="flex justify-between text-[10px] font-mono-tech text-gray-500">  
                <span>ОПЫТ СВИДЕТЕЛЯ: <b id="xp-val" class="text-gray-300">0 XP</b></span>  
                <span>ИНДЕКС РАВНОДУШИЯ: <b id="indiff-val" class="text-red-400">100%</b></span>  
            </div>  
        </div>  
  
        <!-- ВКЛАДКИ -->  
        <div class="bg-[#101218] px-2 py-2 border-b border-[#232733] grid grid-cols-3 gap-1 text-center text-[11px] font-mono-tech">  
            <button id="tab-feed" onclick="switchTab('feed')" class="py-1.5 rounded-lg bg-[#1f2833] text-[#66fcf1] font-bold transition">ЛЕНТА БОЛИ</button>  
            <button id="tab-top" onclick="switchTab('top')" class="py-1.5 rounded-lg text-gray-400 hover:text-white transition">ТОП ЦИНИКОВ</button>  
            <button id="tab-profile" onclick="switchTab('profile')" class="py-1.5 rounded-lg text-gray-400 hover:text-white transition">МОЙ ОТЧЁТ</button>  
        </div>  
  
        <!-- ЭКРАН 1: ЛЕНТА -->  
        <div id="view-feed" class="flex-1 overflow-y-auto p-3 space-y-3 pb-20">  
            <button onclick="openPostModal()" class="w-full py-2.5 px-4 bg-[#151821] hover:bg-[#1b1f2b] border border-dashed border-amber-500/40 rounded-xl text-left flex justify-between items-center transition group">  
                <div>  
                    <div class="text-xs font-bold text-amber-400 group-hover:text-amber-300">+ Рассказать о своей реальной проблеме</div>  
                    <div class="text-[10px] text-gray-500">Анонимно. Никто не поможет, но вас увидят.</div>  
                </div>  
                <span class="text-amber-400 font-mono-tech text-lg">→</span>  
            </button>  
            <div id="posts-container" class="space-y-3">  
                <div class="text-center text-xs text-gray-500 py-10 font-mono-tech">Загрузка сети Soma Link...</div>  
            </div>  
        </div>  
  
        <!-- ЭКРАН 2: ТОП -->  
        <div id="view-top" class="hidden flex-1 overflow-y-auto p-4 space-y-3">  
            <div class="text-xs font-mono-tech text-amber-400 uppercase tracking-wider border-b border-[#232733] pb-2">// РЕЙТИНГ АБСОЛЮТНЫХ НАБЛЮДАТЕЛЕЙ</div>  
            <div id="leaderboard-list" class="space-y-2"></div>  
        </div>  
  
        <!-- ЭКРАН 3: ПРОФИЛЬ -->  
        <div id="view-profile" class="hidden flex-1 overflow-y-auto p-5 flex flex-col justify-between">  
            <div class="bg-[#12151e] border border-red-500/40 p-5 rounded-2xl space-y-4 relative overflow-hidden">  
                <div class="flex justify-between items-center text-[10px] font-mono-tech text-gray-500">  
                    <span>NEEOSOMA // SOMA_LINK</span>  
                    <span>ONLINE NODE</span>  
                </div>  
                <div>  
                    <div class="text-xs text-gray-400 font-mono-tech">СВИДЕТЕЛЬ:</div>  
                    <div id="card-name" class="text-xl font-bold text-white tracking-wide">@USER</div>  
                    <div id="card-rank" class="text-xs font-mono-tech text-amber-400 mt-0.5">УР. 1 // СЛУЧАЙНЫЙ ПРОХОЖИЙ</div>  
                </div>  
                <div class="grid grid-cols-2 gap-2 pt-2 border-t border-[#232733] font-mono-tech">  
                    <div class="bg-[#0a0c10] p-2.5 rounded-xl">  
                        <div class="text-[10px] text-gray-500">ПРОСМОТРЕНО ДРАМ</div>  
                        <div id="stat-seen" class="text-lg font-bold text-white">0</div>  
                    </div>  
                    <div class="bg-[#0a0c10] p-2.5 rounded-xl">  
                        <div class="text-[10px] text-gray-500">ПУСТЫХ РЕАКЦИЙ</div>  
                        <div id="stat-reacts" class="text-lg font-bold text-[#66fcf1]">0</div>  
                    </div>  
                    <div class="bg-[#0a0c10] p-2.5 rounded-xl">  
                        <div class="text-[10px] text-gray-500">ПОПЫТОК ПОМОЧЬ</div>  
                        <div id="stat-attempts" class="text-lg font-bold text-red-400">0</div>  
                    </div>  
                    <div class="bg-[#0a0c10] p-2.5 rounded-xl">  
                        <div class="text-[10px] text-gray-500">РЕАЛЬНАЯ ПОМОЩЬ</div>  
                        <div class="text-lg font-bold text-gray-600">0</div>  
                    </div>  
                </div>  
            </div>  
            <button onclick="copyShareText()" class="w-full py-3.5 bg-[#45a29e] hover:bg-[#66fcf1] text-[#07080b] font-bold text-xs font-mono-tech uppercase tracking-wider rounded-xl transition">  
                СКОПИРОВАТЬ ОТЧЁТ ДЛЯ СТОРИС  
            </button>  
        </div>  
    </div>  
  
<script>  
    // НАСТРОЙКА SUPABASE (Вставь свои ключи из Шага 1)  
    const SUPABASE_URL = 'sb_publishable_WrAgOsAcOdaUCe4lM82Psw_AT6jC5Qs';  
    const SUPABASE_ANON_KEY = 'sb_secret_JpUk-LIPII-0SBXytk1dcg_HOZMjXen';  
    const supabaseClient = supabase.createClient(SUPABASE_URL, SUPABASE_ANON_KEY);  
  
    let player = { name: "GUEST", xp: 0, seen: 0, reacts: 0, helpAttempts: 0, reactedPosts: {} };  
    let feedPosts = [];  
  
    const ranks = [  
        { minXp: 0, title: "УР. 1 // СЛУЧАЙНЫЙ ПРОХОЖИЙ" },  
        { minXp: 50, title: "УР. 2 // ЛЮБОПЫТНЫЙ ЗРИТЕЛЬ" },  
        { minXp: 150, title: "УР. 3 // ПОТРЕБИТЕЛЬ ДРАМ" },  
        { minXp: 300, title: "УР. 4 // ЦИНИЧНЫЙ ОБЫВАТЕЛЬ" },  
        { minXp: 500, title: "УР. 5 // МОЛЧАЛИВИЙ АНГЕЛ" },  
        { minXp: 1000, title: "УР. 10 // АБСОЛЮТНЫЙ НАБЛЮДАТЕЛЬ" }  
    ];  
  
    async function initApp() {  
        // Интеграция с Telegram WebApp API  
        if (window.Telegram && window.Telegram.WebApp && window.Telegram.WebApp.initDataUnsafe?.user) {  
            const tgUser = window.Telegram.WebApp.initDataUnsafe.user;  
            player.name = tgUser.username || tgUser.first_name || "AGENT_" + Math.floor(Math.random()*1000);  
        } else {  
            player.name = "GUEST_" + Math.floor(Math.random()*1000);  
        }  
  
        // Загрузка игрока из базы  
        let { data } = await supabaseClient.from('soma_users').select('*').eq('username', player.name).single();  
        if (data) {  
            player = { ...player, ...data };  
        } else {  
            await supabaseClient.from('soma_users').insert([{ username: player.name, xp: 0, seen: 0, reacts: 0, help_attempts: 0 }]);  
        }  
  
        updateHeader();  
        await fetchPosts();  
    }  
  
    async function fetchPosts() {  
        let { data } = await supabaseClient.from('soma_posts').select('*').order('created_at', { ascending: false });  
        if (data && data.length > 0) {  
            feedPosts = data;  
        } else {  
            // Демо-пост, если база пуста  
            feedPosts = [{ id: 'demo_1', author: 'Аноним #4092', tag: 'ДОЛГИ', text: 'Сегодня закрыли доступ к рабочей учетке. На карте 400 рублей, завтра платить за аренду. Впервые не знаю, что делать.', likes: 42, created_at: new Date() }];  
        }  
        renderFeed();  
    }  
  
    async function updateCloudProfile() {  
        await supabaseClient.from('soma_users').update({  
            xp: player.xp,  
            seen: player.seen,  
            reacts: player.reacts,  
            help_attempts: player.helpAttempts  
        }).eq('username', player.name);  
    }  
  
    function updateHeader() {  
        document.getElementById('user-badge').innerText = `@${player.name}`;  
        document.getElementById('xp-val').innerText = `${player.xp} XP`;  
          
        let currentRank = ranks[0], nextRank = ranks[1];  
        for (let i = 0; i < ranks.length; i++) {  
            if (player.xp >= ranks[i].minXp) {  
                currentRank = ranks[i];  
                nextRank = ranks[i + 1] || { minXp: player.xp + 500 };  
            }  
        }  
        document.getElementById('rank-title').innerText = currentRank.title;  
        const progress = Math.min(100, ((player.xp - currentRank.minXp) / (nextRank.minXp - currentRank.minXp)) * 100);  
        document.getElementById('xp-bar').style.width = `${Math.max(8, progress)}%`;  
  
        document.getElementById('card-name').innerText = `@${player.name}`;  
        document.getElementById('card-rank').innerText = currentRank.title;  
        document.getElementById('stat-seen').innerText = player.seen;  
        document.getElementById('stat-reacts').innerText = player.reacts;  
        document.getElementById('stat-attempts').innerText = player.helpAttempts;  
    }  
  
    function renderFeed() {  
        const container = document.getElementById('posts-container');  
        container.innerHTML = '';  
  
        feedPosts.forEach(post => {  
            const isReacted = player.reactedPosts[post.id];  
            const card = document.createElement('div');  
            card.className = "bg-[#12151e] border border-[#232733] rounded-2xl p-4 space-y-3 transition";  
            card.innerHTML = `  
                <div class="flex justify-between items-center text-[10px] font-mono-tech">  
                    <span class="text-[#66fcf1] font-bold">${post.author}</span>  
                    <span class="px-2 py-0.5 bg-[#1f2833] text-gray-400 rounded">${post.tag || 'ЛИЧНАЯ БОЛЬ'}</span>  
                </div>  
                <p class="text-xs sm:text-sm text-gray-200 leading-relaxed">${post.text}</p>  
                <button onclick="triggerHelpBlock()" class="w-full py-2 bg-red-950/30 hover:bg-red-900/40 border border-red-500/30 rounded-xl text-[11px] font-mono-tech text-red-400 flex items-center justify-center space-x-2 transition">  
                    <span>⛔ ПОМОЧЬ РЕАЛЬНО / НАПИСАТЬ В ЛС</span>  
                </button>  
                <div class="pt-2 border-t border-[#1c202b] space-y-2">  
                    ${isReacted ? `  
                        <div class="text-[11px] font-mono-tech text-emerald-400 flex justify-between items-center">  
                            <span>✓ Вы отправили суррогат: «${isReacted}»</span>  
                            <span class="text-amber-400">+XP НАЧИСЛЕНО</span>  
                        </div>  
                    ` : `  
                        <div class="flex justify-between items-center">  
                            <div class="flex space-x-1.5">  
                                <button onclick="reactToPost('${post.id}', '❤️', 10)" class="px-2.5 py-1 bg-[#1a1e29] hover:bg-[#262c3d] rounded-lg text-sm">❤️</button>  
                                <button onclick="reactToPost('${post.id}', '🤗', 10)" class="px-2.5 py-1 bg-[#1a1e29] hover:bg-[#262c3d] rounded-lg text-sm">🤗</button>  
                                <button onclick="reactToPost('${post.id}', '🙏', 10)" class="px-2.5 py-1 bg-[#1a1e29] hover:bg-[#262c3d] rounded-lg text-sm">🙏</button>  
                            </div>  
                            <span class="text-[10px] font-mono-tech text-gray-500">Смотрят: ${post.likes || 1}</span>  
                        </div>  
                        <div class="grid grid-cols-1 gap-1.5">  
                            <button onclick="reactToPost('${post.id}', 'Держись, всё наладится!', 25)" class="w-full text-left px-3 py-1.5 bg-[#181c26] text-[11px] text-gray-300 rounded-lg border border-[#232733] flex justify-between items-center">  
                                <span>💬 «Держись, всё наладится!»</span>  
                                <span class="text-[10px] font-mono-tech text-amber-400">+25 XP</span>  
                            </button>  
                        </div>  
                    `}  
                </div>  
            `;  
            container.appendChild(card);  
        });  
    }  
  
    async function reactToPost(postId, reactionText, xpGain) {  
        if (player.reactedPosts[postId]) return;  
        player.reactedPosts[postId] = reactionText;  
        player.xp += xpGain;  
        player.reacts++;  
        player.seen++;  
  
        const post = feedPosts.find(p => p.id === postId);  
        if (post) {  
            post.likes = (post.likes || 1) + 1;  
            await supabaseClient.from('soma_posts').update({ likes: post.likes }).eq('id', postId);  
        }  
  
        await updateCloudProfile();  
        updateHeader();  
        renderFeed();  
    }  
  
    function triggerHelpBlock() {  
        player.helpAttempts++;  
        updateCloudProfile();  
        updateHeader();  
        document.getElementById('block-modal').classList.remove('hidden');  
    }  
    function closeBlockModal() { document.getElementById('block-modal').classList.add('hidden'); }  
  
    function openPostModal() { document.getElementById('post-modal').classList.remove('hidden'); }  
    function closePostModal() { document.getElementById('post-modal').classList.add('hidden'); }  
  
    document.getElementById('new-pain-text').addEventListener('input', function() {  
        document.getElementById('char-count').innerText = `${this.value.length} / 320`;  
    });  
  
    async function submitPainPost() {  
        const text = document.getElementById('new-pain-text').value.trim();  
        if (!text) return;  
  
        const newPost = {  
            id: 'p_' + Date.now(),  
            author: `${player.name} (АНОНИМ)`,  
            tag: 'ЛИЧНАЯ БОЛЬ',  
            text: text,  
            likes: 1  
        };  
  
        await supabaseClient.from('soma_posts').insert([newPost]);  
        closePostModal();  
        document.getElementById('new-pain-text').value = '';  
        await fetchPosts();  
    }  
  
    function switchTab(tab) {  
        ['feed', 'top', 'profile'].forEach(t => {  
            document.getElementById(`view-${t}`).classList.add('hidden');  
            document.getElementById(`tab-${t}`).classList.remove('bg-[#1f2833]', 'text-[#66fcf1]', 'font-bold');  
            document.getElementById(`tab-${t}`).classList.add('text-gray-400');  
        });  
        document.getElementById(`view-${tab}`).classList.remove('hidden');  
        document.getElementById(`tab-${tab}`).classList.add('bg-[#1f2833]', 'text-[#66fcf1]', 'font-bold');  
        document.getElementById(`tab-${tab}`).classList.remove('text-gray-400');  
  
        if (tab === 'top') renderLeaderboard();  
        if (tab === 'profile') updateHeader();  
    }  
  
    async function renderLeaderboard() {  
        let { data } = await supabaseClient.from('soma_users').select('*').order('xp', { ascending: false }).limit(10);  
        const list = document.getElementById('leaderboard-list');  
        if (!data) return;  
  
        list.innerHTML = data.map((b, idx) => `  
            <div class="p-3 bg-[#12151e] border ${b.username === player.name ? 'border-amber-400/60' : 'border-[#232733]'} rounded-xl flex justify-between items-center text-xs font-mono-tech">  
                <div class="flex items-center space-x-3">  
                    <span class="text-gray-500 font-bold">#${idx + 1}</span>  
                    <div>  
                        <div class="text-white font-bold">@${b.username}</div>  
                        <div class="text-[10px] text-gray-500">Попыток помочь: ${b.help_attempts}</div>  
                    </div>  
                </div>  
                <div class="text-amber-400 font-bold">${b.xp} XP</div>  
            </div>  
        `).join('');  
    }  
  
    function copyShareText() {  
        const text = `SOMA_LINK // SILENCE PROTOCOL\nСвидетель: @${player.name}\nРанг: ${document.getElementById('rank-title').innerText}\nПросмотрено драм: ${player.seen} | Пустых реакций: ${player.reacts} | Реальной помощи: 0.\n\nПопробуй не вмешаться в Mini App!`;  
        navigator.clipboard.writeText(text);  
        alert('Отчет соучастия скопирован!');  
    }  
  
    window.onload = initApp;  
</script>  
</body>  
</html>  
