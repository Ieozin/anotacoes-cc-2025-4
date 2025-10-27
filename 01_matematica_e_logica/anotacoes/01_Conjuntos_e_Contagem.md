# Tema 1 e 2: Apresentação, Teoria dos Conjuntos e Princípios de Contagem
**Período:** 16/10/2025 - 24/10/2025

## Apresentação da Disciplina (16/10)

[cite_start]O vídeo inicial deixou claro: matemática e lógica são a base para programação e IA[cite: 5]. Sem isso, a casa cai.

**Tópicos Gerais:**
* [cite_start]Teoria dos conjuntos e princípios de contagem [cite: 1, 2]
* Gráficos e interpretações
* Aprofundamento de funções
* Cálculo proposicional
* Cálculo de predicados
* Métodos de demonstração

---

## Teoria dos Conjuntos (16/10 - 17/10)

[cite_start]Revisão do básico: o que é um conjunto e como escrever[cite: 18]. [cite_start]O conceito é intuitivo (conjunto de brinquedos, etc.) [cite: 23][cite_start], mas precisamos de uma escrita formal[cite: 29].

### [cite_start]Representação de Conjuntos [cite: 19]
* [cite_start]**Explícita (Enumeração):** Listar elementos entre `{}` usando `;` para evitar confusão com decimais em português[cite: 31, 36]. Ex: `{ 1; 3; 5; 7; [cite_start]9 }`[cite: 37]. [cite_start]A ordem não importa [cite: 38][cite_start], mas ordenar (se possível) ajuda a ver padrões[cite: 40, 41]. [cite_start]Listar conjuntos infinitos com `...` só funciona se o padrão for óbvio[cite: 45, 46].
* [cite_start]**Implícita (Propriedade):** Descrever a regra/propriedade que os elementos devem satisfazer[cite: 77, 78]. [cite_start]Formato: `A = {x | p(x)}` [cite: 80][cite_start], lido como "o conjunto dos x **tal que** p(x) é verdadeiro"[cite: 81, 82]. [cite_start]É comum restringir o universo antes, ex: `G = { x ∈ Z | x² < 9 }` [cite: 92, 93][cite_start], lido como "x pertencente aos inteiros (Z) tal que x² < 9"[cite: 94].

### Símbolos Importantes
* [cite_start]**Pertinência:** `∈` (pertence) [cite: 53][cite_start], `∉` (não pertence)[cite: 54]. [cite_start]Um conjunto pode ser elemento de outro conjunto (analogia da caixa de ovos na sacola [cite: 65, 67]). Ex: Em `A = { 1; 2; {3, 4}; 5; [cite_start]6 }`, `{3, 4} ∈ A`, mas `3 ∉ A`[cite: 68, 71].
* [cite_start]**Inclusão:** `⊂` (está contido), `⊃` (contém)[cite: 116]. [cite_start]`Y ⊂ X` se todos os elementos de `Y` também são elementos de `X`[cite: 105, 114, 115]. [cite_start]Um conjunto está contido nele mesmo (`X ⊂ X`)[cite: 119]. [cite_start]A barra nega a relação (`⊄`, `⊅`)[cite: 120].
* [cite_start]**Conjunto Vazio:** `∅` ou `{}`[cite: 147]. [cite_start]É um conjunto sem elementos[cite: 146]. [cite_start]É subconjunto de qualquer outro conjunto (`∅ ⊂ X`)[cite: 149]. [cite_start]A justificativa intuitiva é que a afirmação "todo elemento de ∅ é também elemento de X" não pode ser contrariada, já que não há elementos em ∅[cite: 150, 151].

