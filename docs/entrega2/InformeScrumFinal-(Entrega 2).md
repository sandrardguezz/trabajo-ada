# Informe Scrum Final - Proyecto Turbineh

## 1. Introducción

Como ya comentamos en la otra entrega, nuestro proyecto se desarrolla bajo la metodología ágil Scrum, estructurada en tres sprints bien diferenciados.

El objetivo de emplear esta metodología es organizar adecuadamente las tareas, repartir responsabilidades y realizar un seguimiento continuo del proyecto que permita identificar
posibles cambios de cara a la entrega y refinar el *Increment* a lo largo de los sprints.

Gestionar estos cambios de forma eficaz ha sido una tarea fundamental en nuestro trabajo, ya que, como veremos más adelante, siempre hemos partido de una primera versión de todas 
las tareas entregables para someterlas posteriormente a revisión, logrando así un mejor desarrollo y organización.

Finalmente, para centralizar y almacenar todo el trabajo de manera escalable, hemos utilizado un repositorio en GitHub junto con GitHub Projects, manteniendo la misma dinámica de trabajo
de la entrega previa.

---
## 2. Organización del equipo

Durante el proyecto se establecieron los siguientes roles principales:

* Scrum Master: Telesforo Romero
* Product Owner: Adiel Rodríguez

Estos cambios, con respecto a la entrega anterior, no se deben a un mal desempeño o problema, sino a una decisión consensuada en la que todos los integrantes del equipo puedan rotar los roles y desempeñar cualquiera de ellos.

El Scrum Master, Telesforo, se ha dedicado a organizar las tareas de la manera más adaptable al equipo y a prestar 
especial atención a posibles bloqueos o dependencias entre ellas.

Por otra parte, el Product Owner, Adiel, se ha encargado de definir y recopilar todas las tareas entregables, diferenciándolas también 
por sprint (Product Backlog), así como resolver aquellas dudas relacionadas con el producto final.

Igualmente, ambos también se han dedicado a realizar tareas dentro del propio proyecto, al igual que los demás miembros del equipo, habiéndonos
repartido las diferentes áreas de la siguiente manera:
| Área de trabajo | Responsable/s |
|---|---|
| Diagrama ER físico | Telesforo Romero, Hugo Trujillo |
| Diagrama UML de clases | Sergio Ruiz Navas, Adiel Rodríguez |
| Diagrama de componentes | Sandra Rodríguez |
| Documentación Scrum del Sprint 1 | Telesforo Romero |
| Documentación Scrum del Sprint 2 | Sergio Ruiz Navas |
| Documentación Scrum del Sprint 3 | Adiel Rodríguez |
| Informe Scrum Final | Robert Marian Mustafa |
| Guion final | Loretta Martín |
| Presentación | Sandra Rodríguez |

Como podemos ver, en esta tabla no incluimos los diagramas de secuencia, ya que los hemos realizado entre todos y, concretamente, los hemos repartido de la siguiente forma:
| Responsable/s | Casos de uso |
|---|---|
| Sandra Rodríguez | CU11 |
| Hugo Trujillo | CU03, CU06, CU10 |
| Telesforo Romero | CU02, CU12 |
| Loretta Martín | CU01, CU04, CU09 |
| Robert Marian Mustafa | CU07, CU08 |
| Sergio Ruiz Navas | CU13 |
| Adiel Rodríguez | CU05 |

Como hemos visto, para llevar a cabo estas tareas hemos tenido que hacer uso de todo lo realizado en la entrega anterior y, en general, todo el equipo ha participado
en distintas tareas para apoyarnos entre unos y otros.

---

## 3. Sprint 1

### 3.1. Duración del Sprint

* Inicio: 22/10/2026
* Fin: 02/11/2026

---

### 3.2. Objetivo del Sprint

El objetivo fundamental del Sprint 1 ha sido establecer una primera estructura del sistema TurbineH, elaborando distintos modelos con una base común para representar de forma adecuada la organización de nuestra aplicación.

Principalmente, nos dedicamos a las siguientes tareas:

* Diagrama Entidad-Relación (ER)
* Diagrama UML de clases
* Diagrama de componentes

Para realizarlas, revisamos los requisitos y casos de uso de la entrega anterior con el fin de mantener una correlación directa con ellos.

---

### 3.3. Planificación del Sprint

