# Tema 6: Processamento em Paralelo
**Data:** 19/01/2026 | **Status:** Concluído

## 1. O Problema do Desempenho
Durante décadas, a estratégia para melhorar computadores foi aumentar a frequência do clock (GHz). Porém, atingimos barreiras físicas:
* **Calor:** Alta frequência gera calor excessivo.
* **Consumo de Energia:** Inviável para baterias.
* **Litografia:** Limite de tamanho dos transistores.

A solução foi mudar o paradigma: em vez de *um* processador super-rápido, usamos *vários* processadores eficientes trabalhando ao mesmo tempo.

## 2. Tipos de Paralelismo
Como executar mais de uma coisa ao mesmo tempo?

### A. Pipelining (Superpipeline)
É a técnica de "Linha de Montagem". Em vez de esperar uma instrução terminar totalmente para começar a próxima, dividimos a instrução em estágios (Busca, Decodifica, Executa).
* *Exemplo:* Enquanto a instrução A está sendo executada, a B está sendo decodificada e a C está sendo buscada.



### B. Superescalar
O processador possui múltiplas unidades de execução (várias ULAs). Isso permite despachar duas ou mais instruções em um único ciclo de clock.

## 3. Arquiteturas Multiprocessadas
Quando o paralelismo sai de dentro de um único núcleo e passa a usar múltiplos núcleos ou processadores.

### Multicore (Múltiplos Núcleos)
É a padrão atual (Intel Core i5, i7, Ryzen).
* Coloca-se dois ou mais processadores independentes ("cores") dentro do mesmo chip físico.
* Compartilham a memória Cache L3 e o acesso à RAM.
* **Vantagem:** Melhor desempenho por watt e capacidade de rodar vários programas (multitarefa) sem travar.



### SMP (Multiprocessamento Simétrico)
* Dois ou mais processadores idênticos conectados a uma única memória principal compartilhada.
* O Sistema Operacional gerencia todos os processadores como se fossem um recurso único.

## 4. Computação de Alto Desempenho
O paralelismo é a base para:
* **GPUs:** Placas de vídeo têm milhares de núcleos pequenos para processar pixels em paralelo.
* **Clusters/Nuvem:** Vários computadores ligados em rede trabalhando em um problema único.

---

## Resumo Rápido
* **Pipeline:** Linha de montagem de instruções (paralelismo no nível da instrução).
* **Multicore:** Vários cérebros no mesmo chip (paralelismo no nível da tarefa).
* **Motivação:** Aumentar o clock não é mais viável fisicamente (esquenta demais).