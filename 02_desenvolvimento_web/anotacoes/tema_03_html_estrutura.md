# **Tema 3: Linguagem de Marcação (HTML)**

**Data:** 15/12/2025 | **Status:** Concluído

## **1\. Introdução e Ferramentas**

HTML (HyperText Markup Language) **não é linguagem de programação**. É uma linguagem de marcação baseada em tags.

- **Objetivo:** Estruturar o conteúdo ("esqueleto" da página).
- **Origem:** Criado por Tim Berners-Lee (1991).
- **Ferramentas:** Editores simples (Notepad++, Nano, VS Code) são ideais para aprendizado.

## **2\. O Doctype**

Instrução inicial para o navegador identificar a versão do HTML. Não é uma tag.

- **HTML 5:** Simplificada: \<\!DOCTYPE html\>.

## **3\. Estrutura Hierárquica**

O HTML funciona com elementos aninhados (Pai \> Filho).

### **Boilerplate (Estrutura Obrigatória)**

\<\!DOCTYPE html\>  
\<html lang="pt-br"\>  
 \<head\>  
 \<meta charset="UTF-8"\>  
 \<title\>Aba do Navegador\</title\>  
 \</head\>  
 \<body\>  
 \<h1\>Título Principal\</h1\>  
 \<p\>Um parágrafo de texto.\</p\>  
 \</body\>  
\</html\>

**Ponto de Atenção:** Se remover a tag \<head\>, a página continua funcionando (o navegador corrige), mas o documento torna-se tecnicamente inválido (W3C).

## **4\. Semântica (HTML5)**

Uso de tags pelo significado, não pela aparência. Essencial para SEO (Google) e Acessibilidade.

### **Tags Estruturais**

- \<header\>: Cabeçalho.
- \<nav\>: Menu.
- \<main\>: Conteúdo principal.
- \<section\>: Seção temática.
- \<article\>: Conteúdo independente.
- \<footer\>: Rodapé.
- \<div\> / \<span\>: Genéricas (layout/estilo).

## **5\. Tags de Texto: Visual vs Semântico**

| Tag Visual (Evitar) | Tag Semântica (Usar) | Efeito  | Significado Real      |
| :------------------ | :------------------- | :------ | :-------------------- |
| \<b\> (Bold)        | \<strong\>           | Negrito | Importância/Urgência. |
| \<i\> (Italic)      | \<em\> (Emphasis)    | Itálico | Ênfase na entonação.  |

**Raio-X da Questão (Acessibilidade):** Leitores de tela (para deficientes visuais) mudam a entonação de voz ao ler \<strong\>, dando ênfase real. A tag \<b\> é ignorada pelo leitor, servindo apenas para estética. Sempre prefira \<strong\>.

## **6\. Prática: Tags Básicas e Separadores**

Exemplo prático de estrutura com títulos, parágrafos e linha horizontal.

\<body\>  
 \<h1\>Primeiro título\</h1\>  
 \<p\>  
 Lorem ipsum dolor sit amet. Este é um parágrafo contendo texto  
 dentro da tag P, que é a semanticamente correta para blocos de texto.  
 \</p\>

    \<hr/\>

    \<h2\>Subtítulo\</h2\>
    \<p\>
        Novo bloco de texto após a separação.
    \</p\>

\</body\>

- \<hr/\>: Tag "vazia" (não tem conteúdo dentro). Serve para quebra temática visual (linha horizontal).

## **7\. Tags Obsoletas (Descontinuadas)**

Substituídas pelo CSS. Não utilizar:  
\<center\>, \<font\>, \<applet\>, \<dir\>.

# **Resumo p/ Revisão Rápida**

- HTML \= Estrutura | CSS \= Estilo.
- Hierarquia: \<html\> \> \<head\> \> \<body\>.
- Semântica: Priorizar \<strong\> em vez de \<b\> para garantir acessibilidade em leitores de tela.
- Tags de Bloco: \<h1\>, \<p\>, \<hr\>, \<div\> (Ocupam a largura toda).
- Atributos Globais: id (único) e class (grupo).
