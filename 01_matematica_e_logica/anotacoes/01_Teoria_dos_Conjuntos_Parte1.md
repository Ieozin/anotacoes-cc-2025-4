# **Tema 1 e 2: Apresentação e Teoria dos Conjuntos (Parte 1\)**

**Data:** 16/10/2025

## **Apresentação da Disciplina**

Comecei vendo o vídeo de apresentação. Deu pra ver que matemática e lógica não é só coisa de escola, é a base pra muita coisa que eu quero fazer, tipo programação e IA. É a fundação da casa, como dizem. Sem isso, o resto não para em pé.

Os tópicos que vou ter que encarar são:

* Teoria dos conjuntos e princípios de contagem  
* Gráficos e interpretações  
* Aprofundamento de funções  
* Cálculo proposicional  
* Cálculo de predicados  
* Métodos de demonstração

## **Teoria dos Conjuntos \- O Básico**

A matéria começou com o básico do básico: o que é um conjunto e como escrever isso direito.

### **Como Representar um Conjunto**

Existem duas formas principais:

**1\. Representação Explícita (Enumeração)**

É a forma mais direta: simplesmente listar os elementos entre chaves {}.  
O professor frisou pra usar ponto e vírgula ; em vez de vírgula , pra não confundir com número decimal, já que a gente usa vírgula pra isso em português.  
**Exemplos:**

// Conjunto de ímpares entre 0 e 10\. A ordem não importa.  
B \= { 1; 3; 9; 7; 5 }

// Conjunto infinito (os "..." indicam que continua).  
D \= { 1; 4; 9; 16; 25; 36; ... }

**2\. Representação Implícita (Propriedade)**

Em vez de listar, a gente descreve uma propriedade que os elementos têm em comum. O formato é:  
A \= {x | propriedade(x)}  
Lê-se como: "O conjunto de todos os 'x' **tal que** a 'propriedade de x' seja verdadeira".

**Exemplos:**

// O conjunto dos 'x' tal que x ao quadrado é igual a 9\.  
// Ou seja, {3; \-3}.  
F \= { x | x² \= 9 }

// O conjunto dos 'x' que pertencem aos inteiros (Z) tal que x ao quadrado é menor que 9\.  
// Ou seja, {-2; \-1; 0; 1; 2}.  
G \= { x ∈ Z | x² \< 9 }

### **Símbolo de Pertinência (∈)**

* ∈ significa **"pertence a"**.  
* ∉ significa **"não pertence a"**.

Gostei da analogia da sacola de compras e da caixa de ovos: se você coloca a caixa de ovos na sacola, é a *caixa* que pertence à sacola, não os ovos individualmente.

**Exemplo:** A \= { 1; 2; {3, 4}; 5; 6 }

* 1 ∈ A (Verdadeiro)  
* 3 ∉ A (Verdadeiro, porque o 3 está "dentro da caixa")  
* {3, 4} ∈ A (Verdadeiro, a "caixa" pertence ao conjunto)

### **Relação de Inclusão (⊂)**

* ⊂ significa **"está contido em"**.  
* ⊃ significa **"contém"**.

Basicamente, se todos os elementos de um conjunto Y também estão no conjunto X, então Y está contido em X (Y ⊂ X). A barra "/" no símbolo nega a relação, como em ≠.

### **O Conjunto Vazio (∅)**

É um conjunto que não tem nenhum elemento. Pode ser representado por ∅ ou {}.

**Ponto importante:** O conjunto vazio é subconjunto de qualquer outro conjunto (∅ ⊂ X).