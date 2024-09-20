
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



| Juan Jose Navarro Chacon |  |
|----------|----------|
|Soy estudiante de la carrera Ingeniería de Software, actualmente estoy cursando el 8vo ciclo. Me considero una persona divertida, empática, responsable, creativa, honesta y sobre todo organizada en los planes que deseo realizar. Para el trabajo que vamos a realizar puedo aportar con el desarrollo del sistema, ya que tengo conocimientos ciertos lenguajes, además de ser responsable| <img src="/Chapter1/images/student_juanjose.png" width="1250"/>|
|||

| Leonardo Walt Patrocinio Escalante |  |
|----------|----------|
|Me considero una persona creativa, responsable y ordenada. Tengo experiencia trabajando en equipo, escucho las ideas de mis compañeros y me desempeño bien para el avance de los trabajos.| <img src="/Chapter1/images/student_leo.png" width="1250"/>|
|||

| Piero Stefano Márquez |  |
|----------|----------|
|Soy estudiante de 8to ciclo en la carrera Ingeniería de Software. Me considero alguien bastante práctico, directo y honesto. Puedo manejar diversos lenguajes y frameworks ya que un objetivo a corto plazo sería convertirme en un Full Stacks. Siento que aprendo rápido y no tengo problemas con trabajar con diferentes lenguajes o entornos.| <img src="/Chapter1/images/student_piero.png" width="1250"/>|
|||

| Diego Antonio Sánchez Ramírez |  |
|----------|----------|
|Soy un estudiante de la carrera de Ing. De Software en la Universidad de Ciencias Aplicadas (UPC). Estoy familiarizado con los lenguajes de programación C + + y HTML5, CSS y JS. Estoy en vías de aprender otros lenguajes para ser un ingeniero flexible a cualquier necesidad o problema que se presente.| <img src="/Chapter1/images/student_diego.png" width="1250"/>|
|||

| Víctor Yordi Díaz Gonzales |  |
|----------|----------|
|Actualmente ando estudiando la carrera de Ingeniería de Software. Mi pasión por la programación empezó a temprana edad, donde actualmente me permite investigar, analizar y solucionar problemas de la vida cotidiana. Mi objetivo es desarrollar software de calidad que den soluciones innovadoras a la población. Cabe enfatizar que busco la colaboración activa en equipo para llegar a tener éxito en las metas o proyectos. | <img src="/Chapter1/images/student_victor.png" width="1250"/>|
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

En el sector de restaurantes, el personal enfrenta desafíos importantes relacionados con el control de calidad de los insumos y la gestión eficiente de inventarios. Además, los técnicos de mantenimiento necesitan un sistema que les facilite el acceso a solicitudes de trabajo de manera ágil y sencilla.

Los productos y servicios existentes no logran resolver adecuadamente estas necesidades, dejando una oportunidad para optimizar tanto la gestión interna de los restaurantes como la interacción entre el personal y los técnicos.

Nuestro producto, FrostChef, está diseñado para abordar estas carencias al ofrecer una plataforma que mejora el control de calidad de insumos, optimiza la gestión de inventarios, y proporciona a los técnicos de mantenimiento un portal eficiente para gestionar solicitudes de trabajo.

Nos enfocaremos inicialmente en el personal de restaurantes y los técnicos de mantenimiento, quienes enfrentan estos problemas diariamente.

Sabremos que hemos tenido éxito cuando el personal de los restaurantes reporte una mayor eficiencia en la gestión de inventarios, que esto se vea reflejado en ahorro de costes, y los técnicos reduzcan el tiempo de respuesta en un 50% a las solicitudes de mantenimiento.

### 1.2.2.2. Lean UX Assumptions.

**User Assumptions**

**User Outcomes**
 
**Business Assumptions**

**Business Outcomes** 

### 1.2.2.3. Lean UX Hypothesis Statements.

 
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

