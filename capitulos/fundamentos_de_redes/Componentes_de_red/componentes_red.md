# Componentes de una red

¿Alguna vez te has preguntado cuáles dispositivos intervienen en una red para establecer comunicación entre sí?
Si es así, en este documento encontrarás una explicación clara y detallada sobre los principales dispositivos de red y cómo interactúan para permitir la conectividad.
      

## **1. Router: Arquitecto de la Interconexión de Redes**

Un **router** es un dispositivo de **Capa 3 (Red)** del modelo OSI, cuya función principal es interconectar redes lógicamente separadas, como una Red de Área Local (LAN) con una Red de Área Amplia (WAN) o Internet.

**Función Clave: Enrutamiento (Routing)**

El ruteo o enrutamiento es el proceso de seleccionar la ruta más eficiente para dirigir paquetes de datos desde su red de origen hasta su red de destino. Para lograrlo, el router utiliza las direcciones lógicas (direcciones IP) contenidas en los encabezados de los paquetes.

**Proceso Operativo:**

1.  **Recepción del Paquete:** El router recibe un paquete en una de sus interfaces de red.
2.  **Análisis del Encabezado:** Examina la dirección IP de destino en el encabezado del paquete.
3.  **Consulta de la Tabla de Enrutamiento:** Compara la IP de destino con las entradas de su tabla de enrutamiento (routing table). Esta tabla contiene un mapa de redes conocidas y la mejor ruta para llegar a ellas.
4.  **Reenvío del Paquete:** Envía el paquete a través de la interfaz de salida correspondiente al siguiente \"salto\" (next hop) en la ruta hacia el destino final. Si el destino está en una red directamente conectada, lo envía a ese host.

**Caso de Uso:**

Supongamos que tu dispositivo que tiene el nombre de host Juan con identificacion personal `192.168.1.0/24` necesita enviar datos a pedro (servidor web) que tiene una identificacion `208.67.222.222`. Para que este envio se realize de manera sastifactoria debe el paquete llega al router (el gateway por defecto), (Querio darte mi perpectiva del router, este lo veo como una central de envio por correo, ejemplo servientrega, fedex etc. ellos tienen muchas direcciones registradas y alamcenan esta informacion del origen donde se esta enviando la info hacia el destino y tienen las respectivas direccionen por donde enviar el paquete para que el envio sea exitoso). El router, al no encontrar la red de destino en sus redes conectadas directamente, busca en su tabla de enrutamiento y lo reenvía a la interfaz que lo conecta con su proveedor de servicios de Internet (ISP).

En sintesis el router es el arquitecto de las redes, es el encargado de enviar paquetes de origen a destino siempre seleccionando la mejor ruta, debido a esto a este proceso se le llama ruteo o enrutamiento.

---

### **2. Switch: Optimizador del Tráfico en la Red Local**

Un **switch** es un dispositivo diseñado para conectar múltiples dispositivos finales (endpoints) dentro de la misma red local (LAN). Opera principalmente en la **Capa 2 (Enlace de Datos)**, aunque existen variantes más avanzadas.

En relacion con lo anteriormente dicho, existen varios tipos de switch administrados y no administrados, los cuales varian en cuanto a caracterisiticas y funcionamiento.

### Switch no administrado

Estos como indica su nombre no son administrados, lo que quiere decir es que no es necesaria la intervencion de una persona en redes para configurarlo, ya que la funcion que cumplen solo es enviar tramas. Estos equipos suelen operar en la capa 1 (capa fisica del modelo OSI), ya que solo trasmite informacion sin importar el dispositivo. El hub es un switch no administrado el cual funciona como si fuera un solo cable, este tiene varios puertos donde se puede conectar los equipos, pero sin embargo funciona como si fuera un solo cable, si x usuario envia una trama este va dirigida a todos los puertos. Digamos que es un switch no inteligente.


**Características principales de un switch no administrado:**

