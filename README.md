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

# Operações com Números Octais e Hexadecimais

Para adicionar ou subtrair números octais (base 8) ou hexadecimais (base 16), o processo é idêntico ao da base decimal. Começamos sempre a somar pelos **dígitos menos significativos** (à direita) e avançamos para a esquerda, gerando um transporte (*carry*) sempre que o resultado atinge ou ultrapassa o valor da base.

---

## 1. Adição em Octal (Base 8)

Sempre que a soma de uma coluna atinge **$8$ ou mais**, subtraímos $8$ ao resultado e transportamos $1$ para a coluna imediatamente à esquerda.

### Exemplo prático: $47_8 + 25_8$
```text
      1       (transportes)
      4 7 8
+     2 5 8
------------
      7 4 8
```
* **Coluna da direita:** $7 + 5 = 12$. Como $12 \ge 8$, fazemos $12 - 8 = \mathbf{4}$ e transportamos **$1$** para a coluna seguinte.
* **Coluna da esquerda:** $4 + 2 + 1 \text{ (transportado)} = \mathbf{7}$.
* **Resultado final:** **$74_8$**.

---

## 2. Adição em Hexadecimal (Base 16)

Sempre que a soma de uma coluna atinge **$16$ ou mais**, subtraímos $16$ ao resultado e transportamos $1$ para a coluna à esquerda (lembrando que $A=10, B=11, C=12, D=13, E=14, F=15$).

### Exemplo prático: $39_{16} + 58_{16}$
```text
      1       (transportes)
      3 9 16
+     5 8 16
------------
      9 1 16
```
* **Coluna da direita:** $9 + 8 = 17$. Como $17 \ge 16$, fazemos $17 - 16 = \mathbf{1}$ e transportamos **$1$** para a coluna seguinte.
* **Coluna da esquerda:** $3 + 5 + 1 \text{ (transportado)} = \mathbf{9}$.
* **Resultado final:** **$91_{16}$**.
# Subtração em Octal e Hexadecimal

A subtração em bases diferentes da decimal funciona com o mesmo princípio do "empréstimo" (*borrow*), mas com uma regra fundamental: quando pedimos emprestado à coluna da esquerda, **o valor que trazemos para a coluna atual é igual à base** em que estamos a trabalhar ($8$ para octal e $16$ para hexadecimal).

---

## 1. Subtração em Octal (Base 8)

Se o minuendo for menor que o subtraendo numa coluna, pedimos emprestado **$8$** unidades à coluna seguinte.

### Exemplo prático: $53_8 - 25_8$
```text
      4  (11)  (novos valores após empréstimo)
      5   3  8
-     2   5  8
------------
      2   6  8
```
* **Coluna da direita:** $3 - 5$ não é possível. Pedimos emprestado $1$ à coluna das dezenas (o $5$ passa a $4$), e somamos a base ($8$) ao $3$, ficando $3 + 8 = 11$. Agora subtraímos: $11 - 5 = \mathbf{6}$.
* **Coluna da esquerda:** Com o empréstimo, ficamos com $4 - 2 = \mathbf{2}$.
* **Resultado final:** **$26_8$**.

---

## 2. Subtração em Hexadecimal (Base 16)

Se o minuendo for menor que o subtraendo numa coluna, pedimos emprestado **$16$** unidades à coluna seguinte (lembrando que letras representam valores decimais: $A=10, B=11, C=12, D=13, E=14, F=15$).

### Exemplo prático: $52_{16} - 18_{16}$
```text
      4  (18)  (novos valores após empréstimo)
      5   2  16
-     1   8  16
------------
      3   A  16
```
* **Coluna da direita:** $2 - 8$ não é possível. Pedimos emprestado $1$ ao $5$ (que passa a $4$), e somamos a base ($16$) ao $2$, ficando $2 + 16 = 18$. Agora subtraímos: $18 - 8 = \mathbf{10}$. Como $10$ em hexadecimal é a letra **$\text{A}$**, colocamos $\mathbf{A}$.
* **Coluna da esquerda:** $4 - 1 = \mathbf{3}$.
* **Resultado final:** **$3A_{16}$**.

# Representação de Números Negativos

Em sistemas digitais, para além dos números positivos, precisamos de representar números negativos. Como os circuitos só entendem $0$ e $1$, o bit mais à esquerda (**MSB** - *Most Significant Bit*) é utilizado como **bit de sinal**:
* $0$ $\rightarrow$ Número positivo ($+$)
* $1$ $\rightarrow$ Número negativo ($-$)

