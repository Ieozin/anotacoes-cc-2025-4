# Tema 3: Componentes de Hardware
**Data:** 14/01/2026 | **Status:** Concluído

## 1. Estrutura Básica e Interconexão
O computador não é um bloco único, mas peças conversando entre si.
* **Barramento (Bus):** É a "estrada" por onde os dados trafegam. Conecta CPU, Memória e Periféricos.
    * *Barramento de Dados:* Carrega a informação real.
    * *Barramento de Endereço:* Indica *onde* a informação deve ser buscada ou gravada na memória.
    * *Barramento de Controle:* Sinais de comando (ex: "Leitura" ou "Escrita").

## 2. Subsistema de Processamento (A CPU)
Responsável pelo ciclo **Busca-Decodifica-Executa**.
* **Datapath (Caminho de Dados):** Onde a operação acontece. Inclui a **ULA** (Unidade Lógica e Aritmética) e os **Registradores**.
* **Unidade de Controle (UC):** O "maestro". Interpreta as instruções e diz para a ULA o que fazer.
* **Clock:** O relógio que dita o ritmo. Medido em GHz (bilhões de ciclos por segundo).

## 3. Subsistema de Memória (A Hierarquia)
Existe um compromisso eterno entre **Velocidade, Custo e Capacidade**. Para equilibrar, usamos uma pirâmide:

1.  **Registradores (Topo):** Dentro da CPU. Velocidade extrema, capacidade minúscula.
2.  **Memória Cache (L1, L2, L3):** Muito rápida, cara. Guarda dados usados com frequência para a CPU não ter que ir buscar longe.
3.  **Memória Principal (RAM):** Rápida, volátil. Onde ficam os programas abertos.
4.  **Memória Secundária (HD/SSD):** Lenta, barata, permanente. Armazenamento em massa.

> **Regra:** Quanto mais perto do processador, mais rápida e mais cara é a memória.

## 4. Subsistema de Entrada e Saída (E/S)
Permite a comunicação com o mundo externo.
* **Dispositivos:** Teclado (Entrada), Monitor (Saída), Touchscreen (Híbrido).
* **Controladores:** Circuitos físicos que gerenciam o dispositivo.
* **Drivers:** Software que "ensina" o Sistema Operacional a conversar com o controlador.

## 5. O Papel do Sistema Operacional (SO)
O hardware sozinho é "burro". O SO age como um gerente de recursos e uma camada de abstração.
* **Gerência de Processador:** Decide qual programa usa a CPU agora (Escalonamento).
* **Gerência de Memória:** Aloca espaço na RAM e evita que um app invada a memória do outro.
* **Virtualização:** Capacidade de simular hardware (ex: Máquinas Virtuais).

---

## Resumo Rápido
* **Barramento:** O sistema circulatório dos dados.
* **Hierarquia de Memória:** Registradores > Cache > RAM > HD.
* **Drivers:** Tradutores entre SO e Hardware.
* **SO:** O gerente que impede o caos no uso dos recursos físicos.
