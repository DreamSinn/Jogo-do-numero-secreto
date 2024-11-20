Jogo do Número Secreto
Este é um jogo interativo simples onde o objetivo é adivinhar um número secreto gerado aleatoriamente entre 1 e 50. O jogador faz tentativas, e o jogo dá dicas sobre se o número secreto é maior ou menor que o número escolhido. O jogo também fornece feedback sobre o número de tentativas feitas até a solução.

Funcionalidades
O jogador escolhe um número entre 1 e 50.
O jogo informa se o número secreto é maior ou menor que o chute.
Ao acertar, o número de tentativas é exibido e o jogador pode reiniciar o jogo.
O jogo utiliza a API responsiveVoice para ler as mensagens em voz alta.
O número secreto é sorteado aleatoriamente e o jogo impede números repetidos até que todos os números possíveis (1-50) sejam sorteados.
Tecnologias Utilizadas
HTML: Estrutura básica da página web.
CSS: Estilos para a interface (não mostrado no código, mas necessário para uma boa apresentação).
JavaScript: Lógica do jogo e interação com a página.
API responsiveVoice: Para a síntese de voz que lê as mensagens para o jogador.
Como Rodar o Projeto
1. Clone o repositório
bash
Copy code
git clone https://github.com/DreamSinn/Testorino
2. Abra o arquivo index.html no seu navegador
Este projeto não requer instalação de pacotes ou configurações adicionais. Basta abrir o arquivo HTML em qualquer navegador moderno para começar a jogar.

Como Jogar
Iniciar o Jogo: Ao abrir a página, o título "Jogo do número secreto" será exibido e você será instruído a escolher um número entre 1 e 50.
Fazer um Chute: Insira um número no campo de entrada e pressione Enter ou o botão para submeter.
Dicas: O jogo informará se o número secreto é maior ou menor que o seu chute.
Acertou!: Quando você acertar o número, o jogo exibirá o número de tentativas e permitirá que você reinicie o jogo.
Reiniciar: Após acertar ou em qualquer momento, você pode clicar no botão para reiniciar o jogo.
Funções do Código
exibirTextoNaTela(tag, texto)
Exibe um texto dentro de uma tag HTML especificada e também utiliza a API responsiveVoice para falar o texto em voz alta.

exibirMensagemInicial()
Exibe a mensagem inicial do jogo, pedindo para o usuário escolher um número entre 1 e 50.

verificarChute()
Verifica o chute do jogador. Se o chute for correto, exibe a mensagem de sucesso, com o número de tentativas. Se o chute for incorreto, informa se o número secreto é maior ou menor que o chute.

gerarNumeroAleatorio()
Gera um número aleatório entre 1 e 50. Garante que não haja números repetidos até que todos os números possíveis sejam sorteados.

limparCampo()
Limpa o campo de entrada para que o jogador possa fazer um novo chute.

reiniciarJogo()
Reinicia o jogo, gerando um novo número secreto e resetando o número de tentativas.

Exemplo de Interação
O jogo começa com a mensagem: "Escolha um número entre 1 e 50".
O jogador escolhe o número 25.
O jogo pode responder: "O número secreto é maior".
O jogador tenta novamente com 40.
O jogo pode responder: "O número secreto é menor".
O jogador escolhe 32 e acerta, e o jogo mostra: "Você descobriu o número secreto com 3 tentativas!".
Requisitos
Um navegador moderno que suporte JavaScript.
Conexão com a internet para carregar a API responsiveVoice.
Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

Contribuições
Este projeto é pessoal, mas você pode contribuir com melhorias ou sugestões através de pull requests ou abrindo issues no repositório.
