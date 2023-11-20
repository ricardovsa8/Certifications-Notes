**Capitulo 5 - Operaciones de seguridad**

*Modulo 1 - Comprender la seguridad de los datos*

-> Manejo de datos

*Ciclo de vida de un dato*:
- Crear
    - Crear el conocimiento - Tacito
- Almacena
    - Almacenarlo o grabarlo de alguna manera - Explicito
- Usar
    - Utilizar el conocimiento
- Compartir
    - Compartir los datos con otros usuarios, copia o movimiento.
- Archivar
    - Los datos cuando no se necesiten temporalmente.
- Destruir
    - Destruir los datos cuando ya no son necesarios.

*Practicas de manejo de datos*

- Clasificación

    - Es el proceso de reconocer los impactos organizacionales si la información sufre algín compromiso.
    - Dictan reglas y restricciones sobre como se puede usar, almacenar o compartir esa información.
- Etiquetado
    - Son parte de la implementación de controles para proteger la información clasificada.

*Niveles  y etiquetas de confidencialidad de datos*
- Altamente restringido.
- Moderadamente restringido.
- Sensibilidad baja "Para uso interno"
- Datos publicos

*Retención*

Solo deben conservarse el tiempo que sea beneficioso, ni más, ni menos.

*Destrucción*

Datos que quedan despues de la eliminación se llaman "REMANENCIA".
- Limpiar el dispositivo o el sistema
    - "Sobre escribir" poner a cero el dispositivo.
- Purgar el dispositivo o el sistema
    - Desmagnetización
- Destrucción fisica del dispositivo.

*Registro y monitoreo de eventos de seguridad*

Registro es la forma principal de intrumentación que intenta capturar señales generados por eventos.
- Identificaciones de usuario.
- Actividades del sistema.
- Fecha/hora del evento.
- Identidad del dispositivo y la ubicación
- Intentos exitosos y rechazados de acceso al sistema y recursos.
- Cambios en la configuración del sistema y eventos de activación y desactivación.

* Mejores prácticas de registros de eventos*
- El monitoreo de ingreso se refiere a la vigilancia y evaluación de todo el trafico.
    - Cortafuegos
    - Pasarelas
    - Servidores de autenticación remota
    - Herramienta IPS/IDS
    - Soluciones SIEM
    - Soluciones antimalware
- El monitoreo de salida se usan para regularizar los datos que salen del entorno de TI de la organización.

DLP - Prevención de perdida de datos.
- Correo electronico
- Copiar a medios portatiles
- FTP (Protocolo de transferencia de archivos)
- Publicaciones en una pagina web
- API (Aplicaciones /Interfaces de programaciones de aplicaciones)

*Descripción general del cifrado*
- El cifrado protege nuestras transacciones personales y comerciales.
- Se utiliza para proteger la informaación.
- Convertir a un modo "Texto cifrado"

Confidencialidad
- Al ocultar o oscurecer un mensaje para que nadie excepto el destinatario pueda entenderlo.

Integridad
- Funciones de hash
- Firmas digitales

Sistema de cifrado es el conjunto de hardware, software, algoritmo, parametros de central que proporcionan un confunto de servicios de cifrado.

Texto sin formato, solo datos o el mensaje en su forma o formato normal.

Texto plano:  Archivo de imagen audio, video en su forma cruda o comprimida.

Texto y numeros legibles por humanos.

Archivos de BD o registros o cualquier cosa que puede representarse en forma digital para su procesamiento.

OJO: Texto sin formato gran parte no es legible para los humanos.

*Cifrado Simetrico*

Utiliza la misma clave en el proceso de encriptación como en el desencriptación.

*Usos principales de algoritmos simetricos*
- Cifrado de datos masivos.
- Cifrado de mendajes a trave de canales de comunicación
- Transmisión de datos a gran escala y sensibles al tiempo.

Otros nombre
- Misma clave
- Tecla unica
- Llave compartidad
- Llave secreta
- Clave de sesión

*Cifrado Asimetrico*

Utiliza una clave para cifrar y una clave diferente para descifrar el texto sin formato de entrada.

PKI - Clave publica

- Cualquir puede cifrar con la clave publica del destinatario pero solo el destinatario con su clave privada puede descifrarlo.

*Descripción general del cifrado*

Hash
-  Garantiza la integrida de los mensajes

Propiedades
- Util
- No reversible
- Garantia de integrida del contenido.
- Unido
- Determinista (Siempre usa la misma hash cuando el usa el mismo algitmo)

Entrada de datos variables + algoritmo hash = salidad de datos de tamaño de bit fijo (El resumen).

*Modulo 2 - Comprender el endurecimiento del sistema*

Gestión de la configuración

Es un proceso y una disciplina que se utiliza para garantizar que los unicos cambios realizados sean aquellos que fueron autorizados y validados.

*ComponentesA*
- *Identificación*
    - Identificación de linea base de un sistema y todos sus componentes, interfases y documentación.
- *Linea Base*
    - Es el nivel minimo de protección.
    - Esten a un nivel minimo aceptable comprendido de los requisitos de seguridad.
- *Control de cambios (Actualización)*
    - Proceso de revisión y aprobación de todos los cambios.
- *Verificación y auditoria*
    - Verificar que nada en el sistema haya sido dañado con la actualización.
- *Inventario*
    - No puedes proteger lo que no sabes lo que tienes.

Lineas base

Actualizaciones

Parches (Gestión de parches)


*Modulo 3 - Comprender las politicas de seguridad de mejores practicas*

Politicas de seguridad comunes
- Politica de manejo de datos
- Politica de contraseña
- Politica de uso aceptable (AUP)
    - Acceso a los datos
    - Acceso al sistema
    - Divulgación de datos
    - Contraseñas
    - Retención de datos
    - Uso de internet
    - Uso de dispositivos de la empresa
- Politica de trar su propio dispositivo (BYOD)
- Politica de privacidad
- Politica de gestión de cambio
    - Actividades principales:
        - Decidir cambiar
        - Realizar el cambio
        - Confirmar el cambio

Politicas de seguridad comunes
Analisis más profundo

- Se establecen de acierto con la necedisdades de la organización y vision y mision
- Sanciones en el caso de incumplimiento.

Componentes de gestión de cambios
- Documentación ( RFC)
- Aprobación
- Retroceder

*Modulo 4 - Comprender la capacitación de la concientización sobre seguridad*

Objetivo
- Es la capacitación de concientización en función de responsabilidades, evitar poner en riesgo la organización.

Tipos de aprendizaje
- Educación
- Capacitación
- Conciencia

Ejemplos
- Suplantación de identidad - Pishing
- Ingenieria social
- Protección de contraseña