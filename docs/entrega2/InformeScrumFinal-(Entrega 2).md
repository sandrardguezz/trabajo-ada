# Informe Scrum Final - Proyecto TurbineH

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

GitHub también sirvió para almacenar los diagramas -tanto en formato imagen *(.png)* como su código fuente en PlantUML *(.puml)*- y la documentación del Sprint, manteniendo un registro completo de los cambios.

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

* Diagrama ER: Se identificaron las principales tablas del sistema junto con sus atributos, claves primarias, claves foráneas y relaciones.
* Diagrama UML de clases: Se elaboró una primera versión con las clases principales del sistema, sus atributos, métodos y relaciones.
* Diagrama de componentes: Se preparó una representación general de la arquitectura del sistema y varios diagramas detallados para observar sus partes.

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

El objetivo fundamental del Sprint 2 ha sido realizar los diagramas de secuencia de los 13 casos de uso definidos en la primera entrega, manteniendo la coherencia con los modelos estructurales del Sprint 1.

Además, nos propusimos llevar a cabo una revisión conjunta de todos los diagramas estructurales (Diagrama ER, Diagrama UML de clases y Diagrama de componentes) para dejarlos en una versión completa y adecuada.

---

### 4.3. Planificación del Sprint

De cara a este Sprint, la organización de roles del equipo se mantuvo igual que en el anterior debido al corto margen de tiempo disponible. Por su parte, la asignación de los diagramas de secuencia quedó repartida de la siguiente manera:

| Responsable/s | Casos de uso |
|---|---|
| Sandra Rodríguez | CU11 |
| Hugo Trujillo | CU03, CU06, CU10 |
| Telesforo Romero | CU02, CU12 |
| Loretta Martín | CU01, CU04, CU09 |
| Robert Marian Mustafa | CU07, CU08 |
| Sergio Ruiz Navas | CU13 |
| Adiel Rodríguez | CU05 |

De forma paralela, todos los integrantes participaron en puestas en común para definir las versiones mejoradas de los modelos propuestos en el anterior Sprint, siendo los responsables originales de cada diagrama los encargados de actualizar su documentación.

Una vez finalizados los diagramas de secuencia, se buscó realizar una revisión conjunta de cara a mantener una correlación clara entre todos los modelos entregables. Por último, la documentación Scrum del Sprint 2 fue realizada por Sergio Ruiz Navas.

---

### 4.4. Dependencias entre tareas

Durante la planificación nos dimos cuenta de que los diagramas de secuencia dependían directamente de los modelos estructurales del Sprint 1, ya que los objetos, clases y componentes que intervienen en cada interacción deben coincidir con los definidos en dichos modelos. Gracias a esto, definimos el siguiente flujo de trabajo:

**Revisión de los diagramas propuestos en el Sprint anterior (Diagrama UML de clases, Diagrama ER y Diagrama de componentes) → Desarrollo de los diagramas de secuencia → Revisión cruzada de los diagramas de secuencia**

En la práctica, la revisión de los diagramas anteriores y la elaboración de los diagramas de secuencia se realizaron de forma paralela. Aunque tomamos como punto de partida la mejora de los modelos estructurales,
mientras desarrollábamos los diagramas de secuencia fuimos detectando nuevos aspectos que debíamos añadir o eliminar en los primeros para lograr una mayor coherencia. Por ello, la comunicación interna resultó fundamental para coordinar todos los ajustes.

---

### 4.5. Organización mediante GitHub

En este segundo Sprint, el tablero de GitHub Projects resultó clave para coordinar la carga de trabajo entre los siete integrantes, especialmente al repartir los trece diagramas de forma individual.

Cada miembro actualizó el estado de sus casos de uso asignados a medida que los completaba, mientras que en el repositorio se centralizaron los nuevos archivos (*.png* y *.puml*) de los diagramas de secuencia, dejando registradas sus versiones base pendientes de revisión para el siguiente Sprint.

---

### 4.6. Seguimiento del Sprint

Durante el Sprint 2 se realizaron tres puntos de seguimiento para comprobar la evolución del trabajo y coordinar las tareas del equipo:

