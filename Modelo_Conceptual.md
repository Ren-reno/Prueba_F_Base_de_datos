# Modelo Conceptual en notacion Chem

## Primer paso para crear una base de datos

El primer paso para crear una base de datos es entender los requerimientos que tiene la empresa que te contrata, para ello se conversa con los usuarios o clientes para entender qué necesita hacer el sistema. Se identifican procesos clave, reglas del negocio, información que se debe guardar, etc.

**Por suerte para la prueba no tendremos que preguntarle a nadie ya que nos daran el enunciado y con eso debemos crear el modelo conceptual con lo que interpretamos**, es importante decir que no existe una unica solucion para un problema, los requerimientos de una empresa se pueden modelar de diferentes formas y estara correcto siempre y cuando respete algunas reglas que tienen los modelos relacionales de base de datos y lo que necesite la empresa.

a continuacion habalre de los que es un Modelo conceptual comenzare hablando de lo que es, sus elementos y finalmente dare ejemplos y tecnicas de como realizar uno. 

---

## Que es el modelo conceptual
Un modelo conceptual es algo parecido a esto 
![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/image-1.png?raw=true)

Como ves es un diagrama que representa los datos principales de un negocio. **Su objetivo es mostrar qué información se necesita guardar y cómo se relaciona esa información entre sí**, sin preocuparse por los detalles técnicos de cómo se almacenará en una computadora. para hacer este diagrama usamos simbolos estandarizados como los de la Notación Chen que hablaremos a continuacion. 

## Notacion Chen 

La Notación Chen, desarrollada por Peter Chen en 1976, **es una de las formas más clásicas y visuales de representar un Modelo Conceptual de una base de datos.** Piensa en ella como un alfabeto de símbolos que nos permite dibujar el "mapa de datos" de un negocio de una manera clara y estandarizada.

Cada símbolo tiene un significado específico, y al combinarlos, podemos comunicar la estructura de la información sin necesidad de entrar en detalles técnicos de programación o bases de datos específicas.

**La Notación Chen se basa en tres componentes principales: Entidades, Atributos y Relaciones.** Cada uno tiene su propia representación gráfica:

---
### Entidad 

Las entidades en el diagrama en la notacion Chen son representadas por un Rectangulo
![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/entidad.png?raw=true)

Las entidades representan las "cosas" importantes del mundo real sobre las que queremos guardar información. Piensa en ellas como sustantivos: personas, objetos, lugares, eventos o conceptos que son relevantes para el enunciado de la prueba en nuetro caso. Por ejemplo: 

* **En un Hospital ejemplos de entidades podrian ser**:

  * Entidad: Médico
  * Entidad: Paciente
  * Entidad: Cita
  * Entidad: Especialidad
  

* **En una Universidad ejemplos de entidades podrían ser**:

  * Entidad: Estudiante
  * Entidad: Profesor
  * Entidad: Asignatura
  * Entidad: Matrícula

---
### Atributos

Son representados por un ovalos y van unidos a las entidades que describen:

![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/ovalo.png?raw=true)

Los atributos son las características o propiedades que describen a una entidad. Son la información específica que queremos almacenar sobre cada "cosa".
![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/medico-atributos.png?raw=true)

En la foto de ejemplo de arriba se muestra una entidad Medico y los atributos que la describen, cabe recalcar que los atributos no siempre estan en el enunciado del ejericio cuando esto pasa nosotros debemos colocar los atributos que consideramos importantes para el funcionamiento de la base de datos por ejemplo en la creacion de una base de datos de un hospital atributos importantes serian los que aparecen en la imagen de arriba tambien podriamos agregarle un atributo edad. Atributos que no son importantes para el problema no los debemos agregar como por dar un ejemplo colocar un atributo a medico que guarde su partido politico no tendria nada que ver en una base de datos del hospital o Hobbie favorito. a lo que voy es que se deben colocar atributos que sean coherentes con el problema que estamos solucionando.



Tambien es importante decir que todas las entidades tienen una atributo que es la clave primaria, este atributo tiene la tarea de identificar a la entidad y es unico para cada entidad, en el diagrama se representa con un ovalo y una linea horizontal como esta

![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/primarykey.png?raw=true)

