---
title: Reglas de precios de catálogo
description: Obtenga información sobre las reglas de precios de catálogo que se pueden usar para ofrecer productos a los compradores a un precio con descuento según un conjunto de condiciones definidas.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
TQID: https://experienceleague.adobe.com/JZE2DF0tp-XOsKjxo-WaQiwA3Y-FrM4TI5qq-Nze-qo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 468
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
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Use los campos de calendario dinámico (Para: y Desde:) para filtrar la lista en función de la fecha de inicio de la regla definida cuando se creó la regla. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Use los campos de calendario dinámico (Para: y Desde:) para filtrar la lista en función de la fecha de finalización de la regla tal como se definió cuando se creó la regla. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilice esta opción para filtrar la lista según el estado de la regla (`Active` o `Inactive`). |

{style="table-layout:auto"}
