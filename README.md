  O código apresentado cria um jogo interativo em JavaScript utilizando a biblioteca p5.js, no qual o jogador controla um carro (representado pelo emoji 🚗) com o objetivo de atravessar da cidade, situada no lado direito da tela, até a fazenda,
 localizada no lado esquerdo. A principal mecânica do jogo, detalhada no bloco `draw()`, consiste em movimentar o carro horizontalmente usando as setas do teclado, desviando de obstáculos que caem do céu (emojis ⛔), com a meta de alcançar a 
 posição horizontal `x <= 150`, onde se encontra um cavalo (🐎), representando a linha de chegada.
  Inicialmente, o jogo exibe uma tela de boas-vindas com instruções, ativada pela variável `!gameStarted`. Após o clique do jogador (função `mousePressed()`), o jogo é iniciado, os obstáculos são posicionados aleatoriamente no lado da fazenda e os 
 prédios são gerados no lado da cidade por meio da função `gerarEdificios()`. O cenário é dividido visualmente entre os dois mundos: do lado esquerdo (campo), há céu azul claro, estrada de terra, grama e elementos visuais como trator, árvore, 
 cachorro e galinha, todos representados com emojis. Do lado direito (cidade), estão presentes prédios desenhados com retângulos coloridos, janelas aleatoriamente iluminadas, um sol estilizado com raios girando em torno de sua circunferência e 
 outros elementos urbanos como um caminhão e um ponto de ônibus.
  Durante a execução do jogo, o carro se move com as teclas esquerda e direita (`keyIsDown(LEFT_ARROW)` e `keyIsDown(RIGHT_ARROW)` dentro da função `move()` da classe `Carro`) e permanece dentro dos limites da tela graças ao uso da função 
 `constrain()`. Enquanto isso, os obstáculos (classe `Obstaculo`) descem verticalmente com uma velocidade definida e, ao saírem da tela sem colidir com o carro, são reposicionados no topo, incrementando a pontuação do jogador, que é exibida no 
 canto superior esquerdo. A colisão entre carro e obstáculo é detectada por meio do cálculo da distância entre eles (função `dist()`). Se a colisão for confirmada, a função `gameOver()` é chamada e exibe a tela de "Game Over" com a pontuação final 
 e instruções para reiniciar pressionando a tecla ‘R’. Da mesma forma, se o carro atingir a posição final próxima ao cavalo, a função `gameWon()` é chamada, ativando a tela de vitória com visualização dos pontos e a mesma instrução de reinício.
 A estrutura do jogo é organizada em estados controlados pelas variáveis booleanas `gameStarted`, `gameOverFlag` e `gameWonFlag`, que alternam entre a exibição da tela inicial, o jogo em si, e as telas finais. O reinício do jogo, seja após vitória 
ou derrota, é feito pelas funções `resetGame()` e `keyPressed()`, que limpam os obstáculos, regeneram os prédios e reposicionam o carro e as pontuações iniciais. As classes `Carro` e `Obstaculo` encapsulam a lógica dos personagens principais do 
jogo, com métodos de exibição (`display()`), movimento (`move()`) e reinicialização (`reset()`).
 Em resumo, o jogo desenvolvido com base nos trechos apresentados no prompt proporciona uma experiência visual divertida e educativa, utilizando recursos básicos de programação orientada a objetos, manipulação de estados, controle de fluxo, 
interatividade por teclado e mouse, além de composição gráfica com formas básicas e emojis.
  Foi usado o IA chatgpt para corrigir e acrescentar detalhes ao projeto.
