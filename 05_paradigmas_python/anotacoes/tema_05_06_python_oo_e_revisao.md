# Tema 05 e 06: Python Orientado a Objetos e Revisão Geral
**Data:** 29/01/2026 | **Status:** Concluído

Neste módulo, exploramos o paradigma de **Programação Orientada a Objetos (POO)**, que aproxima a codificação do mundo real através de classes, objetos e herança. Além disso, consolidamos os fundamentos da linguagem em uma revisão focada para avaliação.

---

## 1. Pilares da POO (Tema 5)

A POO organiza o software em torno de **Objetos** (instâncias) e **Classes** (moldes).

### 🏛️ Classes e Objetos
*   **Classe:** Um "blueprint" ou blueprint que define atributos (dados) e métodos (comportamento).
*   **Objeto:** Uma instância física na memória de uma classe.
*   **`self`:** Parâmetro obrigatório em métodos de instância que referencia o próprio objeto.
*   **`__init__`:** O método construtor, usado para inicializar o estado do objeto.

```python
class Televisao:
    def __init__(self, canal_inicial, min, max):
        self.canal = canal_inicial
        self.canal_min = min
        self.canal_max = max

    def aumentar_canal(self):
        if self.canal < self.canal_max:
            self.canal += 1
        else:
            self.canal = self.canal_min
```

### 🧬 Associação entre Objetos
1.  **Agregação:** Uma relação "tem um", mas os objetos podem existir de forma independente (ex: Biblioteca e Livros). Representada pelo losango vazado.
2.  **Composição:** Uma relação de posse forte onde o ciclo de vida do objeto dependente está ligado ao principal (ex: Conta e Extrato). Representada pelo losango preenchido.

### 🛡️ Encapsulamento e Propriedades
Visa proteger os dados internos contra alterações indevidas.
*   **Atributos Privados:** Em Python, usamos dois underscores (`__saldo`).
*   **Name Mangling:** O Python renomeia internamente para `_Classe__atributo`.
*   **`@property`:** Decorador usado para criar "Getters" de forma elegante.
*   **`@setter`:** Usado para validar dados antes de alterar um atributo.

### 🔝 Herança e Polimorfismo
*   **Herança Simples/Múltipla:** Uma subclasse herda atributos e métodos de uma ou mais superclasses.
*   **`super()`:** Função para invocar métodos da classe pai.
*   **Polimorfismo:** Capacidade de métodos com o mesmo nome se comportarem de forma diferente em subclasses (Sobrescrita/Override).

### 🧩 Classes Abstratas
Utilizam o módulo `abc`. Uma classe abstrata **não pode ser instanciada** e serve apenas como modelo para garantir que subclasses implementem métodos específicos (`@abstractmethod`).

---

## 2. Tratamento de Exceções

Essencial para a robustez do sistema, permitindo que o programa lide com erros sem encerrar abruptamente.

| Componente | Função |
| :--- | :--- |
| **`try`** | Bloco de código onde o erro pode ocorrer. |
| **`except`** | Captura a exceção e define o plano de ação. |
| **`raise`** | Lança manualmente uma exceção (pode ser customizada). |
| **`finally`** | Bloco que sempre será executado, independente de erro. |

---

## 3. Revisão Geral (Tema 6)

Resumo dos conceitos fundamentais para a prova:

*   **Paradigma Multiparadigma:** Python suporta programação imperativa, estruturada e orientada a objetos.
*   **Tradução de Código:**
    *   **Compilada:** Traduz tudo uma vez (Ex: C++).
    *   **Interpretada:** Traduz e executa linha por linha (Ex: Python).
*   **Tipagem Dinâmica e Forte:** O tipo é definido em tempo de execução e o Python não permite operações ilegais entre tipos diferentes sem conversão explícita.
*   **Aplicações Práticas:** Desenvolvimento de jogos, automação e análise de dados.

---

## ## Resumo Rápido 🚀

*   **Classes:** São moldes. **Objetos:** São os exemplares.
*   **Encapsulamento:** Use `_` para protegido e `__` para privado (convenção).
*   **Agregação:** Independente. **Composição:** Dependência de vida.
*   **Herança:** Reutiliza código. **Polimorfismo:** Redefine comportamento.
*   **Abstract Classes:** Definem obrigações para as subclasses.
*   **Exceptions:** `ZeroDivisionError` e `TypeError` são comuns; trate-os com `try/except`.