#### Seguimiento 1 - Organización del trabajo

En este primer punto se mantuvo la distribución de roles establecida anteriormente y se asignaron los diagramas de secuencia de los casos de uso correspondientes a cada integrante.

Además, se acordó utilizar como referencia los modelos desarrollados durante el Sprint 1 y  la nomenclatura común definida, con el fin de que los diagramas de secuencia fueran coherentes con ellos.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

#### Seguimiento 2 - Elaboración de los diagramas

Durante el desarrollo del Sprint 2 se avanzó en los diagramas de secuencia de cada caso de uso, representando las interacciones entre los actores, las clases y los componentes del sistema.

Al contar ya con las primeras versiones de los diagramas estructurales del anterior Sprint, pudimos iniciar su revisión; sin embargo, al modelar los flujos en los diagramas de secuencia detectamos nuevos aspectos a mejorar en ellos.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

#### Seguimiento 3 - Revisión del trabajo realizado

Para finalizar el Sprint, una vez elaborados los diagramas de secuencia, todos los integrantes realizamos una puesta en común para definir las mejoras necesarias y cerrar los diagramas estructurales del primer Sprint.

Para ello, cada uno de los integrantes redactó una propuesta de cambios necesarios sobre dichos modelos y posteriormente se unificaron en una única lista común, de modo que cada responsable pudiera aplicar la actualización de sus diagramas correspondientes.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

### 4.7. Estado final del Sprint 

Al cierre del Sprint 2 se habían elaborado las primeras versiones de los 13 diagramas de secuencia junto con la lista conjunta y unificada de los cambios necesarios para los diagramas ER, UML de clases y de componentes. No obstante, quedaron dos tareas pendientes para el siguiente sprint:

* Aplicar los cambios acordados en los diagramas del Sprint 1 a partir de la lista unificada al final del sprint.
* Revisar de forma exhaustiva los diagramas de secuencia para garantizar su total coherencia con los modelos estructurales una vez corregidos.

Por tanto, ni la segunda versión de los diagramas estructurales ni la coherencia definitiva entre todos los modelos pudieron darse por cerradas todavía. Una de las decisiones más importantes tomadas fue no modificar los diagramas estructurales de forma individual e inmediata, sino recopilar primero todas las propuestas de cada integrante para asegurar una revisión ordenada.

---

### 4.8. Valoración del Sprint 

El objetivo principal del Sprint 2 se alcanzó en cuanto a la elaboración de las primeras versiones de los 13 diagramas de secuencia correspondientes con cada caso de uso y la identificación unificada de mejoras para los modelos estructurales, aunque por falta de tiempo no se llegaron a aplicar dichos cambios ni a cerrar la revisión final de los diagramas de secuencia.

#### Aspectos positivos:

* División eficaz del trabajo de los diagramas de secuencia entre todos los integrantes, permitiendo avanzar en paralelo.
* Decisión de recopilar y unificar los cambios necesarios antes de modificar los diagramas, logrando que todo el equipo participara en el diseño y que las correcciones respondieran a criterios comunes.
* Empleo de GitHub para centralizar las primeras versiones de los diagramas de secuencia y facilitar su consulta a todo el equipo.

#### Dificultades encontradas:

* Al elaborar los diagramas de secuencia, surgieron nuevos aspectos a corregir y ampliar en los diagramas del Sprint 1.
* Mantener la coherencia terminológica entre los diagramas de secuencia al ser diseñados en paralelo por los compañeros.
* Coordinar al equipo para redactar, unificar y aplicar los cambios en pocos días sin frenar el avance de los diagramas de secuencia.

Por tanto, de cara al Sprint 3, cada responsable deberá aplicar las correcciones acordadas en los diagramas del Sprint 1 y realizar la segunda versión y definitiva de los diagramas de secuencia para garantizar una coherencia total en toda la entrega.

---

## 5. Sprint 3

### 5.1. Duración del Sprint

* Inicio: 14/11/2026
* Fin: 22/11/2026

---

### 5.2. Objetivo del Sprint

