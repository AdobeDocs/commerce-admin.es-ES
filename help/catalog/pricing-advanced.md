---
title: Precios avanzados
description: Obtenga información acerca de los controles de precios avanzados disponibles en Adobe Commerce.
exl-id: 0f353341-1b6b-4093-bba9-4a1b88323f8a
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# Precios avanzados

Adobe Commerce y Magento Open Source admiten varias opciones de precios que puede utilizar para promociones o para satisfacer los requisitos de precios mínimos anunciados por el . Los cambios en los precios de los productos se pueden realizar según lo programado o por regla de precio que se aplique en el nivel de producto o en el carro de compras.

Administre los precios de sus productos con precios avanzados para ofrecer a los clientes mejores tarifas que animen a los consumidores a gastar más, dirigir el tráfico a su sitio y eliminar las existencias antiguas.

La configuración de _[!UICONTROL Advanced Pricing]_define las condiciones necesarias para los precios especiales disponibles para un grupo de clientes o catálogo compartido específico. Los precios avanzados se pueden aplicar a productos simples, virtuales, descargables y agrupados. Para aplicar precios con descuento a otros tipos de productos, usa una [regla de precio de catálogo](../merchandising-promotions/price-rules-catalog.md). Para obtener más información, consulte [Precios](catalog-price-scope.md).

Los datos de precios avanzados se sincronizan con las páginas de productos. Por ejemplo, si actualiza una cantidad de precio de nivel, el sistema actualiza el valor en la página del producto.

