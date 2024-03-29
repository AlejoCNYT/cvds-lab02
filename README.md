# LABORATORIO 2 - PATTERNS

Daniel Alejandro Acero

Julián David Triana Roa

## LA HERRAMIENTA MAVEN

### Cuál es su mayor [utilidad](https://maven.apache.org/what-is-maven.html)

Maven sirve para facilitar la gestión de proyectos a múltiples desarrolladores, aunque tiene múltiples utilidades y potencialidades tales como:

- Eliminación de código innecesario.
- Facilidad para entender un único Modelo de Objeto de Proyecto (POM).
- Proveer información relevante.
- Utilizar o no determinados plugins.
- Boostear las mejores prácticas de desarrollo.

Adicionalmente, posee otros atributos que lo [caracterizan](https://maven.apache.org/maven-features.html):

* Instantaneidad en sus funciones.
* Consistencia del equipo.
* Actualización automática de la dependencia.
* Extensibilidad del plugin.
* Proyecto basado en modelos.

entre otras.

### Fases de maven 

A continuación la lista completa de [fases](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html) del ciclo de vida 'default' en MAVEN:

1. *Validate* Validar la correctitud y completitud de la información relacionada al proyecto.
2. *Compile* Compilación del coódigo fuente.
3. *Test* Ensayo del funcionamiento adecuado.
4. *Package* Compilar el código en formato **.jar**.
5. *Verify* Control de calidad constante.
6. *Install* Uso local de paquetes.
7. *Deploy* Compartir el avance local, con el repositorio.

### Ciclo de vida de la construcción 

El ciclo de vida de construcción puede variar en sus fases. Adicionalmente a la 'default', podemos listar las siguientes:

* *Clean* Eliminar archivos anteriormente creados. Realizar proyectos de elementales antes y después de la limpieza.
* *site* Generar la documentación del sitio web del proyecto. Procesos anteriores y posteriores a la ejecución del sitio. Generar documentación.

### Para qué sirven los plugins 

Sirven para [complementar funcionalidades](https://maven.apache.org/plugins/index.html) de Maven, como por ejemplo:

* Generar EAR.
* Construir EJB, RAR, JAR y AR.
* Construir cliente JavaEE, Uber-JAR, fuente-JAR, Java Run Time Imagen y archivos Java JMod.
* Generar lista de cambios SCM, informe rastreador de emision, informe de checkstyle, DOAP de POM, Javadoc de JDK, referencia cruzada en la fuente, informe Linkcheck, informe PMD, informe de proyecto estándar,                 informe basado en resultados de prueba de unidad.
* Generar archivos Eclipse y archivo de construcción de hormigas.
* Plugins para ayuda de tareas e interacción del legado MAVEN.

además de las herramientas Maven por defecto, MojoHaus y Misc, etc.
    
### Qué es y para qué sirve el repositorio central de maven

Es una biblioteca de artefactos almacenados, a manera de depósito, como parte de la filosofía Maven. Estos artefactos, pueden ser ubicados mediante coordenadas. El repositorio Maven permite añadir o hacer uso de plugins previamente [implementados](https://maven.apache.org/repository/index.html).

## EJERCICIO DE LAS FIGURAS  

### CREAR UN PROYECTO CON MAVEN   

Se crea un [repositorio](https://youtu.be/nMvGzXTAxWg) Maven con ayuda de Archetypes.

![2](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/3c079c1a-f5e1-48a1-92ac-032a8ee11963)    

Se establece la configuración solicitada:

* ProjectId: org.apache.maven.archetypes:maven-archetype-quickstart:1.0
* Id del Grupo: edu.eci.cvds
* Id del Artefacto: Patterns
* Paquete: edu.eci.cvds.patterns.archetype

![Captura de pantalla 2024-02-08 133326](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/465eefca-b815-4719-82ae-cc61c401e641)

Se verifica la creación de nuevos directorios con nuevos archivos y la estructura del proyecto

![Captura de pantalla 2024-02-08 070658](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/92b0df56-a7ea-4723-af1e-0caa9b4bf597)

## AJUSTAR ALGUNAS CONFIGURACIONES EN EL PROYECTO

Se ejecuta el comando para modificar pom.xml

![Captura de pantalla 2024-02-08 073424](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/e0700c78-6063-4879-a935-c752e703c9f8)

este comando, abre un block de notas donde podemos editar el archivo

![Captura de pantalla 2024-02-08 073508](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/d151a436-94aa-4a5d-a184-83d5c1ba12b3)

Se configura el cambio de Java a la versión 8. Para esto, se agrega en la ubicación respectiva

![Captura de pantalla 2024-02-08 074345](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/d4646a77-25f6-4bee-afbe-11faa5781e18)

y se guarda.

## COMPILAR Y EJECUTAR

Se compila la nueva versión con el siguiente comando

![Captura de pantalla 2024-02-08 133649](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/c9fb9303-fe88-4871-93f4-8c13004dd3e0)

al final de la ejecución, nos confirma el proceso
    
![Captura de pantalla 2024-02-08 074654](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/8940fbc2-b814-4d16-9a50-7cc348855337)

por lo cual, no será necesario actualizar las dependencias con el comando ´mvn -U package´. 

El parámetro **package** del comando 'mvn' establece la estructura de los paquetes Java del proyecto. No obstante, el comando ´mvn archetype:generate´ puede recibir otros parámetros tales como

1) *compile* Compilar el códgigo fuente.
2) *test* Para realizar ejecución de pruebas unitarias.
3) *install* Facilita el uso de dependencias en otros proyectos, instalando artefactos del repositorio local.
4) *deploy* Permite copiar artefactos remotos.
5) *clean* elimina archivos o artefactos generados en el proyecto.
6) *validate* Valida el correcto funcionamiento y configuración del proyecto.
7) *help* Ofrece información acerca de objetivos o plugins del proyecto.

