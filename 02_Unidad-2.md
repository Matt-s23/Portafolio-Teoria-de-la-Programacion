⬅ Volver a la Portada](00_Portada.md)
 
---
 
# UNIDAD 2
 
---
 
# ESTRUCTURAS CONDICIONALES Y REPETITIVAS
 
<p align="center">
  <img src="https://github.com/user-attachments/assets/b16ac9bf-3422-461a-be40-4987968c570f" alt="image" width="304">
</p>
---
 
## Índice
 
1. [Estructuras Condicionales](#1-estructuras-condicionales)
   - 1.1 [Condicional Simple (if)](#11-condicional-simple-if)
   - 1.2 [Condicional Doble (if - else)](#12-condicional-doble-if---else)
   - 1.3 [Condicional Múltiple (if - else if)](#13-condicional-múltiple-if---else-if)
2. [Estructuras Repetitivas](#2-estructuras-repetitivas)
   - 2.1 [Ciclo while](#21-ciclo-while)
   - 2.2 [Ciclo do while](#22-ciclo-do-while)
   - 2.3 [Ciclo for](#23-ciclo-for)
3. [Ejercicio Integrador](#3-ejercicio-integrador)
4. [Reflexión](#4-reflexión)
---
 
## 1. Estructuras Condicionales
 
<div style="text-align: justify;">
Un programa no siempre debe comportarse igual: en la mayoría de los casos necesita reaccionar de forma distinta según los datos que recibe. Las estructuras condicionales son el mecanismo que permite esto, ya que evalúan una expresión lógica (verdadera o falsa) y, según el resultado, dirigen el programa hacia un bloque de instrucciones u otro. Sin ellas, un algoritmo estaría obligado a ejecutar siempre la misma secuencia sin importar lo que ingrese el usuario, lo que lo haría prácticamente inútil para resolver problemas reales.
 
### Características de las Estructuras Condicionales
 
- Permiten que el programa tome decisiones en tiempo de ejecución.
- Se basan en la evaluación de expresiones lógicas (verdadero/falso).
- Modifican el orden en que se ejecutan las instrucciones.
- Son la base para resolver problemas con múltiples escenarios posibles.
- Aumentan la flexibilidad y adaptabilidad de un algoritmo.
---
 
### 1.1 Condicional Simple (if)
 
Se usa cuando existe una sola acción que debe ejecutarse, y solo si se cumple una condición puntual; si no se cumple, el programa simplemente continúa sin hacer nada especial. Es la estructura condicional más básica y suele usarse para validaciones rápidas.
 
#### Sintaxis General
 
```txt
SI condición ENTONCES
 
    instrucciones
 
FIN_SI
```
 
#### Pseudocódigo
 
```txt
INICIO
 
    LEER edad
 
    SI edad >= 18 ENTONCES
        ESCRIBIR "Mayor de edad"
    FIN_SI
 
FIN
```
 
#### Diagrama de Flujo
 
<p align="center">
<img width="559" height="774" alt="image" src="https://github.com/user-attachments/assets/9adef7ee-15b8-406d-b865-d3821d61c62d" />
</p>
---
 
### 1.2 Condicional Doble (if - else)
 
A diferencia del condicional simple, esta estructura contempla dos caminos posibles: uno para cuando la condición se cumple y otro para cuando no se cumple. Es la opción adecuada cuando un problema tiene exactamente dos resultados posibles y excluyentes entre sí.
 
#### Sintaxis General
 
```txt
SI condición ENTONCES
 
    instrucciones
 
SINO
 
    instrucciones
 
FIN_SI
```
 
#### Pseudocódigo
 
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
 
#### Diagrama de Flujo
 
<p align="center">
<img width="697" height="802" alt="image" src="https://github.com/user-attachments/assets/90dbe08b-b973-46ea-b6af-6af3bf391333" />
</p>
---
 
### 1.3 Condicional Múltiple (if - else if)
 
Cuando un problema tiene más de dos resultados posibles, encadenar varios condicionales simples se vuelve poco práctico. La estructura múltiple resuelve esto evaluando una condición tras otra dentro de un mismo bloque, hasta encontrar la primera que se cumpla; si ninguna se cumple, se ejecuta un bloque por defecto. Esto ordena mejor el algoritmo y evita repetir lógica innecesaria.
 
#### Sintaxis General
 
```txt
SI condición1 ENTONCES
 
    instrucciones
 
SINO SI condición2 ENTONCES
 
    instrucciones
 
SINO
 
    instrucciones
 
FIN_SI
```
 
#### Pseudocódigo
 
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
 
#### Diagrama de Flujo
 
<p align="center">
<img width="604" height="778" alt="image" src="https://github.com/user-attachments/assets/51f7d387-2d49-4d1a-b490-d6e27898c632" />
</p>
</div>
---
 
## 2. Estructuras Repetitivas
 
<div style="text-align: justify;">
Cuando un mismo conjunto de instrucciones debe ejecutarse varias veces, escribirlo repetidamente en el código sería poco práctico y difícil de mantener. Las estructuras repetitivas, o ciclos, resuelven este problema al permitir que un bloque de instrucciones se repita las veces que sea necesario, ya sea un número fijo de veces o mientras se cumpla una condición determinada.
 
### Características de las Estructuras Repetitivas
 
- Evitan la repetición innecesaria de código.
- Simplifican el mantenimiento y la lectura del programa.
- Permiten automatizar tareas que se repiten un número definido o indefinido de veces.
- Optimizan el rendimiento del algoritmo.
- Son esenciales para procesar listas o conjuntos grandes de datos.
---
 
### 2.1 Ciclo while
 
Este ciclo primero evalúa la condición y, solo si es verdadera, ejecuta el bloque de instrucciones; luego vuelve a evaluar la condición y repite el proceso hasta que esta se vuelva falsa. Su particularidad es que, si la condición es falsa desde el inicio, el bloque puede no ejecutarse ni una sola vez.
 
#### Sintaxis General
 
```txt
MIENTRAS condición HACER
 
    instrucciones
 
FIN_MIENTRAS
```
 
#### Pseudocódigo
 
```txt
INICIO
 
    contador ← 1
 
    MIENTRAS contador <= 5 HACER
 
        ESCRIBIR contador
 
        contador ← contador + 1
 
    FIN_MIENTRAS
 
FIN
```
 
#### Diagrama de Flujo
 
<p align="center">
<img width="506" height="849" alt="image" src="https://github.com/user-attachments/assets/03026e19-a6a7-4295-aee3-85754532aed9" />
</p>
---
 
### 2.2 Ciclo do while
 
A diferencia del `while`, en esta estructura el bloque de instrucciones se ejecuta primero y la condición se evalúa al final. Esto garantiza que las instrucciones se ejecuten al menos una vez, sin importar si la condición es verdadera o falsa desde el principio.
 
#### Sintaxis General
 
```txt
HACER
 
    instrucciones
 
MIENTRAS condición
```
 
#### Pseudocódigo
 
```txt
INICIO
 
    HACER
 
        ESCRIBIR "Ingrese un número positivo"
        LEER n
 
    MIENTRAS n <= 0
 
FIN
```
 
#### Diagrama de Flujo
 
<p align="center">
<img width="616" height="824" alt="image" src="https://github.com/user-attachments/assets/a04d6744-9c25-4494-9842-5be6f00959ca" />
</p>
---
 
### 2.3 Ciclo for
 
Cuando se sabe de antemano exactamente cuántas veces debe repetirse un proceso, el ciclo `for` es la opción más directa, ya que integra en una sola línea la inicialización de la variable de control, la condición de repetición y el incremento (o decremento). Esto lo convierte en una de las estructuras repetitivas más usadas por su compacidad.
 
#### Sintaxis General
 
```txt
PARA variable ← inicio HASTA fin HACER
 
    instrucciones
 
FIN_PARA
```
 
#### Pseudocódigo
 
```txt
INICIO
 
    PARA i ← 1 HASTA 10 HACER
 
        ESCRIBIR i
 
    FIN_PARA
 
FIN
```
 
#### Diagrama de Flujo
 
<p align="center">
<img width="397" height="782" alt="image" src="https://github.com/user-attachments/assets/28a419cc-706c-4412-a0cd-d0741b587a45" />
</p>
</div>
---
 
## 3. Ejercicio Integrador
 
<div style="text-align: justify;">
### 3.1 Planteamiento del Problema
 
Se requiere desarrollar un programa que solicite cinco calificaciones de un estudiante, calcule su promedio general y determine, en función de dicho promedio, si el estudiante aprueba o reprueba la asignatura.
 
---
 
### 3.2 Análisis del Problema
 
<p align="center">
<img width="1727" height="159" alt="image" src="https://github.com/user-attachments/assets/6264aa0a-9e4b-4013-b212-2bd467d29ea4" />
</p>
---
 
### 3.3 Diseño del Algoritmo
 
#### Pseudocódigo
 
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
 
### 3.4 Diagrama de Flujo
 
<p align="center">
<img width="299" height="830" alt="image" src="https://github.com/user-attachments/assets/45928547-676b-45ed-8273-ca0814af8a88" />
</p>
---
 
### 3.5 Codificación
 
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
 
### 3.6 Validación
 
#### Caso 1
 
**Datos de Entrada**
 
- 8
- 9
- 7
- 10
- 8
**Resultado Esperado**
 
<p align="center">
<img width="1196" height="739" alt="image" src="https://github.com/user-attachments/assets/768a8f18-99cd-4541-90c4-f170e6e7ea11" />
</p>
</div>
---
 
## 4. Reflexión
 
<div style="text-align: justify;">
Esta unidad me hizo entender que programar no se reduce a escribir instrucciones, sino a estructurar un razonamiento lógico capaz de adaptarse a distintas situaciones. Al inicio tuve dificultad para diferenciar cuándo convenía usar un ciclo `while`, un `do while` o un `for`, ya que en varios ejercicios cualquiera de los tres parecía resolver el problema; con la práctica fui notando que la clave está en si se conoce de antemano el número de repeticiones (`for`) o si la condición debe evaluarse antes o después de ejecutar el bloque (`while` frente a `do while`).
 
Aplicar las pruebas de escritorio en cada ejercicio, especialmente en el integrador, me ayudó a confirmar que la lógica del ciclo `for` para acumular las cinco notas y calcular el promedio funcionaba correctamente antes de pasarlo a código en C. También reforcé la relación entre las estructuras condicionales y las repetitivas: en el ejercicio final, el condicional que decide entre "APROBADO" y "REPROBADO" solo tiene sentido después de que el ciclo terminó de acumular y calcular el promedio, lo que me dejó más claro cómo ambas estructuras se combinan en un mismo algoritmo para resolver un problema completo.
 
En general, esta unidad fortaleció mi capacidad de análisis antes de codificar y me confirmó la utilidad real del pseudocódigo y los diagramas de flujo como herramientas para detectar errores de lógica antes de enfrentarme a errores de sintaxis en el lenguaje C.
 
</div>
---
 
## 🔗 Navegación
 
[⬅ Volver a la Portada](00_Portada.md)
 
| Navegación |
|---|
| [📘 Unidad 1](01_Unidad-1.md) |
| [📘 Unidad 3](03_Unidad-3.md) |
| [📝 Conclusiones Generales](04_Conclusiones-Generales.md) |
| [📚 Bibliografía](05_Bibliografia.md) |
| [🤖 Declaración de uso de la IA](06_Declaración-de-uso-de-la-IA.md) |
 
---
