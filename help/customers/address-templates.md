---
title: Plantillas de direcciones de clientes
description: Descubra cómo puede personalizar las plantillas de direcciones de clientes.
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/b8tCsMqk6IQJjs5YWCH4-CNmBPrz-3pdPG7ttH4eawk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 0%

---

# Plantillas de direcciones de clientes

{{ee-feature}}

Puede modificar la plantilla que controla el formato de las direcciones de facturación y envío del cliente que aparecen en las facturas impresas, envíos y devoluciones, así como en la libreta de direcciones de la cuenta del cliente. Si desea incluir información adicional, puede crear [atributos personalizados](attribute-properties.md) asociados con la cuenta del cliente y la [dirección](address-attributes.md), e incorporarlos a la plantilla.

## Ejemplo 1: formato corto

Para la plantilla de dirección [!UICONTROL Text One Line]:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## Ejemplo 2: formato largo

Para las plantillas de direcciones [!UICONTROL Text], [!UICONTROL HTML] y [!UICONTROL PDF]:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![Plantillas de direcciones de clientes](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## Cambiar el orden de los campos de dirección

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel lateral izquierdo, expanda **[!UICONTROL Customers]** y seleccione **[!UICONTROL Customer Configuration]**.

1. Haga clic para expandir la sección **[!UICONTROL Address Templates]**.

   La sección incluye un conjunto independiente de instrucciones de formato para cada una de las siguientes opciones:

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. Edite cada plantilla según sea necesario, utilizando los ejemplos como referencia.

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
