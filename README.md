# Capítulo IV Solution Software Design

## 4.1 Strategic-Level Domain-Driven Design

En esta sección, como equipo, introducimos y explicamos el proceso realizado para tomar decisiones de nivel estratégico aplicando Domain-Driven Design (DDD). Este enfoque nos permitió alinear nuestra arquitectura de software con las necesidades del negocio, asegurando que cada componente del sistema esté optimizado para su propósito específico. A través de DDD, identificamos los dominios clave y establecimos una base sólida para el desarrollo de nuestro sistema avanzado de refrigeración para restaurantes.

### 4.1.1 EventStorming

En esta sección, como equipo, explicamos y evidenciamos el proceso de EventStorming, con el objetivo de plantear una primera aproximación al modelado de nivel general para el dominio del problema. Organizamos una sesión de EventStorming de 1 a 2 horas para concentrar nuestros esfuerzos y evitar extender el proceso innecesariamente. Durante la sesión, realizamos actividades específicas para identificar eventos clave y mapear el flujo de trabajo del sistema. Incluimos capturas de lo elaborado en la herramienta indicada para ilustrar nuestro proceso.

#### 4.1.1.1 Candidate Context Discovery

En esta sección, como equipo, explicamos y evidenciamos el proceso realizado para la sesión de Candidate Context Discovery, partiendo del dominio modelado en EventStorming. Utilizamos técnicas como start-with-value, start-with-simple y look-for-pivotal-events para identificar los bounded contexts. Esta sesión, que no duró más de 2 horas, nos permitió descomponer el timeline en pasos secuenciales y reconocer eventos clave que indican cambios de estado en el proceso de negocio. Complementamos la explicación con capturas de los cambios progresivos del EventStorm.

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

#### 4.1.1.2 Domain Message Flows Modeling

En esta sección, como equipo, explicamos y evidenciamos el proceso seguido para visualizar cómo deben colaborar los bounded contexts para resolver los casos que se presentan en el negocio para los usuarios del sistema. Aplicamos la técnica de visualización Domain Storytelling para mapear estas interacciones. Complementamos la explicación con capturas en imágenes de los diagramas de Domain Storytelling elaborados, mostrando cómo los diferentes contextos se comunican y colaboran para cumplir con los requisitos del negocio.

  ##### Scenario: Account creation and verification
  
Este diagrama describe el proceso de creación y verificación de una cuenta. Muestra cómo un propietario de restaurante o técnico crea una cuenta a través de un sistema RUC, que luego envía datos personales registrados al sitio web o aplicación móvil. Tras esto, el usuario es registrado, recibe un correo de verificación y finalmente, el sistema confirma la verificación de la cuenta.
  
<img src="/assets/images/accountcreationandverification.png" width="1250"/>

  ##### Scenario: Collaborate & Request (Technical Issue Request)
El diagrama "Collaborate & Request" muestra el proceso de creación y gestión de una solicitud de soporte técnico. Un propietario de restaurante selecciona el tipo de creación y envía una solicitud a través del sistema de "Collaborate & Request". La solicitud es enviada a una aplicación móvil o web donde un técnico puede leerla y luego aceptarla para proceder con la resolución del problema técnico.

<img src="/assets/images/collaboraterequest.png" width="1250"/>

  ##### Scenario: Collaborate & Request (Invitation Creation)
El segundo diagrama, "Collaborate & Request (Invitation Creation)", ilustra el proceso de creación y envío de invitaciones dentro de un sistema. El dueño del restaurante comienza seleccionando el tipo de creación, tras lo cual el sistema (Collaborate & Request) procede a crear una invitación. Luego, el sistema busca los correos electrónicos de los miembros a través de la aplicación web o móvil, y finalmente, las invitaciones se envían a través del sistema.

<img src="/assets/images/invitationcreation.png" width="1250"/>

  ##### Scenario: Temperature & Managment
