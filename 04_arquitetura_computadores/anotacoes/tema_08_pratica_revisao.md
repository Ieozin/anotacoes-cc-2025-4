# Tema 08: Laboratório Prático e Revisão Final
**Data:** 03/02/2026 | **Status:** Concluído

## 1. Revisão Histórica (Videoaula)
A evolução da computação não foi linear, mas marcada por saltos tecnológicos que permitiram a miniaturização e o aumento de potência.

### A Linha do Tempo Essencial
1.  **Era Mecânica:** Ábaco (cálculo manual) $\to$ Máquina de Pascal (engrenagens).
2.  **Era Eletromecânica:** Colossus (usado na 2ª Guerra para quebra de criptografia).
3.  **1ª Geração (Válvulas):** ENIAC. Computadores de sala inteira, muito calor, programação via cabos físicos.
4.  **2ª Geração (Transistores):** A grande virada. Redução drástica de tamanho e consumo.
5.  **3ª Geração (Circuitos Integrados):** Chips de silício. Início da computação comercial em massa (IBM).
6.  **4ª Geração (Microprocessadores):** Altair, Apple, IBM PC. O computador pessoal.
7.  **Era Moderna:** Mobilidade (Smartphones), IoT (Smart TVs) e Hiperconectividade (Internet).

## 2. Praticando: Lições dos Exercícios
Resumo dos conceitos mais cobrados em avaliações práticas e estudos de caso.

### A. Conversão de Bases (Macetes)
* **Binário para Decimal:** Some as potências de 2 onde o bit é **1**.
    * Ex: `101` $\to$ $(1 \times 4) + (0 \times 2) + (1 \times 1) = 5$.
* **Binário para Hexadecimal:** Agrupe os bits de **4 em 4** (da direita para a esquerda).
    * Ex: `1111 0001`
    * `1111` = 15 = **F**
    * `0001` = 1 = **1**
    * Resultado: **F1**.

### B. Lógica Digital (Resumo de Portas)
Para resolver circuitos rápido:
* **AND (E):** Corta tudo se tiver um **0**. (Série).
* **OR (OU):** Passa tudo se tiver um **1**. (Paralelo).
* **XOR (Ou Exclusivo):** "Os opostos se atraem". Se forem diferentes (0 e 1) dá **1**. Se forem iguais (0 e 0, ou 1 e 1) dá **0**.

### C. Gargalos de Hardware
* **Gargalo de Von Neumann:** A velocidade da CPU aumentou muito mais que a velocidade da Memória. O processador passa muito tempo "esperando" dados virem da RAM.
    * *Solução:* Memória Cache (SRAM) dentro do processador.
* **Volatilidade:**
    * RAM e Cache: Apagam sem energia (Voláteis).
    * HD, SSD e Flash (Pen drive): Mantêm dados sem energia (Não-voláteis).

### D. CISC vs RISC (Palavras-Chave)
* **CISC (PC/Notebook):** Poucas linhas de código, hardware complexo, instruções de tamanho variável.
* **RISC (Celular/Tablet):** Muitas linhas de código, hardware simples (bateria dura mais), instruções de tamanho fixo.

## 3. Resumo da Disciplina para Prova
1.  **Entrada/Saída:** Teclado (Input) $\to$ CPU Processa $\to$ Monitor (Output).
2.  **CPU:** Composta por ULA (Calcula), UC (Comanda) e Registradores (Armazena rápido).
3.  **Clock:** Define o ritmo, mas não é a única métrica de desempenho (Pipeline e Multicore importam mais hoje).
4.  **Bit/Byte:** 1 Byte = 8 bits. É a unidade padrão de armazenamento.