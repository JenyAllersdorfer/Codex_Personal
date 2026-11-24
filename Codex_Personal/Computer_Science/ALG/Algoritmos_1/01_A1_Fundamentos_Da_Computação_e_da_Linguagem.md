
## Conceito Principal

A computação envolve representar informações, processá-las por meio de instruções e produzir resultados. Um algoritmo é uma sequência organizada de instruções para resolver um problema.

Para construir algoritmos, é importante compreender como o computador representa e processa informações e como expressar instruções em uma linguagem algorítmica.

---

## Resumo da Aula & Slides

### 1. Modelo simplificado do computador

O modelo estudado utiliza a arquitetura de Von Neumann como referência para compreender o funcionamento básico de um computador.

Seus principais componentes são:

- **Entrada:** recebe informações do ambiente, como os dados digitados pelo usuário.
    
- **Memória:** armazena dados e instruções.
    
- **CPU (Unidade Central de Processamento):** executa as instruções.
    
- **ULA (Unidade Lógica e Aritmética):** realiza operações aritméticas e lógicas.
    
- **UC (Unidade de Controle):** coordena a execução das instruções.
    
- **Saída:** apresenta os resultados do processamento.
    

### 2. Níveis de representação e linguagens

Os computadores trabalham internamente com representações numéricas, enquanto os programadores podem utilizar linguagens mais próximas da linguagem humana.

- **Linguagem de máquina:** representada por códigos numéricos/binários compreendidos diretamente pelo processador.
    
- **Linguagem de montagem (Assembly):** utiliza instruções simbólicas e mnemônicos para representar operações.
    
- **Linguagem algorítmica estruturada:** permite descrever soluções por meio de instruções organizadas e estruturas de controle.
    

**Mnemônicos:** abreviações utilizadas para representar instruções. Exemplos:

- `ADD` — adição.
    
- `SUB` — subtração.
    
- `MUL` — multiplicação.
    
- `DIV` — divisão.
    

**Montador (Assembler):** programa que traduz instruções de Assembly para códigos de máquina.

### 3. Conjunto de instruções

As instruções podem ser organizadas por finalidade:

- Aritméticas: soma, subtração, multiplicação e divisão.
    
- Lógicas: conjunção, disjunção, disjunção exclusiva e negação.
    
- Movimentação: transferência de dados entre endereços.
    
- Entrada e saída: leitura e apresentação de informações.
    
- Comparação: testes entre valores.
    
- Controle de fluxo: alteração da sequência de execução.
    

### 4. Registradores, IP e flags

**IP (Instruction Pointer):** registrador que indica o endereço da próxima instrução a ser buscada.

**Flag:** indicador de estado armazenado em um bit. Pode registrar informações sobre o resultado de uma operação ou uma condição excepcional.

Exemplos:

- Zero: indica resultado igual a zero.
    
- Overflow: indica estouro na representação numérica.
    
- Carry: indica ocorrência de transporte em uma operação.
    

As instruções de salto podem consultar determinadas flags para decidir se o fluxo de execução deve ser alterado.

### 5. Linguagem algorítmica do professor

A linguagem utilizada na disciplina possui regras específicas de escrita e organização.

**Identificadores:**

- Começam com uma letra ou sublinhado.
    
- Podem conter letras e números.
    
- Não podem conter espaços ou pontuação.
    
- Devem respeitar as regras de palavras reservadas.
    

**Declaração de variáveis:**

As variáveis precisam ser declaradas antes de serem utilizadas.

Tipos mencionados nas aulas:

- Inteiro.
    
- Real.
    
- Lógico.
    
- Caractere.
    

**Atribuição:**

É representada por uma seta apontando para a esquerda e significa que uma variável recebe determinado valor ou resultado.

**Entrada:**

`leia(variavel)`

Recebe um valor fornecido pelo usuário e o armazena na variável.

**Saída:**

`escreva("Mensagem")`

Apresenta uma mensagem ou resultado.

### 6. Estrutura básica de um algoritmo

A estrutura apresentada no caderno segue esta organização:

```
Algoritmo "NomeDoAlgoritmo"

Var
    variavel: inteiro

Início
    escreva("Digite um número")
    leia(variavel)

Fim algoritmo
```

A escrita definitiva deve respeitar a formatação, os sublinhados, a indentação e as demais regras estabelecidas pelo professor.

### 7. Precedência, associatividade e aridade

**Precedência:** determina a prioridade de execução das operações em uma expressão.

**Associatividade:** determina como operações de mesma precedência são agrupadas quando não há parênteses.

**Aridade:** indica a quantidade de operandos de uma operação.

- Unária: utiliza um operando, como a negação.
    
- Binária: utiliza dois operandos, como soma e multiplicação.
    

### 8. Controle de fluxo

O fluxo de execução pode ser:

- **Sequencial:** as instruções são executadas na ordem em que aparecem.
    
- **Condicional:** a execução depende de uma condição.
    
- **Iterativo:** um conjunto de instruções pode ser repetido.
    

Estruturas já mencionadas na linguagem:

```
Se condição então
    instruções
Fim se
```

```
Enquanto condição faça
    instruções
Fim enquanto
```

As regras completas de escrita e as estruturas permitidas serão documentadas conforme os exemplos originais do professor.

---

## Exercícios de Fixação

_Exercícios de compreensão e aplicação serão adicionados conforme o material da disciplina._

1. Identificar os componentes do modelo simplificado de computador.
    
2. Diferenciar linguagem de máquina, Assembly e linguagem algorítmica.
    
3. Identificar a finalidade das principais categorias de instruções.
    
4. Explicar a função do IP e das flags.
    
5. Identificar erros na estrutura de um algoritmo.
    

---

## Flashcards (Anki / Spaced Repetition)

O que é um mnemônico? #card

É uma representação simbólica e abreviada utilizada para identificar uma instrução.

O que é o IP (Instruction Pointer)? #card

É o registrador que indica o endereço da próxima instrução a ser buscada.

O que é uma flag? #card

É um indicador de estado armazenado em um bit, utilizado para registrar uma condição ou situação resultante de uma operação.

Qual é a função da ULA? #card

Executar operações aritméticas e lógicas.

Qual é a função da UC? #card

Controlar e coordenar a execução das instruções.

O que é a aridade de uma operação? #card

É a quantidade de operandos utilizados pela operação.

Qual é a diferença entre precedência e associatividade? #card

Precedência determina a prioridade das operações; associatividade determina como operações de mesma prioridade são agrupadas.