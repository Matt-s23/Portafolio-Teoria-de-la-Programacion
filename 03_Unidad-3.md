[⬅ Volver a la Portada](00_Portada.md)

---

# UNIDAD 3

# Programación Modular y Estructuras de Datos Estáticas

---

## Índice

1. [Programación Modular](#1-programación-modular)
   - 1.1 [Concepto y Ventajas](#11-concepto-y-ventajas)
   - 1.2 [Paso de Parámetros por Valor](#12-paso-de-parámetros-por-valor)
   - 1.3 [Paso de Parámetros por Referencia](#13-paso-de-parámetros-por-referencia)
2. [Arreglos (Estructuras de Datos Estáticas)](#2-arreglos-estructuras-de-datos-estáticas)
   - 2.1 [Concepto General](#21-concepto-general)
   - 2.2 [Arreglo Unidimensional](#22-arreglo-unidimensional)
   - 2.3 [Arreglo Bidimensional](#23-arreglo-bidimensional)
   - 2.4 [Arreglo Multidimensional](#24-arreglo-multidimensional)
3. [Ejercicio Integrador](#3-ejercicio-integrador)
4. [Principales Dificultades Encontradas](#4-principales-dificultades-encontradas)
5. [Reflexión](#5-reflexión)

---

## 1. Programación Modular

<p align="center">
 <img width="530" height="260" alt="image" src="https://github.com/user-attachments/assets/365e6da2-cabb-479f-94d0-418c7004ae66" />
</p>

<div style="text-align: justify;">

### 1.1 Concepto y Ventajas

Cuando un programa crece en tamaño, mantener todo el código dentro de una sola función `main()` se vuelve poco práctico: cualquier cambio pequeño obliga a revisar un bloque enorme de instrucciones. La programación modular resuelve esto dividiendo el programa en piezas independientes llamadas **funciones** o **módulos**, cada una encargada de una tarea concreta (leer datos, calcular un valor, mostrar un resultado, etc.). El programa principal se limita entonces a coordinar el orden en que se llaman estas funciones.

Esta forma de organizar el código trae varias ventajas prácticas:

- Facilita localizar y corregir errores, ya que cada función tiene una responsabilidad delimitada.
- Permite reutilizar una misma función en distintas partes del programa o incluso en otros proyectos.
- Hace que el código sea más legible, porque cada función puede analizarse por separado.
- Simplifica el trabajo en equipo, al poder repartir funciones distintas entre varios programadores.

```text
                main()
           /       |       \
    Función A  Función B  Función C
           \       |       /
             Resultado final
```

---

### 1.2 Paso de Parámetros por Valor

<p align="center">
<img width="320" height="240" alt="image" src="https://github.com/user-attachments/assets/1e896dec-469e-4a1e-b6e9-21d0d69b25c6" />
</p>

En el paso por valor, la función recibe **una copia** del dato original. Cualquier modificación que se haga dentro de la función afecta solo a esa copia; la variable original, en el programa que hizo el llamado, permanece sin cambios una vez que la función termina.

#### Pseudocódigo

```txt
FUNCION aplicarDescuento(precio)

    precio ← precio - (precio * 0.10)
    ESCRIBIR "Precio con descuento (dentro de la función): ", precio

FIN_FUNCION

INICIO

    precioOriginal ← 100

    aplicarDescuento(precioOriginal)

    ESCRIBIR "Precio original (fuera de la función): ", precioOriginal

FIN
```

#### Ejemplo en C

```c
#include <stdio.h>

void aplicarDescuento(float precio) {
    precio = precio - (precio * 0.10);
    printf("Precio con descuento (dentro de la funcion): %.2f\n", precio);
}

int main() {
    float precioOriginal = 100;

    aplicarDescuento(precioOriginal);

    printf("Precio original (fuera de la funcion): %.2f\n", precioOriginal);

    return 0;
}
```

Al ejecutar este programa, dentro de `aplicarDescuento` el precio se muestra ya rebajado, pero en `main()` la variable `precioOriginal` conserva su valor de 100, porque la función trabajó únicamente con una copia.

---

### 1.3 Paso de Parámetros por Referencia

En el paso por referencia, en lugar de enviar una copia del dato, se envía la **dirección de memoria** de la variable mediante un puntero. Esto permite que la función acceda directamente a la variable original y la modifique, de modo que los cambios sí se conservan al terminar la función.

#### Pseudocódigo

```txt
FUNCION aumentarStock(REF cantidad, unidades)

    cantidad ← cantidad + unidades

FIN_FUNCION

INICIO

    stockActual ← 50

    aumentarStock(REF stockActual, 20)

    ESCRIBIR "Stock actualizado: ", stockActual

FIN
```

#### Ejemplo en C

```c
#include <stdio.h>

void aumentarStock(int *cantidad, int unidades) {
    *cantidad = *cantidad + unidades;
}

int main() {
    int stockActual = 50;

    aumentarStock(&stockActual, 20);

    printf("Stock actualizado: %d\n", stockActual);

    return 0;
}
```

Aquí, `stockActual` sí queda modificado después de llamar a la función, porque `aumentarStock` no trabajó con una copia sino con la dirección de memoria real de la variable, a través del puntero `cantidad`.

> **Nota:** el paso por referencia resulta especialmente útil cuando se necesita que una función modifique varias variables a la vez, o cuando se trabaja con estructuras de datos grandes, ya que evita el costo de copiar toda la información en memoria.

</div>

---

## 2. Arreglos (Estructuras de Datos Estáticas)

<p align="center">
<img width="408" height="207" alt="image" src="https://github.com/user-attachments/assets/49cd7499-0879-4ae3-bd87-ce862a6b2d58" />
</p>

<div style="text-align: justify;">

### 2.1 Concepto General

Un arreglo es una estructura que permite almacenar varios valores del mismo tipo bajo un único nombre de variable, ocupando posiciones consecutivas en memoria. Cada valor se identifica mediante un índice, que en lenguaje C siempre comienza en 0. Su principal ventaja frente a declarar variables sueltas es que permite recorrer y procesar grandes cantidades de datos mediante ciclos, en lugar de escribir una instrucción por cada dato.

---

### 2.2 Arreglo Unidimensional

El arreglo unidimensional, o vector, organiza los datos en una sola fila, accesible mediante un único índice. Es útil para representar listas simples, como una serie de mediciones tomadas a lo largo de varios días.

```text
Índice   0    1    2    3    4    5    6
        ┌───┬───┬───┬───┬───┬───┬───┐
        │22 │24 │19 │21 │26 │23 │20 │
        └───┴───┴───┴───┴───┴───┴───┘
```

#### Ejemplo en C

```c
float temperaturas[7] = {22, 24, 19, 21, 26, 23, 20};
```

Este arreglo podría representar las temperaturas registradas durante los siete días de una semana, donde `temperaturas[0]` corresponde al lunes y `temperaturas[6]` al domingo.

---

### 2.3 Arreglo Bidimensional

<p align="center">
<img width="797" height="385" alt="image" src="https://github.com/user-attachments/assets/614350f3-8f74-4dd5-9083-2f8113519e10" />
</p>

El arreglo bidimensional organiza la información en filas y columnas, como una tabla. Resulta natural para representar datos que tienen dos dimensiones, por ejemplo, la distribución de asientos en un autobús o un cine.

```text
          Columna
          0    1    2    3
Fila 0   [L]  [L]  [O]  [L]
Fila 1   [O]  [L]  [L]  [L]
Fila 2   [L]  [O]  [L]  [O]
```
*(L = asiento libre, O = asiento ocupado)*

#### Ejemplo en C

```c
int asientos[3][4] = {
    {1, 1, 0, 1},
    {0, 1, 1, 1},
    {1, 0, 1, 0}
};
```

Aquí `asientos[fila][columna]` indica si un asiento específico está libre (1) u ocupado (0), y recorrer la matriz con dos ciclos anidados permite, por ejemplo, contar cuántos asientos libres quedan en total.

---

### 2.4 Arreglo Multidimensional

<p align="center">
<img width="618" height="420" alt="image" src="https://github.com/user-attachments/assets/d13b7647-0a56-4f48-8804-30da5c3b7387" />
</p>

Cuando la información requiere más de dos dimensiones, se utilizan arreglos multidimensionales. Son comunes en aplicaciones como el procesamiento de imágenes a color, videojuegos o el control de inventario distribuido en varias bodegas y estantes.

```text
inventario[bodega][estante][producto]
```

#### Ejemplo en C

```c
int inventario[2][3][4];
// 2 bodegas, cada una con 3 estantes, cada estante con 4 tipos de producto
```

En este ejemplo, `inventario[0][2][1]` representaría la cantidad de un producto específico ubicado en la bodega 1, estante 3, en la segunda posición de producto. Este tipo de arreglo permite modelar información con múltiples niveles de clasificación dentro de una sola estructura.

</div>

---

## 3. Ejercicio Integrador

<div style="text-align: justify;">

### 3.1 Planteamiento del Problema

Se requiere un programa que registre las temperaturas de los 7 días de una semana en un arreglo, calcule mediante una función el promedio semanal y determine, a través de otra función, si la semana se clasifica como "calurosa" (promedio mayor a 25 grados) o "templada" (promedio de 25 grados o menos).

### 3.2 Análisis del Problema

Se necesita un arreglo de 7 posiciones de tipo flotante para almacenar las temperaturas diarias. Una función se encargará de leer y llenar el arreglo; en C, los arreglos se pasan automáticamente por referencia, por lo que los valores ingresados quedan disponibles para el resto del programa sin necesidad de retornarlos explícitamente. Una segunda función calculará el promedio recorriendo el arreglo, y una tercera función usará ese promedio para clasificar la semana.

### 3.3 Diseño del Algoritmo

#### Pseudocódigo

```txt
FUNCION leerTemperaturas(REF temperaturas[])

    PARA i ← 0 HASTA 6 HACER
        LEER temperaturas[i]
    FIN_PARA

FIN_FUNCION

FUNCION calcularPromedio(temperaturas[])

    suma ← 0

    PARA i ← 0 HASTA 6 HACER
        suma ← suma + temperaturas[i]
    FIN_PARA

    RETORNAR suma / 7

FIN_FUNCION

INICIO

    DECLARAR temperaturas[7]

    leerTemperaturas(REF temperaturas)

    promedio ← calcularPromedio(temperaturas)

    SI promedio > 25 ENTONCES
        ESCRIBIR "Semana calurosa"
    SINO
        ESCRIBIR "Semana templada"
    FIN_SI

FIN
```

### 3.4 Diagrama de Flujo

<p align="center">
<img width="808" height="550" alt="image" src="https://github.com/user-attachments/assets/9f1434c7-72d9-4963-b7ef-884093f7c048" />
</p>


### 3.5 Codificación

```c
#include <stdio.h>

void leerTemperaturas(float temperaturas[]) {
    int i;
    for (i = 0; i < 7; i++) {
        printf("Ingrese la temperatura del dia %d: ", i + 1);
        scanf("%f", &temperaturas[i]);
    }
}

float calcularPromedio(float temperaturas[]) {
    float suma = 0;
    int i;
    for (i = 0; i < 7; i++) {
        suma += temperaturas[i];
    }
    return suma / 7;
}

int main() {
    float temperaturas[7];
    float promedio;

    leerTemperaturas(temperaturas);
    promedio = calcularPromedio(temperaturas);

    printf("\nPromedio semanal: %.2f\n", promedio);

    if (promedio > 25) {
        printf("Clasificacion: Semana calurosa\n");
    } else {
        printf("Clasificacion: Semana templada\n");
    }

    return 0;
}
```

### 3.6 Validación

#### Caso 1

**Datos de Entrada**

- 22, 24, 19, 21, 26, 23, 20

**Resultado Esperado**

Promedio semanal: 22.14 — Clasificación: Semana templada

**Compilación y ejecución**

[PEGA_AQUÍ_TU_IMAGEN_DE_COMPILACIÓN_Y_EJECUCIÓN]

</div>

---

## 4. Principales Dificultades Encontradas

<div style="text-align: justify;">

Durante el desarrollo de esta unidad se presentaron varias dificultades relacionadas con la programación modular y el manejo de arreglos:

- Al inicio me costó identificar cuándo era realmente necesario crear una función independiente y cuándo era más práctico dejar el código dentro de `main()`, ya que en ejercicios pequeños ambas opciones parecían funcionar igual de bien.
- Diferenciar el paso de parámetros por valor y por referencia no fue inmediato: en varias pruebas olvidé colocar el operador `&` al llamar a la función o el asterisco `*` al declarar el parámetro, lo que generaba errores de compilación difíciles de interpretar al principio.
- Comprender el funcionamiento de los punteros en el paso por referencia me tomó más tiempo que el resto de la unidad, especialmente entender la diferencia entre modificar la dirección de memoria y modificar el valor almacenado en esa dirección.
- Al trabajar con arreglos bidimensionales, tuve confusión inicial entre el índice de fila y el de columna al recorrer la matriz con ciclos anidados, lo que provocaba que el programa mostrara datos en una posición distinta a la esperada.
- Visualizar el funcionamiento de un arreglo multidimensional fue lo más abstracto de la unidad, ya que a diferencia del vector o la matriz, no es tan sencillo representarlo gráficamente en papel.

</div>

---

## 5. Reflexión

<div style="text-align: justify;">

Esta unidad me permitió entender que la programación modular no es solo una buena práctica, sino una necesidad real conforme un programa crece: dividir el problema de las temperaturas semanales en tres funciones separadas (leer, calcular promedio y clasificar) hizo que cada parte del código fuera mucho más fácil de revisar y corregir que si todo estuviera junto dentro de `main()`.

El concepto que más trabajo me costó asimilar fue el paso de parámetros por referencia. Al principio memoricé la sintaxis de los punteros sin entender del todo por qué era necesaria, pero al comparar el ejemplo de paso por valor (donde la variable original no cambiaba) con el de paso por referencia (donde sí cambiaba), pude notar la diferencia de forma más clara. Esto también me ayudó a entender por qué en C los arreglos se comportan como si siempre se pasaran por referencia: al modificar el arreglo dentro de una función, el cambio se refleja en todo el programa sin necesidad de retornarlo explícitamente.

Trabajar con arreglos unidimensionales, bidimensionales y multidimensionales me hizo ver cómo un mismo concepto —guardar varios datos bajo un solo nombre— se adapta a distintos niveles de complejidad según el problema: una lista simple de temperaturas, una tabla de asientos, o un inventario clasificado por bodega y estante. Considero que esta unidad sienta una base importante para asignaturas futuras donde estas estructuras de datos, junto con la organización modular del código, serán herramientas constantes.

</div>

---

## 🔗 Navegación

[⬅ Volver a la Portada](00_Portada.md)

| Navegación |
|---|
| [📘 Unidad 1](01_Unidad-1.md) |
| [📘 Unidad 2](02_Unidad-2.md) |
| [📝 Conclusiones Generales](04_Conclusiones-Generales.md) |
| [📚 Bibliografía](05_Bibliografia.md) |
| [🤖 Declaración de uso de la IA](06_Declaración-de-uso-de-la-IA.md) |

---
