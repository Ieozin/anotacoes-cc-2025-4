# Tema 04: Modelagem Lógica e Física de Dados
**Data:** 28/01/2026 | **Status:** Concluído

Neste tema, aprendemos a transformar o Modelo Conceitual (DER) em um **Modelo Lógico (Relacional)** e, finalmente, implementar o **Modelo Físico** no SGBD, garantindo performance e integridade através da normalização e indexação. 💾🚀

---

## 1. O Modelo Relacional
O modelo relacional representa os dados em tabelas (relações).

*   **Tuplas:** São as linhas da tabela (registros).
*   **Atributos:** São as colunas (campos).
*   **Domínio:** O conjunto de valores permitidos para uma coluna (ex: tipo `INT`, `VARCHAR`).

### Tipos de Chaves
| Chave | Descrição |
| :--- | :--- |
| **Primária (PK)** | Identificador único da linha. Não aceita nulos e não repete. |
| **Composta** | Chave primária formada por duas ou mais colunas. |
| **Estrangeira (FK)** | Coluna que estabelece um relacionamento com a PK de outra tabela. |
| **Candidata** | Atributo que tem potencial para ser PK (ex: CPF e Matrícula). |
| **Alternativa** | A chave candidata que *não* foi escolhida como primária. |

---

## 2. Mapeamento Conceitual-Lógico
Regras para transformar o DER em tabelas:

### Entidades
*   **Entidade Forte:** Vira uma tabela própria com sua PK.
*   **Entidade Fraca:** Vira uma tabela cuja PK é composta pela sua própria chave parcial + a PK da entidade forte (proprietária).

### Relacionamentos
*   **1:1:** Geralmente adiciona-se a PK de uma tabela como FK na outra (ou fundem-se as tabelas).
*   **1:N:** A PK do lado "1" vira FK no lado "N".
*   **N:N:** Cria-se uma nova **tabela associativa** contendo as PKs de ambas as entidades como FKs.
*   **Atributos Multivalorados:** Devem virar uma nova tabela relacionada.

---

## 3. Normalização (1FN, 2FN e 3FN)
Processo para eliminar redundâncias e anomalias de atualização.

1.  **Primeira Forma Normal (1FN):** Exige valores **atômicos** (simples). Proíbe atributos compostos ou multivalorados.
2.  **Segunda Forma Normal (2FN):** Estar na 1FN + não possuir **dependências parciais** (todo atributo não-chave deve depender da PK inteira, e não apenas de parte dela).
3.  **Terceira Forma Normal (3FN):** Estar na 2FN + não possuir **dependências transitivas** (um atributo não-chave não pode depender de outro atributo não-chave).

---

## 4. Aspectos Físicos e Performance

### Transações (ACID)
Para garantir a confiabilidade, as transações devem ser:
*   **A**tômicas: Tudo ou nada.
*   **C**onsistentes: Leva o banco de um estado válido a outro.
*   **I**soladas: Uma transação não interfere na outra enquanto executa.
*   **D**uráveis: Uma vez gravado, o dado não se perde.

### Indexação
Estruturas auxiliares que aceleram a busca de dados.
*   **Prós:** Consultas muito mais rápidas.
*   **Contras:** Ocupa mais espaço em disco e deixa as operações de inserção/atualização (`INSERT`/`UPDATE`) mais lentas, pois o índice precisa ser atualizado.

### Desnormalização
Técnica de introduzir redundância proposital (violando as FNs) para ganhar desempenho em consultas complexas ou relatórios pesados. Deve ser usada com cautela!

---

## ## Resumo Rápido 📋
*   **PK:** Única e obrigatória. **FK:** Ponte entre tabelas.
*   **Normalização:** Menos redundância, mais tabelas.
*   **Mapeamento N:N:** Sempre gera uma tabela nova.
*   **Índices:** Bom para ler (`SELECT`), "caro" para escrever.
*   **Integridade Referencial:** FKs garantem que você não aponte para um registro que não existe.