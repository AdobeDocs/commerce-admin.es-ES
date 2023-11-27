---
title: Iniciar presupuesto para un comprador
description: Aprenda cómo un vendedor puede crear una oferta para que un comprador específico inicie el proceso de negociación. El vendedor sólo puede enviar presupuestos a los clientes asociados a una cuenta de la empresa en el sitio web seleccionado.
exl-id: 7bbb281f-7b6a-45fa-b906-da314d159bc8
feature: B2B, Quotes
role: Admin, User
source-git-commit: be3427f6cc2bab68b6d2b0fa0c36b83dc310e528
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# Iniciar un presupuesto para un comprador

Si las comillas están habilitadas en la variable [Configuración de funciones de ventas](configure-quotes.md), un representante de ventas puede iniciar el proceso de negociación con un comprador de la empresa creando una oferta desde el administrador.

- Solo el vendedor puede ver los borradores de presupuestos.
- No se pueden enviar presupuestos provisionales hasta que el vendedor añada artículos, descuentos y notas relevantes para crear la oferta inicial para el comprador.
- Un vendedor puede crear una oferta a partir de la cuadrícula Ofertas o Cliente.

El representante de ventas envía la oferta al comprador para iniciar el proceso de negociación. Consulte [Negociar una oferta](quote-price-negotiation.md).

## Experiencia de creación de presupuesto de representante de ventas

Un representante de ventas puede crear una oferta a partir de la cuadrícula Ofertas o Cliente.

>[!NOTE]
>
>Para ver un vídeo de demostración de cómo un vendedor crea un presupuesto para un comprador, consulta [El representante de ventas inicia la oferta](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/sales-rep-initiates-quote.html) in _Vídeos y Tutorials de Commerce_.

### Creación de una oferta desde la cuadrícula Oferta

1. El representante de ventas inicia sesión en el administrador como administrador con [Permisos de operaciones de ventas](../systems/permissions.md) para administrar presupuestos.

1. En el Administrador, vaya a [!UICONTROL Quotes] cuadrícula seleccionando **[!UICONTROL Sales]**, y luego seleccione **[!UICONTROL Quotes]**.

1. Crea un presupuesto para un comprador.

   - En la cuadrícula Comillas, seleccione **[!UICONTROL Create New Quote]**.

     ![El vendedor que inicia un presupuesto de comprador de parte del administrador](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

   - En el [!UICONTROL Create New Quote] , seleccione el cliente (comprador de la empresa) para crear la oferta.

     ![Seleccionar cliente para nueva oferta](./assets/quote-draft-from-admin-select-buyer.png){width="700" zoomable="yes"}

     Aparece una nueva oferta en `Draft` estado.

     ![Nuevo presupuesto provisional creado por el vendedor](./assets/quote-create-by-seller.png){width="700" zoomable="yes"}

   - Actualice el nombre de la oferta y modifique la fecha de caducidad según sea necesario.

   - Guarde la oferta como borrador.

## Preparar el presupuesto para el comprador

Después de crear el presupuesto provisional, añade artículos de producto, aplica descuentos y comunícate con el comprador añadiendo comentarios y cualquier archivo relacionado al presupuesto. A continuación, envía el presupuesto al comprador para que lo revise o guárdalo como borrador.

1. Añada elementos a la oferta seleccionando **[!UICONTROL Add Product By SKU]**. Introduzca el número de SKU y la cantidad y, a continuación, seleccione **[!UICONTROL Add Product]**.

![El vendedor agrega artículos al presupuesto provisional del comprador](./assets/quote-draft-add-items.png){width="700" zoomable="yes"}

1. Aplique descuentos de artículos de línea a los productos según sea necesario.

   - Desde el [!UICONTROL Select] menú de acción, elija **[!UICONTROL Discount Item]**.

   - En el [!UICONTROL Discount Line item] , seleccione la **[!UICONTROL Discount Type]**.

   ![Aplicar descuento de artículo de línea al presupuesto](./assets/quote-draft-add-items.png){width="700" zoomable="yes"}

   - En el [!UICONTROL Discount] , introduzca el valor del tipo de descuento. Por ejemplo, si seleccionó un porcentaje de descuento, introduzca 10 para aplicar un descuento del 10% al artículo de línea.

   - [!BADGE Funciones beta 1.5.0]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible solo para participantes del programa beta"}

     Después de confirmar el cambio, los atributos de artículo de línea de la cuadrícula de productos se actualizan para mostrar el importe de descuento aplicado. Si el descuento está bloqueado, aparece un icono de bloqueo.

1. Aplique un descuento de nivel de oferta según sea necesario:

   - En el [!UICONTROL Quote Totals - Negotiated Price] , seleccione el tipo de descuento y, a continuación, introduzca el valor que desea aplicar.

     ![El vendedor añade un descuento de nivel de presupuesto](./assets/quote-draft-total-discount.png){width="700" zoomable="yes"}

   La cuadrícula del producto se actualiza para mostrar el descuento.

1. Añade información adicional para el comprador.

   Entrada [!UICONTROL Negotiation - Comments], añade una nota y adjunta los archivos auxiliares necesarios para el comprador en [!UICONTROL Negotiation - Comments]

   ![El vendedor añade información al comprador](./assets/quote-draft-add-info-for-buyer.png){width="700" zoomable="yes"}

   De forma predeterminada, una [archivo adjunto](configure-quotes.md) puede tener hasta 2 MB, en cualquiera de los siguientes formatos de archivo: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG o JPEG, PNG.

1. Procese la oferta.

   Guarda el presupuesto como borrador o envíaselo al comprador.

   Si envías la oferta al comprador, el estado cambia a `Submitted`y la oferta se bloqueará hasta que el comprador la oferta, el estado se actualizará a borrador y se mostrará un mensaje de confirmación:

   ![Presupuesto provisional de confirmación enviado al comprador](./assets/quote-draft-submitted-confirmation.png){width="700" zoomable="yes"}

El comprador recibe una notificación por correo electrónico para revisar la oferta. La oferta está bloqueada hasta que el comprador la devuelva para una negociación posterior. El vendedor puede ver la oferta desde la cuadrícula Oferta o la cuadrícula Cliente.

## Ver y crear presupuestos desde la cuadrícula de cliente

1. En el Administrador, vaya a [!UICONTROL Customer] cuadrícula seleccionando **[!UICONTROL Customers]**, y luego seleccione **[!UICONTROL All Customers]**.

1. Seleccione el ID de cliente de un comprador de empresa.

   ![Presupuesto provisional de confirmación enviado al comprador](./assets/quote-view-customer-quotes.png){width="700" zoomable="yes"}

1. Seleccionar **[!UICONTROL Edit]** para ver la información del cliente.

1. Cree una oferta para el cliente seleccionando, **[!UICONTROL Create Quote]** y siguiendo el proceso para actualizar el borrador de la oferta y enviarlo al cliente.

1. Ver las ofertas existentes de los clientes seleccionando **[!UICONTROL Quotes]**.

   ![Presupuesto provisional de confirmación enviado al comprador](./assets/quote-list-from-customer-information.png){width="700" zoomable="yes"}

1. Abra una oferta seleccionando **[!UICONTROL View]**.

Para obtener más información sobre la gestión del proceso de negociación de presupuestos, consulte [Negociación de una cotización](quote-price-negotiation.md)
