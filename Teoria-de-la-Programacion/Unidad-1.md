---
[⬅ Volver a la Portada](Portada.md)

## UNIDAD 1

</div>

<div style="text-align: justify;">

### Conceptos Fundamentales de Programación

**Algoritmo**  
Un algoritmo se define como un conjunto ordenado y finito de operaciones o pasos lógicos que permiten hallar la solución a un problema determinado. En el ámbito de la informática, constituye la base sobre la cual se construye cualquier proceso de software, debiendo ser preciso, estar bien definido y ser finito. Su importancia radica en que permite estructurar la lógica de resolución antes de ser traducida a un lenguaje que la computadora pueda procesar.

<p align="center">
<img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/73065d5b-ebe4-4ed3-86f9-7ee62936a3d1" />
</p>

**Pseudocódigo**  
El pseudocódigo es una herramienta de programación que utiliza un lenguaje intermedio entre el lenguaje humano y el código de programación real. No es un lenguaje ejecutable por una máquina, sino una técnica para que el programador se concentre en la lógica del algoritmo sin preocuparse por las reglas sintácticas estrictas de un lenguaje específico. Facilita la transición de la idea mental a la implementación técnica final.

<p align="center">
<img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/78ef6310-59d8-4a54-888e-c147db02546a" />
</p>

**Diagrama de Flujo**  
El diagrama de flujo es la representación gráfica de un algoritmo, donde se utilizan símbolos estandarizados como óvalos, rombos y rectángulos para describir la secuencia de pasos de un proceso. Estas figuras se conectan mediante flechas que indican la dirección del flujo de los datos y el control. Es una herramienta visual fundamental para identificar posibles errores lógicos y para comunicar la estructura de un programa a otros desarrolladores de manera sencilla.

<p align="center">
<img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/c83c1fbe-88b6-43d6-bb24-87e098597062" />
</p>

**Prueba de Escritorio**  
La prueba de escritorio es un proceso de verificación manual en el que el programador sigue paso a paso las instrucciones de un algoritmo utilizando valores de entrada específicos. El objetivo es validar que el algoritmo produce los resultados esperados y detectar fallos en la lógica o en el manejo de las variables antes de realizar la codificación. Generalmente se organiza en una tabla donde se registran los cambios de valor en cada variable conforme avanza la ejecución.

<p align="center">
<img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/0683985c-fa0f-4ffd-9631-6a108fc565db" />
</p>

**Lenguajes de Programación**  
Los lenguajes de programación son sistemas de comunicación estructurados que permiten a un ser humano dar instrucciones precisas a una computadora para que realice tareas específicas. Estos se dividen principalmente en lenguajes de bajo nivel (cercanos al hardware) y lenguajes de alto nivel (más legibles y abstractos). Cada lenguaje posee su propia sintaxis y semántica, adaptándose a diferentes necesidades como el desarrollo web, la ciencia de datos o la creación de sistemas operativos.

<p align="center">
<img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/d1e6b552-99ef-43e8-b7b0-4f1e0dc499b7" />
</p>

**Programación por Bloques**  
La programación por bloques es un paradigma de desarrollo visual que sustituye la escritura de texto por el uso de piezas gráficas que encajan entre sí, similar a un rompecabezas. Cada bloque contiene una instrucción lógica (como un bucle o una condición), lo que permite al usuario centrarse en el pensamiento computacional y la resolución de problemas sin el riesgo de cometer errores de escritura. Es ampliamente utilizada en entornos educativos como Scratch o Blockly para facilitar el aprendizaje inicial.

<p align="center">
<img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/979ea4ec-f546-41c3-ae00-fc687f073aa1" />
</p>

<div align="center">

## EJERCICIOS CON ESTRUCTURA SECUENCIAL

</div>

<div style="text-align: justify;">

### Ejercicio 1: Cálculo de presupuesto en PSeInt

**Planteamiento del problema**  
El problema consiste en desarrollar una solución automatizada para un almacén que necesita calcular el costo total de un trabajo basado en la extensión de superficie procesada. Se requiere que el sistema permita el ingreso de una medida variable y aplique una tarifa estándar para generar el monto final de cobro.

