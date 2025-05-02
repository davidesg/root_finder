# RootFinder - Calculadora de Raíces Polinomiales

**Autores**: David E. Guerrero (UCM)
**Licencia**: BSD-3-Clause

Herramienta para calcular raíces y factores de polinomios normalizados de la forma:

P(B) = 1 - c[1]B - c[2]B² - ... - c[N]Bᴺ


---

## 🛠️ Instalación

### Requisitos:
- Compilador C (gcc/clang)
- CMake (versión 3.10+)
- Biblioteca matemática (`libm`)

```bash
git clone https://github.com/warriord/root-finder.git
cd root-finder
mkdir build && cd build
cmake ..
make

Ejecución básica:

./root

Flujo interactivo:

    Ingresar el orden del polinomio (1-12)

    Introducir coeficientes uno por uno

    Ver resultados en consola y en resultados.txt

Ejemplo Completo
Entrada:

* RAICES Y FACTORIZACION DE POLINOMIOS NORMALIZADOS *
* (C) 2025 DAVID E. GUERRERO  (UCM)                 *
* P(B)=1-c[1]B - c[2]B^2 - ... - c [N]B^N           *

Ingrese el orden del polinomio [N]: 3
c[1] = 2.5
c[2] = -1.3
c[3] = 0.4


Salida en consola:

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

