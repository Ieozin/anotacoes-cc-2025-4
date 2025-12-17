# **Tema 3: Linguagem de Marcação (HTML)**

**Data:** 17/12/2025 | **Status:** Concluído

## **1\. Introdução e Ferramentas**

HTML (HyperText Markup Language) **não é linguagem de programação**. É uma linguagem de marcação baseada em tags.

* **Objetivo:** Estruturar o conteúdo ("esqueleto" da página).  
* **Origem:** Criado por Tim Berners-Lee (1991).  
* **Ferramentas:** Editores simples (Notepad++, VS Code).

## **2\. O Doctype**

Instrução inicial para o navegador identificar a versão do HTML.

* **HTML 5:** Simplificada: \<\!DOCTYPE html\>.

## **3\. Estrutura Hierárquica**

### **Boilerplate (Estrutura Obrigatória)**

\<\!DOCTYPE html\>  
\<html lang="pt-br"\>  
    \<head\>  
        \<meta charset="UTF-8"\>  
        \<title\>Minha Página\</title\>  
    \</head\>  
    \<body\>  
        \<h1\>Conteúdo aqui\</h1\>  
    \</body\>  
\</html\>

## **4\. Semântica (HTML5)**

Uso de tags pelo significado. Essencial para SEO e Acessibilidade.

* **Estruturais:** \<header\>, \<nav\>, \<main\>, \<section\>, \<article\>, \<footer\>.  
* **Genéricas:** \<div\> (bloco), \<span\> (linha).

## **5\. Tags de Texto e Listas**

| Tag | Função |
| :---- | :---- |
| \<strong\> | Negrito com semântica de importância. |
| \<em\> | Itálico com semântica de ênfase. |
| \<p\> | Parágrafos de texto. |
| \<br\> | Quebra de linha simples. |
| \<hr\> | Linha horizontal (separação temática). |

### **Listas**

Organizam itens.

* **Não Ordenada (\<ul\>):** Marcadores (bolinhas). Itens dentro de \<li\>.  
* **Ordenada (\<ol\>):** Números (1, 2, 3). Itens dentro de \<li\>.  
* **Definição (\<dl\>):** Termos \<dt\> e descrições \<dd\>.

## **6\. Tabelas**

Usadas para dados tabulares, não para layout.

* \<table\>: Container.  
* \<tr\>: Linha (Row).  
* \<th\>: Cabeçalho (Header) \- Negrito e centralizado.  
* \<td\>: Dado (Data).

## **7\. Multimídia e Links**

* **Imagens (\<img\>):** Tag vazia. Atributos: src (caminho), alt (texto alternativo).  
* **Links (\<a\>):** Atributos: href (destino), target="\_blank" (nova aba).

## **8\. Formulários (Interação)**

Permitem enviar dados para o servidor.

* \<form\>: Container (action, method).  
* \<label\>: Rótulo (melhora usabilidade).  
* \<input\>: Campos (type="text", "email", "password", "date").  
* \<textarea\>: Texto longo.  
* \<button\>: Botão de envio.

### **Validação Nativa**

* required: Campo obrigatório.  
* placeholder: Dica visual.  
* min / max: Limites numéricos.