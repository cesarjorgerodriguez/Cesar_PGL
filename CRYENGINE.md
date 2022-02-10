CRYENGINE


![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/Logo.png)


César Jorge Rodríguez


Índice:

1.- Introducción
2.- Empezar a usar CryEngine.
3.- Ventajas y desventajas.
4.- Requisitos mínimos para poder usar la herramienta.
5.- Ejemplo que he realizado.
6.- Conclusión.














1.- Introducción

¿Qué es CryEngine? Pues un motor de videojuegos lanzado en 2002 creado por un estudio alemán llamado Crytek. Actualmente van por su versión 5. Y fue lanzado originalmente para hacer una demo técnica para la empresa de tarjetas gráficas Nvidia.  Tras el buen resultado acabaron desarrollando Far Cry los mismos creadores del motor.

Programado en Lua, C++ y C#, este gran motor cuenta con importantes desarrollos y mucho apoyo a los desarrolladores indies. 

Cuenta con una comunidad muy activa, documentación para aburrir (en inglés), infinidad de videotutoriales en la web oficial de Youtube así como creación de escenarios, diseños de niveles, etc... Una programación mediante nodos parecida a Unreal para terminar con cinemáticas, efectos de sonido y partículas de alta calidad.

















2.- Empezar a usar CryEngine

Antes de empezar a usar CryEngine debemos registrarnos en la página oficial como usuario ya que sino, no nos será posible usar el programa, una vez hecho, podremos instalarlo. El primer paso para ello es elegir la ruta de instalación:

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/Install1.png)

A continuación nos aparecerá otra ventana en la que simplemente tenemos que clicar en install.

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/Install2.png)

Con esto ya empezará a instalarse, tenemos que esperar a que la barra de progreso acabe para continuar.

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/Install3.png)

Por último nos aparecerá un mensaje indicándonos que la instalación ha acabado y la opción de darle a finish estará disponible.

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/Install4.png)

Lo primero que vemos al iniciar el programa es esta ventana:

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/VentanaPrincipal.png)

Podremos observar que la ventana se compone de una barra superior con el logro de cryengine y 3 pestañas, la primera es la librería donde podremos buscar nuestros proyectos, assets/activos, engines (versiones del motor entre la cuales tendremos que elegir para usar), y envíos que sería algo así como un repositorio del propio cryengine de uso público.

La segunda como su nombre indica son las news/noticias que van saliendo sobre nuevas actualizaciones de cryengine y sus cambios.

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/MenuContent.png)

La tercera es el marketplace que contiene dos links a internet, uno lleva a una pestaña en la web donde habrá muchísimas categorías de productos que podremos descargar, desde plugins hasta modelos 3d, algunos componentes son de uso gratuito y otros no. 

El otro link nos redirige a una guía para informarnos sobre cualquier duda que tengamos y algunos puntos claves sobre el tipo de contenido, sonido y gráficos de los assets.


Fijándonos en la parte central del menú, podremos crear, importar o recargar los proyectos. La recomendación de instalar la versión de cryengine más actual.

Tres botones que nos redireccionará a los foros de usuarios, tutoriales y documentación.

Por último una versión reducida de las últimas noticias sobre cryengine.

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/MenuContent.png)

(Importante, si queremos crear un proyecto es necesario tener una versión del motor instalada, junto con unas librerías y otros programas necesarios entre ellos uno para hacer debugging, todo esto es pedido cuando clicamos en “+new”).





3.- Ventajas y desventajas.

Ventajas:
Gran capacidad gráfica.
Funcionalidad y herramientas.
El mejor editor de terreno.
Optimización.
Bueno para triple AAA.


Desventajas:
Interfaz y herramientas más complejas.
Documentación menos accesible.
No recomendado para inexpertos.

4.- Requisitos mínimos para poder usar la herramienta.

Requisitos mínimos:
Sistema operativo: Windows Vista SP1, Windows 7, Windows 8.1 (64 bit) o 10.
Procesador: Intel Dual-Core 2GHz o AMD Dual-Core 2GHz
Memoria: 4 GB de RAM
Gráficos: NVIDIA GeForce 400 series o AMD Radeon HD 6000 series
DirectX: Versión 11
Almacenamiento: 8 GB de espacio disponible
Requisitos recomendados:
Sistema operativo: Windows 7, Windows 8.1 (64-bit) o 10.
Procesador: Intel Quad-Core (i5 2300) o AMD Octo-Core (FX 8150)
Memoria: 8 GB de RAM
Gráficos: NVIDIA GeForce 660Ti o superior, AMD Radeon HD 7950 o superior
DirectX: Versión 11
Almacenamiento: 8 GB de espacio disponible


5.- Mi ejemplo.

Dentro de nuestro proyecto una vez creado, he ido a la pestaña de new file y seleccionando un nuevo nivel, al cual le he puesto el nombre de nivelUno. 

Una vez creado el nivel nos preguntará las dimensiones de este y la calidad de las texturas.

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/NewLevel.png)

Yo me he decidido por el nivel más pequeño posible que es de 128x128 pero con una calidad de texturas bastante alta.

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/CreadoProyecto.png)

Cuando lo tengamos se nos queda algo tal que así.

Lo siguiente que he hecho es ir a tools, para poner en mi interfaz las herramientas de creación de terreno y vegetación.

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/Tools.png)

Después con la herramienta de edición de terreno he ido a file y le damos a generate terrain que nos mostrará esta ventana:

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/TerrainEditor.png)

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/TerrainGeneration.png)

y en la opción de feature size lo he bajado a 3.2 lo que al darle a ok, me ha formado 2 montañitas que parecen unas pequeñas islas.

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/Isla1.png)

En el menú de las herramientas de cambiar terreno tenemos varias como la de “flatten” que sirve para igualar el terreno, Raise/lowe para elevar o bajar el terreno, y “smooth” para suavizar las elevaciones.



Aplicando estas herramientas he hecho algo tal que así:

![](https://github.com/cesarjorgerodriguez/Cesar_PGL/blob/main/imgCryEngine/Isla2.png)

A partir de aquí me da pereza explicar cada paso que hago para crear la isla pero bueno, es simplemente utilizar las opciones que tengo de los menús de herramientas que dije antes.

Además que con la versión de CryEngine tal cual sin descargar plugins etc. Tenemos poca cosa con la que trabajar en el sentido de usar tipos de texturas…objetos, etc…


6.- Conclusión.

Como ya he descrito en las desventajas es una herramienta con muchísimas opciones lo que requiere de mucho tiempo para aprender a trabajar con cryengine como es debido, teniendo esto en cuenta, la herramienta me parece muy buena, lo poco que he podido aprender una vez lo pones en practica ya te abre un montón de posibilidades a la hora de querer hacer un juego. 

Otra cosa es el tema de la gran comunidad que tiene este motor y que si tu fuerte no es el crear texturas, shaders etc. Es posible con un click y comprarlo a un precio barato obtener carpetas y carpetas de estos.
