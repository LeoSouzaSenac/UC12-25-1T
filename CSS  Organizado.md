Conforme nosso projeto cresce, fica difícil manter toda estilização em um só arquivo. 
Para evitar arquivos CSS gigantescos e manter seu código bem organizado, a melhor prática é **dividir o CSS em múltiplos arquivos 
com responsabilidades específicas**.

---

### 📁 **1. Estrutura Modular**

Claro! Vamos explicar **cada arquivo CSS** de uma estrutura organizada, para que você entenda sua função e como usá-lo corretamente. Essa divisão é essencial para **evitar CSS gigantescos** e facilitar a manutenção do projeto.

---

## 📁 Estrutura Completa e Explicada

```bash
/css
  ├── reset.css
  ├── base.css
  ├── layout.css
  ├── components.css
  ├── pages/
  │    ├── home.css
  │    └── contato.css
  ├── media-queries.css
  └── main.css
```

---

### 1. `reset.css` ou `normalize.css` 🧼

**Função:** Remove os estilos padrão dos navegadores, deixando todos os elementos com um ponto de partida comum.

**Exemplo:**

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

**Por que usar?** Para garantir que seu site tenha a **mesma aparência em diferentes navegadores**.

---

### 2. `base.css` 📚

**Função:** Define os estilos globais da aplicação — cores, fontes, espaçamentos e elementos básicos.

**Inclui:**

* Tipografia padrão (fontes, tamanhos)
* Cores principais
* Estilo de links
* Estilo do `body`, `html`, títulos (`h1`, `h2`, etc.)

**Exemplo:**

```css
body {
  font-family: 'Arial', sans-serif;
  background-color: #f5f5f5;
  color: #333;
}

a {
  text-decoration: none;
  color: #0066cc;
}
```

---

### 3. `layout.css` 🧱

**Função:** Cuida da estrutura da página — **header, footer, sidebar, grid de colunas**, containers principais.

**Inclui:**

* Posições
* Tamanhos
* Flexbox ou Grid
* Espaçamento entre seções

**Exemplo:**

```css
header {
  display: flex;
  justify-content: space-between;
  padding: 20px;
}

main {
  max-width: 1200px;
  margin: 0 auto;
}
```

---

### 4. `components.css` 🧩

**Função:** Guarda os estilos reutilizáveis de **componentes pequenos** como:

* Botões
* Cards
* Formulários
* Navegação
* Ícones

**Exemplo:**

```css
.btn {
  background-color: #ff6600;
  padding: 10px 20px;
  color: white;
  border-radius: 8px;
}

.card {
  background: white;
  border: 1px solid #ddd;
  padding: 20px;
}
```

---

### 5. `pages/home.css` e `pages/contato.css` 🗂️

**Função:** Guarda estilos **específicos de cada página**, que não são reutilizados em outras partes do site.

**Exemplo (home.css):**

```css
.banner-home {
  height: 400px;
  background-image: url('banner.jpg');
  background-size: cover;
}
```

**Exemplo (contato.css):**

```css
.form-contato {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
```

---

### 6. `media-queries.css` 📱

**Função:** Define as **regras de responsividade** para diferentes tamanhos de tela.

**Inclui:**

* Ajustes para celular, tablet e desktop
* Mudança no layout (colunas viram linhas, por exemplo)

**Exemplo:**

```css
@media (max-width: 768px) {
  .menu {
    flex-direction: column;
  }

  .card {
    width: 100%;
  }
}
```

---

### 7. `main.css` 🧠 (arquivo principal)

**Função:** É o **arquivo central** que importa todos os outros. Ele organiza a ordem de carregamento dos estilos.

**Exemplo:**

```css
@import 'reset.css';
@import 'base.css';
@import 'layout.css';
@import 'components.css';
@import 'pages/home.css';
@import 'media-queries.css';
```

Esse arquivo será incluído no seu HTML:

```html
<link rel="stylesheet" href="css/main.css">
```

---

## ✅ Vantagens dessa Organização

