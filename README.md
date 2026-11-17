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
| 0111 | 7 | 7 | 7 |
| 1000 | 8 | 10 | 8 |
| 1001 | 9 | 11 | 9 |
| 1010 | 10 | 12 | A |
| 1011 | 11 | 13 | B |
| 1100 | 12 | 14 | C |
| 1101 | 13 | 15 | D |
| 1110 | 14 | 16 | E |
| 1111 | 15 | 17 | F |
