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
- Corazones: representan la salud deljugador. Cada vez que choca con un enemigo o es golpeado por un proyectil pierde medio corazón.

##### Ítems
- Monedas: objetos coleccionables. En cada nivel hay repartidas 3 monedas, algunas solo alcanzables utilizando los poderes de un personaje en concreto.
- Bayas aranja: nos permiten recuperar un corazón. Son dropeadas por los enemigos irascibles.
- Revivir: nos permite recuperar una vida. Son dropeadas por los bosses.




