# Temas 1 e 2: Conjuntos e Contagem
**Status:** Concluído

## Teoria dos Conjuntos
O básico da linguagem matemática. Sem isso não dá pra ler documentação técnica ou paper.

### Representação
* **Explícita:** Listar tudo entre chaves. `{1; 2; 3}`. Ordem não importa.
* **Implícita:** Regra. `A = {x | p(x)}`. Lê-se: "x tal q a propriedade p(x) é verdadeira".

### Símbolos Chave
* **Pertinência:** `∈` (elemento pertence ao conjunto).
* **Inclusão:** `⊂` (conjunto está contido em outro).
* **Vazio (`∅`):** Subconjunto de todo mundo.

### Intervalos e Módulo
* **Intervalos:**
    * `[a, b]`: Fechado. Inclui as pontas (`<=`).
    * `(a, b)`: Aberto. Exclui as pontas (`<`).
* **Módulo (`|x|`):** Distância até o zero. Sempre positivo.
    * **Atenção em Inequações:** `|x| < k` vira `-k < x < k`. Tem q resolver os dois lados.

### Operações
* **Interseção (`∩`):** O q tem nos dois (E).
* **União (`∪`):** Junta tudo (OU).
* **Diferença (`-`):** O q tem no primeiro e não tem no segundo.

---

## Princípios de Contagem
Foco: saber se a ordem importa ou não.

### Regras de Ouro
1. **Multiplicação:** Se tenho etapas sucessivas, multiplico as possibilidades. (Ex: 3 pães * 2 carnes = 6 sanduíches).
2. **Casa dos Pombos:** Se tenho `n` itens e `m` gavetas (e `n > m`), alguma gaveta vai ter mais de 1 item.

### O Resumo das Fórmulas
* **A ordem importa? (Senha, Fila, Pódio)**
    * **Sim:** É **Arranjo**.
    * Fórmula: `n! / (n-p)!`
    * **Permutação:** É um arranjo usando todos os itens. `n!`.
* **A ordem NÃO importa? (Grupo, Comissão, Salada de Frutas)**
    * **Não:** É **Combinação**.
    * Fórmula: `n! / (p! * (n-p)!)`. (Divide pela permutação dos escolhidos pra tirar a repetição).

### Casos Especiais (Repetição)
* **Arranjo c/ Repetição:** `n^p`. (Senha de banco).
* **Permutação c/ Repetição:** `n! / (a! b! ...)`. (Anagrama de ARARA - divide pelas letras repetidas).
* **Combinação c/ Repetição:** "Barrinhas e estrelas". Fórmula: `C(n+p-1, p)`.

---

## Pontos de Atenção (Erros q cometi)
* **Distribuição de itens iguais:** Se o problema fala "distribuir X itens idênticos em Y caixas", é Combinação com Repetição.
* **Inequações:** Lembrar de fazer a interseção dos intervalos no final.