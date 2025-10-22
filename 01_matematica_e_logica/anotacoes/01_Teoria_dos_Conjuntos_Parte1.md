# **Tema 2: Princípios de Contagem e Agrupamento Simples**

**Data:** 22/10/2025

## **Princípios Básicos da Contagem**

Hoje o foco foi em como contar possibilidades.

### **1\. Princípio da Casa dos Pombos (ou Gavetas)**

* **Ideia:** Se tem mais objetos (n) do que recipientes (m), pelo menos um recipiente terá mais de um objeto (n \> m). Parece óbvio, mas resolve uns problemas complicados.  
* **Exemplo (Fios de Cabelo):** Numa cidade de 1 milhão de pessoas (n=1.000.000), ninguém tem mais de 200.000 fios (m=200.000). Como n \> m, pelo menos duas pessoas têm o mesmo número de fios. Faz sentido.  
* **Exemplo (Números Inteiros):** Dados 12 inteiros (n=12), os restos da divisão por 11 só podem ser 0 a 10 (m=11). Como n \> m, pelo menos dois números terão o mesmo resto. A diferença entre eles terá resto zero, ou seja, é divisível por 11\.

### **2\. Princípio da Adição**

* **Ideia:** Contar elementos na união de conjuntos (A ∪ B).  
* **Com Interseção (A ∩ B ≠ ∅):** Soma tudo e subtrai a interseção pra não contar duas vezes: n(A ∪ B) \= n(A) \+ n(B) \- n(A ∩ B).  
* **Sem Interseção (A ∩ B \= ∅, disjuntos):** Só somar: n(A ∪ B) \= n(A) \+ n(B).

### **3\. Princípio da Multiplicação**

* **Ideia:** Se uma tarefa tem k etapas e a etapa i tem n\_i opções, o total de maneiras é n\_1 \* n\_2 \* ... \* n\_k. É o mais usado na prática.  
* **Exemplo (Árvore de Decisão):** Contar números de 2 dígitos distintos com {1, 2, 3, 4}.  
  * 1ª decisão (dezena): 4 opções.  
  * 2ª decisão (unidade): 3 opções restantes (não pode repetir).  
  * Total: 4 \* 3 \= 12 números.

**Notação Fatorial:** n\! \= n \* (n-1) \* ... \* 1\. (Lembrar: 0\! \= 1). Útil pra simplificar as contas. Ex: $10 \\times 11 \\times ... \\times 14 \= \\frac{14\!}{9\!}$.

## **Agrupamento Simples (Sem Repetição)**

Aqui entram os nomes formais: Arranjo, Permutação, Combinação. A chave é saber se a ordem dos elementos importa ou não.

**Situações:**

* **Ordem Importa:** Arranjo ou Permutação (senhas, filas, anagramas, cargos diferentes).  
* **Ordem NÃO Importa:** Combinação (comissões sem cargos, subconjuntos, escolher itens).

### **1\. Arranjo Simples (A^n\_p)**

* **O que é:** Escolher p objetos de n disponíveis, **onde a ordem importa**.  
* **Como calcular:** Multiplicar p termos decrescentes a partir de n.  
  * Fórmula: $A^n\_p \= \\frac{n\!}{(n-p)\!}$  
* **Exemplo (Filas):** Fazer filas de 5 alunos com 12 disponíveis. Ordem importa. A^{12}\_5 \= 12 \* 11 \* 10 \* 9 \* 8 \= 95040\.

### **2\. Permutação Simples (P\_n)**

* **O que é:** Um Arranjo onde usamos **todos** os n objetos (p=n). Basicamente, embaralhar n objetos distintos.  
* **Como calcular:** P\_n \= n\!  
* **Exemplo (Anagramas):** Anagramas de "trapo" (5 letras distintas) \= $P\_5 \= 5\! \= 120$.

### **3\. Combinação Simples (C^n\_p ou \\binom{n}{p})**

* **O que é:** Escolher p objetos de n disponíveis, **onde a ordem NÃO importa**.  
* **Raciocínio:** Calcula o número de Arranjos (A^n\_p) e divide pelas permutações dos p escolhidos (p\!), pra descontar as repetições onde só muda a ordem.  
* **Como calcular:** $C^n\_p \= \\frac{A^n\_p}{p\!} \= \\frac{n\!}{p\!(n-p)\!}$  
* **Exemplo (Comissão sem cargos):** Formar comissão de 3 com 8 pessoas. Ordem não importa. $C^8\_3 \= \\frac{A^8\_3}{3\!} \= \\frac{8 \\times 7 \\times 6}{3 \\times 2 \\times 1} \= 56$.  
* **Exemplo (Subconjuntos):** Subconjuntos de 3 elementos de um conjunto com 7\. Ordem não importa. $C^7\_3 \= \\frac{7\!}{3\!4\!} \= 35$.

## **Exercícios (Mão na Massa / Verificando Aprendizado)**

* **Q1 (Bolas):** Mínimo para garantir 2 azuis (20A, 30V). Pior caso: 30V \+ 2A \= 32\. (Casa dos Pombos). (Ok)  
* **Q2 (Anagrama "Alfredo"):** 7 letras distintas. $P\_7 \= 7\!$. (Permutação). (Ok)  
* **Q3 (Placas 2L+4N distintos):** (26\*25) \* (10\*9\*8\*7). (Multiplicação). (Ok)  
* **Q4 (Pares 4 alg distintos 1-8):** Fixa unidade par (4 op), depois preenche o resto. 4\*7\*6\*5 \= 840\. (Multiplicação com restrição). (Ok)  
* **Q6 (Subconjuntos {a..g} sem a,b com f,g):** Resta decidir sobre c,d,e (inclui/não inclui). 2\*2\*2 \= 8\. (Multiplicação). (Ok)  
* **Verif. Q1 (Senhas 4 a 6 alg distintos 0-9):** Calcular A(10,4) \+ A(10,5) \+ A(10,6) \= 5040 \+ 30240 \+ 151200 \= 186480\. (Arranjo \+ Adição). (Ok)  
* **Verif. Q2 (Subconjuntos {1,3,5,7,9} com 3 elem sem o 5):** Tira o 5, sobram {1,3,7,9}. Escolher 3 desses 4\. Ordem não importa. $C^4\_3 \= \\frac{4\!}{3\!1\!} \= 4$. Ops, a resposta do PDF diz 6 (C^4\_2). Revendo: "subconjuntos com 3 elementos". Se não pode o 5, escolho 3 dos outros 4\. $C^4\_3 \= 4$. Por que a resposta é 6? Ah, talvez a pergunta no PDF estivesse sutilmente diferente ou a resposta deles que está estranha. Confio no meu cálculo de $C^4\_3 \= 4$. Vou assumir que a resposta correta é 4 e a plataforma pode ter errado ou eu copiei algo errado. A lógica é escolher 3 dos 4 restantes.

*Fim das anotações sobre Princípios Básicos e Agrupamento Simples.*