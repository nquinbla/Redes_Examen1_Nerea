# EXAMEN REDES
Examen de la alumna Nerea Quintanilla Blanco con NP 154409, de la asignatura de Redes.  
* Link: https://github.com/nquinbla/Redes_Examen1_Nerea.git

## [ 📍 ] ÍNDICE

**Parte I: Conceptos y Teoría**
1. [🏛️ El mural de las siete capas](#el-mural-de-las-siete-capas)
2. [ 🧾 Los dos pergaminos del mensajero](#los-dos-pergaminos-del-mensajero)
3. [ 🪨 El Enigma de las Subredes](#el-enigma-de-las-subredes)
4. [ 🏹 La Encrucijada de las Rutas](#la-encrucijada-de-las-rutas)
5. [ 🎭 El Guardián de la Máscara Única](#el-guardian-de-la-mascara-unica)

**Parte II: Práctica con Cisco Packet Tracer**
1. [ 🏜️ La Ruta Perdida entre Dos Reinos](#ejercicio-1-la-ruta-perdida-entre-dos-reinos)
2. [ 🏰 La Ciudad de las Redes Aisladas](#ejercicio-2-la-ciudad-de-las-redes-aisladas)
***

## [ Parte I ] CONCEPTOS Y TEORÍA

### [ 🏛️ ] EL MURAL DE LAS SIETE CAPAS
Este ejercicio busca comprender y relacionar el **Modelo OSI** con un mural antiguo encontrado en un templo, que representa los niveles de comunicación de datos en redes modernas. El mural está compuesto por siete franjas horizontales, cada una representando un nivel en un ritual de comunicación. El ejercicio pide identificar qué representa el mural en términos de redes modernas, explicando las siete capas del Modelo OSI y su función en el proceso de comunicación de datos actual. Cada capa se compara con su equivalente en redes modernas, como la **capa de aplicación**, **capa de transporte** y **capa física**, entre otras.

El **Modelo OSI** (Open Systems Interconnection) es una estructura conceptual que se utiliza para entender cómo los sistemas de comunicación de redes de datos deben ser estructurados y cómo interactúan las distintas capas de comunicación. Cada una de las siete capas cumple con un propósito específico para asegurar que los datos puedan viajar desde una aplicación en un dispositivo hasta su destino en otro dispositivo.

Las siete capas son las siguientes:

1. **Capa 7: Aplicación**: Interacción directa con el usuario final, proporcionando servicios de red a las aplicaciones. Ejemplos: HTTP, FTP, DNS.
2. **Capa 6: Presentación**: Traduce, cifra/descifra y comprime los datos. Ejemplos: SSL/TLS, codificación ASCII/UTF-8.
3. **Capa 5: Sesión**: Establece, mantiene y finaliza sesiones de comunicación entre aplicaciones. Ejemplo: Control de sesiones en NetBIOS, RPC.
4. **Capa 4: Transporte**: Asegura la entrega fiable y ordenada de los datos, además de controlar el flujo de información. Ejemplos: TCP (confiable), UDP (rápido).
5. **Capa 3: Red**: Determina la ruta y direccionamiento de los paquetes. Ejemplos: IP, ICMP, OSPF.
6. **Capa 2: Enlace de datos**: Controla el acceso al medio físico y la detección de errores. Ejemplos: Ethernet, MAC, ARP.
7. **Capa 1: Física**: Transmite los bits a través del medio físico (cables, señales). Ejemplos: cables, voltajes, señales.

Cada capa tiene una función definida que se asegura de que los datos se transmitan de manera correcta, eficiente y segura a través de las redes. El ejercicio compara cómo estas capas trabajan en conjunto para procesar los datos en redes modernas.

![_- visual selection (1)](https://github.com/user-attachments/assets/a57bf596-59cd-441d-82bc-fc20a3b57eaf)

---

### [ 🧾 ] LOS DOS PERGAMINOS DEL MENSAJERO
Este ejercicio explora los protocolos de comunicación **TCP** y **UDP**, a través de los dos rituales descritos en los pergaminos: el "Mensajero Confiable" y el "Mensajero Veloz". El primer ritual se asocia con el protocolo **TCP (Transmission Control Protocol)**, que garantiza la entrega de mensajes mediante confirmaciones y retransmisiones. El segundo ritual se relaciona con el protocolo **UDP (User Datagram Protocol)**, que transmite datos rápidamente sin preocuparse por la confirmación o el orden de los mensajes.

El ejercicio analiza las características, ventajas y desventajas de ambos protocolos, haciendo un paralelo entre sus características y cómo se comportan en la red:

- **TCP**:
  - Protocolo **confiable**: Se asegura de que los datos lleguen completos y en el orden correcto.
  - Establece una **conexión** antes de transmitir los datos.
  - Garantiza que los mensajes lleguen correctamente mediante la **confirmación** de recepción.
  - Es más **lento** debido al proceso de establecimiento de conexión y la retransmisión de mensajes.
  - Usado en aplicaciones que requieren fiabilidad, como la transferencia de archivos o el correo electrónico.

- **UDP**:
  - Protocolo **no confiable**: No garantiza que los datos lleguen, ni en el orden adecuado, ni la corrección de errores.
  - Es **rápido** porque no realiza la verificación de entrega ni la retransmisión de mensajes.
  - Utilizado en aplicaciones que priorizan la **velocidad** sobre la fiabilidad, como **streaming de video** o **juegos en línea**.

![_- visual selection (2)](https://github.com/user-attachments/assets/16adda72-b36d-42bd-be3c-8442073a2368)

---

### [ 🪨 ] EL ENIGMA DE LAS SUBREDES
En este ejercicio, se presenta un enigma relacionado con la **división de una red** en subredes. La red original tiene la dirección **192.168.50.0/24**, y debe ser **dividida en 4 subredes** de igual tamaño. El objetivo es calcular la **máscara de subred** necesaria para lograr esto y determinar cuántas **direcciones de host utilizables** tendrá cada subred resultante.

Al resolver el enigma, descubrimos que para dividir la red en 4 subredes, es necesario tomar **2 bits** del campo de host. Esto transforma la máscara de subred de **/24 a /26**, lo que permite tener 4 subredes, y cada una tendrá **62 direcciones de host utilizables** (64 menos 2, una para la dirección de red y otra para la de broadcast).

Las subredes resultantes son las siguientes:

| Subred 1              | Subred 2              | Subred 3              | Subred 4              |
|-----------------------|-----------------------|-----------------------|-----------------------|
| 192.168.50.0/26       | 192.168.50.64/26      | 192.168.50.128/26     | 192.168.50.192/26     |

Este ejercicio refuerza el concepto de **subneteo** y cómo calcular las subredes necesarias para dividir una red de acuerdo a los requisitos de red.

---

### [ 🏹 ] LA ENCRUCIJADA DE LAS RUTAS
Este ejercicio describe un **tótem** con flechas fijas y móviles que simboliza el proceso de **enrutamiento** en redes modernas. Las flechas fijas representan el **enrutamiento estático**, mientras que las flechas móviles representan el **enrutamiento dinámico**.

La **tabla de enrutamiento** en un router se utiliza para dirigir los paquetes hacia su destino. El enrutamiento estático se configura manualmente, y las rutas no cambian a menos que un administrador las modifique. En contraste, el enrutamiento dinámico ajusta las rutas automáticamente en función de los cambios en la red, utilizando protocolos como **RIP**, **OSPF** o **EIGRP**.

- **Enrutamiento Estático (Flechas Talladas)**: Las rutas son fijas, y deben ser modificadas manualmente. Es confiable, pero difícil de gestionar en redes grandes.
- **Enrutamiento Dinámico (Flechas Móviles)**: Las rutas se ajustan automáticamente, lo que es más adecuado para redes grandes, pero requiere más recursos y puede ser más complejo de configurar.

![_- visual selection (3)](https://github.com/user-attachments/assets/faa571e5-5c09-49a5-9367-ec764b361b66)

---

### [ 🪨 ] El Guardián de la Máscara Única
Este ejercicio trata sobre el concepto de **NAT (Network Address Translation)**, que permite a múltiples dispositivos de una red local compartir una única dirección IP pública al comunicarse con el exterior.

**NAT** modifica las direcciones IP en los paquetes de datos, reemplazando las IPs internas de los dispositivos por la IP pública del router. Esto permite que muchos dispositivos de la red interna utilicen una sola dirección IP pública para acceder a Internet.

**Beneficios de NAT**:
1. **Aislamiento de la red interna**, mejorando la seguridad.
2. **Facilita el acceso remoto** a servicios específicos sin exponer toda la red.
3. **Reducción de costos**, ya que varios dispositivos pueden compartir una sola IP pública.
4. **Seguridad y privacidad**, ocultando las IPs internas.
5. **Escalabilidad**, permitiendo agregar dispositivos sin necesidad de nuevas IPs públicas.

![_- visual selection (4)](https://github.com/user-attachments/assets/bb90372e-80d0-4c10-9728-3651a9556287)

***
***

## [ Parte II ] Práctica con Cisco Packet Tracer

### [ 🏜️ ] LA RUTA PERDIDA ENTRE DOS REINOS
Este ejercicio tiene como objetivo restaurar la conectividad entre **Ciudad A** y **Ciudad B** utilizando **Frame Relay** a través de una **nube**. La tarea incluye configurar los dispositivos de cada ciudad, incluidos los **routers**, **switches**, y **dispositivos finales** (como **PCs**, **laptops**, y **smartphones**). Además, se configuran las interfaces de red y las rutas estáticas necesarias para establecer la comunicación entre las ciudades.

#### Enunciado:
La **Ciudad A** y **Ciudad B** están conectadas por **Frame Relay**. Se asignan **direcciones IP** a las interfaces de los routers y se configuran las **rutas estáticas** necesarias para la comunicación entre las dos ciudades.

#### Tareas:
1. **Topología de la Red**: Configuración de routers y la nube utilizando **Frame Relay**.
2. **Direccionamiento IP y Subredes**: Configuración de direcciones IP para dispositivos.
3. **Rutas Estáticas**: Configuración de rutas para asegurar la conectividad entre las ciudades.
4. **Configuración de la Red**: Configuración completa de routers y dispositivos inalámbricos.

#### Configuración de los Dispositivos:
- **Router A y Router B**: Configuración de interfaces y rutas estáticas.
- **Nube**: Configuración de Frame Relay.
- **Dispositivos Finales**: Configuración de dispositivos con direcciones IP estáticas.

![Redes Diagrama](https://github.com/user-attachments/assets/9bf847f8-4d6a-4c2c-9e37-fa1fb3b7f042)

---

### [ 🏰 ] LA CIUDAD DE LAS REDES AISLADAS
Este ejercicio configura una red segmentada utilizando **VLANs** para distintos grupos (Arquitectos, Escribas y Guerreros), y permite la comunicación entre estas VLANs utilizando un **Router-on-a-Stick**.

#### Enunciado:
La topología incluye tres **VLANs**:
- **VLAN 10 (Arquitectos)**
- **VLAN 20 (Escribas)**
- **VLAN 30 (Guerreros)**

#### Tareas:
1. **Dispositivos Utilizados**: Router Cisco 2811, Switch Cisco 2960, y Access Point.
2. **Direccionamiento IP y Subredes**: Configuración de direcciones IP dentro de cada VLAN.
3. **Configuración de la Red**: Configuración de subinterfaces en el router y VLANs en el switch.
4. **Conexiones de Dispositivos Inalámbricos**: Configuración de un Access Point para la **VLAN 20**.
5. **Pruebas de Funcionamiento**: Verificación de la conectividad entre dispositivos de diferentes VLANs.

#### Configuración de los Dispositivos:
- **Switch**: Configuración de puertos en las VLANs.
- **Router (Router-on-a-Stick)**: Configuración de subinterfaces para cada VLAN.
- **Access Point**: Configuración de un SSID para la **VLAN 20**.

![Copia de Redes Diagrama](https://github.com/user-attachments/assets/91fc8c75-9bbc-4b67-ae55-557189bb5255)

***

### INSTRUCCIONES PARA ABRIR Y VERIFICAR LOS ESCENARIOS EN CISCO PACKET TRACER:
1. **Versión de Cisco Packet Tracer utilizada**: 8.2 o superior.
2. **Archivos .pkt**: Los archivos correspondientes a cada ejercicio están disponibles en este repositorio. Descarga y abre el archivo en Cisco Packet Tracer.
3. **Pasos para probar la conectividad**:
   - Conecta los dispositivos como se describe en cada ejercicio.
   - Asegúrate de que las rutas y subinterfaces estén configuradas correctamente.
   - Realiza un **ping** entre dispositivos en diferentes subredes o VLANs para verificar la conectividad.
4. **Verificación de configuración**:
   - Revisa la configuración de interfaces y rutas en los routers usando el comando `show run`.
   - Verifica la tabla de enrutamiento en los routers con el comando `show ip route`.
