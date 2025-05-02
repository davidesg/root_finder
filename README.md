# RootFinder - Polynomial Roots Calculator

**Authors**: David E. Guerrero (UCM)
**License**: BSD-3-Clause

Tool for calculating roots and factors of normalized polynomials in the form:

P(B) = 1 - c[1]B - c[2]B² - ... - c[N]Bᴺ


---

## 🛠️ Installation

### Requirements:
- C Compiler (gcc/clang)
- CMake (version 3.10+)
- Math library (`libm`)

```bash
git clone https://github.com/davidesg/root-finder.git
cd root-finder
mkdir build && cd build
cmake ..
make

Basic execution:

./root

Interactive workflow:

1.    Enter the polynomial order (1-12)

2.    Input coefficients one by one

3.    View results in console and in resultados.txt

Example
Input:

* RAICES Y FACTORIZACION DE POLINOMIOS NORMALIZADOS *
* (C) 2025 DAVID E. GUERRERO  (UCM)                 *
* P(B)=1-c[1]B - c[2]B^2 - ... - c [N]B^N           *

Ingrese el orden del polinomio [N]: 3
c[1] = 2.5
c[2] = -1.3
c[3] = 0.4


Console output:

------------
    RAIZ #        REAL         IMAG       MOD
      1          0.51234      0.00000      0.51234
      2          1.24321      0.75231      1.45218
      3          1.24321     -0.75231      1.45218

FACTORES REALES (1 - a[1] B): 1
    ** FACTOR 1: a[1] = 1.95122

FACTORES COMPLEJOS (1 - a[1] B - a[2] B^2): 1
    ** FACTOR 1: a[1] = 0.82456   a[2] = -0.43210   d = 0.66   freq = 0.12   per = 8.33
------------

Notes

 1.   Polynomials are automatically normalized

 2.   5 decimal precision in results

 3.   Supports polynomials up to order 12

