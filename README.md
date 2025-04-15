# SafeBridge
SafeBridge
Sistema Preventivo de Grooming en Redes Domésticas y Educativas

Descripción del Proyecto / Introducción: SafeBridge es una solución de bajo costo y de implementación local que busca prevenir el acoso sexual a menores en entornos digitales (grooming) mediante el monitoreo inteligente del tráfico de red. El sistema está diseñado para correr en un entorno controlado, como una red doméstica o escolar, detectando patrones sospechosos en comunicaciones digitales, sin necesidad de invadir la privacidad del usuario mediante el acceso directo a sus dispositivos o redes sociales.
Definiciones del Proyecto:
Grooming: Estrategia de acoso en la que un adulto se gana la confianza de un menor en plataformas digitales con fines sexuales.
Proxy Local: Servidor que intermedia las conexiones de red y permite inspeccionar el tráfico.
MITMProxy: Proxy de código abierto que permite inspeccionar tráfico HTTPS mediante certificados personalizados.
MikroTik: Router configurable que permite redireccionar todo el tráfico de red hacia el proxy de análisis.
Definiciones del Sistema: SafeBridge se basa en una infraestructura de red compuesta por un router MikroTik que fuerza a todos los dispositivos a pasar su tráfico por un proxy local montado en una Raspberry Pi. Este proxy captura y analiza los paquetes utilizando patrones preentrenados de lenguaje y comportamiento para detectar grooming. Las alertas se notifican a los adultos responsables.
Requisitos:
Funcionales:
Monitorear tráfico HTTP/HTTPS de todos los dispositivos de la red local.
Detectar patrones sospechosos (mensajes, URLs, interacciones) relacionados con grooming.
Asociar tráfico a un dispositivo mediante su MAC address.
Emitir alertas a padres/tutores ante detección.
Generar registros de actividad anonimizados.
No funcionales:
Bajo costo de implementación.
Privacidad del usuario (no accede a cuentas personales).
Funcionamiento 24/7 con bajo consumo.
No necesita instalación en cada dispositivo.

Casos de Estudio:
Familia con hijos en edad escolar que navegan redes sociales desde distintos dispositivos.
Institución educativa que desea prevenir acoso digital dentro de su red Wi-Fi.
Cibercafés o centros comunitarios que ofrecen conectividad a niños y adolescentes.
Propuesta de Solución:
Propuesta Funcional:
Implementar un sistema de análisis del tráfico en tiempo real.
Clasificación de mensajes, URLs o metadatos para detección de interacciones inapropiadas.
Registro de dispositivos conectados mediante sus MACs.
Alertas automatizadas vía correo electrónico o interfaz local.
Propuesta Técnica:
Router MikroTik para redireccionamiento y firewall.
Raspberry Pi (o PC económica) con MITMProxy para inspección de tráfico HTTPS.
Certificado SSL autofirmado instalado en los dispositivos.
Backend con Python (Flask) para procesamiento, clasificación e interfaz.
Modelo de lenguaje básico (NLTK, scikit-learn o HuggingFace) entrenado para patrones de grooming.