Además de establecer una nueva organización de roles dentro del equipo, definimos las tareas necesarias para el desarrollo del Sprint 1, quedando la asignación de la siguiente manera:

| Área de trabajo | Responsable/s |
|---|---|
| Diagrama ER físico | Telesforo Romero, Hugo Trujillo |
| Diagrama UML de clases | Sergio Ruiz Navas, Adiel Rodríguez |
| Diagrama de componentes | Sandra Rodríguez |
| Documentación Scrum del Sprint 1 | Telesforo Romero |

Previamente, todo el equipo realizó una revisión conjunta de los requisitos y casos de uso de la entrega anterior para establecer un punto de partida común en todos los diagramas.

---

### 3.4. Dependencias entre tareas

Durante la planificación, identificamos que los distintos modelos estaban estrechamente relacionados, por lo que no podían desarrollarse de forma totalmente aislada. Para construir una base común y coordinar los diagramas de la mejor manera posible, seguimos esta secuencia de trabajo:

**Revisión de requisitos y casos de uso → Desarrollo en paralelo (Diagrama UML de clases, Diagrama ER y Diagrama de componentes)**

Aunque los diagramas se realizaron en paralelo -siendo fundamental la comunicación interna-, se tomó el Diagrama de clases como referencia inicial para trasladar sus conceptos al resto de modelos, cerrando con el Diagrama de componentes por su carácter más visual de cara a la presentación. 

---

### 3.5. Organización mediante GitHub

Para organizar el trabajo continuamos utilizando el repositorio de GitHub junto con el tablero de GitHub Projects creados en la primera entrega. 

Dentro del tablero representamos el estado de las diferentes tareas, donde cada integrante actualizó su progreso a medida que avanzaba, permitiendo conocer en todo momento qué tareas estaban pendientes, cuáles en curso y cuáles finalizadas.

GitHub también sirvió para almacenar los diagramas - tanto en formato imagen *(.png)* como su código fuente en PlantUML *(.puml)* - y la documentación del Sprint, manteniendo un registro completo de los cambios.

---

### 3.6. Seguimiento del Sprint

Durante el Sprint 1 se realizaron tres puntos de seguimiento para comprobar la evolución del trabajo y coordinar las tareas del equipo:

#### Seguimiento 1 - Organización del equipo

En este primer punto se establecieron las responsabilidades de cada integrante, acordando utilizar los requisitos y casos de uso de la primera entrega como referencia para el diseño de los diagramas.

Además, se formalizó la rotación de roles para que todos los miembros tuvieran la oportunidad de desempeñar distintas funciones.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

#### Seguimiento 2 - Elaboración de los diagramas

Durante el desarrollo del Sprint 1 se avanzó en los modelos previstos.

*Diagrama ER: Se identificaron las principales tablas del sistema junto con sus atributos, claves primarias, claves foráneas y relaciones. 
*Diagrama UML de clases: Se elaboró una primera versión con las clases principales del sistema, sus atributos, métodos y relaciones.
*Diagrama de componentes: Se preparó una representación general de la arquitectura del sistema y varios diagramas detallados para observar sus partes.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas (el resto del equipo también colaboró aportando ideas de diseño y manteniendo una comunicación constante para lograr modelos sencillos y completos).

---

#### Seguimiento 3 - Revisión del trabajo realizado

Al finalizar el Sprint, las primeras versiones de los tres diagramas quedaron almacenadas y disponibles en nuestro repositorio de GitHub, permitiendo disponer de una base inicial de datos, clases y componentes.

No obstante, se detectó la necesidad de continuar revisándolos en el siguiente sprint para garantizar una total coherencia entre ellos.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

### 3.7. Estado final del Sprint 

Al cierre del Sprint 1 se habían elaborado las primeras versiones de los modelos principales de diseño, aunque quedaban aspectos por pulir, principalmente comprobar la coherencia entre modelos y unificar los nombres comunes. Asimismo, se verificó que todos los requisitos y casos de uso de la primera entrega estuvieran reflejados.

Una de las decisiones más importantes tomadas fue mantener el diagrama ER lo más sencillo y estable posible, fijándolo como base estructural para evitar cambios en cascada en el resto de modelos ante posibles ajustes conceptuales.

---

### 3.8. Valoración del Sprint 