- **Fácil de usar:** No requiere configuración, es plug-and-play. 
- **Conectividad básica:** Proporciona conectividad de red a través de puertos Ethernet. 
- **Uso en redes pequeñas:** Ideal para hogares o pequeñas oficinas. 
- **Costo accesible:** Suelen ser más económicos que los switches administrados. 
- **Sin gestión remota:** No permite la configuración ni supervisión remota de la red. 
- **Funciones de seguridad limitadas:** Ofrecen funciones básicas de seguridad, como el cierre de puertos, pero no ofrecen características avanzadas de seguridad. 

**¿Cuándo usar un switch no administrado?**

1. Cuando se necesita conectar varios dispositivos a una red local de forma sencilla. 
2. En redes donde no se requiere una gestión avanzada de la red. 
3. En redes domésticas o pequeñas oficinas. 
4. Cuando se busca una opción económica para ampliar una red existente. 

**Switch administrados**

Como su nombre lo indica este tipo son dministrador, por lo que una persona en el ambito de redes lo puede gestionar y aplicar configuraciones. Adicional estos operan en la capa 2 (Enlace de datos) del modelo OSI. Estos son equipos inteligentes a diferencia de los switch no administrados, debido a que estos aprender las direcciones mac de origen asociada a un puerto y la mac de destino asociada a un puerto en especifico y en base a eso toman decisiones de envio de tramas. Adicional, Permiten ajustar la configuración de cada puerto, controlar el tráfico, y ofrecen funcionalidades como VLANs, calidad de servicio (QoS), y redundancia. 

**Características principales de los switches administrados:**

- **Control y gestión centralizada:** Permiten configurar y monitorear la red desde una única ubicación, facilitando la administración y resolución de problemas. 
- **Mayor seguridad:** Ofrecen opciones para restringir el acceso a la red, bloquear ataques y amenazas, y proteger la información. 
- **Configuración avanzada:** Permiten configurar VLANs, establecer la calidad de servicio (QoS), limitar el ancho de banda por puerto, y otras opciones para optimizar el rendimiento de la red. 
- **Monitorización:** Ofrecen herramientas para monitorear el estado de la red, identificar cuellos de botella, y diagnosticar problemas. 
- **Acceso remoto:** Permiten acceder a la configuración y administración del switch desde diferentes ubicaciones, ya sea a través de una interfaz web o línea de comandos. 
- **Mayor costo:** Generalmente son más costosos que los switches no administrados, pero ofrecen mayores funcionalidades y control.
  
**¿En qué se diferencian de los switches no administrados?**
1. Configuración: Los switches no administrados son plug-and-play y no requieren configuración, mientras que los administrados necesitan ser configurados para funcionar. 
2. Funcionalidades:Los switches no administrados solo ofrecen funciones básicas de conectividad, mientras que los administrados ofrecen funcionalidades avanzadas de gestión y control de red. 
3. Control de tráfico:Los switches no administrados no permiten controlar el tráfico, mientras que los administrados ofrecen opciones para priorizar tráfico, limitar ancho de banda, y configurar VLANs. 
4. Seguridad: Los switches no administrados no ofrecen opciones de seguridad, mientras que los administrados permiten restringir el acceso y proteger la red. 

Tambien dentro de los switch administrados encuentran dos categorias Switch capa 2 (estos son los tradicionales ) y  capa 3 (cuenta con funciones de comutacion y routeo).

**Diferenciación Clave: Layer 2 vs. Layer 3**

*   **Switch de Capa 2:** Su función es la **conmutación** (switching). Utiliza direcciones físicas **(direcciones MAC)** para reenviar tramas de datos únicamente al puerto donde se encuentra el dispositivo de destino. Esto segmenta la red en múltiples dominios de colisión, mejorando drásticamente el rendimiento en comparación con los antiguos hubs.

