# Tema 3: Gráficos e Interpretações Gráficas (Parte 1 - Intervalos)
**Data:** 27/10/2025

## Introdução e Importância dos Gráficos

Gráficos são muito importantes. Ver tudo só por números é complicado. Gráficos ajudam a entender e visualizar dados, tipo valores da bolsa, por exemplo. Uma planilha gigante é difícil de ler, um gráfico simplifica. Claro que simplificar pode ter perda de informação, mas a visualização é o ponto principal.

## 1. Conceitos de Intervalos (Revisão e Aprofundamento)

Essa parte é uma revisão do que já vi em Teoria dos Conjuntos, mas focando na representação gráfica.

### A Reta Real (R)
* Representa todos os números reais (racionais e irracionais).
* É infinita, organizada de `-∞` a `+∞`.

### Representação Gráfica de Intervalos
* **Bola Fechada (`●`):** Indica que o extremo **está incluído** no intervalo. Corresponde a `≤` e `≥` e aos colchetes `[` `]`.
* **Bola Aberta (`○`):** Indica que o extremo **NÃO está incluído**. Corresponde a `<` e `>` e aos parênteses `()` ou colchetes invertidos `]` `[`.

**Meu entendimento da notação (reforço):**
* Colchete "abraçando" o número (`[a` ou `b]`) significa que o número está dentro (fechado).
* Colchete "virado de costas" (`]a` ou `b[`) ou parênteses `(` `)` significa que o número está fora (aberto). Usar parênteses `()` para aberto parece mais simples e direto.

### Classificação e Exemplos (Vídeos)
* **Intervalo Fechado:** Inclui os dois extremos. `[a, b] = {x ∈ R | a ≤ x ≤ b}`. É um segmento de reta.
* **Intervalo Aberto:** Exclui os dois extremos. `(a, b) = {x ∈ R | a < x < b}`.
* **Intervalo Semiaberto/Semifechado:** Um lado aberto, outro fechado. `[a, b)` ou `(a, b]`.
* **Semirretas (Intervalos Ilimitados):** Vão até `+∞` ou vêm de `-∞`.
    * `[a, +∞) = {x ∈ R | x ≥ a}` (Fechada em `a`)
    * `(a, +∞) = {x ∈ R | x > a}` (Aberta em `a`)
    * `(-∞, b] = {x ∈ R | x ≤ b}` (Fechada em `b`)
    * `(-∞, b) = {x ∈ R | x < b}` (Aberta em `b`)
    * `(-∞, +∞) = R` (A reta toda)

### Amplitude do Intervalo
* É o "tamanho" do intervalo: `Amplitude = Limite Superior (LS) - Limite Inferior (LI)`.
* **Importante:** A amplitude é a mesma se o intervalo for aberto ou fechado nos extremos. Ex: `[-4, 2]` e `(-4, 2)` ambos têm amplitude `2 - (-4) = 6`. A lógica é que podemos chegar "infinitamente perto" do limite aberto.
* Semirretas têm amplitude infinita.

### Intervalos no Cotidiano (Exemplo do Vídeo)
* Manifestação: começou com 20.000, chegou a 23.000.
    * O número de manifestantes `x` em qualquer instante está no intervalo `[20000, 23000]`. É um intervalo fechado porque esses valores foram estimados/atingidos.
    * Afirmação III (Se `x` é um número *real* no intervalo `[10000, 13000]`, `x` representa a quantidade?) -> Falso. Número de pessoas é natural (ou inteiro não negativo), não real.

### Atividade Discursiva (Trimestre)
* Caracterizar o segundo trimestre (Abril, Maio, Junho) como intervalo.
* Mapeando meses para números: Jan=1, Fev=2, ..., Abr=4, Mai=5, Jun=6, ... Dez=12.
* Resposta: O intervalo que inclui os números 4, 5 e 6 é `[4, 6]`.

### Verificando o Aprendizado
* **Questão 1:** Associar gráfico com notação.
    * Gráfico I: Aberto em -1, Fechado em 5 -> `(-1, 5]` ou `{x ∈ R | -1 < x ≤ 5}`.
    * Gráfico II: Fechado em 0.5, Aberto em 3.14 -> `[0.5, 3.14)` ou `{x ∈ R | 0.5 ≤ x < 3.14}`.
    * **Resposta Correta: B.** (Ok)
* **Questão 2:** Desempenho do corredor. Onde a velocidade foi `>= 99%`?
    * Olhando o gráfico: 99% ocorre em 50m, 100% em 60m, 99% em 70m, 98% em 80m.
    * O intervalo onde foi *maior ou igual* a 99% é dos 50m até (incluindo) os 80m.
    * **Resposta Correta: A `[50, 80]`**. (Ok)

---
*Terminei o submódulo "Conceitos de intervalos" do Tema 3.*