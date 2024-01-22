---
title: Solicitud de presupuesto
description: Descubra cómo los clientes asociados a una cuenta de compañía pueden enviar una solicitud de presupuesto.
exl-id: c52176a7-4076-4cea-8ddb-17e0d1a77fd9
feature: B2B, Quotes
role: Admin, User
source-git-commit: b53d77364f09e587813c50221ebd85ac633f1296
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Solicitud de presupuesto

Si las comillas están habilitadas en la variable [Configuración de funciones de ventas](configure-quotes.md), un comprador autorizado de una empresa puede iniciar el proceso de negociación de precios solicitando un presupuesto de su carro de compras. Si un comprador no está preparado para enviar una oferta para su negociación, puede guardarla como borrador.

>[!NOTE]
>
>Una solicitud de presupuesto no puede incluir códigos de descuento ni tarjetas regalo.

## Experiencia de solicitud de presupuesto de cliente

1. El cliente inicia sesión en su cuenta de usuario como comprador con [permiso](account-company-roles-permissions.md) para solicitar un presupuesto.

1. Agrega los productos que se van a incluir en la cotización al carro de compras.

   >[!TIP]
   > 
   >Los clientes pueden añadir una lista de SKU de productos al carro de compras más rápidamente mediante [Pedido rápido](quick-order.md).

1. Selecciona **[!UICONTROL Request a Quote]**.

   ![Solicitud de una cotización del carro de compras](./assets/quote-request-from-cart.png){width="700" zoomable="yes"}

1. En el **[!UICONTROL Add your comment]** , el cliente introduce una breve nota para describir la solicitud.

1. Introduce un **[!UICONTROL Quote Name]**.

   ![Introducción de los comentarios y el nombre del presupuesto](./assets/quote-request-from-cart-name-comments.png){width="400" zoomable="yes"}

1. Si es necesario, adjunta un documento o una imagen de apoyo a la cita:

   - Selecciona **[!UICONTROL Attach file]**.
   - Selecciona el archivo de su sistema.

   De forma predeterminada, una [archivo adjunto](configure-quotes.md) puede tener hasta 2 MB, en cualquiera de los siguientes formatos de archivo: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG o JPEG, PNG.

1. Crea y procesa la oferta:

   - Envía la oferta al vendedor seleccionando **[!UICONTROL Request a Quote]**.
   - [!BADGE Capacidad beta 1.5.0]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible solo para participantes del programa beta"}**[!UICONTROL Save as Draft]**.

     Si el comprador guarda la oferta como borrador, la oferta estará disponible en [!UICONTROL My Quotes] in `Draft` estado. El vendedor no puede ver los borradores de presupuestos hasta que el comprador los envíe para su revisión.
