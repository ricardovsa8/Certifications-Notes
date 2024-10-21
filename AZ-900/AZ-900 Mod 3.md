**Aspectos básicos de Microsoft Azure: Descripción de la administración y la gobernanza de Azure**

_________________________________________________________

**Descripción de la administración de costos en Azure**

En este módulo, se presentarán los factores que afectan a los costos en Azure y las herramientas para ayudarle a predecir los costos potenciales y supervisar y controlar los costos.

*Descripción de los factores que pueden afectar a los costos en Azure*

Azure desplaza los costos de desarrollo del gasto de capital (CapEx) de la construcción y mantenimiento de la infraestructura y las instalaciones a un gasto operativo (OpEx) de alquiler de la infraestructura según la necesite, ya sea de proceso, de almacenamiento, redes, etc.

Ese costo de OpEx puede verse afectado por muchos factores. Algunos de los factores que afectan son los siguientes:

- Tipo de recurso:
    Varios factores influyen en el costo de los recursos de Azure. El tipo de recursos, la configuración del recurso y la región de Azure afectarán cuánto cuesta un recurso. Al aprovisionar un recurso de Azure, Azure crea instancias de uso medido para ese recurso. Los medidores realizan el seguimiento del uso de los recursos y generan un registro de uso que se usa para calcular la factura.
- Consumo
    El pago por uso ha sido siempre un tema coherente y es el modelo de pago en la nube en el que paga por los recursos que usa durante un ciclo de facturación. Si durante este ciclo usa más proceso, paga más. Si usa menos en el ciclo actual, paga menos. Es un mecanismo de precios directo que permite una máxima flexibilidad.  
- Mantenimiento
    La flexibilidad de la nube permite ajustar rápidamente los recursos en función de la demanda. El uso de grupos de recursos puede ayudar a mantener todos los recursos organizados. Para controlar los costos, es importante mantener el entorno en la nube. 
- Geografía
    Al aprovisionar la mayoría de los recursos en Azure, debe definir una región donde se implementará el recurso. La infraestructura de Azure se distribuye de forma global, lo que le permite implementar los servicios de manera centralizada, acercarlos a los clientes o una solución intermedia. 
- Tipo de suscripción
    Algunos tipos de suscripciones de Azure también incluyen provisiones de uso que afectan a los costos.
- Azure Marketplace
  permite comprar soluciones y servicios basados en Azure de proveedores de terceros.

*Comparación de las calculadoras de precios y costo total de propiedad*

Las calculadoras de precios y de costo total de propiedad (TCO) le ayudan a comprender los posibles gastos de Azure. Las dos calculadoras son accesibles desde Internet y permiten crear una configuración. Pero las dos calculadoras tienen propósitos muy diferentes.

**Calculadora de precios**

está diseñada para proporcionarle un costo estimado para el aprovisionamiento de recursos en Azure.

Puede obtener una estimación de recursos individuales, crear una solución o usar un escenario de ejemplo para ver una estimación del gasto de Azure. La calculadora de precios se centra en el costo de los recursos aprovisionados en Azure.

Con la calculadora de precios, puede calcular los costos de cualquier recurso aprovisionado, incluidos los de proceso, almacenamiento y red asociados. Incluso puede tener en cuenta diferentes opciones de almacenamiento, como el tipo de almacenamiento, el nivel de acceso y la redundancia.

**Calculadora de TCO**

La calculadora de TCO está diseñada para ayudarle a comparar los costos de ejecución de una infraestructura local en comparación con una infraestructura en la nube de Azure. Con la calculadora de TCO, se especifica la configuración de infraestructura actual, incluidos los servidores, las bases de datos, el almacenamiento y el tráfico de red saliente. Después, la calculadora de TCO compara los costos previstos del entorno actual con un entorno de Azure que admite los mismos requisitos de infraestructura.

Con la calculadora de TCO, escribe la configuración, agrega suposiciones como los costos de mano de obra de TI y de energía, y obtiene una estimación de la diferencia de costos para ejecutar el mismo entorno en el centro de datos actual o en Azure.

