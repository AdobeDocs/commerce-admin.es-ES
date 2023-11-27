---
title: Configuración de eventos
description: Aprenda a completar la configuración básica para habilitar eventos y configurar el bloque de eventos en la barra lateral de la tienda.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
source-git-commit: 084d2c3381f57a8a4c7e8ffde9da1abd4d8af670
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Configuración de eventos

{{ee-feature}}

Para poder crear un evento, debe completar la configuración básica para habilitar los eventos y configurar el bloque de eventos en la barra lateral.

## Habilitar y configurar eventos

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Catalog Events]** y haga lo siguiente:

   ![Configuración del catálogo: eventos de catálogo](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Establecer **[!UICONTROL Enable Catalog Events Functionality]** hasta `Yes`.

   - Establecer **[!UICONTROL Enable Catalog Event Widget on Storefront]** hasta `Yes`.

   - Introduzca el **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. De forma predeterminada, este valor se establece en `5`. Si desea mostrar sólo un evento en el control deslizante a la vez, escriba `1`.

   - Introduzca el número de **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. De forma predeterminada, este valor se establece en `2`. Si desea que el control deslizante muestre el siguiente evento en secuencia al hacer clic, introduzca `1`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Restricciones de acceso

El acceso a una venta, evento o sitio privado se puede limitar a los clientes registrados que inician sesión o ampliar a los clientes no registrados que deben registrarse antes de obtener acceso.

![Configuración general: restricciones del sitio web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Restringir el acceso

El acceso a una venta, evento o sitio privado se puede limitar a los clientes registrados que inician sesión o ampliar a los clientes no registrados que deben registrarse antes de obtener acceso.

![Configuración general: restricciones del sitio web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL General]** y elija **[!UICONTROL General]** debajo.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Website Restrictions]** sección.

1. Establecer **[!UICONTROL Access Restriction]** hasta `Yes`.

1. Establecer **[!UICONTROL Restriction Mode]** a uno de los siguientes:

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Establecer **[!UICONTROL Startup Page]** a uno de los siguientes:

   - `To login form (302 Found)` - Los usuarios son redirigidos al formulario de inicio de sesión antes de obtener acceso al sitio.

   - `To landing page (302 Found)` : se redirige a los usuarios a la página de aterrizaje especificada hasta que inicien sesión.

     >[!IMPORTANT]
     >
     >Asegúrese de incluir un vínculo a la página de inicio de sesión desde la página de aterrizaje para que los clientes puedan iniciar sesión y acceder al sitio.

1. Elija la **[!UICONTROL Landing Page]** que aparece antes de que los clientes inicien sesión en el sitio de venta privado.

1. Para que los bots y las arañas de los motores de búsqueda sepan que la página de aterrizaje es correcta y que no hay otras páginas en el sitio para indexar, establezca **[!UICONTROL HTTP Response]** hasta `200 OK`.

   En todos los demás casos se establece en `503 Service Unavailable`.

   >[!NOTE]
   >
   >Solo se aplica si el modo de restricción está establecido en _Sitio web cerrado_. La página de aterrizaje se procesa como HTML sin procesar.

1. Si desea que los campos de los formularios de inicio de sesión del cliente y contraseña olvidada se rellenen automáticamente a partir de las entradas anteriores, establezca **[!UICONTROL Enable Autocomplete on login/forgot password forms]** hasta `Yes`.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

### Restringir ventas

De forma predeterminada, los productos que aparecen en eventos próximos o cerrados no están disponibles para la venta general y la _[!UICONTROL Add to Cart]_El botón no aparece en la lista de productos o en la página de productos.

Para restaurar la _[!UICONTROL Add to Cart]_para un evento cerrado, el evento debe eliminarse (consulte [Eventos de actualización](event-create.md#update-events)). Sin embargo, si un producto está asociado con otra categoría que no tiene restricciones de venta, el botón está disponible en la página del producto. Del mismo modo, el bloque de valor no aparece en la página del producto si el producto está asociado con otra categoría que no tenga restricciones de venta.
