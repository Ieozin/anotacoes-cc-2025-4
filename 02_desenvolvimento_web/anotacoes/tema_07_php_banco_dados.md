# Tema 07: Integração do PHP com Banco de Dados (PDO)
**Data:** 28/01/2026 | **Status:** Concluído

Neste tema, exploramos a integração do backend em PHP com Sistemas Gerenciadores de Banco de Dados (SGBD) utilizando a extensão **PDO (PHP Data Objects)**. O foco é a criação de aplicações seguras, portáveis e orientadas a objetos.

---

## 1. A Camada de Abstração: PDO
Diferente das extensões antigas (como `mysql_connect` ou `pgsql_connect`), a **PDO** funciona como uma interface leve que padroniza o acesso aos dados.

*   **Vantagem Principal:** Se você precisar trocar o banco de dados de MySQL para PostgreSQL, o código de manipulação de dados permanece quase idêntico; altera-se apenas a string de conexão (**DSN**).
*   **Drivers Suportados:** Atualmente suporta 12 drivers, incluindo MySQL, PostgreSQL, SQLite, Oracle e SQL Server.

---

## 2. Realizando a Conexão
A conexão é estabelecida instanciando um objeto da classe PDO. É necessário informar o **DSN (Data Source Name)**, o usuário e a senha.

### Exemplo de Conexão (PostgreSQL)
```php
try {
    $host = "localhost";
    $db = "meu_banco";
    $user = "admin";
    $pass = "12345";
    $port = 5432; // Padrão Postgres (MySQL é 3306)

    $dsn = "pgsql:host=$host;port=$port;dbname=$db";
    $conexao = new PDO($dsn, $user, $pass);
    
    echo "Conexão ativa! 🚀";
} catch (PDOException $e) {
    echo "Erro: " . $e->getMessage();
}
```

> **Dica:** Para encerrar uma conexão, basta atribuir `null` à variável da instância: `$conexao = null;`.

---

## 3. Segurança: SQL Injection e Prepared Statements
O **SQL Injection** é um ataque onde comandos maliciosos são inseridos via formulários para manipular o banco. A PDO mitiga isso através do método **Prepare**.

### O Recurso Bind
Nunca concatene variáveis diretamente na string SQL. Use **parâmetros nomeados** ou interrogações.

```php
// Forma Segura (Prepared Statement)
$login = $_POST['user'];
$senha = $_POST['pass'];

$stmt = $conexao->prepare("SELECT * FROM usuarios WHERE login = :login AND senha = :senha");
$stmt->execute([':login' => $login, ':senha' => $senha]);

$usuario = $stmt->fetch(PDO::FETCH_ASSOC);
```

---

## 4. Principais Métodos da Classe PDO

| Método | Função | Retorno |
| :--- | :--- | :--- |
| **`exec()`** | Executa instruções que não retornam dados (INSERT, UPDATE, DELETE). | Número de linhas afetadas. |
| **`query()`** | Executa uma instrução SQL em uma única chamada (SELECT simples). | Objeto `PDOStatement` (ResultSet). |
| **`prepare()`** | Prepara uma instrução para execução segura com `execute()`. | Objeto `PDOStatement`. |
| **`lastInsertId()`**| Retorna o ID da última linha inserida. | String com o ID. |

---

## 5. Recuperação de Dados (Fetch)
Após executar um `SELECT`, usamos métodos para extrair as linhas do resultado:

*   **`fetch()`**: Obtém a próxima linha do conjunto de resultados.
*   **`fetchAll()`**: Obtém todas as linhas de uma vez em um array.
*   **`PDO::FETCH_ASSOC`**: Retorna um array associativo (índices com os nomes das colunas).

```php
$resultSet = $conexao->query("SELECT nome, email FROM clientes");

while ($row = $resultSet->fetch(PDO::FETCH_ASSOC)) {
    echo "Nome: " . $row['nome'] . " | Email: " . $row['email'] . "<br>";
}
```

---

## ## Resumo Rápido 🐘
*   **PDO** é uma interface orientada a objetos para conexão com múltiplos bancos.
*   **DSN** é a string de configuração que define o driver e o endereço do banco.
*   **Try/Catch** é essencial para tratar `PDOException` e não expor senhas em erros de tela.
*   **Prepare/Execute** é a regra de ouro para evitar SQL Injection.
*   **Encapsulamento:** Em cenários reais, recomenda-se o uso do padrão **MVC** para organizar essa integração.