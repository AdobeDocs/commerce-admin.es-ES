---
title: Iniciar presupuesto para un comprador
description: Aprenda cómo un vendedor puede crear una oferta para que un comprador específico inicie el proceso de negociación. El vendedor sólo puede enviar presupuestos a los clientes asociados a una cuenta de la empresa en el sitio web seleccionado.
exl-id: 7bbb281f-7b6a-45fa-b906-da314d159bc8
feature: B2B, Quotes
role: Admin, User
source-git-commit: 69396421bae610ff02b12054bdea2278a8c0efe5
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Iniciar un presupuesto para un comprador

Si las ofertas están habilitadas en la [configuración de características de ventas](configure-quotes.md), un representante de ventas puede iniciar el proceso de negociación con un comprador de la compañía creando una oferta desde el administrador.

- Solo el vendedor puede ver los borradores de presupuestos.
- No se pueden enviar presupuestos provisionales hasta que el vendedor añada artículos, descuentos y notas relevantes para crear la oferta inicial para el comprador.
- Un vendedor puede crear una oferta a partir de la cuadrícula Ofertas o Cliente.

El representante de ventas envía la oferta al comprador para iniciar el proceso de negociación. Consulte [Negociar un presupuesto](quote-price-negotiation.md).

## Experiencia de creación de presupuesto de representante de ventas

Un representante de ventas puede crear una oferta a partir de la cuadrícula Ofertas o Cliente.

>[!NOTE]
>
>Para ver un vídeo de demostración de un vendedor que crea una cotización para un comprador, consulta [El representante de ventas inicia la cotización](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/sales-rep-initiates-quote.html?lang=es) en _Vídeos y Tutorials de Commerce_.

### Creación de una oferta desde la cuadrícula Oferta

1. El representante de ventas inicia sesión en el administrador como administrador con [permisos de operaciones de ventas](../systems/permissions.md) para administrar presupuestos.

1. En el Administrador, vaya a la cuadrícula [!UICONTROL Quotes] seleccionando **[!UICONTROL Sales]** y, a continuación, seleccione **[!UICONTROL Quotes]**.

