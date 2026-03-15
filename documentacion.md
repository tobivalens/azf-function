**INFORME LABORATORIO 2**

Inicialmente se instalaron las herramientas necesarias para trabajar con infraestructura en Microsoft Azure. Estas herramientas fueron Terraform y Azure CLI, las cuales permiten gestionar recursos en la nube mediante línea de comandos y automatizar el despliegue de infraestructura.

Posteriormente se clonó el repositorio proporcionado, el cual contenía la infraestructura definida mediante archivos de configuración de Terraform. En este repositorio se encontraban todos los archivos necesarios para desplegar una Azure Function junto con los recursos requeridos para su funcionamiento.

Una vez dentro de la carpeta del proyecto, se ejecutó el comando terraform init, el cual se encarga de inicializar el proyecto de Terraform. Este comando descarga el provider de Azure, que permite a Terraform interactuar con los servicios de la plataforma, y prepara el entorno para la ejecución de los despliegues.

Posteriormente se ejecutó el comando terraform apply, el cual analiza los archivos con extensión .tf y muestra los recursos que serán creados dentro de la infraestructura de Azure.

![Ejecución de terraform apply](imagenes/tf_apply.png)

Durante este proceso, el sistema solicitó el parámetro name_function, el cual corresponde al nombre que tendrá la función y los recursos asociados. En este caso se ingresó el nombre azfvalens22, que fue utilizado para crear los diferentes recursos necesarios para la ejecución de la función.

Una vez finalizada la creación de la infraestructura, Terraform mostró en la consola una URL de acceso generada automáticamente. Esta URL se obtiene gracias a la configuración definida en el archivo outputs.tf, que permite mostrar como salida la dirección para invocar la función creada.

La función definida puede ejecutarse desde el navegador o mediante solicitudes HTTP, accediendo a dicha URL.

![URL generada por Terraform](imagenes/url_prueba.png)

Al ingresar a la URL generada se pudo observar que la función responde correctamente, lo cual confirma que el despliegue de la infraestructura se realizó exitosamente.

![Prueba de la función desde el navegador](imagenes/url_navegador.png)

Posteriormente se accedió al portal de Azure, donde fue posible verificar que los recursos habían sido creados correctamente dentro de la plataforma.

![Creacion de recursos en azure ](imagenes/portal_azure.png)

Finalmente, al acceder al dominio de la Function App, se mostró la página predeterminada que indica que la aplicación de Azure Functions se encuentra en ejecución. Esto confirma que la infraestructura fue desplegada correctamente y que la aplicación está activa y funcionando dentro del entorno de Azure.

![Dominio de Azure Function activo](imagenes/dominio_azure.png)