El siguiente diagrama describe un sistema de gestión de temperatura utilizando una solución IoT. Un dueño de restaurante o técnico inicializa un sensor de temperatura que envía los datos recolectados a la solución IoT. Esta solución procesa los datos, calcula la temperatura y los envía a una aplicación web o móvil para que el usuario pueda acceder a la información. El flujo de datos se muestra a través de eventos y comandos que conectan los diferentes sistemas y permiten la gestión eficiente de la temperatura en tiempo real.

<img src="/assets/images/temperaturemanagment.png" width="1250"/>

  ##### Scenario: Calculate and send Metrics
El diagrama "Calculate and send Metrics", ilustra el proceso donde un dueño de restaurante interactúa con un sistema IoT para recopilar y enviar métricas a una aplicación web o móvil. A continuación, describo los pasos:
**Collect Metrics:** El dueño del restaurante envía un comando al sistema IoT para recolectar métricas.
**Received Metrics:** El sistema IoT envía las métricas recolectadas a una aplicación web o móvil.
**Calculated Metrics:** La aplicación calcula las métricas recibidas.
**Send Metrics:** La aplicación envía las métricas calculadas.
**Metrics Sent:** Las métricas se reciben en otra instancia de la aplicación.

<img src="/assets/images/calculatemetrics.png" width="1250"/>

  ##### Scenario: Start Sensors to Collect Data
El diagrama representa un sistema IoT en el que un **dueño de restaurante** inicializa los sensores para recopilar datos. El proceso comienza cuando el usuario envía un comando al sistema IoT para activar los sensores. Luego, el sistema recopila los datos y los envía a una **aplicación web o móvil**, donde se calculan los parámetros necesarios. Finalmente, los datos calculados se envían de vuelta a la aplicación para que el usuario pueda acceder a ellos.

<img src="/assets/images/starsensors.png" width="1250"/>

  ##### Scenario: Inventory Management
El diagrama "Inventory Management" muestra el escenario de gestión de inventarios utilizando una solución IoT. El proceso comienza cuando el **dueño del restaurante** recibe suministros y los agrega al inventario. Una vez que los suministros son añadidos, el sistema de **gestión de inventarios** envía una alerta de bajo inventario al personal a través de la solución IoT. Si se necesita reabastecer, el inventario se actualiza automáticamente y el nivel de inventario se muestra en la **aplicación web o móvil**, donde el dueño puede monitorear la información en tiempo real.

<img src="/assets/images/inventorymanagment.png" width="1250"/>

 ##### Scenario: Temperature sensor alert
Este diagrama muestra un escenario de alerta de sensor de temperatura utilizando una solución IoT. El proceso comienza cuando el **dueño del restaurante o técnico** inicia el monitoreo de temperatura. El sistema IoT supervisa la temperatura y, si hay una anomalía, envía una alerta al personal a través de la **aplicación web o móvil**. El personal ajusta la temperatura según sea necesario. Una vez que la temperatura vuelve a estar dentro del rango adecuado, la aplicación actualiza la información para confirmar que el problema ha sido resuelto.

<img src="/assets/images/temperaturesensor.png" width="1250"/>

### 4.1.1.3 Bounded Context Canvases

En esta sección, como equipo, diseñamos nuestros candidate bounded contexts, detallando los criterios de diseño. Seleccionamos cada bounded context por orden de importancia y elaboramos su Bounded Context Canvas. Este proceso iterativo incluye los pasos de Context Overview Definition, Business Rules Distillation & Ubiquitous Language Capture, Capability Analysis, Capability Layering (si aplica), Dependencies Capture, y Design Critique. Este enfoque nos permite definir claramente los límites y responsabilidades de cada contexto, asegurando una arquitectura coherente y eficiente.

##### Iot Solutions

El diagrama describe cómo las acciones iniciadas desde la web, la aplicación móvil y la solución IoT recopilan datos, los envían para su análisis y luego calculan métricas que se devuelven a las aplicaciones web y móviles. Comienza con la comunicación entrante, donde se recopilan datos de diversas fuentes. Finalmente, en la comunicación saliente, los datos analizados y las métricas calculadas se envían de vuelta a las aplicaciones para su visualización.