Existem três métodos principais para representar números com sinal em binário:

---

## 1. Sinal e Magnitude (Sign-Magnitude)

Neste método, o bit mais à esquerda indica o sinal e os restantes bits representam o valor absoluto (magnitude) do número.

* **Exemplo (em 4 bits):** 
  * $+5_{10} = 0101_2$
  * $-5_{10} = 1101_2$ (o bit mais à esquerda passa a $1$)

* **Desvantagem:** O zero tem duas representações possíveis ($+0$ como `0000` e $-0$ como `1000`), o que torna os circuitos de hardware mais complexos.

---

## 2. Complemento para 1 (One's Complement)

Para obter o negativo de um número em Complemento para 1, **invertemos todos os bits** do número positivo respetivo (os $0$ passam a $1$ e os $1$ passam a $0$).

* **Exemplo (em 4 bits):**
  * Queremos representar $-5_{10}$.
  * Sabemos que $+5_{10} = 0101_2$.
  * Invertendo todos os bits: `1010`.
  * Logo, $-5_{10} = 1010_2$ (em complemento para 1).

---

## 3. Complemento para 2 (Two's Complement)

Este é o **método universalmente utilizado nos computadores modernos**. Resolve o problema do duplo zero e permite que a adição e a subtração de números com sinal sejam feitas exatamente com os mesmos circuitos lógicos.

Para converter um número positivo no seu equivalente negativo (ou vice-versa) em Complemento para 2, seguimos dois passos:
1. **Invertemos todos os bits** (aplicamos o Complemento para 1).
2. **Somamos $1$** ao resultado obtido.

### Exemplo prático: Representar $-5_{10}$ em 4 bits (Complemento para 2)

1. Escrevemos o $+5_{10}$ em binário de 4 bits: `0101`
2. Invertemos os bits: `1010`
3. Somamos $1$ ao resultado:
```text
    1 0 1 0
+         1
------------
    1 0 1 1
```
* **Resultado final:** $-5_{10} = 1011_2$ (em complemento para 2).

# Two’s Complement Representation (Complemento para 2)

A representação em **Two’s Complement** (Complemento para 2) é o padrão universal utilizado na arquitetura de computadores para representar números inteiros com sinal. A sua grande vantagem é permitir que a **adição e a subtração sejam executadas pelo mesmo circuito somador**, eliminando também a ambiguidade de existirem dois zeros ($+0$ e $-0$).

---

## 1. Como funciona o peso dos bits

Num sistema de $N$ bits em Complemento para 2, os pesos são idênticos ao binário natural, **exceto o bit mais significativo (MSB - mais à esquerda)**, que assume um **peso negativo** ($-2^{N-1}$).

* **Exemplo em 4 bits:** Os pesos são **$-8, \ 4, \ 2, \ 1$** ($-2^3, 2^2, 2^1, 2^0$).
* **Intervalo de representação:** Com $N$ bits, conseguimos representar números desde **$-2^{N-1}$** até **$2^{N-1} - 1$**.
  * Para **4 bits**: de **$-8$** (`1000`) até **$+7$** (`0111`).
  * Para **8 bits**: de **$-128$** (`10000000`) até **$+127$** (`01111111`).

---

## 2. Como converter um número negativo para Binário (Two's Complement)

Para obter a representação binária de um número negativo (ex: $-6_{10}$ em 4 bits):

1. Escrevemos o valor absoluto em binário positivo: **$+6_{10} = 0110_2$**
2. **Invertemos todos os bits** (Complemento para 1): **`1001`**
3. **Somamos $1$** ao resultado:
```text
    1 0 0 1
+         1
------------
    1 0 1 0
```
* **Resultado:** $-6_{10} = \mathbf{1010_2}$.
* *(Verificação pelos pesos: $-8 + 0 + 2 + 0 = -6$)*

---

## 3. Como converter de Two's Complement para Decimal

* **Se o bit mais à esquerda (MSB) for `0`:** O número é positivo; converte-se normalmente.
* **Se o bit mais à esquerda (MSB) for `1`:** O número é negativo. Podemos aplicar o processo inverso (inverter os bits e somar $1$ para descobrir a magnitude) ou somar diretamente os pesos considerando o MSB negativo.

