# UNIFOR
**Nome**: Alisson Frota Teixeira <br>
**Disciplina**: Raciocínio Lógico Algorítmico

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

### Exercício 8
Calcule a média de um aluno na disciplina de RLA. Para isso solicite o nome do aluno, a nota da prova e a nota qualitativa. Sabe-se que a nota da prova tem peso 2 e a nota qualitativa peso 1. Mostre a média como resultado.

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite seu nome a nota da prova e a nota qualitativa: }} 
B --> C[/nome, nota1, qualitativa, media/]
C --> D["media = ((nota1*2)+(qualitativa*1)) / 3"]
D --> F{{`A sua media foi: media`, media}}
F --> G([FIM])

```
#### Pseudocódigo
```
ALGORITMO media_rla
DECLARE nome: string, nota1, qualitativa, media: float
INICIO
ESCREVA "Digite seu nome a nota da prova e a nota qualitativa: "
LEIA nome, nota1, qualitativa
media <- ((nota1*2) + (qualitativa*1)) /3
ESCREVA "A sua media foi: media", media
FIM
```

#### Teste
| nome | nota1 | qualitativa | media | saída |
| -- | -- | -- | -- | -- |
| Alisson | 9.0 | 5.0 | 7.6 | A sua media foi: 7.6 |
| Pedro | 10.0 | 10.0 | 10.0 |A sua media foi: 10.0 |
| Enzo | 3.5 | 7.8 | 4.9 | A sua media foi: 4.9|

### Exercício 9
Suponha que você deseja preencher a seguinte ficha de inscrição de um estudante: nome, matrícula, curso, idade, e-mail. Imprima os dados do usuário como uma ficha preenchida.

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite seu nome, matrícula, curso, idade e e-mail: }} 
B --> C[/nome, matricula, curso, idade, mail/]
C --> F{{`FICHA DE INSCRIÇÃO <br> Nome: nome <br> Matrícula: matricula <br> Curso: curso <br> idade: idade <br> e-mail: mail` <br>,nome, matricula, curso, idade}}
F --> G([FIM])

```
#### Pseudocódigo
```
ALGORITMO ficha_de_inscricao
DECLARE nome, matricula, curso, mail: string, idade: int
INICIO
ESCREVA "Digite seu nome, matrícula, curso, idade e e-mail: "
LEIA nome, matricula, curso, mail, idade
ESCREVA "FICHA DE INSCRIÇÃO"
ESCREVA "Nome: nome", nome
ESCREVA "Matrícula: matricula", matricula
ESCREVA "Curso: curso", curso
ESCREVA "idade: idade", idade
ESCREVA "e-mail: mail", mail
FIM
```

#### Teste
| nome | matricula | curso | mail | idade | saída |
| -- | -- | -- | -- | -- | -- |
| Pedro | 2418631 | Eng. Computação | pedro@edu.unifor.br | 18 | FICHA DE INSCRIÇÃO <br> Nome: Pedro <br> Matrícula: 2418631 <br> Curso: Eng. Computação <br> Idade: 18 <br> e-mail: pedro@edu.unifor.br  |

### Exercício 10
Calcule e mostre a área e o perímetro de um círculo. Sabe-se que a área = Ⲡ * raio2 e o perímetro = 2 * Ⲡ * raio.

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite o raio do círculo: }}
B --> C[/raio, area, perimetro/]
C --> D[perimetro = 2*3.14*raio]
D --> E["area = 3.14*(raio**2)"]
E --> F{{`Área = area`, area <br> `Perimetro = perimetro`, perimetro}}
F --> G([FIM]) 

