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

# Minterms and Maxterms (Mintermos e Maxtermos)

Os **Minterms** e **Maxterms** são as formas padrão (canónicas) de representar funções booleanas diretamente a partir de uma Tabela da Verdade. Permitem escrever qualquer expressão lógica de forma sistemática antes de a simplificar.

---

## 1. Minterms ($m_i$) — Soma de Produtos (SOP)

Um **Minterm** é um termo de **produto (AND)** onde **todas** as variáveis da função aparecem exatamente uma vez (na forma normal ou complementada). Cada minterm avalia para **`1`** numa única linha específica da tabela da verdade e para `0` em todas as outras.

* **Regra de escrita:**
  * Variável $= 1 \rightarrow$ escreve-se na forma **normal** ($A$).
  * Variável $= 0 \rightarrow$ escreve-se na forma **complementada** ($A'$).

* **Forma Canónica SOP (*Sum of Products*):** A expressão final da função é a **soma (OR)** de todos os minterms onde a saída da tabela da verdade é igual a **`1`**.

---

## 2. Maxterms ($M_i$) — Produto de Somas (POS)

Um **Maxterm** é um termo de **soma (OR)** onde **todas** as variáveis da função aparecem exatamente uma vez. Cada maxterm avalia para **`0`** numa única linha específica da tabela da verdade e para `1` em todas as outras.

* **Regra de escrita (inversa aos minterms):**
  * Variável $= 0 \rightarrow$ escreve-se na forma **normal** ($A$).
  * Variável $= 1 \rightarrow$ escreve-se na forma **complementada** ($A'$).

* **Forma Canónica POS (*Product of Sums*):** A expressão final da função é o **produto (AND)** de todos os maxterms onde a saída da tabela da verdade é igual a **`0`**.

---

## 3. Tabela de Referência (3 Variáveis: $A, B, C$)

| Linha ($i$) | A | B | C | Minterm ($m_i$) | Maxterm ($M_i$) |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **0** | 0 | 0 | 0 | $m_0 = A' \cdot B' \cdot C'$ | $M_0 = A + B + C$ |
| **1** | 0 | 0 | 1 | $m_1 = A' \cdot B' \cdot C$ | $M_1 = A + B + C'$ |
| **2** | 0 | 1 | 0 | $m_2 = A' \cdot B \cdot C'$ | $M_2 = A + B' + C$ |
| **3** | 0 | 1 | 1 | $m_3 = A' \cdot B \cdot C$ | $M_3 = A + B' + C'$ |
| **4** | 1 | 0 | 0 | $m_4 = A \cdot B' \cdot C'$ | $M_4 = A' + B + C$ |
| **5** | 1 | 0 | 1 | $m_5 = A \cdot B' \cdot C$ | $M_5 = A' + B + C'$ |
| **6** | 1 | 1 | 0 | $m_6 = A \cdot B \cdot C'$ | $M_6 = A' + B' + C$ |
| **7** | 1 | 1 | 1 | $m_7 = A \cdot B \cdot C$ | $M_7 = A' + B' + C'$ |

*(Nota: Pela Lei de De Morgan, cada maxterm é o complemento exato do minterm da mesma linha: $M_i = (m_i)'$).*

---

## 4. Exemplo Prático de Extração

Considera uma função $F(A, B, C)$ que tem saída **`1`** apenas nas linhas **1, 4 e 7** (e saída **`0`** nas linhas **0, 2, 3, 5 e 6**):

* **Em Soma de Minterms (SOP):**
  $$F(A, B, C) = \sum m(1, 4, 7) = m_1 + m_4 + m_7$$
  $$F(A, B, C) = (A' \cdot B' \cdot C) + (A \cdot B' \cdot C') + (A \cdot B \cdot C)$$

* **Em Produto de Maxterms (POS):**
  $$F(A, B, C) = \prod M(0, 2, 3, 5, 6) = M_0 \cdot M_2 \cdot M_3 \cdot M_5 \cdot M_6$$
  $$F(A, B, C) = (A+B+C) \cdot (A+B'+C) \cdot (A+B'+C') \cdot (A'+B+C') \cdot (A'+B'+C)$$

# Combinational Circuit Analysis (Análise de Circuitos Combinacionais)

A **análise de um circuito combinacional** consiste no processo inverso ao projeto (*design*): partimos de um **diagrama lógico já construído** (esquema de portas lógicas) e determinamos qual é a sua **função booleana** e a sua **Tabela da Verdade**, de modo a compreender exatamente o que o circuito faz.

---

## 1. Passos para Analisar um Circuito

Para analisar qualquer circuito combinacional de forma sistemática, seguimos 4 etapas:

1. **Verificar se é combinacional:** Garantir que o circuito não tem elementos de memória (flip-flops) nem ciclos de realimentação (*feedback* de uma saída de volta para uma entrada anterior).
2. **Identificar as entradas e saídas:** Atribuir nomes a todas as entradas primárias (ex: $A, B, C$) e às saídas finais (ex: $F$ ou $Y$).
3. **Etiquetar os nós intermédios (Níveis Lógicos):** Avançar da esquerda (entradas) para a direita (saídas), escrevendo a expressão booleana à saída de cada porta lógica (ex: $T_1, T_2, T_3...$).
4. **Obter a expressão final e a Tabela da Verdade:** Substituir as expressões intermédias até obter a equação da saída apenas em função das entradas primárias. Se necessário, simplificar algebricamente e construir a tabela da verdade correspondente.

---

## 2. Exemplo Prático Passo a Passo

Imagina um circuito com três entradas ($A, B, C$) e uma saída ($F$), composto por:
* Uma porta **AND** que recebe $A$ e $B$ (saída $T_1$).
* Uma porta **NOT** que recebe $C$ (saída $T_2$).
* Uma porta **OR** que recebe $B$ e $T_2$ (saída $T_3$).
* Uma porta **AND** final que recebe $T_1$ e $T_3$ para gerar a saída **$F$**.

### Passo 1: Escrever as expressões por níveis
* **Nível 1 (portas ligadas diretamente às entradas):**
  * $T_1 = A \cdot B$
  * $T_2 = C'$
* **Nível 2:**
  * $T_3 = B + T_2 = B + C'$
* **Nível 3 (Saída final):**
  * $F = T_1 \cdot T_3$

### Passo 2: Substituir e Simplificar a Expressão Final
Substituímos $T_1$ e $T_3$ na equação de $F$:
$$F = (A \cdot B) \cdot (B + C')$$

Aplicando a propriedade distributiva e as leis da Álgebra de Boole:
$$F = (A \cdot B \cdot B) + (A \cdot B \cdot C')$$
$$F = (A \cdot B) + (A \cdot B \cdot C') \quad \text{(Idempotência: } B \cdot B = B\text{)}$$
$$F = A \cdot B \quad \text{(Lei da Absorção: } X + X \cdot Y = X\text{)}$$

> **Conclusão da Análise:** Apesar de o circuito original usar 4 portas lógicas e depender da entrada $C$, a análise revela que a entrada $C$ é redundante e o circuito comporta-se exatamente como uma simples porta **AND** entre $A$ e $B$ ($F = A \cdot B$).

---

## 3. Tabela da Verdade Resultante

| A | B | C | $T_1 = A \cdot B$ | $T_3 = B + C'$ | **F = $T_1 \cdot T_3$** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 0 | 0 | 0 | 0 | 1 | **0** |
| 0 | 0 | 1 | 0 | 0 | **0** |
| 0 | 1 | 0 | 0 | 1 | **0** |
| 0 | 1 | 1 | 0 | 1 | **0** |
| 1 | 0 | 0 | 0 | 1 | **0** |
| 1 | 0 | 1 | 0 | 0 | **0** |
| 1 | 1 | 0 | 1 | 1 | **1** |
| 1 | 1 | 1 | 1 | 1 | **1** |

# Karnaugh Maps (Mapas de Karnaugh / Mapas K)

Os **Mapas de Karnaugh** (ou **Mapas K**) são uma ferramenta gráfica utilizada para simplificar expressões booleanas e otimizar circuitos combinacionais de forma visual, sem a necessidade de aplicar sucessivamente as leis algébricas (evitando erros e termos complexos).

---

## 1. Como funciona um Mapa de Karnaugh?

Um mapa K é uma representação em grelha da Tabela da Verdade, organizada de forma que **cada célula adjacente difere em apenas um único bit** (utilizando a propriedade do Código Gray). 

* Agrupando células adjacentes que contêm o valor **`1`** (em potências de 2: grupos de $1, 2, 4, 8, 16...$), conseguimos eliminar variáveis que mudam de estado, obtendo a expressão lógica mais simplificada na forma de **Soma de Produtos (SOP)**.

---

## 2. Dimensões dos Mapas K (por número de variáveis)

* **2 Variáveis ($2^2 = 4$ células):** Organizado numa grelha de $2 \times 2$.
* **3 Variáveis ($2^3 = 8$ células):** Organizado numa grelha de $2 \times 4$ (as colunas usam o código Gray: `00, 01, 11, 10`).
* **4 Variáveis ($2^4 = 16$ células):** Organizado numa grelha de $4 \times 4$ (linhas e colunas em código Gray: `00, 01, 11, 10`).

---

## 3. Exemplo Prático: Simplificação com um Mapa K de 3 Variáveis ($A, B, C$)

Imagine a função $F(A, B, C) = \sum m(0, 2, 4, 6)$ (saídas `1` nas linhas correspondentes aos minterms 0, 2, 4 e 6).

### Construção do Mapa K:
As linhas representam $A$ (`0` ou `1`) e as colunas representam $BC$ (`00, 01, 11, 10` em código Gray):

| $A \backslash BC$ | `00` ($B'C'$) | `01` ($B'C$) | `11` ($BC$) | `10` ($BC'$) |
| :---: | :---: | :---: | :---: | :---: |
| **`0`** | **1** ($m_0$) | 0 ($m_1$) | 0 ($m_3$) | **1** ($m_2$) |
| **`1`** | **1** ($m_4$) | 0 ($m_5$) | 0 ($m_7$) | **1** ($m_6$) |

### Agrupamento (*Grouping*):
1. No mapa, temos quatro `1`s nas colunas das pontas (`00` e `10`), formando um retângulo vertical de 4 células adjacentes (podemos "enrolar" o mapa da esquerda para a direita, pois as extremidades são adjacentes).
2. Ao abranger todas as linhas de $A$ ($0$ e $1$), a variável $A$ é eliminada.
3. Olhando para as colunas, o único fator comum a essas quatro células é o facto de **$C = 0$** (ou seja, $C'$).

### Resultado Simplificado:
$$F(A, B, C) = C'$$
*(Um circuito que exigiria portas complexas reduz-se apenas a um inversor na entrada $C$!)*

---

## 4. Regras de Ouro para Agrupar no Mapa K

1. **Maximizar os grupos:** Os grupos devem ser o maior possível (tentar agrupar blocos de $8, 4, 2$ ou $1$ células). Quanto maior o grupo, mais variáveis são eliminadas e mais simples fica o termo.
2. **Potências de 2:** O número de células num grupo tem de ser obrigatoriamente uma potência de $2$ ($1, 2, 4, 8, 16$).
3. **Enrolar os extremos:** As extremidades do mapa (esquerda/direita e cima/baixo) ligam-se entre si como se fossem um cilindro ou toro. Podes fazer grupos cruzando as bordas.
4. **Sobreposição permitida:** Uma célula com `1` pode (e deve, se necessário) pertencer a vários grupos para garantir que formamos os maiores agrupamentos possíveis.
5. **Minimizar o número de grupos:** Usa o menor número de grupos possível para cobrir todos os `1`s.

# Karnaugh Maps for 3 Variables (Mapas de Karnaugh de 3 Variáveis)

Para funções lógicas com **três variáveis** (por exemplo, $A, B, C$), a Tabela da Verdade tem $2^3 = 8$ linhas. O Mapa de Karnaugh correspondente é uma grelha bidimensional com **8 células**, habitualmente organizada numa estrutura de $2 \times 4$ (2 linhas por 4 colunas).

---

## 1. Estrutura e Organização do Mapa ($2 \times 4$)

Para garantir a regra de adjacência (onde cada célula difere apenas em 1 bit), as colunas utilizam o **Código Gray** (`00, 01, 11, 10`), enquanto a linha utiliza o binário natural (`0` e `1`).

* **Variáveis:** $A$ (linhas: `0` para $A'$, `1` para $A$) e $BC$ (colunas: $B'C', B'C, BC, BC'$).

| $A \backslash BC$ | `00` ($B'C'$) | `01` ($B'C$) | `11` ($BC$) | `10` ($BC'$) |
| :---: | :---: | :---: | :---: | :---: |
| **`0` ($A'$)** | $m_0$ ($A'B'C'$) | $m_1$ ($A'B'C$) | $m_3$ ($A'BC$) | $m_2$ ($A'BC'$) |
| **`1` ($A$)** | $m_4$ ($AB'C'$) | $m_5$ ($AB'C$) | $m_7$ ($ABC$) | $m_6$ ($ABC'$) |

> **Atenção à ordem das colunas:** Repara que a sequência é `00`, `01`, `11`, `10` (e não `10`, `11`). Isto é crucial para que as colunas das extremidades (`00` e `10`) sejam consideradas adjacentes entre si ("enrolamento" do mapa).

---

## 2. Passo a Passo para Resolver com um Mapa de 3 Variáveis

1. **Preencher o Mapa:** Coloca `1` nas células cujos minterms correspondem às linhas da Tabela da Verdade onde a função é verdadeira ($F = 1$). Coloca `0` nas restantes (ou deixa em branco).
2. **Formar Grupos (Agrupamentos):** 
   * Agrupa os `1`s em blocos cujos tamanhos sejam potências de 2: **4 células** (quartetos) ou **2 células** (pares), ou até um `1` isolado se não tiver adjacências.
   * Cria o menor número de grupos possível, garantindo que cobres todos os `1`s. Lembra-te que podes cruzar as colunas das pontas (a coluna `00` liga-se à coluna `10`).
3. **Extrair a Expressão Simplificada:**
   * Para cada grupo, observa quais as variáveis que **não mudam de estado** (mantêm o valor $0$ ou $1$) entre as células do grupo.
   * As variáveis que mudam de valor são eliminadas. Escreve a soma de produtos final.

---

## 3. Exemplo Prático Completo

Considera a função booleana dada pela soma de minterms:
$$F(A, B, C) = \sum m(0, 1, 4, 5)$$

### Passo A: Preenchimento do Mapa K
* Colocamos `1` nas posições $m_0$ (`000`), $m_1$ (`001`), $m_4$ (`100`) e $m_5$ (`101`).

| $A \backslash BC$ | `00` ($B'C'$) | `01` ($B'C$) | `11` ($BC$) | `10` ($BC'$) |
| :---: | :---: | :---: | :---: | :---: |
| **`0` ($A'$)** | **1** ($m_0$) | **1** ($m_1$) | 0 ($m_3$) | 0 ($m_2$) |
| **`1` ($A$)** | **1** ($m_4$) | **1** ($m_5$) | 0 ($m_7$) | 0 ($m_6$) |

### Passo B: Agrupamento
* Os quatro `1`s formam um **bloco rectangular de 4 células** (um quadrado perfeito no lado esquerdo do mapa, abrangendo as colunas `00` e `01` para ambas as linhas $A=0$ e $A=1$).

### Passo C: Leitura do Resultado
* **Variável $A$:** Como o grupo ocupa tanto a linha $0$ ($A=0$) como a linha $1$ ($A=1$), a variável $A$ muda de estado e é **eliminada**.
* **Variável $B$:** Em ambas as colunas do grupo (`00` e `01`), o bit $B$ é sempre `0`. Logo, mantém-se como **$B'$**.
* **Variável $C$:** Na coluna `00`, $C=0$; na coluna `01`, $C=1$. Como $C$ muda de valor, é **eliminada**.

* **Expressão Simplificada Final:**
  $$F(A, B, C) = B'$$

  # Karnaugh Maps for 4 Variables (Mapas de Karnaugh de 4 Variáveis)

Para funções lógicas com **quatro variáveis** (por exemplo, $A, B, C, D$), a Tabela da Verdade tem $2^4 = 16$ linhas. O Mapa de Karnaugh correspondente é uma grelha de **16 células**, estruturada num formato de $4 \times 4$ (4 linhas e 4 colunas).

---

## 1. Estrutura e Organização do Mapa ($4 \times 4$)

Tanto as linhas ($AB$) como as colunas ($CD$) utilizam o **Código Gray** (`00, 01, 11, 10`) para garantir que células adjacentes diferem em apenas um único bit.

| $AB \backslash CD$ | `00` ($C'D'$) | `01` ($C'D$) | `11` ($CD$) | `10` ($CD'$)|
| :---: | :---: | :---: | :---: | :---: |
| **`00` ($A'B'$)** | $m_0$ | $m_1$ | $m_3$ | $m_2$ |
| **`01` ($A'B$)** | $m_4$ | $m_5$ | $m_7$ | $m_6$ |
| **`11` ($AB$)** | $m_{12}$ | $m_{13}$ | $m_{15}$ | $m_{14}$ |
| **`10` ($AB'$)** | $m_8$ | $m_9$ | $m_{11}$ | $m_{10}$ |

> **Nota de Atenção sobre a Ordem:** Repara que as linhas seguem a ordem `00, 01, 11, 10` (e o mesmo para as colunas). Isto significa que a primeira linha (`00`) é adjacente à última linha (`10`), e a primeira coluna (`00`) é adjacente à última coluna (`10`). O mapa comporta-se como um toro (uma superfície esférica onde os extremos se ligam).

---

## 2. Passo a Passo para Resolver com um Mapa de 4 Variáveis

1. **Preencher o Mapa:** Coloca `1` nas células correspondentes aos minterms onde a função é verdadeira ($F = 1$).
2. **Formar Grupos (Agrupamentos):**
   * Agrupa os `1`s em blocos de potências de 2: **16, 8, 4, 2 ou 1** células.
   * **Enrolamento Total:** Lembra-te que as extremidades esquerda e direita ligam-se, e as extremidades superior e inferior também se ligam. Podes formar grupos de 4 ou 8 células cruzando os quatro cantos do mapa ou as bordas opostas.
3. **Extrair a Expressão Simplificada:** Para cada grupo, identifica quais as variáveis que mantêm o mesmo valor (não mudam) e elimina as que mudam.

---

## 3. Exemplo Prático Completo

Considera a função dada pela soma de minterms:
$$F(A, B, C, D) = \sum m(0, 2, 5, 7, 8, 10, 13, 15)$$

### Passo A: Preenchimento do Mapa K
Colocamos `1` nas posições correspondentes aos minterms indicados:

| $AB \backslash CD$ | `00` | `01` | `11` | `10` |
| :---: | :---: | :---: | :---: | :---: |
| **`00`** | **1** ($m_0$) | 0 ($m_1$) | 0 ($m_3$) | **1** ($m_2$) |
| **`01`** | 0 ($m_4$) | **1** ($m_5$) | **1** ($m_7$) | 0 ($m_6$) |
| **`11`** | 0 ($m_{12}$)| 0 ($m_{13}$)| 0 ($m_{15}$)| 0 ($m_{14}$)|
| **`10`** | **1** ($m_8$) | 0 ($m_9$) | 0 ($m_{11}$)| **1** ($m_{10}$)|

*(Espere, vamos ajustar os minterms para formar um exemplo visualmente perfeito de cantos/bordas: $m_0, m_2, m_8, m_{10}$ formam exatamente os 4 cantos do mapa!)*

Se isolarmos os **cantos** ($m_0, m_2, m_8, m_{10}$):
* Linhas dos cantos: `00` e `10`. O $A$ muda (de $0$ para $1$), logo é eliminado; o $B$ é sempre `0` ($B'$).
* Colunas dos cantos: `00` e `10`. O $C$ muda, logo é eliminado; o $D$ é sempre `0

# Karnaugh Maps for 5 Variables (Mapas de Karnaugh de 5 Variáveis)

Para funções lógicas com **cinco variáveis** (por exemplo, $A, B, C, D, E$), a Tabela da Verdade tem $2^5 = 32$ linhas. Como uma grelha bidimensional normal se tornaria demasiado complexa, o método padrão consiste em utilizar **dois mapas de 4 variáveis (de 16 células cada)** colocados lado a lado ou sobrepostos.

---

## 1. Como funciona a estrutura de 5 Variáveis

* **Divisão:** O mapa de 32 células é dividido em duas metades (duas "fatias" ou planos de 16 células):
  * **Mapa 1:** Corresponde ao caso em que a 5.º variável é **`0`** (ex: $A'$).
  * **Mapa 2:** Corresponde ao caso em que a 5.º variável é **`1`** (ex: $A$).
* **Adjacência Tridimensional (3D):** Além das adjacências normais dentro de cada mapa de 16 células (linhas e colunas), **duas células que ocupam exatamente a mesma posição nos dois mapas são consideradas adjacentes** entre si.

---

## 2. Passo a Passo para Resolver com 5 Variáveis

1. **Dividir os Minterms:** 
   * Os minterms de $0$ a $15$ ($m_0$ a $m_{15}$) vão para o mapa onde $A = 0$.
   * Os minterms de $16$ a $31$ ($m_{16}$ a $m_{31}$) vão para o mapa onde $A = 1$.
2. **Preencher os dois Mapas:** Coloca `1` nas células correspondentes em cada um dos mapas ($A=0$ e $A=1$).
3. **Formar Grupos (2D e 3D):**
   * **Grupos intra-mapa:** Procura grupos normais de $1, 2, 4, 8$ ou $16$ células *dentro* do mesmo mapa.
   * **Grupos inter-mapa (sobrepostos):** Procura células com `1` na **mesma posição exata** em ambos os mapas ($A=0$ e $A=1$). Juntando as duas metades, consegues formar grupos 3D (por exemplo, um grupo de 4 células num mapa pode juntar-se ao grupo idêntico no outro mapa, duplicando o tamanho para um bloco de 8 células e eliminando a variável $A$).
4. **Extrair a Expressão:** As regras de eliminação mantêm-se: sempre que um grupo se estende por ambos os mapas, a variável que distingue os mapas ($A$) é eliminada.

---

## 3. Exemplo Conceptual de Agrupamento 3D

Se tiveres um `1` na posição $m_2$ ($AB'C'D'E' \rightarrow$ no mapa $A=0$) e outro `1` na posição $m_{18}$ ($AB'C'D'E \rightarrow$ no mapa $A=1$):
* Os dois `1`s estão exatamente na mesma célula ($B'C'D'$) em ambos os mapas.
* Ao agrupá-los, formas um par de células 3D.
* **Eliminação:** A variável $A$ muda ($0$ e $1$), logo é eliminada. As restantes variáveis que não mudam de estado formam o termo simplificado correspondente.

# Irrelevant Input Conditions (Don’t Cares / Condições Indiferentes)

As **condições indiferentes** (frequentemente chamadas de **Don't Cares** e representadas por $d$ ou $\times$) correspondem a combinações de entradas que **nunca ocorrem na prática** num determinado sistema, ou cujos valores de **saída não interessam** para o funcionamento correto do circuito.

---

## 1. Porque é que os "Don't Cares" são úteis?

Quando projetamos um circuito digital, saber que certas combinações de entrada nunca vão acontecer (ou que a saída tanto faz ser `0` ou `1`) dá-nos **liberdade de otimização**. 

Podemos tratar esses valores como `1` ou como `0` no Mapa de Karnaugh, escolhendo a opção que nos permitir **formar os maiores agrupamentos possíveis**, resultando em expressões booleanas ainda mais simples e com menos portas lógicas.

---

## 2. Regras para usar Don't Cares nos Mapas de Karnaugh

1. **Tratar como `1` quando ajuda:** Se um `d` estiver numa posição adjacente que ajude a formar um grupo maior (de 2, 4 ou 8 células) com os `1`s reais da função, assumimos o seu valor como **`1`**.
2. **Tratar como `0` quando não ajuda:** Se um `d` não trouxer nenhuma vantagem para criar grupos maiores, tratamo-lo como **`0`** (ignorando-o completamente).
3. **Nunca isolar Don't Cares:** Nunca crias um grupo constituído *apenas* por Don't Cares. Eles servem apenas para "esticar" os grupos de `1`s já existentes.

---

## 3. Notação Matemática

Nas funções booleanas, os Don't Cares são normalmente indicados pela letra $d$ (ou $\sum d$) somados aos minterms:
$$F(A, B, C, D) = \sum m(1, 3, 7) + d(9, 11, 15)$$
* Significa que a função vale `1` nos minterms 1, 3 e 7, e é indiferente (`d`) nos minterms 9, 11 e 15.

---

## 4. Exemplo Prático: Detetor de Dígitos BCD Inválidos

O código **BCD 8421** utiliza 4 bits para representar os algarismos decimais de `0` (`0000`) a `9` (`1001`). No entanto, com 4 bits conseguimos representar 16 valores (até `1111`). As combinações de `10` (`1010`) a `15` (`1111`) **nunca ocorrem** num número BCD válido.

Se quisermos detetar quando ocorre um erro (um valor inválido de BCD):
* As saídas para as combinações de `0` a `9` devem ser **`0`** (números válidos).
* As combinações de `10` a `15` são **Don't Cares (`d`)** para o projetista se o sistema garantir que nunca entram valores inválidos, ou podem ser tratadas consoante a especificação. Se forem usadas como `d`, permitem simplificar drasticamente a lógica do detetor de erros no Mapa K.
