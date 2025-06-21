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

### Atributos

Son representados por un ovalos y van unidos a las entidades que describen:

![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/ovalo.png?raw=true)

Los atributos son las características o propiedades que describen a una entidad. Son la información específica que queremos almacenar sobre cada "cosa".
![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/medico-atributos.png?raw=true)

En la foto de ejemplo de arriba se muestra una entidad Medico y los atributos que la describen, cabe recalcar que los atributos no siempre estan en el enunciado del ejericio cuando esto pasa nosotros debemos colocar los atributos que consideramos importantes para el funcionamiento de la base de datos por ejemplo en la creacion de una base de datos de un hospital atributos importantes serian los que aparecen en la imagen de arriba tambien podriamos agregarle un atributo edad. Atributos que no son importantes para el problema no los debemos agregar como por dar un ejemplo colocar un atributo partido politico no tendria nada que ver en una base de datos del hospital o Hobbie favorito. a lo que voy es que se deben colocar atributos que sean coherentes con el problema que estamos solucionando.



Tambien es importante decir que todas las entidades tienen una atributo que es la clave primaria, este atributo tiene la tarea de identificar a la entidad y es unico para cada entidad, en el diagrama se representa con un ovalo y una linea horizontal como esta

![alt text](https://github.com/Ren-reno/Prueba_F_Base_de_datos/blob/main/Imagenes/primarykey.png?raw=true)

un ejemplo comun de clave primaria (tambien le dicen primary key en ingles) es el rut ya que es unico para cada persona, otro ejemplo de primary key seria para una entidad producto el Id_Producto (Este seria un identificador unico para cada producto )