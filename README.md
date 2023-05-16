<h1 align="center">FastLogistics - Proyecto JAVA Fundación Esplai</h1>

FastLogistics surgió gracias a la unión de ideas junto a mi compañero, sobre la repartición de productos a domicilio y una empresa de limpieza.

#### La aplicación contiene 3 tipos de usuarios.
- repartidor
- limpiador
- administrador

#### Repartidor
En el caso de que tengamos un empleado con rol de *repartidor*, ese usuario, al iniciar su jornada laboral, verá que al iniciar sesión en
la plataforma, tiene una serie de tareas, donde aparece la dirección de entrega pendientes. Cuando el usuario pulsa en una tarea, verá los 
productos asignaos a esa dirección. Cuando el usuario haya completa dicha tarea, simplemente tenrá que pulsar el check al lado de caa tarea y
figurará al administrador como completada.

#### Limpiador

Este usuario tiene las herramientas para solicitar productos que requiera en una dirección en específica. El usuario puede selecionar alguna 
calle que está disponible en la base de datos adjunta en el respositorio. Al rellenar el campo de la dirección, en una lista desplegable,
puede selecionar los productos que requiere en la dirección especificada anteriormente. Al pulsar el boton de *enviar*, esta tarea se le 
asignará al usuario con rol de repartidor que tenga menos tareas, y en el caso de que todos los repartidores tengan la misma cantidad, se
selecionará aleatoriamente la tarea a un usuario.

#### Administrador

Al iniciar sesión en el usuario con rol de administrador, verá que tiene todos los usuarios repartidor, con las tareas completadas y no completadas
hasta el momento, si el repartidor completa una tarea mientras el usuario administrador está logeado, será necesario recargar la página.

El administrador, tiene como privilegios el poder eliminar las tareas, si ve que una tarea de X usuario ya está compleada, podrá eliminarla de la lista, y si no, le saldrá una 
advertencia.

También tiene la opción de poder dar de alta a nuevos usuarios, sin tener que crearlos desde la base de datos.

### Base de Datos

La base de datos, creado con **MYSQL** con el IDE **MYSQL WORKBENCH** contiene difetentes tablas.
- usuarios
- productos
- tareas
- productostareas

Estas tablas se relacionan entre sí, para poder hacer las peticiones correctamente desde la API.
La BBDD contiene información que nos ha servido para hacer pruebas, para solucionar bugs antes de la presentación del proyecto.
<br><br>*La BBDD no contiene ningún dato real. La información disponible en esta, ha sido facilitada por la IA CHATGPT - OPENAI*

### API
La API que hemos creado para este proyecto está realizado en JAVA, gracias a Spring Boot en el IDE de Eclipse de Oracle.
Esta API recibe peticiones desde el FrontEnd, pasa por la API y hace la solicitud correspondiente a la BBDD, y vuelve a enviarlo a la web. Desde el Front, la información se envía
y se recibe en formason JSON, para el mejor tratado de datos y por seguridad.


## Futuras Mejoras

- Agregar la API de Google Maps
- Continuar con la migración a React
- Ocultar las tareas completadas en el usuario administrador
- Mejorar el diseño de la web
- Los usuarios con rol de *limpiador* y *repartidor* tengan una aplicación móvil para mejor comodidad.









