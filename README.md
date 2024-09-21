# 4.1. Strategic-Level Domain-Driven Design.
## 4.1.1. EventStorming.
### 4.1.1.1 Candidate Context Discovery.

**Step 1:** *Unstructured Exploration*
Como primer paso en el EventStoring, iniciamos con una sesión de lluvia de ideas para identificar los eventos del dominio relacionados con el negocio analizado. Es fundamental expresar los acontecimientos del dominio en tiempo pasado para describir lo que ha ocurrido.

<img src="/assets/images/unstructuredexploration.png" width="1250"/>

**Step 2:** *Timelines*
Como segundo paso, revisamos los eventos de dominio generados y los organizamos en el orden en que suceden en el dominio. Es decir, los eventos deben comenzar con un camino exitoso que describa un escenario comercial favorable. Finalmente, una vez completado este camino exitoso, se pueden incorporar escenarios alternativos.

<img src="/assets/images/step2.png" width="1250"/>

**Step 3:** *Paint Points*
Después de organizar los eventos en una línea de tiempo, utilizamos esta visión general para destacar puntos clave a lo largo del proceso.

<img src="/assets/images/step3.png" width="1250"/>

**Step 4:** *Pivotal Points*
Una vez que completamos nuestra línea de eventos con los puntos problemáticos, identificamos eventos comerciales clave que señalan un cambio en el contexto o en la fase. A estos los llamamos eventos principales, y los señalamos con una barra vertical que divide los eventos anteriores y posteriores a dicho evento.

<img src="/assets/images/step4.png" width="1250"/>

**Step 5:** *Commands*
Los comandos de esta fase describen cómo ocurrió o se desarrolló el evento. En otras palabras, los comandos se escriben en forma de imperativo y especifican funciones del sistema en lugar de eventos del dominio.

<img src="/assets/images/step5.png" width="1250"/>

**Step 6:** *Policies*
Nuestra búsqueda actual se centra en reglas de políticas de automatización con la capacidad de llevar a cabo estas instrucciones. Es decir, una política de automatización representa una situación en la que se ejecuta un comando en respuesta a un evento. Entonces, cuando ocurre un evento específico del dominio, el comando se ejecuta automáticamente.

<img src="/assets/images/step6.png" width="1250"/>

**Step 7:** *Read Models*
El modelo de lectura es la representación de datos específica del dominio que el agente utiliza en esta etapa para determinar si debe ejecutar o no el comando. Por este motivo, definimos una vista de datos para cada comando, incluidas las notificaciones, los informes y los monitores del sistema.

<img src="/assets/images/step7.png" width="1250"/>

**Step 8:** *External Systems*
En esta etapa finalizamos el modelo con los sistemas externos, es decir, se considera sistema externo a todo sistema que no forme parte del dominio en el que se está trabajando.

<img src="/assets/images/step8.png" width="1250"/>

**Step 9:** *Aggregates*
Después de la introducción de todos los comandos y eventos, comenzamos a considerar ensamblar ideas similares en agregados que produzcan y reciban eventos.

<img src="/assets/images/step9.png" width="1250"/>

**Step 10:** *Bounded Contexts*
Luego buscamos agregados que representen funciones estrechamente vinculadas o que estén asociadas en función de regulaciones y que tengan significado entre sí. Es decir, los candidatos naturales para los límites del contexto restringido se producen mediante agrupaciones de agregados.

<img src="/assets/images/step10.png" width="1250"/>

### 4.1.1.2 Domain Message Flows Modeling.

  ## Scenario: Account creation and verification
  
Este diagrama describe el proceso de creación y verificación de una cuenta. Muestra cómo un propietario de restaurante o técnico crea una cuenta a través de un sistema RUC, que luego envía datos personales registrados al sitio web o aplicación móvil. Tras esto, el usuario es registrado, recibe un correo de verificación y finalmente, el sistema confirma la verificación de la cuenta.
  
<img src="/assets/images/accountcreationandverification.png" width="1250"/>

  ## Scenario: Collaborate & Request (Technical Issue Request)
El diagrama "Collaborate & Request" muestra el proceso de creación y gestión de una solicitud de soporte técnico. Un propietario de restaurante selecciona el tipo de creación y envía una solicitud a través del sistema de "Collaborate & Request". La solicitud es enviada a una aplicación móvil o web donde un técnico puede leerla y luego aceptarla para proceder con la resolución del problema técnico.

