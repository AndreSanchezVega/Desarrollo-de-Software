# A . Cuestionario
## 1) Motivaciones para la nube
- ¿Qué problemas o limitaciones existían antes del surgimiento de la computación en la nube y cómo los solucionó la centralización de servidores en data centers?
  
Antes del surgimiento de la computación en la nube, las empresas necesitaban invertir grandes cantidades en hardware, software, infraestructura física, mantenimiento,
actualizaciones constantes y personal especializado. Esto generaba altos costos y sistemas vulnerables a fallos locales.
Con la centralización de servidores en data centers y el uso de la nube, las empresas pueden escalar sus recursos según la demanda, reduciendo costos operativos y aumentando la disponibilidad.
Además, si un entorno local falla, el proceso no se detiene, ya que los servicios continúan ejecutándose.

- ¿Por qué se habla de “The Power Wall” y cómo influyó la aparición de procesadores multi-core en la evolución hacia la nube?
  
Se refiere al límite físico que enfrentaron los procesadores cuando, al aumentar la velocidad del reloj (GHz), también aumentaba el consumo de energía y la generación de calor de forma peligrosa , por este motivo
surgió la arquitectura multi-core, donde en lugar de tener un solo núcleo muy rápido, se integraron varios núcleos en un mismo chip. Así, se podían realizar más tareas al mismo tiempo . Gracias a los procesadores
multi-core, los servidores en la nube pueden manejar muchas tareas de múltiples usuarios al mismo tiempo, facilitando la virtualización, el escalado de recursos y el rendimiento necesario para servicios en línea
modernos.

## 2) Clusters y load balancing
- Explica cómo la necesidad de atender grandes volúmenes de tráfico en sitios web condujo a la adopción de clústeres y balanceadores de carga.

Cuando los sitios web empezaron a recibir mucho tráfico, un solo servidor no era suficiente para atender a todos los usuarios. Para solucionarlo, 
se comenzaron a usar clústeres de servidores, que trabajan juntos para repartir el trabajo. Además, se usan balanceadores de carga para distribuir 
las solicitudes entre los servidores del clúster, evitando sobrecargas y asegurando que el sitio funcione rápido y sin interrupciones.

- Describe un ejemplo práctico de cómo un desarrollador de software puede beneficiarse del uso de load balancers para una aplicación web.

Un desarrollador de software está construyendo una aplicación web que se espera tenga un alto volumen de usuarios, como una tienda en línea.
Sin un balanceador de carga, si demasiados usuarios acceden al mismo tiempo, el servidor podría volverse lento o incluso caerse. Usando un 
load balancer, el desarrollador puede distribuir las solicitudes de los usuarios entre varios servidores, asegurando que cada uno maneje solo
una parte del tráfico, lo que mejora el rendimiento, la disponibilidad y la escalabilidad de la aplicación.

## 3) Elastic computing
- Define con tus propias palabras el concepto de Elastic Computing.

Elastic Computing( Computacion elastica) existe gracias al cloud computing y los provedores de este. Consiste en que el provedor de tu servicio en la nube atraves de su monitereo se encargara de brindarte los recursos que necesites, como lo es el poder de computo, el almacenamiento, memoria RAM, etc., dependiendo de la demanda que tengas en ese instante.  Esto permite ahorrar costos ya que solo pagas por los recursos que consumes.

- ¿Por qué la virtualización es una pieza clave para la elasticidad en la nube?

La virtualizacion permite crear entornos virtuales que operan de forma independiente del hardware, por lo tanto es posible copiar, mover, clonar o eliminar sin alterar la infraestructura fisica. Esto es clave para la elasticidad porque permite crear o eliminar instancias dependiendo de la demanda
  
- Menciona un escenario donde, desde la perspectiva de desarrollo, sería muy difícil escalar la infraestructura sin un entorno elástico.