### [cite_start]Intervalos na Reta e Valor Absoluto (17/10) [cite: 153]
* [cite_start]**Conjuntos Numéricos:** Naturais (N={1,2,...}) [cite: 157][cite_start], Inteiros (Z={...,-1,0,1,...}) [cite: 161][cite_start], Racionais (Q=frações) [cite: 163][cite_start], Reais (R=toda a reta)[cite: 168].
* [cite_start]**Intervalos:** Pedaços da reta real[cite: 183, 184]. [cite_start]A convenção visual/escrita[cite: 184]:
    * **Fechado (`≤`, `≥`):** Inclui a ponta. [cite_start]Bolinha cheia `●`, colchetes `[` `]`[cite: 186, 190, 191].
    * **Aberto (`<`, `>`):** Exclui a ponta. [cite_start]Bolinha vazia `○` ou seta, parênteses `()` ou colchetes invertidos `]` `[` [cite: 194-198]. Posso escolher usar só `()` por ser mais fácil.
* [cite_start]**Valor Absoluto (Módulo):** `|x|` é a distância de `x` até zero[cite: 232]. [cite_start]É sempre positivo[cite: 232]. Definição: `$|x| = \sqrt{x^2}$` ou `$|x| = \{ x \text{ se } x \ge 0; [cite_start]-x \text{ se } x < 0 \}$`[cite: 234, 235]. [cite_start]`|x - y|` é a distância entre `x` e `y` na reta[cite: 225].
    * **Raciocínio/Erro:** Calculei `|2 - 5|` como `5-2=3`. **Errado.** O certo é `|2 - 5| = |-3| = 3`. Fixou o conceito.
    * **Inequação:** Resolvi `|2x - 4| < 3`. O PDF divide por 2 antes: `|x-2| [cite_start]< 3/2`[cite: 244]. [cite_start]A pergunta vira "quais x distam de 2 menos que 1.5?"[cite: 245]. [cite_start]Fica entre `2 - 1.5` e `2 + 1.5`, ou seja, `0.5 < x < 3.5`[cite: 247]. Meu método de somar 4 e dividir por 2 deu o mesmo resultado. Outro erro que cometi: `2x/2` não é `0*x`, é `1*x = x`.

### [cite_start]Operações entre Conjuntos (17/10) [cite: 261]
[cite_start]Definidas em relação a um Conjunto Universo (U)[cite: 265, 266]. [cite_start]Usam-se Diagramas de Venn para visualizar[cite: 263].
* [cite_start]**Interseção (`A ∩ B`):** Elementos que estão em A **e** em B[cite: 328, 390]. `{x ∈ U | x ∈ A e x ∈ B}`.
* [cite_start]**União (`A ∪ B`):** Elementos que estão em A **ou** em B (ou ambos)[cite: 331, 391]. `{x ∈ U | x ∈ A ou x ∈ B}`.
* [cite_start]**Diferença (`A - B`):** Elementos que estão em A **e não** estão em B[cite: 360, 363, 392]. `{x ∈ U | x ∈ A e x ∉ B}`.
* [cite_start]**Complementar (`A'`):** Elementos do Universo que **não** estão em A [cite: 364-366]. [cite_start]`A' = U - A = {x ∈ U | x ∉ A}`[cite: 393].

---

## Princípios de Contagem (22/10 - 24/10)

[cite_start]Foco em como contar possibilidades[cite: 558].

### [cite_start]Princípios Básicos (22/10) [cite: 559]

* [cite_start]**Casa dos Pombos (Gavetas):** Se `n` objetos > `m` recipientes, pelo menos um recipiente terá > 1 objeto[cite: 566]. [cite_start]Simples, mas poderoso[cite: 564, 565]. Ex: 1 milhão de pessoas (`n`), máx 200 mil fios de cabelo (`m`). [cite_start]`n>m` => pelo menos 2 pessoas com mesmo nº de fios [cite: 573-576]. Ex2: 12 inteiros (`n`), 11 restos possíveis na divisão por 11 (`m`). `n>m` => pelo menos 2 com mesmo resto. [cite_start]A diferença deles é divisível por 11 [cite: 580-582].
* **Adição:** Contar união (`A ∪ B`). [cite_start]Se `A` e `B` são disjuntos (`A ∩ B = ∅`), só somar: `n(A ∪ B) = n(A) + n(B)`[cite: 606, 607]. [cite_start]Se tiver interseção, subtrai: `n(A ∪ B) = n(A) + n(B) - n(A ∩ B)`[cite: 596]. [cite_start]Para 3 conjuntos, a análise das 7 regiões do diagrama de Venn ajuda[cite: 609, 621].
* **Multiplicação:** Tarefa com `k` etapas? [cite_start]Se a etapa 1 tem `p` maneiras e, para *cada* uma delas, a etapa 2 tem `q` maneiras, o total é `p * q` [cite: 654-658]. Isso generaliza para mais etapas. [cite_start]Atenção: a *quantidade* de escolhas na 2ª etapa deve ser independente da *qual* escolha foi feita na 1ª, mas as opções em si podem depender[cite: 660]. Ex: Números de 2 dígitos distintos com {1, 2, 3, 4}. 1ª etapa (dezena): 4 opções. 2ª etapa (unidade): 3 opções restantes. [cite_start]Total: `4 * 3 = 12` [cite: 663-680].

