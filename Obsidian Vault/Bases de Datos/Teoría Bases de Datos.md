Jueves 19/09/2024

1950: Sistemas de ficheros (Analógico)

1960: BBDD jerárquicas en forma de arbol

1970: E. F. Cono trabajador de IBM, inventa el modelo relacional. Al principio no es muy eficiente pero las grandes empresas optimizan este sistema con el tiempo.

1990: OLAP. Permite expandir una capa más.

2000: Se inventa el modelo noSQL de bases de datos distribuidas.


- Niveles de abstracción
No es necesario que todos las personas de una organización tengan acceso a todos los datos que almacena la BBDD.

Por ello, los datos se clasifican en tres niveles de abstracción:

1- Nivel físico
2- Nivel lógico
3- Nivel de vistas

- Ficheros
Antiguamente se trabajaba con un fichero maestro donde habían datos. Y si tenías varias aplicaciones se duplicaba ese fichero maestro y se creaba un nuevo fichero para cada aplicación.

Esta forma de trabajar presentaba varias desventajas:

1-) Datos dispersos
2-) Consultas ineficientes: hay que buscar la manera de hacer una consulta al fichero. Porque no había una manera predefinida para hacerlo.

- Ficheros vs BBDD (Comparación)

- Objetivos de SGBD
-Posibilitar las consultas no predefinidas de cualquier complejidad.
-Garantizar la independencia física y lógica de los datos.
-Evitar o solucionar problemas derivados de la redundancia.

- Consultas predefinidas
Un SGBD proporciona un lenguaje para realizar consultas y aislar los datos necesarios por el usuario.

- Ejemplo de consulta:
SELECT
FROM
WHERE
ORDER BY ... ASC/DESC;

- Independencia de datos
Es un concepto importante de los sistemas de gestión de bases de datos (SGBD) que se refiere a la capacidad para cambiar la estructura física o lógica de los datos sin afectar a la aplicación que utiliza estos datos. Se divide en dos tipos:

1-) Independencia física de los datos
2-) Independencia lógica

- Independencia física
Se refiere a la capacidad para cambiar la manera en que los datos están almacenadas físicamente en el disco (por ejemplo, cambios en la estructura de almacenamiento) sin afectar a la manera en que los datos son accesibles lógicamente por los usuarios y aplicaciones.

En los SGBD los cambios en la organización física como la reorganización de los registros de datos en el disco duro, no afectan a las aplicaciones que hacen uso de estos datos.

- Independencia lógica
Se refiere a la capacidad de modificar la estructura lógica de los datos (por ejemplo, agregando o eliminando tablas o columnas, cambiar la relación entre los datos, etc) sin afectar a la aplicación que utiliza estos datos. 

En los SGBD, algunos cambios sobre el esquema lógico (como añadir una nueva tabla o añadir una columna) se pueden efectuar sin necesidad de modificar el código de la aplicación que accede a estos datos. 

Los SGBD están diseñados para facilitar la independencia lógica de los datos, pero no se puede garantizar al 100% en todos los casos.


- Redundancia
Consiste en la repetición indeseada de datos, que incrementan los riesgos de perdida de integridad de estas cuando se actualizan.

Son datos íntegros los datos que se mantienen completas y correctas.

La repetición de datos es ineficiente para el almacenamiento de estas ya que ocupan más espacio. No obstante, a veces es necesario tener cierta repetición para garantizar la seguridad, el acceso a estos datos o para reducir costes de comunicación.

Otro tipos de duplicidad admisible son los **datos derivados** que se obtienen a partir de cálculos con datos ya presentes en la BD.

Los SGBD se encargan de administrar debidamente la repetición de los datos y en el caso de los datos derivados, actualizarlos cuando los datos primitivos de los cuales dependen cambien.

Además de la redundancia, hay muchos otros motivos que pueden hacer mal bien a la integridad de los datos.

-Erros humanos
-Deficiencias (Bugs)
-Averías de los soportes físicos de almacenamiento
-Transacciones incompletas como consecuencias de una interrupción del subministro eléctrico.

Los SGBD protegen la integridad de los datos en estos casos, haciendo servir **reglas de integridad** y sistemas de restauración basados en **copias de seguridad**.

- Reglas de Integridad
El sistema valida automáticamente ciertas condiciones al producirse una actualización de datos.

Las reglas de integridad pueden ser de dos tipos:

1-) Restricciones del modelo: reglas inherentes al modelo de datos que utiliza el SGBD. El sistema las incorpora predefinidas y siempre se cumplen.

2-) Restricciones del usuario: son reglas predefinidas poro el usuario (administradores, diseñadores..) de la BD, que no incorpora de serie el SGBD. Y que sirven para modelizar aspectos específicos del mundo real.

Los SGBD también proporcionan herramientas para realizar periódicamente copias de seguridad que permiten restaurar los datos en un estado consistente.

Los valores restaurados se corresponderán con los que había en el momento que se realizó la copia de seguridad. Antes del incidente que originó la restauración. Por lo tanto no estarán del todo actualizadas, aunque sean correctas.

- Concurrencia de usuarios
La concurrencia de usuarios en una BD consiste en el acceso simultaneo a la BD por parte de más de un usuario.

Existen dos tipologías de accesos concurrentes, con problemas diferentes:

1-) Accesos de consulta de datos. Pueden provocar problemas de rendimiento, derivados sobre todo de las limitaciones de los soportes físicos disponibles.

2-) Accesos de modificación de datos: Las peticiones simultaneas de actualización de unos mismos datos pueden provocar problemas de interferencia que tengan como consecuencia la obtención de datos erróneos y perdida de integridad de la BD.

Para tratar correctamente los problemas derivados de la concurrencia de usuarios, los SGBD utilizan fundamentalmente dos técnicas:

1-) Transacciones
2-) Bloqueos

- Transacciones
Una transacción consiste en un conjunto de operaciones simples que deben ejecutarse como una unidad. 

**COMMIT y ROLLBACK** 

La instrucción COMMIT indica, en el SGBD, que un conjunto de operaciones determinado debe ejecutarse de manera transaccional. La operación ROLLBACK deshace los cambios producidos en caso de que las operaciones de una transacción se hayan ejecutado parcialmente.

- Bloqueos
Se puede dar la situación en que diferentes transacciones quieran acceder a la BD simultáneamente. En estos casos, aunque cada transacción, individualmente considerada, sea correcta, no se podría garantizar la consistencia de los datos si no fuera por el uso de la técnica del bloqueo.

- Seguridad de los datos

La expresión seguridad de los datos hace referencia a su confidencialidad. A menudo, el acceso a los datos no debe ser libre o, como mínimo, no debe serlo totalmente. 

Los SGBD deben permitir definir autorizaciones de acceso a las BD, estableciendo permisos diferentes en función de las características del usuario o del grupo de usuarios. 

Actualmente, los SGBD permiten definir autorizaciones a diferentes niveles: 

● Nivel global de toda la BD 
● Nivel de entidad 
● Nivel de atributo 
● Nivel de tipo de operación

- Encriptación
Otro aspecto a tener en cuenta es la encriptación. Muchos SGBD ofrecen esta posibilidad.

Las técnicas de encriptación permiten almacenar la información utilizando códigos secretos que no permiten acceder a los datos a personas no autorizadas y que, por tanto, no disponen de dichos códigos.

La encriptación puede provocar una perdida de rendimiento en el acceso a los datos, ya que comporta la utilización de algoritmos adicionales en las operaciones de consultas.