Cuando un videojuego grande va a ser lanzado, se genera mucha expectación y millones de usuarios intentan loggearse al instante en que el videojuego sale. Esta alta demanda (que suele durar unos días) puede traer problemas serios en los sistemas de login, matchmaking, descarga del cliente del juego, y gestión del tráfico de red.
Desde la perspectiva de desarrollo, escalar manualmente toda la infraestructura para soportar esta carga temporal sería muy complejo y costoso. Sin un entorno elástico, sería necesario aprovisionar muchos más servidores de forma anticipada, lo que implicaría altos costos cuando la demanda baje.
Un entorno de elastico permite escalar automáticamente los recursos según la carga real del sistema: aumentando la capacidad durante el lanzamiento y reduciéndola cuando la demanda baja
Modelos de servicio (IaaS, PaaS, SaaS, DaaS)

## 4) Modelos de servicio (IaaS, PaaS, SaaS, DaaS)
- Diferencia cada uno de estos modelos. ¿En qué casos un desarrollador optaría por PaaS en lugar de IaaS?

   - IaaS (Infrastructure as a Service): Provisión de infraestructura, como lo son los servidores virtuales, redes, almacenamientopara que el usuario la administre.
   - PaaS (Platform as a Service): Plataforma gestionada para desarrollar, desplegar y escalar aplicaciones sin preocuparse por la infraestructura.
   - SaaS (Software as a Service): Software listo para usarse a través de internet, sin necesidad de instalación ni mantenimiento.
   - DaaS (Desktop as a Service): Escritorios virtuales accesibles desde cualquier lugar, gestionados por el proveedo

Un desarrollador optaría por PaaS en lugar de IaaS cuando necesita enfocarse únicamente en escribir y desplegar su código y no quiere encargarse de configurar servidores, redes o sistemas operativos
  
- Enumera tres ejemplos concretos de proveedores o herramientas que correspondan a cada tipo de servicio.

1) *IaaS (Infrastructure as a Service)* : Ofrece infraestructura tecnológica como servidores, almacenamiento y redes, todo gestionado por el proveedor.
     - Ejemplos:
         - Amazon Web Services (AWS): Ofrece EC2 (Elastic Compute Cloud) para la computación y S3 para almacenamiento.
         - Microsoft Azure: Proporciona máquinas virtuales y almacenamiento en la nube.
         - Google Cloud Platform (GCP): Ofrece máquinas virtuales (Compute Engine) y almacenamiento (Cloud Storage).
2) *PaaS (Platform as a Service)*: Ofrece plataformas de desarrollo que permiten a los usuarios crear, probar y ejecutar aplicaciones sin tener que gestionar la infraestructura subyacente.
     - Ejemplos:
         - Heroku: Proporciona una plataforma para desarrollar, ejecutar y gestionar aplicaciones.
         - Google App Engine: Plataforma para crear aplicaciones web y móviles.
         - Microsoft Azure App Service: Permite crear y gestionar aplicaciones web y móviles.
3) *SaaS (Software as a Service)*: Ofrece software accesible a través de Internet, sin necesidad de instalar o gestionar el software en el dispositivo del usuario.
     - Ejemplos:
        - Google Workspace (G Suite): Conjunto de aplicaciones como Gmail, Google Drive y Google Docs.
        - Microsoft 365: Conjunto de aplicaciones como Word, Excel y Teams, accesibles en la nube.
        - Salesforce: Plataforma de gestión de relaciones con clientes (CRM) en la nube.
4) *DaaS (Data as a Service)*: Proporciona acceso a datos como servicio, a menudo incluyendo almacenamiento, procesamiento y análisis de grandes volúmenes de datos.
     - Ejemplos:
        - Amazon Redshift: Servicio de almacenamiento y análisis de datos en la nube.
        - Google BigQuery: Herramienta para análisis de grandes conjuntos de datos.
        - Microsoft Azure Synapse Analytics: Plataforma de análisis y procesamiento de datos.
    
## 5) Tipos de nubes (Pública, Privada, Híbrida, Multi-Cloud)
- ¿Cuáles son las ventajas de implementar una nube privada para una organización grande?

Una nube privada es una infraestructura dedicada exclusivamente a una sola organización, lo que permite tener control total sobre el entorno tecnológico. Esto es ideal para organizaciones grandes que manejan datos sensibles o confidenciales, ya que pueden establecer protocolos de seguridad personalizados, cumplir con normativas específicas (como GDPR, HIPAA, etc.), y reducir los riesgos asociados a la exposición de datos.

