# ISD
---
# Sinais Lógicos das Operações
- **AND** - sinal lógico do produto (multiplicação)
- **OR** - sinal lógico da adição
- **NOT** - inverso

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

# Linguagens, Radicais e Símbolos 
- **Binário** - 2 - 0, 1
- **Octal** - 8 - 0, 1, 2, ..., 7
- **Decimal** - 10 - 0, 1, ..., 9
- **Hexadecimal** - 16 - 0, 1, ..., 9, A, B, C, D, E, F

# Conversão de Binário para as Restantes Bases

| Binário | Decimal | Octal | Hexadecimal |
| :---: | :---: | :---: | :---: |
| 0000 | 0 | 0 | 0 |
| 0001 | 1 | 1 | 1 |
| 0010 | 2 | 2 | 2 |
| 0011 | 3 | 3 | 3 |
| 0100 | 4 | 4 | 4 |
| 0101 | 5 | 5 | 5 |
| 0110 | 6 | 6 | 6 |
| 0111 | 7 | 7 | 7 |
| 1000 | 8 | 10 | 8 |
| 1001 | 9 | 11 | 9 |
| 1010 | 10 | 12 | A |
| 1011 | 11 | 13 | B |
| 1100 | 12 | 14 | C |
| 1101 | 13 | 15 | D |
| 1110 | 14 | 16 | E |
| 1111 | 15 | 17 | F |

# Conversão de Decimal para as Outras Bases (Método das Divisões Sucessivas)

Para convertermos um número decimal para binário, dividimos o número por 2 fazendo sempre uma divisão inteira. O resto da divisão indica um dos dígitos do binário, sendo que o número lê-se da **última divisão para a primeira** (de baixo para cima).

### Exemplo prático: Converter o número 25 para Binário
- $25 \div 2 = 12$ (com resto **1** $\rightarrow$ este é o último dígito do binário)
- $12 \div 2 = 6$ (com resto **0**)
- $6 \div 2 = 3$ (com resto **0**)
- $3 \div 2 = 1$ (com resto **1**)
- $1 \div 2 = 0$ (com resto **1** $\rightarrow$ primeiro dígito)

Lendo os restos da última divisão para a primeira, obtemos o código binário completo: **$25_{10} = 11001_2$**.

# Conversão de Decimal para Hexadecimal

Para convertermos um número decimal para hexadecimal, dividimos o número por 16 fazendo sempre uma divisão inteira. O resto indica o dígito correspondente (lembrando que de 10 a 15 usamos as letras A, B, C, D, E, F), sendo que o número se lê da **última divisão para a primeira** (de baixo para cima).

### Exemplo prático: Converter o número 25 para Hexadecimal
- $25 \div 16 = 1$ (com resto **9**)
- $1 \div 16 = 0$ (com resto **1**)

Lendo os restos da última divisão para a primeira, obtemos: **$25_{10} = 19_{16}$**.

# Casos Especiais de Conversão

## Conversão de Binário para Octal

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

## Conversão de Binário para Hexadecimal

Para converter de binário para hexadecimal, começamos por separar os bits do número binário em **grupos de 4 dígitos**, da direita para a esquerda. 

Se o número de bits à esquerda não for múltiplo de 4, adicionamos zeros à esquerda até completar o grupo. Em seguida, basta converter cada grupo de 4 bits para o seu valor correspondente em hexadecimal.

### Exemplo prático: Converter o binário $11101011_2$ para Hexadecimal
1. **Agrupar de 4 em 4 da direita para a esquerda** (e adicionar zeros à esquerda se necessário):
   * $1110 \quad 1011$

2. **Converter cada grupo isoladamente**:
   * $1110_2 = E_{16}$
   * $1011_2 = B_{16}$

Juntando os dígitos, obtemos o resultado final: **$11101011_2 = EB_{16}$**.

## Conversão de Octal e Hexadecimal para Binário

Para fazer o processo inverso — converter de octal ou hexadecimal para binário —, fazemos o oposto: substituímos cada dígito do número pelo seu grupo correspondente de **3 bits** (no caso do Octal) ou **4 bits** (no caso do Hexadecimal).

### Exemplo 1: Converter o octal $753_8$ para Binário
Convertemos cada dígito isoladamente para 3 bits:
- $7_8 = 111_2$
- $5_8 = 101_2$
- $3_8 = 011_2$

Juntando tudo, obtemos o resultado final: **$753_8 = 111101011_2$**.

---

### Exemplo 2: Converter o hexadecimal $A5E_{16}$ para Binário
Convertemos cada dígito isoladamente para 4 bits (lembrando que $A = 10$ e $E = 14$):
- $A_{16} = 1010_2$
- $5_{16} = 0101_2$
- $E_{16} = 1110_2$

Juntando tudo, obtemos o resultado final: **$A5E_{16} = 101001011110_2$**.

# Conversão de Binário para Decimal

Para convertermos um número binário para decimal, multiplicamos cada bit do número por $2$ elevado à respetiva posição (começando em $0$ da direita para a esquerda) e, em seguida, somamos todos os valores obtidos.

