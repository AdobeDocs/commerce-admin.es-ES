---
title: Plantillas de direcciones de clientes
description: Descubra cómo puede personalizar las plantillas de direcciones de clientes.
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Plantillas de direcciones de clientes

{{ee-feature}}

Puede modificar la plantilla que controla el formato de las direcciones de facturación y envío del cliente que aparecen en las facturas impresas, envíos y devoluciones, así como en la libreta de direcciones de la cuenta del cliente. Si desea incluir información adicional, puede crear lo siguiente [atributos personalizados](attribute-properties.md) que están asociados a la cuenta del cliente y [dirección](address-attributes.md)e incorporarlos a la plantilla.

## Ejemplo 1: formato corto

Para [!UICONTROL Text One Line] plantilla de dirección:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## Ejemplo 2: formato largo

Para [!UICONTROL Text], [!UICONTROL HTML], y [!UICONTROL PDF] plantillas de dirección:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![Plantillas de direcciones de clientes](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## Cambiar el orden de los campos de dirección

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel lateral izquierdo, expanda **[!UICONTROL Customers]** y seleccione **[!UICONTROL Customer Configuration]**.

1. Haga clic en para expandir **[!UICONTROL Address Templates]** sección.

   La sección incluye un conjunto independiente de instrucciones de formato para cada una de las siguientes opciones:

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. Edite cada plantilla según sea necesario, utilizando los ejemplos como referencia.

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.