Además, las organizaciones grandes suelen tener requisitos de rendimiento muy altos y cargas de trabajo críticas que pueden ser mejor gestionadas en un entorno privado, evitando la congestión o variabilidad de recursos propia de una nube pública. También tienen la posibilidad de adaptar y optimizar la infraestructura según sus procesos internos, integrando sus sistemas heredados (on-premise) con mayor facilidad.

Aunque su costo inicial es más elevado, a largo plazo puede resultar más eficiente para empresas con uso constante e intensivo de recursos.

-  ¿Por qué una empresa podría verse afectada por el “provider lock-in”?
  
El “provider lock-in” (bloqueo del proveedor) se refiere a la dependencia excesiva que una empresa puede desarrollar hacia un proveedor de servicios en la nube. Esto sucede cuando las soluciones utilizadas (infraestructura, plataformas o servicios) están fuertemente integradas con tecnologías propietarias del proveedor, dificultando la migración hacia otra nube.

Una empresa afectada por el lock-in puede enfrentar costos elevados, limitaciones técnicas y barreras operativas si decide cambiar de proveedor, lo que limita su capacidad de adaptación. También se ve restringida a las condiciones, precios y políticas del proveedor actual, sin mucha posibilidad de negociación o flexibilidad. Este riesgo es especialmente preocupante en entornos donde la innovación o la expansión requieren agilidad tecnológica.
  
- ¿Qué rol juegan los “hyperscalers” en el ecosistema de la nube?

Los hyperscalers son empresas que ofrecen servicios de nube a gran escala, como Amazon Web Services (AWS), Microsoft Azure y Google Cloud Platform (GCP). Su infraestructura está diseñada para escalar rápidamente y soportar millones de usuarios y aplicaciones simultáneamente. Tienen presencia global con centros de datos distribuidos, lo que permite una alta disponibilidad, baja latencia y confiabilidad.

Su rol en el ecosistema es fundamental porque actúan como impulsores de la transformación digital, permitiendo que empresas de todos los tamaños accedan a tecnologías avanzadas como inteligencia artificial, machine learning, big data, IoT, y más, sin necesidad de construir infraestructuras propias.

También fomentan la estandarización, innovación y competencia en el mercado, ya que constantemente desarrollan nuevos servicios y modelos de negocio. Al mismo tiempo, ofrecen entornos robustos que facilitan tanto el desarrollo como la operación de soluciones empresariales en la nube.

# B) Actividades de investigación y aplicación

## 1) Estudios de casos 
1) Schwarz Group (Lidl y Kaufland):
- Motivaciones para la migración: Schwarz Group decidió migrar a la nube para obtener escalabilidad y flexibilidad en sus operaciones. Necesitaban adaptarse a picos de actividad en días específicos, como Navidad o el Black Friday, y buscaban una solución que les permitiera manejar estas fluctuaciones de manera eficiente. El País.
- Beneficios obtenidos:
     - Escalabilidad: La nube les permitió ajustar rápidamente sus recursos según la demanda, garantizando un rendimiento óptimo durante períodos de alta actividad.
     - Flexibilidad: Pudieron adaptarse a las necesidades cambiantes del negocio sin las limitaciones de una infraestructura local.Skyone+1El País+1
     - Soberanía y seguridad de datos: Al desarrollar su propia nube con centros de datos en Alemania, aseguraron el control y la protección de la información, cumpliendo con las regulaciones europeas. El País
-	Desafíos enfrentados:
     -	Desarrollo interno de la infraestructura: Construir y gestionar su propia nube requirió una inversión significativa en infraestructura, software y personal especializado.
     -	Competencia en el mercado de servicios en la nube: Entrar en un mercado dominado por grandes proveedores estadounidenses supuso desafíos en términos de competitividad y diferenciación. El País
2) SAP:
- Motivaciones para la migración: SAP migró sus soluciones de software a la nube para mejorar la eficiencia operativa y adaptarse a las demandas del mercado actual, centrando su estrategia en servicios de cloud computing e inteligencia artificial. El País
- Beneficios obtenidos:
    - Mejora en márgenes y retención de clientes: La transición a la nube permitió a SAP ofrecer soluciones más innovadoras, mejorando sus márgenes y manteniendo la lealtad de sus clientes.El País
    - Generación de ingresos recurrentes: Los servicios en la nube proporcionaron una fuente estable de ingresos, representando el 51% de sus ingresos totales. El País
