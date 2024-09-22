
# 1.1. Startup Profile


## 1.1.1. Descripción de la Startup

<p align=justify> 
Este proyecto busca implementar un sistema avanzado de refrigeración para restaurantes, integrando máquinas de enfriamiento con software especializado y sensores de temperatura conectados a un microprocesador. El sistema garantiza un control preciso de las temperaturas de los insumos y una gestión eficiente del inventario. Funciona mediante monitoreo en tiempo real, ajustes automáticos de temperatura, y programación de ciclos de enfriamiento. Además, gestiona el inventario registrando entradas y salidas de productos, y proporciona alertas de vencimiento. Los reportes históricos y el análisis de tendencias permiten mejorar continuamente el sistema para mantener la calidad óptima de los alimentos.

**Misión:**

En IOTécnicos, nuestra misión es revolucionar la industria de la refrigeración para restaurantes mediante soluciones tecnológicas avanzadas. Nos dedicamos a integrar máquinas de enfriamiento con software especializado y sensores de temperatura conectados a microprocesadores. Nuestro objetivo es garantizar un control preciso de las temperaturas de los insumos y una gestión eficiente del inventario, todo mientras proporcionamos alertas de vencimiento y reportes históricos. Así, contribuimos a mantener la calidad óptima de los alimentos y a mejorar la experiencia de los clientes en los restaurantes.

**Visión:**

Nos visualizamos como la principal referencia en tecnología de refrigeración para restaurantes. Aspiramos a crear un mundo donde cada establecimiento gastronómico cuente con sistemas inteligentes que optimicen el manejo de sus insumos y garanticen la seguridad alimentaria. Queremos transformar la forma en que los restaurantes se relacionan con la refrigeración, brindando eficiencia, confiabilidad y tranquilidad a nuestros clientes.
</p>


 
## 1.1.2. Perfiles de integrantes del equipo


| Díaz Gonzales, Víctor Yordi  - u20211C384 |  |
|----------|----------|
|Actualmente ando estudiando la carrera de Ingeniería de Software. Mi pasión por la programación empezó a temprana edad, donde actualmente me permite investigar, analizar y solucionar problemas de la vida cotidiana. Mi objetivo es desarrollar software de calidad que den soluciones innovadoras a la población. Cabe enfatizar que busco la colaboración activa en equipo para llegar a tener éxito en las metas o proyectos. | <img src="/Chapter1/images/student_victor.png" width="1250"/>|
|||

|  Márquez, Piero Stefano - u201816402 |  |
|----------|----------|
|Soy estudiante de 8to ciclo en la carrera Ingeniería de Software. Me considero alguien bastante práctico, directo y honesto. Puedo manejar diversos lenguajes y frameworks ya que un objetivo a corto plazo sería convertirme en un Full Stacks. Siento que aprendo rápido y no tengo problemas con trabajar con diferentes lenguajes o entornos.| <img src="/Chapter1/images/student_piero.png" width="1250"/>|
|||

| Navarro Chacon, Juan Jose - u20201f316 |  |
|----------|----------|
|Soy estudiante de la carrera Ingeniería de Software, actualmente estoy cursando el 8vo ciclo. Me considero una persona divertida, empática, responsable, creativa, honesta y sobre todo organizada en los planes que deseo realizar. Para el trabajo que vamos a realizar puedo aportar con el desarrollo del sistema, ya que tengo conocimientos ciertos lenguajes, además de ser responsable| <img src="/Chapter1/images/student_juanjose.png" width="1250"/>|
|||

| Patrocinio Escalante, Leonardo Walt -  u202017075 |  |
|----------|----------|
|Me considero una persona creativa, responsable y ordenada. Tengo experiencia trabajando en equipo, escucho las ideas de mis compañeros y me desempeño bien para el avance de los trabajos.| <img src="/Chapter1/images/student_leo.png" width="1250"/>|
|||


| Sánchez Ramírez, Diego Antonio - u202021367 |  |
|----------|----------|
|Soy un estudiante de la carrera de Ing. De Software en la Universidad de Ciencias Aplicadas (UPC). Estoy familiarizado con los lenguajes de programación C + + y HTML5, CSS y JS. Estoy en vías de aprender otros lenguajes para ser un ingeniero flexible a cualquier necesidad o problema que se presente.| <img src="/Chapter1/images/student_diego.png" width="1250"/>|
|||

