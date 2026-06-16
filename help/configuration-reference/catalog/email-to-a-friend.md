---
title: '[!UICONTROL Catalog] > [!UICONTROL Email to a Friend]'
description: Revise la configuración en la página [!UICONTROL Catalog] > [!UICONTROL Email to a Friend] del administrador de Commerce.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
TQID: https://experienceleague.adobe.com/TzkDDALdwE5MMIEuZBpBL4DnOgngN93-YEf4biNwYMI
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![Plantillas de correo electrónico](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/communications/email-templates#configure-email-templates) -->

| Campo | [Ámbito](../../getting-started/websites-stores-views.md#scope-settings) | Descripción |
|--- |--- |--- |
| [!UICONTROL Enabled] | Vista de tienda | Activa el proceso que permite a los clientes enviar correos electrónicos a sus amigos sobre los productos de su tienda. Opciones: `Yes` / `No` |
| [!UICONTROL Select Email Template] | Vista de tienda | Identifica la plantilla de correo electrónico que se usa para los mensajes generados por la función _Enviar correo electrónico a un amigo_. Plantilla predeterminada: `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | Vista de tienda | Determina si el remitente debe ser un cliente registrado para enviar un correo electrónico sobre un producto a sus amigos. Opciones: `Yes` / `No` |
| [!UICONTROL Max Recipients] | Vista de tienda | Limita el número de personas que pueden estar en la lista de distribución para un solo correo electrónico. |
| [!UICONTROL Max Products Sent in 1  Hour] | Vista de tienda | Limita el número de productos que un solo usuario puede compartir durante un periodo de una hora. |
| [!UICONTROL Limit Sending By] | Vista de tienda | Determina el método utilizado para identificar al remitente. Las opciones incluyen: <br/>**`IP Address`**- (Recomendado) Identifica al remitente por la dirección IP del equipo que se utiliza para enviar los correos electrónicos del producto.<br/>**`Cookie (unsafe)`**: identifica al remitente mediante una cookie del explorador. Este método no es seguro porque el usuario puede eliminar la cookie para evitar la restricción. |

{style="table-layout:auto"}