1. Crea un presupuesto para un comprador.

   - En la cuadrícula Comillas, seleccione **[!UICONTROL Create New Quote]**.

     ![El vendedor está iniciando una cotización de comprador del administrador](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

   - En la página [!UICONTROL Create New Quote], seleccione el cliente (comprador de la compañía) para crear la oferta.

     ![Seleccionar cliente para nuevo presupuesto](./assets/quote-draft-from-admin-select-buyer.png){width="700" zoomable="yes"}

     Aparece una nueva oferta en estado `Draft`.

     ![Nuevo presupuesto provisional creado por el vendedor](./assets/quote-create-by-seller.png){width="700" zoomable="yes"}

   - Actualice el nombre de la oferta y modifique la fecha de caducidad según sea necesario.

   - Guarde la oferta como borrador.

## Preparar el presupuesto para el comprador

Después de crear el presupuesto provisional, añade artículos de producto, aplica descuentos y comunícate con el comprador añadiendo comentarios y cualquier archivo relacionado al presupuesto. A continuación, envía el presupuesto al comprador para que lo revise o guárdalo como borrador.

1. Agregue elementos al presupuesto seleccionando **[!UICONTROL Add Product By SKU]**. Escriba el número de SKU y la cantidad y, a continuación, seleccione **[!UICONTROL Add Product]**.

   ![El vendedor agrega artículos a la oferta provisional para el comprador](./assets/quote-draft-add-items.png){width="675" zoomable="yes"}

1. Aplique descuentos de artículos de línea a los productos según sea necesario.

   - En el menú de acción [!UICONTROL Select], elija **[!UICONTROL Discount Item]**.

   - En el formulario [!UICONTROL Discount Line item], seleccione **[!UICONTROL Discount Type]**.

     ![Aplicar descuento de artículo de línea al presupuesto](./assets/quote-discount-line-item.png){width="675" zoomable="yes"}

   - En el campo [!UICONTROL Discount], introduzca el valor del tipo de descuento. Por ejemplo, si seleccionó un porcentaje de descuento, introduzca 10 para aplicar un descuento del 10% al artículo de línea.

   - De forma opcional, bloquee el valor de descuento de artículo de línea para que el precio del producto no se reduzca aún más por los descuentos aplicados en el nivel de oferta.

     Después de confirmar el cambio, los atributos de artículo de línea de la cuadrícula de productos se actualizan para mostrar el importe de descuento aplicado. Si el descuento está bloqueado, aparece un icono de bloqueo.

   Un representante de ventas puede solicitar un descuento de un artículo de línea específico de una oferta.

   >[!NOTE]
   >
   >Para ver una demostración en vídeo de cómo funcionan los descuentos en el elemento de línea, consulte [El representante de ventas aplica un descuento a un elemento de línea de presupuesto](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/quote-line-item-discount.html?lang=es) en _Vídeos y Tutorials de Commerce_.

1. Aplique un descuento de nivel de oferta según sea necesario:

   - En la sección [!UICONTROL Quote Totals - Negotiated Price], seleccione el tipo de descuento y, a continuación, escriba el valor que desee aplicar.

     ![El vendedor agrega un descuento de nivel de cotización](./assets/quote-draft-total-discount.png){width="700" zoomable="yes"}

   La cuadrícula del producto se actualiza para mostrar el descuento.

1. Añade información adicional para el comprador.

   En la ficha **[!UICONTROL Negotiation - Comments]**, añade una nota y adjunta los archivos auxiliares necesarios para el comprador.

   ![El vendedor agrega información para el comprador](./assets/quote-draft-add-info-for-buyer.png){width="700" zoomable="yes"}

   De manera predeterminada, un [archivo adjunto](configure-quotes.md) puede tener hasta 2 MB, en cualquiera de los siguientes formatos de archivo: DOC, DOCX, XLS, XLSX, PDF, TXT, JPEG o JPG, PNG.

1. Agregar dirección de envío durante las negociaciones.

   Un representante de ventas puede realizar una selección de envío y entrega una vez que el comprador haya añadido una dirección de envío a la oferta.

   Las opciones de envío están bloqueadas en el cierre de compra.

   Para obtener más información, vea [Mis comillas](account-dashboard-my-quotes.md#adding-a-shipping-address).

1. Procese la oferta.

   Guarda el presupuesto como borrador o envíaselo al comprador.

   - Si guarda la oferta como borrador, el estado se actualiza a `Draft` y se muestra un mensaje de confirmación.

   - Si envías la oferta al comprador, el estado cambia a `Submitted`. El comprador recibe una notificación por correo electrónico para revisar la oferta. La oferta está bloqueada hasta que el comprador la devuelva para una negociación posterior. El vendedor puede ver la oferta desde la cuadrícula Oferta o Cliente.

## Ver y crear presupuestos desde la cuadrícula de cliente

1. En el Administrador, vaya a la cuadrícula [!UICONTROL Customer] seleccionando **[!UICONTROL Customers]** y, a continuación, seleccione **[!UICONTROL All Customers]**.

1. Seleccione el ID de cliente de un comprador de empresa.

   ![Presupuesto provisional de confirmación enviado al comprador](./assets/quote-view-customer-quotes.png){width="700" zoomable="yes"}

1. Seleccione **[!UICONTROL Edit]** para ver la información del cliente.

1. Cree una oferta para el cliente seleccionando **[!UICONTROL Create Quote]** y siguiendo el proceso para actualizar la oferta provisional y enviarla al cliente.

1. Vea las ofertas existentes de los clientes seleccionando **[!UICONTROL Quotes]**.

   ![Presupuesto provisional de confirmación enviado al comprador](./assets/quote-list-from-customer-information.png){width="700" zoomable="yes"}

1. Abra una oferta seleccionando **[!UICONTROL View]**.

Para obtener más información sobre cómo administrar el proceso de negociación de ofertas, consulte [Negociar una oferta](quote-price-negotiation.md)