*Describir la herramienta Microsoft Cost Management*

Cost Management proporciona la capacidad de comprobar rápidamente los costos de los recursos de Azure, crear alertas basadas en el gasto de recursos y crear presupuestos que se pueden usar para automatizar la administración de recursos

**Alertas sobre los costos**

Las alertas de costos proporcionan una única ubicación para comprobar rápidamente todos los diferentes tipos de alertas que pueden aparecer en el servicio Cost Management. Los tres tipos de alertas que pueden aparecer son las siguientes:

- Alertas de presupuesto: 
  le envían una notificación cuando el gasto, en función del uso o coste, alcanza o supera la cantidad definida en la condición de alerta del presupuesto. Los presupuestos de Cost Management se crean mediante Azure Portal o la API de consumo de Azure.
  En Azure Portal, los presupuestos se definen por el costo
- Alertas de crédito:
    Las alertas de crédito le avisan cuando se consumen los compromisos monetarios de crédito de Azure. Los compromisos monetarios son para organizaciones con contratos Enterprise (EA). Las alertas de crédito se generan de forma automática al 90 % y al 100 % del saldo de crédito de Azure. 
- Alertas de cuota de gasto de departamento:
    Las alertas de cuota de gasto de departamento notifican cuándo el gasto del departamento alcanza un umbral fijo de la cuota. Las cuotas de gasto se configuran en el portal de EA. Cada vez que se alcanza un umbral, se genera un correo electrónico para los propietarios del departamento y se muestra en las alertas sobre los costos. Por ejemplo, el 50 % o el 75 % de la cuota.

 **Presupuestos** 

 Un presupuesto es donde se establece un límite de gasto para Azure. Puede establecer presupuestos basados en una suscripción, un grupo de recursos, un tipo de servicio u otros criterios. Al establecer un presupuesto, también establecerá una alerta de presupuesto. Cuando el presupuesto alcanza el nivel de alerta de presupuesto, desencadenará una alerta de presupuesto que se muestra en el área de alertas de costos. Si se configuran, las alertas de presupuesto también enviarán una notificación por correo electrónico de que se ha desencadenado un umbral de alerta de presupuesto.

 *Descripción de la finalidad de las etiquetas*

- Administración de recursos: las etiquetas permiten localizar recursos asociados a cargas de trabajo, entornos, unidades de negocio y propietarios específicos y actuar al respecto.
- Optimización y administración de costes: las etiquetas permiten agrupar recursos para que podamos informar sobre los costes, asignar centros de costes internos, mantener los presupuestos a raya y predecir costes estimados.
- Administración de operaciones: las etiquetas permiten agrupar recursos según la importancia que tiene su disponibilidad para nuestro negocio. Esta agrupación nos ayuda a formular acuerdos de nivel de servicio (SLA), que constituyen una garantía de rendimiento o de tiempo de actividad entre nosotros y nuestros usuarios.
- Seguridad: las etiquetas permiten clasificar los datos según su nivel de seguridad, por ejemplo, públicos o confidenciales.
Gobernanza y cumplimiento normativo: las etiquetas permiten identificar los recursos que cumplen con los requisitos de gobernanza o cumplimiento normativo, como la norma ISO 27001. Las etiquetas también pueden formar parte de nuestros esfuerzos de aplicación de estándares. Así, podríamos exigir que todos los recursos se etiqueten con un nombre de departamento o propietario.
- Automatización y optimización de las cargas de trabajo: las etiquetas pueden servir para ver todos los recursos que participan en implementaciones complejas. Por ejemplo, podemos etiquetar un recurso con su nombre de aplicación o carga de trabajo asociado y usar un software como Azure DevOps para realizar tareas automatizadas en esos recursos.
_________________________________________________________
**Descripción de las características y herramientas de Azure para la gobernanza y el cumplimiento**

**Descripción del propósito de Microsoft Purview**

