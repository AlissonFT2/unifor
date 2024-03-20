<img src="https://drive.google.com/uc?id=1SOzRTjUt7cuBJpSqoK90fcAiKBrnpUJo" width="400">

**Curso:** Eng. Computação <br>
**Disciplina:** Raciocínio lógico algorítmico <br>
**Código/Turma:** T998-08 <br>
**Professor:** Ricardo Carubbi <br>
**Data:** 21/03/2024 <br>
**Aluno(a):** Alisson Frota Teixeira <br>
**Matrícula:** 2410301 <br>

**1a chamada (Sim/Não):** Sim <br>
**2a chamada (Sim/Não):** Não

# Avaliação Diagnóstica 1

## Normas e exigências

Avaliação diagnóstica (**AD**) consiste em exercícios ou projetos desenvolvidos em grupo ao longo da disciplina. <br>
A primeira avaliação diagnóstica (**AD1**) será composta por exercícios e equivale a 30% da nota da primeira avaliação (**AV1**).

Segue abaixo a expressão para o cálculo da **AV1**, sendo sendo **AF1** equivale a primeira avaliação formativa e **AD1**, a primeira avaliação diagnóstica.

$$AV_1 = AF_1 \times 0,30 + AD_1 \times 0,70$$

A **AD1** é formada pela entrega dos exercícios (**EX1**) na data prevista e apresentação (**AP1**) de um dos exercícios escolhido pelo professor.
Segue abaixo a expressão para o cálculo da **AD1**.

$$AD_1 = (EX1_1 + AP_1)/2 $$

A **EX1** é avaliada mediante a **correção dos exercícios**, sendo a avaliação no intervalo de 0% (não atende a questão), 50% (atende parcialmente) e 100% (atende em sua totalidade).
Por exemplo, se o exercício equivale a 2 pontos e sua correção atente parcialmente a questão, então sua avaliação deste exercício será 1 ponto.

A **AP1** é avaliada mediante aos pré-requisitos de **clareza, organização e domínio do conteúdo**. Portanto, o aluno deve demonstrar um bom entendimento do algoritmo, explicando seus princípios fundamentais, seu propósito e como ele funciona passo a passo. <br>

A avaliação da **AP1** é apenas considerada no intervalo de 0% (não atende os pré-requisitos), 50% (atende parcialmente) e 100% (atende em sua totalidade).
Por exemplo, se na apresentação do exercício, o aluno atenter parcialmente os pré-requisitos, então sua avaliação da apresentação será 5,0.

## Datas
- Entrega da primeira avaliação formativa (**AF1**) composta pelas listas de exerciícios 1, 2 e 3: 21/03/24
- Entrega dos exercícios da primeira avaliação diagnóstica (**EX1**): 21/03/24
- Apresentação da primeira avaliação diagnóstica (**AP1**): 21/03/24

## Lista de questões

### Questão 1 - Troca dos valores de duas variáveis (1 ponto)

Dadas duas variáveis, $a$ e $b$, implemente e teste um algoritmo para trocar os valores atribuídos a elas.
#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite a: <br> Digite b: }}
B --> C[/a, b, temp/]
C --> J{{a, b}}
J --> D[temp = a]
D --> E[a = b]
E --> F[b = temp]
F --> G{{a, b}}
G --> K([FIM])
```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo TrocaValores
DECLARE a, b, aux: INT
INICIO
ESCREVA "Digite a: "
LEIA a
ESCREVA "Digite b: "
LEIA b
aux <- a
a <- b
b <- aux
ESCREVA "a= ", a
ESCREVA "b= ", b
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| a | b | saída1 | temp | saída2 | 
|      --      |      --      |      --      |      --      |      --      | 
| 3     | 4       | 3, 4    |  3     | 4, 3    |   
| -2     | 6       | -2, 6    |  -2     | 6, -2    | 

### Questão 2 - Contagem (1 ponto)

Dado um conjunto $n$ de notas de alunos em um exame, implemente e teste um algoritmo para fazer uma contagem $cont$ do número de alunos que foram aprovados no exame. 
Será considerado aprovado o aluno que tirar $nota$ 50 ou maior (no intervalo de 0 a 100).

#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B[/cont, i/]
B --> C{{Digite o número de notas e ser processado: }}
C --> D[/n/]
D --> E[[i=1 ATE n]]
E --> J{{`O número total de aprovações é: cont`, cont}}
J --> K([FIM])
E --> F{{Digite a nota: }}
F --> G[/nota/]
G --> H{nota >= 50 and nota <= 100}
H --TRUE--> I[cont =+ 1]
H --LOOP--> E
I --LOOP--> E
```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo ContaAprovacoes
DECLARE i, cont, n: INT, nota: FLOAT
INICIO
cont <- 0
ESCREVA "Digite o número de notas a ser processado: "
LEIA n
PARA i=1 ATE n FAÇA
	ESCREVA "Digite a nota ", i
	LEIA nota
	SE 50 <= nota <= 100
		cont <- cont + 1
	FIM_SE
