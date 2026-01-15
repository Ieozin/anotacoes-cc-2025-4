# Tema 4: Representação de Dados
**Data:** 15/01/2026 | **Status:** Concluído

## 1. O Conceito de Digitalização
O computador é um dispositivo eletrônico digital. Ele não entende "A", "cor azul" ou "som grave". Ele só entende:
* **Ligado / Alta Voltagem:** Representado por **1**.
* **Desligado / Baixa Voltagem:** Representado por **0**.

A **Representação de Dados** é o conjunto de regras (padrões) para converter informações humanas em binário.

## 2. Unidades de Medida
A base de tudo.
* **Bit (b):** A menor unidade (0 ou 1).
* **Byte (B):** Conjunto de 8 bits. É a unidade padrão para armazenar um caractere.

| Unidade | Símbolo | Valor (Potência de 2) | Aproximação Decimal |
| :--- | :--- | :--- | :--- |
| **Kilobyte** | KB | $2^{10}$ bytes | 1.024 bytes |
| **Megabyte** | MB | $2^{20}$ bytes | ~1 Milhão de bytes |
| **Gigabyte** | GB | $2^{30}$ bytes | ~1 Bilhão de bytes |
| **Terabyte** | TB | $2^{40}$ bytes | ~1 Trilhão de bytes |

> **Atenção:** Em redes (velocidade de internet), usamos **bits** por segundo (Mbps). Em armazenamento (HD), usamos **Bytes** (MB, GB).

## 3. Sistemas de Numeração
Nós usamos decimal (10 dedos), o computador usa binário (2 estados).

1.  **Decimal (Base 10):** Símbolos 0-9.
2.  **Binário (Base 2):** Símbolos 0-1. Linguagem nativa da máquina.
3.  **Hexadecimal (Base 16):** Símbolos 0-9 e A-F.
    * *Função:* Simplificar a leitura de binários longos para humanos.
    * *Ex:* O binário `1111 1111` vira `FF` em Hexa. Muito usado em códigos de cores HTML (`#FFFFFF`).



## 4. Representação de Inteiros
Como o computador guarda números negativos?
* **Sinal e Magnitude:** O primeiro bit indica o sinal (0 positivo, 1 negativo). (Pouco eficiente).
* **Complemento de Dois:** Padrão atual. Inverte os bits e soma 1. Permite operações aritméticas diretas sem complicações.

## 5. Representação de Texto (Codificação)
Para guardar letras, usamos tabelas que mapeiam **Número $\to$ Caractere**.

* **ASCII (American Standard):** Usa 7 ou 8 bits. Cobre letras do inglês, números e pontuação básica. Não tem acentos (ã, é, ç).
* **Unicode (UTF-8):** O padrão mundial atual. Pode usar até 32 bits por caractere. Cobre **todos** os idiomas (Japonês, Árabe) e até Emojis (😎).

---

## Resumo Rápido
* **Bit:** 0 ou 1. **Byte:** 8 bits.
* **Bases:** Binário (Máquina), Decimal (Humano), Hexa (Simplificação para programadores).
* **Texto:** **ASCII** é antigo e limitado. **Unicode (UTF-8)** é o padrão global moderno.
* **Hexadecimal:** Essencial para entender endereços de memória e cores.