*   **Switch de Capa 3:** Es un dispositivo híbrido. Combina la funcionalidad de un switch de Capa 2 con capacidades de enrutamiento de Capa 3. Es capaz de enrutar tráfico entre diferentes VLANs (LANs virtuales) sin necesidad de un router dedicado, lo que lo hace ideal para redes corporativas segmentadas.

**Funcionamiento Técnico (Conmutación en Capa 2):**

1.  **Recepción de Trama:** Recibe una trama de datos en uno de sus puertos.
2.  **Aprendizaje de Direcciones (Learning):** Examina la **dirección MAC de origen** y la asocia al puerto por el que ingresó, almacenando esta información en su tabla de direcciones MAC (también conocida como tabla CAM).
3.  **Decisión de Reenvío (Forwarding):** Lee la **dirección MAC de destino** de la trama.
    *   Si la MAC de destino existe en su tabla, reenvía la trama exclusivamente por el puerto asociado.
    *   Si la MAC de destino es desconocida o es una dirección de broadcast (FF:FF:FF:FF:FF:FF), la trama se inunda (*flooding*) por todos los puertos, excepto por el que ingresó.

**Caso de Uso:**
En una oficina, la PC-A envía un archivo a la PC-B. La trama llega al switch. El switch consulta su tabla MAC, identifica que la PC-B está conectada en el puerto 5 y reenvía la trama únicamente a ese puerto. Las demás PCs conectadas a otros puertos no reciben este tráfico, liberando ancho de banda y mejorando la seguridad.

---

### **3. Firewall de Nueva Generación (NGFW): Inteligencia y Control en la Seguridad Perimetral**

Un **Firewall de Nueva Generación (NGFW)** es una plataforma de seguridad de red que evoluciona más allá del filtrado de paquetes tradicional (basado en IP y puertos). Integra capacidades avanzadas para enfrentar amenazas modernas.

**Capacidades Avanzadas Fundamentales:**

*   **Inspección Profunda de Paquetes (DPI - Deep Packet Inspection):** Analiza el contenido (payload) del tráfico de datos, no solo sus encabezados. Esto permite identificar amenazas, malware o datos sensibles que viajan dentro de tráfico aparentemente legítimo.
*   **Conciencia y Control de Aplicaciones:** Identifica y aplica políticas basadas en la aplicación específica (ej. Dropbox, Teams, YouTube), en lugar de depender únicamente del puerto (ej. TCP/80, TCP/443).
*   **Sistema de Prevención de Intrusiones (IPS):** Monitorea el tráfico en busca de patrones que coincidan con firmas de ataques conocidos o comportamientos anómalos, bloqueando activamente las amenazas detectadas.
*   **Integración de Identidad de Usuario:** Aplica políticas de seguridad basadas en la identidad del usuario o grupos (a menudo integrado con servicios como Active Directory), permitiendo un control de acceso granular.

**Proceso Operativo:**

1.  **Intercepción de Tráfico:** Todo el tráfico que atraviesa el perímetro de la red es interceptado.
2.  **Análisis Multinivel:** El NGFW inspecciona el tráfico en múltiples capas: IP/puerto (Capa 3/4), aplicación (Capa 7) y contenido (payload).
3.  **Correlación con Políticas:** Compara los atributos del tráfico (usuario, aplicación, origen, destino, contenido) con el conjunto de reglas de seguridad configuradas.
4.  **Ejecución de Acción:** Basado en la política coincidente, el NGFW permite, bloquea, registra o alerta sobre la conexión.

**Caso de Uso Técnico:**
Un usuario intenta cargar un archivo a un servicio de almacenamiento en la nube no autorizado. El NGFW, a través de DPI y control de aplicaciones, identifica el tráfico en el puerto 443 no como HTTPS genérico, sino como la aplicación \"Mega.nz\". Al verificar las políticas, determina que esta aplicación está prohibida para el grupo de usuarios al que pertenece el empleado y bloquea la conexión, registrando el intento.

---

### **4. Endpoints: El Perímetro Humano y Operativo de la Red**

