# Tema 08: Laboratório Prático - Otimização e Resolução de Problemas
**Data:** 03/02/2026 | **Status:** Concluído

## 1. Estudo de Caso: Otimização de Performance
**Cenário:** Um sistema em produção apresenta lentidão extrema em uma consulta que envolve múltiplas junções e agregações, degradando com o aumento do volume de dados.

### Estratégias de Solução
Para resolver gargalos de performance (Slow Queries), aplicamos as seguintes técnicas:

1.  **Indexação:** Criar índices nas colunas utilizadas nas cláusulas `JOIN` e `WHERE`. Isso evita que o banco leia a tabela inteira (Full Table Scan).
2.  **Refatoração da Consulta:** Simplificar a query, quebrando-a em subconsultas menores ou removendo processamento desnecessário.
3.  **Particionamento:** Em tabelas gigantes, dividir os dados fisicamente (ex: por data ou região) para melhorar a leitura.

## 2. Decisões de Arquitetura e Modelagem
Lições extraídas de cenários de modelagem complexa.

| Cenário | Solução Recomendada | Justificativa |
| :--- | :--- | :--- |
| **Big Data Não Estruturado** | **NoSQL** | Relacionais exigem estrutura rígida. NoSQL oferece escalabilidade e flexibilidade para dados diversos. |
| **Independência Lógica** | **Alterar esquema lógico sem afetar externo** | Permite evoluir o banco (ex: adicionar colunas) sem quebrar a aplicação que o consome. |
| **Relacionamento N:N** | **Entidade Associativa** | Ex: Alunos e Cursos. Cria-se uma tabela intermediária (ex: Inscrição) para gerenciar a ligação. |
| **Relacionamento Ternário** | **Entidade Centralizadora** | Ex: Professor orienta Aluno em um Projeto. Uma única entidade "Orientação" liga as três pontas. |
| **Herança (Tipos)** | **Generalização/Especialização** | Ex: Funcionário (Genérico) -> Professor e Técnico (Específicos). Evita campos nulos e duplicação. |

## 3. Integridade e Normalização (ACID e FN)
Garantindo que os dados sejam confiáveis e sem redundância.

### Propriedades ACID (Transações)
* **Atomicidade:** "Tudo ou Nada". Se uma parte falhar, toda a transação é revertida (`ROLLBACK`). O banco nunca fica em estado parcial.
* **Durabilidade:** Uma vez confirmado (`COMMIT`), o dado persiste mesmo se o servidor cair ou faltar luz.

### Normalização Prática
* **2ª Forma Normal (2FN):** Resolve a **Dependência Parcial**.
    * *Regra:* Toda coluna não-chave deve depender da Chave Primária *inteira*. Se depender só de uma parte da chave composta, deve ir para outra tabela.
* **3ª Forma Normal (3FN):** Resolve a **Dependência Transitiva**.
    * *Regra:* Coluna não deve depender de outra coluna que não seja a chave. (Ex: O nome do departamento depender do ID do departamento, não do ID do funcionário).

## 4. SQL Avançado e Segurança de Operações
Comandos críticos para manutenção e relatórios.

### Manipulação de Estrutura (DDL)
* **Remoção com Dependência:** Ao tentar apagar uma tabela que possui amarras (FKs), use `DROP TABLE tabela CASCADE` para remover as restrições automaticamente.
* **Adição de Colunas:** Use `ALTER TABLE tabela ADD COLUMN coluna tipo`. Nunca tente usar `CHECK` ou `DEFAULT` como substituto de criação de coluna.

### Consultas e Filtros (DQL)
* **WHERE vs HAVING:**
    * `WHERE`: Filtra linhas **antes** de agrupar.
    * `HAVING`: Filtra o resultado da agregação (ex: `COUNT(*) > 100`) **após** o agrupamento.
* **Perigo do CROSS JOIN:** Realiza um produto cartesiano (todas as linhas de A x todas as linhas de B). Em tabelas grandes, isso trava o banco. Use `INNER JOIN`.
* **Operador EXCEPT:** Útil para achar "buracos". Ex: Clientes Inativos = (Todos Clientes) `EXCEPT` (Clientes Ativos).

## Resumo Rápido
1.  **Lentidão?** Crie índices e revise a query.
2.  **Transação falhou?** `ROLLBACK` garante a Atomicidade.
3.  **Dados repetidos?** Normalização (2FN e 3FN).
4.  **Agregação (Count/Sum)?** O filtro é no `HAVING`, não no `WHERE`.