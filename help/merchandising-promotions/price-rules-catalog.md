---
title: Reglas de precios de catálogo
description: Obtenga información sobre las reglas de precios de catálogo que se pueden usar para ofrecer productos a los compradores a un precio con descuento según un conjunto de condiciones definidas.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Reglas de precios de catálogo

Las reglas de precios de catálogo se pueden utilizar para ofrecer productos a los compradores a un precio con descuento, según un conjunto de condiciones definidas. Las reglas de precios de catálogo no utilizan [códigos de cupón](price-rules-cart-coupon.md), ya que se activan antes de que un producto se coloque en el carro de compras.

Por ejemplo, puede definir y establecer las condiciones de una regla de precio que, cuando se cumpla, muestre automáticamente los productos con un precio especial o promocional. Las propiedades de regla definidas pueden incluir grupos de clientes, categorías de productos, una cantidad o porcentaje de descuento, el color del producto, el tamaño del producto o casi cualquier atributo de producto configurado en la tienda. Puede definir fechas de inicio y finalización para una regla de precio que inicie y detenga automáticamente una promoción en las fechas definidas en la regla. Las propiedades de una regla guardada se pueden actualizar o modificar según sea necesario.

- ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) También puedes vincular una regla definida a un [bloque dinámico](../content-design/dynamic-blocks.md) para ayudar a promocionar el evento o el producto en tu tienda.

- ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Para las promociones recurrentes, puedes establecer manualmente una regla guardada en el estado _Activo_ o _Inactivo_ cada vez que quieras ejecutar la promoción.

## Reglas de precio de catálogo de acceso

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![Reglas de precios de catálogo](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. Actualizar las propiedades de una regla:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Haga clic en **[!UICONTROL Edit]** para mostrar la página _Información de la regla_.

   - ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Haga clic en la regla de la lista para mostrar la página Información de la regla.

   Aquí puede cambiar la configuración de la regla (similar a [crear una regla](price-rules-catalog-create.md)).

## Opciones de filtro

| Campo | Descripción |
|--- |--- |
| [!UICONTROL ID] | Introduzca texto para filtrar la lista por un número de ID de regla específico. |
| [!UICONTROL Rule] | Introduzca texto para filtrar la lista en función del nombre de regla definido cuando se creó la regla. |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Escriba texto en este campo para filtrar la lista en función de la prioridad definida para una regla. |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Utilice esta opción para filtrar la lista según los sitios web definidos para una regla. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Haga clic en **[!UICONTROL Edit]** para mostrar la información de la regla y actualizar la configuración de la regla (similar a la creación de una regla). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilice los campos de calendario dinámico (Para: y Desde:) para filtrar la lista en función de la fecha de inicio de la regla definida cuando se creó la regla. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilice los campos de calendario dinámico (Para: y Desde:) para filtrar la lista en función de la fecha de finalización de la regla definida cuando se creó la regla. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilice esta opción para filtrar la lista según el estado de la regla (`Active` o `Inactive`). |

{style="table-layout:auto"}

## Solución de problemas de recursos

Para obtener ayuda sobre la resolución de problemas con las reglas de precios de catálogo, consulte los siguientes artículos de la Base de conocimiento de asistencia de Commerce:

- [Error 404 en la tienda una vez que se actualizaron las programaciones de reglas de precios del catálogo](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/404-error-on-store-front-once-catalog-price-rule-schedules-update-is-performed.html)
- [Rendimiento mejorado de la página de productos con productos relacionados y reglas de destino](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31791-magento-patch-improvement-for-product-page-with-related-products-and-target-rules.html)
- [Las reglas de precios de catálogo no funcionan](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-24201-magento-patch-catalog-price-rules-don-t-work.html)
- [cálculos de precios de GraphQL](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33975-magento-patch-graphql-price-calculations.html)