FIM_PARA
ESCREVA "Número de alunos aprovados: ", cont
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| i    | cont | nota  | n |
|  --  |  --  |   --  | -- |
| 1    | 1    | 70    | 5 |
| 2    | 1    | 40    | 5 |
| 3    | 2    | 60    | 5 |
| 4    | 3    | 55    | 5 |
| 5    | 3    | 30    | 5 |

### Questão 3 - Soma de um conjunto de números (1 ponto)

Dado um conjunto de $n$ números, implemente e teste um algoritmo para calcular a soma desses números. <br>
Aceite apenas $n$ maior ou igual a zero.

#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite a quantidade de números que serão somados: "}}
B --> C[\n\]
C --> D{n >= 0}
D --FALSE-->N{{"O número deve ser >=0"}}
N --> M([FIM])
D --TRUE--> E[/soma = 0/]
E --> F[/i = 1/]
F --> G{i <= n}
G --FALSE--> L{{soma}}
L --> M
G --TRUE--> H{{Digite um número: }}
H --> I[\num\]
I --> J[soma =+ num]
J --> K[i =+ 1]
K --LOOP--> G
```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo SomaNumeros
DECLARE soma, i, num, n: INT
INICIO
ESCREVA "Digite a quantidade de números (n >= 0): "
LEIA n
SE n >= 0 ENTAO
	soma <- 0
	i <- 1
	ENQUANTO i <= n FAÇA
		ESCREVA "Digite um número: "
		LEIA num
		soma <- soma + num
	FIM_ENQUANTO
	ESCREVA "A soma dos números é: ", soma
SENAO
	ESCREVA "O valor deve ser maior ou iqual a zero!"
FIM_SE
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| n | i | num | soma |
|      --      |      --      |      --      |      --      |  
| 3     | 1       | -3    |  -3     | 
| 3   | 1          | 3        | 0 |
| 3 | 2 | 5 | 5 |
| 3 | 3 | 2 | 7|

### Questão 4 - Cálculo de uma série (1 ponto)

Dado um conjunto de $n$ termos da série, implemente e teste um algoritmo para calcular o valor de S, conforme definido abaixo:

$$ S = \frac{1}{2} + \frac{3}{4} + \frac{5}{6} + \frac{7}{8} + \dots $$

#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> Z[/numerador = 1, denominador = 2, s/]
Z --> B{{Digite quantos termos somar: }}
B --> C[/n/]
C --> D[[i=0 ATE n]]
D --> H{{s}}
H --> J([FIM])
D --> E["s =+ (numerador/denominador)"]
E --> F[numerador =+ 2]
F --> G[denominador =+ 2]

G --LOOP--> D
```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo SomaSerie
DECLARE numerador, denominador, n, i: INT, s: FLOAT
INICIO
numerador <- 1
denominador <- 2
s <- 0
ESCREVA "Digite quantos termos somar: "
LEIA n
PARA i=0 ATE n FAÇA
	s <- s + (numerador/denominador)
	numerador <- numerador + 2
	denominador <- denominador + 2
FIM_PARA
ESCREVA s
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| n | i | numerador | denominador | s | 
|      --      |      --      |      --      |      --      |      --      | 
| 3     | 0       | 1    |  2     | 0.5    |
| 3   | 1          | 3        | 4 | 1.25  |
| 3   | 2          | 5       | 6 | 2.08  |

### Questão 5 - Cálculo fatorial (2 pontos)

