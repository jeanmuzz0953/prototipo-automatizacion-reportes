# Prototipo de Sistema Automatizado de Reportes Logísticos

### Introducción
Este proyecto nace con el objetivo de resolver un cuello de botella operativo crítico en una empresa de transporte: el registro y transcripción manual de rutas. 

Anteriormente, los choferes documentaban sus paradas utilizando aplicaciones externas de cámara para estampar la fecha, enviando luego estas fotografías a través de grupos de WhatsApp. Esto obligaba al personal administrativo a transcribir manualmente cientos de registros hacia un archivo de Excel al finalizar el mes. Este prototipo propone una solución que descentraliza el proceso, permitiendo que la información sea procesada y enviada directamente desde el punto de origen hacia una base de datos centralizada, prescindiendo por completo de aplicaciones de terceros.

### Metodología
El desarrollo de esta solución se abordó bajo una arquitectura moderna orientada a la movilidad y a la eficiencia en campo:

*   **Arquitectura PWA y Soporte Offline:** Se estructuró el frontend con capacidades de Progressive Web App (PWA). Esto permite que el sistema funcione y registre datos en caché incluso cuando los choferes se encuentran en zonas de ruta sin cobertura de internet, sincronizándose posteriormente.
*   **Procesamiento de Imágenes en el Cliente:** Se eliminó la dependencia de aplicaciones externas (como Timestamp Camera). Al cargar una imagen, el sistema la comprime automáticamente y genera un *overlay* nativo que adjunta la fecha, hora exacta y la geolocalización del dispositivo.
*   **Integración de Backend (Serverless):** La lógica del formulario fue diseñada para conectarse e interactuar nativamente con Google Apps Script.
*   **Gestión y Visualización de Datos:** La información ingresada elude los canales informales y se inyecta en tiempo real en un documento de Google Sheets. Este entorno está configurado de antemano con tabulación automática y generación dinámica de gráficos, transformando entradas crudas en reportes visuales instantáneos sin requerir ninguna intervención administrativa.

### Resultados
La implementación de este prototipo demuestra que es posible trasladar la carga de trabajo de ingreso de datos al usuario final mediante una interfaz sencilla y robusta. La capacidad de operar sin conexión y el procesamiento automatizado de metadatos eliminan la fricción para los choferes. Por su parte, la administración obtiene un tablero de control (dashboard) automatizado y estructurado, eliminando al 100% el tiempo de digitación y ensamblaje de reportes a fin de mes.

