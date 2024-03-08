# UNIFOR
**Nome**: Alisson Frota Teixeira <br>
**Disciplina**: Raciocínio lógico algorítmico

## Lista de exercícios 02

### Exercício 1
Calcule a média de quatro números inteiros dados.

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite quatro números inteiros: }} 
B --> C[/n1, n2, n3, n4, media/]
C --> E["media = (n1 + n2 + n3 + n4) / 4"]
E --> F{{`A media dos quatro números é: media`,media}}
F --> G([FIM])


```
#### Pseudocódigo
```
ALGORITMO media_entre_4
DECLARE n1, n2, n3, n4: int, media: float
INICIO
ESCREVA "Digite quatro números inteiros: "
LEIA n1, n2, n3, n4
media <- (n1, n2, n3, n4) / 4
ESCREVA "A media dos quatro números é: media", media
FIM
```

#### Teste
| n1 | n2 | n3 | n4 | media | saída |
| -- | -- | -- | -- | -- | -- |
| 5 | 7 | 1 | 9 | 5.5 | A media dos quatro números é: 5.5 | | 
| 18 | 25 | 69 | 48 | 40.0 | A media dos quatro números é: 40.0| |
| 1 | 1 | 1 | 1 | 1.0 | A media dos quatro números é: 1.0 || 

### Exercício 2
Leia uma temperatura dada na escala Celsius (C) e imprima o equivalente em Fahrenheit (F). (Fórmula de conversão: F = (9/5) * C + 32)

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite a temperatura em ºC: }}
B --> D[/c, f/]
D --> E["f = (9/5) * C + 32"]
E --> F{{`A temperatura em fahrenheit é: f`,f}}
F --> G([FIM]) 



```
#### Pseudocódigo
```
ALGORITMO celsius_para_fahrenheit
DECLARE c, f: float
INICIO
ESCREVA "Digite a temperatura em ºC: "
LEIA c
f <- (9/5) * C + 32
ESCREVA "A temperatura em fahrenheit é: f", f
FIM
```

#### Teste
| c | f | saída |
| -- | -- | -- | 
| 10.0 | 50.0 | A temperatura em fahrenheit é: 50.0 |
| 0.0 | 32.0 | A temperatura em fahrenheit é: 32.0 |
| 25.5 | 77.9 | A temperatura em fahrenheit é: 77.9 |

### Exercício 3
Leia uma quantidade de chuva dada em polegadas e imprima o equivalente em milímetros (25,4 mm = 1 polegada).

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite a quantidade de chuva em polegadas: }}
B --> D[/polegadas, mm/]
D --> E[mm = polegadas * 25.4]
E --> F{{`A quantidade de chuva em mm é: mm`,mm}}
F --> G([FIM]) 



```
#### Pseudocódigo
```
ALGORITMO polegadas_para_mm
DECLARE polegadas, mm: float
INICIO
ESCREVA "Digite a quantidade de chuva em polegadas: "
LEIA polegadas
mm <- polegadas * 25.4
ESCREVA "A quantidade de chuva em mm é: mm", mm
FIM
```

#### Teste
| polegadas | mm | saída |
| -- | -- | -- | 
| 10.0 | 254.0 | A quantidade de chuva em mm é: 254.0 |
| 0.2 | 5.08 | A quantidade de chuva em mm é: 5.08 |
| 25.5 | 647.7 | A quantidade de chuva em mm é: 647.7 |

### Exercício 4
O custo ao consumidor de um carro novo é a soma do custo de fábrica com a porcentagem do distribuidor e dos impostos, ambos aplicados ao custo de fábrica. Supondo que a porcentagem do distribuidor seja de 12% e a dos impostos de 45%, prepare um algoritmo para ler o custo de fábrica do carro e imprimir o custo ao consumidor.

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite o preço de fabrica do carro: }}
B --> D[/preco_fabrica, preco_consumidor/]
D --> E["preco_consumidor = (preco_fabrica * 1.12) + (preco_fabrica * 0.45)"]
E --> F{{`O preço do carro para o consumidor é: preco_consumidor`,preco_consumidor}}
F --> G([FIM]) 



```
#### Pseudocódigo
```
ALGORITMO preco_fabrica_para_preco_consumidor
DECLARE preco_fabrica, preco_consumidor: float
INICIO
ESCREVA "Digite o preço de fabrica do carro: "
LEIA preco_fabrica
preco_consumidor <- (preco_fabrica * 1.12) + (preco_fabrica * 0.45)
ESCREVA "O preço do carro para o consumidor é: preco_consumidor", preco_consumidor
FIM
```