El objetivo fundamental del Sprint 3 se ha centrado en la integración, documentación y preparación de la exposición. Asimismo, aplicamos la lista unificada de cambios en los modelos estructurales del primer Sprint y ajustamos los 13 diagramas de secuencia para garantizar una coherencia total entre todos los modelos del sistema.

Una vez realizados todos los cambios finales en los diagramas, elaboramos el informe Scrum final, la presentación de diapositivas y el guion de la exposición, llevando a cabo una revisión general de todo lo entregado.

---

### 5.3. Planificación del Sprint

De cara a este nuevo Sprint, la organización de roles del equipo se mantuvo igual que en el anterior debido al corto margen de tiempo disponible. Por su parte, las tareas documentales asignadas durante este sprint fueron las siguientes:

| Área de trabajo | Responsable/s |
|---|---|
| Documentación Scrum del Sprint 3 | Adiel Rodríguez |
| Informe Scrum Final | Robert Marian Mustafa |
| Guion final | Loretta Martín |
| Presentación | Sandra Rodríguez |

Además de estas tareas,  elaboramos las segundas versiones completas y coherentes de los modelos estructurales (diagrama ER, el diagrama UML de clases y el diagrama de componentes), actualizadas por los responsables de cada modelo. Además, cada integrante cerró la segunda versión definitiva de sus diagramas de secuencia asignados para asegurar su total coherencia con los modelos estructurales.

Previamente a la elaboración del guion final y de la presentación unificada de diapositivas, los distintos responsables aportaron el contenido técnico de cada artefacto para integrar toda la documentación.

---

### 5.4. Dependencias entre tareas

Durante la planificación, identificamos la necesidad de dejar terminados los modelos estructurales antes de ajustar los de secuencia y elaborar la documentación final necesaria de cara a la entrega. Para ello, seguimos este flujo de trabajo:

**Cierre de los modelos estructurales → Cierre de los diagramas de secuencia → Unificación de la presentación y documentación final**

Este orden resultó imprescindible debido a que el ajuste de los diagramas de secuencia dependía directamente de que los modelos estructurales tuvieran aplicadas sus correcciones y fueran coherentes entre sí.

---

### 5.5. Organización mediante GitHub

Durante el Sprint 3, el repositorio de GitHub y el tablero de GitHub Projects sirvieron para coordinar y verificar el cierre completo de la entrega.

En el tablero se gestionaron tanto las tareas de corrección de los modelos anteriores como la elaboración de la documentación final, el guion y la presentación, permitiendo comprobar que todas las tarjetas pasaran a estado finalizado antes del cierre. 

Por su parte, en el repositorio se actualizaron las versiones definitivas de todos los diagramas -tanto estructurales como de secuencia, en formatos *(.png)* y *(.puml)*- junto con la documentación completa del proyecto, dejando todo el trabajo consolidado, ordenado y listo para su entrega.

---

### 5.6. Seguimiento del Sprint

Durante el Sprint 3 se realizaron tres puntos de seguimiento para comprobar la evolución del trabajo y coordinar las tareas del equipo:

#### Seguimiento 1 - Cierre de los modelos estructurales

Durante los primeros días del sprint, los responsables de los modelos estructurales (diagrama ER, diagrama UML de clases y diagrama de componentes) aplicaron la lista común unificada de cambios recogida al final del Sprint 2. 

Una vez realizados estos ajustes, todos los integrantes realizamos una revisión final para verificar que los nombres de tablas, clases, métodos y componentes coincidían sin discrepancias.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

#### Seguimiento 2 - Ajuste y revisión cruzada de los diagramas de secuencia

Con los modelos estructurales ya estabilizados, cada integrante revisó y actualizó de forma independiente los diagramas de secuencia de sus casos de uso asignados.

Una vez ajustados estos diagramas, se realizó una revisión cruzada entre compañeros para comprobar que todas las llamadas, parámetros y entidades reflejaban exactamente la versión definitiva del diseño.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

#### Seguimiento 3 - Revisión del trabajo realizado

Al finalizar el Sprint, cada responsable aportó la explicación técnica detallada de sus artefactos para poder elaborar tanto la presentación de diapositivas como el guion final de la exposición. 