El objetivo principal del Sprint 1 se alcanzó satisfactoriamente, ya que se obtuvo una primera versión bastante completa de los tres diagramas estructurales previstos, proporcionando una base sólida para continuar con el diseño del sistema en el siguiente Sprint.

#### Aspectos positivos:

* División eficaz del trabajo entre varios integrantes, permitiendo avanzar en paralelo.
* Uso de los requisitos y casos de uso de la primera entrega como referencia directa.
* Empleo de GitHub para centralizar los diagramas y facilitar su consulta a todo el equipo.
* Definición de un diagrama ER sencillo y estable que minimiza futuros cambios estructurales.

#### Dificultades encontradas:

* Determinar el nivel de detalle adecuado de cada modelo.
* Mantener la coherencia terminológica entre los diagramas al ser diseñados en paralelo por distintos compañeros.

Por tanto, de cara al Sprint 2, se planificó una revisión conjunta de todos los diagramas para unificar los conceptos principales, manteniendo la comunicación interna como eje clave antes de abordar los diagramas de secuencia.

---

## 4. Sprint 2

### 4.1. Duración del Sprint

* Inicio: 03/11/2026
* Fin: 13/11/2026

---

### 4.2. Objetivo del Sprint

El objetivo fundamental del Sprint 1 ha sido establecer una primera estructura del sistema TurbineH, elaborando distintos modelos con una base común para representar de forma adecuada la organización de nuestra aplicación.

Principalmente, nos dedicamos a las siguientes tareas:

* Diagrama Entidad-Relación (ER)
* Diagrama UML de clases
* Diagrama de componentes

Para realizarlas, revisamos los requisitos y casos de uso de la entrega anterior con el fin de mantener una correlación directa con ellos.

---

### 4.3. Planificación del Sprint

Además de establecer una nueva organización de roles dentro del equipo, definimos las tareas necesarias para el desarrollo del Sprint 1, quedando la asignación de la siguiente manera:

| Área de trabajo | Responsable/s |
|---|---|
| Diagrama ER físico | Telesforo Romero, Hugo Trujillo |
| Diagrama UML de clases | Sergio Ruiz Navas, Adiel Rodríguez |
| Diagrama de componentes | Sandra Rodríguez |
| Documentación Scrum del Sprint 1 | Telesforo Romero |

Previamente, todo el equipo realizó una revisión conjunta de los requisitos y casos de uso de la entrega anterior para establecer un punto de partida común en todos los diagramas.

---

### 4.4. Dependencias entre tareas

Durante la planificación, identificamos que los distintos modelos estaban estrechamente relacionados, por lo que no podían desarrollarse de forma totalmente aislada. Para construir una base común y coordinar los diagramas de la mejor manera posible, seguimos esta secuencia de trabajo:

**Revisión de requisitos y casos de uso → Desarrollo en paralelo (Diagrama UML de clases, Diagrama ER y Diagrama de componentes)**

Aunque los diagramas se realizaron en paralelo -siendo fundamental la comunicación interna-, se tomó el Diagrama de clases como referencia inicial para trasladar sus conceptos al resto de modelos, cerrando con el Diagrama de componentes por su carácter más visual de cara a la presentación. 

---

### 4.5. Organización mediante GitHub

Para organizar el trabajo continuamos utilizando el repositorio de GitHub junto con el tablero de GitHub Projects creados en la primera entrega. 

Dentro del tablero representamos el estado de las diferentes tareas, donde cada integrante actualizó su progreso a medida que avanzaba, permitiendo conocer en todo momento qué tareas estaban pendientes, cuáles en curso y cuáles finalizadas.

GitHub también sirvió para almacenar los diagramas - tanto en formato imagen *(.png)* como su código fuente en PlantUML *(.puml)* - y la documentación del Sprint, manteniendo un registro completo de los cambios.

---

### 4.6. Seguimiento del Sprint

Durante el Sprint 1 se realizaron tres puntos de seguimiento para comprobar la evolución del trabajo y coordinar las tareas del equipo:

#### Seguimiento 1 - Organización del equipo

En este primer punto se establecieron las responsabilidades de cada integrante, acordando utilizar los requisitos y casos de uso de la primera entrega como referencia para el diseño de los diagramas.

Además, se formalizó la rotación de roles para que todos los miembros tuvieran la oportunidad de desempeñar distintas funciones.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

#### Seguimiento 2 - Elaboración de los diagramas