Microsoft Purview es una familia de soluciones de gobernanza, riesgo y cumplimiento de datos que le ayudan a obtener una sola visión unificada de los datos. Microsoft Purview reúne información sobre los datos locales, multinube y software como servicio.


Con Microsoft Purview, puede mantenerse al día en su entorno de datos gracias a:

- Detección de datos automatizada
- Clasificación de datos confidenciales
- Linaje de datos de un extremo a otro

Dos áreas de solución principales comprenden Microsoft Purview: el riesgo y el cumplimiento y la gobernanza unificada de datos.

el riesgo y el cumplimiento 
     Características de Microsoft 365 como componente principal de las soluciones de cumplimiento y riesgos de Microsoft Purview. Microsoft Teams, OneDrive y Exchange son solo algunos de los servicios de Microsoft 365 que Microsoft Purview usa para ayudar a administrar y supervisar los datos. Microsoft Purview, mediante la administración y supervisión de los datos, puede ayudar a su organización a:

- Proteger datos confidenciales en nubes, aplicaciones y dispositivos.
- Identificar los riesgos de datos y administrar los requisitos de cumplimiento normativo.
- Comenzar a usar el cumplimiento normativo.


la gobernanza unificada de datos.

Microsoft Purview proporciona una solución unificada de gobernanza de datos que le ayuda a administrar y gobernar los datos locales, de varias nubes y de software como servicio (SaaS). Las sólidas funcionalidades de gobernanza de datos de Microsoft Purview le permiten administrar los datos almacenados en bases de datos de Azure, SQL y Hive, localmente e incluso en otras nubes, como Amazon S3.

La gobernanza unificada de datos de Microsoft Purview ayuda a su organización a:

- Crear un mapa actualizado de todo el patrimonio de datos que incluya la clasificación de datos y el linaje de un extremo a otro.
- Identificar dónde se almacenan los datos confidenciales en su patrimonio.
- Crear un entorno seguro para que los consumidores de datos encuentren datos valiosos.
- Generar información sobre cómo se almacenan y usan los datos.
- Administrar el acceso a los datos de su patrimonio de forma segura y a gran escala.

**Descripción del propósito de Azure Policy**

¿Cómo puede asegurarse de que estos recursos mantengan su cumplimiento? ¿Puede recibir un aviso cuando la configuración de un recurso cambie?

Azure Policy es un servicio de Azure que permite crear, asignar y administrar directivas que controlan o auditan los recursos. Dichas directivas aplican distintas reglas en las configuraciones de los recursos para que esas configuraciones sigan cumpliendo con los estándares corporativos.

Una iniciativa de Azure Policy es una forma de agrupar las directivas relacionadas. La definición de iniciativa contiene todas las definiciones de directiva para facilitar el seguimiento del estado de cumplimiento de cara a un objetivo mayor.

En esta iniciativa se incluyen las siguientes definiciones de directiva:

- Supervisar base de datos SQL sin cifrar en Security Center: esta directiva supervisa servidores y bases de datos SQL sin cifrar.
- Supervisión de los puntos vulnerables del sistema operativo en Security Center: esta directiva supervisa los servidores que no cumplen la línea base de la vulnerabilidad del sistema operativo configurada.
- Supervisar la falta de Endpoint Protection en Security Center: esta directiva supervisa los servidores que no tienen instalado un agente de Endpoint Protection.

La iniciativa Habilitar la supervisión en Azure Security Center contiene más de 100 definiciones de directiva independientes, de hecho.

**Descripción del propósito de bloqueos de recursos**

Los bloqueos de recursos impiden que se eliminen o modifiquen recursos por error.

*Tipos de bloqueos de recursos*

Hay dos tipos de bloqueos de recursos, uno que impide que los usuarios eliminen un recurso y otro que impide que los usuarios lo cambien o eliminen.

- Eliminar significa que los usuarios autorizados pueden leer y modificar un recurso, pero no eliminarlo.
  
- ReadOnly significa que los usuarios autorizados solo pueden leer recursos, pero no actualizarlos ni eliminarlos. Aplicar este bloqueo es similar a restringir todos los usuarios autorizados a los permisos concedidos por el rol Lector.