**Fatorial:** `n! [cite_start]= n * (n-1) * ... * 1`[cite: 694]. [cite_start]Simplifica produtos[cite: 692]. Por convenção, `0! [cite_start]= 1`[cite: 697].

### [cite_start]Agrupamento Simples (Sem Repetição) (22/10) [cite: 722]

[cite_start]A chave é saber se a ordem dos elementos importa[cite: 726].

* [cite_start]**Ordem Importa:** Arranjo (`A^n_p`) ou Permutação (`P_n`)[cite: 729, 742]. (Senhas, filas, anagramas).
    * [cite_start]**Arranjo (`A^n_p`):** Escolher `p` de `n`, ordem importa[cite: 747, 756]. [cite_start]Fórmula: `$A^n_p = \frac{n!}{(n-p)!}$` (ou multiplicar `p` termos a partir de `n`)[cite: 759]. [cite_start]Ex: Filas de 5 com 12 alunos: `A^{12}_5 = 12*11*10*9*8`[cite: 754].
    * [cite_start]**Permutação (`P_n`):** Arranjo com todos os `n` objetos (`p=n`)[cite: 774]. Ordenar `n` distintos. [cite_start]Fórmula: `$P_n = n!$`[cite: 775]. Ex: Anagramas de "trapo" (5 letras): `$P_5 = 5! [cite_start]= 120$`[cite: 782].
* [cite_start]**Ordem NÃO Importa:** Combinação (`C^n_p`)[cite: 735, 743]. [cite_start](Comissões sem cargos, subconjuntos [cite: 738, 797]).
    * [cite_start]**Raciocínio:** Pega o Arranjo (`A^n_p`) e divide por `p!` (permutações dos `p` escolhidos), para não contar o mesmo grupo várias vezes só por mudar a ordem [cite: 803-808].
    * [cite_start]**Fórmula:** `$C^n_p = \frac{A^n_p}{p!} = \frac{n!}{p!(n-p)!}$`[cite: 810].
    * **Ex: Comissão de 3 com 8 (sem cargos):** Ordem não importa. [cite_start]`$C^8_3 = \frac{A^8_3}{3!} = \frac{8*7*6}{3*2*1} = 56$`[cite: 791].

### [cite_start]Agrupamentos Complementares (Com Repetição) (24/10) [cite: 963]

[cite_start]Situações onde podemos repetir objetos[cite: 974, 975].

1.  [cite_start]**Arranjo com Repetição (`AR^n_p`):** [cite: 977]
    * [cite_start]**O que é:** Escolher `p` de `n`, **ordem importa**, **pode repetir**[cite: 979].
    * [cite_start]**Como calcular:** `$AR^n_p = n^p$` (Sempre `n` opções para cada uma das `p` posições)[cite: 981, 982].
    * [cite_start]**Exemplo:** Senhas de 6 caracteres com 62 opções (26 min+26 MAI+10 alg): `$AR^{62}_6 = 62^6$`[cite: 983, 984].

