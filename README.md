# desafio-site-simples
## Desafio da DIO proposto pelo Felipão
Browser support
Internet Explorer|Edge |Firefox |Chrome	|Safari	|Samsung browser |Brave
-----------------|------|-------|-------|-------|---------------|------
❌              |✔️	  |✔️	  |✔️	  |✔️    |✔️             |✔️

Demo: https://codepen.io/buribalazs/pen/NWvReZN


####Página simples com um título, um espaço para a mensagem e um botão que, ao ser clicado, exibe uma mensagem bíblica motivacional aleatória.


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mensagens Bíblicas Motivacionais</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f5f5f5;
        }
        .container {
            text-align: center;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .message {
            font-size: 24px;
            margin: 20px 0;
        }
        .button {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Mensagens Bíblicas Motivacionais</h1>
        <div class="message" id="message">Clique no botão para receber uma mensagem.</div>
        <button class="button" onclick="generateMessage()">Gerar Mensagem</button>
    </div>

    <script>
        const messages = [
            "O Senhor é meu pastor e nada me faltará. - Salmos 23:1",
            "Tudo posso naquele que me fortalece. - Filipenses 4:13",
            "Confia no Senhor de todo o teu coração. - Provérbios 3:5",
            "Aqueles que esperam no Senhor renovarão as suas forças. - Isaías 40:31",
            "Porque sou eu que conheço os planos que tenho para vocês, diz o Senhor. - Jeremias 29:11"
        ];

        function generateMessage() {
            const randomIndex = Math.floor(Math.random() * messages.length);
            document.getElementById("message").innerText = messages[randomIndex];
        }
    </script>
</body>
</html>