- Desafíos enfrentados:
    - Adaptación cultural y organizativa: La transición a la nube implicó cambios significativos en la cultura empresarial y en la forma de operar, requiriendo capacitación y adaptación por parte del personal.
    - Competencia en el mercado de la nube: Afrontaron la necesidad de diferenciarse en un mercado altamente competitivo, dominado por grandes proveedores. 
3) Empresas en Colombia:
- Motivaciones para la migración: Según un estudio, el 93% de las empresas colombianas migraron a la nube como parte de su estrategia de transformación empresarial, buscando beneficios como eficiencia, disponibilidad y flexibilidad. Datacenter Dynamics
-	Beneficios obtenidos:
    - Reducción de costos: La migración permitió disminuir gastos asociados a infraestructura y mantenimiento de centros de datos locales.Check Point Software+1El País+1
    - Escalabilidad y flexibilidad: Las empresas pudieron ajustar sus recursos tecnológicos según las necesidades del negocio, mejorando la adaptabilidad.
- Desafíos enfrentados:
    - Integración de sistemas: La adaptación de sistemas locales a entornos en la nube requirió esfuerzos significativos de integración y adaptación.Incentro
    - Gestión del cambio: La transición implicó desafíos culturales y operativos, requiriendo capacitación y ajustes en los procesos internos.
      
## 2) Comparativa de modelos de servicio.
- Realiza un cuadro comparativo en el que muestres las responsabilidades del desarrollador, del proveedor y del equipo de operaciones en los distintos modelos (IaaS, PaaS, SaaS).
- Incluye aspectos como: instalación de SO, implementación de aplicaciones, escalado automático, parches de seguridad, etc.

| Aspecto                             | IaaS (Infraestructura como Servicio)                                                                                                                                     | PaaS (Plataforma como Servicio)                                                                                                                       | SaaS (Software como Servicio)                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| *Instalación de Sistema Operativo (SO)* | Responsabilidad del proveedor: El proveedor proporciona el sistema operativo, pero el cliente tiene control sobre la instalación y configuración.                      | Responsabilidad del proveedor: El proveedor gestiona el sistema operativo y las actualizaciones.                                                      | Responsabilidad del proveedor: El proveedor gestiona todo, incluido el sistema operativo.                                           |
| *Implementación de aplicaciones*       | Responsabilidad del cliente (desarrollador): El desarrollador es responsable de instalar y configurar sus propias aplicaciones.                                        | Responsabilidad del cliente (desarrollador): El desarrollador implementa y gestiona las aplicaciones en la plataforma proporcionada por el proveedor. | Responsabilidad del proveedor: El proveedor gestiona e implementa las aplicaciones disponibles para el usuario final.               |
| *Escalado automático*                  | Responsabilidad del cliente (desarrollador): El desarrollador puede configurar el escalado automático según las necesidades de la aplicación.                          | Responsabilidad del proveedor: El proveedor gestiona el escalado automático de la plataforma, pero el cliente puede configurarlo según los recursos utilizados. | Responsabilidad del proveedor: El proveedor gestiona el escalado automático del servicio sin intervención del cliente.             |
| *Parches de seguridad*                | Responsabilidad del proveedor: El proveedor gestiona la infraestructura de seguridad, pero el cliente es responsable de la seguridad de sus aplicaciones.              | Responsabilidad del proveedor: El proveedor gestiona la seguridad de la plataforma, incluidas las actualizaciones de seguridad.                        | Responsabilidad del proveedor: El proveedor gestiona todo, incluyendo los parches de seguridad y las actualizaciones.              |
| *Mantenimiento de hardware*           | Responsabilidad del proveedor: El proveedor es responsable del mantenimiento y funcionamiento del hardware en la infraestructura.                                     | Responsabilidad del proveedor: El proveedor gestiona el mantenimiento de la infraestructura y las plataformas.                                        | Responsabilidad del proveedor: El proveedor gestiona todo el mantenimiento y actualización de la infraestructura.                 |
| *Administración de red*              | Responsabilidad del proveedor: El proveedor maneja la infraestructura de red, pero el cliente puede tener que configurar las redes virtuales.                          | Responsabilidad del proveedor: El proveedor gestiona la red para la plataforma, pero el cliente puede configurar aspectos específicos.                | Responsabilidad del proveedor: El proveedor gestiona toda la infraestructura de red.                                               |
| *Backup de datos*                    | Responsabilidad del cliente (equipo de operaciones): El cliente debe gestionar las copias de seguridad de sus aplicaciones y datos.                                   | Responsabilidad del proveedor: El proveedor generalmente proporciona opciones de backup, aunque el cliente puede configurarlo.                         | Responsabilidad del proveedor: El proveedor es responsable de realizar las copias de seguridad y garantizar la recuperación de datos. |
| *Gestión de la infraestructura*      | Responsabilidad del proveedor: El proveedor es responsable de la infraestructura física y la virtualización, pero el cliente gestiona sus instancias.                | Responsabilidad del proveedor: El proveedor gestiona la infraestructura y la plataforma, pero el cliente gestiona las aplicaciones.                    | *Responsabilidad del proveedor*: El proveedor gestiona la infraestructura, la plataforma y las aplicaciones.                      |

