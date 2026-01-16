# Tema 5: Lógica Digital
**Data:** 16/01/2026 | **Status:** Concluído

## 1. Álgebra Booleana
Desenvolvida por George Boole, é a matemática base dos computadores. Diferente da álgebra comum, aqui só existem dois valores possíveis:
* **Verdadeiro (1):** High / Ligado / 5V.
* **Falso (0):** Low / Desligado / 0V.

## 2. Portas Lógicas Básicas (Gates)
São os dispositivos físicos (transistores) que implementam as operações booleanas.

### A. Porta AND (E) - Multiplicação Lógica
A saída só é **1** se **TODAS** as entradas forem 1.
* *Símbolo:* $A \cdot B$
* *Analogia:* Para o carro andar, preciso de Gasolina **E** Bateria.

| A | B | Saída (A . B) |
| :---: | :---: | :---: |
| 0 | 0 | **0** |
| 0 | 1 | **0** |
| 1 | 0 | **0** |
| 1 | 1 | **1** |

### B. Porta OR (OU) - Soma Lógica
A saída é **1** se **PELO MENOS UMA** entrada for 1.
* *Símbolo:* $A + B$
* *Analogia:* Para entrar na festa, preciso de Convite **OU** Nome na lista.

| A | B | Saída (A + B) |
| :---: | :---: | :---: |
| 0 | 0 | **0** |
| 0 | 1 | **1** |
| 1 | 0 | **1** |
| 1 | 1 | **1** |

### C. Porta NOT (NÃO) - Inversora
Inverte o sinal. Se entra 1, sai 0.
* *Símbolo:* $A'$ ou $\bar{A}$

## 3. Portas Derivadas
Combinações das portas básicas muito usadas na indústria.

* **NAND (Not AND):** O inverso da AND. (Muito barata de fabricar).
* **NOR (Not OR):** O inverso da OR.
* **XOR (Exclusive OR):** A saída é 1 apenas se as entradas forem **diferentes**.
    * *Uso:* Essencial para fazer contas de soma binária.

## 4. Circuitos Digitais
Quando conectamos várias portas lógicas, formamos um circuito.

1.  **Circuitos Combinacionais:**
    * A saída depende *apenas* das entradas atuais. Não tem memória.
    * *Exemplos:* Somadores (calculadora), Decodificadores.

2.  **Circuitos Sequenciais:**
    * A saída depende das entradas atuais **E** do estado anterior (histórico).
    * Possuem **Memória**.
    * *Componente Chave:* **Flip-Flop** (circuito capaz de armazenar 1 bit).

---

## Resumo Rápido
* **AND:** Exigente. Precisa de tudo 1.
* **OR:** Flexível. Basta um 1.
* **NOT:** Do contra. Inverte tudo.
* **XOR:** O "diferentão". 1 se as entradas forem opostas.
* **Combinacional vs Sequencial:** O sequencial tem memória (Flip-Flop), o combinacional não.