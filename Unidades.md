# 📏 Guia Prático de Unidades em CSS (com Exemplos)

As unidades de medida em CSS definem tamanhos como fonte, largura, altura, margem, etc. Elas se dividem em **absolutas** (fixas) e **relativas** (adaptáveis).

---

## 🔹 Unidades Absolutas

Unidades fixas, que **não se adaptam** ao tamanho da tela ou configurações do usuário.

| Unidade | Significado           |
|---------|------------------------|
| `px`    | Pixels                 |
| `cm`    | Centímetros            |
| `mm`    | Milímetros             |
| `in`    | Polegadas              |
| `pt`    | Pontos (1/72 polegada) |
| `pc`    | Picas (12 pt)          |

---

### 📌 Exemplo: `px` (pixels)

```html
<div style="width: 200px; height: 100px; background: #4caf50;">
  Caixa de 200px por 100px
</div>
````

📎 **Quando usar**:

* Ajustes finos em botões, sombras e ícones.
* Nunca em fontes ou layouts principais se quiser responsividade.

---

### 📌 Exemplo: `cm`, `in`, `pt`

```html
<div style="width: 5cm; height: 2in; background: #f44336;">
  5cm de largura e 2 polegadas de altura
</div>
```

📎 **Quando usar**:

* Arquivos para **impressão**, como currículos e etiquetas.

---

## 🔸 Unidades Relativas

Adaptam-se ao tamanho da tela, fonte, ou elemento pai. São as mais recomendadas para **layouts modernos e responsivos**.

---

### 🧠 `em` e `rem`

| Unidade | Base                     |
| ------- | ------------------------ |
| `em`    | Fonte do elemento pai    |
| `rem`   | Fonte do elemento `html` |

---

### 📌 Exemplo: `em`

```html
<div style="font-size: 20px;">
  <p style="font-size: 2em;">Este texto tem 40px</p>
</div>
```

🟢 Cresce proporcional ao pai.

---

### 📌 Exemplo: `rem`

```html
<html style="font-size: 16px;">
  <body>
    <p style="font-size: 2rem;">Este texto tem 32px</p>
  </body>
</html>
```

🟢 Sempre usa como base o tamanho da fonte do `html`.

📎 **Quando usar**:

* `rem` para tamanhos consistentes e fáceis de controlar.
* `em` para tamanhos que se adaptam ao contexto do componente.

---

### 📐 `%` (Porcentagem)

Define tamanhos **baseados no elemento pai**.

---

### 📌 Exemplo: `%`

```html
<div style="width: 300px; background: lightgray;">
  <div style="width: 50%; background: steelblue; color: white;">
    Esta div ocupa 50% da largura da anterior
  </div>
</div>
```

📎 **Quando usar**:

* Layouts fluidos
* Imagens e blocos dentro de containers

---

### 📱 `vw` e `vh` (Viewport Width/Height)

* `1vw` = 1% da largura da tela
* `1vh` = 1% da altura da tela

---

### 📌 Exemplo: `vw` e `vh`

```html
<div style="width: 100vw; height: 50vh; background: darkorange;">
  Esta caixa tem 100% da largura da tela e metade da altura
</div>
```

📎 **Quando usar**:

* Seções de tela cheia (banners, slides)
* Ajustes visuais baseados no tamanho da janela

---

### 📏 `min()`, `max()` e `clamp()`

Essas funções **combinam diferentes unidades** para definir limites.

---

### 📌 Exemplo: `clamp()`

```html
<h1 style="font-size: clamp(1rem, 5vw, 3rem);">
  Título responsivo
</h1>
```

Explicação:

* **Tamanho mínimo:** `1rem`
* **Tamanho ideal:** `5vw` (depende da largura da tela)
* **Tamanho máximo:** `3rem`

📎 **Quando usar**:

* Fontes e layouts adaptáveis
* Evitar textos muito pequenos ou grandes em diferentes telas

---

## 📊 Comparativo Resumido

| Unidade/Função | Base                  | Uso ideal                              |
| -------------- | --------------------- | -------------------------------------- |
| `px`           | Pixel fixo            | Bordas, ícones, espaçamentos finos     |
| `em`           | Fonte do pai          | Padding/margem internos ajustáveis     |
| `rem`          | Fonte do `html`       | Tipografia e layout global             |
| `%`            | Tamanho do pai        | Layouts fluidos, larguras dinâmicas    |
| `vw` / `vh`    | Janela (viewport)     | Seções de tela cheia, fontes dinâmicas |
| `clamp()`      | Combinação            | Fontes e blocos responsivos            |
| `cm`, `in`     | Tamanho real (físico) | Impressão                              |

---

## ✅ Boas práticas para escolher unidades

* Use `rem` para **fontes e espaçamentos consistentes**.
* Use `%`, `em` e `vw/vh` para **tamanhos adaptáveis e layout fluido**.
* Use `clamp()` para elementos que precisam ser **flexíveis com limites**.
* Evite `px` para tamanhos grandes (fontes, seções).
* Evite unidades físicas como `cm`, `pt` exceto em **documentos para impressão**.`
