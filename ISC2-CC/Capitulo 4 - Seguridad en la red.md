**Capitulo 4 - Seguridad de red**

*Comprender las redes informaticos*

Tipos de redes
- LAN (Red de área local)
- WAN (Red de área amplia)

*Dispositivos de red*

Centro: Se utilizan para conectar varios dispositivos en una red.

- *Conmutador*
    - Conocido como concentrador inteligente.
    - Son dispositivos cableados que conocen las direcciones de los dispositivos conectados a ellos y enrutan el trafico a ese puerto en vex de retrasmitirlo.
    - Tambien pueden crear dominios de difusión independeientes.
- *Enrutador*
    - Se usa para controlar el trafico en las redes.
    - Más inteligente que los concentradores y conmutadores.
    - Determinan la ruta más efeciente para el trafico.
- *Corta fuego*
    - Firewalls, son herramientas esenciales para administrar y controlar el trafico de red y proteger la red.
- *Servidor*
    - Es una computadora que proporciona información a otras computadoras de la red.
- *Punto final*
    - Son extremos de un enlace de comunicación de red.
    - Ejm: Un cliente, otro servidor, estación de trabjo, telefono.

Otro terminos
- Ethernet ( IEEE 802.3)
    - Es un estandar que define las conexiones por cable de los dispositivos de red.
- Dirección del dispositivo
    - MAC (Dirección de control de acceso a medios)
        - Se asigna en el fimware de la interfaz
    - IP (Dirección de protocolo de internet)
        -Dirección logica unica.

Modelo de redes

Un modelo de red tiene al menos dos capas
- Capa superior - APLICACIÓN
- Capa inferior - DATA, TRANSPORTE

OSI -> Modelo de interconexión de sistemas abiertos.

| Capa | Nombre |Datos| 
|--|--|--|
|7|Aplicación|Sitio web|
|6|Presentación| Header - Data|
|5|Sesión| puertos logicos|
|4|Transporte| tcp/udp|
|3|Red|paquetes|
|2|Enlace Datos|Tramas|
|1|Fisica|bits|

TCP/IP -> Protocolo de control de trasmisión/protocolo de internet

Capas de arquitectura
- Aplicación
    - Define los protocolos para la capa de transporte.
- Transporte
    - Permite que los datos se muevan entre dispositivos.
- Internet
    - Crea/inserta paquetes.
-Interfaz de red
    - Como se mueven los datos a travez de la red.
- Aplicación
    - FTP (Protocolo de transferencia de archivos)
    - SMTP (Protocolo simple de transferencia de correo)
    - DNS (Servicio de nombre de dominios)
-Transporte
    - TCP (Protocolo orientado a conexión de duplex completo)
    - UDP (Protocolo simples sin conexión)
- Internet
    - ICMP (Protocolo de mensaje de control de internet)
    - Ping

Protocolo de internet - IPv4, IPv6

IPv4 -> Direcciones de 32 bits

IPv6 -> Direcciones de 128 bits

*IPv4*
- Se expresan como cuatro octetos separadas.
- Cada octeto tiene un valor de 0 y 255
- Tiene dos partes: 
    - Numero de red
    - Numero de host

ICANN (Coorporación de internet para la asignación de nombres y numeros)

Direcciones publicas y privadas

*IPv6*
- Un campo de dirección mucho más grande.
- Seguridad mejorada.
- Calidad de servicio mejorada
- Usa el rango hexadecimal
- ::1 es la dirección loopback

¿Que es wifi?
- Redes inalámbricas
- Las intrusiones de mediar inalambricos puede ocurrir a distancia.

Seguridad de red
- Ataques de DOS/DDOS
- Ataques de fragmentos
- Ataques de paquetes de gran tamaño
- Ataques de suplantación de identidad
- Ataques de intermediarios
- Ataques pasivos

Puertos y protocolos (Aplicación/servicio)

*Puertos fisicos*
-   Son puertos de los enrutadores conmutadores, servidores a los que se conecta los cables.

*Puertos logicos*
- Determinan donde van los datos de trafico.
- Ejm. 
    - HTTP (Trafico de red) - Puerto 80
    - HTTPS (Trafico de red seguro) - Puerto 443

Puertos:

*Puertos conocidos* (0-1023)
- Ejm. TCP/IP,  DNS, SMTP

*Puertos registrados* (1024 - 49151)
- Ejm. Radius (1812), SQL (1433/1434), Api rest Docker (2375/2376)

*Puertos privados* (49152 - 65535)
- Ejm. Puertos temporales que se asigna a alguien.

Puertos seguros
| | | | | |
|--|--|--|--|--|
|Puerto INSEGURO|Nombre|-->|puerto SEGURO|Nombre|
|21|FTP|-->|22|SFTP|
|23|Telnet|-->|22|SSH|
|25|SMTP|-->|587|SMTP|
|37|TIME|-->|123|NTP|
|53|DNS|-->|853|DoT|
|80|HTTP|-->|443|HTTPS|
|143|IMAP|-->|993|IMAP|
|161/162|SNMP|-->|161/162|SNMP|
|445|SMB|-->|2049|NFS|
|389|LDAP|-->|636|636|LDAPS|

