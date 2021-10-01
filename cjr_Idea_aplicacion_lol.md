**Alumno:** César Jorge Rodríguez.**Curso:** 2º Desarrollo de aplicaciones multiplataformas.**Asignatura:** Aplicaciones multimedia y dispositivos móviles.

![img](https://lh6.googleusercontent.com/lxyQ3fp_IMzG_mvKiMU6ZHwwZo2et5oeYAyBX3FrSDJuupuEMh3BqekPeptXN6HrzHB-7Msal_n4zqx81tfX0uc3zSnbkPTc8ylm-H9TKIzrsrDThu6c58D0fZPkDw=s0)



































La aplicación consistirá en una base de datos con un launcher(así se le llama a la aplicación/interfaz) del videojuego: *League of Legends*. El cual debe tener una tienda donde los usuarios comprarán varios productos como *skins, campeones y una* opción que guarde la *preferencia* de *pago* utilizada por el jugador (Paypal-Visa-Tarjeta de RP).
Dentro del juego también aparecerán eventos con *misiones* que deberán ir *numeradas*, ya que se desbloquearán conforme el jugador las vaya completando. A parte, estas misiones darán *monedas* del *evento* que servirán para comprar productos de la tienda que solo estarán disponible durante el tiempo que dure el evento.
Los usuarios deben contener un nombre único. Estos tienen que tener un registro del número de partidas jugadas en cada temporada que se lleve a cabo. El personaje con el que tenga mayor maestría y debe aparecer en el perfil del usuario, por último es necesario mostrar el nivel de honor del 1-5.
Los usuarios también tienen un chat que poseerá los *nombres* de los *jugadores* añadidos a su lista de amigos, podrán crear y nombrar *chat grupales,* deberá guardar *el número* de *usuarios* agregados, con un máximo de 60, si se quiere añadir a un nuevo jugador como amigo y supera el máximo, es necesario eliminar un usuario de la lista.
Ya que cada usuario puede cambiar las opciones del juego, que son la de calidad de *sonido* (Alto-Medio-Bajo), *Resolución* del juego (HD-2K-4K), y las *opciones gráfica*s del juego (Calidad Alta-Calidad Media-Calidad Baja).
Los usuarios pueden estar registrados en diferentes regiones, diferenciados por *ID*, *nombre* de la *región* y se guardará el *estado* actual de cada *servidor*. 
El juego posee un ranking en el que están registrados los jugadores junto con el *nombre* de la *temporada.* El ranking está formado por *rangos* que se dividen en *R.Bajo* (Hierro-Bronce-Plata) que pueden tener este rango mientras la cuenta siga activa, *R.Medio* (Oro-Platino-Diamante), requiere que lleven jugado al menos una partida clasificatoria en un mes, *R.Alto,* (Maestro-Gran Maestro-Desafiador) tienen que jugar una partida clasificatoria al día.
Al final de cada temporada, se reparten recompensas a cada jugador, para mantener un control, de quienes pueden recibirla, la *disponibilidad* de la *recompensa* (si-no) según si el jugador posee un nivel de honor por debajo de 2.
El ranking se dividirá en función de varios modos de juego y los tipos de modos de juego: *Flexible 5v5* o *Solo/Duo 5v5*. 






**Modelo Entidad/Relación**

![img](https://lh4.googleusercontent.com/0Eqk7Yz_yYoxzAgDVwDOY49Z3Sdequ4dY9l59TSrjQxaYj3YfLPDT0IZgUicN0qr41H-2pmpTqAWWsguq80rvFUR03Xx3g6TiSy_sDbFMox97k35yeNJSUWvZswzGw=s0)

**Modelo Relacional**

**Eventos:** (Id_evento,Num_misión, Moneda_Evento, Nombre_Misión).
**Productos_Tienda:** (Id_producto, Id_evento(F.K), Precio_Campeon, Tipo_Skin, Opciones_Pago, Precio_Skin, Nombre_Campeon).
**Usuarios:** (Id_usuario, Id_temporada(F.K), Nivel_Honor, Copa_clash, Top_Maestría, Num_Partidas_Jugadas, Nombre_Usuario).
**Compran:** (Id_Compra,Id_Producto(F.K), Id_usuario(F.K)).
**Entran:** (Id_Región, Id_usuario(F.K)).
**Cambiar:** (Id_Usuario, Id_opciones(F.K))
**Tienen:** (Id_Grupo, Id_Usuario).
**Server:** (Id_Región, Estado, Nombre_Región).
**Opciones:** (Id_Opciones, Op_Sonido, Op_Resolución, Op_Juego). 
**Social_Chat:** (Id_Grupo,Nombre_Grupo, Num_Amigos).
**Ranking:** (Id_Temporada, Nombre_Temporada).
**Modos_Juego:** (Id_Modo_Juego, Id_Temporada(F.K), Flexible_5v5, Solo/Duo_5v5).
**Rangos:** (Id_Rango, Id_Temporada(F.K), Nombre_Liga, Num_Division).
**Recompensas:** (Id_Recompensa, Id_Temporada(F.K), Disponibilidad).


**3. Normalización :**
La normalización es un proceso que consiste en asignar y aplicar una serie de reglas a las relaciones obtenidas tras el paso del modelo entidad-relación al modelo relacional. Con objeto de minimizar la redundancia de datos, facilitando su gestión posterior.
Por tanto aplicamos las formas normales para garantizar que el objetivo de la normalización se lleve a cabo.
1ª Forma normal (1FN) : Claves primaria de cada tabla: **Eventos:** Número de identificación del evento.(Id_Evento).**Productos_tienda:** Número de identificación de cada producto. (Id_producto).**Usuarios:** Número de identificación del usuario, en este caso, el nombre al ser único, puede ser utilizado como clave primaria.(Id_Usuario).**Opciones:** Número de identificación de las opciones. (Id_Opciones).**Social chat:** Número de identificación del grupo. (Id_grupo).**Ranking:** Número de identificación de la temporada. (Id_Temporada). **Modos_Juego:** Número de identificación del modo de juego. (Id_Modo_Juego).**Rangos:** Número de identificación de cada rango dentro del ranking.(Id_Rango). **Recompensas:** Número de identificación de cada recompensa. (Id_Recompensa).**Compran:** La relación consiste en que muchos usuarios pueden comprar productos, y muchos productos pueden ser comprados por varios usuarios. (Id_producto, Id_Usuario).**Entran:** Los usuarios deben estar registrados en un servidor para poder entrar al juego, pero pueden estar registrados en varios servidores de distintas regiones así como los servidores albergan muchos usuarios. (Id_Region, Id_Usuario).**Cambiar:** En el juego hay varias opciones que pueden ser ajustadas por los jugadores. (Id_Opciones, Id_Usuarios). **Tienen:** Los usuarios podrán tener varios amigos, con los que podrá formar grupos y poder conversar todos en un único chat. (Id_Usuario,Id_Grupo). 2ª Forma normal (2FN): Una relación está en 2FN si está en 1FN y si los atributos que no forman parte de ninguna clave dependen de forma completa de la clave principal. Es decir, que no existen dependencias parciales. Todos los atributos que no son clave principal deben depender únicamente de la clave principal.En este caso no me ha sido necesario ajustar las tablas a la 2FN (Ninguna dependencia parcial), además la relaciones entre las tablas dependen de una clave foránea. **Productos_Tienda:** (Id_producto, Id_evento(F.K)).**Usuarios:** (Id_usuario, Id_temporada(F.K)).**Modos_Juego:** (Id_Modo_Juego, Id_Temporada(F.K)).**Rangos:** (Id_Rango, Id_Temporada(F.K)).**Recompensas:** (Id_Recompensa, Id_Rango(F.K)).

3ª Forma normal (3FN):
La tabla se encuentra en 3FN si es 2FN y si no existe ninguna dependencia funcional transitiva en los atributos que no son clave.
Hay que tener en cuenta que este paso, es obligatorio que las tablas tengan una clave primaria.
Como las tablas y las relaciones entre ellas estaban bien pensadas desde el principio, no hizo falta.