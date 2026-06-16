---
title: '[!UICONTROL Sales] > [!UICONTROL Quotes]'
description: Revise la configuración en la página [!UICONTROL Sales] > [!UICONTROL Quotes] del administrador de Commerce.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
TQID: https://experienceleague.adobe.com/puZjB2YCCyZXT0U6AdDBd-YjxopU637-yxgOaB6hkvM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Con la instalación y activación de Adobe Commerce B2B, la experiencia de compra se puede personalizar con funciones específicas de la empresa. Adobe Commerce B2B es una solución integrada que admite modelos B2B y B2C. Para obtener más información sobre las características de B2B, consulte la [Guía del usuario de Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=es).

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/es/docs/commerce-admin/b2b/quotes/quotes) -->

## [!UICONTROL General]

![General](./assets/quotes-general.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Sitio web | El importe mínimo del subtotal del carro de compras, después de cualquier descuento, que se requiere antes de que un cliente pueda enviar una solicitud de presupuesto. Valor predeterminado: `0` |
| [!UICONTROL Minimum Amount Message] | Vista de tienda | Mensaje que aparece en el carro de compras cuando un cliente intenta enviar una solicitud de presupuesto, pero no se cumple la cantidad mínima requerida. |
| [!UICONTROL Default Expiration Period] | Sitio web | Determina la vida útil predeterminada de [quote](../../b2b/quote-price-negotiation.md) como período de tiempo desde la fecha en que se envió la solicitud de presupuesto. Opciones: `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![Archivos adjuntos](./assets/quotes-attached-files.png)<!-- zoom -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | Global | Determina los formatos de archivo que se pueden adjuntar a una cita. Valores predeterminados admitidos: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` y `jpeg` |
| [!UICONTROL Maximum file size] | Global | Determina el tamaño máximo de un archivo adjunto a un presupuesto. Esta configuración se puede anular mediante la configuración del servidor. |

{style="table-layout:auto"}
