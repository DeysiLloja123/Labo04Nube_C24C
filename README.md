# Labo04Nube_C24C
Laboratorio de la semana 04 NUBE DEYSI LLOJA


En la presente documentaciòn se abordara la explicaciòn detallada con cada uno de los procedimientos que se realizo para la creaciòn del DockerFile  y sus respectivas cconfiguraciones ya sea de la instancia creada, del git, del dockert, etc:


En primera instancia se ha creado una apliciòn web simple utilizando Node.js y el framework Express.js. Si bien Express.js es un framework de Node.js que facilita la creación de aplicaciones web y APIs. Deentro de nuestro código en particular se ha creado un servidor web que sirve archivos estáticos y define algunas rutas para diferentes URL.

Por otro lado se han definido tres rutas diferentes que corresponden a URLs específicas.Es decir que cuando un cliente accede a la ruta "/", "/clientes" o "/productos", Express enviará como respuesta el archivo HTML correspondiente desde el directorio "static". Esto se hace utilizando el método res.sendFile.
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/70409e90-5c93-42c1-b9bd-f3eff6628eb4)
Asi mismo  dentro del codigo se ha definido que el servidor en expres escuchara en el puerto 5000. Cuando se inicia el servidor, se muestra un mensaje en la consola indicando en qué puerto está escuchando.

En la sisguentes capturas se muestra el codigo de los archivos html de neustra aplicaciòn que el cliente observara al momento de navegar con la aplicaciòn:


Archivo de Index.html: Dentro de este se mostrara la pagina de inicio de la empresa Acme:
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/303d3c97-e16b-4059-a0b6-5d12b924c41b)


Archivo de cientes.html: Dentro de este se implemento el codigo necesario que nos ha permitido mostrar en la vista un lisdo de 3 clientes de la empresa acme con sus respectivas descripciones:
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/6afbccb7-d6be-473d-8b62-1a4278dc4277)
.

Mientras que dentro del archivo productos.html se mostrara el listado de los 4 productos que ofrece la empresa ACME, Si bien se muestra de manera ordenada para que el cliente pueda visualizar.
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/fffd0432-ed9b-47bc-bc5f-e105becb96e1)


Asi mismo se mostraran las vistas de la aplicaciòn de express que corre en el puerto 5000 con sus respectivas rutas:

Pagina de inicio: Esta vista se muestra bajo la primera ruta que es (/), donde se muestra la pagina de inicio de la aplicaciòn ACME y representa al archivo inicio.html
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/8c83ce4a-d910-4139-8681-39c10cd1e472)


Pagina de /clientes:  Si bien estavista muestra la vista de la ruta (/clientes), que mostrara el listado de los clientes que pertenecen a la empresa Acme.
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/e306d83a-aeae-4a7c-8f9e-0f9c03f5e680)


Y finamente la vista de la pagina de productos: Esta vista le permite al cliente observar el listad de los productos y que el cliente pueda observar algunas descripciones del producto tales como el nombre, el precio y color.
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/92874711-5928-4b49-a676-a1307a472d84)

![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/c3f5e060-e04e-46e8-9ff0-6adb8ab59d72)

Despuès de haber finalizado con la creaciòn de la aplicaciòn de express con sus respectivas cistas, se empezo con los procedimientos necesarios para crear nuestro dockerfile, si bien  para ello se realizaron muchas actividades como la creaciòn y lanzamiento de la instancia, la ejecuciòn del Git hast, la crecaiòn del repositorio publico, etc:


1. Primero empezaremos creando nuestra instancia con las que se trabajara, para luego dentro de su respectiva configuraciòn crear las claves que nos permitiran conectarnos al ubuntu,  y luego lanzar la instancia. 
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/9e6602b5-88da-4d72-89b0-6aa509d52776)


2. Despuès de haber lanzado la intancia, deberemos de seleccionar la intancia y verificar la informaciòn necesaria que nos permitira conectarnos tales como la direcciòn IPv4 publica de la instancia  y su respectivo DNS.
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/9e6872d3-027a-4acc-8e02-c0947d7d0d4a)

CREACIÒN DEL REPOSITORIO:

3. Si bien como requesito fundamental para crear nuestro dockerfile de la aplicaciòn expres, debemos de tener un repositorio con nuestra cuenta de git personal, para ello ingresaremos al git hub, y crearemos un nuevo repositorio donde clonaremos las carpetas y archivos de la aplicaciòn.
   
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/3fdc3fc8-3d5a-4fea-8a18-7abb53394f02)

Se clono el repositorio y se subieron los archivos de la aplicaciòn al repsoitorio:
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/db214011-64af-43ef-b746-2ba27c2380bf)


CONEXION CON EL UBUNTU:

4. Si bien despuès de haber creado la instancia correspondiente se ha realizado la conexiòn al ubunto y la descarga, instalaciòn y configuracaiòn del Docker:
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/2117baaa-1132-4f32-b71c-b2d8e83ee5a6)


![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/2cc98599-dcec-4927-b753-f83459e5ef7a)

5. Ya que nos pide lanzar nuestra aplicaciòn de expres en el puerto 9000, se ha agregado una nueva regla de entrada que corra en el puerto 9000: Ya que la instancia server-lab04 fue creada con un puerto de 22, y por ello al momento de eecutar la aplicaciòn nos saldra errro, para evitarnos los problemas màs a delante se realizò la configuraciòn del puerto.
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/8ec9c546-821c-4eeb-abbf-d1a4f45af59a)