un ejemplo comun de clave primaria (tambien le dicen primary key en ingles) es el rut ya que es unico para cada persona, otro ejemplo de primary key seria para una entidad producto el Id_Producto (Este seria un identificador unico para cada producto ).

A veces los atributos de las entidades pueden tener diferentes valores supongamos que en el ejercicio del hospital tambien necesitamos  saber el numero del telefono del medico y este tiene diferentes numeros como podria ser un numero de celular personal, uno de telefono y un numero para la consulta, en este caso el atributo numero tendria multiples valores, a esto se le conoce como **Atributo multievaluado** y es representado por un doble ovalo.

 ![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/multiev.png?raw=true)
 teniendo esto en cuenta la entidad medico con sus atributos se veria asi:

 ![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/medico_multiev.png?raw=true)

En resumen los atributos son los valores que decriben a cada entidad y una entidad siempre lleva 1 atributo que es la clave primaria que sirve como identificador y se representa con un ovalo con una linea horizontal dentro y hay veces en que 1 atributo pueden tomar multiples a esto se le llama atributo multievaluado y se representa como un doble ovalo. 

---
## Relaciones

 Las relaciones muestran cómo las entidades interactúan o se conectan entre sí. Generalmente son verbos que describen una acción o asociación entre dos o más entidades en el problema que estamos modelando.

 Son representadas por un Rombo asi:

 ![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/rombo.png?raw=true)

 Un ejemplo de relacion seria esta 

 ![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/relacion-ejm.png?raw=true)

 otros ejemplos de relaciones podrian ser:

[Persona] ----- <**Tiene**> ----- [Pasaporte]

[Cliente] ----- <**Realiza**> ----- [Pedido]

[Estudiante] ----- <**Cursa**> ----- [Curso]

[Empleado] ----- <**Trabaja_en**> ----- [Proyecto]   

[Alumno] ----- <**Guiado_por**> ----- [Tutor]


Es importante decir que hay veces (no siempre) que el enunciado de la prueba requiere que  las relaciones entre dos entidades lleven atributos si bien no lo va a  decir explicitamente en el enunciado nosotros debemos inferir cuando una relacion tiene que llevar atributos, esto tiene el nombre de **Entidad asociativa** y esta representado por un rectangulo que lleva dentro un rombo asi:

![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/entidad_asociativa.png?raw=true)



Lo mejor es que chat gpt te explique lo que es la entidad asociativa:

A veces, la relación entre dos entidades es tan compleja o tiene información propia que no puede atribuirse a ninguna de las entidades participantes por sí sola. Cuando una relación tiene sus propios atributos, se convierte en una **entidad asociativa**.

Para representar esto en Notación Chen (o algunas de sus variantes), se usa:

* Un **rombo dentro de un rectángulo** (como describes).
* O un rombo con un rectángulo anidado en el medio.


**Ejemplo:** `Estudiante` **se inscribe en** `Curso`.

* Si solo te importa que un estudiante toma un curso, el rombo simple basta.
* Pero, ¿y si, al inscribirse, queremos guardar la **`Fecha_Inscripción`** o la **`nota final`** que obtuvo el estudiante en ese curso? Esos atributos (`Fecha_Inscripción`, `nota final`) no le pertenecen solo al `Estudiante` (porque el estudiante tiene otras inscripciones), ni solo al `Curso` (porque el curso tiene otros estudiantes). Pertenecen a la **inscripción específica** de *ese estudiante* en *ese curso*.

En este escenario, `Inscribe` se convierte en una entidad asociativa. Se representa con el rectangulo rombo y tiene sus propios atributos.

-
espero que con ese ejemplo de gepeto hayas entendido, visto de forma grafica la entidad asociativa entre estudiante y curso se veria asi: 

 ![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/ejemplo_entidad_asoci.png?raw=true)

