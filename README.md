# ISD
---
# Sinais logicos das operações
* AND - sinal logico do produto ( multiplicação )
* OR - sinal logico da adição
* NOT - inverso

# Tabelas 
### 1. AND (Produto Lógico)
| A | B | A · B |
| :---: | :---: | :---: |
| 0 | 0 | **0** |
| 0 | 1 | **0** |
| 1 | 0 | **0** |
| 1 | 1 | **1** |

### 2. OR (Adição Lógica)
| A | B | A + B |
| :---: | :---: | :---: |
| 0 | 0 | **0** |
| 0 | 1 | **1** |
| 1 | 0 | **1** |
| 1 | 1 | **1** |

### 3. NOT (Inversor)
| A | A' (NOT) |
| :---: | :---: |
| 0 | **1** |
| 1 | **0** |

### 4. NAND (Not-AND)
| A | B | $\overline{A \cdot B}$ |
| :---: | :---: | :---: |
| 0 | 0 | **1** |
| 0 | 1 | **1** |
| 1 | 0 | **1** |
| 1 | 1 | **0** |

### 5. NOR (Not-OR)
| A | B | $\overline{A + B}$ |
| :---: | :---: | :---: |
| 0 | 0 | **1** |
| 0 | 1 | **0** |
| 1 | 0 | **0** |
| 1 | 1 | **0** |

### 6. XOR (Ou Exclusivo)
| A | B | $A \oplus B$ |
| :---: | :---: | :---: |
| 0 | 0 | **0** |
| 0 | 1 | **1** |
| 1 | 0 | **1** |
| 1 | 1 | **0** |

### 7. XNOR (Equivalência)
| A | B | $\overline{A \oplus B}$ |
| :---: | :---: | :---: |
| 0 | 0 | **1** |
| 0 | 1 | **0** |
| 1 | 0 | **0** |
| 1 | 1 | **1** |

# Linguagens, radicais e simbolos 

* Binario - 2 - 0, 1
* Octanal - 8 - 0, 1, 2, ...,7
* Decimal - 10 - 0, 1, ..., 9
* Hexadecimal - 16 - 0, 1, ..., 9, A, B, C, D, E, F

# Conversão de Binário para as restantes bases

| Binário | Decimal | Octal | Hexadecimal |
| :---: | :---: | :---: | :---: |
| 0000 | 0 | 0 | 0 |
| 0001 | 1 | 1 | 1 |
| 0010 | 2 | 2 | 2 |
| 0011 | 3 | 3 | 3 |
| 0100 | 4 | 4 | 4 |
| 0101 | 5 | 5 | 5 |
| 0110 | 6 | 6 | 6 |
| 0111 | 7 | 7 | 7 
| 1000 | 8 | 10 | 8 |
| 1001 | 9 | 11 | 9 |
| 1010 | 10 | 12 | A |
| 1011 | 11 | 13 | B |
| 1100 | 12 | 14 | C |
| 1101 | 13 | 15 | D |
| 1110 | 14 | 16 | E |
| 1111 | 15 | 17 | F |


# Conversão de Decimal para as outras bases (Método das Divisões Sucessivas)

Para convertermos um número decimal para binário, dividimos o número por 2 fazendo sempre uma divisão inteira. O resto da divisão indica um dos dígitos do binário, sendo que o número lê-se da **última divisão para a primeira** (de baixo para cima).

### Exemplo prático: Converter o número 25 para Binário

* $25 \div 2 = 12$ (com resto **1** $\rightarrow$ este é o último dígito do binário)
* $12 \div 2 = 6$ (com resto **0**)
* $6 \div 2 = 3$ (com resto **0**)
* $3 \div 2 = 1$ (com resto **1**)
* $1 \div 2 = 0$ (com resto **1** $\rightarrow$ primeiro dígito)

Lendo os restos da última divisão para a primeira, obtemos o código binario completo: **$25_{10} = 11001_2$**.

# Conversão de Decimal para Hexadecimal