SYN - Paquete de sincronización

SYN/ACK

ACK - Acuse de recibido

*Modulo 2 - Comprender las amenazas y ataques (ciberneticos) de red*

*Tipo de amenazas*
- Suplantación de identidad.
- Phising (Direccionamiento de URL)
- DOS/DDOS (Ataque de denegación de servicio)
- Virus (El usuario tiene que participar)
- Gusano (Se propagan solos)
- Troyano (Ranzomware)
- Ataque en ruta - Ataque intermediario (MITM)
- Canal lateral - Ataque pasivo y no invasivo para ver el funcionamiento.
- Amenaza persistente avanzado (ATP)
- Amenaza interna (Perona)
- Malware (programa que se inserta)
- Ransomware

*Identificar amenazas y herramientas para prevenirlos*
- Si un sistema no necesita un servicio o protocolo, no deberia estar en funcionamiento.
- Habilitar los contafuegos

*Herramientas*
- IDS: Identificar amenazas
- HIDS: Host-base IDS - Identifica
- NIDS: Network-base IDS - Identifica
- SIEM
- Antivirus - Identifica y previene
- Scans
- Firewall - Identifica y previene
- IPS: NIPS - HIPS - Identifica y previene

IDS - Sistema de detección de intrusos

*Tipos*
- HIDS: Basada en host supervisa solo una computadora
- NIDS: Supervisa una red observando los patrones de trafico de red.
- SIEM: Información de seguridad y gestión de eventos
 
Prevención de amenazas
- Mantener, actualizar los sistemas y aplicaciones.
- Eliminar o deshabilitar los servicios o protocoles.
- Utilice sistemas de detección y prevención de sistemas.
- Utilice un software antimalware actualizado.
- Utilice cortafuegos

IPS se debe colocar en la linea de trafico, el trafico debe pasar por el IPS.

*Modulo 3 - Comprende la infraestructura de seguridad de red*

Centro de datos locales
- Centro de datos/armarios
    - Telefonos, red, conexiones especiales.
    - Servidores
    - Componentes cableados
- Calefacción, ventilación y aire acondicionado (HVAC)/Ambiental.
- Energia
- Supresión de incendios

Redundancia
- Es diseñar sistemas con componentes duplicado. Ejm. Energia de respaldo.

MOU - Memorando de entendimiento

MOA - Memorando de acuerdo

IOA - Acuerdos operativos conjuntos

SLA - Acuerlo de nivel de servicio

Diferencia de un MOU o MOA y el SLA, es que el MOU esta más directamente relacionado con lo se puede hacer con un sistema o la información
 
*Nube*

CSP - Proveedor de servicios en la nube

*Caracteristicas de la nube*
- El uso se mide y se cotiza según las unidades consumidas.
- Reducción del costo de propiedad.
- Reducción de los costos de energia y enfriamiento.
- Permite a la empresa escalar software.

*Modelo de servicio*
- SaaS -> Software como servicio.
- PaaS -> Plataforma como servicio.
- IaaS -> Infraestructura como servicio.

*Modelo de implementación*
- Publico
- Privado
- Hibrido
- Comunitario

MSP - Proveedor de servicios gestionados

Es una empresa que gestiona activos de tecnologia de la información por otra empresa.

SLA - Acuerdo de nivel de servicio

Entre el proveedor y el cliente.

*Diseño de Red*

Satisfacer los requisitos de comunicación de datos y dar como resultado un redimiento general efeciente.

*Elementos que se tiene en cuenta (Al momento de diseñar una red)*
- Segmentación de red: implica controlar el trafico entre los dispositivos de red.
- Zona Desmilitarizada (DMZ): red diseñada para que accedan visitantes externos.
- Red area local virtual (VLAN)
- Red privada virtual (VPN)
- Defenza de profundidad (protección mediante capas)
- Control de acceso a la red (NAC - politicas de seguridad)

*Defenza en profundidad*

Utiliza un enfoque en capas al diseñar la postura de seguridad de una organización

*Confianza cero*

Suelen ser redes microsegmentadas con contafuegos en casi todos los puntos de conexión.

*Control de acceso a la red - NAC*

Conocer y controlar el acceso a él, tanto para personas internar y externas.

*Segmentación de red (DMZ)*

Forma efectiva de lograr una defenza en profundida para aplicaciones distribuidas o varios niveles

*Segmentación para sistemas embedidas e IoT*

Es una computadora implementada como parte de un sistema más grande.

*Micro Segmentación*

Reglas que se aplican a maquinas y/o usuarios individuales, estas reglas deben ser tan detalladas y complejas.
VPN (Redes privadas virtuales)

*Red de area local virtual (VLAN)*

Separaciones virtuales dentro de un conmutador y se utulizan principalmente para limitar el trafico de difusión.

*Red privada virtualizada (VPN)*

Conexión de punto a punto entre dos host.
