# **Tema 2: O Ambiente Web Cliente X Servidor e as Tecnologias**

Data: 01/12/2025  
Status: Iniciado

## **1\. Conceitos Básicos**

* **Ambiente Web:** Sistema distribuído onde vc acessa serviços (sites, apps) via navegador/internet.  
* **Interface:** O meio de comunicação entre o usuário e o sistema (tela, botões).

## **2\. Arquitetura Cliente x Servidor**

A base de como a internet funciona. Saiu do modelo centralizado (Mainframes) para o distribuído (Xerox PARC, anos 70).

* **Cliente (Frontend):** Quem pede o serviço (**Requisição**). É o seu PC, celular, tablet. Inicia a conversa.  
* **Servidor (Backend):** Quem fornece o serviço (**Resposta**). É robusto, fica ligado 24/7 processando pedidos.

### **Evolução das Camadas (Importante p/ prova)**

A arquitetura evoluiu p/ separar responsabilidades e facilitar manutenção.

1. **2 Camadas:** O Cliente falava direto com o Servidor de Dados.  
   * *Problema:* Se mudar uma regra de negócio, tem q atualizar o software em cada cliente. Manutenção pesada.  
2. **3 Camadas:** Entrou o **Servidor de Aplicação** no meio. (Cliente \-\> App \-\> Dados).  
   * *Melhoria:* Centralizou a regra de negócio, mas o cliente ainda tinha software instalado.  
3. **4 Camadas (O Padrão Web Atual):**  
   * **Cliente:** Só precisa do navegador. Zero instalação.  
   * **Servidor Web:** Cuida da interface (entrega o HTML/CSS/JS).  
   * **Servidor de Aplicação:** Roda a lógica pesada.  
   * **Servidor de Dados:** Guarda a informação.  
   * *Vantagem:* Robustez e portabilidade total. O cliente não precisa saber nada do servidor.

## **3\. Comunicação Web (HTTP)**

Tudo na web é um ciclo eterno de **Pedido e Resposta**.

* **Protocolo:** HTTP (HyperText Transfer Protocol).  
* **O Ciclo:**  
  1. **Request (Requisição):** Cliente digita www.site.com ou clica num link.  
  2. **Processamento:** Servidor recebe, roda o código, busca no banco.  
  3. **Response (Resposta):** Servidor devolve o arquivo (HTML) pro navegador mostrar.

### **Tecnologias (Onde roda o quê?)**

* **Client-Side (Lado do Cliente):** Roda no seu navegador. Foco em interface e beleza.  
  * Exemplos: HTML, CSS, JavaScript.  
* **Server-Side (Lado do Servidor):** Roda no servidor. Foco em lógica, segurança e banco de dados.  
  * Exemplos: PHP, Java, Python, Node.js.

## **4\. Páginas Dinâmicas**

* **Estática:** O conteúdo é fixo (só HTML). Igual pra todo mundo.  
* **Dinâmica:** O conteúdo é **gerado na hora** pelo servidor, personalizado (seu feed, seu saldo).

### **Exemplo Prático (PHP)**

Como o dado sai do formulário e chega no servidor.  
**1\. O Formulário (HTML \- Frontend):**  
\<\!-- action: pra onde vai. method: como vai (POST \= escondido no corpo) \--\>  
\<form action="welcome.php" method="POST"\>  
    Nome: \<input type="text" name="nome"\>  
    \<input type="submit"\>  
\</form\>

**2\. O Recebimento (PHP \- Backend):**  
\<\!-- $\_POST é a variável mágica que pega o dado pelo 'name' do input \--\>  
Bem-vindo, \<?php echo $\_POST\["nome"\]; ?\>

* **Métodos de Envio:**  
  * **GET:** Dados vão na URL (site.com?id=10). Rápido, mas **inseguro** p/ senhas.  
  * **POST:** Dados vão no corpo da requisição. Mais seguro e cabe mais coisa.

## **5\. Resumo Prático (Para não esquecer)**

* **Modelo 4 Camadas:** É o melhor pq tira a responsabilidade do cliente. Só precisa de browser.  
* **Request/Response:** A web é um bate-bola constante entre cliente e servidor.  
* **PHP:** Para pegar dados de um form POST, usa $\_POST\["nome\_do\_campo"\]. O comando echo imprime na tela.