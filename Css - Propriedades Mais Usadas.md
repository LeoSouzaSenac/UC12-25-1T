# CSS – Propriedades Mais Usadas (Tabela de Referência)

## Como usar este material

* Use como consulta rápida
* Não precisa decorar tudo
* Foque em entender os conceitos

---

## Propriedades de Layout e Display

| Propriedade                 | Valores comuns                                | Explicação                                                                          |
| --------------------------- | --------------------------------------------- | ----------------------------------------------------------------------------------- |
| display                     | block, inline, inline-block, flex, grid, none | Define como o elemento se comporta no layout (quebra linha, fica lado a lado, etc.) |
| position                    | static, relative, absolute, fixed, sticky     | Controla o posicionamento do elemento na página                                     |
| top / left / right / bottom | px, %, etc                                    | Define posição quando `position` não é static                                       |
| z-index                     | número (1, 10, 999)                           | Controla quem fica “na frente” de quem                                              |
| overflow                    | hidden, scroll, auto                          | Controla o que acontece quando o conteúdo passa do limite                           |

---

## Box Model

| Propriedade | Valores comuns          | Explicação                                          |
| ----------- | ----------------------- | --------------------------------------------------- |
| width       | px, %, vw               | Define a largura do elemento                        |
| height      | px, %, vh               | Define a altura do elemento                         |
| padding     | px, %                   | Espaço interno (entre conteúdo e borda)             |
| margin      | px, auto                | Espaço externo (entre elementos)                    |
| border      | 1px solid black         | Define a borda (espessura, tipo e cor)              |
| box-sizing  | content-box, border-box | Define como o tamanho total do elemento é calculado |

---

## Flexbox (Layout moderno)

| Propriedade     | Valores comuns                    | Explicação                       |
| --------------- | --------------------------------- | -------------------------------- |
| display         | flex                              | Ativa o Flexbox                  |
| flex-direction  | row, column                       | Define direção dos elementos     |
| justify-content | flex-start, center, space-between | Alinhamento horizontal           |
| align-items     | flex-start, center, stretch       | Alinhamento vertical             |
| gap             | px                                | Espaço entre elementos           |
| flex            | 1, auto                           | Define crescimento dos elementos |

---

## Grid (Layout avançado)

| Propriedade           | Valores comuns          | Explicação                    |
| --------------------- | ----------------------- | ----------------------------- |
| display               | grid                    | Ativa o Grid                  |
| grid-template-columns | 1fr 1fr, repeat(3, 1fr) | Define colunas                |
| grid-template-rows    | auto, 100px             | Define linhas                 |
| gap                   | px                      | Espaço entre linhas e colunas |

---

## Texto e Fonte

| Propriedade    | Valores comuns       | Explicação             |
| -------------- | -------------------- | ---------------------- |
| color          | red, #000, rgb()     | Cor do texto           |
| font-size      | px, rem              | Tamanho da fonte       |
| font-weight    | normal, bold         | Peso da fonte          |
| text-align     | left, center, right  | Alinhamento do texto   |
| text-transform | uppercase, lowercase | Transformação do texto |
| font-family    | Arial, sans-serif    | Tipo de fonte          |

---

## Background

| Propriedade         | Valores comuns | Explicação        |
| ------------------- | -------------- | ----------------- |
| background-color    | red, #fff      | Cor de fundo      |
| background-image    | url()          | Imagem de fundo   |
| background-size     | cover, contain | Ajuste da imagem  |
| background-position | center, top    | Posição da imagem |

---

## Bordas e Sombras

| Propriedade   | Valores comuns   | Explicação         |
| ------------- | ---------------- | ------------------ |
| border-radius | px, %            | Arredondamento     |
| box-shadow    | 2px 2px 5px gray | Sombra do elemento |

---

## Espaçamento e Visibilidade

| Propriedade | Valores comuns  | Explicação                       |
| ----------- | --------------- | -------------------------------- |
| opacity     | 0 a 1           | Transparência                    |
| visibility  | hidden, visible | Mostra ou oculta (mantém espaço) |
| display     | none            | Remove da tela                   |

---

## Interação

| Propriedade    | Valores comuns | Explicação                      |
| -------------- | -------------- | ------------------------------- |
| cursor         | pointer        | Tipo do cursor                  |
| transition     | 0.3s           | Animação suave                  |
| hover (:hover) | pseudo-classe  | Aplica estilo ao passar o mouse |

---

## Unidades mais usadas

| Unidade | Significado              |
| ------- | ------------------------ |
| px      | pixel fixo               |
| %       | relativo ao elemento pai |
| rem     | relativo ao root         |
| vw      | largura da tela          |
| vh      | altura da tela           |

---

## Observações importantes (didáticas)

* `margin` → espaço externo
* `padding` → espaço interno
* `display` → comportamento do elemento
* `box-sizing: border-box` → evita erros de tamanho
* `flex` e `grid` → usados para layout moderno

---