| Zamora Rivera, Ismael Sebastian - u202116671 |  |
|----------|----------|
|Me llamo Ismael Sebastian Zamora Rivera. Tengo 20 años y estudio Ingeniería de Software. He adquirido experiencia en lenguajes de programación como C++, Python, HTML y SQL, lo que me ha permitido desarrollar diversos proyectos. Además, he participado en proyectos colaborativos que me han ayudado a fortalecer mis habilidades interpersonales y adaptarme a diferentes situaciones. | <img src="/Chapter1/images/student_victor.png" width="1250"/>|
|||

# 1.2. Solution Profile


## 1.2.1 Antecedentes y problemática

<u>**Problemática**</u>
<p align=justify> 
En los últimos años, la industria de la restauración ha experimentado un crecimiento considerable, acompañado de un incremento en las expectativas de los consumidores respecto a la calidad y seguridad de los alimentos. Según Paucar Luna et al. (2022), muchos empresarios están invirtiendo en restaurantes peruanos como resultado del auge gastronómico del país, pero deben esperar a que el Estado peruano los declare patrimonio cultural nacional y se establezcan normas de seguridad y calidad. Esto significa que deben abordar desde el lanzamiento y funcionamiento de nuevas empresas hasta la importancia de una legislación unívoca para las pequeñas y medianas empresas. La frescura y correcta conservación de los insumos se han convertido en aspectos clave para garantizar la satisfacción del cliente y el cumplimiento de las normativas sanitarias. Sin embargo, a pesar de los avances en tecnología de refrigeración, muchos restaurantes aún enfrentan desafíos en el control de las temperaturas de sus insumos, lo que puede llevar a desperdicios, pérdidas económicas y riesgos para la salud de los comensales. Este problema se agrava cuando la gestión de inventarios no es eficiente, ocasionando que se adquieran más productos de los necesarios o que se utilicen insumos en mal estado. Por lo tanto, surge la necesidad de un sistema que no solo monitoree y regule las temperaturas de los insumos, sino que también optimice la gestión del inventario.
</p>

**What (Qué):** El problema es la falta de un sistema integral en los restaurantes que permita un control preciso de las temperaturas de los insumos, junto con una gestión eficiente del inventario.

**Why (Por qué):** Es necesario garantizar la calidad y seguridad de los alimentos, minimizar el desperdicio, y optimizar los recursos, lo cual impacta directamente en la rentabilidad del restaurante y la satisfacción del cliente.

**Who (Quién):** Los principales afectados son los dueños y administradores de restaurantes que buscan mejorar la eficiencia operativa y cumplir con las normativas sanitarias, así como los empleados responsables del manejo de insumos.

**When (Cuándo):** Este problema es continuo y puede manifestarse en cualquier momento del año, especialmente durante picos de demanda o en condiciones ambientales adversas.

**Where (Dónde):** La problemática se presenta en restaurantes de cualquier tamaño y ubicación, pero es más crítica en aquellos con alta rotación de insumos perecederos.

