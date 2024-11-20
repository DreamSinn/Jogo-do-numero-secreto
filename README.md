Jogo do Número Secreto
🎯 Sobre
Este é um jogo simples desenvolvido como parte de um projeto para cursos de lógica de programação. O objetivo é adivinhar um número secreto gerado aleatoriamente entre 1 e 50, e o jogo fornece feedback sobre se o número secreto é maior ou menor do que o chute do jogador.

🚀 Tecnologias
<div> <img src="https://img.shields.io/badge/HTML-239120?style=for-the-badge&logo=html5&logoColor=white"> <img src="https://img.shields.io/badge/CSS-239120?&style=for-the-badge&logo=css3&logoColor=white"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> </div>
📜 Como Funciona
Iniciar o Jogo: Ao acessar a página, o título "Jogo do número secreto" será exibido, e você será instruído a escolher um número entre 1 e 50.
Chutar o Número: Insira um número no campo de entrada e pressione Enter ou clique no botão para submeter.
Dicas: O jogo indicará se o número secreto é maior ou menor que o seu chute.
Acertou!: Quando o número secreto for descoberto, o jogo mostrará o número de tentativas e permitirá reiniciar.
Reiniciar: Após acertar ou em qualquer momento, você pode reiniciar o jogo com um botão.
⚙️ Funcionalidades
Exibição de mensagens: O jogo utiliza a API responsiveVoice para ler as mensagens em voz alta, tornando a experiência mais interativa.
Número secreto aleatório: O número secreto é gerado aleatoriamente entre 1 e 50, sem repetições até que todos os números sejam sorteados.
Tentativas: O número de tentativas é contado, e ao acertar o número, o jogo mostra quantas tentativas foram necessárias.
💻 Como Rodar o Projeto
1. Clone o repositório
bash
Copy code
git clone https://link-do-repositorio.git
2. Abra o arquivo index.html
Abra o arquivo index.html em qualquer navegador moderno para começar a jogar.

📝 Exemplo de Interação
O jogo começa com a mensagem: "Escolha um número entre 1 e 50".
O jogador escolhe o número 25.
O jogo responde: "O número secreto é maior".
O jogador tenta com 40.
O jogo responde: "O número secreto é menor".
O jogador escolhe 32 e acerta! O jogo mostra: "Você descobriu o número secreto com 3 tentativas!".
🔧 Funcões do Código
exibirTextoNaTela(tag, texto)
Exibe um texto dentro de uma tag HTML especificada e utiliza a API responsiveVoice para falar o texto.

exibirMensagemInicial()
Exibe a mensagem inicial do jogo, pedindo para o jogador escolher um número.

verificarChute()
Verifica se o chute do jogador está correto, e dá dicas sobre o número secreto.

gerarNumeroAleatorio()
Gera um número aleatório entre 1 e 50, sem repetições.

limparCampo()
Limpa o campo de entrada para o próximo chute.

reiniciarJogo()
Reinicia o jogo, gerando um novo número secreto e resetando as tentativas.

📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

🤝 Contribuições
Este projeto é pessoal, mas contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests para melhorias.
