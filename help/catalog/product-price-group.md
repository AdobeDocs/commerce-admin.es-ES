---
title: Precios de grupo
description: Aprenda a utilizar los precios de grupo para establecer precios de artículos con descuento en función de los grupos de clientes de su tienda.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
TQID: https://experienceleague.adobe.com/OCeX5pLtUzWdwOW5W8qpI4DCeab2PTAVi5xF8HUr91A
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 0%

---

# Precios de grupo

Puede usar los ajustes de configuración del producto en Administración para establecer los precios de los artículos con descuento en función de los grupos de clientes de su tienda. Este modelo de precios estratégicos se denomina _precios de grupo_.

El precio con descuento de cualquier producto se puede ofrecer a los miembros de un grupo de clientes específico cuando el comprador tiene sesión en su cuenta. El precio de grupo del cliente se muestra en la página del producto junto con el precio normal, de modo que un comprador pueda comparar precios fácilmente y actuar en consecuencia. Después de agregar el producto al carro de compras, el precio normal se reemplaza por el precio de grupo basado en el grupo de clientes.

Los precios para los grupos de clientes son un componente de [precios por niveles](product-price-tier.md) y se establecen de manera similar. La única diferencia es que los precios de grupo de clientes tienen una cantidad de 1.

![Descuento de grupo de clientes](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## Ventajas de utilizar los precios de grupo

- Adecuado para compradores mayoristas

- Incentivo para que los clientes actualicen su grupo de clientes para aprovechar los descuentos

- Campañas de marketing dirigidas

- Genere confianza y credibilidad recompensando a los clientes fieles

## Configurar un precio de grupo

1. Abra el producto en modo de edición.

1. Debajo del campo _[!UICONTROL Price]_, haga clic en **[!UICONTROL Advanced Pricing]**.

1. En la sección _[!UICONTROL Customer Group Price]_, haga clic en **[!UICONTROL Add]**.

   Si tu tienda incluye [Adobe Commerce B2B](../b2b/introduction.md) y tiene [catálogos compartidos](../b2b/catalog-shared.md) habilitados, esta sección tiene la etiqueta _[!UICONTROL Catalog and Tier Price]_.

   ![Precios avanzados](./assets/product-price-group.png){width="600" zoomable="yes"}

1. Configure el precio del grupo:

   - Para una instalación en varios sitios, elija **[!UICONTROL Website]** donde se aplica el precio del grupo.

   - Elija el(la) **[!UICONTROL Customer Group]** que recibirá el descuento.

   - Escriba **[!UICONTROL Quantity]** de `1`.

   - Para **[!UICONTROL Price]**, establezca el tipo de precio y la cantidad:

      - `Fixed` - Escriba el precio del producto con descuento.

      - `Discount` - Escriba el precio con descuento como porcentaje del precio del producto.

     ![Precios de grupo de clientes](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. Para agregar otro precio de grupo, haga clic en **[!UICONTROL Add]** y repita el paso anterior.

1. Una vez finalizado, haga clic en **[!UICONTROL Done]** y luego en **[!UICONTROL Save]**.

>[!NOTE]
>
>El precio del producto **_final_** se calcula como el precio relevante **_mínimo_**, utilizando la siguiente fórmula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Precio fijo_** Las opciones personalizables del producto están _no_ afectadas por las reglas de Precio de grupo, Precio de nivel, Precio especial o Precio de catálogo.
