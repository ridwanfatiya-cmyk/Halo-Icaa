<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Special Message for You ❤️</title>
    <style>
        /* Mengatur background merah cerah yang hangat */
        body {
            margin: 0;
            padding: 0;
            background-color: #d63031;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: white;
            overflow: hidden;
        }

        .card-container {
            text-align: center;
            padding: 20px;
        }

        /* Membuat hati pink dengan CSS */
        .heart {
            background-color: #ff75a0;
            display: inline-block;
            height: 100px;
            margin: 0 10px;
            position: relative;
            top: 0;
            transform: rotate(-45deg);
            width: 100px;
            /* Efek animasi berdegup */
            animation: beat 1.2s infinite;
            filter: drop-shadow(0 0 15px rgba(255, 117, 160, 0.6));
        }

        .heart:before,
        .heart:after {
            content: "";
            background-color: #ff75a0;
            border-radius: 50%;
            height: 100px;
            position: absolute;
            width: 100px;
        }

        .heart:before {
            top: -50px;
            left: 0;
        }

        .heart:after {
            top: 0;
            left: 50px;
        }

        /* Animasi Detak Jantung */
        @keyframes beat {
            0% { transform: scale(1) rotate(-45deg); }
            20% { transform: scale(1.1) rotate(-45deg); }
            40% { transform: scale(1) rotate(-45deg); }
            60% { transform: scale(1.15) rotate(-45deg); }
            80% { transform: scale(1) rotate(-45deg); }
            100% { transform: scale(1) rotate(-45deg); }
        }

        h1 {
            font-size: 2.5rem;
            margin-top: 40px;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        p {
            font-size: 1.2rem;
            opacity: 0.9;
            line-height: 1.6;
        }
    </style>
</head>
<body>

    <div class="card-container">
        <!-- Komponen Hati Pink -->
        <div class="heart"></div>
        
        <!-- Teks Ucapan (Bisa kamu ganti sesukamu) -->
        <h1>Halo, Kamu! ✨</h1>
        <p>Aku cuma mau bilang terima kasih ya sudah ada sampai hari ini.<br>
        Semoga harimu semanis warna hati di atas!</p>
    </div>

</body>
</html>