Para convertermos um número decimal para hexadecimal, dividimos o número por 16 fazendo sempre uma divisão inteira. O resto indica o dígito correspondente (lembrando que de 10 a 15 usamos as letras A, B, C, D, E, F), sendo que o número se lê da **última divisão para a primeira** (de baixo para cima).

### Exemplo prático: Converter o número 25 para Hexadecimal

* $25 \div 16 = 1$ (com resto **9**)
* $1 \div 16 = 0$ (com resto **1**)

Lendo os restos da última divisão para a primeira, obtemos: **$25_{10} = 19_{16}$**.

# Casos especias de conversão

# Conversão de Binário para Octal

Para converter de binário para octal, começamos por separar os bits do número binário em **grupos de 3 dígitos**, da direita para a esquerda. 

Se o número de bits à esquerda não for múltiplo de 3, adicionamos zeros à esquerda até completar o grupo. Em seguida, basta converter cada grupo de 3 bits para o seu valor correspondente em decimal/octal.

### Exemplo prático: Converter o binário $11101011_2$ para Octal

1. **Agrupar de 3 em 3 da direita para a esquerda** (e adicionar zeros à esquerda se necessário):
   * $011 \quad 101 \quad 011$

2. **Converter cada grupo isoladamente**:
   * $011_2 = 3_8$
   * $101_2 = 5_8$
   * $011_2 = 3_8$

Juntando os dígitos, obtemos o resultado final: **$011101011_2 = 353_8$**.

# Conversão de Binário para Hexadecimal

Para converter de binário para hexadecimal, começamos por separar os bits do número binário em **grupos de 4 dígitos**, da direita para a esquerda. 

Se o número de bits à esquerda não for múltiplo de 4, adicionamos zeros à esquerda até completar o grupo. Em seguida, basta converter cada grupo de 4 bits para o seu valor correspondente em hexadecimal.

### Exemplo prático: Converter o binário $11101011_2$ para Hexadecimal

1. **Agrupar de 4 em 4 da direita para a esquerda** (e adicionar zeros à esquerda se necessário):
   * $1110 \quad 1011$

2. **Converter cada grupo isoladamente**:
   * $1110_2 = E_{16}$
   * $1011_2 = B_{16}$

Juntando os dígitos, obtemos o resultado final: **$11101011_2 = EB_{16}$**.
# Conversão de Octal e Hexadecimal para Binário

Para fazer o processo inverso — converter de octal ou hexadecimal para binário —, fazemos o opuesto: substituímos cada dígito do número pelo seu grupo correspondente de **3 bits** (no caso do Octal) ou **4 bits** (no caso do Hexadecimal).

### Exemplo 1: Converter o octal $753_8$ para Binário

Convertemos cada dígito isoladamente para 3 bits:
* $7_8 = 111_2$
* $5_8 = 101_2$
* $3_8 = 011_2$

Juntando tudo, obtemos o resultado final: **$753_8 = 111101011_2$**.

---

### Exemplo 2: Converter o hexadecimal $A5E_{16}$ para Binário

Convertemos cada dígito isoladamente para 4 bits (lembrando que $A = 10$ e $E = 14$):
* $A_{16} = 1010_2$
* $5_{16} = 0101_2$
* $E_{16} = 1110_2$

Juntando tudo, obtemos o resultado final: **$A5E_{16} = 101001011110_2$**.

# Conversões para decimal
* Para convertermos um numero binario para decimal é muito simples, cada elemento do numero multiplica por 2 elevado ao numero da posição que se encontra contando com o 0 e em seguida somamos os valores obtendo um valor total que é a correspondencia em decimal:

* Por exemplo 110111:

* 1 * 2⁵ = 10
* 1 * 2⁴ = 8
* 0 * 2³ = 0
* 1 * 2² = 4
* 1 * 2¹ = 2
* 1 * 2⁰ = 1

* 10 + 8 + 0 + 4 + 2 + 1 = 25
