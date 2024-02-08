# LABORATORIO 2 - PATTERNS

Daniel Alejandro Acero Varela

Julián David Triana Roa


## LA HERRAMIENTA MAVEN

### Cuál es su mayor [utilidad](https://maven.apache.org/what-is-maven.html)

    Maven sirve para facilitar la gestión de proyectos a múltiples a múltiples desarrolladores, aunque tiene múltiples utilidades y potencialidades tales como:

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

        1. ´Validate´ Validar la correctitud y completitud de la información relacionada al proyecto.
        2. ´Compile´ Compilación del coódigo fuente.
        3. ´Test´ Ensayo del funcionamiento adecuado.
        4. ´Package´ Compilar el código en formato **.jar**.
        5. ´Verify´ Control de calidad constante.
        6. ´Install´ Uso local de paquetes.
        7. ´Deploy´ Compartir el avance local, con el repositorio.

### Ciclo de vida de la construcción 

    El ciclo de vida de construcción puede variar en sus fases. Adicionalmente a la ´default´, podemos listar las siguientes:

        * ´Clean´ Eliminar archivos anteriormente creados. Realizar proyectos de elementales antes y después de la limpieza.
        * ´site´ Generar la documentación del sitio web del proyecto. Procesos anteriores y posteriores a la ejecución del sitio. Generar documentación.

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

    Es una biblioteca de artefactos almacenados, a manera de depósito, como parte de la filosofía Maven. Estos artefactos, pueden ser ubicados mediante coordenadas. El repositorio Maven permite añadir o hacer uso de            plugins previamente [implementados](https://maven.apache.org/repository/index.html).

## EJERCICIO DE LAS FIGURAS  

### CREAR UN PROYECTO CON MAVEN   

    Se crea un [repositorio](https://youtu.be/nMvGzXTAxWg) Maven con ayuda de Archetypes.

![2](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/3c079c1a-f5e1-48a1-92ac-032a8ee11963)    

    Se establece la configuración solicitada:

        * ProjectId: org.apache.maven.archetypes:maven-archetype-quickstart:1.0
        * Id del Grupo: edu.eci.cvds
        * Id del Artefacto: Patterns
        * Paquete: edu.eci.cvds.patterns.archetype

![Captura de pantalla 2024-02-08 070346](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/9732e6b1-1d43-4e11-bada-2c8fa9c87572)

    Se verifica la creación de nuevos directorios con nuevos archivos y la estructura del proyecto

![Captura de pantalla 2024-02-08 070658](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/92b0df56-a7ea-4723-af1e-0caa9b4bf597)

## AJUSTAR ALGUNAS CONFIGURACIONES EN EL PROYECTO

    Se ejecuta el comando para modificar pom.xml

![Captura de pantalla 2024-02-08 073424](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/e0700c78-6063-4879-a935-c752e703c9f8)

    este comando, abre un block de notas donde podemos editar el archivo

![Captura de pantalla 2024-02-08 073508](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/d151a436-94aa-4a5d-a184-83d5c1ba12b3)

    Se onfigura el cambio de Java a la versión 8. Para esto, se agrega en la ubicación respectiva

![Captura de pantalla 2024-02-08 074345](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/d4646a77-25f6-4bee-afbe-11faa5781e18)

    y se guarda.

## COMPILAR Y EJECUTAR

    Compilamos la nueva versión con el siguiente comando

![Captura de pantalla 2024-02-08 074613](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/c454b532-c70c-458b-a386-567b1230cdda)

    al final de la ejecución, nos confirma el proceso
    
![Captura de pantalla 2024-02-08 074654](https://github.com/AlejoCNYT/cvds-lab02/assets/89206637/8940fbc2-b814-4d16-9a50-7cc348855337)

    por lo cual, no será necesario actualizar las dependencias con el comando ´mvn -U package´. 

    El parámetro **package** del comando ´mvn archetype:generate´ establece la estructura de los paquetes Java del proyecto. No obstante, el comando ´mvn archetype:generate´ puede recibir otros parámetros tales como

        1. ´-DgroupId´ Es el identificador del grupo de proyecto. Particularmente, su notación es inversa tal y como se muestra en ´edu.eci.cvds´.
        2. ´-DartifactId´ Se usa para definir el identificador del artefacto del proyecto. Este, es el nombre único del proyecto y genera e nombre del archvo JAR entre otros artefactos de manera similar a como ´Patterns´ lo hace.
        3. ´-DarchetypeGroupId´ Se usa para definir el identificador de grupo archetype Maven. De este modo, se especifica el grupo archetype que genera el proyecto.
        4. ´-DarchetypeArtifactId´ Define el identificador archetype Maven. Con él, se especifica el archetype Maven que genera el proyecto. Es el papel que cumple ´maven-archetype-quickstart´.
        5. ´-DarchetypeVersion´ Indica la versión del archetype Maven a utilizar. Esto, dado que pueden haber diversas versiones disponibles. 
        6. ´-DinteractiveMode´ Establece o no el modo interactivo al generar el proyecto. Si se proporciona ´false´, se utilizarán los valores por defecto.

            

## HACER EL ESQUELETO DE LA APLICACIÓN
        
 ![mvn](http://url/a.png)                                                                                                                                                                                                                                                                                        
                            
                                                                                                                                                                                            *Autores* 
                                                                                                                                                                                                          
                                                                                                                                                                                                Daniel Alejandro Acero 
                                                                                                                                                                                                -----------------------
                                                                                                                                                                                                Julian Triana
                                                                                                                                                                                                -----------------------
