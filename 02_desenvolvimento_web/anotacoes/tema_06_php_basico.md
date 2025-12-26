# Tema 6: Programação de Páginas Dinâmicas com PHP
**Data:** 24/12/2025 | **Status:** Concluído

## 1. O que é PHP?
* **Sigla:** Hypertext Preprocessor.
* **Definição:** Linguagem de script **Server-Side** (Lado do Servidor).
* **Como funciona:**
    1. O navegador pede a página.
    2. O servidor roda o código PHP.
    3. O servidor envia **apenas HTML** puro para o navegador.
    * *Segurança:* O usuário nunca vê o código fonte PHP, apenas o resultado.

## 2. Sintaxe Básica
Todo código PHP deve estar dentro das tags delimitadoras.

* **Delimitador:** `<?php ... ?>`
* **Arquivos:** Devem ter a extensão `.php`.
* **Variáveis:** Sempre começam com o cifrão (`$`). Ex: `$idade`.
* **Comentários:** `//` (uma linha) ou `/* ... */` (várias linhas).
* **Concatenação:** Usa-se o ponto (`.`) para juntar textos.

## 3. Estruturas de Controle
A lógica é muito parecida com C, C++ e Java.

* **Condicional:** `if`, `else`, `elseif`, `switch`.
* **Repetição:** `for`, `while`, `do/while`.
* **Foreach:** Um loop especial para percorrer listas (arrays).

## 4. Arrays (Vetores)
Diferente de algumas linguagens, no PHP os arrays são super flexíveis.

```php
<?php
    // Criando um array
    $frutas = array("Maçã", "Banana", "Uva");
    
    // Acessando pelo índice (começa no 0)
    echo "Eu gosto de " . $frutas[1]; // Saída: Eu gosto de Banana
?>
```

## Resumo Rápido
Server-Side: O código roda no servidor, não no navegador.

Variáveis: Sempre use $.

Dinâmico: PHP gera HTML diferente dependendo de quem acessa ou do horário (ex: "Bom dia, Leonardo").