<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tarot do Carlin</title>
    <style>
        /* CSS para layout com fundo laranja e cartas roxas */
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #FFA500; /* Fundo laranja */
            margin: 0;
        }
        .container {
            text-align: center;
        }
        .cards {
            margin-top: 20px;
            display: flex;
            justify-content: center;
        }
        .card {
            width: 100px;
            height: 150px;
            margin: 10px;
            background-color: #800080; /* Cor roxa para as cartas */
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            color: #fff; /* Texto branco nas cartas */
            font-size: 36px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Faz a pergunta aí Júlia🥺</h1>
        <input type="text" id="question" placeholder="Digite sua pergunta">
        <div class="cards">
            <div class="card" onclick="revealAnswer(this)">?</div>
            <div class="card" onclick="revealAnswer(this)">?</div>
            <div class="card" onclick="revealAnswer(this)">?</div>
        </div>
    </div>
    
    <script>
        function revealAnswer(card) {
            const answers = ["Sim", "Não"];
            const randomAnswer = answers[Math.floor(Math.random() * answers.length)];
            card.innerHTML = randomAnswer;
            card.style.backgroundColor = '#fff'; /* Muda a cor da carta ao revelar a resposta */
            card.style.color = '#000'; /* Muda a cor do texto ao revelar a resposta */
            card.style.fontSize = '24px';
        }
    </script>
</body>
</html>
