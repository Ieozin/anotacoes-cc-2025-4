# Tema 5: Criação e Manipulação de Objetos no PostgreSQL
**Data:** 08/01/2026 | **Status:** Concluído

## 1. Arquitetura e Ferramentas
O PostgreSQL é um SGBD Objeto-Relacional (ORDBMS) robusto e Open Source.
* **Modelo Cliente-Servidor:**
    * **Servidor (`postgres`):** Processo principal que gerencia os arquivos e aceita conexões.
    * **Cliente:** Ferramenta que envia comandos (ex: **psql** via terminal ou **pgAdmin 4** via interface gráfica).

## 2. Tipos de Dados Essenciais
Escolher o tipo certo economiza espaço e evita erros.

| Tipo | Descrição | Exemplo |
| :--- | :--- | :--- |
| `INTEGER` / `SERIAL` | Números inteiros. `SERIAL` é usado para IDs autoincrementais. | `1, 20, 500` |
| `NUMERIC(p,s)` | Números exatos com casas decimais (ideal para dinheiro). | `150.50` |
| `VARCHAR(n)` | Texto de tamanho variável com limite `n`. | `"João da Silva"` |
| `DATE` | Apenas data (Ano-Mês-Dia). | `'2026-01-08'` |
| `BOOLEAN` | Verdadeiro ou Falso. | `TRUE`, `FALSE` |

cc 3. DDL (Data Definition Language)
Comandos que definem a **estrutura** do banco.

### CREATE TABLE (Criar Tabela)


```sql
CREATE TABLE clientes (
    id SERIAL PRIMARY KEY,            -- Chave Primária Automática
    nome VARCHAR(100) NOT NULL,       -- Não aceita nulo
    email VARCHAR(100) UNIQUE,        -- Não pode repetir email
    data_cadastro DATE DEFAULT CURRENT_DATE
);
```

### ALTER TABLE (Alterar Estrutura)
Usado quando o requisito muda no meio do projeto.

```
ALTER TABLE clientes ADD COLUMN telefone VARCHAR(15); -- Adiciona coluna
ALTER TABLE clientes DROP COLUMN data_cadastro;       -- Remove coluna
```

### DROP TABLE (Apagar Tabela)
Cuidado: Apaga a estrutura e todos os dados dentro dela.

### DROP TABLE clientes;
-- Se tiver chave estrangeira apontando pra ela, use: DROP TABLE clientes CASCADE;


## 4. DML (Data Manipulation Language)
Comandos que manipulam os dados dentro das tabelas.

### INSERT (Inserir):
```
INSERT INTO clientes (nome, email) VALUES ('Leonardo', 'leo@email.com');
```

### UPDATE (Atualizar): ⚠️ Sempre use WHERE!

```
UPDATE clientes SET nome = 'Leonardo Martins' WHERE id = 1;
```

### DELETE (Deletar): ⚠️ Sempre use WHERE!

```
DELETE FROM clientes WHERE id = 1;
```

## 5. Transações (Controle e Segurança)
Uma transação é um bloco de operações que deve ser Atômico (Tudo ou Nada). Segue o princípio ACID.

### BEGIN: Inicia a transação.

### COMMIT: Confirma e salva tudo permanentemente.

### ROLLBACK: Cancela tudo e volta ao estado anterior (ideal quando dá erro no meio do processo).

### SAVEPOINT: Cria um ponto de restauração intermediário.

```
BEGIN;
UPDATE conta SET saldo = saldo - 100 WHERE id = 1; -- Tira de A
UPDATE conta SET saldo = saldo + 100 WHERE id = 2; -- Põe em B
COMMIT; -- Se der erro antes disso, nada acontece.
```