2.  [cite_start]**Permutação com Repetição (`PR^n_{p,q,...}`):** [cite: 986]
    * [cite_start]**O que é:** Embaralhar `n` objetos onde há repetições (`p` de um tipo, `q` de outro, etc.)[cite: 987].
    * **Como calcular:** `$PR^n_{p,q,...} = \frac{n!}{p!q!...}$` (Permutação total dividida pelos fatoriais das repetições).
    * [cite_start]**Exemplo:** Anagramas de "Araraquara" (10 letras: 5 A, 3 R, 1 Q, 1 U): `$PR^{10}_{5,3,1,1} = \frac{10!}{5!3!1!1!}$`[cite: 989].
    * [cite_start]**Exemplo:** Anagramas de "arranjo" (7 letras: 2 A, 2 R): `$PR^7_{2,2} = \frac{7!}{2!2!} = 1260$`[cite: 1034, 1047].

3.  [cite_start]**Permutação Circular (`PC_n`):** [cite: 994]
    * [cite_start]**O que é:** Organizar `n` objetos em círculo (onde rotações do mesmo arranjo não contam como diferentes)[cite: 996].
    * [cite_start]**Como calcular:** `$PC_n = (n-1)!$` (Fixa um objeto e permuta os outros `n-1`)[cite: 1002, 1004].
    * **Exemplo:** 4 amigos em mesa redonda: `$PC_4 = (4-1)! = 3! [cite_start]= 6$`[cite: 999, 1003].

4.  [cite_start]**Combinação com Repetição (`CR^n_p`):** [cite: 1006]
    * [cite_start]**O que é:** Escolher `p` de `n`, **ordem NÃO importa**, **pode repetir** [cite: 1009] [cite_start](Ex: escolher `p` sabores de sorvete dentre `n` opções, podendo repetir [cite: 975]).
    * [cite_start]**Como calcular:** Usa uma fórmula equivalente a Combinação Simples: `$CR^n_p = C^{n+p-1}_p = \frac{(n+p-1)!}{p!(n-1)!}$`[cite: 1013, 1031].
    * [cite_start]**Exemplo:** Comprar 8 chocolates de 3 marcas (pode repetir): `$CR^3_8 = C^{3+8-1}_8 = C^{10}_8 = 45$`[cite: 1011, 1012].
    * **Exemplo (Divisão itens idênticos):** Dividir 20 moedas idênticas entre 3 herdeiros. [cite_start]É equivalente a `$CR^3_{20} = C^{22}_{20} = 231$`[cite: 1134, 1136]. (Aqui `n=3` é o nº de herdeiros/recipientes, `p=20` é o nº de moedas/itens idênticos).

[cite_start]**Importante:** O PDF reforça que o Princípio da Multiplicação é a base de tudo[cite: 1017, 1189]. [cite_start]As fórmulas são atalhos úteis, mas não essenciais se você entender a lógica da multiplicação/adição[cite: 1018, 1189].

---

## Resumo das Atividades (Tema 2) (24/10)

Fiz os exercícios da plataforma para fechar o Tema 2.

* **Desempenho Geral:** Acertei 7 de 10 questões.
* **Erros:**
    * **Q2 (Sanduíches):** Errei. Era só multiplicar as opções (3\*5\*2\*5\*4 = 600). **Lição:** Ler com calma.
    * **Q7 (x+y+z=7, inteiros não negativos):** Não vi que era Combinação com Repetição. `$CR^3_7 = C^9_7 = 36$. **Lição:** Associar "distribuir itens idênticos em caixas" com CR.
    * **Q8 (Sistema Inequações {x-1>2x ; |x|<2}):** Errei o intervalo final. $|x| < 2 \implies -2 < x < 2$. E $x-1 > 2x \implies -1 > x$. Interseção é $]-2; -1[$. **Lição:** Resolver cada parte e achar a interseção.

* **Acertos Notáveis:** Q1 (Interseção), Q3 (Subconjuntos da Interseção), Q4 (Casa dos Pombos - balas), Q5 (Combinação - Mega Sena), Q6 (Arranjo - Senha ENEM), Q9 (União de Intervalos).

**Conclusão do Tema 2:** Fechei o conteúdo de Conjuntos e Contagem. Contagem exige mais atenção para saber qual princípio/fórmula usar (ordem importa? repete?). Os erros mostraram onde preciso revisar (Multiplicação básica, CR, Interseção de inequações).