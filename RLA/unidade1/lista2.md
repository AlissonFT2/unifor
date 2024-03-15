# UNIFOR
**Nome**: Nome do estudante <br>
**Disciplina**: Raciocínio lógico algorítm

## Exercício exemplo
Represente, em fluxograma e pseudocódigo, um algoritmo para calcular o adicional de salário de funcionário por cargo de uma empresa fictícia. Sabe-se que os funcionários de cargo técnico receberão reajuste de 50%, cargo de gerência, um reajuste de 30% e demais, um reajuste de 10%. 

#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite o salário e profissão}}
B --> C[\sal, prof\]
C --> D{prof == 'Tecnico'}
D --FALSE--> E{prof == 'Gerente'}
D --TRUE--> F[sal_reaj = 1.5 * sal]
E --FALSE--> H[sal_reaj = 1.1 * sal]
E --TRUE--> G[sal_reaj = 1.3 * sal]
G --> I([FIM])
F --> I
H --> J{{'Salário Reajustado = ', sal_reaj}}
J --> I
```

#### Pseudocódigo
```
1  ALGORITMO calReajuste
2  DECLARE  sal, sal_reaj: real, prof: caractere
3  INICIO
4  LEIA sal, prof
5  ESCOLHA
6   CASO prof == “Técnico”		// caso 1
7     sal_reaj ← 1.5 * sal
8   CASO prof = “Gerente”		// caso 2
9     sal_reaj ← 1.3 * sal
10  SENÃO
11    sal_reaj ← 1.1 * sal
12 FIM_ESCOLHA
13 ESCREVA “Salário Reajustado = “, sal_reaj
14 FIM
```

#### Teste
| sal | prof | prof == “Técnico” | prof = “Gerente” | sal_reaj | Saída |
| -- | -- | -- | -- | -- | -- |
| 1000 | Técnico | V | F | 1500 | “Salário Reajustado = 1500“ |
| 2000 | Gerente | F | V | 2600 | “Salário Reajustado = 2600“ |
| 9000 | Diretor | F | F | 9900 | “Salário Reajustado = 9900“ |

## Lista de exercícios 02

### Exercício 01 (2.5 pontos)
Calcule a média de quatro números inteiros dados.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite quatro números inteiros: }} 
B --> C[/n1, n2, n3, n4, media/]
C --> E["media = (n1 + n2 + n3 + n4) / 4"]
E --> F{{A media dos quatro números é: media,media}}
F --> G([FIM])
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo Media
DECLARE n1, n2, n3, n4: int, media: float
INICIO
ESCREVA "Digite quatro números inteiros: "
LEIA n1, n2, n3, n4
media <- (n1, n2, n3, n4) / 4
ESCREVA "A media dos quatro números é: media", media
FIM_ALGORITMO
```

#### Teste de mesa (0.5 ponto)

| n1 | n2 | n3 | n4 | media | saída |
| -- | -- | -- | -- | -- | -- |
| 5 | 7 | 1 | 9 | 5.5 | A media dos quatro números é: 5.5 | | 
| 18 | 25 | 69 | 48 | 40.0 | A media dos quatro números é: 40.0| |
| 1 | 1 | 1 | 1 | 1.0 | A media dos quatro números é: 1.0 ||

### Exercício 02 (2.5 pontos)
Leia uma temperatura dada em Celsius (C) e imprima o equivalente em Fahrenheit (F). (Fórmula de conversão: F = (9/5) * C + 32)

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite a temperatura em ºC: }}
B --> D[/c, f/]
D --> E["f = (9/5) * c + 32"]
E --> F{{A temperatura em fahrenheit é: f,f}}
F --> G([FIM])
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo ConverteCelsiusFarenheit
DECLARE c, f: float
INICIO
ESCREVA "Digite a temperatura em ºC: "
LEIA c
f <- (9/5) * c + 32
ESCREVA "A temperatura em fahrenheit é: f", f
FIM_ALGORITMO
```

#### Teste de mesa (0.5 ponto)

| c | f | saída |
| -- | -- | -- | 
| 10.0 | 50.0 | A temperatura em fahrenheit é: 50.0 |
| 0.0 | 32.0 | A temperatura em fahrenheit é: 32.0 |
| 25.5 | 77.9 | A temperatura em fahrenheit é: 77.9 |

### Exercício 03 (2.5 pontos)
Receba dois números reais e um operador e efetue a operação correspondente com os valores recebidos (operandos). 
O algoritmo deve retornar o resultado da operação selecionada simulando todas as operações de uma calculadora simples.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite a operação que deseja fazer [+][-][*][/]: <br> Digite os dois números que deseja operar: "}}
B --> C[/operacao, n1, n2, calc/]
C --> D{operacao == `+`}
D --NAO--> E{operacao == `-`}
E --NAO--> F{operacao == `*`}
F --NAO--> G{operacao == `/`}
G --NAO--> H{{Simbolo de operação invalido!}}
D --SIM--> L[calc = n1 + n2]
E --SIM--> M[calc = n1 - n2]
F --SIM--> N[calc = n1 * n2]
G --SIM--> O{n2 == 0}
O --NAO--> P[calc = n1 / n2]
O --SIM--> R{{Não se pode dividir por zero!}}
L & M & N & P --> S{{calc}}
S & R & H --> T([FIM])
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo Calculadora
DECLARE operacao: char, n1, n2, calc: float
INICIO
ESCREVA "Digite a operação que deseja fazer [+][-][*][/]: "
ESCREVA "Digite os dois números que deseja operar: "
LEIA operacao, n1, n2
ESCOLHA
  CASO operacao == "+"
    calc <- n1 + n2
    ESCREVA calc
  CASO operacao == "-"
    calc <- n1 - n2
    ESCREVA calc
  CASO operacao == "*"
    calc <- n1 * n2
    ESCREVA calc
  CASO operacao == "/"
    SE n2 == 0 ENTAO
      ESCREVA "Não se pode dividir por zero!"
    SENAO
      calc <- n1 / n2
      ESCREVA calc
    FIM_SE
  SENAO
    ESCREVA "Simbolo de operação invalido"
FIM_ESCOLHA
FIM_ALGORITMO
```

#### Teste de mesa (0.5 ponto)

| operacao | n1 | n2 | saída
| -- | -- | -- | -- |
| / |  10 | 0 | Não se pode dividir por zero!
| + | 5 | 3| 8
| = | 5 | 6 | Simbolo de operação invalido!
| * | 5 | 2 | 10 |
| - | 5 | 10 | -5 |
| - | 10 | 5 | 5 |

### Exercício 04 (2.5 pontos)
Elaborar um algoritmo que, dada a idade, classifique nas categorias: infantil A (5 - 7 anos), infantil B (8 -10 anos), juvenil A (11 - 13 anos), juvenil B (14 -17 anos) e adulto (maiores que 18 anos).

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B([FIM])
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo ClassificaCategoria
FIM_ALGORITMO
```

#### Teste de mesa (0.5 ponto)

| nome_coluna1 | nome_coluna2 | nome_coluna3 | nome_coluna4 | nome_coluna5 | 
|      --      |      --      |      --      |      --      |      --      | 
| Adicione     | espaço       | se quiser    |  alinhar     | as barras    |
| verticais,   | mas          | não é        | obrigatório. | Entendido ?  |