**Análisis del problema**  
Para resolver este requerimiento, se identifica como entrada principal la cantidad de metros cuadrados (m2), la cual debe ser un número real para permitir decimales. El proceso interno consiste en asignar un valor constante de 50 a la variable Trabajo y realizar la multiplicación de esta tarifa por los metros cuadrados ingresados. La salida esperada es el valor almacenado en la variable Precio.

**Diseño del algoritmo**

<p align="center">
<img width="620" height="681" alt="image" src="https://github.com/user-attachments/assets/26a27771-30a1-482a-9d11-916dcd0c5c05" />
</p>

**Diagrama de flujo**

<p align="center">
<img width="1109" height="732" alt="image" src="https://github.com/user-attachments/assets/9e12b524-3d1a-4f7e-904f-87c11a7637b3" />

**ejecución de programa**

<p align="center">
<img width="555" height="372" alt="image" src="https://github.com/user-attachments/assets/33063871-bd50-4fa7-9184-e1895d4f7efe" />
</p>

**Prueba de escritorio**

<p align="center">
<img width="650" height="226" alt="image" src="https://github.com/user-attachments/assets/1ee9570a-f10a-4280-be0c-34cf3e7e6532" />
</p>

---

### Ejercicio 2: Sistema de comisiones en Lenguaje C

**Planteamiento del problema**  
Se busca crear un programa en lenguaje C que gestione el pago de comisiones de ventas de una empresa. El sistema debe procesar tres montos de ventas predefinidos de diferentes clientes, aplicar una tasa de comisión del 4% a cada uno y calcular el gasto total que representa para la empresa el pago de estas bonificaciones.

**Análisis del problema**  
En el análisis se determinan tres constantes de tipo flotante para los montos de las ventas correspondientes a 30,000.00, 29,000.00 y 33,000.00. El proceso matemático requiere calcular el 4% individualmente para cada venta (porcentaje1, porcentaje2, porcentaje3) y sumarlos en una variable global denominada pagototal. Las salidas deben ser tanto el total acumulado como el desglose por cada vendedor.

**Diseño del algoritmo**

<p align="center">
<img width="1086" height="730" alt="image" src="https://github.com/user-attachments/assets/8ac9ff11-8023-4286-acdc-e7c0d0ef064a" />
</p>

**ejecución de programa**

<p align="center">
<img width="912" height="233" alt="image" src="https://github.com/user-attachments/assets/94e8c4ff-66ba-4a32-bb89-b606e6990f5e" />
</p>


**Prueba de escritorio**

<p align="center">
<img width="591" height="238" alt="image" src="https://github.com/user-attachments/assets/fa3bafcd-c682-4eab-bab3-92f47abff73b" />
</p>

</div>
---

<div align="center">

### Principales dificultades y reflexión crítica

</div>

<div style="text-align: justify;">

**Reflexión**  
El desarrollo de soluciones computacionales, ya sea mediante pseudocódigo o lenguajes de alto nivel como C, demuestra que la programación no es solo un ejercicio de escritura de código, sino un proceso riguroso de estructuración del pensamiento. Al trabajar con estructuras secuenciales, se hace evidente la importancia de la precisión en el análisis previo; un error en la definición de una constante o en la interpretación de un requerimiento (como el porcentaje de comisión) puede derivar en resultados erróneos independientemente de qué tan bien esté escrito el programa. La transición del diagrama de flujo al código fuente nos enseña que la lógica es universal, pero la implementación exige un dominio de la sintaxis y las reglas específicas del lenguaje para que la máquina ejecute fielmente nuestra intención.

**Conclusión**  
En conclusión, la aplicación de algoritmos y el uso de herramientas como PSeInt y el compilador de C permiten validar que la resolución de problemas técnicos depende fundamentalmente de la descomposición de tareas en pasos finitos y lógicos. La estructura secuencial aplicada en estos ejercicios desde el cálculo de costos por superficie hasta la gestión de comisiones resalta que la entrada, el proceso y la salida son los pilares de cualquier sistema funcional. Además, la práctica constante de realizar pruebas de escritorio garantiza la fiabilidad del software, asegurando que el producto final sea una herramienta útil y precisa para la toma de decisiones en entornos reales como almacenes o departamentos financieros.

</div>

<div align="center">

---

[⬅ Volver a la Portada](Portada.md)
