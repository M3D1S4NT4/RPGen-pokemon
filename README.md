# RPGen - Generador de Combates Pokémon

Este proyecto es un sistema completo que te permite crear equipos de Pokémon, personalizarlos con todo lujo de detalles y llevar a cabo combates estratégicos que simulan las mecánicas de los juegos originales.

## Características Principales

### 🎮 Sistema de Combate Completo

  - **Combates por turnos**: libra combates con una mecánica realista, fiel a la saga Pokémon.
  - **Cálculo de daño**: el sistema calcula el daño teniendo en cuenta tipos, estadísticas y efectividad.
  - **Animaciones**: disfruta de animaciones de ataque y daño que aportan dinamismo a los combates.
  - **Sistema de velocidad**: la velocidad de cada Pokémon es crucial para determinar el orden de ataque en cada turno.
  - **Cambio de Pokémon**: puedes cambiar de Pokémon en cualquier momento del combate para adaptar tu estrategia.
  - **Registro de batalla**: sigue el transcurso del combate con un registro detallado de cada acción.

### 📊 Estadísticas Avanzadas

  - **IVs (Individual Values)**: personaliza los valores individuales de cada estadística, en un rango de 0 a 31.
  - **EVs (Effort Values)**: distribuye los puntos de esfuerzo (de 0 a 252 por estadística, con un máximo de 510 en total) para potenciar a tus Pokémon.
  - **Naturalezas**: elige entre 25 naturalezas distintas que modifican las estadísticas de tus Pokémon, aumentando una y disminuyendo otra en un 10%.
  - **Cálculo automático**: el sistema calcula de forma automática las estadísticas finales de tus Pokémon basándose en su nivel, IVs, EVs y naturaleza.

### 🎯 Habilidades y Objetos

  - **Habilidades**: cada Pokémon cuenta con sus habilidades correspondientes, incluyendo las habilidades ocultas.
  - **Objetos equipados**: puedes equipar a tus Pokémon con más de 20 objetos diferentes, cada uno con efectos únicos en combate.
  - **Modificadores de estadísticas**: tanto las habilidades como los objetos aplican automáticamente modificadores a las estadísticas de tus Pokémon.
  - **Efectos especiales**: algunos objetos y habilidades tienen efectos especiales, como restaurar PS, aumentar la potencia de los movimientos, etc..

### 🏆 Gestión de Equipos

  - **Crea múltiples equipos**: puedes crear y guardar diferentes equipos con nombres personalizados.
  - **Selección de movimientos**: elige hasta 4 movimientos para cada Pokémon de tu equipo.
  - **Configuración completa**: personaliza cada aspecto de tus Pokémon de forma individual.
  - **Guardado automático**: todos tus equipos y configuraciones se guardan automáticamente en el almacenamiento local de tu navegador.

### 🎨 Interfaz Moderna

  - **Modo oscuro/claro**: elige el tema que prefieras para la interfaz.
  - **Diseño responsivo**: la aplicación se adapta a diferentes tamaños de pantalla para que puedas usarla en cualquier dispositivo.
  - **Información detallada**: obtén información detallada sobre cada elemento del juego a través de tooltips y ventanas modales.
  - **Animaciones suaves**: disfruta de animaciones fluidas y transiciones agradables.
  - **Iconos intuitivos**: la interfaz utiliza iconos de Font Awesome para que todas las acciones sean fáciles de entender.

## Tecnologías Utilizadas

### Backend

  - **Java 17** con **Spark Framework** para el servidor web.
  - **PokéAPI** como fuente de datos para Pokémon, habilidades, etc..
  - **Cliente HTTP de Java** para realizar peticiones asíncronas a la API.
  - **Gson** para el manejo de datos en formato JSON.

### Frontend

  - **HTML5** y **CSS3** para la estructura y el diseño de la aplicación.
  - **JavaScript (ES6+)** con `async/await` para la lógica del cliente y la interactividad.
  - **Font Awesome** para los iconos de la interfaz.
  - **Grid** y **Flexbox** para la maquetación de la interfaz.

## Instalación y Uso

### Requisitos

  - **Java 17** o superior.
  - **Maven 3.6** o superior.

### Ejecución

1.  Clona el repositorio en tu máquina local.
2.  Descarga el núcleo desde `https://github.com/M3D1S4NT4/RPGen`
3.  Abre una terminal en el directorio raíz del núcleo
4.  Instala el núcleo usando
    ```bash
    mvn clean install
    ```
5.  Abre una terminal en el directorio raíz del proyecto.
6.  Ejecuta el comando `mvn spring-boot:run` para compilar el proyecto y descargar las dependencias.
7.  Abre tu navegador y ve a `http://localhost:4567`.

### Uso del Sistema

#### 1\. Crear Equipos

  - Abre `http://localhost:4567/pokemon.html` en tu navegador
  - En esta página de **Pokédex**, busca los Pokémon que quieras por su nombre o tipo.
  - Haz clic en un Pokémon para añadirlo a tu equipo actual.
  - Abre el modal de configuración para personalizar sus movimientos, habilidad, objeto y estadísticas.
  - Guarda tus equipos con un nombre único para usarlos más tarde.

#### 2\. Configurar Pokémon

  - **Habilidades**: elige una de las habilidades disponibles para tu Pokémon.
  - **Objetos**: equípale un objeto para potenciarlo en combate.
  - **Naturalezas**: selecciona la naturaleza que mejor se adapte a tu estrategia.
  - **IVs/EVs**: ajusta los valores de esfuerzo e individuales para optimizar sus estadísticas.

#### 3\. Iniciar Combate

  - Una vez seleccionados y configurados los equipos, dale a "Iniciar Batalla" en la **Pokédex** o vete a `http://localhost:4567/battle.html`
  - Selecciona dos de tus equipos guardados.
  - Elige los Pokémon que quieres que salten al campo de batalla.
  - ¡Que empiece el combate\! Ataca o cambia de Pokémon según tu estrategia.

## Estructura del Proyecto

```
RPGen-Pokemon/
├── pom.xml
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── rpgen/
│   │   │           ├── Main.java
│   │   │           ├── chrono/
│   │   │           ├── core/
│   │   │           │   ├── action/
│   │   │           │   ├── battle/
│   │   │           │   ├── entity/
│   │   │           │   └── web/
│   │   │           └── pokemon/
│   │   │               ├── battle/
│   │   │               ├── data/
│   │   │               ├── entity/
│   │   │               └── web/
│   │   └── resources/
│   │       ├── logback.xml
│   │       └── public/
│   │           ├── battle.html
│   │           ├── chrono-battle.html
│   │           ├── chrono-team.html
│   │           ├── index.html
│   │           └── pokemon.html
│   └── test/
└── README.md
```
