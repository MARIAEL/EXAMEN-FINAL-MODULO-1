EXAMEN FINAL MÓDULO. ADMINISTRACIÓN DE SERVICIOS WEB. 16/2/2015  
MARIA ELVIRA MIRALLES I ALBERO  


##1.-Definir los siguientes términos: FTP, FTPS, SFTP  

**FTP.-**  

FTP ( File Transfer Protocol,) es un Protocolo de Transferencia de Archivos.   
Es un protocolo de red para la transferencia de archivos entre sistemas conectados a una red TCP (Transmission Control Protocol), basado en la arquitectura cliente-servidor.   
Desde un equipo cliente se puede conectar a un servidor para descargar archivos desde él o para enviarle archivos, independientemente del sistema operativo utilizado en cada equipo.  
Un problema básico de FTP es que está pensado para ofrecer la máxima velocidad en la conexión, pero no la máxima seguridad, ya que todo el intercambio de información, desde el  login y password del usuario en el servidor hasta la transferencia de cualquier archivo, se realiza en texto plano sin ningún tipo de cifrado, con lo que un posible atacante puede capturar este tráfico, acceder al servidor y/o apropiarse de los archivos transferidos.  
Para solucionar este problema son de gran utilidad aplicaciones como scp y sftp, incluidas en el paquete SSH, que permiten transferir archivos pero cifrando todo el tráfico.  

**FTPS.-**  

Es un protocolo que se utiliza para abarcar un número de formas en las cuales el software FTP (FTP Secure) puede realizar transferencias de ficheros seguras.   
Cada forma conlleva el uso de una capa SSL/TLS debajo del protocolo estándar FTP para cifrar los canales de control y/o datos.   
FTPS no debe ser confundido con el SFTP (SSH File Transfer Protocol) que es un subsistema para transferencia de archivos seguros con protocolo SSH (Secure Shell).  

**SFTP.-**  

SFTP (Secure File Transfer Protocol), es el mismo sistema de protocolo, solo que los datos viajan cifrados por SSH. Si transferimos información por este protocolo, tendremos la seguridad de que aunque estuvieran “esnifando” tráfico en nuestra red, todo lo que encontrarían serían datos cifrados.  
La ventaja que tiene es que nos da la seguridad de que todo lo que se transfiere no es interceptado por nadie.
Por el contrario, la velocidad baja considerablemente. No es recomendable para descargas o subidas de archivos grandes.  
SFTP no se debe confundir con el Protocolo simple de transferencia de archivos , que es un intermediario sin cifrar entre FTP y TFTP.  


##2.-Qué es un CMS? Enumera los más populares. Ventajas del uso de un CMS.  

**CMS** (Content Management System), es un sistema de gestión de contenidos.  
Es un programa informático que permite crear una estructura de soporte (framework) para la creación y administración de contenidos, principalmente en páginas web, por parte de los administradores, editores, participantes y demás usuarios.  
Consiste en una interfaz que controla una o varias bases de datos donde se aloja el contenido del sitio web. El sistema permite manejar de manera independiente el contenido y el diseño. Así, es posible manejar el contenido y darle en cualquier momento un diseño distinto al sitio web sin tener que darle formato al contenido de nuevo, además de permitir la fácil y controlada publicación en el sitio a varios editores.  
Un ejemplo clásico es el de editores que cargan el contenido al sistema y otro de nivel superior (moderador o administrador) que permite que estos contenidos sean visibles a todo el público (los aprueba).  

**Los más populares son:**  

*WordPress*: Convertido en un potente CMS por derecho propio en las últimas versiones y sin duda, el más popular.   

*Joomla*: Uno de los más populares disponibles para medianos y grandes sitios que necesitan más flexibilidad y características.  

*Drupal*: Muy sólido, es conocido por su alta estabilidad y soportar alto tráfico con muy pocos problemas.  

*Blogger*: Una plataforma de blogs sencillo para las personas que sólo quieren crear un blog rápido.  

*Processwire*: Es de código abierto, escrito en PHP (5.3+).  

