# Tema 4: Linguagem de Marcação e Estilos (CSS)
**Data:** 22/12/2025 | **Status:** Concluído

## 1. O que é CSS?
* **Cascading Style Sheets (Folhas de Estilo em Cascata):** Define a apresentação visual (cores, layout, fontes).
* **Sintaxe:** `seletor { propriedade: valor; }`
  * Exemplo: `p { color: red; }` (Deixa todos os parágrafos vermelhos).

## 2. Formas de Uso
1.  **Inline:** Direto na tag HTML (atributo `style="..."`). *Não recomendado.*
2.  **Interno:** Dentro da tag `<style>` no `<head>`.
3.  **Externo:** Arquivo `.css` separado linkado no HTML. *Melhor prática (Cache e Organização).*

## 3. Box Model (O Modelo de Caixa)
Este é o conceito mais importante para layouts. Toda tag HTML é um retângulo composto por 4 camadas:

1.  **Content:** O conteúdo real (texto, imagem).
2.  **Padding:** Espaço interno (entre o conteúdo e a borda).
3.  **Border:** A borda em si.
4.  **Margin:** Espaço externo (distância para outros elementos).

## 4. Design Responsivo
Técnica para o site se adaptar a qualquer tamanho de tela (PC, Tablet, Celular).
* **Viewport:** A área visível do navegador.
* **Unidades Relativas:** Uso de `%`, `vw`, `vh`, `rem` em vez de pixels fixos (`px`).
* **Media Queries:** Regras condicionais baseadas na resolução.

```css
/* Exemplo de Media Query */
@media (max-width: 600px) {
    body {
        background-color: lightblue; /* Fundo muda no celular */
    }
}
```

## Resumo Rápido

**CSS** = Estilo ("A Roupa").

Externo é melhor que Inline.

**Box Model:** Margin > Border > Padding > Content.

**Responsividade:** Use % e Media Queries para adaptar ao celular.