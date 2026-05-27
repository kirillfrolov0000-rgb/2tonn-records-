<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>2TONN Records | Тяжелый саунд</title>
    <meta name="description" content="Независимый лейбл 2TONN Records. Выпускаем честную музыку. Сделано артистами для артистов.">
    <!-- Предзагрузка шрифта для скорости -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <!-- Font Awesome 6 (бесплатные иконки) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #000000;
            color: #e5e5e5;
            font-family: 'Inter', sans-serif;
            line-height: 1.5;
            scroll-behavior: smooth;
        }

        /* Грубая текстура для фона (намёк на вес) */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI4MCIgaGVpZ2h0PSI4MCIgdmlld0JveD0iMCAwIDQwIDQwIj48cGF0aCBmaWxsPSIjMjIyIiBmaWxsLW9wYWNpdHk9IjAuMTUiIGQ9Ik0wIDBoMXYxSDB6bTIgMGgxdjFIMnptMiAwaDF2MUg0em0yIDBoMXYxSDZ6bTIgMGgxdjFIOHptMiAwaDF2MUgxMHptMiAwaDF2MUgxMnptMiAwaDF2MUgxNHptMiAwaDF2MUgxNnptMiAwaDF2MUgxOHoiLz48L3N2Zz4=');
            background-repeat: repeat;
            opacity: 0.4;
            pointer-events: none;
            z-index: 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
            position: relative;
            z-index: 1;
        }

        /* Header */
        .header {
            padding: 32px 0 24px;
            border-bottom: 1px solid rgba(255,255,255,0.08);
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            flex-wrap: wrap;
            gap: 16px;
        }

        .logo h1 {
            font-size: 28px;
            font-weight: 700;
            letter-spacing: -0.5px;
            background: linear-gradient(135deg, #FFFFFF 0%, #9C9C9C 100%);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .logo p {
            font-size: 12px;
            color: #777;
            letter-spacing: 1px;
        }

        .cta-header a {
            color: #fff;
            background: #1f1f1f;
            padding: 8px 20px;
            border-radius: 40px;
            text-decoration: none;
            font-weight: 500;
            font-size: 14px;
            transition: 0.2s;
            border: 1px solid #333;
        }

        .cta-header a:hover {
            background: #2c2c2c;
            border-color: #555;
        }

        /* Hero */
        .hero {
            padding: 100px 0 80px;
            text-align: center;
        }

        .badge {
            display: inline-block;
            background: #111;
            padding: 6px 16px;
            border-radius: 60px;
            font-size: 13px;
            font-weight: 500;
            color: #bbb;
            margin-bottom: 24px;
            border: 1px solid #222;
        }

        .hero h2 {
            font-size: 48px;
            font-weight: 700;
            line-height: 1.2;
            letter-spacing: -1px;
            max-width: 800px;
            margin: 0 auto 24px;
        }

        .hero h2 span {
            background: linear-gradient(120deg, #FFFFFF, #a0a0a0);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }

        .hero p {
            font-size: 18px;
            color: #9a9a9a;
            max-width: 600px;
            margin: 0 auto 40px;
        }

        .btn-group {
            display: flex;
            gap: 16px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn-primary {
            background: #fff;
            color: #000;
            padding: 14px 32px;
            border-radius: 40px;
            text-decoration: none;
            font-weight: 600;
            transition: 0.2s;
            border: none;
            cursor: pointer;
        }

        .btn-primary:hover {
            background: #ddd;
            transform: scale(0.98);
        }

        .btn-outline {
            border: 1px solid #333;
            background: transparent;
            color: #fff;
            padding: 14px 32px;
            border-radius: 40px;
            text-decoration: none;
            font-weight: 500;
            transition: 0.2s;
        }

        .btn-outline:hover {
            border-color: #777;
            background: #111;
        }

        /* разделы общие */
        .section {
            padding: 80px 0;
            border-bottom: 1px solid rgba(255,255,255,0.05);
        }

        .section-title {
            font-size: 32px;
            font-weight: 700;
            margin-bottom: 48px;
            letter-spacing: -0.3px;
        }

        .section-sub {
            color: #aaa;
            font-weight: 400;
            font-size: 16px;
            margin-top: 8px;
        }

        /* Карточки условий */
        .cards {
            display: flex;
            gap: 30px;
            flex-wrap: wrap;
            justify-content: space-between;
        }

        .card {
            background: #0b0b0b;
            border: 1px solid #1f1f1f;
            border-radius: 28px;
            padding: 32px 24px;
            flex: 1;
            min-width: 250px;
            transition: 0.2s;
        }

        .card:hover {
            border-color: #353535;
            background: #0e0e0e;
        }

        .card i {
            font-size: 32px;
            color: #ccc;
            margin-bottom: 20px;
        }

        .card h3 {
            font-size: 22px;
            margin-bottom: 12px;
        }

        .price {
            font-size: 28px;
            font-weight: 700;
            margin: 20px 0 12px;
        }

        .small-price {
            font-size: 14px;
            color: #777;
        }

        .card ul {
            list-style: none;
            margin: 20px 0;
        }

        .card li {
            margin: 12px 0;
            font-size: 14px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .card li i {
            font-size: 14px;
            color: #aaa;
            margin: 0;
        }

        .divider {
            height: 1px;
            background: #1c1c1c;
            margin: 20px 0;
        }

        /* Лейбл факты */
        .facts-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 24px;
        }

        .fact {
            background: #080808;
            padding: 24px;
            border-radius: 20px;
            border: 1px solid #181818;
        }

        .fact-number {
            font-size: 42px;
            font-weight: 800;
            color: white;
        }

        /* форма демки */
        .demo-box {
            background: #0a0a0a;
            border-radius: 32px;
            padding: 48px 40px;
            border: 1px solid #222;
            text-align: center;
        }

        .demo-input-group {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            justify-content: center;
            margin: 32px 0 16px;
        }

        .demo-input-group input {
            background: #121212;
            border: 1px solid #2c2c2c;
            border-radius: 60px;
            padding: 14px 24px;
            width: 280px;
            color: white;
            font-family: inherit;
            outline: none;
        }

        .demo-input-group input:focus {
            border-color: #666;
        }

        .small-note {
            font-size: 12px;
            color: #5a5a5a;
        }

        footer {
            padding: 48px 0;
            text-align: center;
            color: #5a5a5a;
            font-size: 13px;
        }

        @media (max-width: 680px) {
            .hero h2 { font-size: 32px; }
            .section-title { font-size: 26px; }
            .demo-box { padding: 32px 20px; }
        }
    </style>
</head>
<body>

<div class="container">
    <!-- Шапка -->
    <div class="header">
        <div class="logo">
            <h1>2TONN RECORDS</h1>
            <p>тяжелый саунд / честные релизы</p>
        </div>
        <div class="cta-header">
            <a href="#demo">отправить демо</a>
        </div>
    </div>

    <!-- Герой -->
    <div class="hero">
        <div class="badge">сделано артистами для артистов</div>
        <h2>Не жди, пока заметят.<br>Выпускай <span>с нами</span>.</h2>
        <p>2TONN Records — молодой лейбл, который мы основали вдвоем. Один из нас сам артист. Мы не обещаем золотые горы, но выпустим твою музыку честно.</p>
        <div class="btn-group">
            <a href="#conditions" class="btn-outline">как работаем</a>
            <a href="#demo" class="btn-primary">прислать трек</a>
        </div>
    </div>

    <!-- История лейбла коротко -->
    <div class="section">
        <div class="facts-grid">
            <div class="fact">
                <div class="fact-number">2</div>
                <div style="font-weight:600; margin: 8px 0;">основателя</div>
                <div style="font-size:14px; color:#888;">Я — артист, и мой друг. Оба слушаем демки лично.</div>
            </div>
            <div class="fact">
                <div class="fact-number">0</div>
                <div style="font-weight:600; margin: 8px 0;">₽ за прослушивание</div>
                <div style="font-size:14px; color:#888;">Никакой платной проверки демо. Никогда.</div>
            </div>
            <div class="fact">
                <div class="fact-number">20-40%</div>
                <div style="font-weight:600; margin: 8px 0;">роялти лейблу</div>
                <div style="font-size:14px; color:#888;">Только после вычета комиссий площадок.</div>
            </div>
            <div class="fact">
                <div class="fact-number">24/7</div>
                <div style="font-weight:600; margin: 8px 0;">человеческий подход</div>
                <div style="font-size:14px; color:#888;">Отвечаем быстро, не пропадаем.</div>
            </div>
        </div>
    </div>

    <!-- Условия сотрудничества ( два варианта ) -->
    <div class="section" id="conditions">
        <div class="section-title">⚡️ как мы работаем</div>
        <div class="cards">
            <!-- Партнерство -->
            <div class="card">
                <i class="fas fa-handshake"></i>
                <h3>Партнерство</h3>
                <div class="price">20–40%</div>
                <div class="small-price">лейблу с дохода</div>
                <div class="divider"></div>
                <ul>
                    <li><i class="fas fa-pen-fancy"></i> Мы вносим правки в трек</li>
                    <li><i class="fas fa-gavel"></i> Финальное решение за лейблом</li>
                    <li><i class="fas fa-chart-line"></i> Релиз на всех площадках</li>
                    <li><i class="fas fa-user-check"></i> Личный пиар и помощь</li>
                </ul>
                <div class="small-note">*процент обсуждается индивидуально (выше 30% — при активном вложении)</div>
            </div>
            <!-- Платная дистрибуция -->
            <div class="card">
                <i class="fas fa-cloud-upload-alt"></i>
                <h3>Дистрибуция</h3>
                <div class="price">500 ₽</div>
                <div class="small-price">за трек</div>
                <div class="divider"></div>
                <ul>
                    <li><i class="fas fa-check-circle"></i> Размещение на стримингах (VK, Apple, Spotify)</li>
                    <li><i class="fas fa-times-circle"></i> Без правок / без % лейблу</li>
                    <li><i class="fas fa-chart-simple"></i> 100% роялти ваши</li>
                    <li><i class="fas fa-fast-forward"></i> Быстрый релиз без головной боли</li>
                </ul>
                <div class="small-note">*вы платите только за размещение</div>
            </div>
        </div>
    </div>

    <!-- Почему выбирают нас (мягкий оффер) -->
    <div class="section">
        <div class="section-title">почему артисты уже с нами</div>
        <div class="cards" style="gap:20px;">
            <div class="card" style="background:#080808;">
                <i class="fas fa-microphone-alt"></i>
                <h3>Мы сами начинали с нуля</h3>
                <p style="font-size: 14px; color:#bbb;">Артист с демками на телефоне — это мы недавно. Поэтому знаем, как это — быть незамеченным.</p>
            </div>
            <div class="card" style="background:#080808;">
                <i class="fas fa-clock"></i>
                <h3>Никаких «ответим через месяц»</h3>
                <p style="font-size: 14px; color:#bbb;">Ответ в течение 3-5 дней. Даже если это отказ с фидбеком.</p>
            </div>
            <div class="card" style="background:#080808;">
                <i class="fas fa-charging-station"></i>
                <h3>Творческая свобода</h3>
                <p style="font-size: 14px; color:#bbb;">Мы не лезем в твой стиль. Только помогаем звучать лучше.</p>
            </div>
        </div>
    </div>

    <!-- форма отправки демки (имитация, но с активной кнопкой) -->
    <div class="section" id="demo">
        <div class="demo-box">
            <i class="fas fa-head-side-headphones" style="font-size: 40px; opacity: 0.7; margin-bottom: 20px; display: inline-block;"></i>
            <h3 style="font-size: 28px; margin-bottom: 12px;">пришли демку</h3>
            <p style="margin-bottom: 16px; color: #aaa;">просто вставь ссылку на трек (VK / SoundCloud / telegram)</p>
            <div class="demo-input-group">
                <input type="text" id="demoLink" placeholder="ссылка на трек или голосовое сообщение">
                <a href="#" class="btn-primary" style="display: inline-block;" id="submitDemoBtn">отправить</a>
            </div>
            <div class="small-note" id="demoMessage" style="margin-top: 8px;"></div>
            <div class="small-note">*Мы не берем плату за прослушивание. Если трек зайдет — ответим и предложим договор.</div>
        </div>
    </div>

    <!-- контакты -->
    <footer>
        <p><strong>2TONN Records</strong> — ваш независимый саунд</p>
        <p style="margin-top: 12px;">
            <i class="fab fa-telegram"></i> <strong> Telegram: </strong> 
            <a href="#" style="color:#aaa; text-decoration: none;">@[ВАШ_TELEGRAM_НИК]</a>&nbsp;&nbsp;|&nbsp;&nbsp;
            <i class="fab fa-vk"></i> <strong> VK: </strong> 
            <a href="#" style="color:#aaa; text-decoration: none;">[ССЫЛКА_VK]</a>
        </p>
        <p style="margin-top: 20px;">© 2026 — всё по честному. Тяжело только в начале.</p>
    </footer>
</div>

<!-- Простой скрипт для имитации отправки демки -->
<script>
    const submitBtn = document.getElementById('submitDemoBtn');
    const demoInput = document.getElementById('demoLink');
    const messageSpan = document.getElementById('demoMessage');

    submitBtn.addEventListener('click', (e) => {
        e.preventDefault();
        let link = demoInput.value.trim();
        if (link === "") {
            messageSpan.innerHTML = "❌ вставь ссылку на трек (даже raw voice)";
            messageSpan.style.color = "#d47b7b";
            return;
        }
        if (!link.startsWith("http")) {
            messageSpan.innerHTML = "✏️ похоже на ссылку? вставь адрес (vk.com/... или телеграм)";
            messageSpan.style.color = "#d47b7b";
            return;
        }
        // Имитируем отправку (реальный функционал можно добавить через телеграм бота или форму)
        messageSpan.innerHTML = "✅ демо улетело! Мы слушаем. ответим в телеграм/вк в течение 3-5 дней";
        messageSpan.style.color = "#7eaa7e";
        demoInput.value = "";
        // Здесь в будущем можно подключить отправку на ваш API, либо просто создать mailto: 
        // Пока пользователь сам пишет — но мы даём понять, что лейбл активен.
        setTimeout(() => {
            messageSpan.innerHTML = "";
        }, 5000);
        // опционально — открыть ваш мессенджер:
        // window.open('https://t.me/ВАШ_НИК', '_blank');
    });
</script>

<!-- инструкция: заменить в footer [ВАШ_TELEGRAM_НИК] и [ССЫЛКА_VK] на реальные -->
</body>
</html>