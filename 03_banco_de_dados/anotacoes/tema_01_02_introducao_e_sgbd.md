# Temas 1 e 2: Apresentação e Fundamentos de Banco de Dados
**Data:** 05/01/2026
**Status:** Concluído

## 1. Visão Geral da Disciplina (Tema 1)
Diferente do desenvolvimento web, onde o foco é a interface e a lógica momentânea, aqui o foco é a **persistência** e a **integridade** da informação a longo prazo.

### O Papel do Banco de Dados
* **Persistência:** Garantir que os dados não se percam quando o computador desliga ou o sistema reinicia.
* **Segurança:** Controlar quem acessa o quê (ex: estagiário não vê salário de diretor).
* **Tomada de Decisão:** Transformar dados brutos em inteligência para o negócio (ex: "Qual produto vendeu mais no Natal?").

### O Caminho do Aprendizado
1.  **Modelagem Conceitual:** Desenhar o banco (Diagramas) antes de programar.
2.  **Modelagem Lógica/Física:** Otimizar e criar as tabelas reais.
3.  **SQL (PostgreSQL):** A linguagem para manipular esses dados.

---

## 2. Sistema de Banco de Dados - SGBD (Tema 2)
Entendendo a ferramenta que gerencia tudo isso.

### Conceitos Básicos
* **Dado:** Fato bruto, sem contexto. (Ex: `2500`).
* **Informação:** Dado processado com significado. (Ex: `Salário: R$ 2.500,00`).
* **SGBD (Sistema Gerenciador de Banco de Dados):** É o software que controla o acesso, a organização e a escrita dos dados.
    * *Exemplos:* PostgreSQL, MySQL, Oracle, SQL Server.
    * *Função:* Isolar a aplicação dos arquivos físicos no HD.

### Evolução Histórica
* **Década de 60:** Modelos Hierárquicos (rígidos, parecidos com pastas do Windows).
* **Década de 70 (A Revolução):** Edgar Frank Codd cria o **Modelo Relacional**.
    * *Conceito:* Dados organizados em **tabelas** (linhas e colunas). É o padrão mundial até hoje.
* **Atualidade:** Modelo Relacional convive com **NoSQL** (para Big Data e dados não estruturados).

### Arquitetura ANSI/SPARC (Os 3 Níveis)
Para garantir segurança e independência, um banco é dividido em camadas:
1.  **Nível Externo (Visão):** O que o usuário vê. (Ex: Telas do sistema).
2.  **Nível Conceitual (Lógico):** A estrutura completa do banco (Quais tabelas existem e como se ligam).
3.  **Nível Interno (Físico):** Como os bytes são gravados no disco rígido.

### A Linguagem SQL
Dividida em subconjuntos de comandos:
* **DDL (Definição):** Cria e altera estruturas (`CREATE`, `ALTER`, `DROP`).
* **DML (Manipulação):** Mexe nos dados (`INSERT`, `UPDATE`, `DELETE`).
* **DQL (Consulta):** Busca dados (`SELECT`).

---

## Resumo p/ Revisão Rápida
* **Objetivo:** Persistência de dados confiável.
* **SGBD:** O software (PostgreSQL) que gerencia o banco.
* **Modelo Relacional:** Organização em Tabelas (Linhas e Colunas). Criado por Codd.
* **Abstração:** O usuário (Nível Externo) não precisa saber como os dados estão gravados no HD (Nível Interno).