De forma paralela, se recopiló y cerró el informe Scrum final de la entrega.

* Asistentes: Sandra Rodríguez, Adiel Rodríguez, Telesforo Romero, Hugo Trujillo, Sergio Ruiz Navas, Loretta Martín y Robert Marian Mustafa.

---

### 5.7. Estado final del Sprint 

Al cierre del Sprint 3 se habían completado todas las tareas pendientes de los anteriores sprints, incluyendo las versiones definitivas de los modelos estructurales y de los diagramas de secuencia, garantizando una correlación total entre todos ellos para un correcto diseño y explicación de cada uno.

Además, quedó terminada toda la documentación necesaria de la entrega: el informe Scrum final, la presentación y el guion redactado de cara a la exposición.

### Decisiones clave

* No iniciar las segundas versiones de los diagramas de secuencia sin haber dejado antes cerradas y coherentes las versiones definitivas de los modelos estructurales.
* Para lograr una presentación clara y dinámica, se decidió no explicar uno por uno los 13 diagramas de secuencia, sino dejar constancia de su realización y utilizar un flujo continuo representativo del sistema.
* Independientemente de que la exposición estuviera fijada para el 24/11, se decidió mantener el 22/11 como fecha límite interna para tener toda la entrega y diapositivas listas, disponiendo así de tiempo suficiente para preparar la exposición.

---

### 5.8. Valoración del Sprint 

El objetivo principal del Sprint 3 se alcanzó satisfactoriamente, ya que se obtuvieron versiones completas y coherentes tanto de los modelos estructurales como de los diagramas de secuencia iniciados en anteriores sprints.

Además, se completó toda la documentación Scrum requerida y se dejó preparada la presentación junto con el guion para afrontar la defensa del proyecto con seguridad.

#### Aspectos positivos:

* Aplicar de forma ordenada la lista unificada de cambios en los modelos estructurales antes de modificar los diagramas de secuencia, lo que evitó rehacer el trabajo innecesariamente.
* Buena coordinación del equipo en la recta final para integrar todo el contenido técnico en una presentación, un guion e informe Scrum final coherentes.

#### Dificultades encontradas:

* Gestionar la carga de trabajo acumulada en pocos días.
* Unificar el nivel de detalle técnico aportado por cada miembro para ajustarlo a la duración de la exposición, lo que requirió varias revisiones sobre el guion y la presentación.

Una vez terminado el Sprint, todos los integrantes centrarán sus últimos esfuerzos en realizar el ensayo general cronometrado de la exposición y, en caso necesario, aplicar correcciones menores.

---
## 6. Evolución entre Sprint 1, Sprint 2 y Sprint 3

Como hemos visto anteriormente, los sprints reflejan fases claramente diferenciadas dentro del proyecto.

| Sprint 1 | Sprint 2 | Sprint 3 |
|---|---|---|
| Primeras versiones de los diagramas propuestos (ER, UML de clases y de componentes) | Lista común y unificada de los cambios finales sobre ellos | Versiones finales y completas |
| -- | Primera versión de los diagramas de secuencia | Versión final y completa | 
| Documentación parcial | Documentación parcial | Documentación finalizada y completa |
| Objetivo global alcanzado parcialmente | Objetivo global alcanzado parcialmente | Objetivo global alcanzado completamente |

El Sprint 1 permitió cambiar roles dentro del equipo para que todos pudiéramos realizar diferentes tareas y se crearon las primeras versiones de los diagramas ER, UML de clases y de componentes, siendo estos los que englobaban todos los requisitos y casos de uso analizados en la primera entrega.

El Sprint 2 permitió mejorar esos modelos estructurales definiendo una lista común unificada por todos los integrantes (aplicada en el Sprint 3) y realizar los diagramas de secuencia sobre cada caso de uso, ayudándonos también a identificar otros posibles cambios de cara a los diagramas del Sprint 1.

El Sprint 3 permitió realizar toda la documentación final de la entrega, aplicar todos los cambios acordados sobre los modelos estructurales y realizar una segunda versión completa de los diagramas de secuencia, dando así por finalizada la entrega.

---

## 7. Comunicación y coordinación del equipo

