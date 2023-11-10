**Capitulo 3 - Conceptos de control de acceso**
____________
*Modulo 1 - Comprender los conceptos de control de acceso*

¿Que es control de seguridad?

Es un salvaguarda o contramedida diseñada para preservar la CIA.

Descripción general de los controles

- No solo consiste en restringir el acceso a los sistemas de información y datos si no tambien en permitir el acceso.

Elementos

*Sujetos*
- Cualquier entidad que solicita acceso a nuestros activos. (Usuario, cliente, proceso o programa)
- Se denomina "Activo"
- Debe tener un nivel de autización (permisos)

*Objetos*
- Cualquier cosa a la que el sujeto intenta acceder.(Dispositivo, proceso, persona, usuario, programa, servidor, cliente, otra entidad que responde a una solicitud de servicio)
- Se denomina "PASIVO", no realiza ninguna acción hasta que el sujeto lo solicita.
- Es todo aquello que presta servicio.

*Normas*
- Compare multiples atributos para determinar el acceso apropiado.
- Permitir el acceso a un objeto.
- Definir cuanto acceso esta permitido.
- Denegar el acceso a un objeto.
- Aplicar acceso basado en el tiempo.

*Control*

Sirve para reducir el riesgo.
- Control fisico. Ejm: Cinturon de seguridad
- Control Administrativo. Ejm: Ley que exije usar el cinturon.

Evaluación de controles

La reducción de riesgo depende de la eficacia del control. Debe aplicarse a la situación actual y adaptarse a un entorno cambiante.

*Defensa en profundidad*
- Una estrategia es la defensa en capas, tambien conocidad como defensa en profundidad.
- Integra: Personas, tecnogias y capacidades operativas.
- Debe implementarse para disuadir un ataque cibernetico.
Ejm. Protección multifactor.

*Principio de privilegio minimo*

Acceso minimo necesario para que los usuarios o programas cumplan su función.

*Gestión de acceso privilegiado*
Cuentas privilegiadas
- Lo manejan los gerentes y administradores.
- Tienen privilegios elevados.
- Lo usan los administradores de sistemas, mesa de ayuda o soporte de TI, analistas de seguridad.

*Medidas tipicas utilizadas para monejar el potencial de riesgos elevado por el uso indevido de cuentas privilegiadas*
- Registro más extenso y detallado de las cuentas de usuario (Que se puedan auiditar)
- Control de accesi más estricto que las cuentas de usuario regulares (hacer uso de MFA)
- Verificación de confianza más profunda que los cuentas normales (antecedentes)
- Mas auditorias que las cuentas regulares.

*Segregación de deberes*

Tambien conocido como SEPARACIÓN de funciones

*Integridad de dos personas*: Ayuda a reducir las amenazas internas.

Personal autorizado versus personal no autorizados.

Como se aprovicionan los usuarios, situaciones:
- Un nuevo empleado
- Cambio de puesto
- Separación de empleo
______________-
*Modulo 2 - Comprender los controles de acceso fisico*

Son elementos que se pueden tocar fisicamente. Ejm: guardias de seguridad, cercas, detectores de movimiento, luces, etc.

Se usan para proteger su activo más importante "Las personas"

¿Porque tener?
- Evitar personar no autorizadas a un sitio fisico.
- No solo proteger a las personas si no tambien las computadoras.

*Tipos de controles de acceso fisico*
- Sistema de credencial y puerta de entrada.
    - Utilizan tarjetas: Codigo de barras, banda magnetica, proximidad, hibrido.
- Diseño ambiental.
- Biometria
    - Procesos que implica: inscripción, verificación.
    - Dos formas principales:
        - Fisiologica: Huella dactilar, escaneo de iris, escaneo de la palma de la mano.
        - Conductual o comportamiento: huella de voz, dinamica de pulsaciones de la tecla.
    - Alto costo de implementarla.

- Vigilancia
    - Camaras
    - Registros
         - BITACORA: Registro de eventos que han ocurrido.

- Guardia de seguridad
- Sistemas de alarma
______________
*Modulo 3 - Comprender los controles de acceso lógico*
Incluyen:
- Contrseñas
- Biometria: implementada a un sistema, como un telefono inteligente.
- Lectores de tarjetas/fichas conectadas a un sistema.

Existen tipos de herramientas electronicas limitan quien puede tener acceso logico a un activo, incluso si la persona ya tiene acceso fisico.

DAC (Control de acceso discrecional)
- Discreción de propietarios del objeto
- Saber a quien dar acceso del activo.

MAC (Control de acceso obligatorio)
- Controlar acceso.
- Administradores de seguridad asignen derechos o permisos de acceso.

RBAC (Control de acceso basado en roles)
- Se configura permisos basados en roles.
- Funciona bien en un entorno de alta rotación del personal.