### Exemplo prático: Converter `1101` (4 bits) para Decimal
* **Método dos pesos:** $(-1 \times 8) + (1 \times 4) + (0 \times 2) + (1 \times 1) = -8 + 4 + 0 + 1 = \mathbf{-3_{10}}$.
* **Método da inversão:** Invertemos `1101` $\rightarrow$ `0010`, somamos $1$ $\rightarrow$ `0011` ($3_{10}$). Como começava por `1`, o valor é **$-3_{10}$**.

---

## 4. Subtração usando Adição ($A - B = A + (-B)$)

Com Complemento para 2, subtrair dois números resume-se a somar o primeiro com o complemento para 2 do segundo. Qualquer transporte (*carry out*) que saia fora do número de bits definido é simplesmente ignorado.

### Exemplo prático: $7 - 3$ em 4 bits ($7 + (-3)$)
* $+7_{10} = 0111_2$
* $-3_{10} = 1101_2$

```text
    1 1 1 1     (transportes)
    0 1 1 1     (+7)
+   1 1 0 1     (-3)
------------
  1 0 1 0 0     (o 5.º bit '1' à esquerda é descartado)
```
* Ficamos com os 4 bits: **`0100`** = **$+4_{10}$**.

# Gray Code (Código Gray)

O **Gray Code** (ou código binário refletido) é um sistema de numeração binária onde **dois valores sucessivos diferem em apenas um único bit**. 

Enquanto no binário natural a transição de $7$ (`0111`) para $8$ (`1000`) altera todos os 4 bits em simultâneo, no código Gray apenas 1 bit muda de cada vez.

---

## 1. Porquê que o Código Gray é importante?

Em sistemas eletromecânicos (como *encoders* de posição, sensores industriais ou rodas óticas), se vários bits mudarem exatamente ao mesmo tempo, pequenas diferenças no tempo de comutação (*skew*) podem fazer com que o sistema leia temporariamente um valor totalmente errado. Como no código Gray **só um bit muda de cada vez**, este problema de transição é totalmente eliminado.

---

## 2. Tabela comparativa (Binário vs. Gray de 4 bits)

| Decimal | Binário Natural | Código Gray |
| :---: | :---: | :---: |
| **0** | `0000` | `0000` |
| **1** | `0001` | `0001` |
| **2** | `0010` | `0011` |
| **3** | `0011` | `0010` |
| **4** | `0100` | `0110` |
| **5** | `0101` | `0111` |
| **6** | `0110` | `0101` |
| **7** | `0111` | `0100` |
| **8** | `1000` | `1100` |
| **9** | `1001` | `1101` |
| **10** | `1010` | `1111` |
| **11** | `1011` | `1110` |
| **12** | `1100` | `1010` |
| **13** | `1101` | `1011` |
| **14** | `1110` | `1001` |
| **15** | `1111` | `1000` |

---

## 3. Como converter de Binário para Gray

1. O **bit mais à esquerda (MSB)** do código Gray é exatamente igual ao MSB do binário.
2. Para encontrar os bits seguintes, fazemos a operação **XOR exclusivo** ($\oplus$) entre o bit atual do binário e o bit anterior do binário.

### Exemplo: Converter o binário $1011_2$ para Gray
* 1.º bit (mais à esquerda): mantém-se $\rightarrow$ **`1`**
* 2.º bit: $1 \oplus 0 = \mathbf{1}$
* 3.º bit: $0 \oplus 1 = \mathbf{1}$
* 4.º bit: $1 \oplus 1 = \mathbf{0}$
* **Resultado:** $1011_2$ em binário corresponde a **$1110_{\text{Gray}}$**.

---

## 4. Como converter de Gray para Binário

1. O **bit mais à esquerda (MSB)** mantém-se igual.
2. Para os bits seguintes, fazemos a operação **XOR** entre o bit do Gray atual e o **bit do resultado binário já calculado** na posição anterior.

### Exemplo: Converter o código Gray $1110_{\text{Gray}}$ para Binário
* 1.º bit: mantém-se $\rightarrow$ **`1`**
* 2.º bit: $1 \text{ (Gray)} \oplus 1 \text{ (Binário anterior)} = \mathbf{0}$
* 3.º bit: $1 \text{ (Gray)} \oplus 0 \text{ (Binário anterior)} = \mathbf{1}$
* 4.º bit: $0 \text{ (Gray)} \oplus 1 \text{ (Binário anterior)} = \mathbf{1}$
* **Resultado:** $1110_{\text{Gray}}$ corresponde a **$1011_2$** em binário.

