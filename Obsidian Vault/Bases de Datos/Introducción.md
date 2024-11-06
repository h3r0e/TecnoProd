# Qué son los datos?

Unidades de información que representan hechos, observaciones o conceptos concretos sobre el mundo real.

- Tipos de datos:
Números, textos, imágenes, sonidos o cualquier cosa registrable i procesable digitalmente en sistema binario.

- Interpretación de los datos
Los datos por si mismos no tienen significado completo hasta que no se organicen y se interpreten para convertirse en información útil. Es necesario proporcionar los datos en un contexto útil (metadatos).

Si nos dicen 4, 4 que?

Cuando tenemos datos y metadatos podemos extraer información útil y podemos obtener conocimiento. Y una vez tenemos conocimiento podemos actuar y operar con ellas.

- Ejemplo:
   - Datos: [05012024, 41.362, 2.157, Cynara cardunculus].
   - Metadatos: [Fecha con formato "ddmmaaaa", latitud, longitud, nombre científico de la especie identificada].
   - Informació: El 5 de enero de 2024 habia almenos una carxofera (planta) al Jardin Botánico de Barcelona.
   - Conocimiento: Las carxofas son una especie de interés.


# Entidades, Atributos y Valores

Tres elementos caracterizan fundamentalmente las informaciones:
- Entidades: son los objetos del mundo real que conceptualizamos. Son identificables, es decir, distinguibles unos de otros. I nos interesan algunas (como mínimo una) de sus propiedades.
- Los atributos son las propiedades de las entidades que nos interesan.
- Los valores son los contenidos concretos de los atributos, las determinaciones concretas que asumen.

- Ejemplo:
   - Entidad: Película
   - Atributos:
   - Valores:

Podemos distinguir entre dos tipos de entidades:
- La entidad tipo: se trata de un tipo genérico de entidad o, si se prefiere, de una abstracción, que hace referencia a una clase de cosas como, por ejemplo, los coches, en general.

- La entidad instancia: se refiere a una conceptualización de un objeto concreto del mundo real, como por ejemplo, un coche concreto, distinguible de otros objetos del mismo tipo, gracias a alguna propiedad (como podría ser el valor del atributo matrícula).

Los conceptos de entidad, atributos y valores son fácilmente reproducibles en una tabla.

- Tipos de datos:
Un tipo de dato define un conjunto de valores con unas características comunes que los hacen compatibles, por lo que también define una serie de operaciones admisibles sobre estos valores.

Si el atributo es un nombre entero (diferentes a los nombres reales o los caracteres), se pueden definir ciertas operaciones como la suma, la resta, multiplicación y división entera especificas para este tipo de datos.

- Dominio:
Llamamos dominio a todo el conjunto de valores que un atributo determinado puede tomar válidamente.

   - Ejemplo:
Si el atributo es la edad de una persona, todos las edades negativas estarían fuera del Dominio.

* Nulo
A veces, el valor de un atributo es desconocido o, hasta puede no existir. Para representar esta circunstancia, el atributo en cuestión tendrá que admitir el valor nulo a su Dominio.

- Atributos identificadores y claves
Atributo identificador: es el que permite identificar inequívocamente cada entidad instancia del resto, por lo que su valor es único. No se repite en diferentes entidades instancia. 

A veces, un único atributo no es suficiente para identificar una instancia.
Ejemplo: nombre y apellido.

Todo atributo o conjunto de atributos que permiten identificar inequívocamente las instancias de una entidad se llama clave.


# Qué es una base de datos?

Una base de datos es un conjunto de datos relacionadas entre sí, almacenadas y organizadas en un sistema físico mediante una estructura de datos que permite la consulta y la modificación de datos.

Ejemplo: un libro. 

En un sistema informático las bases de datos están almacenadas en una memoria externa (Disco Duro, SSD) que nos permite almacenar los 0 y 1. Y también existen bases de datos que trabajan en la memoria interna (RAM).

La estructura de datos hace referencia a la organización física de los datos y como se producen el acceso a estos: árbol, grafo, tabla, etc.

Las bases de datos se diseñan para cumplir los requisitos informáticos de una empresa, organización o conjunto de usuarios que quieran acceder al mismo conjunto de datos.

- Definición de Interrelación
Las interrelaciones son informaciones que permiten asociar las entidades entre ellas.

Las bases de datos contienen datos y metadatos. Es importante mantener los metadatos junto con los datos por varios motivos:

- **Organización**: facilitan la búsqueda y recuperación de información específica.
- **Contexto:** proporcionan información sobre como se crean los datos, quien las creó y cuando.
- **Interoperabilidad:** permiten que los datos sean entendidas y utilizadas por diferentes sistemas y aplicaciones ya que contienen información sobre la estructura de los datos y las interrelaciones.


Como se almacenan los datos?
- Nivel lógico
- Nivel físico

- SGBD:
Es un tipo de programa que tiene como finalidad la gestión y control de las BBDD.

Todos los SGBD tienen una serie de objetivos y ofrecen una serie de funcionalidades:
- Posibilitar las consultas no predefinidas de cualquier complejidad.
- Garantizar la independencia física y la independencia lógica de los datos.
- Evitar o solucionar los problemas derivados de la redundancia.
- Proteger la integridad de los datos.
- Permitir la concurrencia de usuarios.
- Contribuir a la seguridad de los datos.

- Arquitectura y componentes del SGBD:
1-) Los ficheros como a bases de datos.
2-) Evolución de los SGBD.