# Tema 5: Linguagem JavaScript
**Data:** 22/12/2025 | **Status:** Concluído

## 1. Características Principais
* **Definição:** Linguagem de script **Client-Side** (roda no navegador do usuário).
* **Objetivo:** Adicionar **interatividade** (validar formulários, animações, botões, pop-ups).
* **Case-sensitive:** Diferencia letras maiúsculas de minúsculas (`Var` é diferente de `var`).

## 2. DOM (Document Object Model)
O DOM é a representação da página na memória do navegador. É uma "árvore" de elementos que o JavaScript pode manipular.

* **O que o JS faz com o DOM?**
  * Altera textos e cores em tempo real.
  * Cria ou remove elementos HTML.
  * Reage a ações do usuário.

**Seletores Principais:**
* `document.getElementById('meuId')`: Busca elemento pelo ID.
* `document.querySelector('.minhaClasse')`: Busca o primeiro elemento que usa essa classe.

## 3. Eventos
São "gatilhos" que disparam códigos JavaScript.

* `onclick`: Quando o usuário clica em algo.
* `onload`: Quando a página termina de carregar.
* `oninput`: Quando o usuário digita em um campo.
* `onmouseover`: Quando o mouse passa por cima.

## 4. Sintaxe Básica

```javascript
// 1. Variáveis
let nome = "Leonardo";  // Texto (String)
const pi = 3.14;        // Constante (Número)

// 2. Função (Um bloco de código reutilizável)
function saudar() {
    alert("Olá, " + nome);
}

// 3. Condicional (Tomada de decisão)
if (pi > 3) {
    console.log("A matemática está correta.");
}
```

## Resumo Rápido
HTML = Estrutura. CSS = Estilo. JS = Comportamento.

DOM: É a ponte entre o HTML e o JavaScript.

Eventos: Permitem que a página reaja ao usuário (cliques, teclado).