Durante el desarrollo del Sprint 1 se avanzó en los modelos previstos.

*Diagrama ER: Se identificaron las principales tablas del sistema junto con sus atributos, claves primarias, claves foráneas y relaciones. 
*Diagrama UML de clases: Se elaboró una primera versión con las clases principales del sistema, sus atributos, métodos y relaciones.
*Diagrama de componentes: Se preparó una representación general de la arquitectura del sistema y varios diagramas detallados para observar sus partes.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas (el resto del equipo también colaboró aportando ideas de diseño y manteniendo una comunicación constante para lograr modelos sencillos y completos).

---

#### Seguimiento 3 - Revisión del trabajo realizado

Al finalizar el Sprint, las primeras versiones de los tres diagramas quedaron almacenadas y disponibles en nuestro repositorio de GitHub, permitiendo disponer de una base inicial de datos, clases y componentes.

No obstante, se detectó la necesidad de continuar revisándolos en el siguiente sprint para garantizar una total coherencia entre ellos.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

### 4.7. Estado final del Sprint 

Al cierre del Sprint 1 se habían elaborado las primeras versiones de los modelos principales de diseño, aunque quedaban aspectos por pulir, principalmente comprobar la coherencia entre modelos y unificar los nombres comunes. Asimismo, se verificó que todos los requisitos y casos de uso de la primera entrega estuvieran reflejados.

Una de las decisiones más importantes tomadas fue mantener el diagrama ER lo más sencillo y estable posible, fijándolo como base estructural para evitar cambios en cascada en el resto de modelos ante posibles ajustes conceptuales.

---

### 4.8. Valoración del Sprint 

El objetivo principal del Sprint 1 se alcanzó satisfactoriamente, ya que se obtuvo una primera versión bastante completa de los tres diagramas estructurales previstos, proporcionando una base sólida para continuar con el diseño del sistema en el siguiente Sprint.

#### Aspectos positivos:

* División eficaz del trabajo entre varios integrantes, permitiendo avanzar en paralelo.
* Uso de los requisitos y casos de uso de la primera entrega como referencia directa.
* Empleo de GitHub para centralizar los diagramas y facilitar su consulta a todo el equipo.
* Definición de un diagrama ER sencillo y estable que minimiza futuros cambios estructurales.

#### Dificultades encontradas:

* Determinar el nivel de detalle adecuado de cada modelo.
* Mantener la coherencia terminológica entre los diagramas al ser diseñados en paralelo por distintos compañeros.

Por tanto, de cara al Sprint 2, se planificó una revisión conjunta de todos los diagramas para unificar los conceptos principales, manteniendo la comunicación interna como eje clave antes de abordar los diagramas de secuencia.

---

## 5. Sprint 3

### 5.1. Duración del Sprint

* Inicio: 14/11/2026
* Fin: 22/11/2026

---

### 5.2. Objetivo del Sprint

El objetivo fundamental del Sprint 1 ha sido establecer una primera estructura del sistema TurbineH, elaborando distintos modelos con una base común para representar de forma adecuada la organización de nuestra aplicación.

Principalmente, nos dedicamos a las siguientes tareas:

* Diagrama Entidad-Relación (ER)
* Diagrama UML de clases
* Diagrama de componentes

Para realizarlas, revisamos los requisitos y casos de uso de la entrega anterior con el fin de mantener una correlación directa con ellos.

---

### 5.3. Planificación del Sprint

Además de establecer una nueva organización de roles dentro del equipo, definimos las tareas necesarias para el desarrollo del Sprint 1, quedando la asignación de la siguiente manera:

| Área de trabajo | Responsable/s |
|---|---|
| Diagrama ER físico | Telesforo Romero, Hugo Trujillo |
| Diagrama UML de clases | Sergio Ruiz Navas, Adiel Rodríguez |
| Diagrama de componentes | Sandra Rodríguez |
| Documentación Scrum del Sprint 1 | Telesforo Romero |

Previamente, todo el equipo realizó una revisión conjunta de los requisitos y casos de uso de la entrega anterior para establecer un punto de partida común en todos los diagramas.

---

### 5.4. Dependencias entre tareas

Durante la planificación, identificamos que los distintos modelos estaban estrechamente relacionados, por lo que no podían desarrollarse de forma totalmente aislada. Para construir una base común y coordinar los diagramas de la mejor manera posible, seguimos esta secuencia de trabajo:

