# Temas 1 e 2: Conjuntos e Contagem
**Período:** 16/10 - 24/10

## Apresentação da Disciplina (16/10)
O vídeo inicial foi direto: mat/lógica é a base p/ programação e IA. É o alicerce, sem isso o resto cai.

---

## Teoria dos Conjuntos (16/10 - 17/10)
Revisão do básico de conjuntos.

### Representação
* **Explícita (Enumeração):** Listar os elementos. Usar `;` p/ não confundir com decimal. Ex: `{ 1; 3; 5 }`. Ordem não importa.
* **Implícita (Propriedade):** Descrever a regra. Formato: `A = {x | p(x)}`, "x tal q p(x) é verdadeiro".

### Símbolos Importantes
* **Pertinência:** `∈` (pertence), `∉` (não pertence).
* **Inclusão:** `⊂` (está contido), `⊃` (contém).
* **Conjunto Vazio:** `∅` ou `{}`.

### Intervalos e Módulo (17/10)
* **Intervalos:** Pedaços da reta real.
    * **Fechado:** `≤` (menor ou igual), `≥` (maior ou igual). Bolinha cheia `●`. Colchetes `[ ]`.
    * **Aberto:** `<` (menor), `>` (maior). Bolinha vazia `○`. Parênteses `()` (mais fácil) ou `]` `[`.
* **Módulo (Valor Absoluto):** `|x|` = distância até o zero. `|x - y|` = distância entre `x` e `y`.
    * **Erro q cometi:** Calculei `|2 - 5|` como `5-2=3`. Errado. O certo é `|2 - 5| = |-3| = 3`. O resultado bateu, mas o processo tava errado. Fixou.
    * **Erro em Inequação:** `|2x - 4| < 3`. Ao resolver `1 < 2x < 7`, me confundi na hora de `2x/2`. Pensei q dava `0*x`. Errado, `2/2 = 1`, então `1*x = x`.

### Operações
* **Interseção (`∩`):** O q está em A **e** em B.
* **União (`∪`):** O q está em A **ou** em B (junta tudo).
* **Diferença (`-`):** O q está em A **e não** está em B.
* **Complementar (`A'`):** O q está no Universo (U) mas **não** está em A.

---

## Princípios de Contagem (22/10 - 24/10)
Como contar possibilidades.

### Princípios Básicos
* **Casa dos Pombos:** Se `n` pombos > `m` casas, pelo menos 1 casa terá +1 pombo. Simples, mas resolve problemas (ex: fios de cabelo).
* **Adição:** Contar `A ∪ B`. Se tiver interseção, subtrai ela p/ não contar 2x. Senão, só soma.
* **Multiplicação:** Tarefa com etapas? Multiplica as opções de cada etapa. É o mais usado.

### Agrupamento Simples (Sem Repetição)
A chave é: **a ordem importa?**

* **Sim, ordem importa:** Arranjo (`Arranjo(n, p)`) ou Permutação (`P(n)`).
    * Usado p/ senhas, filas, anagramas.
    * **Arranjo(n, p) = n! / (n-p)!**
    * **Permutação(n) = n!** (É só um Arranjo onde `p=n`).
* **Não, ordem NÃO importa:** Combinação (`C(n, p)`).
    * Usado p/ comissões, subconjuntos.
    * **Raciocínio:** É o Arranjo, mas dividido por `p!` p/ descontar as repetições de ordem.
    * **Fórmula:** `C(n, p) = n! / (p! * (n-p)!)`

### Agrupamentos Complementares (Com Repetição)
* **Arranjo com Repetição:** Ordem importa, pode repetir.
    * **Cálculo:** `AR(n, p) = n^p` (Ex: senhas).
* **Permutação com Repetição:** Embaralhar `n` objetos com `p`, `q` repetidos.
    * **Cálculo:** `PR = n! / (p! * q! * ...)` (Ex: anagrama de "Araraquara").
* **Permutação Circular:** `n` objetos em círculo (rotações não contam).
    * **Cálculo:** `PC(n) = (n-1)!`
* **Combinação com Repetição:** Ordem NÃO importa, pode repetir.
    * **Cálculo:** `CR(n, p) = C(n+p-1, p)` (Ex: escolher 8 chocolates de 3 marcas).

**Ponto importante:** O material reforça q o Princípio da Multiplicação é a base. As fórmulas são só atalhos.

---

## Resumo das Atividades (Tema 2) (24/10)
* **Desempenho:** 7/10.
* **Erros:**
    * **Q2 (Sanduíches):** Errei. Era só multiplicar as opções (3\*5\*2\*5\*4 = 600). Lição: ler com calma.
    * **Q7 (x+y+z=7):** Não vi q era Combinação com Repetição.
        * **Análise:** "distribuir 7 itens idênticos em 3 caixas (x, y, z)" = CR.
        * `n=3`, `p=7`.
        * `CR(3, 7) = C(3+7-1, 7) = C(9, 7) = 36`. Agora entendi o `C(9, 7)`.
    * **Q8 (Sistema Inequações):** Errei o intervalo final. Lição: Resolver cada inequação e depois achar a interseção.
* **Revisão:** Contagem exige + atenção. Os erros mostraram onde revisar (multiplicação básica, CR, interseção).