![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/8d346823-b363-410b-8e31-fcec27f48321)


6. Instalamos los paquetes y herramientas necesarios para habilitar la descarga e instalación segura de software en tu sistema Ubuntu o Debian, especialmente cuando se trata de repositorios que utilizan el protocolo HTTPS
 ![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/7adbcbf0-978a-4c00-9a2a-c0d79cfef5b6)

el comando sudo snap intall docker nos permitira instalar la nueva versiòn del  docker:
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/63c58862-7ca9-42bb-a025-e089c72b15b3)


7. posteriormente se debe de verificar el estado del docker para validar que se haya instalado adecuadamente:
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/4200bc2d-f0e6-48ae-86ca-2dab74af459a)

8. Por consiguente despuès de veridficar el estado dl docker, empesaremos con los pasos para la creaciòn de nuestro archivo Dockerfile que expondra nuestra aplicaciòn express en el puerto 9000.  Si bien para ello debemos de ejecutar el comando nano Dockerfile, este comando se encargara de crear el archivo de nuestra aplicaciòn y nos permitira modificarlo.
   ![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/4f269694-05e2-4e7c-99ce-3a1305b4d45b)



9. Por condiguente en un archivo de block de notas copiaremos la estructura del DockerFile que se construira, para ello debemos de colocar tal como se muestra en la siguente imagen, sumandole a este nuestro correo donde con la que se ha creado el repsoitorio y el link del git para su respectiva clonaciòn, para luego colocar e nombre del repositorio con la que se validara y el puerto que expondra en nuestro caso debe de exponer la aplicaciòn el el puerto 9000.
    
    block de notas:
   ![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/6883fa61-e4cf-4225-9276-842d87e72f14)


   Creamos el archivo dockerfile:
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/475fef6b-67c2-4fef-8906-e4a1ffe54f79)

11.  Por consiguente, mediante el comando docker build . se construira una imagen de Docker a partir de un archivo llamado "Dockerfile", que leera nuestra aplicaciòn de express.
    ![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/0efea145-c533-4452-8879-d6d35f6dd461)

13. Mediante el comando docker images, listamos las imágenes  que están almacenadas en el Docker, en este caso se observa a la imagen creada llamada none y su respectivo id: Entonces mediante el comando docker tag acompañado del id de la imagen se realizará el cambio de nombre o de la etiqueta en este caso se llamará labo04deysi.

![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/a6c0c34e-c5a4-4038-a9ba-b854c1aa409e)


14. Por consiguiente se ejecutó el siguiente comando para ejecutar el contenedor de la imagen labo4deysi y que la aplicación que se encuentra dentro de este corra en el puerto 9000.
    
![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/7fe15071-4c3c-4bb4-9150-4bcbe62d5ea4)
Tal como se puede observar en la imagen, nos indica que nuestra aplicaciòn de express del node index,js se esta ejecutando en el puerto 9000, y cuando nostros ingresemos nuestra ip de la instancia y la el puerto 9000 màs la ruta ya sea (/), (/productos) y la ruta (/clientes), podremos observar las vistas de nuestra aplicaciòn:



5. Mostrar el URL

ip:9000

![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/0bee5fd3-843c-4f13-ae85-db190031c71e)


ip:9000/clientes

![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/fdbb022b-e8f4-4931-bd3c-241bf3ba4ce1)

ip:9000/productos

![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/780d3c95-fe31-412c-b692-c690220ef21b)

![image](https://github.com/Tecsupsoft/lab04-microservicios-DeysiLloja123/assets/129902954/3e98b64a-8256-4914-ac36-0ab454e3f7d6)

Finalmente se concluye que se ha logrado desplegar nuestra aplicación al docker, si bien para ello fue de suma importancia crear nuestro repositorio personal de tipo público para alojar ahi el código, estableciendo una base sólida para el control de versiones y la colaboración. Luego, se tuvo que aplicación a este repositorio, asegurando su disponibilidad en línea. A continuación, diseñó un Dockerfile, que contenía las instrucciones necesarias para construir una imagen de Docker configurada para ejecutar la aplicación en el puerto 9000. Posteriormente, se construyó la imagen con Docker y se ejecutó en un contenedor, permitiendo que la aplicación funcione en un ambiente aislado y controlado. Finalmente, se confirmó el correcto funcionamiento de la aplicación al navegar y probar las diversas rutas del proyecto, consolidando así el despliegue efectivo de tu aplicación en Docker y la adopción de buenas prácticas de desarrollo y colaboración. Si bien la actividad mencionada, se ha adquirido conocimientos esenciales sobre Docker al aprender a utilizar comandos fundamentales como `docker build`, `docker run`, y al crear un archivo Dockerfile para construir una imagen personalizada. En particular, hemos configurado una imagen Docker que ejecuta una aplicación Node.js Express en el puerto 5000, con rutas definidas para `/cliente` y `/producto`. Esto nos permitirá empaquetar y desplegar tu aplicación de manera más eficiente y controlada, beneficiándose de la versatilidad y aislamiento que Docker ofrece en el desarrollo y despliegue de aplicaciones.
