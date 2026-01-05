# Tema 3: Projeto de Banco de Dados - Modelagem Conceitual
**Data:** 05/01/2026 | **Status:** Concluído

## 1. Etapas de um Projeto de DB
Antes de criar a tabela no PostgreSQL, precisamos projetar.
1.  **Levantamento de Requisitos:** Entender o negócio (entrevista com cliente).
2.  **Modelo Conceitual (Alto Nível):** Diagramas focados no entendimento humano (independente de software).
3.  **Modelo Lógico:** Tradução para tabelas, chaves primárias e estrangeiras.
4.  **Modelo Físico:** Script SQL e configurações de servidor.

## 2. O Modelo Conceitual (DER)
Usamos o **Diagrama de Entidade e Relacionamento**.
* **Abstração:** Focamos no "O QUE" será armazenado, não "COMO".

### Elementos do DER


1.  **Entidade (Retângulo):** Objeto do mundo real (Ex: `Aluno`, `Produto`).
2.  **Atributo (Elipse):** Característica da entidade.
    * *Identificador (Chave):* Único (Ex: CPF, Matrícula). Bolinha preenchida.
    * *Atômico:* Simples (Ex: Sexo).
    * *Composto:* Pode ser dividido (Ex: Endereço -> Rua, CEP, Bairro).
3.  **Relacionamento (Losango):** Ação ou ligação entre entidades (Ex: Aluno *cursa* Disciplina).

## 3. Cardinalidade
Define a quantidade de ocorrências no relacionamento (Min, Max).
* **(1,1):** Um para Um (Ex: Marido e Esposa).
* **(1,N):** Um para Muitos (Ex: Cliente faz Pedidos).
* **(N,N):** Muitos para Muitos (Ex: Aluno cursa Disciplinas).
