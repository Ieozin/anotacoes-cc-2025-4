# Tema 7: Arquitetura CISC x RISC
**Data:** 20/01/2026 | **Status:** Concluído

## 1. O Conceito de ISA (Instruction Set Architecture)
Antes de comparar, precisamos entender que todo processador tem um "vocabulário" nativo. Esse conjunto de instruções que o hardware entende é chamado de ISA.
Existem duas filosofias principais de como criar esse vocabulário.

## 2. CISC (Complex Instruction Set Computer)
**Filosofia:** "Hardware complexo, Software simples".
O objetivo era economizar memória RAM (que era caríssima antigamente) criando instruções poderosas que fazem várias coisas ao mesmo tempo.

* **Características:**
    * Instruções complexas e de tamanho variável.
    * Poucos registradores.
    * Faz muito trabalho com apenas uma linha de código Assembly.
    * **Hardware:** Difícil de projetar, ocupa mais silício.
* **Exemplos:** Intel x86, AMD (Desktops e Laptops).

## 3. RISC (Reduced Instruction Set Computer)
**Filosofia:** "Hardware simples, Software (Compilador) inteligente".
A ideia é ter instruções pequenas, simples e muito rápidas, otimizadas para **Pipeline**.

* **Características:**
    * Instruções simples e de tamanho fixo.
    * Muitos registradores (para evitar ir à RAM).
    * Arquitetura **Load/Store**: Só acessa a memória para carregar ou salvar; o processamento ocorre apenas nos registradores.
    * **Hardware:** Mais simples, menor consumo de energia e gera menos calor.
* **Exemplos:** ARM (Celulares, Apple M1/M2/M3), MIPS.



## 4. Comparativo Direto

| Característica | CISC (Intel/AMD) | RISC (ARM) |
| :--- | :--- | :--- |
| **Foco** | Hardware | Software (Compilador) |
| **Instruções** | Complexas, tamanho variável | Simples, tamanho fixo |
| **Ciclos de Clock** | Vários ciclos por instrução | 1 ciclo por instrução (idealmente) |
| **Uso de RAM** | Eficiente (Código menor) | Intenso (Código maior) |
| **Pipeline** | Difícil implementação | Fácil e eficiente |
| **Consumo** | Alto | Baixo (Eficiência energética) |

## 5. A Realidade Atual: Híbridos
Hoje em dia, a linha que divide os dois está borrada.
* Os processadores **CISC** modernos (Intel Core, Ryzen) internamente traduzem suas instruções complexas em micro-operações simples (estilo RISC) para ganhar velocidade.
* Os processadores **RISC** ganharam instruções mais complexas para lidar com multimídia e IA.

---

## Resumo Rápido
* **CISC:** O "faz-tudo". Instruções poderosas, hardware complexo. Domina PCs.
* **RISC:** O "especialista". Instruções simples e rápidas. Domina Celulares.
* **Tendência:** O mundo mobile impulsionou o RISC devido à eficiência de bateria.