La coordinación ha sido fundamental debido a las estrechas dependencias existentes entre las distintas tareas del proyecto.

Aunque había responsables asignados a cada artefacto, la comunicación interna ha resultado clave para consensuar cambios sobre los distintos modelos y mejorar el proyecto en su conjunto. 

Por otra parte, todos los miembros hemos colaborado activamente en el desarrollo global, apoyándonos mutuamente cuando surgían dudas o bloqueos, lo cual ha sido un pilar esencial para el buen funcionamiento del equipo.

Finalmente, para documentar y centralizar todo el trabajo, GitHub -junto con su tablero de seguimiento- ha sido una herramienta muy útil al proporcionar un espacio común donde almacenar los diagramas, gestionar el avance de las tareas y mantener al equipo sincronizado.

---

## 8. Herramientas utilizadas

Para el desarrollo, gestión y documentación de esta segunda entrega del proyecto TurbineH, el equipo se ha apoyado principalmente en las siguientes herramientas:

* GitHub: Utilizado como repositorio centralizado para almacenar tanto el código fuente como las versiones exportadas de los diagramas y toda la documentación generada, manteniendo un control de versiones ordenado.
* GitHub Projects: Empleado como tablero para organizar el flujo de trabajo, asignar responsabilidades y hacer un seguimiento visual del estado de cada tarea a lo largo de los tres sprints.
* PlantUML: Herramienta principal para el modelado y generación mediante código de los distintos diagramas del sistema (Entidad-Relación, UML de clases, componentes y diagramas de secuencia).
* Markdown: Formato estándar utilizado para redactar de forma clara y estructurada la documentación de cada sprint y el informe Scrum final.

El uso combinado de estas herramientas ha facilitado la centralización de la información, permitiendo tanto el avance individual en paralelo como una revisión conjunta ágil y coherente.

---

## 9. Resultado Global

El trabajo desarrollado durante los tres sprints ha permitido elaborar distintos modelos estructurales y diagramas de secuencia a partir de los requisitos y casos de uso definidos en la primera entrega, ofreciendo así una visión arquitectónica y funcional mucho más clara de la aplicación de cara al cliente.

Como resultado final, se han completado y verificado los siguientes entregables:

* Diagrama ER físico
* Diagrama UML de clases
* Diagrama de componentes
* Diagramas de secuencia (CU01-CU13)
* Documentación Scrum
* Material para la exposición (presentación de diapositivas y guion)

Más allá de los artefactos entregados, el desarrollo iterativo a lo largo de los tres sprints ha permitido mejorar progresivamente la organización interna, la comunicación y la coordinación de todo el equipo.
---

## 10. Conclusión

La utilización de Scrum nos ha permitido estructurar el trabajo de forma progresiva y adaptarnos con agilidad a los cambios que han surgido durante el diseño del sistema.

El Sprint 1 sirvió para elaborar los modelos estructurales, siendo estos los más difíciles de abordar al tener que englobar toda la información analizada (requisitos y casos de uso) de la primera entrega, además de permitir la rotación de roles y responsabilidades entre los diferentes integrantes del equipo.

Por su difícil realización, en el Sprint 2 revisamos las dificultades encontradas y elaboramos una lista común unificada con los cambios necesarios. Paralelamente, desarrollamos los 13 diagramas de secuencia, los cuales resultaron claves en esta fase al ayudarnos a identificar nuevos aspectos a mejorar en los modelos estructurales.

Finalmente, el Sprint 3 permitió cerrar la entrega aplicando todos los ajustes pendientes sobre los diagramas y completando la documentación final de cara a la exposición.

La principal aportación de esta metodología no ha sido únicamente repartir las tareas entre los miembros del equipo, sino permitir que el trabajo desarrollado pueda revisarse, relacionarse y refinarse de manera iterativa.

De este modo, el avance a lo largo de los tres sprints nos ha permitido evolucionar desde unos primeros bocetos con discrepancias hasta unos modelos estructurales y de comportamiento sólidos, fáciles de analizar y totalmente coherentes, ofreciendo así una visión clara y organizada del sistema TurbineH.