Un **endpoint** es cualquier dispositivo final que se conecta a la red y actúa como origen o destino de la comunicación de datos. Esto incluye: computadoras, servidores, smartphones, impresoras y dispositivos IoT.

**Rol en la Arquitectura de Red:**

Los endpoints son los dispositivos donde los datos son finalmente consumidos o creados por los usuarios o las aplicaciones. Representan la **superficie de ataque** más extensa y distribuida de una organización.

**Importancia Crítica en la Seguridad:**

Aunque los routers, switches y firewalls protegen la infraestructura de red, los endpoints son inherentemente vulnerables a amenazas como:

*   **Malware (Ransomware, Spyware).**
*   **Phishing e Ingeniería Social.**
*   **Explotación de vulnerabilidades de software no parcheado.**

Un endpoint comprometido puede servir como punto de entrada para un atacante, permitiéndole eludir las defensas perimetrales y moverse lateralmente dentro de la red. Por esta razón, su protección a través de soluciones EDR (Endpoint Detection and Response) y políticas de seguridad robustas es un pilar fundamental de la ciberseguridad moderna.


### 5. Access Point (AP): El Puente Inalámbrico hacia la Red

Un **Access Point (AP)** permite que los dispositivos inalámbricos se conecten a la red cableada mediante Wi-Fi. Es esencial en entornos donde la movilidad y la flexibilidad son clave.

**Rol en la Arquitectura de Red:**

El AP actúa como un **puente entre la red cableada y los dispositivos inalámbricos**, extendiendo la cobertura de red sin necesidad de cables físicos.

**Caso de Uso:**

En una oficina moderna, los empleados utilizan laptops y smartphones conectados por Wi-Fi. El AP transmite la señal inalámbrica y conecta estos dispositivos al switch principal, permitiendo acceso a servidores, impresoras y recursos compartidos.

**Importancia en Seguridad:**

Los APs mal configurados pueden ser puntos de entrada para ataques como:

- **Rogue APs** (puntos de acceso falsos).
- **Sniffing de tráfico inalámbrico.**
- **Acceso no autorizado a la red interna.**

Por ello, se recomienda implementar **WPA3**, segmentación de red (VLANs), y control de acceso por MAC.

---

### 6. Servidores: El Núcleo de los Servicios en Red

Un **servidor** es un dispositivo que proporciona servicios a otros dispositivos en la red, como almacenamiento, autenticación, correo electrónico o aplicaciones.

**Rol en la Arquitectura de Red:**

Los servidores son el **centro de procesamiento y distribución de datos**. Todo lo que los usuarios consumen —archivos, páginas web, correos— proviene de servidores.

**Caso de Uso:**

Un servidor de archivos permite que los empleados accedan a documentos compartidos desde cualquier dispositivo autorizado en la red.

**Importancia en Seguridad:**

Los servidores son objetivos críticos para los atacantes. Un compromiso puede significar:

- **Exfiltración de datos sensibles.**
- **Interrupción de servicios.**
- **Propagación de malware.**

Se recomienda aplicar **hardening**, segmentación, monitoreo continuo y actualizaciones periódicas.

---

### 7. Tecnología PoE: Energía y Datos en un Solo Cable

**Power over Ethernet (PoE)** permite transmitir energía eléctrica junto con datos a través del mismo cable de red Ethernet.

**Rol en la Arquitectura de Red:**

PoE simplifica la instalación de dispositivos como APs, cámaras IP y teléfonos VoIP, eliminando la necesidad de fuentes de alimentación externas.

**Caso de Uso:**

Una cámara IP instalada en el techo de una oficina se conecta a un switch PoE. El mismo cable proporciona energía y conectividad de red.

**Importancia en Seguridad y Gestión:**

Aunque PoE no afecta directamente la seguridad lógica, su implementación debe considerar:

- **Protección contra sobrecargas.**
- **Monitoreo del consumo energético.**
- **Uso de switches PoE gestionados para control granular.**