| Vantagem             | Explicação                                                  |
| -------------------- | ----------------------------------------------------------- |
| 🔍 Fácil manutenção  | Você sabe exatamente onde está o estilo que precisa alterar |
| 📦 Reutilização      | Componentes podem ser usados em várias páginas              |
| 📄 Código mais limpo | Evita arquivos gigantescos e desorganizados                 |
| 📐 Escalabilidade    | Fica mais fácil trabalhar em equipe ou crescer o projeto    |


---
## reset.css

O arquivo **`reset.css`** serve para **“zerar” ou “normalizar”** os estilos padrões que cada navegador aplica aos elementos HTML. 
Isso ajuda a evitar diferenças visuais entre navegadores diferentes (Chrome, Firefox, Edge, Safari etc).

---

## O que geralmente vai no `reset.css`?

### 1. Remover margens e paddings padrões

Muitos navegadores aplicam margens e espaçamentos padrão em elementos como `<body>`, `<h1>`, `<p>`, `<ul>`, etc.

```css
* {
  margin: 0;
  padding: 0;
}
```

---

### 2. Definir o `box-sizing` para todos os elementos

O `box-sizing: border-box;` faz com que o padding e a borda sejam incluídos na largura e altura do elemento — isso facilita o controle de layouts.

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
```

---

### 3. Remover estilos de listas (quando não forem usados)

```css
ul,
ol {
  list-style: none;
}
```

---

### 4. Resetar bordas, fontes e cores padrões de elementos básicos

```css
img,
video,
canvas,
svg {
  display: block;
  max-width: 100%;
  height: auto;
  border: 0;
}

a {
  text-decoration: none;
  color: inherit; /*  faz o elemento herdar o valor da propriedade do seu elemento pai. */
}
```

---

### 5. Resetar botões, inputs e formulários

```css
button,
input,
select,
textarea {
  background: none;
  border: none;
  outline: none;
  font: inherit;
  color: inherit;
}
```

---

### 6. Resetar tabelas

```css
table {
  border-collapse: collapse;
  border-spacing: 0;
}
```

---

## 📚 O que é o `base.css`?

O arquivo `base.css` contém os **estilos globais básicos da aplicação** — aquelas definições que vão servir de base para todos os elementos do seu site.

Ele fica logo após o `reset.css` (que "zera" os estilos padrões do navegador) e antes dos estilos mais específicos (layout, componentes, páginas).

---

## ✍️ O que colocar no `base.css`?

### 1. Tipografia global

Definir fontes, tamanhos, pesos e cores padrão para texto, títulos, links.

```css
body {
  font-family: 'Arial', sans-serif;
  font-size: 16px;
  line-height: 1.5;
  color: #333;
  background-color: #fff;
}
```

---

### 2. Estilos para elementos básicos

Configurar aparência de tags comuns, como:

* Parágrafos `<p>`
* Títulos `<h1>`, `<h2>`, ..., `<h6>`
* Links `<a>`
* Listas `<ul>`, `<ol>`, `<li>`
* Imagens `<img>`

Exemplo:

```css
h1, h2, h3, h4, h5, h6 {
  font-weight: 600;
  color: #222;
}

a {
  color: #007bff;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

p {
  margin-bottom: 1em;
}
```

---

### 3. Definições de cores e variáveis CSS (se usar)

Se usar CSS custom properties, pode definir cores base, por exemplo:

```css
:root {
  --cor-primaria: #ff6600;
  --cor-secundaria: #333333;
  --cor-fundo: #f5f5f5;
  --font-base: 'Arial', sans-serif;
}
```

---

### 4. Estilos para formulários básicos

Inputs, botões, labels, etc.

```css
input, button, select, textarea {
  font-family: inherit;
  font-size: 1em;
  margin: 0;
}
```

---

### 5. Pequenas regras para melhorar acessibilidade e usabilidade

```css
button {
  cursor: pointer;
}

img {
  max-width: 100%;
  height: auto;
}
```

---

## 💡 Resumo rápido

| O que vai no `base.css`          | Por quê?                         |
| -------------------------------- | -------------------------------- |
| Tipografia geral (fontes, cores) | Para padronizar texto            |
| Estilos para tags HTML comuns    | Para ter aparência consistente   |
| Variáveis CSS (cores, fontes)    | Facilita manutenção              |
| Estilos básicos de formulário    | Uniformizar inputs e botões      |
| Melhorias de usabilidade         | Melhora a experiência do usuário |

---


## 🧱 `layout.css` — Estilos estruturais da página

### 📌 O que é?

Esse arquivo define o **esqueleto geral do site**, ou seja, como os blocos maiores se organizam: `header`, `footer`, `main`, `container`, `sidebar`, etc.

### ✅ O que normalmente vai aqui:

* Tamanhos e posicionamento de containers
* Definição de `header`, `main`, `footer`, `section`
* Layout com `flexbox` ou `grid`
* Espaçamentos entre as grandes seções

### 🧪 Exemplo:

```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: var(--cor-primaria);
  color: white;
}

