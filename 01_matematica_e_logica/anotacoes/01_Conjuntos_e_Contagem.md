# Temas 1 e 2: Conjuntos e Contagem
**Período:** 16/10 - 24/10

## Teoria dos Conjuntos
Revisão do básico de conjuntos.

### Representação
* **Explícita:** Listar elementos entre `{}`. Usar `;` para separar. Ex: `{1; 3; 5}`. Ordem não importa.
* **Implícita:** Regra. `A = {x | p(x)}` (x tal q p(x) é verdade).

### Símbolos
* **Pertinência:** `∈` (pertence), `∉` (não pertence). Elemento -> Conjunto.
* **Inclusão:** `⊂` (está contido). Conjunto -> Conjunto. `Y ⊂ X` se todo elemento de Y está em X.
* **Vazio:** `∅`. Subconjunto de todos.

### Intervalos e Módulo
* **Intervalos:**
    * Fechado `[]`: Inclui extremos (`≤`, `≥`).
    * Aberto `()`: Exclui extremos (`<`, `>`).
* **Módulo (`|x|`):** Distância até o zero. Sempre positivo.
    * `|x - y|` = distância entre x e y.
    * **Ponto de atenção:** Em inequações com módulo (ex: `|2x-4| < 3`), resolver para os dois casos (positivo e negativo) ou usar a propriedade da distância.

### Operações
* **Interseção (`∩`):** Elementos comuns (E).
* **União (`∪`):** Todos os elementos (OU).
* **Diferença (`-`):** O q tem no primeiro e não no segundo.

---

## Princípios de Contagem

### Básicos
* **Casa dos Pombos:** Se `n` objetos > `m` lugares, algum lugar tem +1 objeto. Útil p/ provar repetições.
* **Adição:** `n(A ∪ B) = n(A) + n(B) - n(A ∩ B)`. Se não tem interseção, só soma.
* **Multiplicação:** Se tem etapas sucessivas, multiplica as opções de cada uma. É a regra principal.

### Agrupamento (Sem Repetição)
* **Ordem importa?**
    * **Sim:** Arranjo. `n! / (n-p)!`. (Senhas, filas, pódio).
    * **Permutação:** Arranjo usando todos os itens. `n!`. (Anagramas, filas completas).
* **Não:** Combinação. `n! / (p!(n-p)!)`. (Comissões, grupos). Divide o arranjo pela permutação dos escolhidos.

### Agrupamento (Com Repetição)
* **Arranjo c/ Repetição:** `n^p`. (Senha podendo repetir número).
* **Permutação c/ Repetição:** Divide o total pelas repetições. `n! / (a! b! ...)` (Anagrama de ARARA).
* **Circular:** `(n-1)!`. (Mesa redonda).
* **Combinação c/ Repetição:** `C(n+p-1, p)`. (Escolher sabores de sorvete, dividir itens idênticos).

---

## Resumo Prático das Atividades
* **Sanduíches:** Multiplicar opções de cada ingrediente (Princípio Multiplicativo). Não complicar.
* **Distribuição de itens iguais:** Usar Combinação com Repetição.
* **Sistemas:** Atenção à interseção de intervalos em inequações.