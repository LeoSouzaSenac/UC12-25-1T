# Projeto: Jogo da Memória (HTML, CSS e JavaScript)

## Objetivo

Desenvolver um jogo da memória completo utilizando HTML, CSS e JavaScript puro, aplicando conceitos de:

* Manipulação do DOM
* Eventos em JavaScript
* Controle de estado (lógica do jogo)
* Estilização com CSS
* Layout com display flex

---

## Organização

O trabalho deve ser feito em duplas, conforme definido:

* Angela Muller + Miguel Steinhorst
* Davi de Oliveira Alves + Sidnei Alberto Kleischmitt Junior
* Eduarda Cristina dos Santos + Jorge Júnior de Oliveira Corrêa
* Erica Rodrigues Barbosa + Juan Diovani Sarassa Fiorini
* Gabriel Dornelles de Almeida + Vagner Melo Pires
* Gabriela Silva da Rosa + Kalléo Kaefer Roque Antunes
* Henrique Bilhan de Souza + Miguel Vargas Ferreira
* Henry Bittencourt Padilha + Luiz Vinícius Cassabone Muniz
* Jesus Eduardo Sanchez Lopez + Nicolas Bittencourt Studzinski Liell
* Jian Luca Palini + Timóteo de Almeida Colares

---

## Requisitos do Jogo

### Cartas

* Cartas viradas para baixo inicialmente
* Ao clicar, a carta deve virar (mostrar conteúdo)
* Deve haver pares de cartas iguais
* Ao encontrar um par correto:

  * As cartas permanecem abertas
* Ao errar:

  * As cartas devem virar novamente após um pequeno tempo

---

### Lógica do Jogo (JavaScript)

O jogo deve implementar:

* Controle da primeira e segunda carta clicada
* Comparação entre cartas
* Bloqueio de clique enquanto verifica o par
* Uso de:

  * addEventListener
  * classList (add, remove ou toggle)

---

### Pontuação

O jogo deve ter um sistema de pontuação, como por exemplo:

* +1 ponto ao acertar um par
* -1 ponto ao errar (opcional)
* Exibir a pontuação na tela

---

### Informações na tela

Exibir pelo menos:

* Pontuação
* Número de jogadas (tentativas)

---

### Layout (CSS)

* Utilizar display flex para organizar os elementos
* Cartas organizadas em grade (flex)
* Interface visual organizada
* Diferenciação visual entre:

  * carta fechada
  * carta aberta
  * carta correta

---

### Extras obrigatórios

* As cartas devem ser 'embaralhadas' ao iniciar o jogo
* O jogo deve permitir reiniciar (botão de reset)

---

## Diferenciais

* Animação de virar carta
* Temporizador (tempo de jogo)
* Tema visual (filmes, jogos, etc.)
* Efeitos visuais mais elaborados
* Sons (acerto/erro)

---

## Entrega

Cada dupla deve entregar:

* Arquivos:

  * index.html
  * style.css
  * script.js
* Código organizado e indentado
* Comentários explicando a lógica principal

---

## Regras importantes

* Não usar bibliotecas ou frameworks
* Não copiar da internet
* O código deve ser autoral da dupla
* Cada integrante deve saber explicar o funcionamento

---

## Critérios de Avaliação

* Funcionamento do jogo
* Lógica em JavaScript
* Organização do código
* Uso correto de CSS (especialmente flex)
* Clareza e estrutura do projeto
