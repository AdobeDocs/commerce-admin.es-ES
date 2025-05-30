---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: Revise la configuración en la página [!UICONTROL Customers] &gt; [!UICONTROL Promotions] del administrador de Commerce.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Reglas automatizadas de recordatorio por correo electrónico](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://experienceleague.adobe.com/es/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules#configure-email-reminders) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | Global | Activa los recordatorios de correo electrónico automatizados. Si se establece en No, se omiten los ajustes restantes. Opciones: `Yes` / `No` |
| [!UICONTROL Frequency] | Global | Indica la frecuencia con la que Commerce debe comprobar si hay nuevos clientes que cumplan los requisitos para los recordatorios de correo electrónico automatizados. Opciones: <br/>**`Minute Intervals`**- Envía el correo electrónico según el intervalo seleccionado. (5 minutos, 10 minutos, 15 minutos, 20 minutos o 30 minutos)<br/>**`Hourly`**: envía un mensaje de correo electrónico cada hora, en el minuto posterior a la hora especificada. Escriba un valor entre 0 y 59. <br/>**`Daily`**: envía un correo electrónico diariamente, desde la hora de inicio. |
| [!UICONTROL Interval] | Global | El intervalo debe ser igual o mayor que el periodo de lanzamiento de cron.php. Opciones: `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | Global | Establece el día, el minuto y el segundo en que se envía el correo electrónico. Especificado en formato de 24 horas, en función de la hora del sistema en el servidor. |
| [!UICONTROL Maximum Emails per One Run] | Global | Limita el número de correos electrónicos enviados en un bloque programado. |
| [!UICONTROL Email Send Failure Threshold] | Global | El número de veces que el recordatorio intenta enviar notificaciones a una dirección de correo electrónico específica y falla. Cuando el valor se establece en 0, no hay umbral y las notificaciones se siguen enviando a pesar de los errores. |
| [!UICONTROL Reminder Email Sender] | Vista de tienda | La identidad del almacén que aparece como el remitente del correo electrónico. |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![Códigos de cupón específicos generados automáticamente](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://experienceleague.adobe.com/es/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart-coupon#configure-coupon-codes)  -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Define la longitud del código de cupón, excluyendo el prefijo, el sufijo y los separadores. |
| [!UICONTROL Code Format] | Global | Define el formato del código de cupón. Las opciones incluyen: <br/>**`Alphanumeric`**- Cualquier combinación de letras y números.<br/>**`Alphabetical`** - Solo cartas. <br/>**`Numeric`**- Solo números. |
| [!UICONTROL Code Prefix] | Global | Un valor que se anexa al principio de todos los códigos de cupones. Si no desea utilizar un prefijo, deje el campo en blanco. |
| [!UICONTROL Code Suffix] | Global | Un valor que se anexa al final de todos los códigos. Si no desea utilizar un sufijo, deje el campo en blanco. |
| [!UICONTROL Dash Every X Characters] | Global | Intervalo para insertar un guión (-) en todos los códigos de cupones. Si no desea utilizar un guión, deje el campo en blanco. <br/>_&#x200B;**Nota:**&#x200B;_ Los códigos de cupón que difieren solo en un guión se consideran códigos diferentes. |

{style="table-layout:auto"}