**Revisión de requisitos y casos de uso → Desarrollo en paralelo (Diagrama UML de clases, Diagrama ER y Diagrama de componentes)**

Aunque los diagramas se realizaron en paralelo -siendo fundamental la comunicación interna-, se tomó el Diagrama de clases como referencia inicial para trasladar sus conceptos al resto de modelos, cerrando con el Diagrama de componentes por su carácter más visual de cara a la presentación. 

---

### 5.5. Organización mediante GitHub

Para organizar el trabajo continuamos utilizando el repositorio de GitHub junto con el tablero de GitHub Projects creados en la primera entrega. 

Dentro del tablero representamos el estado de las diferentes tareas, donde cada integrante actualizó su progreso a medida que avanzaba, permitiendo conocer en todo momento qué tareas estaban pendientes, cuáles en curso y cuáles finalizadas.

GitHub también sirvió para almacenar los diagramas - tanto en formato imagen *(.png)* como su código fuente en PlantUML *(.puml)* - y la documentación del Sprint, manteniendo un registro completo de los cambios.

---

### 5.6. Seguimiento del Sprint

Durante el Sprint 1 se realizaron tres puntos de seguimiento para comprobar la evolución del trabajo y coordinar las tareas del equipo:

#### Seguimiento 1 - Organización del equipo

En este primer punto se establecieron las responsabilidades de cada integrante, acordando utilizar los requisitos y casos de uso de la primera entrega como referencia para el diseño de los diagramas.

Además, se formalizó la rotación de roles para que todos los miembros tuvieran la oportunidad de desempeñar distintas funciones.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

#### Seguimiento 2 - Elaboración de los diagramas

Durante el desarrollo del Sprint 1 se avanzó en los modelos previstos.

*Diagrama ER: Se identificaron las principales tablas del sistema junto con sus atributos, claves primarias, claves foráneas y relaciones. 
*Diagrama UML de clases: Se elaboró una primera versión con las clases principales del sistema, sus atributos, métodos y relaciones.
*Diagrama de componentes: Se preparó una representación general de la arquitectura del sistema y varios diagramas detallados para observar sus partes.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas (el resto del equipo también colaboró aportando ideas de diseño y manteniendo una comunicación constante para lograr modelos sencillos y completos).

---

#### Seguimiento 3 - Revisión del trabajo realizado

Al finalizar el Sprint, las primeras versiones de los tres diagramas quedaron almacenadas y disponibles en nuestro repositorio de GitHub, permitiendo disponer de una base inicial de datos, clases y componentes.

No obstante, se detectó la necesidad de continuar revisándolos en el siguiente sprint para garantizar una total coherencia entre ellos.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

### 5.7. Estado final del Sprint 

Al cierre del Sprint 1 se habían elaborado las primeras versiones de los modelos principales de diseño, aunque quedaban aspectos por pulir, principalmente comprobar la coherencia entre modelos y unificar los nombres comunes. Asimismo, se verificó que todos los requisitos y casos de uso de la primera entrega estuvieran reflejados.

Una de las decisiones más importantes tomadas fue mantener el diagrama ER lo más sencillo y estable posible, fijándolo como base estructural para evitar cambios en cascada en el resto de modelos ante posibles ajustes conceptuales.

---

### 5.8. Valoración del Sprint 

El objetivo principal del Sprint 1 se alcanzó satisfactoriamente, ya que se obtuvo una primera versión bastante completa de los tres diagramas estructurales previstos, proporcionando una base sólida para continuar con el diseño del sistema en el siguiente Sprint.

#### Aspectos positivos:

* División eficaz del trabajo entre varios integrantes, permitiendo avanzar en paralelo.
* Uso de los requisitos y casos de uso de la primera entrega como referencia directa.
* Empleo de GitHub para centralizar los diagramas y facilitar su consulta a todo el equipo.
* Definición de un diagrama ER sencillo y estable que minimiza futuros cambios estructurales.

#### Dificultades encontradas:

* Determinar el nivel de detalle adecuado de cada modelo.
* Mantener la coherencia terminológica entre los diagramas al ser diseñados en paralelo por distintos compañeros.

Por tanto, de cara al Sprint 2, se planificó una revisión conjunta de todos los diagramas para unificar los conceptos principales, manteniendo la comunicación interna como eje clave antes de abordar los diagramas de secuencia.