```
#### Pseudocódigo
```
ALGORITMO area_e_perimetro
DECLARE raio, area, perimetro: float
INICIO
ESCREVA "Digite o raio do círculo: "
LEIA raio
perimetro <- 2*3.14*raio
area = 3.14*(raio**2)
ESCREVA "Área = area", area
ESCREVA "Perimetro = perimetro", perimetro
FIM
```

#### Teste
| raio | area | perimetro | saída | 
| -- | -- | -- | -- | 
| 5.0 | 78.5 |31.4 | Área = 78.5 <br> Perimetro = 31.4   | 
| 0.0 | 0.0 | 0.0 | Área = 0.0 <br> Perimetro = 0.0
| 1.0 | 3.14 | 6.28 | Área = 3.14 <br> Perimetro = 6.28

### Exercício 11
Faça um programa que receba um número positivo e maior que zero, calcule e mostre: a) o número digitado ao quadrado; <br>b) o número digitado ao cubo;<br> c) a raiz quadrada do número digitado;<br> d) a raiz cúbica do número digitado.
#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número: }}
B --> C[/num, num_pow2, num_pow3, num_sqrt, num_s3/]
C --> D{num > 0}
D --NAO--> E{{O número digitado não e maior que zero}}
D --SIM--> F[num_pow3 = num**3]
F --> G["num_sqrt = num**(1/2)"]
G --> H["num_s3 = num**(1/3)"]
H --> I[num_pow2 = num**2]
I --> L{{`O número elevado ao cubo é: num_pow3`, num_pow3 <br> `A raiz quadrada do número é: num_sqrt`, num_sqrt <br> `A raiz cubica do número é: num_s3`, num_s3 <br> `O número elevado ao quadrado é: num_pow2`, num_pow2}}
L & E --> M([FIM])
```
#### Pseudocódigo
```
ALGORITMO operacao_num
DECLARE num, num_pow2, num_pow3, num_sqrt, num_s3: float
INICIO
ESCREVA "Digite um número: "
LEIA num
SE num > 0 ENTAO
	num_pow2 <- num**2
	num_pow3 <- num**3
	num_sqrt <- num**(1/2)
	num_s3 <- num**(1/3)
	ESCREVA "O número elevado ao quadrado é: num_pow2", num_pow2
	ESCREVA "O número elevado ao cubo é: num_pow3", num_pow3
	ESCREVA "A raiz quadrada do número é: num_sqrt", num_sqrt
	ESCREVA "A raiz cubica do número é: num_s3", num_s3
SENAO
	ESCREVA "O número digitado não e maior que zero"
FIM_SE
FIM
```

#### Teste
| num | num > 0 | num_pow2 |num_pow3 | num_sqrt | num_s3 | saída |
| -- | -- | -- | -- | -- | -- | -- |
| 5.0 | True | 25.0 |125.0 | 2.2   | 1.7 | O número elevado ao quadrado é: 25.0 <br> O número elevado ao cubo é: 125.0 <br> A raiz quadrada do número é: 2.2 <br> A raiz cubica do número é: 1.7
| -3.0 | False | | |  | | O número digitado não e maior que zero

### Exercício 12
Faça um algoritmo que lê três números inteiros e mostra-os em ordem crescente.
#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite tres números: }}
B --> C[/n1, n2, n3/]
C --> D{n1 <= n2 and n1 <= n3}
D --NAO--> E{n2 <= n1 and n2 <= n3}
E --NAO--> F{n1 <= n2}
F --NAO--> G{{n3, n2, n1}}
D --SIM--> H{n2 <= n3}
H --NAO--> L{{n1, n3, n2}}
E --SIM--> M{n1 <= n3}
M --NAO--> O{{n1, n3, n1}}
F --SIM--> P{{n3, n1, n2}}
M --SIM--> Q{{n2, n1, n3}}
H --SIM--> R{{n1, n2, n3}}
R & Q & P & O & L & G --> T([FIM])

```
#### Pseudocódigo
```
ALGORITMO ordem_crescente
DECLARE n1, n2, n3: int
INICIO
ESCREVA "Digite tres números: "
LEIA n1, n2, n3
SE n1 <= n2 and n1 <= n3 ENTAO
	SE n2 <= n3 ENTAO
		ESCREVA n1, n2, n3
	SENAO
		ESCREVA n1, n3, n2
	FIM_SE
SENAO
	SE n2 <= n1 and n2 <= n3 ENTAO
		SE n1 <= n3 ENTAO
			ESCREVA n2, n1, n3
		SENAO
			ESCREVA n1, n3, n1
		FIM_SE
FIM_SE
	SENAO
		SE n1 <= n2 ENTAO
			ESCREVA n3, n1, n2
		SENAO
			ESCREVA n3, n2, n1
		FIM_SE