**How (Cómo:** Actualmente, los restaurantes enfrentan dificultades para monitorear las temperaturas en tiempo real y carecen de herramientas que integren este monitoreo con la gestión de inventarios, lo que lleva a ineficiencias operativas y posibles incumplimientos sanitarios.

**How Much (Cuánto):** La falta de un sistema adecuado puede resultar en pérdidas económicas significativas debido al desperdicio de alimentos, multas por incumplimiento de normativas y pérdida de clientes debido a la baja calidad de los productos.

## 1.2.2 Lean UX Process.

### 1.2.2.1. Lean UX Problem Statements.

En esta seccion se presenta un problem statement del proyecto, la cual nos ayuda a enfocar o proyectar nuestra solucion e identificar los segmentos objetivos: 

En el sector de restaurantes, el personal enfrenta desafíos importantes relacionados con el control de calidad de los insumos y la gestión eficiente de inventarios. Además, los técnicos de mantenimiento necesitan un sistema que les facilite el acceso a solicitudes de trabajo de manera ágil y sencilla.

Los productos y servicios existentes no logran resolver adecuadamente estas necesidades, dejando una oportunidad para optimizar tanto la gestión interna de los restaurantes como la interacción entre el personal y los técnicos.

Nuestro producto, FrostChef, está diseñado para abordar estas carencias al ofrecer una plataforma que mejora el control de calidad de insumos, optimiza la gestión de inventarios, y proporciona a los técnicos de mantenimiento un portal eficiente para gestionar solicitudes de trabajo.

Nos enfocaremos inicialmente en el personal de restaurantes y los técnicos de mantenimiento, quienes enfrentan estos problemas diariamente.

Sabremos que hemos tenido éxito cuando el personal de los restaurantes reporte una mayor eficiencia en la gestión de inventarios, que esto se vea reflejado en ahorro de costes, y los técnicos reduzcan el tiempo de respuesta en un 50% a las solicitudes de mantenimiento.

### 1.2.2.2. Lean UX Assumptions.

### **User Assumptions**

Para esta sección, crearemos supuestos de cómo serían nuestros segmentos objetivos para poder tener una idea principal de sus características y poder refutarlos luego con una investigación y análisis más profundos:

#### **Segmentos Objetivos**

#### **Personal de Restaurante**

- **Edad**: Persona mayor en un rango de 22-50 años.  
- **Estado civil**: Soltero o casado.
- **Trabajo**: Pueden ser gerentes, personal de cocina, recepcionistas o mozos.  
  - La carga de trabajo puede variar según el cargo que ejercen (6-8 horas de trabajo).
  
- **Necesidades**:
  - Poder pagar los estudios, de ellos mismos o de sus hijos.
  - Cubrir los gastos del hogar.
  
- **Obstáculos**:
  - Altas cargas de trabajo en horarios variables.
  - Limitaciones en la gestión de inventarios y control de insumos debido a la falta de herramientas tecnológicas automatizadas.
  
---

#### **Técnico de Mantenimiento**

- **Edad**: Persona en un rango de 25-55 años.
- **Estado civil**: Soltero, casado o con hijos.
- **Trabajo**: Especialistas en mantenimiento de equipos de refrigeración, aire acondicionado y sistemas relacionados.
  - Trabajan de forma independiente o para empresas, con jornadas que pueden variar según las solicitudes de los clientes.

- **Necesidades**:
  - Tener acceso a trabajos constantes y mejor remunerados.
  - Reducir los tiempos de diagnóstico de fallas para incrementar la eficiencia en sus intervenciones.
  
- **Obstáculos**:
  - Dificultad para encontrar clientes o restaurantes que necesiten sus servicios de forma eficiente.
  - Falta de herramientas tecnológicas para llevar un control adecuado de sus trabajos y historial de servicios.



### **User's Outcomes & Benefits**

Para definir los beneficios que nuestros usuarios y clientes van a obtener mediante nuestro producto, realizaremos las siguientes preguntas clave:

#### ¿Qué es lo que mis clientes van a conseguir si utilizan mi producto o servicio?

**Primer segmento: Personal de restaurantes**  
El personal de restaurantes podrá:
- Conseguir una **gestión eficiente de inventarios** que les permitirá mantener control sobre sus insumos, evitando pérdidas por caducidad o mal manejo.
- Tener un **control automatizado de las temperaturas** de sus refrigeradoras y cámaras de almacenamiento, asegurando que los alimentos se mantengan en condiciones óptimas.
- Optimizar la **gestión energética**, reduciendo el consumo innecesario de electricidad mediante la regulación automática de temperaturas.

**Segundo segmento: Técnicos de mantenimiento**  
Los técnicos de mantenimiento podrán:
- Acceder a una **bolsa de trabajo** en la que encontrarán solicitudes de mantenimiento de restaurantes cercanos a su ubicación, facilitando la búsqueda de oportunidades laborales.
- Tener acceso a un sistema de **diagnóstico rápido ante fallos** en los equipos de refrigeración, lo que les permitirá identificar y solucionar problemas con mayor eficiencia.
- Llevar un **historial de trabajos realizados**, lo que les permitirá hacer seguimiento de sus intervenciones anteriores, facilitando futuras reparaciones.
- Establecer una **vinculación directa con negocios**, lo que podría fomentar relaciones a largo plazo y garantizar un flujo constante de trabajos.

#### ¿Qué beneficios podrían ellos ganar al usarlo?

Nuestra solución ofrece los siguientes beneficios:

**Segmento objetivo: Personal de restaurante**
- **Registro eficiente de espacios de inventario**: Mantener un control más preciso de los insumos disponibles.
- **Control automatizado de temperaturas**: Evitar fluctuaciones de temperatura que podrían comprometer la calidad de los alimentos.
- **Monitoreo de temperaturas en tiempo real**: Recibir alertas cuando la temperatura de los refrigeradores se desvíe de los rangos permitidos, evitando la pérdida de insumos.

**Segmento objetivo: Técnico de mantenimiento**
- **Mayor bolsa de trabajo**: Tendrán acceso a múltiples oportunidades de empleo en su área de especialización.
- **Diagnóstico rápido ante fallos**: Reducir el tiempo de inactividad de los equipos y agilizar los procesos de mantenimiento.
- **Historial de trabajos realizados**: Facilitará el seguimiento de problemas recurrentes y mejorará la eficiencia de futuras reparaciones.
- **Vinculación con negocios**: Establecer relaciones laborales duraderas con restaurantes que necesitan mantenimiento continuo.

#### ¿Qué comportamientos podrían observarse si ellos cumplen sus objetivos?

Para ambos segmentos, se podrían observar los siguientes comportamientos:

- **Personal de restaurante**: Mayor eficiencia operativa y ahorro en costos, ya que un mejor control de inventarios y temperaturas reducirá el desperdicio de alimentos y el consumo energético.
- **Técnicos de mantenimiento**: Mayor número de trabajos realizados y mejor gestión de su tiempo, al poder seleccionar las solicitudes más convenientes según su ubicación y especialización.

### **Business Assumptions**

Somos una empresa que busca dar soluciones alineadas con las últimas tecnologías disponibles en el mundo. De carácter abierto y recién conformado, contamos con poca experiencia en el rubro de la problemática que estamos eligiendo. Sin embargo, nuestro objetivo es innovar en el mercado objetivo con una solución disruptiva que se aleja de lo tradicional en Perú. Además, adoptaermos un enfoque de aprendizaje continuo mediante ciclos de prueba y validación rápida. Esto significa que nuestras metas serían:

- Testear nuestras hipótesis con prototipos funcionales mínimos (MVP) en los primeros clientes para obtener feedback constante y realizar iteraciones rápidas.
  
- Observar y medir el comportamiento de nuestros usuarios en escenarios reales de uso para ajustar nuestras soluciones según sus necesidades.
  
- Estar abiertos al cambio y ajustar nuestras prioridades conforme vayamos recolectando datos de uso, manteniendo siempre el enfoque en la mejora continua y la reducción de riesgos a través de experimentación.

### **Business Outcomes & Benefits**

Para lograr los resultados esperados por nuestros clientes y usuarios, realizaremos un **User Journey: Pirate Metrics** que nos permitirá identificar los puntos críticos de interacción entre el usuario y el sistema, asegurándonos de mejorar continuamente la experiencia y los beneficios ofrecidos.

#### Adquisición
- Restaurantes: Los restaurantes serán atraídos por la posibilidad de implementar una solución integral que les permita monitorear en tiempo real la temperatura de los insumos almacenados en refrigeradores y cámaras de almacenamiento. Esto se logrará mediante la integración de sensores IoT que registran y reportan las condiciones de temperatura constantemente, lo cual les ayudará a evitar pérdidas por fallos en la cadena de frío y reducir costos operativos al optimizar el uso de energía.
- Técnicos de mantenimiento: Los técnicos se sentirán atraídos por la posibilidad de acceder a una plataforma donde podrán encontrar fácilmente trabajos de mantenimiento en restaurantes locales que requieran soporte en sus equipos de refrigeración y otros electrodomésticos. Esto les abrirá una nueva bolsa de trabajo que centraliza las solicitudes de servicio, brindándoles una oportunidad única de incrementar sus ingresos de manera constante.

#### Retención
- Restaurantes: Para retener a los restaurantes, se les ofrecerá un sistema de monitoreo continuo de los sensores, enviando alertas automáticas cuando las temperaturas se desvíen de los rangos establecidos. Esta funcionalidad de prevención de fallos será clave para mantener la fidelidad de los usuarios, ya que evitará que sufran pérdidas por mal estado de los insumos.
- Técnicos de mantenimiento: Los técnicos serán retenidos gracias al acceso a una base de datos de historial de mantenimiento, que les permitirá llevar un registro de los trabajos realizados. Además, la plataforma garantizará un flujo constante de oportunidades laborales cercanas, lo cual fomentará la lealtad hacia la solución al hacer su día a día más eficiente y rentable.
#### Activación
- Restaurantes: La activación se logrará al demostrar rápidamente el valor de los sensores de temperatura mediante un proceso de instalación sencillo y la entrega inmediata de alertas y reportes en tiempo real. Al implementar el sistema, los restaurantes podrán visualizar de manera clara los beneficios del control automatizado, como la reducción de riesgos en la conservación de insumos.
 Técnicos de mantenimiento: Los técnicos podrán activar su perfil y empezar a recibir solicitudes de trabajo de manera inmediata, con notificaciones automáticas sobre los restaurantes que necesiten sus servicios. Al ofrecer una plataforma fácil de usar, los técnicos podrán rápidamente empezar a trabajar y ver los beneficios en forma de ingresos adicionales.
#### Ingresos
- Restaurantes: Los restaurantes generarán ingresos al reducir las pérdidas de insumos por mal almacenamiento o fallos en el equipo de refrigeración, optimizando así su operación. Además, la plataforma permitirá optimizar el consumo energético al regular automáticamente las temperaturas, generando ahorros significativos.
- Técnicos de mantenimiento: Los técnicos podrán aumentar sus ingresos al tener acceso a una mayor cantidad de trabajos en su área local, permitiendo optimizar sus tiempos y especializarse en intervenciones rápidas y eficientes. El acceso a la plataforma les garantizará oportunidades laborales constantes, lo que se traducirá en un flujo de ingresos más predecible.
#### Recomendación
- Restaurantes: Los restaurantes satisfechos recomendarán la solución a otros negocios del rubro, destacando los beneficios del monitoreo de temperatura automatizado y la capacidad de evitar pérdidas por insumos dañados. Además, resaltarán la facilidad de uso de la plataforma y los ahorros energéticos obtenidos.
- Técnicos de mantenimiento: Los técnicos que encuentren valor en la plataforma recomendarán a otros colegas debido a la facilidad para encontrar trabajo y a la posibilidad de recibir solicitudes en tiempo real. La vinculación directa con los restaurantes también les permitirá establecer relaciones laborales duraderas, lo cual incentivará la recomendación del sistema a otros profesionales.
 
 

### 1.2.2.3. Lean UX Hypothesis Statements.

### 1. Monitoreo y Control de Temperatura

- **Creemos que lograremos**: Un control de temperatura constante en las unidades de refrigeración, reduciendo riesgos a la seguridad alimentaria y mejorando la calidad de los alimentos.
- **Si**: El personal del restaurante (gerentes y personal de cocina).
- **Obtiene**: La capacidad de monitorear y mantener temperaturas óptimas en sus unidades de refrigeración de manera más constante, evitando fluctuaciones de temperatura.
- **Con**: Un sistema que proporciona monitoreo en tiempo real, ajustes automáticos de temperatura y alertas proactivas.

---

### 2. Gestión de Inventarios

- **Creemos que lograremos**: Mejor control de inventarios, reducción de errores y mejora en la rentabilidad.
- **Si**: El personal del restaurante (gerentes, personal de cocina y responsables de inventarios).
- **Obtiene**: Un manejo más preciso y en tiempo real del inventario, reduciendo desperdicios y minimizando errores.
- **Con**: Una interfaz intuitiva para la gestión de inventarios en tiempo real que facilita el seguimiento de existencias y automatiza las actualizaciones.

---

### 3. Mantenimiento de Sensores

- **Creemos que lograremos**: Procesos de mantenimiento más eficientes y mayor confiabilidad en el sistema de refrigeración.
- **Si**: Los técnicos de mantenimiento.
- **Obtiene**: La capacidad de calibrar, diagnosticar y mantener los sensores de temperatura de manera más eficiente, asegurando lecturas precisas.
- **Con**: Una interfaz dedicada para la calibración, diagnóstico y mantenimiento de los sensores.

---

### 4. Usabilidad y Adopción

- **Creemos que lograremos**: Alta adopción por parte de los usuarios y uso efectivo del sistema con una formación mínima.
- **Si**: Todos los tipos de usuarios (empleados, técnicos y administradores).
- **Obtiene**: Interfaz del sistema fácil de usar e intuitiva, que requiere poca o ninguna formación extensiva.
- **Con**: Un diseño centrado en el usuario que tenga en cuenta los diferentes niveles de habilidad y necesidades específicas.

---

### 5. Integración y Compatibilidad

- **Creemos que lograremos**: Una integración fluida con el hardware existente, reduciendo costos de transición y fomentando la adopción.
- **Si**: Los restaurantes que usan diversos modelos de unidades de refrigeración y sensores.
- **Obtiene**: La capacidad de implementar el nuevo sistema sin necesidad de costosas actualizaciones de hardware.
- **Con**: Un sistema compatible con una amplia gama de modelos de unidades de refrigeración y sensores.

---

### 1.2.2.4. Lean UX Canvas.

<img src="/Report/images/ux_canvas.png" width="1250"/>
 
# 1.3. Segmentos objetivo.

1.  Personal de Restaurantes: 

Rango de Edad: 22 a 50 años.

Ocupaciones: Cocineros, ayudantes de cocina, encargados de compras, gerentes de restaurantes.

Ubicación: Principalmente en zonas urbanas y metropolitanas de Lima, Perú.

Nivel Educativo: Desde educación secundaria completa hasta educación técnica en gastronomía o administración
.
Experiencia Laboral: Entre 2 y 15 años en la industria de la gastronomía o gestión de restaurantes.

Tecnología Utilizada: Uso frecuente de herramientas básicas de gestión de inventario y POS (Point of Sale), smartphones con aplicaciones para monitoreo y control de inventarios, y software de gestión de restaurantes.

Descripción
Este grupo incluye a empleados y miembros del equipo administrativo que se beneficiarán enormemente de la implementación del sistema de refrigeración avanzado. Les proporcionará herramientas efectivas para realizar un seguimiento detallado de la calidad de los insumos, garantizando que los alimentos se mantengan a las temperaturas adecuadas. Además, facilitará una gestión más eficiente del inventario, permitiendo una mejor planificación y reducción de desperdicios. Con el sistema, tendrán acceso a datos precisos y alertas oportunas, lo que les permitirá tomar decisiones informadas y mantener altos estándares en la conservación de alimentos.

2.  Personal de Mantenimiento del Software: 

Rango de Edad: 30 a 50 años.

Ocupaciones: Tecnicos y personal de mantenimiento de equipos de refrigeración y aire acondicionado

Ubicación: Principalmente en zonas urbanas y metropolitanas de Lima, Perú.

Nivel Educativo:  educación técnica en electricidad y mecánica.
.
Experiencia Laboral: Entre 5 y 15 años en la industria de la gastronomía o gestión de restaurantes.

Tecnología Utilizada: 
Herramientas Técnicas: Multímetros, pinzas amperimétricas, termómetros infrarrojos, detectores de fugas de refrigerante, manómetros de refrigeración, soldadores, bombas de vacío, y herramientas mecánicas como alicates, destornilladores, llaves ajustables, y cortatubos.
Equipos de Diagnóstico: Escáneres digitales para diagnóstico de sistemas de refrigeración y aire acondicionado, y analizadores de sistemas HVAC (Heating, Ventilation, and Air Conditioning).

Descripción
Este equipo es crucial para el buen funcionamiento del sistema de refrigeración. Su rol implica gestionar y mantener el software que controla el sistema, asegurándose de que todos los componentes operen de manera fluida y eficiente. Son responsables de resolver cualquier problema técnico que pueda surgir, ya sea un fallo en los sensores, problemas de conectividad, o errores en el software. Su tarea es garantizar que el sistema esté siempre actualizado y funcionando sin contratiempos, proporcionando soporte técnico y realizando ajustes cuando sea necesario para mantener la estabilidad y el rendimiento óptimo del sistema. 

