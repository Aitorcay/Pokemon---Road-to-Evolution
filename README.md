# Pokemon---Road-to-Evolution

Pokémon - Road to Evolution es un plataformas clásica en el que deberemos superar varios niveles aprovechando los poderes de cada personaje para avanzar por los escenarios.
En la versión definitiva el juego cuenta con 4 niveles y 6 personajes jugables. Para completar el juego deberemos superar todos los niveles, perdiéndose la partida si nos quedamos sin vidas.

### Mecánicas
Las mecánicas implementadas se pueden clasificar en las siguientes categorías.

##### Controles
 - Flechas de dirección: movimiento del personaje.
 - Z: ataque.
 - X: rotación de personaje.

##### Personajes
- Pikachu: utiliza el movimiento básico del componente platformerControls. Ataca con proyectiles eléctricos.
- Bulbasaur: utiliza el movimiento básico del componente platformerControls. Ataca con hojas cortantes.
- Charmander: utiliza el movimiento básico del componente platformerControls. Ataca con bolas de fuego.
- Squirtle: utiliza el movimiento básico del componente platformerControls. Ataca con burbujas.
- Machop: utiliza el movimiento básico del componente platformerControls. Ataca con golpes kárate.
- Gastly: al ser de tipo fantasma puede moverse libremente por el escenario. No ataca.

##### Obstáculos
- Torretas: se activan al recibir ataqué eléctricos.
- Árboles: pueden destruirse con los ataques cortantes de Bulbasaur.
- Bloques de hielo: pueden derretirse con las llamas de Charmander.
- Fuego: puede extinguirse con los ataques de agua de Squirtle. Daña al contacto.
- Rocas: pueden destruirse con la fuerza de Machop.
- Portales: solo pueden atravesarse usando un pokémon de tipo fantasma.
- Bloques: pueden ser destruidos con una explosión.
- Meta: nos permite avanzar al siguiente nivel.

##### Enemigos
- Normales: son derrotados al saltar sobre ellos o al ser golpeados con un ataque de proyectil. Se mueven por el escenario cambiando de dirección al chocar con un obstáculo.
- Voladores: son derrotados al saltar sobre ellos o al ser golpeados con un ataque de proyectil. Se mueven por el aire dentro de un rango de espacio.
- Disparadores: son derrotados al saltar sobre ellos o al ser golpeados con un ataque de proyectil. No tienen movilidad. Atacan lanzando proyectiles cada cierto tiempo.
- Irascibles: son derrotados al saltar sobre ellos o al ser golpeados con un ataque de proyectil. Resisten dos golpes. Tras recibir el primer golpe se enfurece y su velocidad de movimiento aumenta.
- Explosivos: son derrotados al saltar sobre ellos o al ser golpeados con un ataque de proyectil. Al morir crean una explosión dañina capaz de destruir bloques especiales.
- Elásticos: no pueden ser derrotados. Al saltar sobre ellos el rebote nos permite alcanzar zonas elevadas.
- Plataformas: no pueden ser derrotados. Son enemigos voladores que podemos ultlizar como plataforma móvil para alcanzar ciertas zonas del escenario.
- Bosses: son derrotados al saltar sobre ellos o al ser golpeados con un ataque de proyectil. Resisten varios golpes. Es necesario derrotarlos para superar el nivel.

##### HUD
- Vidas: cada vez que el jugador se cae del escenario o se queda sin salud pierde una vida. Al quedarse sin vidas termina el juego.
- Corazones: representan la salud del jugador. Cada vez que choca con un enemigo o es golpeado por un proyectil pierde medio corazón. Como excepción Gastly será derrotado con un solo golpe, compensando así su gran capacidad de movimiento.

##### Ítems
- Monedas: objetos coleccionables. En cada nivel hay repartidas 3 monedas, algunas solo alcanzables utilizando los poderes de un personaje en concreto.
- Bayas aranja: nos permiten recuperar un corazón. Son dropeadas por los enemigos irascibles.
- Revivir: nos permite recuperar una vida. Son dropeadas por los bosses.


