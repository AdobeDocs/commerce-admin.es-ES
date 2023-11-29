---
title: '[!UICONTROL General] &gt; [!UICONTROL General]'
description: Revise la configuración de en [!UICONTROL General] &gt; [!UICONTROL General] de la administración de Commerce.
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

Consulte [Opciones de país](../../getting-started/store-details.md#country-options) para obtener más información sobre estos campos de configuración y estas opciones.

![General > Opciones de país](./assets/general-country-options.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Default Country] | Vista de tienda | El país donde se encuentra su tienda. |
| [!UICONTROL Allow Countries] | Sitio web | Los países en los que acepta pedidos. |
| [!UICONTROL Zip/Postal Code is Optional for] | Global | Países que no requieren un código postal en la dirección de envío. |
| [!UICONTROL European Union Countries] | Global | Países miembros de la Unión Europea. |
| [!UICONTROL Top Destinations] | Vista de tienda | Los países principales a los que se dirigen las ventas. |

{style="table-layout:auto"}

## [!UICONTROL State Options]

Consulte [Opciones de estado](../../getting-started/store-details.md#state-options) para obtener más información sobre estos campos de configuración y estas opciones.

![General > Opciones de estado](./assets/general-state-options.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL State is required for] | Global | Los países (donde realiza negocios) que requieren que se incluya una región o un estado en la dirección postal. |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | Global | En el caso de países en los que no es obligatorio, determina si la variable _Región o estado_ Este campo se incluye en la dirección postal del cliente.<br /> <br />**`Yes`**- Incluye el _Región o estado_ en la dirección del cliente, aunque el país no lo requiera.<br />**`No`** - Omite el campo Región/Estado de la dirección del cliente si el país no lo requiere. |

{style="table-layout:auto"}

## [!UICONTROL Locale Options]

Consulte [Opciones de configuración regional](../../getting-started/store-details.md#locale-options) para obtener más información sobre estos campos de configuración y estas opciones.

![General > Opciones de configuración regional](./assets/general-locale-options.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Timezone] | Sitio web | Zona horaria del mercado primario que sirve el sitio web. Por lo general, la zona horaria es la misma que se utiliza en la ubicación física de su empresa. |
| [!UICONTROL Locale] | Vista de tienda | El idioma, la moneda y el sistema de medición que se utiliza en el mercado servido por la vista de la tienda. |
| [!UICONTROL Weight Unit] | Vista de tienda | La unidad de medida que se suele utilizar para envíos desde la configuración regional. Opciones: `lbs` / `kgs` |
| [!UICONTROL First Day of Week] | Vista de tienda | El día que se considera el primer día de la semana en el mercado servido por la vista de la tienda. |
| [!UICONTROL Weekend Days] | Vista de tienda | Los días que caen en el fin de semana en el mercado servido por la vista de la tienda. |

{style="table-layout:auto"}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![General > Restricciones de sitios web](./assets/general-website-restrictions.png)<!-- zoom -->

Para obtener más información sobre cómo cambiar esta configuración, consulte [Restricciones de acceso](../../merchandising-promotions/event-configure.md#access-restrictions) en el _Guía de promociones y comercialización_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | Sitio web | Determina si el sitio web funciona en modo restringido.<br /> <br />**`Yes`**- El acceso al sitio web está restringido de la manera establecida en los campos siguientes.<br />**`No`** - Las restricciones están desactivadas y la siguiente configuración no tiene efecto. |
| [!UICONTROL Restriction Mode] | Sitio web | Determina el tipo de restricción de acceso que se aplica al sitio web.<br /> <br />**`Website Closed`**: todo acceso a la tienda está restringido y las direcciones URL de la tienda se redirigen temporalmente a la página de aterrizaje. Esta configuración puede resultar útil durante el mantenimiento del sitio o antes del lanzamiento.<br />**`Private Sales: Login Only`** - Solo los clientes registrados pueden iniciar sesión para acceder a la tienda. Todas las URL de la tienda se redirigen temporalmente a la página de aterrizaje especificada o al formulario de inicio de sesión. Los usuarios no pueden crear una cuenta en este modo.<br />**`Private Sales: Login and Register`**- Los usuarios deben iniciar sesión para acceder a la tienda. Todas las URL de tienda se redirigen temporalmente al formulario de inicio de sesión hasta que el usuario inicia sesión. Los usuarios pueden registrarse para obtener una cuenta mientras el sitio se encuentra en este modo. |
| [!UICONTROL Startup Page] | Vista de tienda | Cuando el sitio web se encuentra en modo de ventas privadas, esta configuración determina la página que aparece hasta que el cliente inicia sesión.<br />  <br />**`To login form`**- Los usuarios son redirigidos al formulario de inicio de sesión hasta que inician sesión.<br />**`To landing page`** - Los usuarios se redirigen a la página estática especificada a continuación hasta que inician sesión.<br /> <br />**_¡Importante!_**Asegúrese de incluir un vínculo a la página de inicio de sesión de la página de aterrizaje especificada para que los clientes puedan iniciar sesión y acceder al sitio completo. |
| [!UICONTROL Landing Page] | Vista de tienda | Determina la primera página que aparece cuando el sitio web se encuentra en modo Ventas privadas. |
| [!UICONTROL HTTP Response] | Sitio web | Determina la respuesta HTTP que se envía cuando se cierra el sitio web y un bot, rastreador o araña intenta establecer una conexión.<br /> <br />**`503 Service unavailable`**: la página no está disponible, pero la araña no debe actualizar el índice.<br />**`200 OK`** - La página de aterrizaje es correcta y la araña debe tratarla como la única página del sitio. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Sitio web | Determina si los campos del _Iniciar sesión_ y _Contraseña olvidada_ los formularios se rellenan automáticamente a partir de entradas anteriores. Opciones: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Store Information]

![General > Información de la tienda](./assets/general-store-information.png)<!-- zoom -->

Para obtener más información sobre cómo cambiar esta configuración, consulte [Información de tienda](../../getting-started/store-details.md) en el _Guía de introducción_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Store Name] | Vista de tienda | El nombre de la tienda asociada con la vista de la tienda. |
| [!UICONTROL Store Phone Number] | Vista de tienda | El número de teléfono principal de la tienda (asociado a la vista de la tienda) está abierto para las empresas. Por ejemplo: Lun - Vie, 9-5, Sáb 9-mediodía PST |
| País | Sitio web | El país de la empresa que administra el sitio web. |
| [!UICONTROL Region/State] | Sitio web | La región o el estado de la empresa que administra el sitio web. |
| [!UICONTROL ZIP/Postal Code] | Sitio web | El código postal de la empresa que administra el sitio web. |
| [!UICONTROL City] | Sitio web | La ubicación de la ciudad de la empresa que administra el sitio web. |
| [!UICONTROL Street Address] | Sitio web | La dirección postal de la empresa que administra el sitio web. |
| [!UICONTROL Street Address Line 2|]Sitio web | La segunda línea de la dirección de la calle comercial, si es necesario. |
| [!UICONTROL VAT Number] | Sitio web | El número de IVA de la empresa propietaria de la instalación de Commerce, si corresponde. |
| [!UICONTROL Validate VAT Number] |  | Comprueba el número de identificación del impuesto sobre el valor añadido. |

{style="table-layout:auto"}

## [!UICONTROL Single-Store Mode]

![General > Modo de una sola tienda](./assets/general-single-store-mode.png)<!-- zoom -->

Para obtener más información sobre cómo cambiar esta configuración, consulte [Modo de tienda única](../../getting-started/websites-stores-views.md#single-store-mode) en el _Guía de introducción_.

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | Global | Cuando se habilita para instalaciones de una sola tienda, oculta el cuadro Ámbito de configuración y las etiquetas de campo relacionadas Opciones: `Yes` / `No` <br/>**_Nota:_**El modo de tienda única se omite en las tiendas con más de una vista. |

{style="table-layout:auto"}
