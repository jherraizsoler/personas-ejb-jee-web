
**Readme realizado por Jorge Herraiz Soler**

# Procedimiento para iniciar desde cero este proyecto.


## REQUERIMIENTOS  TECNICOS  Y  PRACTICOS

1. Tener Apache Netbeans IDE 26  
 
2. Tener instalado el jdk-21  
   | java -version 21.0.7 | 

3. Tener instalado GassFish Server 8.0.0  
   | Propiedades > Java (Pestaña) >> Java Platform JDK =>  JDK 21  | 

   Vinculo (revisar en caso de no tener instalado GassFish Server 8.0.0 )
        - Archivo  / url  --  Documentation/readmeInstallGlassfishServer8.0.0.md


## PROCEDIMIENTO  APPLICATION  DEPLOY  PERSONAS-JEE-WEB

1. Tener instalado MySQL Workbench 8.0.42  (Community Version)

2. Dentro de MySQL Workbench crear Schema con el nombre test 

3. Dentro de MySQL Workbench en Server > Data Import  seleccionar la carpeta que esta en Documentation que se llama importarBD_test y darle a importar

4. Tener instalado Glassfish Server 8.0.0 en caso de no tenerlo instalado 
    - Archivo  / url  --  Documentation/readmeInstallGlassfishServer8.0.0.md

5. Configurar el DataSource  PersonaPool / PersonaDB  dentro de Glassfish 
    - Archivo / url  --  Documentation/readmeConfigurateDataSourceGlassfish.md

6. Configurar el DataSource  UsuarioPool / UsuarioDB  dentro de Glassfish 
    - Archivo / url  --  Documentation/readmeConfigurateDataSourceGlassfish.md

7. Configurar los usuarios dentro de Glassfish
    - Archivo / url  -- Documentation/readmeConfigureUsers.md

7. Seleccionar el proyecto en Apache Netbeans 26 IDE en  Projects y ejecutar el proyecto (run)

8. Te saldrá un recuadro pequeño donde te pedirá que insertes tanto el Username como el password 

8.1. Usuario Rol Admin:
Username: admin
Password: 123

Ahora si quieres probar otro usuario tienes que borrar el historial de "Sistema SGA" y de "Listado de Personas"
Después en Chrome - borrar los datos de navegación 
Ahora puedes volver a ejecutar el proyecto y darle a (run)

8.2. Usuario Rol User:
Username: user
Password: 123

Ahora si quieres probar otro usuario tienes que borrar el historial de "Sistema SGA" y de "Listado de Personas"
Después en Chrome - borrar los datos de navegación 
Ahora puedes volver a ejecutar el proyecto y darle a (run)

8.3. Usuario Rol Guest:
Username: guest
Password: 123