<img src="/assets/images/Bounded_Context_Canvases_4.png" width="1250"/>

##### Inventory Management

El diagrama describe cómo se controla y actualiza el inventario, permitiendo visualizar si hay exceso o falta de productos, mediante la recepción y actualización de suministros en el sistema. Comienza con la comunicación entrante, donde se reciben suministros y se actualiza el inventario. Finalmente, en la comunicación saliente, los mensajes se envían para confirmar si los suministros fueron recibidos correctamente o si hubo algún error

<img src="/assets/images/Bounded_Context_Canvases_3.png" width="1250"/>

##### Collaborate & Request

El diagrama describe cómo los propietarios gestionan búsquedas o crean invitaciones, los miembros seleccionan correos electrónicos, los técnicos validan solicitudes o suben documentos, y los colaboradores reciben y envían solicitudes dentro del sistema. Comienza con la comunicación entrante, donde se reciben solicitudes de colaboración o búsqueda. Finalmente, en la comunicación saliente, los mensajes se envían a los colaboradores para completar las solicitudes.

<img src="/assets/images/Bounded_Context_Canvases_2.png" width="1250"/>

##### Account

El diagrama describe el proceso de creación y verificación de cuentas en un sistema de software. Comienza con la comunicación entrante, donde se reciben solicitudes de creación de cuenta. Finalmente,en la comunicación saliente, los mensajes se envían a un sistema de registro y a un proceso de verificación de cuentas, asegurando que las cuentas sean verificadas y registradas correctamente.

<img src="/assets/images/Bounded_Context_Canvases_1.png" width="1250"/>

### 4.1.2 Context Mapping

En esta sección, como equipo, explicamos y evidenciamos el proceso de elaboración de un conjunto de context maps, visualizaciones de las relaciones estructurales entre bounded contexts. Revisamos la información recolectada y la utilizamos para producir los diseños candidatos. 

Account Management y Collaborate & Request están interconectados: El contexto de Account Management permite a los usuarios crear invitaciones para colaborar con otros, facilitando así la formación de equipos y la gestión conjunta de tareas. Esta interacción es fundamental para fomentar un entorno de trabajo colaborativo, donde la creación de cuentas y la participación de miembros se vuelven esenciales para el funcionamiento eficaz del sistema.

Además, Account Management se relaciona con Inventory Management: En este contexto, los usuarios pueden acceder al registro de inventario, gestionar niveles de stock y supervisar aspectos críticos como la temperatura de los productos. Esta conexión asegura que los usuarios tengan control total sobre los recursos disponibles, optimizando la eficiencia operativa y permitiendo una rápida toma de decisiones.

Por otro lado, IoT Solutions está vinculado con Inventory Management: La recopilación de datos a través de sensores IoT permite monitorear condiciones como temperatura y humedad, lo que es vital para la gestión adecuada del inventario. Esta relación garantiza que los datos en tiempo real se integren en la administración de inventario, proporcionando alertas y análisis que mejoran la precisión y la capacidad de respuesta ante problemas potenciales.

Estas interacciones reflejan cómo cada bounded context se complementa y apoya, creando un ecosistema cohesivo que optimiza la gestión de cuentas, la colaboración, y el control del inventario a través de soluciones IoT. Este enfoque integrado proporciona a los usuarios una experiencia fluida y efectiva, alineando los procesos de negocio con las necesidades operativas del sistema. A través de este análisis, hemos identificado oportunidades para mejorar la eficiencia y la funcionalidad del sistema en su conjunto.


### 4.1.3 Software Architecture

En esta sección, como equipo, presentamos y explicamos la representación de la Arquitectura de Software para la solución, aplicando el C4 Model y utilizando la herramienta indicada. 

#### 4.1.3.1 Software Architecture System Landscape Diagram

En esta sección, como equipo, presentamos y explicamos el System Landscape Diagram. Este diagrama muestra una vista de alto nivel de todos los sistemas y componentes involucrados en la solución, sus interacciones y cómo se integran para formar el sistema completo.