quiero hacer un parentesis y aprovechar el ejemplo de la imagen de arriba para hablar de las **claves primarias compuestas**, si recuerdas, cuando hablamos de los atributos  habia uno que estaba representado por un ovalo y una linea horizontal que se llamaba **clave primaria** todas las entidades llevan una clave primaria,la clave primaria es el valor unico que identifica a cada entidad (como un rut en las personas) en este caso para que no se repita los valores de `Inscribe` y como `Inscribe` esta relacionado con estudiante y curso usamos las claves primarias de `Id estudiante` y `Id curso` como indentificador unico para `Inscribe` (como se ve en la imagen de arriba) esto tiene un nombre y se llama **clave primaria compuesta** osea que cuando una entidad tiene mas de 2 claves primarias la llamamos clave primaria compuesta, Aunque la clave compuesta es la forma "natural", también es posible (y a veces preferible por simplicidad o rendimiento en el modelo físico) asignar una **clave primaria artificial** a la entidad asociativa ¿Cómo? Simplemente se le añade un nuevo atributo, como un `ID_Inscripcion`, que se autoincrementa o genera de forma única.
Ejemplo: La entidad `Inscribe` podría tener un `ID_Inscripcion` propio, además de `ID_Estudiante` y `ID_Curso` (que serían claves foráneas a sus entidades originales). En este caso, `ID_Inscripcion` sería la clave primaria.

✨ **En resumen:** Las relaciones pueden ser **simples**, representadas por un **rombo**, o convertirse en **entidades asociativas** cuando el enunciado del ejercicio sugiere que la relación necesita **atributos propios**. En ese caso, se representan mediante un **rombo dentro de un rectángulo**.

--- 

## Lo que tenemos hasta ahora

Ya vimos los **3 elementos principales** del modelo conceptual según la Notación Chen:

1. **Entidades** → Representadas por rectángulos. Son los objetos o conceptos del mundo real sobre los que queremos guardar información (por ejemplo: Estudiante, Curso, Paciente).

2. **Atributos** → Representados por óvalos. Describen las características de las entidades (por ejemplo: nombre, edad, RUT).  
   - La **clave primaria** se subraya.
   - Si un atributo puede tener varios valores, se representa como un **doble óvalo** (atributo multivaluado).

3. **Relaciones** → Representadas por rombos. Indican cómo se conectan las entidades entre sí (por ejemplo: cursa, realiza, trabaja_en).  
   - Si la relación tiene atributos propios, se transforma en una **entidad asociativa**, representada por un **rectángulo con un rombo dentro**.

---

✨ **Recuerda:** Estos tres elementos nos permiten construir el "mapa" de cómo se organiza la información en un sistema, sin necesidad de pensar aún en tablas o código. pero existen otros 2 elementos importantes tambien que debemos tener en cuenta a la hora de crear un modelo conceptual: **Cardinalidad** y **Participacion**

### Cardinalidad
¿Qué es? Nos dice cuántas instancias de una entidad pueden asociarse con cuántas instancias de otra entidad a través de una relación. Es la "cantidad" de la relación(Se va a entender mejor mas abajo)

Símbolos en Chen: Se representan con números o letras (1, N, M) junto a las líneas que conectan la relación con las entidades.

**Tipos de cardinalidad:**

#### 1:1 (Uno a Uno): 
Una instancia de la Entidad A se relaciona con exactamente una instancia de la Entidad B, y viceversa.
**Ejemplo**: Un `Ciudadano` tiene un solo `Carnet`, y un `Carnet` pertenece a un solo `Ciudadano`. visto graficamente seria asi:

 ![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/1a1.png?raw=true)  
 nota: no le puse los atributos en las entidades porque me dio flojera, pero deberia llevar, igual lo que quiero que se fijen en el ejemplo de arria es en la cardinalidad.


#### 1:N (Uno a Muchos):
  una instancia de la Entidad A se relaciona con muchas instancias de la Entidad B, pero una instancia de la Entidad B se relaciona con solo una instancia de la Entidad A.
  
  La notación (min, max) se usará de la siguiente manera para N o M:

* (0,N) o (0,M): Cero a Muchos (opcional).
* (1,N) o (1,M): Uno a Muchos (obligatorio).
* 
Veamos ejemplos


  **Ejemplo 1: Departamento y Empleado**

* **Descripción:**
    * Un departamento tiene muchos empleados.
    * Un empleado pertenece a un solo departamento (en un momento dado).
