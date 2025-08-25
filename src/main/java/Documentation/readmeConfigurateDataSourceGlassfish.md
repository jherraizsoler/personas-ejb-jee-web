

**Readme realizado por Jorge Herraiz Soler**

# Procedimiento para configurar el Data Source funcionalidad persistencia 
(El servidor glassfish necesita que configuremos jdbc/PersonaDB              



## REQUERIMIENTOS TECNICOS Y  PRACTICOS

1. Tener Apache Netbeans IDE 26  
 
2. Tener instalado el jdk-21  
   | java -version 21.0.7 | 

3. Tener instalado GassFish Server 8.0.0  
   | Propiedades > Java (Pestaña) >> Java Platform JDK =>  JDK 21  | 

   Vinculo (revisar en caso de no tener instalado GassFish Server 8.0.0 )
        - Archivo  / url  --  Documentation/readmeInstallGlassfishServer8.0.0


## PROCEDIMIENTO  APPLICATION  DEPLOY  PERSONAS-JEE-WEB

1. Dentro de Netbeans nos vamos a la pestaña Services
   (En caso de no encontrarlo  Arriba en el toolbar |  Window  > Services)

5. Ahora le damos click izquierdo a Servers y le damos click derecho y le damos
   a "View Domain Admin Console" al servidor Glassfish 8.0.0 ya configurado en el 
   archivo / url  -- Documentation/readmeInstallGlassfishServer8.0.0

6. Ahora en el Menu desplegable de la izquierda "Common Tasks" nos vamos a 
   "Resources".

7. Una vez dentro de "Resources" le damos a JDBC y una vez dentro en "JDBC Connection Pools" y le damos al botón "New".

8. Escribimos lo siguiente para crear y configurar PersonaPool
    __________________________ G E N E R A L ________________________________
    Pool Name:  PersonaPool
    Resource Type: javax.sql.ConnectionPoolDataSource
    Database Driver Vendor(El TextField no el spinner):  com.mysql.cj.jdbc.MysqlDataSource
    Insolation Level:  Guaranteed(Marcado)
    
    ___________________________ A D V A N C E D ______________________________
    Wrap JDBC Objects: Marcado()
    Pooling: marcado()

    _____________  A D D I T I O N A L   P R O P E R T I E S _________________
    * Añade Propiedades en Add Property
    
    Name                             Value        

    allowPublicKeyRetrieval          true
    serverTimezone                   UTC
    useTimezone                      true
    useSSL                           false
    password                         alumno
    databaseName                     test
    serverName                       localhost
    datasourceName                   com.mysql.cj.jdbc.MysqlDataSource
    user                             root
    portNumber                       3306

    ** Le damos al botón "Save" para guardar los cambios.
    ** Le damos a ping para comprobar que esta correctamente

9. Una vez dentro de "Resources" le damos a JDBC y una vez dentro en JDBC Resources y le damos al botón "New".
   
   Escribimos lo siguiente para crear y configurar PersonaDB

   En JNDI Name: jdbc/PersonaDB 
   En Pool Name: PersonaPool