#### Teste
| preco_fabrica | preco_consumidor | saída |
| -- | -- | -- | 
| 1500.0 | 2355.0 | O preço do carro para o consumidor é: 2355.0|
| 300.0 | 471.0 | O preço do carro para o consumidor é: 471.0|
| 353.32 | 554.746 | O preço do carro para o consumidor é: 554.746 |

### Exercício 5
Calcule o quadrado de um número.

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número: }}
B --> D[/n, n_pow/]
D --> E["n_pow = n**2"]
E --> F{{`O seu número ao quadrado é: n_pow`, n_pow}}
F --> G([FIM]) 



```
#### Pseudocódigo
```
ALGORITMO calc_quadrado_numero
DECLARE n, n_pow: float
INICIO
ESCREVA "Digite um número: "
LEIA n
n_pow <- n**2
ESCREVA "O seu número ao quadrado é: n_pow", n_pow
FIM
```

#### Teste
| n | n_pow | saída |
| -- | -- | -- | 
| 5.0 | 25.0 | O seu número ao quadrado é: 25.0|
| 1.0 | 1.0 | O seu número ao quadrado é: 1.0|
| 2.3 | 5.29 | O seu número ao quadrado é: 5.29 |

### Exercício 6
O cardápio de uma lanchonete é dado abaixo. Prepare um algoritmo que leia a quantidade de cada item que você consumiu e calcule a conta final. <br>
a) Hambúrguer................ R$ 3,00 <br>
b) Cheeseburger.............. R$ 2,50 <br>
c) Fritas.................... R$ 2,50 <br>
d) Refrigerante ............. R$ 1,00 <br>
e) Milkshake................. R$ 3,00

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Quantos Hambúrgueres, Cheeseburgers, Fritas, Refrigerantes e Milkshakes voçe pediu: }} 
B --> C[/qts_ham, qts_che, qts_fri, qts_ref, qts_mil, total/]
C --> D["total = (qts_ham * 3.0) + (qts_che * 2.5) + (qts_fri * 2.5) + (qts_ref * 1.0) + (qts_mil * 3.0)"]
D --> F{{`O total foi: total`, total}}
F --> G([FIM])

```
#### Pseudocódigo
```
ALGORITMO total_conta
DECLARE qts_ham, qts_che, qts_fri, qts_ref, qts_mil: int, total: float
INICIO
ESCREVA "Quantos Hambúrgueres, Cheeseburgers, Fritas, Refrigerantes e Milkshakes voçe pediu: "
LEIA qts_ham, qts_che, qts_fri, qts_ref, qts_mil
total <- (qts_ham * 3.0) + (qts_che * 2.5) + (qts_fri * 2.5) + (qts_ref * 1.0) + (qts_mil * 3.0)
ESCREVA "O total foi: total", total
FIM
```

#### Teste
| qts_ham | qts_che | qts_fri | qts_ref | qts_mil | total | saída |
| -- | -- | -- | -- | -- | -- | -- |
| 1 | 0 | 1 | 2 | 0 |7.5 | O total foi: 7.5
| 0 | 3 | 4 | 0 | 2 |23.5 | O total foi: 23.5 |
| 0 | 0 | 0 | 0 | 0 | 0 | O total foi: 0.0  

### Exercício 7
Uma companhia de carros paga a seus empregados um salário de R$ 500,00 por mês mais uma comissão de R$ 50,00 para cada carro vendido e mais 5% do valor da venda. Elabore um algoritmo para calcular e imprimir o salário do vendedor num dado mês recebendo como dados de entrada o nome do vendedor, o número de carros vendidos e o valor total das vendas.

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite seu nome o número de carros vendidos e o valor total das vendas: }} 
B --> C[/nome, qts_carr, vendas, salario/]
C --> D["salario = 500.00 + (qts_carr * 50.00) + (vendas * 0.05)"]
D --> F{{`O salario foi: salario`, salario}}
F --> G([FIM])

```
#### Pseudocódigo
```
ALGORITMO salario_funcionario
DECLARE nome: string, qts_carr: int, vendas, salario: float
INICIO
ESCREVA "Digite seu nome o número de carros vendidos e o valor total das vendas: "
LEIA nome, qts_carr, vendasa
salario <- 500.00 + (qts_carr * 50.00) + (vendas * 0.05)
ESCREVA "O salario foi: salario", salario
FIM
```

#### Teste
| nome | qts_carr | vendas | salario | saída |
| -- | -- | -- | -- | -- |
| Alisson | 3 | 60000.00 | 3650.00 | O salario foi: 3650.00 |
| Pedro | 0 | 0 | 500.00 |O salario foi: 500.00 |
| Enzo | 11 | 2000000.00 | 101050.00 | O salario foi: 101050.00|










