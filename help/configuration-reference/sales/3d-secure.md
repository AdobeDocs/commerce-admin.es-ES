---
title: '[!UICONTROL Sales] > [!UICONTROL 3D Secure]'
description: Revise la configuración en la página [!UICONTROL Sales] > [!UICONTROL 3D Secure] del administrador de Commerce.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
TQID: https://experienceleague.adobe.com/WzxM9ZYbobbC1fWSIph0jv89uXLte6Wzjs5be27eMyU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 1%

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
