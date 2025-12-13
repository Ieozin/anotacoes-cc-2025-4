# Temas 1 e 2: Apresentação e Ambiente Web (Fullstack)
**Data:** 12/12/2025
**Status:** Concluído

## 1. Visão Geral da Disciplina (Tema 1)
O objetivo é entender os bastidores da web para criar aplicações rápidas, interativas e seguras (e-commerce, sistemas, portais).

### O "Tripé" do Desenvolvimento
A disciplina cobre a stack completa:
* **Frontend:** O que o usuário vê (HTML, CSS, JS).
* **Backend:** O que processa os dados (PHP).
* **Persistência:** Onde guardamos os dados (Banco de Dados).

---

## 2. Arquitetura Cliente x Servidor (Tema 2)
A premissa básica da web: separar quem pede (interface) de quem processa (dados).

### As 4 Camadas do Modelo Web
1.  **Cliente:** Navegador (Chrome, Edge). Só exibe a interface.
2.  **Servidor Web:** Entrega as páginas.
3.  **Servidor de Aplicação:** Processa a regra de negócio (PHP).
4.  **Banco de Dados:** Guarda a informação (MySQL).

### Ciclo de Vida
* **Request (Solicitação):** Cliente clica/digita URL.
* **Response (Resposta):** Servidor devolve HTML/JSON.

---

## 3. Interface e Design Responsivo
* **Interface (IHC):** Ponte homem-máquina. Foco em usabilidade.
* **Design Responsivo:** Site elástico. Se adapta pixel a pixel a qualquer tela.
    * *Técnica:* Layout Fluido (%) + Media Queries.
* **Mobile First:** Começar desenhando para celular (telas pequenas) e expandir para desktop.

### Responsivo vs. Adaptativo
* **Responsivo:** Fluido/Líquido. (Moderno).
* **Adaptativo:** Saltos fixos (Breakpoints de 360px, 720px, etc). (Legado).

---

## 4. Tecnologias do Lado Cliente (Frontend)
O que roda no navegador.

### A. HTML (Estrutura)
* **Função:** Marcação e Semântica (Esqueleto).
* **HTML5:** Trouxe tags semânticas (`<header>`, `<nav>`) e multimídia nativa.
* **Atenção:** HTML **não** é linguagem de programação.

### B. CSS (Estilo)
* **Função:** Visual e Layout (Roupa).
* **Sintaxe:** `Seletor { propriedade: valor; }`.
* **Dica:** Sempre usar arquivo externo (`.css`) para cache e organização.

### C. JavaScript (Comportamento)
* **Função:** Interatividade e Lógica no navegador (Cérebro).
* **DOM:** A árvore de elementos que o JS manipula em tempo real (ex: `document.getElementById`).
* **Eventos:** Cliques, mouseover, carregamento.

---

## 5. Tecnologias do Lado Servidor (Backend)
O que o usuário não vê.

### PHP (Hypertext Preprocessor)
* **Função:** Gerar páginas **dinâmicas** (conteúdo personalizado).
* **Segurança:** O código fonte nunca vai para o navegador, apenas o HTML gerado.
* **Variáveis:** Começam com `$` (ex: `$nome`).

### Banco de Dados (SGBD)
* **Função:** Armazenamento persistente.
* **Integração:** O PHP conecta no banco, pega os dados e monta a página.

---

## Resumo p/ Revisão Rápida
* **Mobile First:** Ordem de criação = Celular -> Desktop.
* **Responsivo:** Unidades fluidas (%). **Adaptativo:** Unidades fixas (px).
* **HTML** = Estrutura | **CSS** = Estilo | **JS** = Comportamento | **PHP** = Dinamismo.
* **Acesso a Dados:** Só é possível com linguagem Server-Side (PHP), nunca só com HTML/JS.