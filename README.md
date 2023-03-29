# Bot de Discord con VS CODE

*Es necesario tener instalado **Node.js**, **Visual Studio Code** y tener una cuenta en **Discord***

## Pasos para crear un Bot

1. Iniciar sesion en Discord

2. Crear un nuevo servidor (tambien se puede usar uno anteriormente creado)

3. Entrar a Discord Developer (https://discord.com/developers/)

4. Una vez en la página, entrar en el apartado 'Applications'

![imagen](https://user-images.githubusercontent.com/127338496/228414746-b47cf58b-86af-4a47-9dcc-ed193fd22a30.png)

5. En el apartado de aplicaciones, crear una nueva aplicación con el botón 'New Application'

![imagen](https://user-images.githubusercontent.com/127338496/228415047-8b58e28b-f2c4-4fce-93ef-cdc8258869f0.png)

*Una vez dentro, dispondrás de múltiples opciones, pero por ahora nos enfocaremos en lo básico para crear nuestro bot*

6. Iremos al apartado 'Bot', dentro de este apartado crearemos un nuevo bot con el botón 'Add Bot'

![imagen](https://user-images.githubusercontent.com/127338496/228415890-59ff0db4-9ebd-4956-a1b3-0bc1c5b97bee.png)
![imagen](https://user-images.githubusercontent.com/127338496/228415963-eaac6c6c-8840-4f3d-836a-8e1b6a35a9e2.png)

7. Dentro del mismo apartado, desactivaremos la opción 'Public Bot' y activaremos las opciones 'Precense Intent', 'Server Members Intent', 'Message Content Intent' y guardamos los cambios

![imagen](https://user-images.githubusercontent.com/127338496/228416580-be36fb46-0237-41f4-8078-21d17023c2a2.png)
![imagen](https://user-images.githubusercontent.com/127338496/228416648-54b97417-acb7-401f-b9b0-bf7a2a0410bb.png)

8. Nos dirigimos al apartado 'OAuth2' y vamos al submenú 'URL Generator'

![imagen](https://user-images.githubusercontent.com/127338496/228435341-9683b693-099b-4024-83ea-30fde4253496.png)

9. En 'Scopes' tildamos las opciones 'bot' y 'applications.commands'

![imagen](https://user-images.githubusercontent.com/127338496/228417093-ae349e09-5d81-4a7f-9f17-1575c0b6f562.png)

10. Aparecerá un nuevo formulario llamado 'Bot Permissions', en el que tildaremos la opción 'Administrator'

![imagen](https://user-images.githubusercontent.com/127338496/228417326-ad40d2bf-cb4e-47ea-a7ba-1acd2fa76a42.png)

11. En 'Generated URL' copiamos la URL que nos aparece y la pegamos en nuestro navegador

![imagen](https://user-images.githubusercontent.com/127338496/228417504-963ab370-7eb0-4499-a66b-301747011328.png)

12. Nos llevará a un menú para agregar nuestro bot a un servidor, lo agregaremos al server de nuestra preferencia

13. Una vez agregado al server, nos vamos a dirigir a Visual Studio Code, en el que haremos el resto del trabajo

14. Abriremos la carpeta donde tengamos los archivos, previamente descargados, con nuestro editor

15. Abriremos la terminal de VS Code (Ctrl - `)

16. Procedemos a instalar las dependencias necesarias para el funcionamiento de nuestro bot 

- En la terminal, escribiremos el comando 'npm i dotenv axios discord.js'

![imagen](https://user-images.githubusercontent.com/127338496/228420059-ac0d9f8d-e1e7-4945-afa2-3b7a1a426401.png)

17. Vamos a dirigirnos de nuevo a Discord Developer

- En el apartado 'Bot' copiaremos el token

![imagen](https://user-images.githubusercontent.com/127338496/228420903-27c3d327-f2d0-4910-9c84-5692ca8f6557.png)

18. En Visual Studio Code, crearemos un nuevo archivo al que le llamaremos '.env'

19. Dentro de este mismo archivo, escribiremos 'DISCORD_BOT_ID=token' (remplazar 'token' con el token copiado anteriormente)
  
 ![imagen](https://user-images.githubusercontent.com/127338496/228421967-f15d7b1e-8e3a-4276-a647-1f7f40e52f33.png)

 20. Para finalizar, escribiremos en la terminal 'node index.js', el comando va a retornar 'Bot is ready'
  
  - Una vez veamos este mensaje, ya nuestro bot va a estar activo y listo para usar 
  
 ![imagen](https://user-images.githubusercontent.com/127338496/228422660-a2c5e36f-6ebe-451f-8e00-c8a7f7db4b1c.png)
 
 ### Lista de comandos 
 
 **COMANDO | RESPUESTA**
 
 - ping | pong

 - quote | cita generada aleatoriamente (https://api.quotable.io/random)

 - hola | Hola, bienvenido a este servidor
 
## Incorporar Nodemon

- Nodemon nos permitirá editar nuestro código y que nuestro bot se actualice al guardar, sin necesidad de volver a iniciar nuestro bot. Para incorporarlo, debemos seguir los siguientes pasos:

1. En la terminal de VS Code escribiremos el comando 'npm init -yes'

![imagen](https://user-images.githubusercontent.com/127338496/228432359-b5d34b9d-c7a3-4419-8eb8-2eb8a8aee83e.png)

2. Instalaremos nodemon escribiendo 'npm i nodemon --D' en la terminal

![imagen](https://user-images.githubusercontent.com/127338496/228432412-f5da64f4-f5b8-48cb-af6a-28cdc9d13ad3.png)

3. Nos dirigimos al archivo 'package.json'

  - Buscaremos la siguiente linea, y remplazaremos el texto señalado con 'nodemon index.js'

![imagen](https://user-images.githubusercontent.com/127338496/228433964-0c8cec1f-cfdb-4769-b8e8-93117ec8182d.png)

  - Opcionalmente, podemos remplazar 'test' por otro nombre, pero en este caso lo dejaremos intacto

4. En la terminal, escribiremos npm run test (si has remplazado 'test' en tu archivo 'package.json', utiliza el nombre que colocaste en vez de test)

- De esta forma todos los cambios que realicemos en nuestro código se veran reflejados en nuestro bot una vez guardemos, una vez la consola retorne 'Bot is ready'

![imagen](https://user-images.githubusercontent.com/127338496/228434709-c23b37ff-12f7-4890-bcb6-50cd55648537.png)








