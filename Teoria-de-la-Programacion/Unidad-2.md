---
[⬅ Volver a la Portada](Portada.md)

--- 

# UNIDAD 2

--- 

# ESTRUCTURAS CONDICIONALES Y REPETITIVAS

---

# 1. Estructuras Condicionales

Las estructuras condicionales permiten controlar el flujo de ejecución de un programa mediante la evaluación de condiciones lógicas. Gracias a ellas, un algoritmo puede tomar decisiones y ejecutar diferentes acciones dependiendo de si una condición es verdadera o falsa.

Estas estructuras son fundamentales en la programación porque permiten adaptar el comportamiento de un sistema a distintas situaciones. Sin ellas, todos los programas ejecutarían siempre las mismas instrucciones sin importar los datos ingresados por el usuario.

## Características de las Estructuras Condicionales

- Permiten la toma de decisiones dentro de un programa.
- Evalúan expresiones lógicas.
- Controlan el flujo de ejecución.
- Facilitan la resolución de problemas complejos.
- Mejoran la flexibilidad y eficiencia de los algoritmos.

---

## 1.1 Condicional Simple (if)

La estructura condicional simple se utiliza cuando una acción debe ejecutarse únicamente si una condición determinada es verdadera. Si la condición resulta falsa, el programa continúa normalmente con las instrucciones siguientes.

### Sintaxis General

```txt
SI condición ENTONCES

    instrucciones

FIN_SI
```

### Pseudocódigo

```txt
INICIO

    LEER edad

    SI edad >= 18 ENTONCES
        ESCRIBIR "Mayor de edad"
    FIN_SI

FIN
```

### Diagrama de Flujo


<img width="559" height="774" alt="image" src="https://github.com/user-attachments/assets/9adef7ee-15b8-406d-b865-d3821d61c62d" />

---

## 1.2 Condicional Doble (if - else)

La estructura condicional doble permite ejecutar una acción cuando la condición es verdadera y otra diferente cuando la condición es falsa.

Este tipo de estructura resulta útil cuando solamente existen dos posibles resultados dentro de un problema.

### Sintaxis General

```txt
SI condición ENTONCES

    instrucciones

SINO

    instrucciones

FIN_SI
```

### Pseudocódigo

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

### Diagrama de Flujo

<img width="697" height="802" alt="image" src="https://github.com/user-attachments/assets/90dbe08b-b973-46ea-b6af-6af3bf391333" />

---

## 1.3 Condicional Múltiple (if - else if)

La estructura condicional múltiple permite evaluar varias condiciones dentro de un mismo bloque de decisión.

Su principal ventaja es que evita el uso excesivo de múltiples estructuras independientes, facilitando la organización y comprensión del algoritmo.

### Sintaxis General

```txt
SI condición1 ENTONCES

    instrucciones

SINO SI condición2 ENTONCES

    instrucciones

SINO

    instrucciones

FIN_SI
```

### Pseudocódigo

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

### Diagrama de Flujo

<img width="604" height="778" alt="image" src="https://github.com/user-attachments/assets/51f7d387-2d49-4d1a-b490-d6e27898c632" />

---

# 2. Estructuras Repetitivas

Las estructuras repetitivas, también conocidas como bucles o ciclos, permiten ejecutar un conjunto de instrucciones varias veces sin necesidad de escribir el mismo código repetidamente.

Su utilización optimiza el desarrollo de programas, mejora la organización del código y facilita la automatización de tareas repetitivas.

## Características de las Estructuras Repetitivas

- Reducen la cantidad de código.
- Facilitan el mantenimiento de programas.
- Automatizan procesos repetitivos.
- Mejoran la eficiencia de los algoritmos.
- Permiten trabajar con grandes volúmenes de información.

---

## 2.1 Ciclo while

El ciclo `while` evalúa primero una condición lógica y ejecuta las instrucciones únicamente mientras dicha condición sea verdadera.

Su principal característica es que puede ejecutarse cero veces si la condición inicial resulta falsa.

### Sintaxis General

```txt
MIENTRAS condición HACER

    instrucciones

FIN_MIENTRAS
```

### Pseudocódigo

```txt
INICIO

    contador ← 1

    MIENTRAS contador <= 5 HACER

        ESCRIBIR contador

        contador ← contador + 1

    FIN_MIENTRAS

FIN
```

### Diagrama de Flujo

<img width="506" height="849" alt="image" src="https://github.com/user-attachments/assets/03026e19-a6a7-4295-aee3-85754532aed9" />

---

## 2.2 Ciclo do while

La estructura `do while` ejecuta primero el bloque de instrucciones y posteriormente evalúa la condición.

Por esta razón garantiza al menos una ejecución.

### Sintaxis General

```txt
HACER

    instrucciones

MIENTRAS condición
```

### Pseudocódigo

```txt
INICIO

    HACER

        ESCRIBIR "Ingrese un número positivo"
        LEER n

    MIENTRAS n <= 0

FIN
```

### Diagrama de Flujo

<img width="616" height="824" alt="image" src="https://github.com/user-attachments/assets/a04d6744-9c25-4494-9842-5be6f00959ca" />

---

## 2.3 Ciclo for

El ciclo `for` se utiliza cuando se conoce previamente el número de repeticiones que debe realizar el programa.

