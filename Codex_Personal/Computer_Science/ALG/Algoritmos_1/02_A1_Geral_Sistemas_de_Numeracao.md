
## Conceito Principal

Um sistema de numeração é uma forma de representar quantidades utilizando símbolos e regras específicas.

Um mesmo número pode ser representado por diferentes numerais, dependendo da base utilizada.

**Número:** representa uma quantidade ou valor.

**Numeral:** é a representação simbólica utilizada para expressar esse número.

---

## Resumo da Aula & Slides

### 1. Sistema decimal

É o sistema de numeração utilizado normalmente no cotidiano.

- Base: 10.
    
- Algarismos: 0, 1, 2, 3, 4, 5, 6, 7, 8 e 9.
    
- É um sistema posicional: o valor de cada algarismo depende de sua posição.
    

Exemplo:

[  
572 = 5 \cdot 100 + 7 \cdot 10 + 2 \cdot 1  
]

### 2. Sistemas de outras bases

|Sistema|Base|Algarismos|
|---|---|---|
|Binário|2|0 e 1|
|Ternário|3|0, 1 e 2|
|Octal|8|0 a 7|
|Decimal|10|0 a 9|
|Duodecimal|12|0 a 9 e dois símbolos adicionais|
|Hexadecimal|16|0 a 9 e A a F|
|Vigesimal|20|20 símbolos distintos|

No sistema hexadecimal, as letras representam os valores:

- A = 10
    
- B = 11
    
- C = 12
    
- D = 13
    
- E = 14
    
- F = 15
    

### 3. Representação posicional

Em um sistema de base (b), cada posição representa uma potência dessa base.

Exemplo em binário:

[  
1011_2  
]

[  
1\cdot 2^3 + 0\cdot 2^2 + 1\cdot 2^1 + 1\cdot 2^0  
]

[  
8+0+2+1=11_{10}  
]

Portanto:

[  
1011_2=11_{10}  
]

### 4. Conversões entre bases

As conversões estudadas incluem:

- Decimal para binário.
    
- Binário para decimal.
    
- Decimal para octal.
    
- Octal para decimal.
    
- Decimal para hexadecimal.
    
- Hexadecimal para decimal.
    
- Binário para octal e hexadecimal.
    
- Octal e hexadecimal para binário.
    

**Decimal para outra base:**

O procedimento usual é realizar divisões sucessivas pela base de destino, guardar os restos e lê-los na ordem inversa.

Exemplo:

[  
13_{10}  
]

Divisões por 2:

|Divisão|Quociente|Resto|
|---|---|---|
|13 / 2|6|1|
|6 / 2|3|0|
|3 / 2|1|1|
|1 / 2|0|1|

Lendo os restos de baixo para cima:

[  
13_{10}=1101_2  
]

**Outra base para decimal:**

Multiplicamos cada algarismo pelo peso de sua posição, isto é, pela potência da base correspondente, e somamos os resultados.

Exemplo:

[  
1101_2=1\cdot8+1\cdot4+0\cdot2+1\cdot1=13  
]

**Binário para hexadecimal:**

Agrupamos os bits de quatro em quatro, da direita para a esquerda. Cada grupo representa um algarismo hexadecimal.

Exemplo:

[  
11010110_2 = 1101\ 0110_2 = D6_{16}  
]

_As demais conversões serão desenvolvidas com exemplos e exercícios próprios._

---

## Exercícios de Fixação

1. Converter números decimais para binário.
    
2. Converter números binários para decimal.
    
3. Converter números decimais para octal.
    
4. Converter números decimais para hexadecimal.
    
5. Converter números binários para hexadecimal.
    
6. Converter números octais para binário.
    
7. Converter números hexadecimais para decimal.
    

---

## Flashcards (Anki / Spaced Repetition)

O que caracteriza um sistema de numeração posicional? #card

O valor de cada algarismo depende da posição que ocupa no numeral.

Qual é o valor decimal do algarismo hexadecimal A? #card

Como converter um número decimal para binário pelo método das divisões sucessivas? #card

Dividir sucessivamente por 2, guardar os restos e lê-los de baixo para cima.

Como converter um número binário para decimal? #card

Multiplicar cada bit pela potência de 2 correspondente à sua posição e somar os resultados.