* **Diagrama Conceptual (en texto):**

    ```
    +------------+         (1,1)     +-----------+     (0,N)         +----------+
    | Departamento |-------------------| Tiene     |-------------------| Empleado |
    +------------+                   +-----------+                   +----------+
    ```

    * **Interpretación:**
        * Cada `Departamento` **tiene** *uno y solo un* `Departamento` principal (el rombo se lee desde el punto de vista del Departamento).
        * Cada `Departamento` puede tener *cero o muchos* `Empleados` (desde la perspectiva del Departamento hacia el Empleado).
        * Cada `Empleado` **pertenece_a** *uno y solo un* `Departamento` (desde la perspectiva del Empleado hacia el Departamento).
        * Un `Empleado` puede estar sin `Departamento` temporalmente (`0` de participación mínima) o debe tenerlo (`1` si fuera `(1,1)` en ese lado). El ejemplo dado es para que un departamento debe tener al menos un empleado.

**Ejemplo 2: Cliente y Pedido**

* **Descripción:**
    * Un cliente puede realizar muchos pedidos.
    * Un pedido es realizado por un solo cliente.
* **Diagrama Conceptual (en texto):**

    ```
    +--------+         (1,1)     +---------+     (0,N)         +--------+
    | Cliente|-------------------| Realiza |-------------------| Pedido |
    +--------+                   +---------+                   +--------+
    ```

    * **Interpretación:**
        * Cada `Cliente` **puede realizar** *cero o muchos* `Pedidos`.
        * Cada `Pedido` **es_realizado_por** *uno y solo un* `Cliente`.

**Ejemplo 3: Autor y Libro**

* **Descripción:**
    * Un autor puede escribir muchos libros.
    * Un libro es escrito por un solo autor (para este ejemplo simplificado, asumimos un único autor principal).
* **Diagrama Conceptual (en texto):**

    ```
    +-------+         (1,1)     +-------------+     (0,N)         +-------+
    | Autor |-------------------| Escribe     |-------------------| Libro |
    +-------+                   +-------------+                   +-------+
    ```

    * **Interpretación:**
        * Cada `Autor` **puede escribir** *cero o muchos* `Libros`.
        * Cada `Libro` **es_escrito_por** *uno y solo un* `Autor`.

**Ejemplo 4: Categoría de Producto y Producto**

* **Descripción:**
    * Una categoría de producto puede contener muchos productos.
    * Un producto pertenece a una sola categoría.
* **Diagrama Conceptual (en texto):**

    ```
    +-------------------+         (1,1)     +-----------+     (0,N)         +---------+
    | Categoria_Producto|-------------------| Contiene  |-------------------| Producto|
    +-------------------+                   +-----------+                   +---------+
    ```

    * **Interpretación:**
        * Cada `Categoria_Producto` **contiene** *cero o muchos* `Productos`.
        * Cada `Producto` **pertenece_a** *uno y solo un* `Categoria_Producto`.

#### N:M (Muchos a Muchos): 

Una instancia de la Entidad A se relaciona con muchas instancias de la Entidad B, y una instancia de la Entidad B se relaciona con muchas instancias de la Entidad A.

La notación (min, max) se usará de la siguiente manera para N o M:

* (0,N) o (0,M): Cero a Muchos (opcional).
* (1,N) o (1,M): Uno a Muchos (obligatorio).
  
Veamos los ejemplos:

**Ejemplo 1: Estudiante y Curso**

* **Descripción:**
    * Un estudiante puede inscribir muchos cursos.
    * Un curso puede tener muchos estudiantes inscritos.
* **Diagrama Conceptual (en texto):**

    ```
    +-----------+         (0,N)     +-------------+     (0,M)         +-------+
    | Estudiante|-------------------| Inscribe    |-------------------| Curso |
    +-----------+                   +-------------+                   +-------+
    ```

    * **Interpretación:**
        * Cada `Estudiante` **inscribe** *cero o muchos* `Cursos`.
        * Cada `Curso` **es_inscrito_por** *cero o muchos* `Estudiantes`.
    * **Nota:** Esta relación `Inscribe` sería un candidato ideal para convertirse en una entidad asociativa (`Inscripción`) si necesitamos almacenar datos como `Fecha_Inscripcion` o `Calificacion`.

**Ejemplo 2: Película y Actor**

* **Descripción:**
    * Una película puede tener muchos actores.
    * Un actor puede participar en muchas películas.
