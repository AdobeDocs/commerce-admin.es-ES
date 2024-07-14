---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Revise la configuración en la página [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] del administrador de Commerce.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] fue desarrollado por [!DNL Visa] para promover transacciones en línea seguras. [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey] y [!DNL CardinalCommerce Consumer Authentication] verifican ejemplos de soluciones [!DNL 3-D Secure] creadas por redes de tarjetas. [!DNL CardinalCommerce] es un líder global en autenticación de transacciones digitales y una subsidiaria de [!DNL Visa] que pertenece en su totalidad.

[!DNL 3-D Secure] versión 2.0 admite numerosas mejoras, incluidos métodos de autenticación avanzados y flujo de autenticación, así como un uso compartido de datos mejorado entre comerciante y emisor.

>[!NOTE]
>
>La puerta de enlace de pago [Braintree](../../stores-purchase/braintree.md) también admite la verificación [!DNL 3-D Secure].

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Environment] | Sitio web | Indica el modo de funcionamiento de su cuenta de [!DNL CardinalCommerce]. Si está ejecutando en un entorno de prueba, elija &quot;Zona protegida&quot;. Opciones: Zona protegida/Producción (predeterminada) |
| [!UICONTROL Org Unit ID] | Sitio web | Identificador de unidad de organización de su cuenta de comerciante [!DNL CardinalCommerce]. |
| [!UICONTROL API Key] | Sitio web | La clave API de su cuenta de comerciante [!DNL CardinalCommerce]. |
| [!UICONTROL API Identifier] | Sitio web | El identificador de API de su cuenta de comerciante [!DNL CardinalCommerce]. |
| [!UICONTROL Debug] | Sitio web | Opciones: `Yes` / `No` |

{style="table-layout:auto"}
