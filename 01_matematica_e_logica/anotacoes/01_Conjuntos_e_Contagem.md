# Tema 1 e 2: Apresentação, Teoria dos Conjuntos e Princípios de Contagem
**Período:** 16/10/2025 - 24/10/2025

## Apresentação da Disciplina (16/10)

O vídeo inicial deixou claro: matemática e lógica são a base para programação e IA. Sem isso, a casa cai.

**Tópicos Gerais:**
* Teoria dos conjuntos e princípios de contagem
* Gráficos e interpretações
* Aprofundamento de funções
* Cálculo proposicional
* Cálculo de predicados
* Métodos de demonstração

---

## Teoria dos Conjuntos (16/10 - 17/10)

Revisão do básico: o que é um conjunto e como escrever. O conceito é intuitivo (conjunto de brinquedos, etc.), mas precisamos de uma escrita formal.

### Representação de Conjuntos
* **Explícita (Enumeração):** Listar elementos entre `{}` usando `;` para evitar confusão com decimais em português. Ex: `{ 1; 3; 5; 7; 9 }`. A ordem não importa, mas ordenar (se possível) ajuda a ver padrões. Listar conjuntos infinitos com `...` só funciona se o padrão for óbvio.
* **Implícita (Propriedade):** Descrever a regra/propriedade que os elementos devem satisfazer. Formato: `A = {x | p(x)}`, lido como "o conjunto dos x **tal que** p(x) é verdadeiro". É comum restringir o universo antes, ex: `G = { x ∈ Z | x² < 9 }`, lido como "x pertencente aos inteiros (Z) tal que x² < 9".

### Símbolos Importantes
* **Pertinência:** `∈` (pertence), `∉` (não pertence). Um conjunto pode ser elemento de outro conjunto (analogia da caixa de ovos na sacola). Ex: Em `A = { 1; 2; {3, 4}; 5; 6 }`, `{3, 4} ∈ A`, mas `3 ∉ A`.
* **Inclusão:** `⊂` (está contido), `⊃` (contém). `Y ⊂ X` se todos os elementos de `Y` também são elementos de `X`. Um conjunto está contido nele mesmo (`X ⊂ X`). A barra nega a relação (`⊄`, `⊅`).
* **Conjunto Vazio:** `∅` ou `{}`. É um conjunto sem elementos. É subconjunto de qualquer outro conjunto (`∅ ⊂ X`). A justificativa intuitiva é que a afirmação "todo elemento de ∅ é também elemento de X" não pode ser contrariada, já que não há elementos em ∅.

### Intervalos na Reta e Valor Absoluto (17/10)
* **Conjuntos Numéricos:** Naturais (N={1,2,...}), Inteiros (Z={...,-1,0,1,...}), Racionais (Q=frações), Reais (R=toda a reta).
* **Intervalos:** Pedaços da reta real. A convenção visual/escrita:
    * **Fechado (`≤`, `≥`):** Inclui a ponta. Bolinha cheia `●`, colchetes `[` `]`.
    * **Aberto (`<`, `>`):** Exclui a ponta. Bolinha vazia `○` ou seta, parênteses `()` ou colchetes invertidos `]` `[`. Posso escolher usar só `()` por ser mais fácil.
* **Valor Absoluto (Módulo):** `|x|` é a distância de `x` até zero. É sempre positivo. Definição: `$|x| = \sqrt{x^2}$` ou `$|x| = \{ x \text{ se } x \ge 0; -x \text{ se } x < 0 \}$`. `|x - y|` é a distância entre `x` e `y` na reta.
    * **Raciocínio/Erro:** Calculei `|2 - 5|` como `5-2=3`. **Errado.** O certo é `|2 - 5| = |-3| = 3`. Fixou o conceito.
    * **Inequação:** Resolvi `|2x - 4| < 3`. O PDF divide por 2 antes: `|x-2| < 3/2`. A pergunta vira "quais x distam de 2 menos que 1.5?". Fica entre `2 - 1.5` e `2 + 1.5`, ou seja, `0.5 < x < 3.5`. Meu método de somar 4 e dividir por 2 deu o mesmo resultado. Outro erro que cometi: `2x/2` não é `0*x`, é `1*x = x`.

