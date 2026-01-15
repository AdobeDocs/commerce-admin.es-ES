---
title: Precios de nivel
description: Aprenda a utilizar los precios de nivel para ofrecer un descuento por cantidad desde una lista de productos o una página de productos.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# Precios de nivel

El nivel de precios le permite ofrecer un descuento por cantidad desde una lista de productos o una página de productos en la tienda. El descuento se puede aplicar a una vista de tienda, a un grupo de clientes o a un catálogo compartido específicos.

Si tiene muchos productos que actualizar, es más eficiente importar los cambios de precio de nivel, en lugar de introducirlos individualmente. Para obtener más información, consulte [Importar precios de nivel](../systems/data-import-price-tier.md).

![Precio de nivel en una página de productos de tienda](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

La página de productos calcula el descuento por cantidad y muestra un mensaje como el siguiente:

`Buy 6 for $5.95 each and save 15%`

Los precios de la tienda tienen prioridad de la cantidad más alta a la más baja. Si tiene un precio de nivel para la cantidad `5` y uno para `10`, y un cliente agrega cinco, seis, siete, ocho o nueve artículos al carro de compras, el cliente recibe el precio con descuento para el nivel de cantidad `5`. Cuando el cliente agrega el décimo artículo, el precio con descuento especificado para el nivel de cantidad `10` reemplaza al nivel de una cantidad de `5`, y se aplica el precio con descuento para `10`.

## Agregar un nivel de precios para un producto

1. Abra el producto en modo de edición.

1. Debajo del campo _[!UICONTROL Price]_, haga clic en **[!UICONTROL Advanced Pricing]**.

1. En la sección _[!UICONTROL Tier Price]_, haga clic en **[!UICONTROL Add]**.

   Si está creando un nivel de varios precios, haga clic en **[!UICONTROL Add]** para cada nivel adicional, de modo que pueda trabajar en todos los niveles al mismo tiempo. Cada nivel del grupo tiene el mismo sitio web y grupo de clientes o asignación de catálogo compartido, pero una cantidad y un precio diferentes.

## Configuración del nivel de precios

1. Si su tienda tiene varios sitios web, elija el **[!UICONTROL Website]** al que se aplican los precios de nivel.

1. Si es necesario, limite la disponibilidad del nivel de precios seleccionando **[!UICONTROL Customer Group]** o **[!UICONTROL Shared Catalog]** (![Adobe Commerce B2B](../assets/b2b.svg) Disponible solo con [Adobe Commerce B2B](./b2b/../introduction.md)).

1. Para **[!UICONTROL Qty]**, escriba la cantidad que debe pedirse para recibir el descuento.

   - **Método 1:** Escriba el precio como importe fijo

     Establezca **[!UICONTROL Price]** en `Fixed` e introduzca el precio ajustado de una unidad en ese nivel.

     ![Precio de nivel como importe fijo](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Método 2:** Escriba el precio como porcentaje

     Establezca **[!UICONTROL Price]** en `Discount` e introduzca el precio con descuento como porcentaje del precio base del producto.

     Por ejemplo, para obtener un descuento del 15 por ciento, escriba el número `15`. (El precio se guarda con dos posiciones decimales, como `15.00`.)

     >[!NOTE]
     >
     >Para obtener el precio con descuento, el porcentaje definido se calcula respecto al valor definido en el campo _[!UICONTROL Price]_, no en el campo&#x200B;_[!UICONTROL Special Price]_.

     ![Precio de nivel como porcentaje](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Completar la configuración de precios

1. Para agregar otro conjunto de precios de nivel para un sitio web o grupo de clientes diferente, repita los pasos anteriores.

1. Una vez finalizado, haga clic en **[!UICONTROL Done]** y luego en **[!UICONTROL Save]**.

>[!NOTE]
>
>El precio del producto **_final_** se calcula como el precio relevante **_mínimo_**, utilizando la siguiente fórmula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Precio fijo_** Las opciones personalizables del producto están _no_ afectadas por las reglas de Precio de grupo, Precio de nivel, Precio especial o Precio de catálogo.

## Activar asignación de precios de nivel para reglas de precios de catálogo

[!BADGE Solo SaaS]{type=Positive url="https://experienceleague.adobe.com/es/docs/commerce/user-guides/product-solutions" tooltip="Solo se aplica a proyectos de Adobe Commerce as a Cloud Service (infraestructura de SaaS administrada por Adobe)."}

[!BADGE espacio aislado]{type=Caution tooltip="Actualmente, los elementos enumerados solo están disponibles en entornos de espacio aislado. Adobe hace que las nuevas versiones estén disponibles primero en entornos de espacio aislado para que pueda probar los próximos cambios antes de que el lanzamiento esté disponible en entornos de producción."}

En versiones anteriores de Commerce, no se podían utilizar precios de nivel junto con reglas de precios de catálogo. Las reglas de catálogo omiten la configuración de precios de nivel y calculan los descuentos sólo desde el precio base original. Con Adobe Commerce as a Cloud Service, ahora puede optar por incluir los precios de nivel en el cálculo de las reglas de precios de catálogo.

Para habilitar esta funcionalidad:

1. Vaya a **[!UICONTROL Stores]** > *[!UICONTROL Settings]* > **[!UICONTROL Configuration]** > **[!UICONTROL Sales]** > **[!UICONTROL Sales]** > **[!UICONTROL Promotions]** y establezca el campo **[!UICONTROL Apply Catalog Price Rule on Grouped Price]** en **[!UICONTROL Yes]**.

   ![Habilitar precios de nivel para reglas de precios de catálogo](../configuration-reference/sales/assets/sales-promotions-settings.png){width="700" zoomable="yes"}

1. Defina un precio de nivel con una cantidad de `1` para cada grupo de clientes o catálogo compartido específico (como `Wholesale`, `Retail` o grupo definido por el comerciante) al que desee destinar con reglas de precios de catálogo. El grupo de clientes `ALL GROUPS` y el catálogo compartido `Default` no se pueden usar para este propósito. El precio de nivel no está habilitado para ningún grupo que no tenga un precio de nivel definido con una cantidad de `1`.

1. Defina los precios de nivel adicionales con cantidades superiores a `1` según sea necesario. Estos precios de nivel adicional se aplicarán de la forma habitual cuando el cliente añada cantidades adicionales del producto al carro de compras. Las reglas de precios de catálogo no se aplicarán a estos precios de nivel adicionales.

Para ilustrar el funcionamiento de la asignación de precios de nivel con las reglas de precios de catálogo al comprar un único producto, observe el siguiente ejemplo:

- El precio base estándar de un producto es de 100 USD.
- Se ha definido un precio de nivel para el grupo de clientes `Wholesale` con una cantidad de `1` y un precio fijo de 90 USD.
- Una regla de precio de catálogo proporciona un descuento del 10% para el grupo de clientes `Wholesale`.

Cuando se activa la asignación de precios de nivel para las reglas de precios de catálogo, el sistema utiliza el siguiente flujo para calcular el precio final:

1. Antes de que el cliente inicie sesión, el precio del producto se muestra como 100 USD (el precio base estándar).

1. Una vez que el cliente inicia sesión como miembro del grupo `Wholesale`, el precio del producto se ajusta a 90 USD (el precio de nivel para el grupo `Wholesale`).

1. Se aplica la regla de precio de catálogo, que proporciona un descuento del 10% sobre el precio de nivel de 90 USD, lo que da como resultado un precio final de 81 USD.

La siguiente tabla resume los cálculos de precios cuando se activa la asignación de precios de nivel para las reglas de precios de catálogo y una regla de precios de catálogo proporciona un descuento del 10% para todos los grupos de clientes:

Producto: Precio estándar $100 (compra de un solo artículo)

| Grupo de clientes | Precio de nivel (cantidad=1) | Nuevo precio base | Precio final |
|---|---|---|---|
| TODOS LOS GRUPOS | No configurado | 100 $ | 100 $ - 10 % = 90 $ |
| Venta al por mayor | Fijo: 85 $ | 85 $ | 85 $ - 10 % = 76,50 $ |
| Retailer | 20% de descuento | 80 $ | 80 $ - 10 % = 72,00 $ |
| VIP | 15% de descuento | 85 $ | 85 $ - 10 % = 76,50 $ |