## 3) Armar una estrategia multi-cloud o híbrida
- Diseña una estrategia (de forma teórica) para migrar el 50% de tus cargas de trabajo a un segundo proveedor de nube, con el fin de no depender exclusivamente de uno.
Para seleccionar al nuevo proveedor, debemos evaluar distintos factores, como el costo, la ubicación de sus servidores, el soporte técnico, los servicios que ofrecen en su plataforma, entre otros. Es necesario analizar las cargas de trabajo en función de su criticidad, los requisitos de rendimiento, la sensibilidad de los datos y cuáles pueden aprovechar mejor las funciones que el nuevo servicio de nube ofrece.
- Explica dónde iría la base de datos, cómo manejarías la configuración de red y cuál sería el plan de contingencia si un proveedor falla
Lo más sensato es que la base de datos se mantenga en el lugar donde estaba originalmente almacenada, ya sea en el servicio de nube original o en el data center propio, y luego hacer conexiones seguras desde el segundo servicio de nube. Si tuviéramos dos bases de datos, una en cada servicio de nube, esto resultaría más costoso y habría que establecer mecanismos de sincronización entre ambos proveedores. Para la conexión de red, se pueden utilizar VPNs para conectar el data center propio y los dos servicios de nube. Si el proveedor del servicio fuera una empresa grande, como AWS, se podría usar sus servicios de conexión directa que ofrecen. Para las cargas de trabajo críticas, mantenemos una réplica pasiva en el otro proveedor de nube. En caso de fallo del proveedor primario, se activa la réplica en el proveedor secundario. También podemos distribuir las cargas de trabajo críticas entre ambos proveedores de nube de forma activa. De este modo, si un proveedor falla, el otro proveedor puede absorber el tráfico adicional.
## 4) Debate sobre costos

# Comparación de Tipos de Nube

| Tipo de Nube    | Costos Iniciales (CAPEX vs. OPEX)                      | Flexibilidad y Escalabilidad                     | Cumplimiento con Normativas             | Barreras/Complejidades al Cambiar de Proveedor     |
|-----------------|--------------------------------------------------------|--------------------------------------------------|------------------------------------------|-----------------------------------------------------|
| Nube Pública |  OPEX: Pago por uso, sin inversión inicial            |  Alta escalabilidad a demanda                   |  Depende del proveedor y región          |  Alto dependencia (vendor lock-in) si se usan servicios nativos  |
| Nube Privada |  CAPEX: Alta inversión en infraestructura             |  Limitada; escalar requiere más inversión       |  Control total sobre los datos          |  Menor lock-in si se usan tecnologías abiertas     |
| Nube Híbrida |  Mixto: inversión + operación                         |  Flexibilidad combinada con escalabilidad       |  Posibilidad de segmentar según normativa |  Complejidad técnica en interoperabilidad          |
| Multi-Cloud  |  OPEX: sin gran inversión inicial, pero más gestión   |  Muy alta; acceso a múltiples proveedores        |  Difícil de gestionar entre proveedores  |  Menor lock-in, pero mayor complejidad operativa   |

# C) Ejercicio de mini-proyecto