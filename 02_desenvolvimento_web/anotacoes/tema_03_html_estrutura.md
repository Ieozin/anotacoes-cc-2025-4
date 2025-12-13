# **Tema 3: Linguagem de Marcação (HTML)**

**Data:** 12/12/2025 | **Status:** Concluído

## **1\. Introdução e Ferramentas**

HTML (HyperText Markup Language) **não é linguagem de programação**. É uma linguagem de marcação baseada em tags.

* **Objetivo:** Estruturar o conteúdo ("esqueleto" da página).  
* **Origem:** Criado por Tim Berners-Lee (1991). Baseado no SGML.  
* **Ferramentas:** Editores simples (Notepad++, Nano, VS Code) são ideais para aprendizado.

## **2\. O Doctype**

Instrução inicial para o navegador identificar a versão do HTML. Não é uma tag.

* **HTML 4:** Baseada em SGML, longa e complexa.  
* **HTML 5:** Simplificada: \<\!DOCTYPE html\>.

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

**Ponto de Atenção:** Se remover a tag \<head\>, a página continua funcionando pois os navegadores modernos corrigem o erro automaticamente, mas o documento torna-se tecnicamente inválido (W3C).

## **4\. Semântica (HTML5)**

Uso de tags pelo significado, não pela aparência. Essencial para SEO (Google) e Acessibilidade (Leitores de tela).

### **Tags Estruturais**

* \<header\>: Cabeçalho (Logo, busca).  
* \<nav\>: Menu de links.  
* \<main\>: Conteúdo principal (único por página).  
* \<section\>: Seção temática.  
* \<article\>: Conteúdo independente.  
* \<aside\>: Barra lateral.  
* \<footer\>: Rodapé.  
* \<div\> / \<span\>: Genéricas (sem significado, usadas para layout/estilo).

## **5\. Tags de Texto: Visual vs Semântico**

| Tag Visual (Evitar) | Tag Semântica (Usar) | Efeito | Significado Real |
| :---- | :---- | :---- | :---- |
| \<b\> (Bold) | \<strong\> | Negrito | Importância/Urgência. |
| \<i\> (Italic) | \<em\> (Emphasis) | Itálico | Ênfase na entonação. |

