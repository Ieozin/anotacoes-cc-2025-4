# **Tema 1 e 2: Apresentação e Teoria dos Conjuntos**

**Data:** 16/10/2025 \- 21/10/2025

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
O professor frisou pra usar ponto e vírgula ; em vez de vírgula , pra não confundir com número decimal. A ordem não importa.  
**2\. Representação Implícita (Propriedade)**

Em vez de listar, a gente descreve uma propriedade que os elementos têm em comum. O formato é:  
A \= {x | propriedade(x)}  
Lê-se como: "O conjunto de todos os 'x' **tal que** a 'propriedade de x' seja verdadeira".

### **Símbolo de Pertinência (∈)**

* ∈ significa **"pertence a"**.  
* ∉ significa **"não pertence a"**.

A analogia da sacola de compras e da caixa de ovos ajudou: se você coloca a caixa de ovos na sacola, é a *caixa* que pertence à sacola, não os ovos individualmente.

### **Relação de Inclusão (⊂ e ⊃)**

* ⊂ significa **"está contido em"**.  
* ⊃ significa **"contém"**.

Basicamente, Y ⊂ X se todos os elementos de Y também estão em X.

**Igualdade:** Dois conjuntos são iguais se um está contido no outro e vice-versa. $X \= Y \\iff (X \\subset Y \\text{ e } Y \\subset X)$.

### **O Conjunto Vazio (∅)**

É um conjunto que não tem nenhum elemento. Representado por ∅ ou {}.  
Ponto importante: O conjunto vazio é subconjunto de qualquer outro conjunto (∅ ⊂ X).

## **Continuação: Intervalos, Módulo e Operações**

**Data:** 21/10/2025

### **Intervalos na Reta Numérica e Valor Absoluto**

Essa parte entra nos conjuntos numéricos e como representá-los na reta.

**Convenção de Intervalos:**

* **Fechado (≤, ≥):** Inclui a ponta. Usa colchetes \[ \].  
* **Aberto (\<, \>):** Exclui a ponta. Usa parênteses () ou colchetes invertidos \] \[.

**Meu raciocínio:**

* \\{x \\in \\mathbb{R} \\mid a \< x \< b\\} \-\> Se o sinal é só \<, é aberto. Usa parênteses (a, b). Posso preferir só usar () por ser mais fácil.  
* \\{x \\in \\mathbb{R} \\mid a \\le x \< b\\} \-\> Se o sinal é ≤, é fechado. Usa colchete \[. Então aqui inclui o a e exclui o b, ficando \[a, b). Faz sentido.

### **Valor Absoluto (Módulo)**

Módulo (|x|) é a distância de um número x até a origem (zero). |x \- y| é a distância entre x e y.

**Exemplo do vídeo:** Resolver |x+1| \+ |x-5| \= a para a=2, 3, 1\.

* **Meu entendimento:** O professor interpretou geometricamente. |x+1| é a distância de x até \-1. |x-5| é a distância de x até 5\. A distância entre \-1 e 5 na reta é 6\. Se x está entre \-1 e 5, a soma das distâncias |x+1| \+ |x-5| será sempre 6\. Se x está fora desse intervalo, a soma será maior que 6\.  
* **Conclusão:** Para a=2, a=3 e a=1, não existe solução, porque a soma nunca será menor que 6\.

### **Operações entre Conjuntos**

* **Interseção (∩):** O que pertence aos dois conjuntos ao mesmo tempo.  
* **União (∪):** Tudo que pertence a pelo menos um dos conjuntos.  
* **Diferença (-):** O que está em um conjunto, mas não está no outro. A-B são os elementos de A que não estão em B.

### **Mão na Massa e Exercícios**

**Exemplo do vídeo:** Achar os inteiros em X \= (A ∩ B) ∪ C, com A=\[-3, 2\], B=\]-∞, 1\] e C=\[-1, 4\[.

* **Meu raciocínio:** Desenhar na reta ajuda muito.  
  * A ∩ B (interseção) é onde os dois se sobrepõem: \[-3, 1\].  
  * \[-3, 1\] ∪ C (união) é juntar tudo: \[-3, 4\[.  
* **Resultado:** Os inteiros nesse intervalo são {-3, \-2, \-1, 0, 1, 2, 3}. O 4 fica de fora porque o intervalo em C é aberto. O exercício serviu pra praticar isso de aberto/fechado.

**Outros exercícios:**

* **Questão 1:** A ∩ Q. Resposta: {1; 3; \-4; 0,111...}. Correto, π é o único não racional.  
* **Questão 2:** A={x∈Z | x²\<4} e B={x∈R | x²\<4}. Resposta: A={-1,0,1} e B=\]-2,2\[. Correto, um é só inteiros, o outro é o intervalo real.  
* **Questão 6:** Solução de |x-3|\<5. Resposta: \]-2, 8\[. Correto, são os números cuja distância até 3 é menor que 5\.

*Amanhã começo a estudar Princípios de Contagem. Acabei por hoje.*