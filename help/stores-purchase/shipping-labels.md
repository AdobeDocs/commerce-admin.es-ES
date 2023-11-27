---
title: Etiquetas de envío
description: Obtenga información sobre el flujo de trabajo de etiquetas de envío para envíos regulares y productos con autorización de devolución de mercancía.
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Etiquetas de envío

Commerce incluye un alto nivel de integración con los principales transportistas, lo que le permite acceder a los sistemas de envío de los transportistas para rastrear pedidos, crear etiquetas de envío y mucho más. Se pueden crear etiquetas de envío para envíos regulares y productos con autorización de devolución de mercancía. Además de la información proporcionada por el transportista, la etiqueta también incluye el número de pedido de comercio, el número del paquete y la cantidad total de paquetes para el envío.

![Etiqueta de envío con prioridad USPS](./assets/shipping-usps-priority-label.png){width="300"}

- [Configurar etiquetas de envío](shipping-label-configure.md)
- [Crear etiquetas y paquetes de envío](shipping-label-create.md)

## Flujo de trabajo de etiquetas de envío

Las etiquetas de envío se pueden producir en el momento en que se crea un envío o más tarde. Las etiquetas de envío se almacenan en formato PDF y se descargan en el equipo.

### Paso 1: el comerciante envía una solicitud de etiqueta de envío

El comerciante/gestor de tienda completa la información necesaria para generar etiquetas y envía la solicitud.

### Paso 2: Solicitud enviada al transportista

Commerce se pone en contacto con el transportista y crea un pedido en su sistema. Se crea un pedido independiente para cada paquete enviado.

### Paso 3: El operador envía la etiqueta y el número de seguimiento

El transportista envía la etiqueta de envío y el número de seguimiento del envío.

- Un solo envío con varios paquetes recibe varias etiquetas de envío.

- Si genera las mismas etiquetas de envío varias veces, se conservan los números de seguimiento originales.

- Para los productos devueltos con números RMA, los números de seguimiento antiguos se sustituyen por otros nuevos.

### Paso 4: El comerciante descarga e imprime la etiqueta

Una vez generada la etiqueta de envío, se guarda el nuevo envío y se puede imprimir la etiqueta. Si la etiqueta de envío no se puede crear debido a problemas con la conexión o a cualquier otro motivo, el envío no se crea. Según la configuración del explorador, el archivo del PDF se puede abrir e imprimir. Cada etiqueta aparece en una página independiente en el PDF.