### Diseño e implementación

El juego ha sido implementada con el motor Quintus y los escenarios han sido construidos con el editor de mapas Tiled.
Para un código más limpio y reutilizable hemos encapsulado el código en distintos componentes:

- Player: gestiona el daño y la muerte del jugador, así como las animaciones asociadas al movimiento.
Además de esto, en cada personaje jugable está implementado su ataque y la rotación con el siguiente personaje.

- DefaultEnemy: gestiona las colisiones del jugador y sus ataques con los enemigos.
- NormalEnemy: implementa el comportamiento de los enemigos normales.
- ShooterEnemy: implementa el comportamiento de los enemigos disparadores.
- AngryEnemy: implementa el comportamiento de los enemigos irascibles.
- FlyingEnemy: implementa el comportamiento de los enemigos voladores.
- ElasticEnemy: implementa el comportamiento de los enemigos elásticos.
- ExplosiveEnemy: implementa el comportamiento de los enemigos explosivos.
- PlatformEnemy: implementa el comportamiento de los enemigos que podemos usar como plataforma móvil.
Los bosses únicamente cuentan con el componente defaultEnemy.

El código de los proyectiles es similar entre todos. Al chocar con el obstáculo correspondiente lo eliminan, o en el caso de los proyectiles enemigos causan daño al jugador.
Salvo la torreta, que puede tener distintos efectos sobre el escenario, el resto de obstáculos desaparecen cuando se da el evento necesario.

Los ítems han sido implementados como sensores. Las bayas y revivires cuentan con un pequeño delay para ser recogidos y están animadas con tween para llamar la atención del jugador.

### Equipo de desarrollo

##### Game & level design:
- Aitor Cayón Ruano
##### Programmers:
- Aitor Cayón Ruano
- Yu Liu
- Gabriel Sellés Salvà
- Víctor Tobes Pérez

##### Carga de trabajo
- Aitor Cayón Ruano: 40%
- Yu Liu: 20%
- Gabriel Sellés Salvà: 20%
- Víctor Tobes Pérez: 20%

Para facilitar la transmisión del concepto del juego uno de los miembros ha asumido más carga de trabajo con el fin de encaminar el proyecto. Una vez clara la idea a desarrollar el reparto en las distintas áreas de programación ha sido equitativo.

##### Reparto del trabajo
- Aitor Cayón Ruano: niveles e interfaz, personajes jugables y obstaculos.
- Yu Liu: enemigos
- Gabriel Sellés Salvá: enemigos.
- Víctor Tobes Pérez: HUD e ítems.

Debido a la gran cantidad y diversidad de enemigos decidimos destinar a dos miembros para esa tarea.

### Assets

##### Sprites
Pertenecientes a la saga Pokémon Mundo Misterioso de Nintendo.
https://www.spriters-resource.com/ds_dsi/pokemonmysterydungeonexplorersoftimedarkness/

##### Música
Perteneciente a los juegos Pokémon Rojo y Azul de Nintendo.
https://downloads.khinsider.com/game-soundtracks/album/pokemon-original-game-soundtrack

##### Otros assets
Fuego: https://www.spriters-resource.com/arcade/joenmac/sheet/27553/
Background de cueva: http://pukahuna.deviantart.com/art/Cave-Background-584380837
Background de ciudad: http://grigoreen.tumblr.com/post/106167118417
Estatua de arceus: http://photobucket.com/gallery/user/V0RT3X-1989/media/bWVkaWFJZDoxNDk3NjE0NQ==/?ref=
Moneda: http://www.sprites-unlimited.com/game/?code=PokemonTCG
Tileset:http://www.supermariobrosx.org/forums/viewtopic.php?f=49&t=4572 BMatSantos 

Disculpas por los assets que hayamos olvidado mencionar. Gracias por vuestra ayuda y gracias por jugar. Esperamos que lo disfrutéis.