FIM_SE
FIM
```

#### Teste
| n1 | n2 | n3 | saída | 
| -- | -- | -- | -- |
| 3 | 10 |5 | 3 / 5 / 10   |
| 9 | 5 | 9 | 5 / 9 / 9 | 
| 15 | 11 | 10 | 10 / 11 / 15 | 

### Exercício 13
Elaborar um algoritmo que, dada a idade de um nadador, classificá-lo nas categorias: <br>a) infantil A (5 - 7 anos), <br>b) infantil, B (8 -10 anos), <br>c) juvenil A (11 - 13 anos), <br>d) juvenil B (14 -17 anos) e <br>e) adulto (maiores que 18 anos).
#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite sua idade: }}
B --> C[/idade, categoria/]
C --> D{idade >= 5 and idade <= 7}
D --NAO--> E{idade >= 8 and idade <= 10}
E --NAO--> F{idade >= 11 and idade <= 13}
F --NAO--> G{idade >= 14 and idade <= 17}
G --NAO--> H{idade >= 18}
H --NAO--> L[categoria = `nao_existe`]
D --SIM--> M[categoria = `infantil A`]
E --SIM--> N[categoria = `infantil B`]
F --SIM--> O[categoria = `juvenil A`]
G --SIM--> P[categoria = `juvenil B`]
H --SIM--> R[categoria = `adulto`]
L & M & N & O & P & R --> S{{categoria}}
S --> T([FIM])
```
#### Pseudocódigo
```
ALGORITMO categorias
DECLARE idade: int, categoria: string
INICIO
ESCREVA "Digite sua idade: "
LEIA idade
SE idade >= 5 and idade <= 7 ENTAO
	categoria <- `infantil A`
SENAO SE idade >= 8 and idade <= 10 ENTAO
	categoria <- `infantil B`
SENAO SE idade >= 11 and idade <= 13 ENTAO
	categoria <- `juvenil A` 
SENAO SE idade >= 14 and idade <= 17 ENTAO
	categoria <- `juvenil B`
SENAO SE idade >= 18 ENTAO
	categoria <- `adulto`
SENAO
	categoria <- `nao_existe`
FIM_SE
ESCREVA categoria
FIM
```

#### Teste
| idade | categoria | saída | 
| -- | -- | -- |
| 3 | nao_existe |nao_existe |
| 9 | infantil B | infantil B |
| 23 | adulto | adulto | 

### Exercício 14
Dado três inteiros crie um algoritmo para retornar o menor deles.
#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite tres números: }}
B --> C[/n1, n2, n3/]
C --> D{n1 <= n2 and n1 <= n3}
D --NAO--> E{n2 <= n1 and n2 <= n3}
E --NAO--> F{{n3}}
D --SIM--> G{{n1}}
E --SIM--> H{{n2}}
F & G & H --> L([FIM])

```
#### Pseudocódigo
```
ALGORITMO menor_num
DECLARE n1, n2, n3: int
INICIO
ESCREVA "Digite tres números: "
LEIA n1, n2, n3
SE n1 <= n2 and n1 <= n3 ENTAO
	ESCREVA n1
SENAO SE n2 <= n1 and n2 <= n3 ENTAO
	ESCREVA n2
SENAO
	ESCREVA n3
FIM_SE
FIM
```

#### Teste
| n1 | n2 | n3 | n1 <= n2 <br>and <br>n1 <= n3 | n2 <= n1 <br>and<br> n2 <= n3 | saída |
| -- | -- | -- | -- | -- | -- |
| 1 |  2 | 3 | True |  | 1
| 3 | 2 | 1 | False | False | 1
| 2 | 1 | 3 | False | True | 1  

### Exercício 15
Faça um algoritmo para converter um peso expresso em libras para quilogramas (1Kg = 1Lb * 2.2). Uma vez que o peso não pode ser um número negativo, o nosso programa não deve aceitar um número negativo como um peso válido.
#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite o peso em libras: }}
B --> C[/p_lb, p_kg/]
C --> D{p_lb >= 0}
D --NAO--> E{{O peso digitado não é positivo!}}
D --SIM--> F[p_kg = p_lb / 2.2]
F --> G{{`O peso em kg é: p_kg`, p_kg}}
E & G --> H([FIM])


```
#### Pseudocódigo
```
ALGORITMO lb_para_kg
DECLARE p_lb, p_kg: float
INICIO
ESCREVA "Digite o peso em libras: "
LEIA p_lb
SE p_lb >= 0 ENTAO
	p_kg <- p_lb / 2.2
	ESCREVA "O peso em kg é: p_kg", p_kg
SENAO
	ESCREVA "O peso digitado não é positivo"
FIM_SE
FIM
```

#### Teste
| p_lb | p_lb >= 0 | p_kg | saída | 
| -- | -- | -- | -- | 
| 10 |  True | 4.5 | O peso em kg é: 4.5 | 
| 0 | True | 0.0 | O peso em kg é: 0.0 | 
| -1 | False |  | O peso digitado não é positivo |

