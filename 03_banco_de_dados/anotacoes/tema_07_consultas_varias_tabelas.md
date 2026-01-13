# Tema 7: Consulta com Várias Tabelas no PostgreSQL

**Data:** 12/01/2026 | **Status:** Concluído

---

## 1. Junções (JOINs)

No modelo relacional, os dados ficam separados para evitar redundância. O `JOIN` é o mecanismo que permite unir essas tabelas no momento da consulta.

### Principais Tipos de JOIN

1. **INNER JOIN**
   Retorna apenas os registros que possuem correspondência em **ambas** as tabelas (interseção).

   * *Exemplo:* Listar clientes que fizeram pedidos. Quem nunca comprou não aparece.

2. **LEFT JOIN**
   Retorna **todos** os registros da tabela da esquerda (primeira citada) e os correspondentes da tabela da direita. Quando não há correspondência, os valores da direita são preenchidos com `NULL`.

   * *Exemplo:* Listar todos os clientes, inclusive os que nunca compraram.

3. **RIGHT JOIN**
   Retorna **todos** os registros da tabela da direita. É o inverso do `LEFT JOIN`. Pouco usado na prática, pois normalmente prefere-se inverter a ordem das tabelas e usar `LEFT JOIN`.

4. **FULL OUTER JOIN**
   Retorna todos os registros de ambas as tabelas (união). Onde não houver correspondência, o valor será `NULL`.

5. **CROSS JOIN (Produto Cartesiano)**
   Combina cada linha da tabela A com **todas** as linhas da tabela B.

   * **Cuidado:** Se A possui 100 linhas e B possui 1000, o resultado terá 100.000 linhas, o que pode causar lentidão ou travamento do banco.

### Sintaxe Básica de JOIN

```sql
SELECT c.nome, p.data_pedido
FROM clientes c
INNER JOIN pedidos p
    ON c.id = p.cliente_id;
```

---

## 2. Operadores de Conjunto

Tratam os resultados de dois ou mais `SELECT`s como conjuntos matemáticos. As consultas envolvidas devem possuir colunas compatíveis (mesma quantidade e tipos semelhantes).

* **UNION**
  Junta os resultados de duas consultas (`A + B`) e remove duplicatas por padrão.

* **INTERSECT**
  Retorna apenas os registros que existem em **ambos** os resultados (`A ∩ B`).

* **EXCEPT**
  Retorna os registros que existem no primeiro resultado e **não** existem no segundo (`A - B`).

---

## 3. Subconsultas (Subqueries)

Uma subconsulta é um `SELECT` dentro de outro comando SQL.

### Tipos de Subconsulta

* **Subconsulta Aninhada**
  Executada uma única vez. O resultado é utilizado pela consulta externa.

  ```sql
  SELECT *
  FROM produtos
  WHERE preco > (
      SELECT AVG(preco)
      FROM produtos
  );
  ```

* **Subconsulta Correlata**
  Executada uma vez para cada linha da consulta externa. Geralmente é mais lenta, pois depende dos valores da query principal.

---

## Resumo Rápido

* **INNER JOIN:** Apenas registros com correspondência em ambas as tabelas.
* **LEFT JOIN:** Todos os registros da tabela da esquerda, com ou sem correspondência.
* **UNION:** Soma os resultados de consultas.
* **Subquery:** Uma consulta dentro de outra.
