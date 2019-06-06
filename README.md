# IBMCloudAPICall
Hands On para construir una aplicación en NodeJs para invocar un API en IBM Cloud

## Índice

*
*
*

## Introducción 

En esta guía podrá ver la creación de una aplicación en NodeJS, para hacer la invocación de un API publicada en el portal de desarrolladores con el que cuenta IBM Cloud API Connect. 

# parte 1

Para realizar la creación de la aplicación, se dirige a la página principal de Cloud IBM en la cual pude acceder
por medio de la siguiente **URL** https://cloud.ibm.com/login/, una vez allí va a iniciar sesión con su cuenta
de IBM Cloud.

<img width="600" alt="1" src="https://user-images.githubusercontent.com/50923637/58988050-6fb58a00-87a6-11e9-9d23-6b0cf0cde805.png">

Una vez le haya dado clic en `log-in`, va a aparecer la siguiente pantalla.

<img width="600" alt="2" src="https://user-images.githubusercontent.com/50923637/58988061-73e1a780-87a6-11e9-9fad-3cab02af432b.png">

Luego de la autenticación de usuario y contraseña, se va a ver la página inicial de IBM Cloud donde puede
verificar los servicios y aplicaciones que tiene creados actualmente, Una vez allí se va a dirigir a el **menu de hamburguesa** el se encuentra en la parte superior izquierda de su pantalla, cuando se despliegue ese menu seleccione la opción Web Apps.

<img width="200" alt="4" src="https://user-images.githubusercontent.com/50923637/59062473-870a7b00-886b-11e9-9262-30173e570b03.png">

Luego de seleccionar la opción podrá ver la siguiente ventana.

<img width="600" alt="4" src="https://user-images.githubusercontent.com/50923637/59062645-f7190100-886b-11e9-824c-6f256bb95c01.png">

Luego de eso seleccione **Starter kits**, esto se encuentra en la parte izquiera, justo debajo de **Overview**.

<img width="600" alt="6" src="https://user-images.githubusercontent.com/50923637/59063338-7d821280-886d-11e9-94a1-1fbd7a01ba67.png">

Luego de seleccionar la opción podrá ver la siguiente ventana, donde usted tiene varios servicios que ofrece IBM Cloud para usted, en este caso se seleccionará la opción **Mean stack: MongoDb, EXpress.js, Angular, Node.js**. 

<img width="600" alt="7" src="https://user-images.githubusercontent.com/50923637/59063589-0dc05780-886e-11e9-8345-53967e87dc0b.png">

Luego de seleccionar la opción debe seleccionar el boton de **Create app**.

<img width="600" alt="8" src="https://user-images.githubusercontent.com/50923637/59063870-a8b93180-886e-11e9-8b1f-565ae438d3f6.png">

Luego usted podrá ver la siguiente ventana, en la cual debe colocar un nombre de aplicación, y el resource group en el que va a clasificar o asignar el servicio que va a crear en IBM Cloud, despues de completar estos espacios usted debe dar clic en **Create**.

**Nota: El nombre de aplicación es utilizado como hostname, por lo que debe ser único e irrepetible con los anteriormente creados.**

<img width="600" alt="9" src="https://user-images.githubusercontent.com/50923637/59064442-e074a900-886f-11e9-8b3c-93089013d23a.png">

Una vez seleccione **Create App**, se genera el código de la aplicación.  A continuación debe seleccionar configurar `Continuos Delivery` para habilitar el uso de las herramientas de desarrollo para su aplicación (IBM Cloud Toolchain), si ya lo tiene habilitado puede omitir este paso.

<img width="600" alt="10" src="https://user-images.githubusercontent.com/50923637/59064597-3d705f00-8870-11e9-86c2-0691b182b158.png">

Puede seleccionar la plataforma en donde va a hacer el despliegue de la aplicación.  Se tienen como alternativas Virtual Servers (VSI), IBM Kuberentes Services y Cloud Foundry.  

En esta guía va a seleccionar ‘Deploy to Cloud Foundry’ para la implementación de la aplicación y su toolchain, luego de seleccionarlo y darle las especificaciones de memoria, región, organización y demas, usted debe dar clic en **Next**.

<img width="600" alt="11" src="https://user-images.githubusercontent.com/50923637/59065119-97bdef80-8871-11e9-87e0-4d4187819c96.png">

Una vez configuradas las opciones de despliegue puede visualizar las herramientas de DevOps para la aplicación dando clic en **View toolchain**.

<img width="600" alt="12" src="https://user-images.githubusercontent.com/50923637/59065229-d8b60400-8871-11e9-9631-dfe6687f3175.png">

Luego vera la siguiente ventana donde podrá ver el detalle del toolchain, que le permitirá editar, compilar, desplegar y ejecutar la aplicación. 

<img width="600" alt="13" src="https://user-images.githubusercontent.com/50923637/59065345-17e45500-8872-11e9-83f2-35908c0d8b5f.png">

Luego debe seleccionar la opción de delivery pipeline para ver que las etapas de ejecución de la aplicación hayan sido superadas satisfactoriamente.

<img width="600" alt="14" src="https://user-images.githubusercontent.com/50923637/59065505-77dafb80-8872-11e9-8067-861f37804243.png">

Ahora estando en el `pipeline` que muestra las tareas o pasos para **Build, Deploy and Health**.  Una vez se muestran en verde podrá acceder a la aplicación en el navegador.  

<img width="600" alt="15" src="https://user-images.githubusercontent.com/50923637/59065610-b8d31000-8872-11e9-9c54-24742bbbda92.png">

Para poder acceder a la URL de la aplicación busca la aplicación de Cloud Foundry en `Resource List`,  en la opción de `overview` de la aplicación que usted creo.

<img width="600" alt="16" src="https://user-images.githubusercontent.com/50923637/59066053-c210ac80-8873-11e9-821a-336d2ff8e484.png">
