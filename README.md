<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Usmon Bakhodirov - The Cyber Panther</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        html, body {
            width: 100%;
            min-height: 100vh;
            background: radial-gradient(circle at top, #1f0505 0%, #060a14 55%, #02040a 100%);
            color: #ffffff;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow-x: hidden;
        }
        .fullscreen-wrapper {
            width: 100%;
            min-height: 100vh;
            padding: 30px 5vw;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            border-top: 6px solid #dc052d; /* Bayern Red */
            border-bottom: 6px solid #0099b5; /* UZB Blue */
        }
        header {
            text-align: center;
            padding: 25px;
            background: rgba(15, 20, 34, 0.85);
            border: 2px solid #d4af37;
            border-radius: 20px;
            box-shadow: 0 0 40px rgba(212, 175, 55, 0.25);
            margin-bottom: 25px;
        }
        h1 {
            color: #d4af37;
            font-size: clamp(2.2em, 5vw, 3.8em);
            text-shadow: 0 0 15px rgba(212, 175, 55, 0.6);
            letter-spacing: 1px;
        }
        .nickname {
            color: #00d2ff;
            font-size: clamp(1.2em, 2.5vw, 1.8em);
            font-weight: bold;
            letter-spacing: 3px;
            margin-top: 8px;
        }
        .badges {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }
        .badge {
            background: linear-gradient(135deg, #161d2e, #0d121d);
            padding: 12px 24px;
            border-radius: 12px;
            border: 2px solid #00d2ff;
            font-weight: bold;
            font-size: 1.1em;
            box-shadow: 0 4px 15px rgba(0, 210, 255, 0.2);
        }
        .grid-main {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 25px;
            width: 100%;
            margin-bottom: 25px;
        }
        .card {
            background: rgba(15, 20, 34, 0.9);
            border-radius: 20px;
            padding: 25px;
            border: 2px solid #28334a;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }
        .card.cyber-card {
            border-color: #ff0044;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        .card h2 {
            color: #d4af37;
            margin-bottom: 15px;
            font-size: 1.6em;
        }
        .clean-sheet {
            font-size: 1.5em;
            color: #ff0044;
            font-weight: bold;
            background: rgba(255, 0, 68, 0.1);
            padding: 10px 20px;
            border-radius: 10px;
            border: 1px solid #ff0044;
            margin-bottom: 15px;
        }
        .counter-display {
            font-size: clamp(1.6em, 3.2vw, 2.6em);
            color: #00ff66;
            font-weight: bold;
            margin: 15px 0;
            font-family: 'Courier New', Courier, monospace;
            text-shadow: 0 0 12px rgba(0, 255, 102, 0.5);
            word-break: break-all;
        }
        .cyber-button {
            background: linear-gradient(90deg, #dc052d, #d4af37);
            color: #ffffff;
            border: none;
            padding: 16px 36px;
            font-size: 1.25em;
            font-weight: bold;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 6px 20px rgba(220, 5, 45, 0.5);
            transition: transform 0.2s, box-shadow 0.2s;
            margin-top: 10px;
        }
        .cyber-button:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 30px rgba(220, 5, 45, 0.8);
        }
        .cyber-button:active {
            transform: scale(0.95);
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }
        th, td {
            padding: 14px;
            border-bottom: 1px solid #28334a;
            text-align: left;
            font-size: 1.05em;
        }
        th {
            color: #00d2ff;
            background-color: rgba(0, 210, 255, 0.08);
        }
        .tactic-pitch {
            background: linear-gradient(180deg, #0b4f26 0%, #07381a 100%);
            border: 3px solid #ffffff;
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            margin-top: 10px;
        }
        .pitch-row {
            margin: 14px 0;
            font-weight: bold;
            font-size: 1.1em;
            background: rgba(0, 0, 0, 0.45);
            padding: 10px;
            border-radius: 8px;
        }
        footer {
            text-align: center;
            padding: 18px;
            background: rgba(15, 20, 34, 0.85);
            border-radius: 15px;
            border: 1px solid #28334a;
            color: #a0aec0;
            font-size: 1.1em;
        }
        footer a {
            color: #00d2ff;
            text-decoration: none;
            font-weight: bold;
        }
        footer a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

<div class="fullscreen-wrapper">
    <header>
        <h1>USMON BAKHODIROV</h1>
        <div class="nickname">💻🐆 THE CYBER PANTHER 🐆💻</div>
        <div class="badges">
            <div class="badge" style="color: #00ff66; border-color: #00ff66;">🇺🇿 UZB LOGOTIPI</div>
            <div class="badge" style="color: #ff4d6d; border-color: #ff4d6d;">🔴 #13 FORMA</div>
            <div class="badge" style="color: #d4af37; border-color: #d4af37;">👑 8 YOSH</div>
            <div class="badge" style="color: #00d2ff; border-color: #00d2ff;">💎 NARXI: CHEKSIZ</div>
        </div>
    </header>

    <div class="grid-main">
        <!-- Chap blok: Jonli JS Seyf Hisoblagichi -->
        <div class="card cyber-card">
            <h2>⚡ KOINOT SEYFLAR TIZIMI</h2>
            <div class="clean-sheet">O‘TKAZILGAN GOLLAR: 0 TA GOL! 🛑</div>
            <p style="color: #cbd5e1; font-size: 1.1em;">Jami kiber-seyflar rekordi (30 Trilliondan boshlanadi):</p>
            <div id="save-counter" class="counter-display">30,000,000,000,000,000</div>
            <button class="cyber-button" onclick="addCyberSave()">Yangi Seyf Qo‘shish 🧤</button>
            <p id="status-msg" style="color: #00d2ff; margin-top: 12px; font-size: 0.95em;">Tugmani bosib yangi seyflarni qo‘shing!</p>
        </div>

        <!-- O'ng blok: Sovrinlar Muzeyi -->
        <div class="card">
            <h2>🏆 5 TRILLIONLIK KUBOKLAR MUZEYI</h2>
            <table>
                <tr>
                    <th>Turnir Nomi</th>
                    <th>Kuboklar Soni</th>
                </tr>
                <tr>
                    <td>🇩🇪 Bundesliga Chempionligi</td>
                    <td style="color: #d4af37; font-weight: bold;">5 000 000 000 000 ta</td>
                </tr>
                <tr>
                    <td>⚡ UEFA Super Kubogi</td>
                    <td style="color: #d4af37; font-weight: bold;">400 ta</td>
                </tr>
                <tr>
                    <td>🇪🇺 UEFA Chempionlar Ligasi</td>
                    <td style="color: #d4af37; font-weight: bold;">200 ta</td>
                </tr>
                <tr>
                    <td>🇺🇿 Jahon Chempionati (JCH)</td>
                    <td style="color: #d4af37; font-weight: bold;">100 ta</td>
                </tr>
                <tr>
                    <td><strong>JAMI SOVRINLAR</strong></td>
                    <td style="color: #00ff66; font-weight: bold;">5 000 000 000 700 ta!</td>
                </tr>
            </table>
        </div>

        <!-- Pastki blok: 4-2-3-1 Taktik Maydon -->
        <div class="card">
            <h2>📋 TASDIQLANGAN 4-2-3-1 TAKTIKASI</h2>
            <div class="tactic-pitch">
                <div class="pitch-row" style="color: #ffd700;">⚽ HUJUMCHI (ST): Harri Keyn (Oltin to‘p №1)</div>
                <div class="pitch-row" style="color: #00d2ff;">💎 QANOT & PLEYMEYKER: Maykl Olise</div>
                <div class="pitch-row" style="color: #ffffff;">🛡️ HIMOYA VA TAYANCH: 4 Himoyachi + 2 Tayanch</div>
                <div class="pitch-row" style="color: #00ff66; border: 2px solid #00ff66;">🧤 DARVOZABON (GK): Usmon Bakhodirov (#13)</div>
            </div>
        </div>
    </div>

    <footer>
        Junior IT Academy talabasi <strong>Usmon Bakhodirov</strong> loyihasi | 
        Rasmiy sayt: <a href="https://sites.google.com/view/fifa-world-cup-2030" target="_blank">Football score u9 💻</a>
    </footer>
</div>

<script>
    let currentSaves = 30000000000000000;

    function formatNumber(num) {
        return num.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
    }

    function addCyberSave() {
        currentSaves += 100000000000000;
        document.getElementById("save-counter").innerText = formatNumber(currentSaves);
        document.getElementById("status-msg").innerText = "⚡ +100 Trillion yangi kiber-seyf qo‘shildi!";
    }
</script>

</body>
</html>
