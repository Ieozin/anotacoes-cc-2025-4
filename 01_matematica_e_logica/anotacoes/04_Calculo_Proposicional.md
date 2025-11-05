# Tema 5: Cálculo Proposicional (Parte 1)
**Data:** 05/11/2025

## 1. Introdução à Lógica Proposicional

Começando o Tema 5. O vídeo de introdução bateu na tecla de que a lógica matemática é a "caixa de ferramentas" para profissionais de TI, usada para derivar novas verdades a partir de premissas válidas.

A base disso tudo vem de Aristóteles, o "pai do pensamento lógico". O ponto principal dele era a **teoria do silogismo**: se as premissas são verdadeiras, a conclusão tem que ser verdadeira.

* **Exemplo clássico:** "Todo homem é mortal. Sócrates é homem. Logo, Sócrates é mortal."

O problema da lógica dele é que usava linguagem natural (imprecisa). Por isso, matemáticos como **George Boole** e **Augustus De Morgan** criaram uma notação matemática (simbólica) para a coisa ficar mais rigorosa.

## 2. Proposições (A Base do Cálculo)

A lógica funciona em cima de **proposições**: são sentenças declarativas com sentido completo, que podem ser claramente definidas como **Verdadeiras (V)** ou **Falsas (F)**.

* **NÃO é proposição:** Frases interrogativas ("Qual seu nome?"), exclamativas ("Feliz Natal!") ou imperativas ("Estude, agora!").
* **É proposição:** "Carlos é estudioso", "2 < 5".

### Três Princípios da Lógica
1.  **Princípio do 3º Excluído:** Ou é Verdadeiro ou é Falso. Não existe "talvez".
2.  **Princípio da Não Contradição:** Não pode ser V e F ao mesmo tempo.
3.  **Princípio da Identidade:** Uma proposição é igual a ela mesma.

### Tipos de Proposição
* **Simples (Atômica):** Só uma ideia. Usa-se letras minúsculas (`p`, `q`).
    * Ex: `p: João é inteligente.`
* **Composta (Molecular):** Formada por duas ou mais proposições simples, ligadas por conectivos.
    * Ex: "Maria é bonita **e** Pedro é estudioso."

---

## 3. Conectivos Lógicos (Os "Juntores")

São os símbolos que usamos para transformar a linguagem natural em simbólica e criar proposições compostas.

* **Negação (NÃO):**
    * **Símbolo:** `~` (ou `¬`)
    * **Linguagem:** "não", "é falso que..."
    * **Dupla Negação:** `~(~p)` é a mesma coisa que `p`.

* **Conjunção (E):**
    * **Símbolo:** `∧`
    * **Linguagem:** "e", "mas", "além disso"
    * **Ex:** `p: "Paulo é trabalhador"`, `q: "Paulo é estudioso"` -> `p ∧ q`: "Paulo é trabalhador e estudioso".

* **Disjunção Inclusiva (OU):**
    * **Símbolo:** `∨`
    * **Linguagem:** "ou"
    * **Ex:** "Ana é professora ou médica" (pode ser as duas).

* **Disjunção Exclusiva (OU... OU...):**
    * **Símbolo:** `⊻` (ou `V` sublinhado)
    * **Linguagem:** "Ou... ou..."
    * **Ex:** "Ou Ana é paulista, ou é gaúcha" (não pode ser as duas).

* **Condicional (SE... ENTÃO...):**
    * **Símbolo:** `→`
    * **Linguagem:** "Se p, então q"
    * `p` é o **antecedente** (condição suficiente).
    * `q` é o **consequente** (condição necessária).

* **Bicondicional (SE E SOMENTE SE):**
    * **Símbolo:** `↔`
    * **Linguagem:** "p se e somente se q"
    * `p` é condição necessária e suficiente para `q` (e vice-versa).

* **(Menos comuns: NAND (↑) = `~(p∧q)` e NOR (↓) = `~(p∨q)`)**

---

## 4. Tradução: Linguagem Natural para Simbólica

O processo é identificar as proposições simples (p, q, r) e os conectivos.

* **Exemplo 1 (Negação + "ou"):** "O aluno não aprende rápido ou o professor possui muito conhecimento."
    * `p: "O aluno aprende rápido"`
    * `q: "O professor possui muito conhecimento"`
    * **Simbólica: `~p ∨ q`**

* **Exemplo 2 (Condicional + "ou"):** "Se não vejo Paulo, então não vou ao cinema ou fico triste."
    * `p: "Não vejo Paulo"`
    * `q: "Não vou ao cinema"`
    * `r: "Fico triste"`
    * **Simbólica: `p → (q ∨ r)`**

* **Exemplo 3 (Negações diversas):**
    * `"Carla comprou um carro, mas não comprou um apartamento."` -> `p ∧ ~q`
    * `"Não é verdade que Carla comprou um carro ou um apartamento."` -> `~(p ∨ q)`
    * `"Carla nem comprou um carro e nem comprou um apartamento."` -> `~p ∧ ~q`
    * `"É falso que Carla não comprou o carro ou não comprou o apartamento."` -> `~(~p ∨ ~q)`

* **Exercício (Q1 Atividade 4):** "Nem Carlos é engenheiro nem Paulo é professor."
    * `p: "Carlos é engenheiro"`
    * `q: "Paulo é professor"`
    * "Nem... nem..." é o mesmo que "não... E não...".
    * **Simbólica: `~p ∧ ~q`** (Alternativa C).

---
*Terminei a primeira parte do Tema 5. Próximo passo: Tabela-Verdade.*