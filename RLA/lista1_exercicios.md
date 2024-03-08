# UNIFOR
**Nome**: Alisson Frota Teixeira <br>
**Disciplina**: Raciocínio Lógico Algorítimico

## Lista de exercícios 01

### Exercício 3
Represente, em fluxograma e pseudocódigo, um algoritimo para determinar se um número inteiro e positivo é par ou impar

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número: }} 
B --> C[/num/] 
C --> D{num >= 0}
D --NAO--> E{{O número deve ser positivo!}}
E --> F([FIM])
D --SIM--> G[resto = num % 2]
G --> H{resto == 0}
H --NAO--> L{{IMPAR}}
H --SIM--> M{{PAR}}
L --> F
M --> F
```
#### Pseudocódigo
```
ALGORITMO verifica_par_impar
DECLARE num, resto: int
INICIO
ESCREVA "Digite um número: "
LEIA num
SE num >= 0 ENTAO
	resto <- num % 2
	SE resto == 0 ENTAO
		ESCREVA "PAR"
	SENAO
		ESCREVA "IMPAR"
	FIM_SE
SENAO
	ESCREVA "Esse número não e positivo"
FIM_SE
FIM
```

#### Teste
| num | num >= 0 | resto | resto == 0 | saída |
| -- | -- | -- | -- | -- |
| -1 | False |  |  | "O número deve ser positivo" | 0 | True | 0 | True | "O número é par !" | 10 | True | 0 | True | "O número é par!" | 11 | True | 1 | False | "O número e impar" 