### Operações entre Conjuntos (17/10)
Definidas em relação a um Conjunto Universo (U). Usam-se Diagramas de Venn para visualizar.
* **Interseção (`A ∩ B`):** Elementos que estão em A **e** em B. `{x ∈ U | x ∈ A e x ∈ B}`.
* **União (`A ∪ B`):** Elementos que estão em A **ou** em B (ou ambos). `{x ∈ U | x ∈ A ou x ∈ B}`.
* **Diferença (`A - B`):** Elementos que estão em A **e não** estão em B. `{x ∈ U | x ∈ A e x ∉ B}`.
* **Complementar (`A'`):** Elementos do Universo que **não** estão em A. `A' = U - A = {x ∈ U | x ∉ A}`.

---

## Princípios de Contagem (22/10 - 24/10)

Foco em como contar possibilidades.

### Princípios Básicos (22/10)

* **Casa dos Pombos (Gavetas):** Se `n` objetos > `m` recipientes, pelo menos um recipiente terá > 1 objeto. Simples, mas poderoso. Ex: 1 milhão de pessoas (`n`), máx 200 mil fios de cabelo (`m`). `n>m` => pelo menos 2 pessoas com mesmo nº de fios. Ex2: 12 inteiros (`n`), 11 restos possíveis na divisão por 11 (`m`). `n>m` => pelo menos 2 com mesmo resto. A diferença deles é divisível por 11.
* **Adição:** Contar união (`A ∪ B`). Se `A` e `B` são disjuntos (`A ∩ B = ∅`), só somar: `n(A ∪ B) = n(A) + n(B)`. Se tiver interseção, subtrai: `n(A ∪ B) = n(A) + n(B) - n(A ∩ B)`. Para 3 conjuntos, a análise das 7 regiões do diagrama de Venn ajuda.
* **Multiplicação:** Tarefa com `k` etapas? Se a etapa 1 tem `p` maneiras e, para *cada* uma delas, a etapa 2 tem `q` maneiras, o total é `p * q`. Isso generaliza para mais etapas. Atenção: a *quantidade* de escolhas na 2ª etapa deve ser independente da *qual* escolha foi feita na 1ª, mas as opções em si podem depender. Ex: Números de 2 dígitos distintos com {1, 2, 3, 4}. 1ª etapa (dezena): 4 opções. 2ª etapa (unidade): 3 opções restantes. Total: `4 * 3 = 12`.

**Fatorial:** `n! = n * (n-1) * ... * 1`. Simplifica produtos. Por convenção, `0! = 1`.

### Agrupamento Simples (Sem Repetição) (22/10)

A chave é saber se a ordem dos elementos importa.

* **Ordem Importa:** Arranjo (`A^n_p`) ou Permutação (`P_n`). (Senhas, filas, anagramas).
    * **Arranjo (`A^n_p`):** Escolher `p` de `n`, ordem importa. Fórmula: `$A^n_p = \frac{n!}{(n-p)!}$` (ou multiplicar `p` termos a partir de `n`). Ex: Filas de 5 com 12 alunos: `A^{12}_5 = 12*11*10*9*8`.
    * **Permutação (`P_n`):** Arranjo com todos os `n` objetos (`p=n`). Ordenar `n` distintos. Fórmula: `$P_n = n!$`. Ex: Anagramas de "trapo" (5 letras): `$P_5 = 5! = 120$`.
* **Ordem NÃO Importa:** Combinação (`C^n_p`). (Comissões sem cargos, subconjuntos).
    * **Raciocínio:** Pega o Arranjo (`A^n_p`) e divide por `p!` (permutações dos `p` escolhidos), para não contar o mesmo grupo várias vezes só por mudar a ordem.
    * **Fórmula:** `$C^n_p = \frac{A^n_p}{p!} = \frac{n!}{p!(n-p)!}$`.
    * **Ex: Comissão de 3 com 8 (sem cargos):** Ordem não importa. `$C^8_3 = \frac{A^8_3}{3!} = \frac{8*7*6}{3*2*1} = 56$`.

### Agrupamentos Complementares (Com Repetição) (24/10)