*Bootstrap*: Su particularidad es la de adaptar la interfaz del sitio web al tamaño del dispositivo en que se visualice.

**Ventajas del uso de un CMS:**  

*Uso sencillo*: No es necesario saber programar para publicar y gestionar contenido dinámico o estático.  

*Personalizable*: Suelen ser sistemas con un alto grado de personalización: Desde el diseño de la web hasta nuevas funcionalidades y opciones.  

*Escalable*: Uno de los puntos fuertes de los CMS son los plugins o módulos que podremos añadir en cualquier momento y pueden significar una nueva funcionalidad.    

*Seguridad*: Actualizaciones de seguridad frecuentes, protocolos de encriptación de información sensible y buen entendimiento con las opciones de seguridad del propio servidor.  

La gran ventaja de estos CMS es que solo debes contar con los servicios de un programador en el momento de creación y lanzamiento de una web con CMS. Desde ese  momento, el usuario es quien añade, borra o modifica todo el contenido de la web, con el ahorro en horas de programación que eso supone.  

##3.-Existen varias técnicas para optimizar el rendimiento de una web ¿en qué consisten los siguientes? Optimización de imágenes, cache de contenidos y compresión de ficheros.

**Optimización de imágenes**  

Es importante preocuparse por el tamaño de las imágenes que subimos a una web por varios motivos:  
- Los usuarios móviles agradecerán que nuestra web no tarde demasiado en cargar.  
- No perder usuarios por tener una web lenta y pesada.  
- Google dispone de un tiempo limitado para rastrear tu web, por lo que cuanto menos pese, más páginas podrá rastrear y tendremos más posibilidades de posicionar mejor.  
Lo primero es saber elegir el formato de imagen adecuado a nuestras necesidades. Por lo que vamos a ver cuándo es mejor utilizar un formato u otro:  

*.GIF*  
Un formato obsoleto, prácticamente solo se utiliza ya para imágenes animadas.  

*.PNG*  
El sustituto de Gif, porque también permite transparencia. Es ideal para imágenes planas o con grandes espacios blancos, como capturas de pantalla, logotipos, etc. PNG es un formato de imagen sin pérdidas, por lo que aunque no reduce tanto el tamaño como el JPG, la calidad siempre será mayor.  

*.JPG*  
Ideal para fotografías con detalles y muchos colores. Es un formato de compresión con pérdidas, es decir, que pierde calidad para reducir el tamaño, y con ello pierde nitidez, por lo que pueden aparecer aberraciones cromáticas en determinadas zonas.  

 RESUMEN: En general usaremos PNG para todas las imágenes que componen nuestra web (logotipos, iconos, botones…) y JPG solo para las fotografías, sobre todo las grandes.  

Además de estos, cada vez es más normal utilizar formatos vectoriales (.EPS o .SVG) para logotipos e iconos, ya que son totalmente escalables a todas las resoluciones.  

**Caché de contenidos**  

Veamos en primer lugar estos conceptos:  

La *caché de disco* (Disk cache o Cache buffer en inglés) es una porción de memoria RAM asociada a un disco con la utilidad de almacenar los datos recientemente leídos y por lo tanto agilizar la carga de los mismos en caso de que estos vuelvan a ser solicitados.  
Se llama *caché web* a la caché que almacena documentos web (es decir, páginas, imágenes, etcétera) para reducir el ancho de banda consumido, la carga de los servidores y el retardo en la descarga. Un caché web almacena copias de los documentos que pasan por él, de forma que subsiguientes peticiones pueden ser respondidas por el propio caché, si se cumplen ciertas condiciones.  
Hay una gran variedad de soluciones sencillas que aumentan drásticamente la velocidad de nuestros sitios web. Una implementación sencilla, barata y efectiva es la de colocar un acelerador cache delante del servidor web.  
La función de estos aceleradores es la de recibir peticiones HTTP, realizar la solicitud al servidor web y cachear los contenidos devueltos (imágenes, vídeos,…) en su caché interna que incorpora para futuras peticiones. De esta forma, cuando se solicite información que esté almacenada en memoria o «cacheada», no acudirá al servidor web, sino que la recuperará directamente desde la caché.  
De esta manera, conseguimos reducir la carga, las llamadas a la base de datos y al servidor web.  Como el contenido está en memoria, éste se muestra muy rápidamente y no necesitamos acudir al disco.   
Hay muchos aceleradores caché como por ejemplo  Varnish.  

