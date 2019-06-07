# IBMCloudAPICall
Hands On para construir una aplicación en NodeJs para invocar un API en IBM Cloud

## Índice

* Creación de la aplicación en IBM Cloud
* Paso opcional, Habilitación del continuos delivery toolchain.
* Modificaciones en el codigo de la interfaz de la pagina Web de la aplicación

## Introducción 

En esta guía podrá ver la creación de una aplicación en NodeJS, para hacer la invocación de un API publicada en el portal de desarrolladores con el que cuenta IBM Cloud API Connect. 

# Creación de la aplicación en IBM Cloud

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

### Paso Opcional

**Nota: Si ya tiene agregado el Continuos Delivery habilitado puede omitir los dos pasos siguientes.**

Una vez seleccione **Create App**, se genera el código de la aplicación.  A continuación debe seleccionar configurar `Continuos Delivery` para habilitar el uso de las herramientas de desarrollo para su aplicación (IBM Cloud Toolchain).

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

Después en la sección de Cloud Foundry apps va a seleccionar la aplicación que usted creo. 

<img width="600" alt="18" src="https://user-images.githubusercontent.com/50923637/59108061-ad79f600-88ff-11e9-971a-9a45d56803b6.png">

Después de haber seleccionado su aplicación vera la siguiente imagen en la cual para poder acceder a ella, se debe ubicar en la opción de `Overview` de la aplicación.

<img width="600" alt="19" src="https://user-images.githubusercontent.com/50923637/59108307-2f6a1f00-8900-11e9-89e7-859a40754213.png">

Después de estar en `Overview` debe seleccionar el vinculo que dice **Visit App URL***, par acceder a la pagina web creada.

<img width="600" alt="20" src="https://user-images.githubusercontent.com/50923637/59108553-c7680880-8900-11e9-80bc-ad9cfab31289.png">

Luego de seleccionar **Visit  App URL** puede ver la aplicación publicada. 

<img width="600" alt="21" src="https://user-images.githubusercontent.com/50923637/59108674-1ca41a00-8901-11e9-8d53-e42cfa98166a.png">

Luego nuevamente se debe dirigir a los App details de la aplicación para acceder a la sección de Eclipse Orion Web IDE, para realizar modificaciones en el código.

<img width="600" alt="22" src="https://user-images.githubusercontent.com/50923637/59108894-9805cb80-8901-11e9-842a-46a3531b94ed.png">

## Modificaciones en el codigo de la interfaz de la pagina Web de la aplicación
Después de seleccionar Orion web IDE hará las siguientes modificaciones en el código fuente.

El código que se muestra a continuación es la página web ajustada para agregar un valor ‘quantity’ que se envía como parámetro en la invocación del API  utilizada en el ejercicio. 

<img width="600" alt="23" src="https://user-images.githubusercontent.com/50923637/59109681-1c0c8300-8903-11e9-85df-5822948bac5e.png">

El código que se muestra a continuación corresponde a la vista de la aplicación en angular, y le permitirá hacer la invocación del API desde JavaScript.

<img width="600" alt="24" src="https://user-images.githubusercontent.com/50923637/59109808-59711080-8903-11e9-8f78-40cc44c2abd6.png">

Las siguientes son las modificaciones correspondientes realizadas en el código para modificar la pagina que anteriormente pudo ver al dar clic en **Visit App URL**.

### Modificación 1

```

<section>
    <header id="flex-header">
        <div class="cloud-header"></div>
        <h1>IBM Cloud</h1>
    </header>
    <main>
       <p align="center" style="font-size:28px;">
        Enter Quantity:
        <input type="text" ng-model="quantity"/>
        <button ng-click="getbalance(quantity)"  style="font-size: 14px;background-color: #e7e7e7; color: black;border: 2px solid black;">Balance</button>
      </p>
      
      <div style="font-size: 24px;">
	
	<table style="width:40%">
		 <tr>
			    <td>Quantity</td>
			    <td>{{quantity}}</td>
			  </tr>	
			  <tr>
			    <td>Balance</td> 
			    <td>{{value}}</td> 		    
			  </tr>	
			  <tr>			    
			    <td>Body</td>
			    <td>{{body}}</td>			    
			  </tr>	
			  <tr>			    
			    <td>Response</td>	
			    <td>{{response}}</td>					    
			  </tr>
			</table>
      </div>
    </main>
</section>


``` 

### Modificación 2

```

angular.module('MainView', [])
.controller('MainCtrl', ['$scope', function($scope) {
	
   $scope.response = "" ;
    $scope.body  = "" ;
    $scope.value = "" ;
    
    var request = require("request");

    $scope.getbalance = function(qval) {      
        
        var options = { method: 'GET',
        url: 'https://api.us.apiconnect.ibmcloud.com/damaya-demo-api-connect/sb/getBalance/status',
        qs: { balance: qval },
        headers: 
        { accept: 'application/json',
            'x-ibm-client-secret': 'U0bV7bO6vB8lS0jF6tF3uR2qI8qQ4vV2rF0aC1uI5uR2kP2mO7',
            'x-ibm-client-id': 'f3f81651-b2c7-456a-bf3d-02145a0b713f' } };
       
        request(options, function (error, response, body) {
          if (error) return console.error('Failed: %s', error.message);
        
          $scope.response = response ;
          $scope.body = body ;
          
          var obj = JSON.parse(body) ;
          $scope.value = obj.return ;
          
          console.log('Success: ', body);
        });
    } 
    
}]);


``` 

Después de las modificaciones realizadas al dar clic nuevamente en Visit App URL, podrá ver la pagina web con la invocación de la API publicada en API Connect.

<img width="600" alt="25" src="https://user-images.githubusercontent.com/50923637/59110582-0f892a00-8905-11e9-89f8-88982b7ecf9c.png">
