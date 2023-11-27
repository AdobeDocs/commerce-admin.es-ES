---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: Revise la configuración de en [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] de la administración de Commerce.
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>A [Carro de compras persistente](../../stores-purchase/cart-persistent.md) permite la retención de artículos no comprados que quedan en el carro de compras y los guarda durante un periodo configurado en _Duración de persistencia_. Las cookies deben permitirse en el explorador del cliente para utilizar el carro de compras persistente.

## [!UICONTROL General Options]

![Opciones generales](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Sitio web | Determina si la persistencia está habilitada. |
| [!UICONTROL Persistence Lifetime (seconds)] | Sitio web | Define la duración de la cookie persistente en segundos. El valor máximo permitido es de 3153600000 segundos (100 años). |
| [!UICONTROL Enable "Remember Me"] | Sitio web | Define si la variable _Recordar mis datos_ La casilla de verificación de aparece en las páginas de inicio de sesión y registro de la tienda. Opciones: <br/>**`Yes`**- Muestra el _Recordar mis datos_ casilla de verificación<br/>**`No`** - No muestra el _Recordar mis datos_ y la cookie persistente solo se utiliza para los clientes que ya la tienen. |
| [!UICONTROL "Remember Me" Default Value] | Sitio web | Define el estado predeterminado para _Recordar mis datos_ casilla de verificación |
| [!UICONTROL Clear Persistence on Log Out] | Sitio web | Define si la cookie persistente se elimina cuando un cliente de tienda cierra la sesión. Independientemente de cómo se configure, si un cliente no cierra la sesión, pero la cookie de sesión caduca, se seguirá utilizando la cookie persistente. |
| [!UICONTROL Persist Shopping Cart] | Sitio web | Define si el uso de la cookie persistente da acceso a los datos del carro de compras de la cuenta correspondiente. Opciones: <br/>**`Yes`**: el contenido del carro de compras se guarda después de que finalice la sesión.<br/>**`No`** : el contenido del carro de compras no se guarda después de que finalice la sesión. |
| [!UICONTROL Persist Wish List] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Determina si el estado de las listas de deseos del cliente se conserva cuando finaliza la sesión. Opciones: <br/>**`Yes`**- El contenido de la lista de deseos se guarda al finalizar la sesión.<br/>**`No`** - La lista de deseos no se guarda al finalizar la sesión. |
| [!UICONTROL Persist Recently Ordered Items] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Determina si el estado de los elementos pedidos recientemente se conserva cuando finaliza la sesión. Opciones: <br/>**`Yes`**- El estado de los artículos pedidos recientemente se guarda al finalizar la sesión.<br/>**`No`** - El estado de los artículos pedidos recientemente no se guarda al finalizar la sesión. |
| [!UICONTROL Persist Currently Compared Products] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Determina si el estado de los productos comparados actualmente se conserva cuando finaliza la sesión. Opciones: <br/>**`Yes`**: el estado de los productos comparados actualmente se guarda cuando finaliza la sesión.<br/>**`No`** : el estado de los productos comparados actualmente no se guarda cuando finaliza la sesión. |
| [!UICONTROL Persist Comparison History] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Determina si se conserva el estado del historial de comparación cuando finaliza la sesión. Opciones: <br/>**`Yes`**- El estado del historial de comparación se guarda cuando finaliza la sesión.<br/>**`No`** - El estado del historial de comparación no se guarda cuando finaliza la sesión. |
| [!UICONTROL Persist Recently Viewed Products] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Determina si el estado de los productos visualizados recientemente se conserva cuando finaliza la sesión. Opciones: <br/>**`Yes`**: el estado de los productos vistos recientemente se guarda cuando finaliza la sesión.<br/>**`No`** : el estado de los productos vistos recientemente no se guarda cuando finaliza la sesión. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Determina si se conserva el estado de los criterios de segmentación y pertenencia a grupos de los clientes cuando finaliza la sesión. Opciones: <br/>**`Yes`**: el estado de los datos de segmentación y pertenencia a grupos del cliente se guarda cuando finaliza la sesión.<br/>**`No`** : el estado de los datos de segmentación y pertenencia a grupos del cliente no se guarda al finalizar la sesión. |

{:style=&quot;table-layout:auto&quot;}