**Compresión de ficheros.**  

La compresión de ficheros se utiliza básicamente con el fin de reducir el espacio ocupado por los mismos en nuestros discos y en la transferencia de archivos entre ordenadores. Este sistema también permite encriptar la información como medida de seguridad.  
Al ser más pequeño el tamaño de los ficheros, el tiempo de transferencia es menor y las redes no se saturan tanto. Este es el motivo por el que casi todos los ficheros que encontremos en la red estarán comprimidos, y para poder utilizarlos deberemos descomprimirlos.  
Existen varias técnicas de compresión, y para cada una de ellas programas que nos permiten comprimir/descomprimir los ficheros. En Internet existe un consenso bastante generalizado en utilizar sólo algunos formatos y en identificar cada uno de ellos añadiendo al final del nombre un atributo (denominado extensión) de la forma .xxx que nos indicará con que aplicación debemos descomprimir el fichero que deseamos (por ejemplo PKZip y WinZip).  

##4.-Describe qué son J2EE, .NET  

Se trata de dos lenguajes de programación.  

**J2EE** (Java 2 Platform Enterprise Edition) es, según Sun Microsystems, un conjunto de especificaciones que permiten el desarrollo de aplicaciones basadas en la tecnlogía Java.  

**.NET** es, según Microsoft, una plataforma de desarrollo de servidores, clientes y servicios.

**Sus principales diferencias** son:  

*Sintaxis*: Java es el que mejor sintaxis tiene,   

*Curva de aprendizaje*: ASP.NET es bastante sencillo y J2EE el más complicado de aprender.  

*Velocidad de desarrollo*: ASP.NET es el más rápido. J2EE es el más lento.  

*Plataforma*: ASP.NET es Windows y J2EE trabaja bien en cualquier plataforma.  

*Base de datos*: Oracle para J2EE y MSSQL para ASP.NET.  

*IDE* (Integrated Development Environments): ASP.NET tiene Visual Studio que es una gran aplicación, pero de coste elevado. J2EE tiene varias herramientas comerciales, pero Eclipse es la mejor (incluso alguna de las comerciales como WASD está basada en Eclipse).  

*Soporte orientado a objetos*: J2EE y ASP.NET son los mejores.  

*Seguridad*: J2EE parece el más seguro. ASP.NET tiene mala fama debido a fallos de seguridad debidos a Windows.  

*Rendimiento*: J2EE es más pesado, parecido a ASP.NET.  

*Servidor Web*: ASP.NET solo funciona con IIS,  J2EE tiene versiones comerciales y open source.  

*Librerías y frameworks*: los dos tiene muchas librerías y frameworks disponibles.  

*Soporte y comunidad*: para ASP.NET la mayoría de los foros, grupos de usuarios y comunidades de desarrolladores están manejados por Microsoft, mientras que para J2EE existen muchos grupos independientes.  

*Coste*: ASP.NET tiene licencias bastante caras, mientras que J2EE puede desarrollarse con herramientas gratuitas y de pago.   

##5.-Definir Oracle, Mysql  

**Oracle Database** es un sistema de gestión de base de datos objeto-relacional desarrollado por Oracle Corporation.
Se considera a Oracle Database como uno de los sistemas de bases de datos más completos, destacando por su soporte de transacciones, estabilidad,escalabilidad y soporte multiplataforma.  

**MySQL** es un sistema de gestión de bases de datos relacional, multihilo y multiusuario con más de seis millones de instalaciones.  Sun Microsystems  desarrolla MySQL como software libre en un esquema de licenciamiento dual.  

