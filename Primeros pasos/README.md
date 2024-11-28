# Instalacion de  Flutter
Con ayuda del siguiente tutorial instalaremos tanto Flutter como Android Studio en nuestro equipo.

<a href="https://www.youtube.com/watch?v=BTubOBvfEUE">Tutorial 

# Crear un proyecto nuevo
En este caso estaremos utilizando Visual Studio Code para la manipulacion y ejecucion de los proyectos.

 1- Inicia Visual Studio Code y abre la paleta de comandos (con F1, Ctrl+Shift+P o Shift+Cmd+P). Comienza a ingresar escribir "flutter new". Selecciona el comando Flutter: New Project.
 
 2- A continuación, selecciona Application y, luego, una carpeta en la que se creará tu proyecto. Podría ser tu directorio principal o alguno como C:\src\.
 
 3- Por último, asígnale un nombre al proyecto. Uno como namer_app o my_awesome_namer.

# Configuraciones iniciales

 1- Al archivo nombrado "pubspec.yaml" le cambiaremos su contenido por el siguiente:
 ```markdown
 name: namer_app
 description: A new Flutter project.

 publish_to: 'none' # Remove this line if you wish to publish to pub.dev

 version: 0.0.1+1

 environment:
   sdk: '>=2.19.4 <4.0.0'

 dependencies:
   flutter:
     sdk: flutter

   english_words: ^4.0.0
   provider: ^6.0.0

 dev_dependencies:
   flutter_test:
     sdk: flutter

   flutter_lints: ^2.0.0

 flutter:
   uses-material-design: true
```
 2- A continuación, en el archivo "analysis_options.yaml" se le cambiara su contenido por lo siguiente:
 ```markdown
include: package:flutter_lints/flutter.yaml

linter:
  rules:
    prefer_const_constructors: false
    prefer_final_fields: false
    use_key_in_widget_constructors: false
    prefer_const_literals_to_create_immutables: false
    prefer_const_constructors_in_immutables: false
    avoid_print: false
 ```
 3- Ahora configuraremos un emulador. En la barra inferior de Visual Studio Code, en la parte derecha, lo que esta justo alado de la campana debemos pulsar en ello y seleccionar nuestro emulador que deceemos utilizar.
 
# Programa
Ya con esos elementos listos podemos comenzar a programar nuestra aplicacion