**Descripción de las ventajas del portal de confianza de servicios**

El Portal de confianza de servicios de Microsoft es un portal que proporciona contenido, herramientas y otros recursos sobre las prácticas de seguridad, privacidad y cumplimiento de Microsoft.

El Portal de confianza de servicios contiene detalles sobre la implementación de controles y procesos de Microsoft que protegen nuestros servicios en la nube y los datos de los clientes que contienen. Para acceder a algunos de los recursos del Portal de confianza de servicios, debe iniciar sesión con un usuario autenticado con su cuenta de Servicios en la nube de Microsoft (cuenta de organización de Microsoft Entra). Deberá revisar y aceptar el acuerdo de no divulgación de Microsoft para acceder a los materiales de cumplimiento.


_________________________________________________________

**Descripción de las características y herramientas para administrar e implementar recursos de Azure**

**Descripción de las herramientas para interactuar con Azure**

Para sacar el máximo partido de Azure, necesita una manera de interactuar con el entorno de Azure, los grupos de administración, las suscripciones, los grupos de recursos, los recursos, etc. Azure proporciona varias herramientas para administrar el entorno, lo que incluye:

- Azure portal
- Azure PowerShell
- Interfaz de la línea de comandos (CLI) de Azure

Azure Cloud Shell

Azure Cloud Shell es una herramienta de Shell basada en explorador que permite crear, configurar y administrar recursos de Azure mediante un Shell. Azure Cloud Shell admite tanto Azure PowerShell como la interfaz de la línea de comandos (CLI) de Azure, que es un Shell de Bash.

¿Qué es la CLI de Azure?

La CLI de Azure es funcionalmente equivalente a Azure PowerShell, y la diferencia principal es la sintaxis de los comandos. Azure PowerShell usa comandos de PowerShell y la CLI de Azure usa comandos de Bash.

La CLI de Azure proporciona las mismas ventajas de controlar tareas discretas u organizar operaciones complejas a través del código. También se puede instalar en plataformas Windows, Linux y Mac, así como a través de Azure Cloud Shell.

Debido a las similitudes en las funcionalidades y el acceso entre Azure PowerShell y la CLI de Azure basada en Bash, la elección entre uno y otra depende básicamente del lenguaje con el que esté más familiarizado.

**Descripción del propósito de Azure Arc**

La administración de entornos híbridos y de varias nubes puede complicarse rápidamente. Azure proporciona una serie de herramientas para aprovisionar, configurar y supervisar recursos de Azure. ¿Qué ocurre con los recursos locales en una configuración híbrida o los recursos de nube en una configuración de varias nubes?

Al usar Azure Resource Manager (ARM), Arc le permite ampliar el cumplimiento y la supervisión de Azure a las configuraciones híbridas y de varias nubes. Azure Arc simplifica el gobierno y la administración al ofrecer una plataforma de administración local y multinube coherente.

Actualmente, Azure Arc le permite administrar los siguientes tipos de recursos hospedados fuera de Azure:

- Servidores
- Clústeres de Kubernetes
- Servicios de datos de Azure
- SQL Server
- Máquinas virtuales (versión preliminar)

**Descripción de las plantillas de Azure Resource Manager y Azure ARM**

Azure Resource Manager (ARM) es el servicio de implementación y administración de Azure. Proporciona una capa de administración que le permite crear, actualizar y eliminar recursos de la cuenta de Azure. Cada vez que haga algo con los recursos de Azure, ARM está implicado.

Ventajas de Azure Resource Manager
Con Azure Resource Manager, puede realizar lo siguiente:

