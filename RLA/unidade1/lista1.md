# UNIFOR
**Nome**: Alisson Frota Teixeira <br>
**Disciplina**: Raciocínio lógico algorítmico

## Lista de exercícios 01

### Exercício 01 (1 ponto)
Represente, em fluxograma e pseudocódigo, um algoritmo para determinar se um número inteiro e positivo é par ou impar.

#### Fluxograma (0,25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número:}}
B --> C[\numero\]
C --> D{numero >= 0}
D --FALSE--> E[O número não é positivo!]
D --TRUE--> F[resto = numero % 2]
E --> Z([FIM])
F --> G{resto == 0}
G --FALSE--> H{{O número é impar!}}
G --TRUE--> I{{O número é par!}}
H --> Z
I --> Z
```

#### Pseudocódigo (0,5 ponto)
```
1  ALGORTIMO verifica_par_impar
2  DECLARE numero, resto: INTEIRO
3  ESCREVA "Digite um número: "
4  INICIO
4  LEIA numero
5  SE numero >= 0 ENTAO                  // verifica se o inteiro é positivo
6    resto = numero % 2                 // calcula o resto da divisão por 2
7    SE resto == 0 ENTAO                // verifica se o resto é igual a zero
8      ESCREVA "O número é par!"
9    SENAO
10     ESCREVA "O número é impar!"
11   FIM_SE
11  SENAO                                // caso inteiro for negativo (condição linha 5)
12    ESCREVA "O número deve ser postivo!"
13  FIM_SE
13 FIM
```

#### Teste de mesa (0,25 ponto)
| numero | numero >= 0 | resto | resto == 0 | Saída |
| -- | -- | -- | -- | -- | 
| -1 | F |   |   | "O número deve ser postivo!" |
| 0  | V | 0 | V | "O número é par!" |
| 13 | V | 1 | F | "O número é impar!" |
| 30 | V | 0 | V | "O número é par!" |

## Exercício 02 (3 pontos)
Represente, em fluxograma e pseudocódigo, um algoritmo para calcular o novo salário de um funcionário. 
Sabe-se que os funcionários que recebem atualmente salário de até R$ 500 terão aumento de 20%; os demais terão aumento de 10%.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite seu salario: }}
B --> C[/salario, novo_salario/]
C --> D{salario > 500}
D --NAO--> E[novo_salario = salario * 1.2]
D --SIM--> F[novo_salario = salario * 1.1]
E & F --> G{{novo_salario}}
G --> H([FIM])
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo ContaAprovacoes
DECLARE salario, novo_salario: float
ESCREVA "Digite seu salario: "
INICIO
LEIA salario
SE salario > 500 ENTAO
    novo_salario <- salario * 1.1
SENAO
    novo_salario <- salario * 1.2
FIM_SE
ESCREVA novo_salario
FIM_ALGORITMO
```

#### Teste de mesa (1.0 ponto)

| salario | salario > 500 | novo_salario |
| -- | -- | -- |
| 300 | False | 330 |
| 500 | False | 550 |
| 501 | True | 601.2 |

## Exercício 03 (3 pontos)
Represente, em fluxograma e pseudocódigo, um algoritmo para calcular a média aritmética entre duas notas de um aluno e mostrar sua situação, que pode ser aprovado ou reprovado.

#### Fluxograma (1 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite suas notas: }}
B --> C[/n1, n2, media/]
C --> D["media = (n1+n2) / 2"]
D --> E{media >= 7}
E --NAO--> F{{Reprovado}}
E --SIM--> G{{Aprovado}}
F & G --> H([FIM])
```

#### Pseudocódigo (1 ponto)

```
Algoritmo ContaAprovacoes
DECLARE n1, n2, media: float
ESCREVA "Digite suas notas: "
INICIO
LEIA n1, n2
media <- (n1 + n2) / 2
SE media >= 7 ENTAO
    ESCREVA "Aprovado"
SENAO
    ESCREVA "Reprovado"
FIM_SE
FIM_ALGORITMO
```

#### Teste de mesa (1 ponto)

| n1 | n2 | media | media>=7 | saída
| -- | -- | -- | -- | -- |
| 10 | 10 | 10 | True | Aprovado
| 7 | 7 | 7 | True | Aprovado
| 6.5 | 7.4 | 6.9 | False | Reprovado

## Exercício 04 (3 pontos)
Represente, em fluxograma e pseudocódigo, um algoritmo que, a partir da idade do candidato(a), determinar se pode ou não tirar a CNH. 
Caso não atender a restrição de idade, calcular quantos anos faltam para o candidato estar apto.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite sua idade: }} 
B --> C[/idade, falta/]
C --> D{idade >= 18}
D --NAO--> E[falta = 18 - idade]
D --SIM--> F{{Pode retirar CNH}}
E --> G{{`falta: falta`,falta}}
G & F --> H([FIM])
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo ContaAprovacoes
DECLARE idade, falta: int
INICIO
ESCREVA "Digite sua idade: "
LEIA idade
SE idade >= 18 ENTAO
    ESCREVA "Pode retirar CNH"
SENAO
    falta <- 18 - idade
    Escreva f"falta {falta} ano(s)"
FIM_SE
FIM_ALGORITMO
```

#### Teste de mesa (1.0 ponto)

| idade | idade >= 18 | falta | saída |
| -- | -- | -- | -- |
| 17 | False | 1 | falta 1 ano(s) | 
| 18 | True |  | Pode retirar CNH |
| 23 | True |  | Pode retirar CNH |
