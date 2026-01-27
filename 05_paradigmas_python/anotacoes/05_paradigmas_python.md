# Temas 1 e 2: Apresentação e Paradigmas em Python
**Data:** 26/01/2026 | **Status:** Concluído

## 1. Apresentação da Disciplina (Tema 1)
O objetivo desta matéria é ir além da sintaxe básica. Vamos entender **como** as linguagens funcionam e **por que** escolhemos Python para resolver problemas modernos.

### O que vamos estudar?
1.  **Paradigmas:** Os "estilos" de programação (Imperativo, Orientado a Objetos, Funcional).
2.  **Python Básico:** Variáveis, tipos e lógica.
3.  **Python Estruturado:** Controle de fluxo e subprogramas.
4.  **Orientação a Objetos (OO):** Classes, herança e polimorfismo.

---

## 2. Paradigmas e Linguagem Python (Tema 2)

### Classificação das Linguagens
As linguagens evoluíram para ficar mais próximas da linguagem humana e mais longe do código de máquina (binário).

* **Baixo Nível:** Próximo ao hardware. Ex: Assembly, Código de Máquina. Difícil de ler, mas execução muito rápida.
* **Alto Nível:** Próximo à linguagem humana (inglês). Ex: Python, Java. Fácil manutenção e alta produtividade.

### Critérios de Avaliação
O que faz uma linguagem ser "boa"?
1.  **Legibilidade (Readability):** Facilidade de ler e entender o código. (Ponto forte do Python).
2.  **Redigibilidade (Writability):** Facilidade de escrever o código.
3.  **Confiabilidade:** O código se comporta como esperado e trata erros de forma segura.
4.  **Custo:** Tempo de treinamento, desenvolvimento e execução.

### Tradução: Compilação vs. Interpretação
O computador não entende Python ou C. Ele precisa de um tradutor.

| Tipo | Como funciona | Exemplo |
| :--- | :--- | :--- |
| **Compilador** | Traduz o código inteiro **uma única vez** criando um executável (.exe). Se tiver um erro, ele nem roda. | C, C++ |
| **Interpretador** | Traduz e executa **linha por linha** em tempo real. Mais lento, mas facilita testes e desenvolvimento. | Python, PHP, JS |
| **Híbrido** | Compila para um código intermediário (Bytecode) e depois interpreta. | Java |

### Paradigmas de Programação
Um paradigma é um **modelo** ou padrão de desenvolvimento. Python é **Multiparadigma**, ou seja, aceita vários estilos.

1.  **Imperativo (Procedural):** Foca no *COMO* fazer. É uma lista de instruções passo a passo, alterando estados e variáveis.
    * *Ex:* C, Pascal, Python Básico.
2.  **Orientado a Objetos (POO):** Foca em *QUEM* faz. Organiza o código em **Classes** e **Objetos** que interagem entre si. Tenta imitar o mundo real.
    * *Ex:* Java, C++, Python.
3.  **Funcional:** Foca no *QUE* fazer. Baseado em funções matemáticas, sem alterar estados (imutabilidade).
    * *Ex:* Haskell, Lisp, (Python suporta parcialmente).
4.  **Lógico:** Baseado em fatos e regras de inferência.
    * *Ex:* Prolog.

### Por que Python?
* É **Interpretada** (desenvolvimento rápido).
* É **Multiparadigma** (flexível).
* É **Fortemente Tipada** (não soma texto com número sem converter), mas **Dinâmica** (não precisa declarar o tipo da variável antes, ex: `x = 10` em vez de `int x = 10`).

---

## Resumo Rápido
* **Python:** Linguagem de Alto Nível, Interpretada e Multiparadigma.
* **Compilador:** Traduz tudo antes. **Interpretador:** Traduz na hora.
* **Imperativo:** Receita de bolo (passo a passo).
* **OO:** Objetos interagindo.
* **Legibilidade:** É o critério onde Python brilha (parece inglês).