Dado um número $n$, implemente e teste um algoritmo para calcular o fatorial de $n$ (escrito como $n!$), onde $n ≥ 0$.

#### Fluxograma (0.5 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um numero: }}
B --> C[/num/]
C --> D{num >= 0}
D --TRUE--> E[fatorial = 1]
D --FALSE--> J{{O valor deve ser positivo}}
J --> I([FIM])
E --> F[[i=1 ATE num PASSO 1]]
F --> H{{fatorial}}
F --> G[fatorial =* i]
G --LOOP--> F
H --> I
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo CalcFatorial
DECLARE i, fator, n: INT
INICIO
ESCREVA "Digite um número"
LEIA n
SE n >= 0
	fator <- 1
	PARA i=1 ATE n FAÇA
		fator <- fator * i
	FIM_PARA
	ESCREVA "O fatorial de {n} é: {fator}"
SENAO
	ESCREVA "O valor deve ser maior ou igual a zero!"
FIM_SE
FIM_ALGORITMO
```

#### Teste de mesa (0.5 ponto)

|  numero  |  fatorial  |  i  |
| -- | -- | -- |
| 6 | 1 | |
|    6     |     2      |  2  |
|    6     |     6      |  3  |
|    6     |    24      |  4  |
|    6     |   120      |  5  |
|    6     |   720      |  6  |


### Questão 6 - Geração da sequência de Fibonacci (2 pontos)

Gerar e imprimir os $n$ primeiros termos da sequência de Fibonacci, onde $n ≥ 1$. <br>
Os primeiros termos são: $0, 1, 1, 2, 3, 5, 8, 13, \dots$ <br>
Cada termo, além dos dois primeiros, é derivado da soma dos seus dois antecessores mais próximos.

#### Fluxograma (0.5 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Quantos termos: }}
B --> K[/n/]
K --> C[/fib0 = 0/]
C --> D[/fib1 = 1/]
D --> Z[/fibnext/]
Z --> E[[i=1 ATÉ n PASSO 1]]
E --> J([FIM])
E --> F{{fib0}}
F --> G[fibnext = fib0 + fib1]
G --> H[fib0 = fib1]
H --> I[fib1 = fibnext]
I --LOOP--> E 
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo GeraFibonacci
DECLARE a, b, termo_atual, i, n: INT
INICIO
a <- 0
b <- 1
ESCREVA "Número de termos da série Fibonacci: "
LEIA n
PARA i=1 ATE n FAÇA
	ESCREVA a
	termo_atual <- a + b
	a <- b
	b <- termo_atual
FIM_PARA
FIM_ALGORITMO
```
#### Teste de mesa (0.5 ponto)

| n	| i | fibnext | fib0 | fib1 | 
|      --      |      --      |      --      |      --      |      --      | 
| 3     |  1      |     |  0     | 1    |
| 3   | 2          | 1        | 1 | 1  |
| 3   | 3          | 2        | 1 | 2  |

### Questão 7 - Inversão dos dígitos de um número inteiro (2 pontos)

Implemente e teste um algoritmo para inverter a ordem dos dígitos de um número inteiro positivo de dois dígitos.

#### Fluxograma (0.5 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B[/invertido = 0, resto = 0/]
B --> C{{Digite o número a ser invertido: }}
C --> D[/num/]
D --> E{num != 0}
E --FALSE--> I{{invertido}}
I --> Z([FIM])
E --TRUE--> F[resto = num % 10]
F --> G["invertido = (invertido * 10) + resto"]
G --> H[num = num // 10]
H --LOOP--> E
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo InverteInteiro
DECLARE num_inv, resto, num: INT
INICIO
num_inv <- 0
resto <- 0
ESCREVA "Digite um número inteiro: "
LEIA num
SE num >= 0 ENTAO
	ENQUANTO num != 0 FAÇA
		resto <- num % 10
		num_inv <- (num_inv * 10) + resto
		num <- num // 10
	FIM_ENQUANTO
	ESCREVA "Número invertido: ", num_inv
SENAO
	ESCREVA "O número deve ser positivo!"
FIM_ALGORITMO
```

#### Teste de mesa (0.5 ponto)

| num    | resto | invertido | 
|      --      |      --      |      --      |  
| 354     | 4         | 4     | 
| 35    | 5          | 45        |
| 3     | 3          | 453        |