* **Diagrama Conceptual (en texto):**

    ```
    +---------+         (1,N)     +-------------+     (0,M)         +-------+
    | Pelicula|-------------------| Actua_en    |-------------------| Actor |
    +---------+                   +-------------+                   +-------+
    ```

    * **Interpretación:**
        * Cada `Pelicula` **tiene** *uno o muchos* `Actores` (asumimos que una película debe tener al menos un actor).
        * Cada `Actor` **actúa_en** *cero o muchas* `Peliculas`.
    * **Nota:** La relación `Actua_en` podría ser una entidad asociativa (`Participacion`) si quisiéramos registrar el `Rol_Actor` en esa película, o `Fecha_Contrato`.

**Ejemplo 3: Usuario y Rol (de Sistema)**

* **Descripción:**
    * Un usuario puede tener muchos roles (por ejemplo, "Administrador", "Editor", "Visor").
    * Un rol puede ser asignado a muchos usuarios.
* **Diagrama Conceptual (en texto):**

    ```
    +--------+         (1,N)     +----------+     (0,M)         +------+
    | Usuario|-------------------| Asigna   |-------------------| Rol  |
    +--------+                   +----------+                   +------+
    ```

    * **Interpretación:**
        * Cada `Usuario` **tiene asignado** *uno o muchos* `Roles` (asumiendo que todo usuario debe tener al menos un rol).
        * Cada `Rol` **es_asignado_a** *cero o muchos* `Usuarios`.
    * **Nota:** `Asigna` también se convertiría en una entidad asociativa (`Asignacion_Rol`) si quisieras registrar la `Fecha_Asignacion` o si el rol es `Activo`/`Inactivo` para ese usuario en particular.

**Ejemplo 4: Profesor y Asignatura**

* **Descripción:**
    * Un profesor puede impartir muchas asignaturas.
    * Una asignatura puede ser impartida por muchos profesores (por ejemplo, un equipo de profesores o un profesor auxiliar).
* **Diagrama Conceptual (en texto):**

    ```
    +----------+         (0,N)     +-------------+     (0,M)         +-----------+
    | Profesor |-------------------| Imparte     |-------------------| Asignatura|
    +----------+                   +-------------+                   +-----------+
    ```

    * **Interpretación:**
        * Cada `Profesor` **imparte** *cero o muchos* `Asignaturas`.
        * Cada `Asignatura` **es_impartida_por** *cero o muchos* `Profesores`.
    * **Nota:** Esta relación `Imparte` podría convertirse en una entidad asociativa (`Enseñanza`) si quisiéramos registrar la `Carga_Horaria` del profesor en esa asignatura o el `Periodo_Academico` específico.

**Ejemplo 5: Pedido y Producto**

* **Descripción:**
    * Un pedido puede contener muchos productos.
    * Un producto puede estar incluido en muchos pedidos.
* **Diagrama Conceptual (en texto):**

    ```
    +--------+         (1,N)     +-----------+     (0,M)         +---------+
    | Pedido |-------------------| Contiene  |-------------------| Producto|
    +--------+                   +-----------+                   +---------+
    ```

    * **Interpretación:**
        * Cada `Pedido` **contiene** *uno o muchos* `Productos` (asumimos que un pedido tiene al menos un producto).
        * Cada `Producto` **es_contenido_en** *cero o muchos* `Pedidos`.
    * **Nota:** Esta relación `Contiene` siempre se convierte en una entidad asociativa (`Detalle_Pedido` o `Linea_Pedido`) para guardar la `Cantidad` de ese producto en ese pedido, el `Precio_Unitario_al_momento_del_pedido`, etc.




## Conclusión 

Bueno esos son casi todos los elementos del modelo conceptual hay otros pero la porfe no los menciono en clases asi que supongo que no vale la pena perder tiempo en estudiarlo, esta un poco enredada la cosa, me cuesta lo de cardinalidad, pero supongo que haciendo ejercicios dominaremos la cosa, despues de aprender lo de modelo conceptual hay que aprender a hacer el modelo logico y fisico, esos ultimos 2 son mas faciles segun chat gpt.

Para aprender te recomiendo que le digas a chat gpt esto:

"quiero aprender a hacer modelos conceptuales en notacion chen, muestrame un enunciado y resuelvelo paso a paso pero no me des nada de codigo, tu respuesta damela de forma escrita y complementala de forma visual con graficos para ayudarme a entender"