Es una de las estructuras repetitivas más utilizadas debido a que integra en una sola línea la inicialización, condición e incremento.

### Sintaxis General

```txt
PARA variable ← inicio HASTA fin HACER

    instrucciones

FIN_PARA
```

### Pseudocódigo

```txt
INICIO

    PARA i ← 1 HASTA 10 HACER

        ESCRIBIR i

    FIN_PARA

FIN
```

### Diagrama de Flujo

<img width="397" height="782" alt="image" src="https://github.com/user-attachments/assets/28a419cc-706c-4412-a0cd-d0741b587a45" />

---

# 3. Ejercicio Integrador

## 3.1 Planteamiento del Problema

Desarrollar un programa que solicite cinco notas de un estudiante, calcule el promedio general y determine si el estudiante aprueba o reprueba la asignatura.

---

## 3.2 Análisis del Problema

<img width="1727" height="159" alt="image" src="https://github.com/user-attachments/assets/6264aa0a-9e4b-4013-b212-2bd467d29ea4" />


---

## 3.3 Diseño del Algoritmo

### Pseudocódigo

```txt
INICIO

    suma ← 0

    PARA i ← 1 HASTA 5 HACER

        LEER nota

        suma ← suma + nota

    FIN_PARA

    promedio ← suma / 5

    SI promedio >= 6 ENTONCES

        ESCRIBIR "APROBADO"

    SINO

        ESCRIBIR "REPROBADO"

    FIN_SI

FIN
```

---

## 3.4 Diagrama de Flujo

<img width="299" height="830" alt="image" src="https://github.com/user-attachments/assets/45928547-676b-45ed-8273-ca0814af8a88" />

---

## 3.5 Codificación

```c
#include <stdio.h>

int main() {

    int i;
    float nota, suma = 0, promedio;

    for(i = 1; i <= 5; i++) {

        printf("Ingrese la nota %d: ", i);
        scanf("%f", &nota);

        suma += nota;
    }

    promedio = suma / 5;

    printf("\nPromedio final: %.2f\n", promedio);

    if(promedio >= 6) {

        printf("Estado: APROBADO\n");

    } else {

        printf("Estado: REPROBADO\n");
    }

    return 0;
}
```

---

## 3.6 Validación

### Caso 1

**Datos de Entrada**

- 8
- 9
- 7
- 10
- 8

**Resultado Esperado**

<img width="1196" height="739" alt="image" src="https://github.com/user-attachments/assets/768a8f18-99cd-4541-90c4-f170e6e7ea11" />

4. Principales Dificultades y Reflexión Crítica

## Reflexión

El desarrollo de esta unidad me permitió comprender que la programación no consiste únicamente en escribir código, sino en aprender a resolver problemas mediante un razonamiento lógico y estructurado. Durante el estudio de las estructuras condicionales y repetitivas entendí cómo un programa puede tomar decisiones y repetir procesos automáticamente dependiendo de ciertas condiciones establecidas.

Una de las mayores dificultades que tuve fue comprender el funcionamiento de los ciclos `for` y `while`, ya que al inicio resultaban confusos debido a la manera en que controlan las repeticiones dentro de un programa. En algunos ejercicios se me dificultaba identificar cuándo debía utilizar cada estructura y cómo funcionaban las variables contadoras y acumuladoras dentro del ciclo. También tuve problemas al elaborar diagramas de flujo relacionados con estructuras repetitivas, porque era necesario organizar correctamente la secuencia lógica del proceso para evitar errores.

Sin embargo, mediante la práctica constante, las pruebas de escritorio y la corrección de errores en los programas, logré entender mejor el comportamiento de las estructuras repetitivas y su importancia dentro de la programación. Poco a poco fui desarrollando una mejor capacidad de análisis para identificar errores lógicos y mejorar la organización de los algoritmos.

---

# 5. Conclusión

En conclusión, esta unidad fortaleció significativamente mi comprensión sobre las estructuras condicionales y repetitivas, las cuales representan una base fundamental en el desarrollo de programas. Aprendí que las estructuras condicionales permiten que un sistema tome decisiones dependiendo de determinadas situaciones, mientras que las estructuras repetitivas ayudan a automatizar tareas que deben ejecutarse varias veces.

Además, comprendí la importancia de realizar pruebas de escritorio antes de ejecutar un programa, ya que este proceso facilita la detección de errores y mejora la lógica del algoritmo. El uso de pseudocódigo, diagramas de flujo y lenguaje C permitió relacionar la teoría con la práctica, fortaleciendo mi pensamiento lógico-computacional y mi capacidad para resolver problemas mediante programación.

---

# 6. Declaración de Uso de Inteligencia Artificial

Durante la elaboración de este trabajo utilicé herramientas de inteligencia artificial como apoyo para mejorar la redacción, organizar algunas secciones y aclarar conceptos relacionados con los temas estudiados. No obstante, la comprensión de los contenidos, el desarrollo de las actividades y las conclusiones presentadas son resultado de mi propio proceso de aprendizaje y revisión.

# 7. Navegación

[Volver a la Portada](Portada.md)

| Documento |
|-----------|
| [Unidad 1](Unidad-1.md) |
| [Unidad 3](Unidad-3.md) |

---