Para verificar la salida como parámetro en "mainClass" y [ejecutar](https://www.mojohaus.org/exec-maven-plugin/usage.html) el proyecto pulsamos:

![Captura de pantalla 2024-02-08 133858](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/8a265a71-dc9d-470e-9b63-891436484ca4)

y, finalmente

![Captura de pantalla 2024-02-08 133910](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/04816622-d751-4bb0-90f5-0ac920696091)

Para crear el saludo personalizado se ejecuta la clase App.java 

![Captura de pantalla 2024-02-08 135154](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/7ebaa169-3081-4c71-a9c5-387c993a4a3c)

y, luego, se modifica

![imagen](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/ee1774f8-0064-4eec-a405-ef271a4d74e4)

Ahora, se verifica la ejecución del programa

![Captura de pantalla 2024-02-09 090546](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/ccbad1a0-e688-4cf9-8ba0-1024150cbf3f)

Se [cambia la salida](https://www.mojohaus.org/exec-maven-plugin/examples/example-exec-for-java-programs.html) con el nombre propio, con ayuda del comando

´´´
    mvn exec:java -Dexec.mainClass="edu.eci.cvds.patterns.App" -Dexec.args="'argument1' 'argument2'"
    
![image](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/b37f3ab9-0894-49ec-bb5a-ae4971b3a798)

Se cambia la salida con el nombre y apellido


![image](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/d1f5d096-6134-40c6-8d99-850b3153f7ef)

Se ejecuta la clase desde línea de comandos, con nombres como parámetro.
![image](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/7aaf22f3-3f7c-4148-b601-ce7968f656c1)

## HACER EL ESQUELETO DE LA APLICACIÓN
        
Hacer el esqueleto de la aplicacion de acuerdo a la guia de laboratorio
![screenshot](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/2a26cffd-0bf6-42bd-b832-5a83dd9aad69)

Creacion de paquetes:
## Paquete Shapes 
RegularShapeType
![IMG_2527](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/f0000d08-3ed2-4e76-a59d-a1e35fea5a6c)

Shape
![IMG_2528](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/36889947-d651-4a04-afc0-b52119fecee8)

ShapeMain

![IMG_2531 2](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/b5647402-6ff9-4178-bbe5-2ed1dd47e2a5)


## Paquete Concrete
Hexagon

![IMG_2532](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/eba66caa-caf5-4c95-a243-fdd58fc27a62)

Pentagon

![IMG_2533](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/5d5ad6b3-e54c-419d-8a29-1de99378d27d)

Quadrilateral
![IMG_2534](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/a3fbf172-a437-444e-bd0e-394fe643025a)

Triangle
![IMG_2535](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/93586e7f-4bb3-4832-9204-0d9523cdf994)


## Finalmente el Factory


ShapeFactory 

![IMG_2526](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/2723e81c-e612-41b6-864f-50972db20ea3)



Se ejecuta varias veces la clase ShapeMain, usando el plugin exec de maven con los siguientes parámetros y verifique la salida en consola para cada una:

Sin parámetros

![image](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/8ade8212-c966-485e-b7d0-bb63a5e6ec90)

Parámetro: qwerty
![image](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/dc6e8a0c-c6b8-4752-9c5b-808da0cc0bc3)


Parámetro: pentagon

![image](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/531b2efe-dffa-41b7-8866-3692312aa765)
![image](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/39c0f52f-b2c7-4109-a907-df70dc6cbf42)

Parámetro: Hexagon

![image](https://github.com/AlejoCNYT/cvds-lab02/assets/74771189/85ed2dac-c3ff-478e-ad7c-5fcc2a4e1d9d)


## ¿Cuál(es) de las anteriores instrucciones se ejecutan y funcionan correctamente y por qué?

Todas las intrucciones ejecutadas funcionan correctamente, pues hace las correspondientes validaciones como lo son: que tenga párametro, que exista la figura ingresada y por último si cumple lo anterior muestra los vértices de la figura

    


                            

