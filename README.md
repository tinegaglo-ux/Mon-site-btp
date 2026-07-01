<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculateur de Dosage de Béton | BTP</title>
    <style>
        :root {
            --primary: #f39c12;
            --dark: #2c3e50;
            --light: #ecf0f1;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f6f7;
            margin: 0;
            padding: 20px;
            color: #333;
        }
        .container {
            max-width: 600px;
            margin: 30px auto;
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            border-top: 5px solid var(--primary);
        }
        h1 {
            text-align: center;
            color: var(--dark);
            margin-bottom: 25px;
            font-size: 24px;
        }
        .form-group {
            margin-bottom: 20px;
        }
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: var(--dark);
        }
        select, input {
            width: 100%;
            padding: 12px;
            border: 2px solid #bdc3c7;
            border-radius: 6px;
            font-size: 16px;
            box-sizing: border-box;
        }
        select:focus, input:focus {
            border-color: var(--primary);
            outline: none;
        }
        button {
            width: 100%;
            background-color: var(--dark);
            color: white;
            padding: 14px;
            border: none;
            border-radius: 6px;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s;
        }
        button:hover {
            background-color: #1a252f;
        }
        .results {
            margin-top: 25px;
            padding: 20px;
            background-color: #fcf8e3;
            border-left: 5px solid var(--primary);
            border-radius: 4px;
            display: none;
        }
        .results h3 {
            margin-top: 0;
            color: #c0392b;
        }
        .result-item {
            margin: 10px 0;
            font-size: 16px;
        }
        .result-item span {
            font-weight: bold;
            color: var(--dark);
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Calculateur de Dosage de Béton</h1>
    
    <div class="form-group">
        <label for="type">Type d'ouvrage (Dosage) :</label>
        <select id="type">
            <option value="350">Béton armé courant (Poutres, Dalles) - 350 kg/m³</option>
            <option value="300">Béton de fondation - 300 kg/m³</option>
            <option value="150">Béton de propreté - 150 kg/m³</option>
        </select>
    </div>

    <div class="form-group">
        <label for="volume">Volume de béton nécessaire (m³) :</label>
        <input type="number" id="volume" placeholder="Ex: 2.5" step="0.1" min="0.1">
    </div>

    <button onclick="calculerBeton()">Calculer les Matériaux</button>

    <div id="results" class="results">
        <h3>Matériaux requis :</h3>
        <div class="result-item">Ciment (Sacs de 50kg) : <span id="resCiment">0</span> sacs</div>
        <div class="result-item">Sable : <span id="resSable">0</span> m³ (ou <span id="resSableL">0</span> Litres)</div>
        <div class="result-item">Gravier : <span id="resGravier">0</span> m³ (ou <span id="resGravierL">0</span> Litres)</div>
        <div class="result-item">Eau : <span id="resEau">0</span> Litres</div>
    </div>
</div>

<script>
    function calculerBeton() {
        const dosage = parseFloat(document.getElementById('type').value);
        const volume = parseFloat(document.getElementById('volume').value);
        
        if (isNaN(volume) || volume <= 0) {
            alert("Veuillez saisir un volume valide.");
            return;
        }

        // Calculs de base basés sur les ratios standards du bâtiment
        let nbrSacs = Math.ceil((dosage * volume) / 50);
        let volSable = (0.4 * volume).toFixed(2);
        let volGravier = (0.8 * volume).toFixed(2);
        let eau = Math.round(175 * volume);

        // Conversion en Litres pour les seaux sur chantier
        let sableL = Math.round(volSable * 1000);
        let gravierL = Math.round(volGravier * 1000);

        // Affichage des résultats
        document.getElementById('resCiment').innerText = nbrSacs;
        document.getElementById('resSable').innerText = volSable;
        document.getElementById('resSableL').innerText = sableL;
        document.getElementById('resGravier').innerText = volGravier;
        document.getElementById('resGravierL').innerText = gravierL;
        document.getElementById('document.getElementById').innerText = eau;
        
        document.getElementById('results').style.display = 'block';
    }
</script>
</body>
</html>
