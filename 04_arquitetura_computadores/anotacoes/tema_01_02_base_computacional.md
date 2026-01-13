# Temas 1 e 2: Apresentação e Base Computacional
**Data:** 13/01/2026 | **Status:** Concluído

## 1. Apresentação da Disciplina (Tema 1)
O foco desta matéria é desmistificar a "caixa preta" do computador. Entender o hardware é essencial para tomar decisões melhores no desenvolvimento de software, escolha de infraestrutura e otimização de desempenho.

### O que vamos estudar?
1.  **Base Computacional:** Hardware, Software, SO e Redes.
2.  **Componentes de Hardware:** A estrutura interna (Processador, Memória, I/O).
3.  **Representação de Dados:** Como bits viram números e caracteres.
4.  **Lógica Digital:** Álgebra Booleana e Circuitos.
5.  **Processamento Paralelo:** Arquiteturas Multicore.
6.  **Arquiteturas:** Diferenças entre CISC (Complexo) e RISC (Reduzido).

---

## 2. Base Computacional (Tema 2)
Computadores são máquinas programáveis que processam dados para gerar informação.

### Evolução Histórica
A história é marcada pela miniaturização dos componentes e aumento exponencial de velocidade (Lei de Moore).

| Geração | Tecnologia Principal | Características |
| :--- | :--- | :--- |
| **1ª** | Válvulas | Gigantes (ENIAC), alto consumo de energia, baixa confiabilidade. |
| **2ª** | Transistores | Menores, mais rápidos e mais duráveis. A grande revolução. |
| **3ª** | Circuitos Integrados (CI) | Múltiplos transistores em uma pastilha de silício. |
| **4ª** | Microprocessadores | A CPU inteira em um único chip (Era dos PCs). |

### O Sistema Computacional
Um sistema completo é formado por três pilares:
* **Hardware:** Parte física (o que você chuta).
* **Software:** Parte lógica (o que você xinga).
* **Peopleware:** O usuário ou técnico que opera o sistema.

### A. Hardware (Arquitetura de Von Neumann)
O modelo padrão utilizado até hoje divide o computador em 4 funções:

1.  **Entrada:** Dispositivos que enviam dados (Teclado, Mouse, Sensores).
2.  **Processamento (UCP/CPU):** O "cérebro" que executa as instruções.
    * **UC (Unidade de Controle):** Gerencia o fluxo de dados e busca instruções.
    * **ULA (Unidade Lógica e Aritmética):** Executa cálculos (+, -) e lógica (AND, OR).
    * **Registradores:** Memória interna minúscula e ultra-rápida.
3.  **Armazenamento (Memória):**
    * **Primária (RAM):** Rápida, volátil (apaga sem energia), usada para programas em execução.
    * **Secundária (HD/SSD):** Lenta, não-volátil (permanente), usada para guardar arquivos.
4.  **Saída:** Dispositivos que mostram o resultado (Monitor, Impressora).

### B. Software
* **Software de Sistema:** Fundamental para o funcionamento. Ex: **Sistema Operacional** (Gerencia o hardware) e Drivers.
* **Software de Aplicação:** Focado em tarefas do usuário. Ex: Editores de texto, Navegadores, Jogos.

### C. Redes e Conectividade
A integração permite o compartilhamento de recursos.
* **Rede:** Conjunto de computadores conectados.
* **Internet:** A infraestrutura global de conexões (cabos, satélites, roteadores).
* **WWW (Web):** O sistema de hipermídia (sites) que roda *sobre* a internet.

---

## Resumo Rápido
* **Processo Básico:** Entrada $\to$ Processamento $\to$ Saída.
* **Evolução:** Válvula $\to$ Transistor $\to$ CI $\to$ Microprocessador.
* **CPU:** É composta por UC (Gerente) e ULA (Calculadora).
* **Memória:** RAM é temporária/rápida. HD/SSD é permanente/lento.
* **Conceito Chave:** Hardware e Software dependem um do outro para funcionar.
