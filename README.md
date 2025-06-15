<!DOCTYPE html><html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Quem é Você?</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #1e1e2f;
      color: #f6f6f6;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      padding: 2rem;
    }
    h1 {
      color: #fdd9f5;
      text-shadow: 0 0 10px #ff80cc;
      text-align: center;
    }
    .quiz {
      background-color: #2b2b3d;
      padding: 2rem;
      border-radius: 20px;
      box-shadow: 0 0 20px #00000088;
      max-width: 500px;
      width: 100%;
    }
    .question {
      margin-bottom: 1rem;
    }
    .question label {
      display: block;
      margin-bottom: 0.5rem;
    }
    .question input[type="text"] {
      width: 100%;
      padding: 0.5rem;
      border: none;
      border-radius: 10px;
      background-color: #444;
      color: #fff;
    }
    button {
      margin-top: 1rem;
      padding: 0.7rem 1.5rem;
      border: none;
      border-radius: 10px;
      background-color: #ff80cc;
      color: #1e1e2f;
      font-weight: bold;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    button:hover {
      background-color: #ff66b2;
    }
    .result {
      margin-top: 2rem;
      padding: 1rem;
      background-color: #333;
      border-radius: 15px;
      display: none;
      white-space: pre-line;
    }
  </style>
</head>
<body>
  <h1>🌙 Quem é você nesse mundinho estranho?</h1>
  <div class="quiz">
    <div class="question">
      <label for="cor">Se você fosse uma cor, qual seria?</label>
      <input type="text" id="cor" placeholder="ex: lilás lunar">
    </div>
    <div class="question">
      <label for="animal">Qual animal representa seu lado secreto?</label>
      <input type="text" id="animal" placeholder="ex: coruja sombria">
    </div>
    <div class="question">
      <label for="sentimento">Descreva um sentimento que te visita à noite:</label>
      <input type="text" id="sentimento" placeholder="ex: saudade adormecida">
    </div>
    <button onclick="mostrarResultado()">Mostrar minha essência</button>
    <div class="result" id="resultado"></div>
  </div>  <script>
    function mostrarResultado() {
      const cor = document.getElementById('cor').value.trim();
      const animal = document.getElementById('animal').value.trim();
      const sentimento = document.getElementById('sentimento').value.trim();

      if (!cor || !animal || !sentimento) {
        alert("Preencha tudo direitinho, por favorzinho 🥺");
        return;
      }

      const resultado = `Você é feito(a) de ${cor},
caminha como um(a) ${animal},
e é acompanhado(a) pelo sentimento de \"${sentimento}\" nas noites mais silenciosas.`;

      const resultDiv = document.getElementById('resultado');
      resultDiv.innerText = resultado;
      resultDiv.style.display = 'block';
    }
  </script></body>
</html>