### Exercício 16
Leia uma média e exiba o status de um aluno:<br> a) AP se o aluno está aprovado (média final >= 6);<br> b) RM se o aluno está reprovado (média final < 3);<br> c) PF se o aluno está em prova fina (caso contrário).
#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite sua media: }}
B --> C[/media/]
C --> D{media >= 6}
D --NAO--> E{media < 3}
E --NAO--> F{{PF}}
D --SIM--> G{{AP}}
E --SIM--> H{{RM}}
F & G & H --> L([FIM])



```
#### Pseudocódigo
```
ALGORITMO status_aluno
DECLARE media: float
INICIO
ESCREVA "Digite sua media: "
SE media >= 6 ENTAO
	ESCREVA "AP"
SENAO SE media < 3 ENTAO
	ESCREVA "RM"
SENAO
	ESCREVA "PF"
FIM_SE
FIM
```

#### Teste
| media | media >= 6 | media < 3 | saída | 
| -- | -- | -- | -- | 
| 10.0 |  True |  | AP | 
| 0.0 | False | True | RM | 
| 5 | False | False | PF |

### Exercício 17
Suponha que saindo da UNIFOR seu primeiro salário será de R$ 5.000,00. O do seu colega que não fez UNIFOR é de R$ 2.500,00. Infelizmente, ambos precisam pagar impostos. Crie um algoritmo para calcular o salário líquido de vocês e de outras pessoas. <br> algoritmo para calcular o salário líquido de vocês e de outras pessoas.<br> Faixa Salarial Imposto Até 1.499,15 isento (não paga imposto) <br>1.499,16 ~ 2.246,75 7.5% <br>2.246,76 ~ 2.995, 70 15% <br>2.995,71 ~ 3.743,19 22,5% <br>A partir de 3.743,20 27,5%
#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite seu salário: }}
B --> C[/salario, sal_liq/]
C --> D{salario <= 1499.14}
D --NAO--> E{salario >= 1499.16 and salario <= 2246.75}
E --NAO--> F{salario >= 2246.76 and salario <= 2995.70}
F --NAO--> G{salario >= 2995.71 and salario <= 3743.19}
G --NAO--> H["sal_liq = salario - (56.06 + 112.34 + 168.18) - (salario - 3743.19) * 0.275"]
D --SIM--> L["sal_liq = salario"]
E --SIM--> M["sal_liq = salario - (salario - 1499.14) * 0.075"]
F --SIM--> N["sal_liq = salario - (56.06 + (salario - 2246.75) * 0.15)"]
G --SIM--> O["sal_liq = salario - (56.06 + 112.34 + (salario - 2995.70) * 0.225)"]
L & M & N & O & H --> P{{`O seu salário liquido é: sal_liq`, sal_liq}}
P --> Q([FIM])




```
#### Pseudocódigo
```
ALGORITMO salario_liquido
DECLARE sal_liq, salario: float
INICIO
ESCREVA "Digite seu salário: "
LEIA salario
SE salario <= 1499.15 ENTAO
	sal_liq <- salario
SENAO SE salario >= 1499.16 and salario <= 2246.75 ENTAO
	sal_liq <- salario - (salario - 1499.14) * 0.075
SENAO SE salario >= 2246.76 and salario <= 2995.70 ENTAO
	sal_liq <- salario - (56.06 + (salario - 2246.75) * 0.15
SENAO SE salario >= 2995.71 and salario <= 3743.19 ENTAO
	sal_liq <- salario - (56.06 + 112.34 + (salario - 2995.70) * 0.225)
SENAO 
	sal_liq <- salario - (56.06 + 112.34 + 168.18) - (salario - 3743.19) * 0.275
FIM_SE
ESCREVA "O seu salário liquido é: sal_liq", sal_liq
FIM
```

#### Teste
| salario | salario <= 1499.15 | salario >= 1499.16 <br>and <br>salario <= 2246.75 |salario >= 2246.76 <br>and <br>salario <= 2995.70 | salario >= 2995.71 <br>and <br>salario <= 3743.19 | sal_liq | saída |
| -- | -- | -- | -- | -- | -- | -- |
| 5000.00 |  False | False | False | False  | 4317.54| O seu salário liquido é: 4317.54|
| 2500.00 | False | False | True | | 2405.95 | O seu salário liquido é: 2405.95