#### 4.1.3.2 Software Architecture Context Level Diagrams

En esta sección, como equipo, presentamos en imagen el context diagram. Este diagrama muestra el sistema como un recuadro en el centro, rodeado por sus usuarios y otros sistemas con los que interactúa. Utilizamos la herramienta indicada para la elaboración del diagrama y proporcionamos una explicación detallada del mismo, destacando las interacciones clave y los flujos de información entre los diferentes componentes del sistema

#### 4.1.3.3 Software Architecture Container Level Diagrams

En esta sección, como equipo, presentamos y explicamos el Container Diagram. Este diagrama muestra los elementos de alto nivel de la arquitectura de software y cómo se distribuyen las responsabilidades entre ellos. También destacamos las principales decisiones de tecnología y cómo los containers se comunican entre sí, asegurando una integración eficiente y coherente de todos los componentes del sistema.

#### 4.1.3.4 Software Architecture Deployment Diagrams

En esta sección, como equipo, presentamos y explicamos los Deployment Diagrams. Estos diagramas muestran cómo los componentes de software se despliegan en la infraestructura física o virtual, detallando la distribución de los componentes en servidores, contenedores, y otros recursos de infraestructura.

## 4.2 Tactical-Level Domain-Driven Design

En este capítulo, como equipo, explicamos y presentamos nuestra propuesta para la perspectiva táctica del diseño de la solución de software. Incluimos una sección interna por cada bounded context, detallando las clases identificadas y su documentación.

### 4.2.1 Bounded Context: Account
El dominio de Account se centra en gestionar todas las interacciones y operaciones
asociadas con cuentas de usuario. Este dominio es responsable de manejar las cuentas de usuario, tanto para
editar como para actualizar su membresía.

**Diccionario de Clases:**

 En el Diccionario de Clases, hemos incluido 2 clases principales: UsserAccount y Role. Estas clases
 representan los elementos esenciales de nuestra plataforma y definen las entidades y se relaciona con el rol que tendra cada usuario en la plataforma
<img src="/assets/images/UserAccount.png"/>

<img src="/assets/images/Role1.png"/>

#### 4.2.1.1 Domain Layer

El Domain Layer de Account contiene la lógica de negocio relacionada con la gestión de cuentas de usuario, como creación, autenticación, roles y permisos.

  Entidades:
- **Account:** Almacena la información básica del usuario, como el correo electrónico, contraseña y roles.
- **Role:** Define los permisos asignados a los usuarios (administrador, técnico, personal de restaurante).
  
  Servicios:
- **AccountService:** Proporciona las operaciones relacionadas con la creación de cuentas, autenticación y gestión de perfiles.
- **RoleService:** Maneja las asignaciones de roles y permisos a cada cuenta.
  
#### 4.2.1.2 Interface Layer

  Descripción: El Interface Layer proporciona las interfaces y controladores que permiten la interacción entre los usuarios y el sistema.
  
  Componentes:
- **AccountController:** Maneja las solicitudes HTTP relacionadas con el inicio de sesión, registro y actualización de perfiles.
- **SessionManager:** Gestiona las sesiones de usuario y el estado de autenticación.
- **ProfileView:** Proporciona las interfaces de usuario para visualizar y actualizar la información de la cuenta.
  
#### 4.2.1.3 Application Layer

  Descripción: El Application Layer coordina las operaciones entre el dominio y la infraestructura, manejando las reglas de negocio para las cuentas de usuario.
  Servicios:
- **AuthenticationService:** Proporciona la autenticación de usuarios, validación de credenciales y generación de tokens.
- **UserProfileService:** Gestiona las interacciones entre la capa de dominio y la interfaz de usuario para actualizar la información de la cuenta.
  
#### 4.2.1.4 Infrastructure Layer
  Descripción: El Infrastructure Layer soporta las operaciones relacionadas con la persistencia de datos, redes y almacenamiento de credenciales de usuarios.
  Componentes:
