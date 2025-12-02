# Tema 2: Interface Web, Design Responsivo e HTML
**Data:** 02/12
**Status:** Concluído

## 1. Conceito de Interface (IHC)
A ponte entre o usuário e o sistema.
* **Foco:** Usabilidade e Clareza. O usuário não técnico tem q conseguir usar sem sofrer.
* **Evolução:** * Linha de comando (CLI) -> Interface Gráfica (GUI) -> Interfaces Naturais/Toque.
* **Mudança de Paradigma:** Antigamente o usuário se adaptava ao hardware. Hoje (com smartphones/tablets), a interface tem q se adaptar ao dispositivo.

## 2. Design Responsivo
É a capacidade da página se adaptar **automaticamente** ao tamanho da tela, orientação e plataforma.
* **Origem:** Arquitetura responsiva (salas q mudam conforme o fluxo de pessoas).
* **Objetivo:** Evitar criar um site diferente para cada dispositivo (m.site.com). Um código único serve p/ todos.

### O "Tripé" do Responsivo
Para funcionar, usamos 3 técnicas juntas:
1. **Layouts Fluidos:** As larguras não são fixas. O conteúdo estica ou encolhe.
2. **Media Queries:** O CSS aplica regras diferentes dependendo da condição (ex: `se largura < 600px`).
3. **Scripts (JS):** Para interações dinâmicas e ajustes de conteúdo.

### Unidades de Medida (CSS)
Isso cai muito em questão técnica. Diferença entre fixo e relativo:
* **PX (Pixel):** Fixo. Ruim p/ responsivo.
* **% (Porcentagem):** Fluido.
* **EM:** Relativo ao tamanho da fonte do elemento **pai**.
* **REM (Root EM):** Relativo ao tamanho da fonte do elemento **raiz** (`html`). *Mais previsível q o EM.*

---

## 3. Responsivo vs. Adaptativo
Parecem iguais, mas a lógica interna é diferente.

| Característica | Design Responsivo | Design Adaptativo |
| :--- | :--- | :--- |
| **Layout** | Fluido / Líquido | Estático (com "saltos") |
| **Técnica** | Se ajusta pixel a pixel | Usa "Breakpoints" fixos |
| **Flexibilidade** | Alta (qualquer tela) | Média (telas predefinidas) |
| **Complexidade** | Mais difícil de codar | Mais trabalhoso (vários layouts) |

> **Ponto de Atenção:** No adaptativo, se a tela tiver 700px e o breakpoint for 720px, ele pode carregar o layout de 360px (perde espaço). O responsivo aproveitaria os 700px totais.

---

## 4. Mobile First
Abordagem de desenvolvimento moderna.
* **Lógica:** Cria primeiro p/ celular (telas pequenas, internet lenta, toque) e depois expande p/ desktop.
* **Progressive Enhancement:** Começa simples e adiciona recursos (melhoria progressiva).
* **Graceful Degradation:** (Oposto/Antigo) Cria p/ desktop e vai "capando" recursos p/ funcionar no mobile.

---

## 5. HTML (HyperText Markup Language)
A estrutura da página (o esqueleto/vigas). Não é programação, é **marcação**.
* **Analogia:** HTML = Estrutura (Vigas/Paredes) | CSS = Acabamento (Pintura/Decoração).
* **Estrutura Base:** `<!DOCTYPE html>`, `html`, `head` (metadados), `body` (o q aparece na tela).

### HTML5 e Semântica
As tags agora têm significado (semântica), não servem só p/ formatar. Isso ajuda o Google (SEO) e leitores de tela (acessibilidade).

**Tags Estruturais Essenciais:**
* `<header>`: Cabeçalho (logo, busca).
* `<nav>`: Menu de navegação.
* `<main>`: Conteúdo principal.
* `<section>`: Agrupamento temático de conteúdo.
* `<article>`: Conteúdo independente (ex: post de blog).
* `<footer>`: Rodapé.

---

## Resumo p/ Revisão Rápida
* **Responsivo:** Usa fluid grid + media queries. É elástico.
* **Adaptativo:** Usa layouts fixos baseados em breakpoints. É estático em blocos.
* **Unidades:** Prefira **REM** ou **%** para layouts modernos. Evite **PX** para containers.
* **Mobile First:** Começa pequeno e expande (Progressive Enhancement).
* **HTML Semântico:** Usar `<nav>` e `<header>` é melhor q usar `<div>` pra tudo.