### Exercício 18
Converta o critério de avaliação de alunos em escolas brasileiras para o critério utilizado em escolas americanas. Nas escolas brasileiras, a avaliação dos alunos é reportada por uma nota que varia de 0 a 10. Nas escolas americanas, a avaliação dos alunos é baseada em conceitos: A, B, C, D, ou F. <br>a) A (9.0 a 10.0);<br> b) B (8.0 a 8.9); <br>c) C (7.0 a 7.9);<br> d) D (5.0 a 6.9), e <br>e) F (menor que 5.0)
#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite sua nota: }}
B --> C[/nota/]
C --> D{nota < 5}
D --NAO--> E{nota >= 5.0 and nota <= 6.9}
E --NAO--> F{nota >= 7.0 and nota <= 7.9}
F --NAO--> G{nota >= 8.0 and nota <= 8.9}
G --NAO--> H{nota >= 9.0 and nota <= 10.0}
H --NAO--> L{{nota invalida}}
D --SIM--> M{{F}}
E --SIM--> N{{D}}
F --SIM--> O{{C}}
G --SIM--> P{{B}}
H --SIM--> R{{A}}
L & M & N & O & P & R --> S([FIM])





```
#### Pseudocódigo
```
ALGORITMO avaliacao_alunos
DECLARE nota: float
INICIO
ESCREVA "Digite sua nota: "
LEIA nota
SE nota < 5 ENTAO
	ESCREVA "F"
SENAO SE nota >= 5.0 and nota <= 6.9 ENTAO
	ESCREVA "D"
SENAO SE nota >= 7.0 and nota <= 7.9 ENTAO
	ESCREVA "C"
SENAO SE nota >= 8.0 and nota <= 8.9 ENTAO
	ESCREVA "B"
SENAO SE nota >= 9.0 and nota <= 10.0 ENTAO
	ESCREVA "A"
SENAO
	ESCREVA "nota invalida"
FIM_SE
FIM
```

#### Teste
| nota | saída | 
| -- | -- | 
| 5 |  D | 
| 8.9 | B | 
| 5.5 | D |
| 9.9 | A |

### Exercício 19
Leia um número e diga se é: nulo, positivo ou negativo.
#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número: }}
B --> C[/num/]
C --> D{num == 0}
D --NAO--> E{num > 0}
E --NAO--> F{{O seu número é negativo!}}
D --SIM--> G{{o seu número é nulo!}}
E --SIM--> H{{O seu número é positivo!}}
F & G & H --> L([FIM])


```
#### Pseudocódigo
```
ALGORITMO nulo_pos_neg
DECLARE num: float
INICIO
ESCREVA "Digite um número: "
LEIA num
SE num == 0 ENTAO
	ESCREVA "O seu número é nulo!"
SENAO SE num > 0 ENTAO 
	ESCREVA "O seu número é positivo!"
SENAO
	ESCREVA "O seu número é negativo!"	
FIM_SE
FIM
```

#### Teste
| num | num == 0 | num > 0 | saída
| -- | -- | -- | -- |
| 0 |  True |  | O seu número é nulo!
| -1 | False | False | O seu número é negativo!
| 1 | False | True | O seu número é positivo!

### Exercício 20
Receba dois números reais e um operador (vide slide 9). e efetue a operação correspondente com os valores recebidos (operandos). O algoritmo deve retornar o resultado da operação selecionada simulando todas as opeações de uma calculadora simples.
#### Fluxograma
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
#### Pseudocódigo
```
ALGORITMO calculador_simples
DECLARE operacao: string, n1, n2, calc: float
INICIO
ESCREVA "Digite a operação que deseja fazer [+][-][*][/]: "
ESCREVA "Digite os dois números que deseja operar: "
LEIA operacao, n1, n2
SE operacao == "+" ENTAO
	calc <- n1 + n2
SENAO SE operacao == "-" ENTAO
	calc <- n1 - n2
SENAO SE operacao == "*" ENTAO
	calc <- n1 * n2
SENAO SE operacao == "/" ENTAO
	SE n2 == 0 ENTAO
		ESCREVA "Não se pode dividir por zero!"
	SENAO
		calc <- n1 / n2
	FIM_SE
ESCREVA calc
SENAO
	ESCREVA "Simbolo de operação invalido!"
FIM_SE

FIM
```

#### Teste
| operacao | n1 | n2 | saída
| -- | -- | -- | -- |
| / |  10 | 0 | Não se pode dividir por zero!
| + | 5 | 3| 8
| = | 5 | 6 | Simbolo de operação invalido!
| * | 5 | 2 | 10 |
| - | 5 | 10 | -5 |
| - | 10 | 5 | 5 |






























