# **Tema 1 e 2: Apresentação e Teoria dos Conjuntos**

**Data:** 16/10/2025 \- 17/10/2025

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
O professor frisou pra usar ponto e vírgula ; em vez de vírgula , pra não confundir com número decimal, já que a gente usa vírgula pra isso em português. A ordem não importa.  
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
G \= { x ∈ Z | x² \< 9 } // Forma mais usual, declarando a restrição antes.

### **Símbolo de Pertinência (∈)**

* ∈ significa **"pertence a"**.  
* ∉ significa **"não pertence a"**.

Gostei da analogia da sacola de compras e da caixa de ovos: se você coloca a caixa de ovos na sacola, é a *caixa* que pertence à sacola, não os ovos individualmente.

**Exemplo:** A \= { 1; 2; {3, 4}; 5; 6 }

* 1 ∈ A (Verdadeiro)  
* 3 ∉ A (Verdadeiro, porque o 3 está "dentro da caixa")  
* {3, 4} ∈ A (Verdadeiro, a "caixa" pertence ao conjunto)

### **Relação de Inclusão (⊂ e ⊃)**

* ⊂ significa **"está contido em"**.  
* ⊃ significa **"contém"**.

Basicamente, se todos os elementos de um conjunto Y também estão no conjunto X, então Y está contido em X (Y ⊂ X). A barra "/" no símbolo nega a relação (Ex: ⊄).

**Igualdade:** Dois conjuntos X e Y são iguais se, e somente se, X está contido em Y e Y está contido em X. $X \= Y \\iff (X \\subset Y \\text{ e } Y \\subset X)$. Ou seja, todo elemento de x está em y e vice versa.

### **O Conjunto Vazio (∅)**

É um conjunto que não tem nenhum elemento. Pode ser representado por ∅ ou {}.

**Ponto importante:** O conjunto vazio é subconjunto de qualquer outro conjunto (∅ ⊂ X).

## **Intervalos na Reta Numérica e Valor Absoluto**

**Data:** 17/10/2025

Essa parte entra nos conjuntos numéricos e como representá-los na reta.

### **A Reta Real e os Intervalos**

Intervalos são pedaços da reta real. A convenção é:

* **Fechado (≤, ≥):** Inclui a ponta. Usa colchetes \[ \].  
* **Aberto (\<, \>):** Exclui a ponta. Usa parênteses () ou colchetes invertidos \] \[.

**Meu raciocínio:**

* \\{x \\in \\mathbb{R} \\mid a \< x \< b\\} \-\> Se o sinal é só \< (menor), é aberto. Usa parênteses (a, b). Posso preferir só usar () por ser mais fácil.  
* \\{x \\in \\mathbb{R} \\mid a \\le x \< b\\} \-\> Se o sinal é ≤ (menor ou igual), é fechado. Usa colchete \[. Então aqui inclui o a e exclui o b, ficando \[a, b). Faz sentido.

### **Valor Absoluto (Módulo)**

Módulo (|x|) é a distância de um número x até a origem (zero). Como é distância, é sempre positivo.  
Achei confuso no começo, mas a ideia de |x \- y| ser a distância entre x e y ajudou a clarear.  
**Análise de Erro:**

Tentei calcular |x \- 5| para x \= 2\. Meu primeiro instinto foi fazer 5 \- 2 \= 3\. **Errado.** O cálculo correto é substituir o x na fórmula: |2 \- 5| \= |-3|. Como o resultado do módulo é sempre positivo, a distância é 3\. O resultado foi o mesmo, mas o caminho estava errado. Um erro básico, mas que fixa o conceito.

### **Resolvendo Inequação com Módulo: |2x \- 4| \< 3**

Aqui eu me perdi um pouco. Acompanhei a resolução para entender o passo a passo.

**Meu Raciocínio (com correções):**

1. **Entender o problema:** |2x \- 4| \< 3 significa que a distância da expressão (2x \- 4\) até o zero é menor que 3\. Ou seja, essa expressão está entre \-3 e 3\.  
   * \-3 \< (2x \- 4\) \< 3\. Até aqui, ok.  
2. **Isolar o x:** O objetivo é deixar o x sozinho no meio.  
   * Primeiro, somei \+4 em tudo para eliminar o \-4 do meio.  
     \-3 \+ 4 \< 2x \- 4 \+ 4 \< 3 \+ 4  
     1 \< 2x \< 7  
   * **Ponto de atenção:** Minha dúvida era se eu sempre precisava fazer o número que acompanha o x virar zero. Não. O objetivo é isolar o x, não zerar os termos. A operação oposta (+4 para \-4) serve para cancelar o termo. Se fosse \+1000, eu usaria \-1000.  
3. Finalizar o isolamento do x: O termo do meio é 2x (2 \* x). Para tirar o 2, uso a operação inversa da multiplicação, que é a divisão. Divido tudo por 2\.  
   1/2 \< 2x/2 \< 7/2  
4. **Análise do Erro (de novo):**Na hora de simplificar 2x/2, eu me enrolei. Pensei que 2/2 daria 0, o que zeraria o x. **Errado.** 2/2 é 1\. E 1 \* x é x, porque qualquer número multiplicado por 1 é ele mesmo. Fiquei confuso, mas agora entendi.  
5. **Resultado Final:**  
   * 0.5 \< x \< 3.5  
   * **Conclusão:** Fiz isso tudo pra achar o intervalo do x. O resultado não é só x, mas o intervalo onde x pode existir. A solução é o conjunto de todos os números entre 0.5 e 3.5.

*Terminei o submódulo "Intervalos na reta numérica e valor absoluto". Falta ver o vídeo ainda.*