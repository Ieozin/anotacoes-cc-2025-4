# Resolução de Problemas: Introdução a Redes e Histórico
**Data:** 24/11/2025
**Status:** Concluído

## 1. Introdução e Conceitos
As redes saíram dos mainframes militares/acadêmicos para o uso global em smartphones.
* **Definição:** Conjunto de dispositivos conectados p/ compartilhar info e recursos.
* **Estrutura:** Para haver comunicação, precisa de:
    * Origem e Destino.
    * Meio de transmissão.
    * Protocolo (regras, ex: TCP/IP).
* **Elementos:**
    * **Nós:** Quem gera/consome dados (PCs, roteadores).
    * **Enlaces:** O caminho físico (fibra, wi-fi).
    * **Protocolos:** As regras que organizam a bagunça (tratam erros, fluxo).

---

## 2. Comutação (A Virada de Chave)
A forma como os dados trafegam define a eficiência da rede. A internet só escalou por causa da mudança de Circuitos para Pacotes.

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

## 3. Classificação das Redes

### Topologias (O Desenho)
Como os nós são ligados fisicamente ou logicamente.
* **Tipos:** Barramento, Estrela, Anel, Árvore.
* **Malha (Distribuída):** A mais robusta. Se um nó cai, a rede acha outro caminho. É a base da internet.

### Área de Cobertura (Alcance)
* **PAN:** Pessoal (bluetooth).
* **LAN:** Local (casa, escritório).
* **MAN:** Metropolitana (cidade).
* **WAN:** Longa distância (país, mundo).

---

## 4. Meios de Transmissão

### Cabeados (Guiados)
* **Par Trançado:** Barato, mas sofre interferência.
* **Fibra Óptica:** Luz. Cara, mas alcança longe e é **imune** a ruído eletromagnético.

### Sem Fio (Não Guiados)
* **Histórico:** Começou com a **ALOHAnet** (Havaí, 1971), precursora do Wi-Fi.
* **Prós:** Mobilidade, instala onde cabo não chega (prédios históricos).
* **Contras:** Segurança (sinal aberto), interferência, chuva/paredes atrapalham, propagação multivias (sinal reflete).

---

## 5. Redes Móveis e Protocolos
* **Celular:** Divide a área em células (hexágonos) com Estações Base (BS).
    * **Handoff:** Tecnologia que permite trocar de antena sem cair a ligação enquanto você se move.
* **Evitando Colisão (Múltiplo Acesso):**
    * **WiFi:** Usa **CSMA/CA** (escuta antes de falar).
    * **Celular:** Usa **TDMA/FDMA** (divisão rígida de tempo/frequência).

---

## 6. Tendências Atuais (O Futuro)

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

## 7. Resumo Prático das Atividades
* **Q1 (Evolução):** O marco principal foi a **Comutação de Pacotes**, que permitiu a escala global da rede.
* **Q2 (Diferenças Técnicas):**
    * **Circuitos:** Exige conexão prévia, segue o mesmo caminho, chega ordenado.
    * **Pacotes:** Sem conexão física dedicada, caminhos distintos (rotas dinâmicas), pode chegar desordenado.
* **Q3 (Robustez):** Topologia **Distribuída** (Malha) é a mais tolerante a falhas.
* **Q4 (Física):** Fibra óptica é a escolha para imunidade a ruído.
* **Q5 (Wireless):** Handoff é essencial para mobilidade celular; CSMA/CA organiza o WiFi.

**Ponto de revisão:** Focar na diferença entre Circuitos e Pacotes. É a base de como a internet funciona.