footer {
  background-color: var(--cor-secundaria);
  color: white;
  padding: 20px;
  text-align: center;
}
```

---

## 🧩 `components.css` — Estilos de componentes reutilizáveis

### 📌 O que é?

Aqui ficam **peças pequenas e reutilizáveis** da interface, como botões, cards, formulários, campos de input, alertas, menus, etc.

### ✅ O que normalmente vai aqui:

* `.btn` (botão padrão)
* `.card` (caixa de conteúdo com sombra)
* `.form-control`, `.input-group`
* `.menu`, `.badge`, `.alert`, etc.

### 🧪 Exemplo:

```css
.btn {
  background-color: var(--cor-primaria);
  color: white;
  padding: 10px 20px;
  border-radius: 6px;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn:hover {
  background-color: #cc5200;
}

.card {
  background-color: white;
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}
```

---

## 🏠 `pages/home.css` — Estilos específicos da página inicial

### 📌 O que é?

Esse arquivo serve para guardar estilos **exclusivos da página inicial** (`index.html`), que não fazem sentido em outras páginas.

### ✅ O que normalmente vai aqui:

* Banner da página inicial
* Destaques ou seções exclusivas da home
* Layouts ou estilos de promoções e sliders

### 🧪 Exemplo:

```css
.banner-home {
  background-image: url('../img/banner.jpg');
  background-size: cover;
  background-position: center;
  height: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.5);
}

.destaque-home {
  margin-top: 40px;
  text-align: center;
}
```

---

## 📞 `pages/contato.css` — Estilos específicos da página de contato

### 📌 O que é?

Aqui você coloca tudo que for **exclusivo da página de contato**, como o formulário, mapa, título da seção, etc.

### ✅ O que normalmente vai aqui:

* Formulário de contato (inputs, textarea, botão)
* Estilo para o mapa
* Layout da seção de contato

### 🧪 Exemplo:

```css
.form-contato {
  max-width: 600px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.form-contato input,
.form-contato textarea {
  border: 1px solid #ccc;
  padding: 10px;
  border-radius: 5px;
  font-family: inherit;
}

.form-contato button {
  background-color: var(--cor-primaria);
  color: white;
  padding: 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
```

---

## 🧠 `main.css` — Arquivo principal que importa todos os outros

### 📌 O que é?

Esse arquivo **não contém estilos diretos**. Ele serve apenas para **importar os outros arquivos CSS em ordem**, como se fosse o "gerente" dos estilos do site.

### ✅ O que normalmente vai aqui:

```css
@import 'reset.css';
@import 'base.css';
@import 'layout.css';
@import 'components.css';
@import 'pages/home.css';
@import 'pages/contato.css';
```

Esse arquivo deve ser o **único linkado no seu HTML**:

```html
<link rel="stylesheet" href="css/main.css">
```

---

## ✅ Resumo final

| Arquivo             | Serve para...                                    |
| ------------------- | ------------------------------------------------ |
| `layout.css`        | Estrutura geral do site (header, footer, etc.)   |
| `components.css`    | Peças reutilizáveis (botões, cards, formulários) |
| `pages/home.css`    | Estilos exclusivos da página inicial             |
| `pages/contato.css` | Estilos exclusivos da página de contato          |
| `main.css`          | Importa e organiza todos os arquivos acima       |

---