![Adobe Commerce B2B](../assets/b2b.svg) (disponible solo con [Adobe Commerce B2B](./b2b/../introduction.md)) Si utiliza catálogos compartidos, los datos de precios avanzados se sincronizan con las páginas de productos y los catálogos compartidos. Por ejemplo, si actualiza una cantidad de precio de nivel, el sistema actualiza el valor en el catálogo compartido y en la página del producto. Cualquier precio personalizado que se indique en el catálogo compartido tiene prioridad sobre los precios del grupo de clientes. Consulte también [Establecer precios y estructura de catálogo compartido](https://experienceleague.adobe.com/docs/commerce-admin/b2b/shared-catalogs/define/catalog-shared-pricing-structure.html) en la _Guía B2B de Adobe Commerce_.

![Precios avanzados](./assets/product-pricing-advanced-link.png){width="600" zoomable="yes"}

## Acceso a las opciones de precios avanzadas

1. Abra el producto en modo de edición.

1. En **[!UICONTROL Price]**, haga clic en **[!UICONTROL Advanced Pricing]**.

1. Siga las instrucciones para el tipo de precio avanzado que se necesita.

   - [Precio de grupo](product-price-group.md)

   - [Precio especial](product-price-special.md)

   - [Precio de nivel](product-price-tier.md)

   - [Precio Mínimo Anunciado](product-price-minimum-advertised.md)

## Referencia de página

### [!UICONTROL Special Price]

Para ofrecer un precio con descuento durante un periodo de tiempo específico o una campaña programada, introduzca el precio especial. Cuando hay un precio especial disponible, el precio de venta se tachará y el precio especial aparecerá a continuación en un texto grande y en negrita.

#### [!UICONTROL Special Price From] fechas

{{ce-feature}}

| Campo | Descripción |
| ---- | ----------- |
| [!UICONTROL From] | Establece la primera fecha en la que está disponible el precio especial. Puede introducir la fecha o seleccionarla en el calendario. |
| [!UICONTROL To] | Establece la última fecha en la que está disponible el precio especial. Puede introducir la fecha o seleccionarla en el calendario. |

{style="table-layout:auto"}

### [!UICONTROL Cost]

Introduzca el coste real del artículo.

### [!UICONTROL Customer Group Price]

![Precios avanzados](./assets/product-pricing-advanced-group-price.png){width="600" zoomable="yes"}

Establece precios promocionales y de nivel para grupos de clientes específicos.

| Elemento | Descripción |
| ---- | ----------- |
| [!UICONTROL Website] | Identifica el sitio web donde se aplica la regla de precios de grupo. Esta opción solo aparece si la instalación tiene varios sitios web. |
| [!UICONTROL Customer Group] | (Obligatorio) Identifica el grupo de clientes que cumple los requisitos para recibir el precio de descuento. Cuando se cambia un valor de un grupo o campo de catálogo, la fila de precio personalizado correspondiente que coincide con la configuración anterior se elimina del catálogo compartido. <br/>**[!UICONTROL ALL GROUPS]**- Aplica la regla a todos los grupos de clientes.<br/>**[!UICONTROL NOT LOGGED IN]**: aplica la regla a los invitados y clientes que no iniciaron sesión en sus cuentas. |
| [!UICONTROL Quantity] | Especifica la cantidad necesaria para recibir un precio de nivel. |
| [!UICONTROL Price] | (Obligatorio) Especifica un precio de producto fijo o descuento para los miembros del grupo de clientes, dentro del sitio web específico. Opciones: <br/>**[!UICONTROL Fixed]**- (Predeterminado) El precio de descuento se introduce como un valor decimal fijo. Por ejemplo, escriba `9.99` como precio de descuento.<br/>**[!UICONTROL Discount]** - El precio de descuento se introduce como porcentaje (%) del precio base del producto. Por ejemplo, escriba `10` para obtener un descuento del 10%. |
| ![Icono de papelera](../assets/icon-delete-trashcan-solid.png) | Elimina la regla actual. |
| **[!UICONTROL Add]** | Inserta otra fila para una regla nueva. |

{style="table-layout:auto"}

### [!UICONTROL Catalog and Tier Price]

Establece precios promocionales y de nivel para catálogos compartidos específicos y grupos de clientes.

{{b2b-feature}}

![Precios avanzados para tiendas B2B con catálogos compartidos](./assets/product-pricing-advanced.png){width="600" zoomable="yes"}

| Elemento | Descripción |
|----|-----------|
| [!UICONTROL Website] | Identifica el sitio web donde se aplica la regla de precios de grupo. Esta opción solo aparece si la instalación tiene varios sitios web. <br>**_Importante:_**ALso selecciona_Sitio web _en la configuración de [Ámbito del precio del catálogo](catalog-price-scope.md); de lo contrario, se muestran los precios avanzados establecidos para**todos los **sitios web. |
| [!UICONTROL Group or Catalog] | (Obligatorio) Identifica el grupo de clientes o el catálogo compartido que cumple los requisitos para recibir el precio de descuento. Cuando se cambia un valor de un grupo o campo de catálogo, la fila de precio personalizado correspondiente que coincide con la configuración anterior se elimina del catálogo compartido. <br/>**[!UICONTROL ALL GROUPS]**- Aplica la regla a todos los grupos de clientes. El valor no se aplica al catálogo compartido y los cambios en los datos de precios avanzados no se sincronizan con el catálogo compartido.<br/>**[!UICONTROL NOT LOGGED IN]**: aplica la regla a los invitados y clientes que no iniciaron sesión en sus cuentas.<br/>**[!UICONTROL Shared Catalogs]**- Aplica la regla a un catálogo compartido específico. |
| Cantidad | Especifica la cantidad necesaria para recibir un precio de nivel. |
| [!UICONTROL Price] | (Obligatorio) Especifica un precio de producto fijo o descuento para los miembros del grupo de clientes, dentro del sitio web específico. Opciones: <br/>**[!UICONTROL Fixed]**- (Predeterminado) El precio de descuento se introduce como un valor decimal fijo. Por ejemplo, escriba `9.99` como precio de descuento.<br/>**[!UICONTROL Discount]** - El precio de descuento se introduce como porcentaje (%) del precio base del producto. Por ejemplo, escriba `10` para obtener un descuento del 10%. |
| ![Icono de papelera](../assets/icon-delete-trashcan-solid.png) | Elimina la regla actual. |
| **[!UICONTROL Add]** | Inserta otra fila para una regla nueva. |

{style="table-layout:auto"}

### [!UICONTROL Minimum Advertised Price]

El precio mínimo anunciado (MAP) para el producto.

### [!UICONTROL Display Actual Price]

Determina si el cliente puede ver el precio real del producto.

| Elemento | Descripción |
|----|-----------|
| [!UICONTROL Use Config] | Utiliza el valor de configuración actual para la visualización de precios. |
| [!UICONTROL On Gesture] | Muestra el precio real del producto en una ventana emergente, en respuesta a _Haga clic para ver el precio_ o _¿Qué es esto?_ vínculo. |
| [!UICONTROL In Cart] | Muestra el precio real del producto en el carro de compras. |
| [!UICONTROL Before Order Confirmation] | Muestra el precio real del producto al final del proceso de cierre de compra, justo antes de que se envíe el pedido. |

{style="table-layout:auto"}
