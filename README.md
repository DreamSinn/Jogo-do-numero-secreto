<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jogo do Número Secreto</title>
  <link rel="stylesheet" href="styles.css">
  <script src="https://code.responsivevoice.org/responsivevoice.js"></script>
</head>
<body>
  <header>
    <h1>Jogo do Número Secreto</h1>
    <p>🎯 Adivinhe o número secreto entre 1 e 50!</p>
  </header>

  <main>
    <section id="game">
      <div id="instructions">
        <h2>Como jogar:</h2>
        <p>Escolha um número entre 1 e 50 e tente adivinhar o número secreto.</p>
        <p>Dicas serão dadas para ajudar você a acertar!</p>
      </div>

      <div id="interaction">
        <input type="number" id="guessInput" placeholder="Digite seu chute" min="1" max="50">
        <button id="submitGuess">Enviar</button>
        <button id="restartGame">Reiniciar</button>
        <p id="feedback"></p>
      </div>
    </section>

    <section id="about">
      <h2>🚀 Tecnologias</h2>
      <div>
        <img src="https://img.shields.io/badge/HTML-239120?style=for-the-badge&logo=html5&logoColor=white">
        <img src="https://img.shields.io/badge/CSS-239120?&style=for-the-badge&logo=css3&logoColor=white">
        <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
      </div>
    </section>

    <section id="example">
      <h2>📝 Exemplo de Interação</h2>
      <p>Você escolhe: <strong>25</strong>. O jogo responde: "O número secreto é maior".</p>
      <p>Você escolhe: <strong>40</strong>. O jogo responde: "O número secreto é menor".</p>
      <p>Você escolhe: <strong>32</strong>. O jogo responde: "Você descobriu o número secreto com 3 tentativas!"</p>
    </section>

    <section id="license">
      <h2>📄 Licença</h2>
      <p>Este projeto está sob a licença MIT.</p>
    </section>

    <footer>
      <p>🤝 Contribuições são bem-vindas!</p>
    </footer>
  </main>

  <script>
    let numeroSecreto = gerarNumeroAleatorio();
    let tentativas = 0;

    function gerarNumeroAleatorio() {
      return Math.floor(Math.random() * 50) + 1;
    }

    function exibirTextoNaTela(tag, texto) {
      const elemento = document.querySelector(tag);
      elemento.textContent = texto;
      responsiveVoice.speak(texto, "Portuguese Female");
    }

    function verificarChute() {
      const chute = parseInt(document.getElementById("guessInput").value);
      tentativas++;
      if (isNaN(chute) || chute < 1 || chute > 50) {
        exibirTextoNaTela("#feedback", "Por favor, insira um número válido entre 1 e 50.");
        return;
      }
      if (chute === numeroSecreto) {
        exibirTextoNaTela("#feedback", `Parabéns! Você acertou o número secreto ${numeroSecreto} em ${tentativas} tentativas!`);
      } else if (chute < numeroSecreto) {
        exibirTextoNaTela("#feedback", "O número secreto é maior!");
      } else {
        exibirTextoNaTela("#feedback", "O número secreto é menor!");
      }
    }

    function reiniciarJogo() {
      numeroSecreto = gerarNumeroAleatorio();
      tentativas = 0;
      document.getElementById("guessInput").value = "";
      exibirTextoNaTela("#feedback", "Novo jogo iniciado! Escolha um número entre 1 e 50.");
    }

    document.getElementById("submitGuess").addEventListener("click", verificarChute);
    document.getElementById("restartGame").addEventListener("click", reiniciarJogo);

    window.onload = () => exibirTextoNaTela("#feedback", "Escolha um número entre 1 e 50 para começar!");
  </script>
</body>
</html>
