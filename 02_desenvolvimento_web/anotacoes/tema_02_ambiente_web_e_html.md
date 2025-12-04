# Tema 2: O Ambiente Web e Tecnologias
**Data:** 04/12/2025
**Status:** Revisão

## 1. Arquitetura Cliente x Servidor
A base de como a web funciona. A premissa é separar dados (servidor) da interface (cliente).

### Evolução das Camadas
1.  **2 Camadas:** Cliente (Interface + Lógica) ↔ Banco de Dados. *Problema: Difícil atualizar a lógica em todos os clientes.*
2.  **3 Camadas:** Cliente (Interface) ↔ Servidor de Aplicação (Lógica) ↔ Banco de Dados.
3.  **4 Camadas (Modelo Web):** Cliente (Navegador) ↔ Servidor Web ↔ Servidor de Aplicação ↔ Banco de Dados.
    * **Vantagem:** O cliente não instala nada, só usa o navegador. A interface vem do servidor web.

### Ciclo de Comunicação
* **Request (Solicitação):** O cliente pede um recurso (ex: digitar URL, clicar em link).
* **Response (Resposta):** O servidor processa e devolve o HTML/JSON.

---

## 2. Interface e Design Responsivo
A interface é a ponte entre o usuário e o sistema (IHC - Interação Humano-Computador).

### Design Responsivo
O site se adapta **automaticamente** ao tamanho da tela, plataforma e orientação do dispositivo.
* **Tripé Técnico:** Layouts Fluidos (unidades flexíveis) + Media Queries (CSS condicional) + Scripts.
* **Mobile First:** Começa projetando para telas pequenas (celular) e expande para desktop (Progressive Enhancement).

### Responsivo vs. Adaptativo
* **Responsivo:** Layout fluido. Se ajusta pixel a pixel (elástico).
* **Adaptativo:** Layouts estáticos com "pontos de quebra" fixos (ex: layout p/ 360px, layout p/ 720px). Menos flexível.

---

## 3. Tecnologias do Lado Cliente (Frontend)
O que roda no navegador do usuário.

### HTML (Estrutura)
Linguagem de marcação. Define o esqueleto da página.
* **HTML5:** Foco em semântica e multimídia (áudio/vídeo nativos).
* **Tags Semânticas:** `<header>`, `<nav>`, `<main>`, `<footer>`. Ajudam o Google (SEO) a entender o conteúdo.

### CSS (Estilo)
Controla a apresentação visual (cores, fontes, layout).
* **Sintaxe:** `Seletor { propriedade: valor; }`
* **Formas de Inserção:**
    1.  **Inline:** Na tag (`style="..."`). *Evitar.*
    2.  **Interno:** Na tag `<style>` no head.
    3.  **Externo (Recomendado):** Arquivo `.css` separado. Facilita manutenção e cache.

### JavaScript (Comportamento)
Linguagem de programação interpretada pelo navegador. Adiciona interatividade.
* **Função:** Manipular o HTML/CSS em tempo real (DOM), validar formulários e criar animações sem recarregar a página.
* **Exemplo:** Clicar em um botão para acender uma lâmpada (trocar a imagem `src`).

---

## 4. Tecnologias do Lado Servidor (Backend)
O que roda no servidor e o usuário não vê.

### PHP (Hypertext Preprocessor)
Linguagem de script interpretada no servidor. Gera o HTML que é enviado pro cliente.
* **Páginas Dinâmicas:** O conteúdo muda dependendo de quem acessa (ex: "Olá, Leonardo").
* **Integração:** Conecta o HTML ao Banco de Dados.
* **Segurança:** O código fonte PHP nunca chega ao navegador, apenas o resultado (HTML).

### Banco de Dados (SGBD)
Onde as informações ficam salvas (MySQL, PostgreSQL).
* **Fluxo:** HTML (Formulário) -> PHP (Processa) -> SQL (Banco) -> PHP (Formata) -> HTML (Resposta).

---

## Resumo p/ Revisão Rápida
* **Cliente-Servidor:** Cliente pede (Request), Servidor processa e devolve (Response).
* **Responsividade:** Layout fluido + Media Queries. Prefira **Mobile First**.
* **HTML:** Estrutura semântica.
* **CSS:** Estilo. Use arquivo externo.
* **JS:** Interatividade no navegador.
* **PHP:** Lógica no servidor. Gera páginas dinâmicas e acessa o banco.