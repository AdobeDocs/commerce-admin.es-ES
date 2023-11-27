---
title: Recordatorios de correo electrónico
description: Obtenga información acerca de los recordatorios de correo electrónico que se pueden enviar automáticamente a los clientes cuando se cumple un conjunto específico de condiciones.
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Recordatorios de correo electrónico

{{ee-feature}}

El propósito de un recordatorio por correo electrónico es animar a las personas que han visitado su tienda a aprovechar una promoción y hacer una compra. Los recordatorios de correo electrónico se pueden enviar automáticamente a los clientes cuando se cumple un conjunto específico de condiciones. Por ejemplo, puede enviar un recordatorio a los clientes que han agregado algo al carro o a la lista de deseos, pero que aún no han realizado una compra. Puede utilizar recordatorios de correo electrónico para animar a los clientes a volver a su tienda e incluir un [código de cupón](price-rules-cart-coupon.md) como incentivo. Los códigos de cupón se pueden generar automáticamente para cada lote de recordatorios de correo electrónico, para darle control sobre las ofertas asociadas con cada lote.

Los recordatorios de correo electrónico se pueden activar después de que haya transcurrido un número específico de días desde que se abandonó un carro de compras o para cualquier otra condición que desee definir. Las condiciones comunes incluyen el valor total del carro de compras, la cantidad, los artículos que contiene, etc.

>[!NOTE]
>
>Si un cliente tiene más de un carro de compras abandonado, una lista de deseos o una combinación de ambos coincidentes, el recordatorio de correo electrónico se activa solo una vez para ese cliente. Para almacenar en déclencheur el mismo recordatorio de correo electrónico de nuevo, utilice el _[!UICONTROL Repeat Schedule]_para establecer el número de días entre correos electrónicos.

![Recordatorios de correo electrónico](./assets/email-reminders.png){width="700" zoomable="yes"}

## Configurar recordatorios de correo electrónico

Las reglas de recordatorio de correo electrónico se pueden enviar a intervalos regulares por minuto, hora o día. La configuración determina cuántos correos electrónicos se envían en un lote y la identidad del almacén que aparece como remitente del mensaje.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Customers]** y elija **[!UICONTROL Promotions]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Automated Email Reminder Rules]** y haga lo siguiente:

   ![Configuración de clientes: reglas de recordatorio de correo electrónico automatizadas](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - Establecer **[!UICONTROL Enable Reminder Emails]** hasta `Yes`.

   - Para establecer la frecuencia con la que se ejecutan las comprobaciones de nuevos clientes que califican como recordatorios de correo electrónico automatizado, establezca **[!UICONTROL Frequency]** a uno de los siguientes:

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - Configure las variables apropiadas **[!UICONTROL Interval]**, basado en el _[!UICONTROL Frequency]_configuración.

   - Establecer **[!UICONTROL Start Time]** a la hora, los minutos y el segundo en que se envía el correo electrónico, en función de un reloj de 24 horas.

   - Para limitar el número de correos electrónicos que se pueden enviar en un lote, introduzca el número en la **[!UICONTROL Maximum Emails per One Run]** field.

   - Para evitar intentos repetidos de enviar correos electrónicos fallidos, introduzca el número máximo de intentos en la **[!UICONTROL Email Send Failure Threshold]** field.

   - Establecer **[!UICONTROL Reminder Email Sender]** a la [contacto de tienda](../getting-started/store-details.md#store-email-addresses) que aparece como el remitente del correo electrónico de recordatorio.

   Para ver una lista detallada de estas opciones, consulte [Reglas de recordatorio de correo electrónico automatizado](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) en el _Referencia de configuración_.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

## Plantillas de recordatorio de correo electrónico

La plantilla de recordatorio de correo electrónico predeterminada se puede personalizar y se pueden crear plantillas adicionales para diferentes promociones. Los recordatorios de correo electrónico tienen una selección de variables específicas que se pueden incorporar al mensaje. La información de estas variables viene determinada por la regla de recordatorio de correo electrónico que ha configurado y por la regla de precio de carro de compras asociada al cupón. El botón Insertar variable se puede utilizar para insertar la etiqueta de marcado con la variable en la plantilla. Para obtener más información, consulte [Correo electrónico](../systems/email-templates.md).

![Vista previa de recordatorio de correo electrónico](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### Personalizar una plantilla de recordatorio de correo electrónico

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Haga clic **[!UICONTROL Add New Template]**.

1. En el **[!UICONTROL Template]** lista debajo de `Magento_Reminder`, elija la **[!UICONTROL Promotion Notification/Reminder]** plantilla.

1. Haga clic **[!UICONTROL Load Template]**.

Siga el estándar [instrucciones](../systems/email-template-custom.md) para personalizar la plantilla.

### Variables de recordatorio de correo electrónico

#### Código de cupón

```
{{var coupon.getCode()|escape}}
```

#### Límite de uso de cupones

```
{{var coupon.usage_limit|escape}}
```

#### Uso de cupones por cliente

```
{{var coupon.usage_per_customer|escape}}
```

#### URL de cuenta de cliente

```
{{var this.getUrl($store,'customer/account/',[_nosid:1])}}
```

#### Nombre del cliente

```
{{var customer_data.name|escape}}
```

#### Plantilla de pie de correo electrónico

```
{{template config_path="design/email/footer_template"}}
```

#### Plantilla de encabezado de correo electrónico

```
{{template config_path="design/email/header_template"}}
```

#### Imagen de logotipo de correo electrónico Alt

```
{{var logo_alt}}
```

#### URL de imagen de logotipo de correo electrónico

```
{{var logo_url}}
```

#### Descripción de promoción

```
{{var promotion_description|escape|nl2br}}
```

#### Nombre de promoción

```
{{var promotion_name|escape}}
```

#### Nombre del almacén

```
{{var store.frontend_name}}
```

#### URL de tienda

```
{{store url=""}}
```