# Circuitos Combinacionais

Os **circuitos combinacionais** são circuitos digitais cujas **saídas dependem única e exclusivamente da combinação atual das entradas** num determinado instante. 

Ao contrário dos circuitos sequenciais, **não possuem elementos de memória** (como flip-flops ou latches) nem realimentação (*feedback*), o que significa que não têm capacidade de armazenar estados anteriores.

---

## 1. Características Principais

* **Sem memória:** O passado não afeta o presente; se as entradas forem iguais, a saída será sempre a mesma, independentemente do que aconteceu antes.
* **Modelo Matemático:** Podem ser integralmente descritos por uma ou mais **tabelas da verdade** ou por **expressões booleanas** simplificadas (muitas vezes otimizadas através de mapas de Karnaugh).
* **Atraso de Propagação ($T_{pd}$):** Como os sinais precisam de percorrer portas lógicas em série, existe sempre um pequeno atraso temporal desde que as entradas mudam até que a saída estabilize.

---

## 2. Exemplos Comuns de Circuitos Combinacionais

Os blocos lógicos combinacionais mais utilizados em sistemas digitais incluem:

### A. Descodificadores (Decoders)
* **Função:** Possui $N$ entradas e até $2^N$ saídas. Ativa apenas **uma** saída específica correspondente ao valor binário presente nas entradas.
* **Exemplo:** Um descodificador de $2 \times 4$ ativa a saída $S_3$ se a entrada for `11`.

### B. Codificadores (Encoders)
* **Função:** É o inverso do descodificador. Tem $2^N$ entradas (onde apenas uma está ativa de cada vez) e gera uma saída binária de $N$ bits correspondente a essa entrada.

### C. Multiplexadores (MUX)
* **Função:** Funciona como um "comutador" ou seletor. Tem várias entradas de dados, entradas de seleção (*select lines*) e **uma única saída**. Direciona o sinal de uma das entradas de dados para a saída, dependendo do código selecionado.
* **Exemplo:** Um MUX de $4$ para $1$ ($4$-to-$1$ MUX) usa $2$ linhas de seleção para escolher qual das $4$ entradas é transmitida para a saída.

### D. Desmultiplexadores (DEMUX)
* **Função:** Faz o oposto do MUX. Recebe um sinal de entrada e distribui-o por uma de várias saídas possíveis, escolhida através de linhas de seleção.

### E. Somadores (Adders)
* **Half-Adder (Meio-Somador):** Soma dois bits ($A$ e $B$) e produz duas saídas: a Soma ($S$) e o Transporte de saída ($C_{out}$). Utiliza uma porta XOR para a soma e uma porta AND para o transporte.
* **Full-Adder (Somador Completo):** Soma dois bits mais um transporte de entrada anterior ($C_{in}$), permitindo encadear vários somadores para criar somadores de vários bits (ex: 4 ou 8 bits).

# Axiomas e Leis da Álgebra de Boole

A **Álgebra de Boole** é a estrutura matemática que suporta a lógica digital. Os axiomas, leis e propriedades seguintes são utilizados para analisar, simplificar e otimizar expressões lógicas e circuitos combinacionais.

---

## 1. Postulados Básicos (Axiomas)
Considerando variáveis binárias ($A, B, C \in \{0, 1\}$):

* **Identidade:**
  * $A \cdot 1 = A$
  * $A + 0 = A$

* **Anulação (ou Domínio):**
  * $A \cdot 0 = 0$
  * $A + 1 = 1$

* **Idempotência:**
  * $A \cdot A = A$
  * $A + A = A$

* **Complementaridade (ou Inversão):**
  * $A \cdot A' = 0$
  * $A + A' = 1$