- **AccountRepository:** Almacena y recupera información de las cuentas desde la base de datos.
- **SecurityManager:** Proporciona la encriptación de contraseñas y seguridad en el acceso a los datos.
- **EmailService:** Maneja las notificaciones por correo, como la recuperación de contraseñas o alertas de seguridad.

#### 4.2.1.5 Bounded Context Software Architecture Component Level Diagrams
#### 4.2.1.6 Bounded Context Software Architecture Code Level Diagrams

### 4.2.2 Bounded Context: Collaborate & Request
En el dominio de Collaborate $ Request se centra en gestionar la logica de negocio para la creacion y gestión de solicitudes al personas tecnico

**Diccionario de Clases:**

En el Diccionario de Clases, hemos incluido 2 clases principales: MaintenanceRequest y Technician. Estas clases
 representan los elementos el funcionamiento de las solicitudes al personal tecnico
<img src="/assets/images/Maintenance.jpg"/>

<img src="/assets/images/Technician.jpg"/>

#### 4.2.2.1 Domain Layer

  Descripción: Gestiona la lógica de negocio para la creación y gestión de solicitudes de soporte técnico o invitaciones en el sistema.
  
  Entidades:
- **Request:** Representa las solicitudes de soporte enviadas por los usuarios.
- **TechnicianProfile:** Almacena la información de los técnicos asignados a resolver las solicitudes.

  Servicios:
- **RequestService:** Maneja la creación, actualización y seguimiento de las solicitudes de soporte.
- 
#### 4.2.2.2 Interface Layer

  Descripción: Proporciona las interfaces que permiten a los usuarios enviar y gestionar solicitudes de soporte o invitaciones.
  
  Componentes:
- **RequestController:** Controla las interacciones entre el usuario y el sistema para enviar solicitudes.
- **InvitationController:** Permite la creación y envío de invitaciones a través del sistema.
- **TechnicianDashboard:** Visualiza las solicitudes asignadas a cada técnico.
  
#### 4.2.2.3 Application Layer

  Descripción: Coordina las interacciones entre las solicitudes de soporte y los técnicos encargados de resolverlas.
  
  Servicios:
- **RequestManagementService:** Orquesta las operaciones de asignación de solicitudes a los técnicos y realiza seguimiento.
- **InvitationService:** Gestiona la creación y envío de invitaciones dentro del sistema.
  
#### 4.2.2.4 Infrastructure Layer

  Descripción: Gestiona las operaciones relacionadas con el almacenamiento y notificaciones de las solicitudes de soporte.
  
  Componentes:
- **RequestRepository:** Almacena y recupera las solicitudes de soporte.
- **NotificationService:** Envía alertas a los técnicos cuando se asigna una solicitud.
#### 4.2.2.5 Bounded Context Software Architecture Component Level Diagrams
#### 4.2.2.6 Bounded Context Software Architecture Code Level Diagrams

### 4.2.3 Bounded Context: Inventory Management

En el dominio de Inventory Management se centra en gestionar la logica del inventario, control de insumos y alertas.

**Diccionario de Clases:**

En el Diccionario de Clases, hemos incluido 4 clases principales: InventoryItem, InventoryReport, CoolingUnit y TemperatureSensor. Estas clases representan los elementos del funcionamiento del inventario y control de insumos.

<img src="/assets/images/Inventory.jpg"/>

<img src="/assets/images/InventoryReport.jpg"/>

<img src="/assets/images/Cooling.jpg"/>

<img src="/assets/images/TemperatureSensor.jpg"/>

#### 4.2.3.1 Domain Layer

  Descripción: Define la lógica de negocio para la gestión del inventario, control de stock y alertas de reabastecimiento.
  
  Entidades:
- **Inventory:** Representa el inventario del restaurante y sus niveles de stock.
- **Item:** Almacena la información de los insumos registrados en el sistema.
  
  Servicios:
- **InventoryService:** Gestiona el control de entradas y salidas de insumos, así como las alertas de bajo stock.