### Exemplo prático: Converter o binário $110111_2$ para Decimal
- $1 \times 2^5 = 1 \times 32 = 32$
- $1 \times 2^4 = 1 \times 16 = 16$
- $0 \times 2^3 = 0 \times 8 = 0$
- $1 \times 2^2 = 1 \times 4 = 4$
- $1 \times 2^1 = 1 \times 2 = 2$
- $1 \times 2^0 = 1 \times 1 = 1$

Somando todas as parcelas: $32 + 16 + 0 + 4 + 2 + 1 = \mathbf{55_{10}}$

# Conversão de Octal para Decimal

Para convertermos um número octal para decimal, multiplicamos cada dígito do número por $8$ elevado à respetiva posição (começando em $0$ da direita para a esquerda) e, em seguida, somamos todos os valores obtidos.

### Exemplo prático: Converter o octal $16532_8$ para Decimal
- $1 \times 8^4 = 1 \times 4096 = 4096$
- $6 \times 8^3 = 6 \times 512 = 3072$
- $5 \times 8^2 = 5 \times 64 = 320$
- $3 \times 8^1 = 3 \times 8 = 24$
- $2 \times 8^0 = 2 \times 1 = 2$

Somando todas as parcelas: $4096 + 3072 + 320 + 24 + 2 = \mathbf{7514_{10}}$

# Conversão de Hexadecimal para Decimal

Para convertermos um número hexadecimal para decimal, multiplicamos cada dígito do número por $16$ elevado à respetiva posição (começando em $0$ da direita para a esquerda) e, em seguida, somamos todos os valores obtidos (lembrando que $A=10, B=11, C=12, D=13, E=14, F=15$).

### Exemplo prático: Converter o hexadecimal $ABE5_{16}$ para Decimal
- $A \times 16^3 = 10 \times 4096 = 40960$
- $B \times 16^2 = 11 \times 256 = 2816$
- $E \times 16^1 = 14 \times 16 = 224$
- $5 \times 16^0 = 5 \times 1 = 5$

Somando todas as parcelas: $40960 + 2816 + 224 + 5 = \mathbf{44005_{10}}$

---
# O que é o BCD 8421

- O **BCD** (*Binary-Coded Decimal*) é um código utilizado em sistemas digitais para representar números decimais (de 0 a 9) usando grupos de **4 bits**.
- A designação **8421** refere-se aos pesos atribuídos a cada uma das 4 posições do bit, da esquerda para a direita ($2^3 = 8, 2^2 = 4, 2^1 = 2, 2^0 = 1$), exatamente igual aos pesos do código binário natural.

### Como é que funciona?

No sistema BCD, **cada dígito decimal individual** (de 0 a 9) é convertido em separado para o seu grupo de 4 bits correspondente. 

Por exemplo, para o número decimal **$25_{10}$**, convertemos cada algarismo isoladamente:
- $2_{10} = 0010_2$
- $5_{10} = 0101_2$

Juntando tudo: **$25_{10} = 0010 \, 0101_{\text{BCD}}$**.

---
# Operações com Números Binários

A adição e a subtração de números binários utilizam técnicas semelhantes às do sistema decimal. A única diferença notória são as regras de cálculo (tabelas operatórias) devido à base 2.

---

## 1. Adição Binária (Soma)

A soma de dois bits segue estas regras fundamentais:
- $0 + 0 = 0$
- $0 + 1 = 1$
- $1 + 0 = 1$
- $1 + 1 = 10$ ($0$ e transporta **$1$** para a coluna seguinte)
- $1 + 1 + 1 = 11$ ($1$ e transporta **$1$** para a coluna seguinte, quando há transporte anterior)

### Exemplo prático: $1011_2 + 0110_2$
```text
    1 1 1     (transportes)
    1 0 1 1   (11 em decimal)
+   0 1 1 0   (6 em decimal)
------------
  1 0 0 0 1   (17 em decimal)
```

---

## 2. Subtração Binária

A subtração de bits segue estas regras:
- $0 - 0 = 0$
- $1 - 0 = 1$
- $1 - 1 = 0$
- $0 - 1 = 1$ (com empréstimo de **$1$** à coluna seguinte, tal como na base 10)

### Exemplo prático: $1010_2 - 0011_2$
```text
    1 0 1 0   (10 em decimal)
-   0 0 1 1   (3 em decimal)
------------
    0 1 1 1   (7 em decimal)
```
*(Nota no bit menos significativo: $0 - 1$ pede emprestado $1$ ao vizinho, ficando $10_2 - 1_2 = 1$).*

# Overflow (Estouro)

Um **overflow** acontece quando o resultado de uma operação aritmética excede o número máximo de bits que o sistema tem capacidade para armazenar.

### Como funciona:

Caso estejamos a trabalhar com um sistema de **4 bits**, o maior número sem sinal que conseguimos representar é o $15$ ($1111_2$).

Se somarmos $9$ e $8$:
- $9_{10} = 1001_2$
- $8_{10} = 1000_2$

Se fizermos a soma binária:
```text
    1 0 0 1   (9)
+   1 0 0 0   (8)
------------
  1 0 0 0 1   (17)
```

O resultado correto é $17$, mas o nosso registador só tem **4 bits** de espaço. Logo, o quinto bit gerado à esquerda "salta fora" e o computador fica apenas com os quatro bits menos significativos (`0001`), que representam o valor **$1$**. 

Ou seja, devido ao overflow, o sistema fica a achar que **$8 + 9 = 1$**!
