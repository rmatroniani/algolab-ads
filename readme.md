# {;} AlgoLab ADS — Simulador Interativo de Algoritmos e Estruturas de Dados

> **Simulador didático passo a passo em VisuAlg (Portugol), Linguagem C e Python para estudantes do 1º ano de Análise e Desenvolvimento de Sistemas (ADS).**

---

## 🎯 Objetivo Pedagógico

1. **Compreender o Teste de Mesa (Rastreamento de Memória):** Acompanhar como os valores das variáveis (`i`, `j`, `aux`, `meio`, `soma`, etc.) mudam a cada linha executada.
2. **Transitar entre VisuAlg, C e Python:** Visualizar o mesmo algoritmo nas três linguagens — individualmente ou **as 3 lado a lado** — com destaque sincronizado da linha exata em execução.
3. **Dominar a Diferença de Indexação (`Base 1` vs `Base 0`):** Todo vetor e matriz exibe simultaneamente o índice **VisuAlg (`[1..N]`)** e o índice **C / Python (`[0..N-1]`)**, eliminando erros clássicos de *off-by-one* (estouro de limite de vetor).
4. **Visualizar Estruturas Abstratas:** Observar graficamente comparações, trocas de posição (*swaps*), desvios condicionais e laços de repetição acontecendo em tempo real ao lado do código.

---

## 📚 Catálogo de Atividades Disponíveis

O simulador está organizado em **5 módulos fundamentais** da disciplina de Algoritmos e Lógica de Programação:

### 1. Vetores Unidimensionais (1D) — Busca e Algoritmos Clássicos
* **Busca Sequencial (Linear):** Percorre o vetor elemento por elemento até encontrar o valor procurado (`alvo`) ou chegar ao fim. Complexidade: $O(n)$.
* **Busca Binária:** Divide o espaço de busca pela metade a cada iteração utilizando os ponteiros `ini`, `meio` e `fim` em um vetor ordenado. Complexidade: $O(\log n)$.
* **Maior, Menor e Soma:** Percorre o vetor atualizando variáveis acumuladoras (`soma`) e comparadores de extremo (`maior` e `menor`). Complexidade: $O(n)$.

### 2. Vetores Unidimensionais (1D) — Algoritmos de Ordenação
* **Bubble Sort (Ordenação da Bolha):** Compara elementos adjacentes (`v[j]` e `v[j+1]`) e realiza trocas sucessivas utilizando a variável auxiliar `aux`. Complexidade: $O(n^2)$.
* **Selection Sort (Ordenação por Seleção):** Localiza o índice do menor elemento (`menor`) a cada varredura e realiza apenas uma troca ao final do laço interno. Complexidade: $O(n^2)$.
* **Insertion Sort (Ordenação por Inserção):** Elege uma `chave` e desloca os elementos maiores para a direita até inseri-la na posição ordenada. Complexidade: $O(n^2)$.

### 3. Matrizes Bidimensionais (2D)
* **Travessia e Soma de Matriz $M \times N$:** Demonstra o funcionamento de laços aninhados (`para i` nas linhas e `para j` nas colunas) acumulando a soma total dos elementos.
* **Diagonal Principal e Secundária:** Em uma matriz quadrada $N \times N$, destaca as células onde $i = j$ (Diagonal Principal) e onde $i + j = N - 1$ em C/Python ou $i + j = N + 1$ no VisuAlg (Diagonal Secundária).

### 4. Estruturas de Decisão (Condicionais)
* **Par/Ímpar e Positivo/Negativo (`SE / SENAO` | `if / else`):** Avalia expressões lógicas usando o operador de módulo (`%`) e operadores relacionais.
* **Média Escolar Encadeada (`SENAO SE` | `else if` | `elif`):** Demonstra desvios condicionais compostos para classificar o aluno em *Aprovado*, *Em Exame* ou *Reprovado*.
* **Calculadora Menu (`ESCOLHA` | `switch` | `match-case`):** Ilustra estruturas de seleção múltipla baseadas na opção escolhida pelo usuário.

### 5. Estruturas de Repetição (Laços / Loops)
* **Tabuada Interativa (`PARA` | `for`):** Laço contado com número fixo de repetições.
* **Cálculo de Fatorial $N!$ (`ENQUANTO` | `while`):** Uso de variável contadora regressiva (`cont`) e acumulador multiplicativo (`fat`).
* **Série de Fibonacci:** Geração passo a passo dos $N$ primeiros termos atualizando as variáveis `ant`, `atual` e `prox`.

---

## 🖥️ Como o Simulador Funciona (Passo a Passo)

A barra superior da aplicação guia o estudante em **3 passos simples**:

1. **Escolha a Atividade (`Passo 1`):** Selecione no menu suspenso qual estrutura ou algoritmo deseja explorar.
2. **Escolha a Linguagem (`Passo 2`):** Alterne a qualquer momento entre **VisuAlg**, **C**, **Python** ou clique em **3 Lado a Lado** para comparar as sintaxes simultaneamente.
3. **Configure as Entradas (`Passo 3`):**
   * Altere o tamanho $N$ do vetor, digite seus próprios números separados por vírgula ou clique em **🎲 Sortear**.
   * Em algoritmos de busca, defina qual valor deseja procurar.
   * Em matrizes, ajuste o número de linhas ($M$) e colunas ($N$).
   * Em decisão e repetição, modifique as notas, números ou limites do laço.

### ⌨️ Controles de Execução e Atalhos de Teclado

O aluno pode controlar a velocidade do próprio aprendizado avançando ou retrocedendo no algoritmo:

| Tecla / Botão | Ação no Simulador |
| :--- | :--- |
| **`Enter`** ou **`Seta para Baixo (↓)`** | Avança para o **Próximo Passo** da execução |
| **`Seta para Cima (↑)`** | Retorna para o **Passo Anterior** (permite rever uma troca ou comparação) |
| **`Home`** ou botão **`⏮ Início`** | Reinicia a simulação a partir do Passo 1 |
| **Botão `▶ Auto`** | Executa os passos automaticamente em sequência (clique novamente para pausar) |

---

## 🔍 Entendendo a Tela Dividida

* **Painel Esquerdo (Código-Fonte Sincronizado):** Exibe o código adaptado dinamicamente aos valores inseridos pelo aluno. A linha destacada em **amarelo/âmbar** indica a instrução exata que está sendo processada naquele instante.
* **Painel Direito Superior (Demonstração Visual):**
  * 🟨 **Amarelo:** Elementos sendo lidos, comparados ou avaliados no momento.
  * 🟥 **Vermelho/Rosa:** Elementos sofrendo troca de posição (*swap*) ou escrita na memória.
  * 🟩 **Verde:** Elementos já ordenados, encontrados na busca ou condições avaliadas como verdadeiras.
* **Painel Direito Inferior (Teste de Mesa + Terminal):**
  * **Teste de Mesa (RAM Atual):** Mostra os cartões de memória com o valor exato de cada variável naquele passo.
  * **Terminal / Saída:** Simula a tela preta do console exibindo o resultado dos comandos `escreval()`, `printf()` e `print()`.




## 🛠️ Tecnologias Utilizadas

* **HTML5 & JavaScript (ES6+):** Motor de simulação determinístico de estados para geração de passos (*Time-Travel Debugging*).
* **Tailwind CSS (via CDN):** Estilização responsiva com suporte nativo a **Modo Escuro (Dark Mode)** e **Modo Claro (Light Mode)**.
* **Fontes Tipográficas:** *Inter* (interface) e *JetBrains Mono* (código-fonte e variáveis de memória).