<img src="/assets/images/collaboraterequest.png" width="1250"/>

  ## Scenario: Collaborate & Request (Invitation Creation)
El segundo diagrama, "Collaborate & Request (Invitation Creation)", ilustra el proceso de creación y envío de invitaciones dentro de un sistema. El dueño del restaurante comienza seleccionando el tipo de creación, tras lo cual el sistema (Collaborate & Request) procede a crear una invitación. Luego, el sistema busca los correos electrónicos de los miembros a través de la aplicación web o móvil, y finalmente, las invitaciones se envían a través del sistema.

<img src="/assets/images/invitationcreation.png" width="1250"/>

  ## Scenario: Temperature & Managment
El siguiente diagrama describe un sistema de gestión de temperatura utilizando una solución IoT. Un dueño de restaurante o técnico inicializa un sensor de temperatura que envía los datos recolectados a la solución IoT. Esta solución procesa los datos, calcula la temperatura y los envía a una aplicación web o móvil para que el usuario pueda acceder a la información. El flujo de datos se muestra a través de eventos y comandos que conectan los diferentes sistemas y permiten la gestión eficiente de la temperatura en tiempo real.

<img src="/assets/images/temperaturemanagment.png" width="1250"/>

  ## Scenario: Calculate and send Metrics
El diagrama "Calculate and send Metrics", ilustra el proceso donde un dueño de restaurante interactúa con un sistema IoT para recopilar y enviar métricas a una aplicación web o móvil. A continuación, describo los pasos:
**Collect Metrics:** El dueño del restaurante envía un comando al sistema IoT para recolectar métricas.
**Received Metrics:** El sistema IoT envía las métricas recolectadas a una aplicación web o móvil.
**Calculated Metrics:** La aplicación calcula las métricas recibidas.
**Send Metrics:** La aplicación envía las métricas calculadas.
**Metrics Sent:** Las métricas se reciben en otra instancia de la aplicación.

<img src="/assets/images/calculatemetrics.png" width="1250"/>

  ## Scenario: Start Sensors to Collect Data
El diagrama representa un sistema IoT en el que un **dueño de restaurante** inicializa los sensores para recopilar datos. El proceso comienza cuando el usuario envía un comando al sistema IoT para activar los sensores. Luego, el sistema recopila los datos y los envía a una **aplicación web o móvil**, donde se calculan los parámetros necesarios. Finalmente, los datos calculados se envían de vuelta a la aplicación para que el usuario pueda acceder a ellos.

<img src="/assets/images/starsensors.png" width="1250"/>

  ## Scenario: Inventory Management
El diagrama "Inventory Management" muestra el escenario de gestión de inventarios utilizando una solución IoT. El proceso comienza cuando el **dueño del restaurante** recibe suministros y los agrega al inventario. Una vez que los suministros son añadidos, el sistema de **gestión de inventarios** envía una alerta de bajo inventario al personal a través de la solución IoT. Si se necesita reabastecer, el inventario se actualiza automáticamente y el nivel de inventario se muestra en la **aplicación web o móvil**, donde el dueño puede monitorear la información en tiempo real.

<img src="/assets/images/inventorymanagment.png" width="1250"/>

  ## Scenario: Temperature sensor alert
Este diagrama muestra un escenario de alerta de sensor de temperatura utilizando una solución IoT. El proceso comienza cuando el **dueño del restaurante o técnico** inicia el monitoreo de temperatura. El sistema IoT supervisa la temperatura y, si hay una anomalía, envía una alerta al personal a través de la **aplicación web o móvil**. El personal ajusta la temperatura según sea necesario. Una vez que la temperatura vuelve a estar dentro del rango adecuado, la aplicación actualiza la información para confirmar que el problema ha sido resuelto.

<img src="/assets/images/temperaturesensor.png" width="1250"/>

El diagrama describe el proceso de creación y verificación de cuentas en un sistema de software. Comienza con la **comunicación entrante**, donde se reciben solicitudes de creación de cuenta. Luego, en la sección de **Lenguaje ubicuo**, se detallan los pasos de "Creación de cuenta", "Información iniciada" y "Cuenta acreditada". Finalmente, en la **comunicación saliente**, los mensajes se envían a un sistema de registro y a un proceso de verificación de cuentas, asegurando que las cuentas sean verificadas y registradas correctamente.
