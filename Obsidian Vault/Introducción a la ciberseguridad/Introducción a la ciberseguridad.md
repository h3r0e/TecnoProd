
Arpanet
Antecesor de internet.
El gobierno de los estados unidos tenían desplegado un sistema distribuido de comunicaciones que servía para fines militares. Tiempo después lo abren y se convierte en internet.


Modelo OSI:

![[Pasted image 20240925084251.png]]


1-) Capa física:
Trata con la parte física de la red. Gestiona la transmisión de bits (a través del medio físico).

2-) Capa de enlace:
Se encarga de entregar la información al medio físico y establecer una conexión fiable entre dos dispositivos directamente conectados. Controla el envío de "trames" sobre la red, asegurándose que los datos se transmiten correctamente y gestionando la detección de errores.

3-) Capa de red:
Se encarga de la conmutación y encaminamiento de paquetes de datos entre dispositivos situados en diferentes redes. En esta capa se definen las direcciones lógicas, como las direcciones IP, y se encarga de encontrar el mejor camino para enviar los datos desde el origen hasta el destino.

4-) Capa de transporte:
Garantiza que los datos se transmiten de manera fiable y en orden correcto entre los dispositivos de la red. Gestiona el establecimiento, mantenimiento y cierre de conexiones, así como la detección y corrección de errores.

El TCP controla como divide los paquetes un mensaje y como los envía.
Cuando enviamos un correo, este paquete se divide y se envía por diferentes vías de transmisión, las que encuentre mejores. Por lo que antes de que le llegue el correo al remitente, se vuelve a construir.

5-) Capa de sesión:
Se encarga de establecer, gestionar y finalizar las conexiones (o sesiones) entre dos dispositivos en comunicación. Esta capa coordina el dialogo entre los dispositivos, asegurándonos que se mantengan activos y gestionando la sincronización de los datos.

Protocolos asociados: NetBIOS, RPC (Remote Procedure Call).

6-) Capa de presentación:
Se encarga de normalizar (traducir, cifrar y comprimir) los datos para que el sistema receptor pueda interpretar los datos correctamente. Actúa como un traductor entre la capa de aplicación y el resto de capas inferiorees.

Protocolos asociados: SSL/TLS (para seguridad),  formatos de datos.

7-) Capa de aplicación:
Es donde los usuarios interactúan directamente con las aplicaciones. Proporciona servicios de red a las aplicaciones, como el envió de correos electrónicos, la navegación web o la transferencia de ficheros.

Protocolos asociados: HTTP/HTTPS, FTP, SMTP, DNS.

Cada vez que voy subiendo de nivel en el modelo de capa OSI. Tengo que poner información de a quien enviarle la información, de que forma, etc. Esto lo hacemos através de cabeceras.

Modelo TCP/IP:

![[Pasted image 20240925092838.png]]

Protocolos de comunicación:
Es un conjunto de reglas y normas que definen como dos o mas dispositivos o sistemas se comunican y intercambian datos en una red. Estos protocolos establecen como se han de transmitir, recibir y interpretar los datos, asegurando que los dispositivos involucrados puedan entenderse y coordinarse adecuadamente, incluso si se utilizan tecnologias o sistemas diferentes.

Protocolos de red:
* TCP/IP
* UDP

Protocolos de transporte:
* HTTP/HTTPS
* FTP

Protocolos de red local:
* Ethernet
* Wi-Fi
* Bluetooth

Protocolos de correo electrónico
* SMTP
* IMAP
* IPOP3

Protocolos de seguridad:
* SSL/TLS
* IPsec


Hardware de red

* Modem: convierte un tipo de señal a otra.
* Acces Point: permite conectar dispositivos sin cables.
* Adaptador de red: permite conectar dispositivos con cables (Ethernet o Fibra).
* Repetidor: reciben todo el transito, amplifican la señal y la regresan a la red sin entrar en su contenido. No tienen capacidad de enrutamiento ni conmutación. Trabajan únicamente en la capa física.
* Bridge: conecta dos segmentos de una red. Trabaja en la capa de enlace y puede analizar trazas. Almacena las direcciones MAC para saber que interfase tiene que enviar los paquetes. También pueden verificar el CRC y descartar trazas si hay errores.
* Switch: son la evolución de los bridge. Añade funcionalidades para lo que hace el direccionamiento de las trazas. Hay switches que analizan la capa de aplicación de forma que pueden implementar políticas y filtros. Trabaja dentro de una red de area local.
* Router

Los puertos inferiores a 1024 están reservados para servicios comunes.
* Puerto 21: FTP
* Puerto 22: SSH
* Puerto 80: HTTP
* Puerto 443: HTTPS

Los puertos superiores a a1024 se pueden utilizar para aplicaciones personalizadas o usos temporales.
* Base de Datos SQL
