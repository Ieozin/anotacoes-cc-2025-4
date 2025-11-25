# Resolução de Problemas: Introdução a Redes e Histórico
**Data:** 24/11/2025
**Status:** Iniciado

## 1. Introdução e Conceitos
As redes evoluíram de mainframes militares/acadêmicos para uso global em dispositivos móveis.
* **O que é:** Conjunto de dispositivos conectados p/ compartilhar informações e recursos.
* **Estrutura:** Para haver comunicação, precisa de:
    * Origem e Destino.
    * Meio de transmissão.
    * Protocolo (regras, ex: TCP/IP).

---

## 2. Paradigmas de Comutação (O Conceito Chave)
A forma como os dados trafegam define a eficiência da rede. A grande virada da internet foi a mudança de Circuitos para Pacotes.

### A. Comutação de Circuitos (Legado/Telefonia)
* **Como funciona:** Cria um **caminho físico dedicado** e exclusivo entre A e B antes de enviar qualquer dado.
* **Processo em 3 fases:**
    1.  **Estabelecimento:** Sinalização cria o caminho.
    2.  **Troca de Dados:** O canal fica preso exclusivamente para essa conversa.
    3.  **Encerramento:** Desfaz o circuito e libera o recurso.
* **Características:**
    * Garante ordem de chegada e velocidade constante.
    * **Problema:** Desperdiça banda se houver silêncio na chamada (o canal continua ocupado).

### B. Comutação de Pacotes (Internet)
* **Como funciona:** A informação é quebrada em pedaços menores ("pacotes"). Não reserva caminho físico.
* **Características:**
    * Cada pacote tem o endereço de origem/destino.
    * Pacotes podem seguir rotas diferentes (roteadores decidem o melhor caminho na hora).
    * Podem chegar fora de ordem (o destino remonta).
    * **Vantagem:** Otimiza a rede. Vários usuários usam o mesmo cabo ao mesmo tempo sem travar o recurso.

---

## 3. Tendências Atuais

### SDN (Redes Definidas por Software)
* **Problema:** Gerenciar redes com muitos equipamentos físicos e heterogêneos é difícil e caro.
* **Solução:** Separar o "cérebro" da rede do "músculo".
    * **Plano de Controle (Software):** Um Controlador Central define as regras e políticas.
    * **Plano de Dados (Hardware):** Os equipamentos apenas encaminham os pacotes seguindo as ordens do controlador.
* **Benefício:** Permite programar e gerenciar a rede toda de forma centralizada.

### IoT (Internet das Coisas)
* **Conceito:** Conectividade expandida para além de PCs e celulares.
* **Aplicação:** Conectar objetos do dia a dia (geladeiras, carros, sensores agrícolas, indústria).
* **Foco:** Coleta massiva de dados e atuação remota.

---

## 4. Resumo dos Exercícios
* **Q1 (Evolução):** O marco principal foi a **Comutação de Pacotes**, que permitiu a escala global da rede.
* **Q2 (Diferenças Técnicas):**
    * **Circuitos:** Exige conexão prévia, segue o mesmo caminho, chega ordenado.
    * **Pacotes:** Sem conexão física dedicada, caminhos distintos (rotas dinâmicas), pode chegar desordenado.

**Ponto de revisão:** Focar na diferença entre Circuitos e Pacotes. É a base de como a internet funciona.