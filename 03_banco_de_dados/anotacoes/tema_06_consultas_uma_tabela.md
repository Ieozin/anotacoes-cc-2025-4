# Tema 6: Consultas em Uma Tabela no PostgreSQL

**Data:** 09/01/2026
**Status:** Concluído

---

## 1. O Comando `SELECT`

O comando `SELECT` é a instrução mais utilizada em SQL. Ele é responsável por **recuperar dados** de uma ou mais tabelas, processo conhecido como *projeção*.

### Sintaxe Básica

```sql
SELECT coluna1, coluna2 FROM tabela;

SELECT * FROM tabela; -- Retorna todas as colunas (evitar em produção)
```

### Alias (Apelido)

O alias permite renomear colunas ou expressões apenas na exibição do resultado, utilizando a palavra-chave `AS`.

```sql
SELECT 
  nome AS "Nome do Cliente",
  salario * 1.1 AS "Salário com Aumento"
FROM funcionarios;
```

---

## 2. Filtrando Dados (`WHERE`)

A cláusula `WHERE` é utilizada para restringir quais **linhas** serão retornadas pela consulta.

### Operadores Comuns

* **Comparação:** `=`, `>`, `<`, `<>` (diferente)
* **Lógicos:** `AND`, `OR`, `NOT`
* **Intervalo (`BETWEEN`):**

```sql
salario BETWEEN 1000 AND 2000
```

* **Lista (`IN`):**

```sql
estado IN ('SP', 'RJ')
```

* **Busca textual (`LIKE`):**

```sql
nome LIKE 'Ana%'
```

* **Verificação de valores nulos:**

```sql
IS NULL
```

---

## 3. Ordenação dos Resultados (`ORDER BY`)

A cláusula `ORDER BY` define a ordenação do resultado da consulta.

```sql
SELECT nome, salario
FROM funcionarios
ORDER BY salario DESC; -- Ordena do maior para o menor
```

---

## 4. Funções de Agregação

Funções de agregação realizam cálculos sobre um conjunto de valores e retornam um único resultado.

* `COUNT(*)` – Conta o número de linhas
* `SUM(coluna)` – Soma os valores de uma coluna
* `AVG(coluna)` – Calcula a média
* `MAX(coluna)` – Retorna o maior valor
* `MIN(coluna)` – Retorna o menor valor

---

## 5. Agrupamento (`GROUP BY` e `HAVING`)

Utilizado para gerar **consultas resumidas** e relatórios.

* `GROUP BY`: Agrupa linhas que possuem valores iguais em uma ou mais colunas
* `HAVING`: Filtra os grupos após o agrupamento (equivalente ao `WHERE` para dados agregados)

### Exemplo

Consulta que retorna a média salarial por departamento, considerando apenas departamentos com média superior a 5000.

```sql
SELECT 
  departamento, 
  AVG(salario) AS media_salarial
FROM funcionarios
GROUP BY departamento
HAVING AVG(salario) > 5000;
```

### Regra Importante

* `WHERE` filtra **linhas individuais** antes do agrupamento
* `HAVING` filtra **grupos** após o `GROUP BY`

---