Situações onde podemos repetir objetos.

1.  **Arranjo com Repetição (`AR^n_p`):**
    * **O que é:** Escolher `p` de `n`, **ordem importa**, **pode repetir**.
    * **Como calcular:** `$AR^n_p = n^p$` (Sempre `n` opções para cada uma das `p` posições).
    * **Exemplo:** Senhas de 4 caracteres com 39 opções (letras+números+símbolos): `$AR^{39}_4 = 39^4$`.

2.  **Permutação com Repetição (`PR^n_{p,q,...}`):**
    * **O que é:** Embaralhar `n` objetos onde há repetições (`p` de um tipo, `q` de outro, etc.).
    * **Como calcular:** `$PR^n_{p,q,...} = \frac{n!}{p!q!...}$` (Permutação total dividida pelos fatoriais das repetições).
    * **Exemplo:** Anagramas de "Araraquara" (10 letras: 5 A, 3 R, 1 Q, 1 U): `$PR^{10}_{5,3,1,1} = \frac{10!}{5!3!1!1!}$`.
    * **Exemplo:** Anagramas de "arranjo" (7 letras: 2 A, 2 R): `$PR^7_{2,2} = \frac{7!}{2!2!} = 1260$`.

3.  **Permutação Circular (`PC_n`):**
    * **O que é:** Organizar `n` objetos em círculo (onde rotações do mesmo arranjo não contam como diferentes).
    * **Como calcular:** `$PC_n = (n-1)!$` (Fixa um objeto e permuta os outros `n-1`).
    * **Exemplo:** 4 amigos em mesa redonda: `$PC_4 = (4-1)! = 3! = 6$`.

4.  **Combinação com Repetição (`CR^n_p`):**
    * **O que é:** Escolher `p` de `n`, **ordem NÃO importa**, **pode repetir** (Ex: escolher `p` sabores de sorvete dentre `n` opções, podendo repetir).
    * **Como calcular:** Usa uma fórmula equivalente a Combinação Simples: `$CR^n_p = C^{n+p-1}_p = \frac{(n+p-1)!}{p!(n-1)!}$`.
    * **Exemplo:** Comprar 8 chocolates de 3 marcas (pode repetir): `$CR^3_8 = C^{3+8-1}_8 = C^{10}_8 = 45$`.
    * **Exemplo (Divisão itens idênticos):** Dividir 20 moedas idênticas entre 3 herdeiros. É equivalente a `$CR^3_{20} = C^{22}_{20} = 231$`. (Aqui `n=3` é o nº de herdeiros/recipientes, `p=20` é o nº de moedas/itens idênticos).

**Importante:** O PDF reforça que o Princípio da Multiplicação é a base de tudo. As fórmulas são atalhos úteis, mas não essenciais se você entender a lógica da multiplicação/adição.

---

## Resumo das Atividades (Tema 2) (24/10)

Fiz os exercícios da plataforma para fechar o Tema 2.

* **Desempenho Geral:** Acertei 7 de 10 questões.
* **Erros:**
    * **Q2 (Sanduíches):** Errei. Era só multiplicar as opções (3\*5\*2\*5\*4 = 600). **Lição:** Ler com calma.
    * **Q7 (x+y+z=7, inteiros não negativos):** Não vi que era Combinação com Repetição. `$CR^3_7 = C^9_7 = 36$. **Lição:** Associar "distribuir itens idênticos em caixas" com CR.
    * **Q8 (Sistema Inequações {x-1>2x ; |x|<2}):** Errei o intervalo final. $|x| < 2 \implies -2 < x < 2$. E $x-1 > 2x \implies -1 > x$. Interseção é $]-2; -1[$. **Lição:** Resolver cada parte e achar a interseção.

* **Acertos Notáveis:** Interseção (Q1, Q3), Casa dos Pombos (Q4), Combinação Simples (Q5), Permutação/Arranjo (Q6).

**Conclusão do Tema 2:** Fechei o conteúdo de Conjuntos e Contagem. Contagem exige mais atenção para saber qual princípio/fórmula usar (ordem importa? repete?). Os erros mostraram onde preciso revisar (Multiplicação básica, CR, Interseção de inequações).