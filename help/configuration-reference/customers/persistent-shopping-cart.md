---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: Revise la configuración en la página [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] del administrador de Commerce.
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>Un [carro de compras persistente](../../stores-purchase/cart-persistent.md) permite retener artículos sin comprar que quedan en el carro y los guarda durante un período configurado en _Duración de la persistencia_. Las cookies deben permitirse en el explorador del cliente para utilizar el carro de compras persistente.

## [!UICONTROL General Options]

![Opciones generales](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Sitio web | Determina si la persistencia está habilitada. |
| [!UICONTROL Persistence Lifetime (seconds)] | Sitio web | Define la duración de la cookie persistente en segundos. El valor máximo permitido es de 3153600000 segundos (100 años). |
| [!UICONTROL Enable "Remember Me"] | Sitio web | Define si la casilla de verificación _Recordarme_ aparece en las páginas de inicio de sesión y registro de la tienda. Opciones: <br/>**`Yes`**- Muestra la casilla de verificación _Recordarme_.<br/>**`No`**: no muestra la casilla de verificación _Recordarme_ y la cookie persistente solo se usa para los clientes que ya la tienen. |
| [!UICONTROL "Remember Me" Default Value] | Sitio web | Define el estado predeterminado de la casilla de verificación _Recordarme_. |
| [!UICONTROL Clear Persistence on Log Out] | Sitio web | Define si la cookie persistente se elimina cuando un cliente de tienda cierra la sesión. Independientemente de cómo se configure, si un cliente no cierra la sesión, pero la cookie de sesión caduca, se seguirá utilizando la cookie persistente. |
| [!UICONTROL Persist Shopping Cart] | Sitio web | Define si el uso de la cookie persistente da acceso a los datos del carro de compras de la cuenta correspondiente. Opciones: <br/>**`Yes`**: el contenido del carro de compras se guarda después de que finalice la sesión.<br/>**`No`**: el contenido del carro de compras no se guarda después de que finalice la sesión. |
| [!UICONTROL Persist Wish List] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Determina si se conserva el estado de las listas de deseos del cliente cuando finaliza la sesión. Opciones: <br/>**`Yes`**: el contenido de la lista de deseos se guarda al finalizar la sesión.<br/>**`No`** - La lista de deseos no se guarda cuando finaliza la sesión. |
| [!UICONTROL Persist Recently Ordered Items] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Determina si el estado de los elementos pedidos recientemente se conserva al finalizar la sesión. Opciones: <br/>**`Yes`**- El estado de los elementos pedidos recientemente se guarda al finalizar la sesión.<br/>**`No`** - El estado de los elementos pedidos recientemente no se guarda cuando finaliza la sesión. |
| [!UICONTROL Persist Currently Compared Products] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Determina si el estado de los productos comparados actualmente se conserva al finalizar la sesión. Opciones: <br/>**`Yes`**: el estado de los productos comparados actualmente se guarda al finalizar la sesión.<br/>**`No`**: el estado de los productos comparados actualmente no se guarda cuando finaliza la sesión. |
| [!UICONTROL Persist Comparison History] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Determina si se conserva el estado del historial de comparación cuando finaliza la sesión. Opciones: <br/>**`Yes`**- El estado del historial de comparación se guarda cuando finaliza la sesión.<br/>**`No`**: el estado del historial de comparación no se guarda cuando finaliza la sesión. |
| [!UICONTROL Persist Recently Viewed Products] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Determina si el estado de los productos vistos recientemente se conserva al finalizar la sesión. Opciones: <br/>**`Yes`**: el estado de los productos vistos recientemente se guarda al finalizar la sesión.<br/>**`No`**: el estado de los productos vistos recientemente no se guarda cuando finaliza la sesión. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Sitio web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) Determina si se conserva el estado de los criterios de segmentación y pertenencia a grupos de clientes cuando finaliza la sesión. Opciones: <br/>**`Yes`**: el estado de los datos de segmentación y pertenencia a grupos del cliente se guarda al finalizar la sesión.<br/>**`No`**: el estado de los datos de segmentación y pertenencia a grupos del cliente no se guarda al finalizar la sesión. |

{style="table-layout:auto"}