* **Involução (Dupla Negação):**
  * $(A')' = A$

---

## 2. Propriedades e Leis Fundamentais

* **Propriedade Comutativa:**
  * $A + B = B + A$
  * $A \cdot B = B \cdot A$

* **Propriedade Associativa:**
  * $(A + B) + C = A + (B + C)$
  * $(A \cdot B) \cdot C = A \cdot (B \cdot C)$

* **Propriedade Distributiva:**
  * $A \cdot (B + C) = (A \cdot B) + (A \cdot C)$
  * $A + (B \cdot C) = (A + B) \cdot (A + C)$ *(Nota: esta segunda lei é específica da Álgebra de Boole e não existe na álgebra comum).*

---

## 3. Leis de Simplificação Avançada

* **Lei da Absorção:**
  * $A + (A \cdot B) = A$
  * $A \cdot (A + B) = A$
  * $A + (A' \cdot B) = A + B$
  * $A \cdot (A' + B) = A \cdot B$

* **Teoremas de De Morgan (Essenciais para conversão de portas):**
  * $\overline{A \cdot B} = A' + B'$ *(A NAND é equivalente a uma OR de entradas invertidas)*
  * $\overline{A + B} = A' \cdot B'$ *(A NOR é equivalente a uma AND de entradas invertidas)*

# Single-Variable Theorems (Teoremas de Uma Variável)

Na Álgebra de Boole, os **teoremas de uma única variável** envolvem apenas uma variável lógica ($A$) e as constantes ($0$ ou $1$). Estes teoremas são ferramentas básicas mas essenciais para simplificar expressões booleanas e otimizar circuitos combinacionais.

---

## 1. Teoremas com as Constantes (0 e 1)

Estes teoremas descrevem o comportamento de uma variável quando operada com os valores lógicos fixos $0$ e $1$:

* **Identidade:**
  * $A + 0 = A$ *(somar zero não altera o valor)*
  * $A \cdot 1 = A$ *(multiplicar por um não altera o valor)*

* **Anulação (ou Domínio):**
  * $A + 1 = 1$ *(qualquer coisa somada a 1 resulta em 1)*
  * $A \cdot 0 = 0$ *(qualquer coisa multiplicada por 0 resulta em 0)*

---

## 2. Teoremas de Idempotência

Demonstram o que acontece quando uma variável é operada consigo mesma:

* $A + A = A$
* $A \cdot A = A$

---

## 3. Teoremas de Complementaridade

Descrevem a interação entre uma variável e o seu complemento (o seu inverso lógico):

* $A + A' = 1$ *(uma variável somada ao seu inverso dá sempre verdadeiro)*
* $A \cdot A' = 0$ *(uma variável multiplicada pelo seu inverso dá sempre falso)*

---

## 4. Teorema da Involução (Dupla Negação)

* $(A')' = A$ *(negar uma variável duas vezes anula a negação, regressando ao valor original)*

# Two- and Three-Variable Theorems (Teoremas de Duas e Três Variáveis)

Estes teoremas envolvem múltiplas variáveis lógicas ($A, B, C$) e permitem simplificar e transformar expressões booleanas complexas em circuitos combinacionais.

---

## 1. Propriedades e Leis de Duas Variáveis

* **Propriedade Comutativa:**
  * $A + B = B + A$
  * $A \cdot B = B \cdot A$

* **Propriedade Associativa:**
  * $(A + B) + C = A + (B + C)$
  * $(A \cdot B) \cdot C = A \cdot (B \cdot C)$

* **Lei da Absorção (Duas Variáveis):**
  * $A + (A \cdot B) = A$
  * $A \cdot (A + B) = A$
  * $A + (A' \cdot B) = A + B$
  * $A \cdot (A' + B) = A \cdot B$

---

## 2. Teoremas de Três Variáveis

* **Propriedade Distributiva:**
  * $A \cdot (B + C) = (A \cdot B) + (A \cdot C)$
  * $A + (B \cdot C) = (A + B) \cdot (A + C)$ *(exclusiva da Álgebra de Boole)*

* **Teorema do Consenso (Consensus Theorem):**
  * $(A \cdot B) + (A' \cdot C) + (B \cdot C) = (A \cdot B) + (A' \cdot C)$
  * $(A + B) \cdot (A' + C) \cdot (B + C) = (A + B) \cdot (A' + C)$
  *(O termo redundante $B \cdot C$ ou $(B + C)$ pode ser eliminado).*

* **Teoremas de De Morgan (Essenciais para equivalência de portas):**
  * $\overline{A \cdot B} = A' + B'$
  * $\overline{A + B} = A' \cdot B'$

# Principle of Duality (Princípio da Dualidade)

O **Princípio da Dualidade** afirma que qualquer teorema, axioma ou identidade válida na Álgebra de Boole permanece igualmente verdadeiro se trocarmos entre si os operadores lógicos e os elementos identidade.

Na prática, isto significa que todos os teoremas booleanos existem em **pares duais**: se provares um deles, o seu dual é automaticamente verdadeiro sem precisar de demonstração adicional.

---

## 1. Como obter a expressão Dual

Para encontrar o **dual** de qualquer expressão booleana, aplicamos duas regras simultâneas (mantendo as variáveis e os seus complementos inalterados):

1. **Trocar os operadores:** Substituir todos os **AND** ($\cdot$) por **OR** ($+$), e todos os **OR** ($+$) por **AND** ($\cdot$).
2. **Trocar as constantes:** Substituir todos os **$0$** por **$1$**, e todos os **$1$** por **$0$**.

> **Nota importante:** As variáveis ($A, B, C...$) e as suas negações ($A', B'$) **não são alteradas** (ao contrário do que acontece nos Teoremas de De Morgan). Atenção também à ordem de precedência: o AND tem prioridade sobre o OR, pelo que deves usar parênteses para preservar a estrutura original da operação ao fazer a troca.

---

## 2. Exemplos de Pares Duais

| Teorema Original | Expressão Dual | Nome / Propriedade |
| :--- | :--- | :--- |
| $A + 0 = A$ | $A \cdot 1 = A$ | Identidade |
| $A + 1 = 1$ | $A \cdot 0 = 0$ | Anulação |
| $A + A = A$ | $A \cdot A = A$ | Idempotência |
| $A + A' = 1$ | $A \cdot A' = 0$ | Complementaridade |
| $A + (B \cdot C) = (A + B) \cdot (A + C)$ | $A \cdot (B + C) = (A \cdot B) + (A \cdot C)$ | Distributiva |
| $A + (A \cdot B) = A$ | $A \cdot (A + B) = A$ | Absorção |

### Exemplo prático com parênteses:
* **Expressão original:** $F = (A \cdot B) + (C' \cdot 1)$
* **Expressão dual ($F^D$):** $F^D = (A + B) \cdot (C' + 0)$

# Truth Table (Tabela da Verdade)

Uma **Tabela da Verdade** (*Truth Table*) é uma representação matemática que lista todas as combinações possíveis dos valores das entradas lógicas de um circuito (ou expressão booleana) e mostra o valor correspondente da(s) saída(s) para cada caso.

---

## 1. Número de Combinações (Linhas)

Se um circuito possui **$N$ variáveis de entrada**, o número total de linhas (combinações binárias possíveis) na tabela é dado por:

$$\text{Número de linhas} = 2^N$$

* **$2$ entradas** ($A, B$) $\rightarrow 2^2 = \mathbf{4}$ linhas (de `00` a `11`)
* **$3$ entradas** ($A, B, C$) $\rightarrow 2^3 = \mathbf{8}$ linhas (de `000` a `111`)
* **$4$ entradas** ($A, B, C, D$) $\rightarrow 2^4 = \mathbf{16}$ linhas (de `0000` a `1111`)

---

## 2. Como construir uma Tabela da Verdade

Para evitar saltar combinações, as entradas preenchem-se sempre em **ordem binária crescente** (do $0$ até $2^N - 1$):
* A coluna mais à direita (LSB) alterna a cada linha: `0, 1, 0, 1...`
* A segunda coluna da direita alterna de 2 em 2: `0, 0, 1, 1...`
* A terceira coluna alterna de 4 em 4: `0, 0, 0, 0, 1, 1, 1, 1...`

---

## 3. Exemplo Prático: Expressão $F = (A \cdot B) + C'$

Como temos $3$ variáveis ($A, B, C$), a tabela terá $2^3 = 8$ linhas. Para facilitar o cálculo manual, podemos incluir colunas intermédias ($A \cdot B$ e $C'$):

| Linha | A | B | C | $A \cdot B$ | $C'$ | **F = $(A \cdot B) + C'$** |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **0** | 0 | 0 | 0 | 0 | 1 | **1** |
| **1** | 0 | 0 | 1 | 0 | 0 | **0** |
| **2** | 0 | 1 | 0 | 0 | 1 | **1** |
| **3** | 0 | 1 | 1 | 0 | 0 | **0** |
| **4** | 1 | 0 | 0 | 0 | 1 | **1** |
| **5** | 1 | 0 | 1 | 0 | 0 | **0** |
| **6** | 1 | 1 | 0 | 1 | 1 | **1** |
| **7** | 1 | 1 | 1 | 1 | 0 | **1** |
