# Media Queries no CSS

## O que são Media Queries?

Media Queries são recursos do CSS usados para aplicar estilos diferentes dependendo do tamanho da tela, orientação, resolução e outras características do dispositivo onde o site está sendo exibido.

Elas são fundamentais para criar layouts responsivos, ou seja, interfaces que se adaptam corretamente a celulares, tablets e computadores.

---

## Sintaxe básica

```css
@media condição {
    /* estilos CSS */
}
```

### Exemplo

```css
@media (max-width: 600px) {
    body {
        background-color: lightblue;
    }
}
```

Isso significa:

Se a largura da tela for menor ou igual a 600px, o fundo da página ficará azul claro.

---

## Media Features mais utilizadas

| Feature       | Função                                         |
| ------------- | ---------------------------------------------- |
| `max-width`   | Aplica estilos até determinada largura         |
| `min-width`   | Aplica estilos a partir de determinada largura |
| `max-height`  | Aplica estilos até determinada altura          |
| `min-height`  | Aplica estilos a partir de determinada altura  |
| `orientation` | Detecta se a tela está em retrato ou paisagem  |
| `resolution`  | Detecta a resolução da tela                    |

---

## Exemplo prático de layout responsivo

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Media Query Exemplo</title>

    <style>

        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        .container {
            padding: 20px;
            text-align: center;
            background-color: lightgreen;
        }

        /* Celulares */
        @media (max-width: 600px) {

            .container {
                background-color: lightcoral;
                font-size: 18px;
            }

        }

        /* Tablets */
        @media (min-width: 601px) and (max-width: 1024px) {

            .container {
                background-color: lightblue;
                font-size: 22px;
            }

        }

        /* Computadores */
        @media (min-width: 1025px) {

            .container {
                background-color: lightgreen;
                font-size: 26px;
            }

        }

    </style>
</head>
<body>

    <div class="container">

        <h1>Bem-vindo ao site!</h1>

        <p>
            Este layout se adapta ao tamanho da tela.
        </p>

    </div>

</body>
</html>
```

---

## Importância da meta viewport

Para que as Media Queries funcionem corretamente em celulares, é necessário adicionar esta meta tag no `<head>`:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Ela faz com que o navegador utilize a largura real do dispositivo.

---

## Como testar

1. Abra o site no navegador.
2. Diminua a largura da janela.
3. Observe as mudanças no layout.
4. Teste também pelo celular.
5. Utilize o modo responsivo do navegador.

---

## Flexbox

### O que é Flexbox?

Flexbox é um sistema de layout do CSS utilizado para organizar elementos dentro de um container.

Ele permite:

* Alinhamento horizontal e vertical
* Distribuição automática de espaço
* Organização em linhas e colunas
* Controle de espaçamento entre elementos
* Reorganização de itens

---

## Quando usar Flexbox

| Situação                 | Exemplo             |
| ------------------------ | ------------------- |
| Centralizar elementos    | Botão centralizado  |
| Criar linhas e colunas   | Cards lado a lado   |
| Espaçar itens igualmente | Menu horizontal     |
| Organizar conteúdo       | Layouts responsivos |

---

## Exemplo com Flexbox

```css
.container {
    display: flex;

    justify-content: space-between;

    align-items: center;
}
```

### Explicação

| Propriedade       | Função                 |
| ----------------- | ---------------------- |
| `display: flex`   | Ativa o Flexbox        |
| `justify-content` | Alinha horizontalmente |
| `align-items`     | Alinha verticalmente   |

---

## Media Queries

### O que elas fazem?

Media Queries permitem alterar estilos dependendo do tamanho da tela.

Isso possibilita adaptar o layout para diferentes dispositivos.

---

## Quando usar Media Queries

| Situação                  | Exemplo                       |
| ------------------------- | ----------------------------- |
| Alterar layout no celular | Transformar colunas em linhas |
| Diminuir fontes           | Ajustar títulos no mobile     |
| Esconder elementos        | Menu hambúrguer               |
| Reorganizar conteúdo      | Imagem acima do texto         |

---

## Exemplo de Media Query

```css
@media (max-width: 768px) {

    .menu {
        flex-direction: column;
    }

}
```

### Explicação

Se a tela tiver até 768px:

* O menu muda de linha para coluna.
* Os itens ficam empilhados.

---

## Usando Flexbox e Media Queries juntos

```css
.container {

    display: flex;

    flex-direction: row;

    gap: 20px;
}

/* Celulares */
@media (max-width: 600px) {

    .container {

        flex-direction: column;

    }

}
```

### Funcionamento

Em telas grandes:

* Os elementos ficam lado a lado.

Em telas pequenas:

* Os elementos ficam empilhados.

---

## Resumo

| Objetivo                       | Flexbox | Media Query |
| ------------------------------ | :-----: | :---------: |
| Alinhar elementos              |   Sim   |     Não     |
| Distribuir espaço              |   Sim   |     Não     |
| Alterar layout conforme a tela |   Não   |     Sim     |
| Organizar linhas e colunas     |   Sim   |   Às vezes  |
| Adaptar o site ao dispositivo  |   Não   |     Sim     |
