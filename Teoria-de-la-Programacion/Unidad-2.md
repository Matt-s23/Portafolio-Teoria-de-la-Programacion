# 📘 Unidad 2

---

# 📚 Contenido de la Unidad

- [1. Estructuras Condicionales](#1-estructuras-condicionales)
  - [Tipos de estructuras condicionales](#-tipos-de-estructuras-condicionales)
  - [Condicional simple](#-condicional-simple-if)
  - [Condicional doble](#-condicional-doble-if---else)
  - [Condicional múltiple](#-condicional-múltiple-if---else-if)
  - [Estructura en diagrama de flujo](#-estructura-en-diagrama-de-flujo)

- [2. Estructuras Repetitivas](#2-estructuras-repetitivas)
  - [Tipos de estructuras repetitivas](#-tipos-de-estructuras-repetitivas)
  - [Ciclo while](#-ciclo-while)
  - [Ciclo do while](#-ciclo-do-while)
  - [Ciclo for](#-ciclo-for)

- [3. Ejercicio con estructura condicional y repetitiva](#3-ejercicio-con-estructura-condicional-y-repetitiva)
  - [Planteamiento del problema](#-planteamiento-del-problema)
  - [Análisis del problema](#-análisis-del-problema)
  - [Diseño del algoritmo](#-diseño-del-algoritmo-diagrama-de-flujo)
  - [Codificación](#-codificación-código-fuente)
  - [Validación](#-validación-prueba-de-escritorio)

- [4. Principales dificultades y reflexión crítica](#4-principales-dificultades-y-reflexión-crítica)

- [🔗 Navegación](#-navegación)

---

# 1. Estructuras Condicionales

Las estructuras condicionales permiten que un programa tome decisiones dependiendo de si una condición es verdadera o falsa. Estas estructuras son fundamentales dentro de la programación, ya que permiten controlar el flujo de ejecución de un algoritmo y adaptar el comportamiento del programa según determinadas situaciones.

---

## 🔹 Tipos de estructuras condicionales

### ✅ Condicional simple (`if`)

La estructura `if` ejecuta un bloque de instrucciones únicamente cuando la condición establecida es verdadera.

### 📌 Pseudocódigo

```txt
INICIO

  LEER edad

  SI edad >= 18 ENTONCES
      ESCRIBIR "Mayor de edad"
  FIN_SI

FIN
````

---

### ✅ Condicional doble (`if - else`)

La estructura `if - else` permite ejecutar una acción cuando la condición es verdadera y otra distinta cuando la condición es falsa.

### 📌 Pseudocódigo

```txt
INICIO

  LEER nota

  SI nota >= 6 ENTONCES
      ESCRIBIR "Aprobado"
  SINO
      ESCRIBIR "Reprobado"
  FIN_SI

FIN
```

---

### ✅ Condicional múltiple (`if - else if`)

Esta estructura se utiliza cuando existen varias condiciones posibles dentro de un mismo problema.

### 📌 Pseudocódigo

```txt
INICIO

  LEER promedio

  SI promedio >= 9 ENTONCES
      ESCRIBIR "Excelente"

  SINO SI promedio >= 7 ENTONCES
      ESCRIBIR "Bueno"

  SINO SI promedio >= 6 ENTONCES
      ESCRIBIR "Suficiente"

  SINO
      ESCRIBIR "Reprobado"

  FIN_SI

FIN
```

---

## 🔹 Estructura en diagrama de flujo

### Condicional simple

```txt
        ┌─────────────┐
        │  Condición  │
        └──────┬──────┘
               │
         ┌─────▼─────┐
         │ Verdadero │
         └───────────┘
```

---

### Condicional doble

```txt
          ┌─────────────┐
          │ Condición   │
          └──────┬──────┘
          Sí     │     No
      ┌────────┐ │ ┌────────┐
      │ Acción │ │ │ Acción │
      └────────┘ │ └────────┘
```

---

# 2. Estructuras Repetitivas

Las estructuras repetitivas permiten ejecutar un conjunto de instrucciones varias veces mientras se cumpla una condición determinada. Estas estructuras ayudan a automatizar procesos y evitar la repetición innecesaria de código.

---

## 🔹 Tipos de estructuras repetitivas

### ✅ Ciclo `while`

El ciclo `while` evalúa primero la condición y posteriormente ejecuta las instrucciones mientras dicha condición sea verdadera.

### 📌 Pseudocódigo

```txt
INICIO

  contador ← 1

  MIENTRAS contador <= 5 HACER

      ESCRIBIR contador

      contador ← contador + 1

  FIN_MIENTRAS

FIN
```

---

### ✅ Ciclo `do while`

La estructura `do while` ejecuta primero el bloque de instrucciones y luego evalúa la condición, garantizando al menos una ejecución.

### 📌 Pseudocódigo

```txt
INICIO

  HACER

      ESCRIBIR "Ingrese un número positivo"
      LEER n

  MIENTRAS n <= 0

FIN
```

---

### ✅ Ciclo `for`

La estructura `for` se utiliza cuando se conoce previamente la cantidad de veces que se repetirá una instrucción.

### 📌 Pseudocódigo

```txt
INICIO

  PARA i ← 1 HASTA 10 HACER

      ESCRIBIR i

  FIN_PARA

FIN
```

---

## 🔹 Estructura en diagrama de flujo

### Ciclo while

```txt
      ┌─────────────┐
      │ Condición   │
      └──────┬──────┘
          Sí │
             ▼
      ┌─────────────┐
      │ Instrucción │
      └──────┬──────┘
             │
             └───────────↺
```

---

### Ciclo for

```txt
      ┌─────────────┐
      │ Inicializar │
      └──────┬──────┘
             ▼
      ┌─────────────┐
      │ Condición   │
      └──────┬──────┘
          Sí │
             ▼
      ┌─────────────┐
      │ Instrucción │
      └──────┬──────┘
             ▼
      ┌─────────────┐
      │ Incremento  │
      └──────┬──────┘
             └────────↺
```

---

# 3. Ejercicio con estructura condicional y repetitiva

## 🔹 Planteamiento del problema

Desarrollar un programa que solicite cinco notas de un estudiante, calcule el promedio general y determine si el estudiante aprueba o reprueba la asignatura.

---

## 🔹 Análisis del problema

### 📥 Entradas

* Cinco calificaciones.

### ⚙ Procesos

* Leer las notas.
* Sumar las calificaciones.
* Calcular el promedio.
* Evaluar la condición de aprobación.

### 📤 Salidas

* Promedio final.
* Estado del estudiante.

---

## 🔹 Diseño del algoritmo (diagrama de flujo)

```txt
        ┌────────────┐
        │ Inicio     │
        └─────┬──────┘
              ▼
      ┌───────────────┐
      │ Leer notas    │
      └─────┬─────────┘
            ▼
      ┌───────────────┐
      │ Calcular prom │
      └─────┬─────────┘
            ▼
      ┌───────────────┐
      │ ¿Prom >= 6?   │
      └─────┬─────────┘
         Sí │ No
            ▼
   ┌─────────────┐
   │ Aprobado    │
   └─────────────┘
```

---

## 🔹 Codificación (código fuente)

```c
#include <stdio.h>

int main() {

    int i;
    float nota, suma = 0, promedio;

    for(i = 1; i <= 5; i++) {

        printf("Ingrese la nota %d: ", i);
        scanf("%f", &nota);

        suma = suma + nota;
    }

    promedio = suma / 5;

    printf("\nPromedio: %.2f\n", promedio);

    if(promedio >= 6) {

        printf("Estado: APROBADO");

    } else {

        printf("Estado: REPROBADO");
    }

    return 0;
}
```

---

## 🔹 Validación (prueba de escritorio)

### Caso 1

Notas:

* 8
* 9
* 7
* 10
* 8

Resultado:

```txt
Promedio: 8.40
Estado: APROBADO
```

---

### Caso 2

Notas:

* 4
* 5
* 3
* 6
* 4

Resultado:

```txt
Promedio: 4.40
Estado: REPROBADO
```

---

# 4. Principales dificultades y reflexión crítica

## Reflexión

El desarrollo de esta unidad me permitió comprender que la programación no consiste únicamente en escribir código, sino en aprender a resolver problemas mediante un razonamiento lógico y estructurado. Durante el estudio de las estructuras condicionales y repetitivas entendí cómo un programa puede tomar decisiones y repetir procesos automáticamente dependiendo de ciertas condiciones establecidas.

Una de las mayores dificultades que tuve fue comprender el funcionamiento de los ciclos `for` y `while`, ya que al inicio resultaban confusos debido a la manera en que controlan las repeticiones dentro de un programa. En algunos ejercicios se me dificultaba identificar cuándo debía utilizar cada estructura y cómo funcionaban las variables contadoras y acumuladoras dentro del ciclo. También tuve problemas al elaborar diagramas de flujo relacionados con estructuras repetitivas, porque era necesario organizar correctamente la secuencia lógica del proceso para evitar errores.

Sin embargo, mediante la práctica constante, las pruebas de escritorio y la corrección de errores en los programas, logré entender mejor el comportamiento de las estructuras repetitivas y su importancia dentro de la programación. Poco a poco fui desarrollando una mejor capacidad de análisis para identificar errores lógicos y mejorar la organización de los algoritmos.

---

## Conclusión

En conclusión, esta unidad fortaleció significativamente mi comprensión sobre las estructuras condicionales y repetitivas, las cuales representan una base fundamental en el desarrollo de programas. Aprendí que las estructuras condicionales permiten que un sistema tome decisiones dependiendo de determinadas situaciones, mientras que las estructuras repetitivas ayudan a automatizar tareas que deben ejecutarse varias veces.

Además, comprendí la importancia de realizar pruebas de escritorio antes de ejecutar un programa, ya que este proceso facilita la detección de errores y mejora la lógica del algoritmo. El uso de pseudocódigo, diagramas de flujo y lenguaje C permitió relacionar la teoría con la práctica, fortaleciendo mi pensamiento lógico-computacional y mi capacidad para resolver problemas mediante programación.

---

# 🔗 Navegación

[⬅ Volver a la Portada](Portada.md)

| Navegación                 |
| -------------------------- |
| [📘 Unidad 1](Unidad-1.md) |
| [📘 Unidad 3](Unidad-3.md) |

---

```
```
