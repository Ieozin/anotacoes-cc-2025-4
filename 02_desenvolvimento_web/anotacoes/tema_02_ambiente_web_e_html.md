# Tema 2: O Ambiente Web e Tecnologias (Fullstack)
**Data:** 05/12/2025
**Status:** Concluído

## 1. Arquitetura Cliente x Servidor
A base da web. A premissa é **separar** dados (servidor) da interface (cliente).

### Evolução das Camadas
* **2 Camadas:** Cliente (Interface + Lógica) ↔ Banco de Dados. *Problema: Difícil manutenção.*
* **3 Camadas:** Cliente ↔ Servidor de Aplicação (Regras) ↔ Banco.
* **4 Camadas (Modelo Web Atual):**
    1.  **Cliente:** Navegador (Chrome, Opera, Edge). Só exibe.
    2.  **Servidor Web:** Cuida da interface/páginas.
    3.  **Servidor de Aplicação:** Processa a regra de negócio (PHP, Java).
    4.  **Banco de Dados:** Guarda a info (MySQL, PostgreSQL).

### Ciclo de Comunicação
1.  **Request (Solicitação):** Cliente pede (ex: digita URL, clica em botão).
2.  **Response (Resposta):** Servidor processa e devolve HTML/JSON.

---

## 2. Interface e Design Responsivo
* **Interface (IHC):** Ponte entre homem e máquina. Deve ser intuitiva.
* **Design Responsivo:** O site se adapta **automaticamente** (fluido) ao tamanho da tela.
    * *Técnicas:* Layouts Fluidos (%) + Media Queries + Scripts.
* **Mobile First:** Cria p/ celular primeiro (telas pequenas/recursos limitados) e expande p/ desktop. *Melhoria progressiva.*
* **Responsivo vs. Adaptativo:**
    * *Responsivo:* Elástico (pixel a pixel).
    * *Adaptativo:* Saltos fixos (carrega layout de 360px ou de 720px).

---

## 3. Tecnologias do Lado Cliente (Frontend)
O "Tripé" que roda no navegador.

### A. HTML (HyperText Markup Language)
**Estrutura.** Não é linguagem de programação, é de **marcação**.
* **HTML5:** Foco em semântica (significado).
* **Tags Semânticas:** `<header>`, `<nav>`, `<main>`, `<footer>`. Ajudam o Google (SEO) e leitores de tela.
* **Multimídia:** Áudio e vídeo nativos (sem plugins).

### B. CSS (Cascading Style Sheets)
**Estilo/Aparência.** Cores, fontes, layout.
* **Sintaxe:** `Seletor { propriedade: valor; }`.
* **Inserção:**
    * *Inline:* `<p style="...">` (Ruim).
    * *Interno:* Tag `<style>` no head.
    * *Externo:* Arquivo `.css`. **(O ideal)**.
* **Seletores:** Tag (`p`), ID (`#nome` - único), Classe (`.box` - vários).

### C. JavaScript (JS)
**Comportamento.** Linguagem de programação do navegador.
* **Função:** Interatividade, validação de formulário, manipulação do DOM.
* **DOM:** A árvore de elementos da página. JS usa `document.getElementById('id')` para pegar e alterar elementos.
* **Eventos:** `onclick`, `onload`. Ex: Clicar num botão para trocar uma imagem (lâmpada acesa/apagada).

---

## 4. Tecnologias do Lado Servidor (Backend)
O que roda "atrás das cortinas". O usuário nunca vê esse código.

### PHP (Hypertext Preprocessor)
Linguagem de script server-side.
* **Função:** Gerar páginas **dinâmicas**. O conteúdo muda (ex: "Olá, Leonardo").
* **Sintaxe:** Código entre `<?php ... ?>`. Variáveis começam com `$` (ex: `$nome`).
* **Segurança:** O navegador recebe apenas o HTML gerado, nunca o código fonte PHP.
* **Integração:** Recebe dados de formulários via `$_POST` ou `$_GET`.

### Banco de Dados e SGBD
* **Repositório:** Onde os dados ficam salvos (ex: cadastro de usuários).
* **SGBD:** Sistema que gerencia o banco (MySQL, PostgreSQL).
* **Fluxo:** O PHP pede dados ao SGBD -> SGBD devolve -> PHP monta o HTML -> Servidor envia pro Cliente.

---

## 5. Raio-X das Questões (Baseado nos seus Erros/Acertos)
*Análise dos prints enviados:*

* **Pegadinha do HTML:** HTML **NÃO** é linguagem de programação. Não faz cálculos complexos nem lógica. É estruturação.
* **Mobile First:** A ordem é Celular -> Desktop (do menor para o maior).
* **Sintaxe PHP:** Se vir `$` na frente de variável (ex: `$v1 = 40`), é **PHP**.
* **Cliente x Servidor:** Navegadores (Opera, Chrome) são **Clientes**.
* **Acesso a Dados:** Não dá pra acessar Banco de Dados só com HTML/JS. Precisa de uma linguagem Server-Side (PHP).
* **Layout Fluido:** É a solução para adaptar sites a diversas resoluções (desktop, tablet, mobile).

---

## Resumo p/ Revisão Rápida
1.  **HTML** = Esqueleto (Semântica).
2.  **CSS** = Roupa (Estilo).
3.  **JS** = Músculos/Cérebro (Comportamento no navegador).
4.  **PHP** = Servidor (Lógica, segurança e conexão com Banco).
5.  **Responsivo** = Site elástico. **Adaptativo** = Site com tamanhos fixos.