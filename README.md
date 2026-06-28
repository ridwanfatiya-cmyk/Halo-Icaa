
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semangat UAS Ica!</title>
    <style>
        /* --- TEMA WARNA UNGU & BACKGROUND --- */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #2e1065, #3b0764, #581c87);
            color: #f5f3ff;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .container {
            max-width: 800px;
            width: 100%;
            text-align: center;
            margin-top: 40px;
        }

        /* --- STYLING GAMBAR MEME (BARU) --- */
        .meme-container {
            margin-bottom: 20px; /* Jarak antara meme dan judul */
        }

        .meme-img {
            max-width: 100%; /* Agar gambar tidak meluber di HP */
            height: auto; /* Jaga rasio gambar */
            max-height: 300px; /* Batas tinggi maksimal di desktop */
            border-radius: 15px; /* Sudut melengkung */
            box-shadow: 0 5px 15px rgba(0,0,0,0.3); /* Bayangan */
            border: 3px solid #a855f7; /* Bingkai ungu */
        }

        h1 {
            font-size: 3rem;
            color: #ddd6fe;
            text-shadow: 0 0 15px rgba(167, 139, 250, 0.7);
            margin-top: 0; /* Sesuaikan margin atas karena ada gambar */
            margin-bottom: 10px;
            animation: pulse 2s infinite alternate;
        }

        @keyframes pulse {
            from { transform: scale(1); }
            to { transform: scale(1.03); }
        }

        .subtitle {
            color: #c084fc;
            font-style: italic;
            margin-bottom: 30px;
        }

        /* --- AUDIO PLAYER STYLING --- */
        .audio-box {
            background: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 30px;
            margin-bottom: 30px;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(192, 132, 252, 0.2);
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }
        
        .audio-box span { font-size: 14px; color: #e9d5ff; }

        /* --- TABS / MENU NAVIGATION --- */
        .menu-container {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 30px;
        }

        .menu-btn {
            background: #6b21a8;
            color: #f5f3ff;
            border: 2px solid #a855f7;
            padding: 12px 24px;
            font-size: 16px;
            font-weight: bold;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .menu-btn:hover:not(.locked) {
            background: #a855f7;
            box-shadow: 0 0 15px #a855f7;
            transform: translateY(-2px);
        }

        .menu-btn.active {
            background: #c084fc;
            color: #1e1b4b;
            border-color: #f5f3ff;
            box-shadow: 0 0 15px #c084fc;
        }

        /* Styling khusus tombol terkunci */
        .menu-btn.locked {
            background: #3b0764;
            border-color: #4c1d95;
            color: #701a75;
            cursor: not-allowed;
            opacity: 0.6;
        }

        /* --- CONTENT SECTIONS --- */
        .content-panel {
            display: none;
            background: rgba(15, 23, 42, 0.6);
            padding: 30px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(167, 139, 250, 0.2);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            margin-bottom: 40px;
        }

        .content-panel.active { display: block; }

        /* --- FORM & INPUT --- */
        .input-group {
            display: flex;
            gap: 10px;
            margin-bottom: 25px;
            justify-content: center;
        }

        textarea {
            width: 70%;
            height: 60px;
            padding: 12px;
            border-radius: 10px;
            border: 1px solid #a855f7;
            background: rgba(255, 255, 255, 0.9);
            color: #1e1b4b;
            font-family: inherit;
            resize: none;
        }

        .submit-btn {
            background: #10b981;
            color: white;
            border: none;
            padding: 0 20px;
            border-radius: 10px;
            cursor: pointer;
            font-weight: bold;
            transition: background 0.2s;
        }
        .submit-btn:hover { background: #059669; }

        /* --- STICKY NOTES BOARD --- */
        .notes-board {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin-top: 20px;
        }

        .sticky-note {
            background: #fef08a; /* Warna kuning khas sticky note */
            color: #1e293b;
            padding: 15px;
            width: 160px;
            min-height: 120px;
            box-shadow: 5px 5px 10px rgba(0,0,0,0.3);
            transform: rotate(-2deg);
            font-family: 'Courier New', Courier, monospace;
            font-weight: bold;
            text-align: left;
            word-wrap: break-word;
            border-bottom-right-radius: 20px 5px;
            animation: fadeIn 0.5s ease-out forwards;
        }

        /* Efek rotasi acak sedikit supaya estetik */
        .sticky-note:nth-child(even) { transform: rotate(3deg); background: #fbcfe8; /* Ungu/pink muda */ }
        .sticky-note:nth-child(3n) { transform: rotate(-1deg); background: #bfdbfe; /* Biru muda */ }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.8) translateY(10px); }
            to { opacity: 1; }
        }

        /* --- DOA GUWEH TEXT BOX --- */
        .doa-text {
            font-size: 1.3rem;
            line-height: 1.8;
            color: #ffe4e6;
            text-shadow: 0 0 10px rgba(244, 63, 94, 0.3);
            border-left: 4px solid #f43f5e;
            padding-left: 20px;
            text-align: left;
        }
    </style>
</head>
<body>

<div class="container">
    <div class="meme-container">
        <img src="meme.jpeg" class="meme-img">
    </div>

    <h1>SEMANGAT UAS ICAAA</h1>
    <p class="subtitle">🎵 tebak apa hayooo</p>

    <div class="audio-box">
        <span>🎧 Play Dulu Woyy:</span>
        <audio controls id="bg-music">
            <source src="yoyok.mp3" type="audio/mpeg">
            Browser kamu tidak mendukung pemutar audio.
        </audio>
    </div>

    <div class="menu-container">
        <button class="menu-btn active" onclick="switchTab('kesulitan')">Kesulitan</button>
        <button class="menu-btn" onclick="switchTab('harapan')">Harapan</button>
        <button class="menu-btn locked" id="btn-doa" onclick="switchTab('doa')">🔒 Doa Guweh</button>
    </div>

    <div id="panel-kesulitan" class="content-panel active">
        <h3>Ketik Keresahan yang Kamu Alami Saat Ini:</h3>
        <div class="input-group">
            <textarea id="input-kesulitan" placeholder="Tulis kesulitanmu di sini ca..."></textarea>
            <button class="submit-btn" onclick="addNote('kesulitan')">Submit</button>
        </div>
        <div id="board-kesulitan" class="notes-board"></div>
    </div>

    <div id="panel-harapan" class="content-panel">
        <h3>Ketik Harapan yang Ingin Kamu Capai:</h3>
        <div class="input-group">
            <textarea id="input-harapan" placeholder="Tulis harapan/impianmu di sini ca..."></textarea>
            <button class="submit-btn" onclick="addNote('harapan')">Submit</button>
        </div>
        <div id="board-harapan" class="notes-board"></div>
    </div>

    <div id="panel-doa" class="content-panel">
        <div class="doa-text">
            "Semoga lancar Ica UAS nya, gw percaya uas jadi game gampang buat lu, karna lu adalah orang yang teguh dann tekun ca! semangattt!" ✨💜
        </div>
    </div>
</div>

<script>
    // Variabel pengunci sistem
    let kesulitanSubmitted = false;
    let harapanSubmitted = false;

    // Fungsi untuk ganti menu/tab
    function switchTab(tabName) {
        // Jika klik menu doa tapi belum terbuka, abaikan
        if (tabName === 'doa' && (!kesulitanSubmitted || !harapanSubmitted)) {
            alert("Eitss! Kamu harus mengisi dan men-submit menu 'Kesulitan' dan 'Harapan' terlebih dahulu ya ca! 😉");
            return;