Administrar la infraestructura mediante plantillas declarativas en lugar de scripts. Una plantilla de Resource Manager es un archivo JSON que define lo que quiere implementar en Azure.
Implementar, administrar y supervisar todos los recursos de la solución en grupo, en lugar de controlarlos individualmente.
Vuelva a implementar la solución a lo largo del ciclo de vida de desarrollo y tenga la seguridad de que los recursos se implementan en un estado coherente.
Defina las dependencias entre recursos de modo que se implementen en el orden correcto.
Aplique control de acceso a todos los servicios, puesto que RBAC se integra de forma nativa en la plataforma de administración.
Aplicar etiquetas a los recursos para organizar de manera lógica todos los recursos de la suscripción.
Comprenda la facturación de la organización viendo los costos de un grupo de recursos que comparten la misma etiqueta.

Infraestructura como código

 Las plantillas de ARM y Bicep son dos ejemplos de uso de la infraestructura como código con Azure Resource Manager para mantener el entorno.

Plantillas de ARM

 Al usar plantillas de ARM, puede describir los recursos que quiere usar en un formato JSON declarativo. Con una plantilla de ARM, el código de implementación se comprueba antes de que se ejecute cualquier código. Esto garantiza que los recursos se crearán y se conectarán correctamente. 

Bicep

Bicep es un lenguaje que usa sintaxis declarativa para implementar recursos de Azure. Un archivo de Bicep define la infraestructura y la configuración. A continuación, ARM implementa ese entorno en función del archivo Bicep. Aunque es similar a una plantilla de ARM, que está escrita en JSON, los archivos de Bicep tienden a usar un estilo más sencillo y conciso.

_________________________________________________________

**Descripción de las herramientas de supervisión de Azure**

**Descripción del propósito de Azure Advisor**

Azure Advisor evalúa los recursos de Azure y hace recomendaciones que contribuyen a mejorar la confiabilidad, la seguridad y el rendimiento, lograr la excelencia operativa y reducir los costos. Azure Advisor está diseñado para ayudarle a ahorrar tiempo en la optimización en la nube. El servicio de recomendaciones sugiere medidas que puede adoptar de inmediato, posponer o descartar.

Cuando está en Azure Portal, el panel de Advisor muestra recomendaciones personalizadas para todas las suscripciones. Puede usar filtros a fin de seleccionar recomendaciones para suscripciones, grupos de recursos o servicios específicos. Las recomendaciones se dividen en cinco categorías:

- La fiabilidad se usa para garantizar y mejorar la continuidad de las aplicaciones críticas para la empresa.
- La seguridad se usa para detectar amenazas y vulnerabilidades que podrían conducir a vulneraciones de la seguridad.
- El rendimiento se usa para mejorar la velocidad de las aplicaciones.
- La excelencia operativa se usa para aumentar la eficiencia de procesos y flujos de trabajo, mejorar la administración de recursos y -obtener procedimientos recomendados para la implementación.
- El costo se usa para optimizar y reducir el gasto general de Azure.

**Descripción de Azure Service Health**

Microsoft Azure proporciona una solución global en la nube para ayudarle a administrar sus necesidades de infraestructura, llegar a sus clientes, innovar y adaptarse rápidamente. Conocer el estado de la infraestructura global de Azure y los recursos individuales podría parecer una tarea abrumadora. Azure Service Health le permite realizar un seguimiento de los recursos de Azure, tanto los recursos implementados específicamente como el estado general de Azure. 

Azure Service Health lo hace combinando tres servicios de Azure diferentes:
- Estado de Azure
- Service Health
- Resource Health

**Descripción de Azure Monitor**

Azure Monitor es una plataforma para recopilar datos sobre los recursos, analizar esos datos, visualizar la información e incluso actuar en función de los resultados. Azure Monitor puede supervisar los recursos de Azure, los recursos locales e incluso los recursos de varias nubes, como las máquinas virtuales hospedadas con otro proveedor de nube.

Application Insights

Application Insights, una característica de Azure Monitor, supervisa las aplicaciones web. Application Insights es capaz de supervisar aplicaciones que se ejecutan en Azure, en el entorno local o en otro entorno de nube.

Hay dos maneras de configurar Application Insights para ayudar a supervisar la aplicación. Puede instalar un SDK en la aplicación, o bien puede usar el agente de Application Insights.
