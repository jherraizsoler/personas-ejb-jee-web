

**Readme realizado por Jorge Herraiz Soler  este tiene todos los derechos**

- Prohibido distribuir este readme de ninguna forma sin el 
  consentimiento  del autor


# Procedimiento para configurar los  usuarios en Servidor Glassfish Server 8.0.0 (Netbeans)

## REQUERIMIENTOS TECNICOS Y  PRACTICOS

1. Tener Apache Netbeans IDE 26  
 
2. Tener instalado el jdk-21  
   | java -version 21.0.7 | 

3. Tener instalado GassFish Server 8.0.0  
   | Propiedades > Java (Pestaña) >> Java Platform JDK =>  JDK 21  | 

   Vinculo (revisar en caso de no tener instalado GassFish Server 8.0.0 )
        - Archivo  / url  --  Documentation/readmeInstallGlassfishServer8.0.0


## CONFIGURAR ROLES / USUARIOS EN    GLASSFISH   SERVER 

1. Dentro de Netbeans nos vamos a la pestaña Services
   (En caso de no encontrarlo  Arriba en el toolbar |  Window  > Services)

5. Ahora le damos click izquierdo a Servers y le damos click derecho y le damos
   a "View Domain Admin Console" al servidor Glassfish 8.0.0 ya configurado en el 
   archivo / url  -- Documentation/readmeInstallGlassfishServer8.0.0

6. Ahora en el Menu desplegable de la izquierda "Common Tasks" nos vamos a 
   "Configurations".

7. Una vez dentro de "Configurations" le damos a "default-config",  una vez dentro en "Security", le damos a "Realms" y le damos click en "file".

8. Ahora nos vamos a Manage Users (Botón) y le damos a "New" (Botón)

9. Escribimos lo siguiente para crear y configurar el usuario admin
    __________________________ admin ________________________________
    Realm Name:  file
    User ID: admin
    Group List:  ROLE_ADMIN:ROLE_USER:ROLE_GUEST
    New Password: 123
    Confirm New Password: 123
    
10. Y le das al botón "OK" para confirmar el usuario admin

9. Escribimos lo siguiente para crear y configurar el usuario user
    __________________________ user ________________________________
    Realm Name:  file
    User ID: user
    Group List:  ROLE_USER
    New Password: 123
    Confirm New Password: 123
    
10. Y le das al botón "OK" para confirmar el usuario user

9. Escribimos lo siguiente para crear y configurar el usuario guest
    __________________________ guest ________________________________
    Realm Name:  file
    User ID: guest
    Group List:  ROLE_GUEST
    New Password: 123
    Confirm New Password: 123
    
10. Y le das al botón "OK" para confirmar el usuario guest

11. Nos salimos de esta pagina web de configuración, cerramos esta pestaña.
    
  