#### 4.2.3.2 Interface Layer

  Descripción: Ofrece interfaces y APIs para gestionar y visualizar el inventario en tiempo real.
  
  Componentes:
- **InventoryController:** Proporciona las interfaces de usuario para gestionar el inventario.
- **InventoryView:** Visualiza los niveles de inventario y las alertas de reabastecimiento.
- **IoTInventoryMonitor:** Integra los sensores IoT para monitorear los niveles de inventario.
  
#### 4.2.3.3 Application Layer

  Descripción: Coordina la gestión de inventarios y las operaciones automáticas como el envío de alertas de bajo stock.
  Servicios:
- **StockMonitoringService:** Monitorea los niveles de stock en tiempo real utilizando los sensores IoT.
- **ReplenishmentService:** Gestiona las órdenes de reabastecimiento cuando se detecta un bajo inventario.
  
#### 4.2.3.4 Infrastructure Layer

  Descripción: Soporta las operaciones de almacenamiento y conectividad con los dispositivos IoT para la gestión del inventario.
  
  Componentes:
- **InventoryRepository:** Almacena los datos de inventario y registros de entradas y salidas.
- **IoTGateway:** Conecta los sensores de inventario con el sistema central para transmitir los datos en tiempo real.
  
#### 4.2.3.5 Bounded Context Software Architecture Component Level Diagrams
#### 4.2.3.6 Bounded Context Software Architecture Code Level Diagrams

### 4.2.4 Bounded Context: IoT Solutions

| Nombre     | IoTSensor        |
|------------|------------------|
| Descripción| Monitoreo de temperatura en unidades de refrigeración. |
| **Atributos** | **Relaciones** | **Métodos** |
| `sensorID`  | String | Composición | `TemperatureController` | `monitorTemperature()` |
| `location`  | String | Agregación | `RefrigerationUnit` | `adjustTemperature()` |
| `temperature` | Float | | | `sendAlert()` |
| `status`    | Boolean | | | `logData()` |

#### 4.2.4.1 Domain Layer

  Descripción: Gestiona la lógica de negocio relacionada con el monitoreo y control de los sensores IoT instalados en las unidades de refrigeración.
  
  Entidades:
- **IoTSensor:** Representa los sensores de temperatura instalados en los equipos de refrigeración.
- **TemperatureController:** Maneja los ajustes automáticos de las temperaturas en base a los datos recogidos por los sensores.
  
Servicios:
- **IoTMonitoringService:** Monitorea en tiempo real los datos de los sensores IoT y ajusta las temperaturas según sea necesario.
  
#### 4.2.4.2 Interface Layer
  Descripción: Proporciona las interfaces para que los usuarios puedan monitorear y ajustar los datos de los sensores IoT.
  
  Componentes:
- **IoTControlPanel:** Visualiza los datos de los sensores y permite a los usuarios ajustar manualmente las temperaturas.
- **TemperatureDashboard:** Muestra los datos históricos y las tendencias de temperatura para mejorar la toma de decisiones.
  
#### 4.2.4.3 Application Layer

  Descripción: Coordina las interacciones entre los sensores IoT y los controladores de temperatura para mantener la temperatura óptima.
  
  Servicios:
- **TemperatureAdjustmentService:** Coordina los ajustes de temperatura automáticos en base a los datos de los sensores.
- **AlertService:** Envía notificaciones cuando se detectan temperaturas fuera del rango óptimo.
  
#### 4.2.4.4 Infrastructure Layer

  Descripción: Gestiona la conectividad y almacenamiento de los datos generados por los sensores IoT.
  
  Componentes:
- **IoTDataStorage:** Almacena los datos generados por los sensores IoT.
- **SensorGateway:** Conecta los sensores IoT con el sistema central para la transmisión de datos en tiempo real.
  
#### 4.2.4.5 Bounded Context Software Architecture Component Level Diagrams
#### 4.2.4.6 Bounded Context Software Architecture Code Level Diagrams


