# Tema 4: Aprofundamento de Funções
**Data:** 30/10 - 04/11

## 1. Conceito de Função (Revisão)
Aprofundamento do Tema 3.
* **Regra Chave:** Cada `x` tem **exatamente um** `y`.
* **Domínio (D):** Conjunto de partida (A). Valores q `x` pode ter.
* **Contradomínio (CD):** Conjunto de chegada (B). Todos os `y` possíveis.
* **Imagem (Im):** Apenas os `y` q são *realmente* atingidos. Imagem é subconjunto do Contradomínio.

---

## 2. Domínio (D) - Restrições
O q realmente importa: achar o domínio é achar as **restrições** (o q quebra a conta).

* **Restrição 1: Divisão por Zero (Denominador != 0)**
    * Ex: `f(x) = 1/x`. Domínio: `x != 0`.
    * Ex: `L(x) = 1 / (x+2)`. Domínio: `x+2 != 0` => `x != -2`.
* **Restrição 2: Raiz Quadrada (Radiciando >= 0)**
    * Ex: `f(x) = sqrt(x)`. Domínio: `x >= 0`.
* **Restrição Mista (Ex: Boleira):** `f(x) = 1 / sqrt(x-3)`
    * Tem 2 restrições: `x-3 >= 0` (raiz) e `sqrt(x-3) != 0` (divisão).
    * Juntando: `x-3 > 0` => `x > 3`.

---

## 3. Imagem (Im) - Como Achar
Valores de "saída" `y` q a função gera.

* **Método 1: Inversa:** `Domínio da f-1(x) = Imagem da f(x)`.
    * Achar a inversa é trocar `x` por `y` e isolar `y`.
    * Ex: `f(x) = 1/x`. Inversa é `f-1(x) = 1/x`. Domínio da inversa é `x != 0`. Logo, Imagem da original é `y != 0`.
* **Método 2: Análise Direta:** `f(x) = |x|`. `x` pode ser qualquer real, mas `y` (o resultado) é sempre `>= 0`. Imagem é `[0, +infinito)`.
* **Método 3: Projeção Gráfica:** "Amassar" o gráfico no eixo Y.

---

## 4. Classificação de Funções
* **Função Injetora (Um-para-um):** `x` diferentes levam a `y` diferentes.
    * **Teste da Reta Horizontal:** Se a reta horizontal bate +1 vez no gráfico, **NÃO é** injetora.
    * Ex: `f(x) = x^2` não é injetora (pq `f(-2)=4` e `f(2)=4`).
* **Função Sobrejetora (Cobre tudo):** Não sobra elemento no Contradomínio.
    * **Regra:** `Imagem = Contradomínio`.
    * Ex: `f(x) = x^2` (com CD=R) não é sobrejetora (Imagem é `[0, +infinito)`).
* **Função Bijetora:** É Injetora **E** Sobrejetora. (Ex: `f(x) = 2x+1` de R em R).

---

## 5. Comportamento
* **Crescente:** Gráfico sobe (da esq. p/ dir.). `x` aumenta, `y` aumenta.
* **Decrescente:** Gráfico desce. `x` aumenta, `y` diminui.
* **Periódica:** Padrão do gráfico se repete (Período `T`). `f(x + T) = f(x)`.

---

## 6. Resumo das Atividades (Tema 4) (03/11)
* **1ª Tentativa:** 1/9. Chutei tudo, não entendi a aplicação.
* **2ª Tentativa (04/11):** 6/9. Progresso claro.
* **Erros q sobraram:**
    * **Q7 (Imposto):** Função por partes. A imagem tinha um "buraco". `[0, 1000] U (4000, +infinito)`.
    * **Q8 (senx):** Erro de conceito. `sen(x)` é ímpar (não par) e não é sobrejetora de R em R (Imagem é `[-1, 1]`).
    * **Q9 (Domínio Misto):** O mais difícil. `f(x) = sqrt(num) / sqrt(den)`. Tinha q analisar 2 restrições (Numerador `≥ 0`, Denominador `> 0`) e fazer a **interseção** dos resultados.
* **Conclusão:** Entendi a lógica, mas errei os problemas q misturavam vários conceitos. Preciso revisar Domínio Misto e Trig.