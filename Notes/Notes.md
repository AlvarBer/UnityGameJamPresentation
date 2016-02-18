Curso Unity 2016
===============================

### Presentación

- Disclaimer
- Yo. RedBricks.
- Concepto de las Game Jams.

### Suposiciones

- Ya sabes programar. Idealmente, has aprobado TP (aka sabes lo que es una interfaz, un patrón de diseño, encapsulación...).
- Quieres hacer juegos.
- Eres capaz de levantar la mano y preguntar. 
       - Este curso irá muy rápido sobre cada cosa de Unity, así que si algo necesita clarificación, levanta la mano.

### Consejos Principales:

- Diseña pequeño. (Diseño del juego)
- CODE: TODOS los programadores tienen que seguir el mismo workflow. (Presentamos el nuestro)
- CODE: NO esperes reutilizar el código. (Buenas prácticas).
- ARTE: Define MUY BIEN y DESDE EL PRINCIPIO cómo quieres que te den las cosas los artistas. (Explico los problemas con MEOW).
- SONIDO: Ten en cuenta la música!. (Cómo se pone música en Unity).
- Google-foo.

### Diseña pequeño

- Todo el equipo debería estar implicado.
- Listad palabras/conceptos que se os ocurran con el tema.
- Perded media hora discutiendo como hacer la idea mas molona de la lista.
- Tachadla de la lista. Es demasiado grande. Lo siento.
- Repetid el proceso hasta que encontreis una idea que:
    - a) Los programadores dicen "hmm, si sin problema" a implementar todas las mecánicas.
    - b) Los artistas dicen "Si, eso para mañana ya está" (Spoilers: No).
- Poned en Trello todo lo que hay que hacer, y que cada uno tenga su panel.

- Si alguien quiere hacer un cambio, que pregunte primero a todos los implicados.

### Workflow

- Muestra la estructura de carpetas.

- Eligo en Trello la tarea que quiero hacer.
    - Ejemplo: Quiero hacer los controles.
    
- [Escena] Cada programador tiene una **Escena** <Nombre>Dev, sobre la que desarrolla su parte. 
    - Ejemplo: Estoy desarrollando los controles, 
               así que me hago una escena BorjaDev en la que pongo mis propios objetos, y los voy marcando.
               
- [Objeto][Componente] Hago **Objetos** de prueba, y voy probando funcionalidades, poniendoles **Componentes**.
    - Ejemplo: Para los controles, necesito que el cuerpo reaccione a la física, así que necesita un 
                **Rigidbody2D**, y probablemente un **Collider**.
                
- [Prefab] Cuando estoy 100% seguro de que el obeto que estoy usando funciona, lo hago un **Prefab**. 
           Para eso, conviene preguntar al equipo, y tomar git-precauciones antes de tocarlo, para evitar conflictos.

- Commit, pull, push. Esto ya os lo explicará Álvaro.

- Marco la tarea como hecha en Trello.

### Buenas prácticas

Como programadores, estaremos creando Scripts la mayoría del tiempo (la otra parte es Animar y poner Sonidos).

- IMPORTANTE: Asume que NO vas a reutilizar el código. Puede que lo reutilizes (código de IA), 
              pero intentar diseñar código reutilizable quita precioso tiempo de desarrollo. 
              El momento de hacer las librerías es ANTES de la Jam.
              Aún así, deberíais poneros de acuerdo en algunas cosas.
 
- [MonoBehaviour] Usad mayormente MonoBehaviours (Unity Script). Se inicializan automáticamente, y sirven como componente.
                    Cómo hacer que los arrays aparezcan en el Inspector.
              
- [Find][Tag] Poneos de acuerdo en **como encontrar objetos en la escena** (por Tag? Nombre?...)
         Funciones Find(""), FindByTag(), etc. Da igual cuál uséis, pero POENOS DE ACUERDO!
         Nosotros usamos Tags.

- [SendMessage] La función SendMessage() es súper útil (y muy guarra). Usadla.
                Básicamente le pasas una string con el nombre del método que quieres ejecutar, y
                si CUALQUIERA DE SUS COMPONENTES tiene ese método, lo ejecuta.                
                Uso genial: que todo lo dañable responda a onDamage(); Así, la lógica de muerte
                Está en un componente del objeto que se muere.

- [UnityPackages] Si es NECESARIO pasar archivos por GoogleDrive/Pendrive/... Pasadlos en un UnityPackage.

- [Mapas] Pensad antes de hacer nada si el mapa va a ser a base de tiles. Si es así, puede que merezca la pena 
            Escribir un importador, o mirar Tiled...
            Si quereis fondos chulos a medida, pasadles una captura del nivel en Unity/Tiled a los artistas,
            para que tengan en cuenta las proporciones.
            
- [Google-foo] Acostumbraos a mirar las páginas de Unity. Es como un javadoc.
            
### Arte

- Tened un repertorio de cuadrados de colores preparados para hacer de placeholders. (Ejemplo con el paint).
- Los artistas tienen que tener la posibilidad de ser agnósticos de Unity. Es decir, que os pasan .pngs
- Poneos de acuerdo en lo que queréis. Idealmente (Para 2D), una de las dos opciones:
    - Spritesheet: Todos los frames de una animación están en el mismo archivo. Tienen que asegurarse de que:
        - El fondo es transparente. (Paint Tool SAI no lo pernite, creo).
        - El centro de cada frame es el centro de la animación (Ejemplo en la pizarra). Si no, se te descojona la animación.
        
        - Ejemplo de importación.
        
    - Frames en archivos individuales. Idealmente, todos los frames son de la misma anchura, y por supuesto fondo transparente.
    
### Git Gud

### Anchors and other dark magic

### Q&A
 
    