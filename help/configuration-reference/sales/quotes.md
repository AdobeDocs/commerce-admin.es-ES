---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Quotes]'
description: Revise la configuración en la página [!UICONTROL Sales] &gt; [!UICONTROL Quotes] del administrador de Commerce.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '188'
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
