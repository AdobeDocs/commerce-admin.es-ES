---
title: Referencia de configuración del carro de compras persistente
description: Contenido reutilizable para la referencia de configuración del carro de compras persistente.
source-git-commit: d23cb0d63409e533cf950d8d14514d9f9157fd05
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# [!UICONTROL General Options]

![Opciones generales](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Campo | [Ámbito](/help/getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | Sitio web | Determina si la característica de persistencia está habilitada. |
| [!UICONTROL Persistence Lifetime (seconds)] | Sitio web | Define la duración de la cookie persistente en segundos. El valor máximo permitido es de 34560000 segundos (400 días). Esta es una limitación de la duración máxima recomendada de la cookie. |
| [!UICONTROL Enable "Remember Me"] | Sitio web | Define si la casilla de verificación _Recordarme_ se muestra en las páginas de inicio de sesión y registro de la tienda. Opciones: <br/>**`Yes`**- Muestra la casilla de verificación _Recordarme_.<br/>**`No`**: no muestra la casilla de verificación _Recordarme_ y la cookie persistente solo se usa para los clientes que ya la tienen. |
| [!UICONTROL "Remember Me" Default Value] | Sitio web | Define el estado predeterminado de la casilla de verificación _Recordarme_. |
| [!UICONTROL Clear Persistence on Log Out] | Sitio web | Define si la cookie persistente se elimina cuando un cliente de tienda cierra la sesión. Independientemente de cómo se configure esta opción, si un cliente no cierra la sesión, pero la cookie de sesión caduca, se seguirá utilizando la cookie persistente. |
| [!UICONTROL Persist Shopping Cart] | Sitio web | Define si el uso de la cookie persistente da acceso a los datos del carro de compras de la cuenta correspondiente. Opciones: <br/>**`Yes`**o **`No`**. |
| [!UICONTROL Persist Wish List] | Sitio web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) Determina si se conserva el estado de las listas de deseos del cliente cuando finaliza la sesión. Opciones: <br/>**`Yes`**: el contenido de la lista de deseos se guarda al finalizar la sesión.<br/>**`No`** - La lista de deseos no se guarda cuando finaliza la sesión. |
| [!UICONTROL Persist Recently Ordered Items] | Sitio web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) Determina si el estado de los elementos pedidos recientemente se guarda al finalizar la sesión. Opciones: <br/>**`Yes`**o **`No`**. |
| [!UICONTROL Persist Currently Compared Products] | Sitio web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) Determina si se conserva el estado de los productos comparados actualmente cuando finaliza la sesión. Opciones: <br/>**`Yes`**o **`No`**. |
| [!UICONTROL Persist Comparison History] | Sitio web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) Determina si se conserva el estado del historial de comparación cuando finaliza la sesión. Opciones: <br/>**`Yes`**o **`No`**. |
| [!UICONTROL Persist Recently Viewed Products] | Sitio web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) Determina si se conserva el estado de los productos vistos recientemente cuando finaliza la sesión. Opciones: <br/>**`Yes`**o **`No`**. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Sitio web | ![Adobe Commerce](/help/assets/adobe-logo.svg) (solo Adobe Commerce) Determina si se conserva el estado de los criterios de segmentación y pertenencia a grupos de clientes cuando finaliza la sesión. Opciones: <br/>**`Yes`**: el estado de los datos de segmentación y pertenencia a grupos del cliente se guarda al finalizar la sesión.<br/>**`No`**: el estado de los datos de segmentación y pertenencia a grupos del cliente no se guarda al finalizar la sesión. |

{style="table-layout:auto"}