##6.-Qué son y para qué sirven las cookies  

**Una cookie  es** una pequeña información enviada por un sitio web y almacenada en el navegador del usuario, de manera que el sitio web puede consultar la actividad previa del usuario. Es un apunte que un sitio web guarda en tu navegador. Su aspecto es el de un pequeño archivo de texto.  

**Sus principales funciones son:**  

1.- *Llevar el control de usuarios*: cuando un usuario introduce su nombre de usuario y contraseña, se almacena una cookie para que no tenga que estar introduciéndolas para cada página del servidor. Sin embargo, una cookie no identifica solo a una persona, sino a una combinación de computador-navegador-usuario.  

2.- *Conseguir información sobre los hábitos de navegación del usuario*, e intentos de spyware (programas espía), por parte de agencias de publicidad y otros. Esto puede causar problemas de privacidad y es una de las razones por la que las cookies tienen sus detractores.  

##7.- Qué es un servidor proxy  

Un servidor proxy, en una red informática, es un servidor que sirve de intermediario en las peticiones de recursos que realiza un cliente a otro servidor.  
El servidor proxy es un ordenador que intercepta las conexiones de red que un cliente hace a un servidor de destino.  
Esta situación estratégica de punto intermedio suele ser aprovechada para soportar una serie de funcionalidades:   control de acceso, registro del tráfico, prohibir cierto tipo de tráfico, mejorar el rendimiento, mantener el anonimato, proporcionar Caché web, etc; este último sirve para acelerar y mejorar la experiencia del usuario mediante permisos que guardará la web, esto se debe a que la próxima vez que se visiten las páginas web no se extraerá información de la web si no que se recuperara información de la cache.  

##8.-Indicar el porcentaje de agujeros de seguridad aparecidos para los SO: Windows, Mac y Linux  

Un agujero de seguridad, afecta a todos los datos que se envían encriptados –es decir, supuestamente, de forma segura- en Internet.  

El porcentaje para los sistemas operativos indicados es:  

Windows:  92.05%  
Mac:  6.39%  
Linux: 1.56%  

##9.- Indicar las 5 vulnerabilidades principales de las aplicaciones web.  

Las cinco vulnerabilidades principales de las aplicaciones web son las siguientes:  

**1 – Inyecciones**  

Vulnerabilidades de inyección de código, desde SQL o comandos del sistema hasta LDAP, ocurren cuando se envían datos no confiables a un intérprete como parte de un comando o consulta.  

**2 – Pérdida de autenticación y gestión de sesiones**  

Comprende los errores y fallos en las funciones de gestión de sesiones y autenticación. Se produce cuando las funciones de la aplicación relacionadas con la autenticación y la gestión de sesiones no se implementan correctamente, lo que puede permitir a los atacantes comprometer contraseñas, claves, token de sesiones, o explotar otros problemas que podrían permitir asumir la identidad de otros usuarios.  

**3 – Secuencias de comandos en sitios cruzados (XSS)**  

Permite a una tercera parte inyectar en páginas web vistas por el usuario código JavaScript o en otro lenguaje script similar, evitando medidas de control.  

**4 – Referencias directas inseguras a objetos**  

Errores al exponer partes privadas o internas de una aplicación sin  control y accesibles públicamente. Ocurre cuando un desarrollador expone al exterior una referencia a un objeto de implementación interno, tal como un fichero, directorio, o base de datos.  

**5 – Configuración de seguridad incorrecta**  

Más que un error en el código se trata de la falta o mala configuración de seguridad de todo el conjunto de elementos que comprende el despliegue de una aplicación web, desde la misma aplicación hasta la configuración del sistema operativo o el servidor web. Es decir, se refiere a la definición e implementación de una configuración segura para la aplicación, marcos de trabajo, servidor de aplicación, servidor web, base de datos y plataforma. Todas estas configuraciones deben ser definidas, implementadas y mantenidas, ya que por lo general no son seguras por defecto. Esto incluye mantener todo el software actualizado, incluidas las librerías de código utilizadas por la aplicación.  

















