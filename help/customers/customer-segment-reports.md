---
title: Informe Segmento de cliente
description: El informe Segmento de cliente proporciona información sobre la cantidad de clientes en cada segmento.
exl-id: a767ee80-7b6e-4acd-9772-2f8adcf3233e
TQID: https://experienceleague.adobe.com/asBYmrf5lkWyfH6xf8o-OxZwK25rr4okrtsyON3Fv1s
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
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
source-wordcount: 247
ht-degree: 0%

---

# Informe Segmento de cliente

{{ee-feature}}

El informe Segmento de cliente proporciona información sobre la cantidad de clientes que hay en cada segmento.

![Informe de segmento de cliente](assets/customer-segments-reports.png){width="700" zoomable="yes"}

| Columna | Descripción |
|--- |--- |
| **[!UICONTROL Select]** | Seleccione la casilla de verificación para cada segmento que vaya a estar sujeto a una acción o utilice el control de selección en el encabezado de la columna. Opciones: `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| **[!UICONTROL ID]** | Un identificador numérico único asignado a cada segmento |
| **[!UICONTROL Segment]** | Nombre del segmento |
| **[!UICONTROL Status]** | Estado del segmento. Opciones: `Active` / `Inactive` |
| **[!UICONTROL Website]** | Sitio web al que se asigna el segmento |
| **[!UICONTROL Customers]** | Número de clientes asignados a un segmento |

{style="table-layout:auto"}

Puede explorar en profundidad una lista de clientes del segmento y exportar los datos.

![Profundizar en los datos del cliente](assets/customer-segment-drilldown.png){width="600" zoomable="yes"}

Para asegurarse de que tiene los datos más recientes, se deben actualizar los datos del segmento. Si los datos del segmento no están disponibles o no están actualizados, haga clic en **[!UICONTROL Refresh Segment Data]** en la barra de botones para actualizar.

1. Para **[!UICONTROL Export to]**, elija un formato de exportación:

   * CSV: archivo de valores separados por comas que contiene datos de texto sin formato.
   * XML de Excel: formato de datos de hoja de cálculo basado en XML.

1. Haga clic en **[!UICONTROL Export]**.

   | Columna | Descripción |
   |--- |--- |
   | **[!UICONTROL ID]** | Identificador numérico único asignado a cada usuario |
   | **[!UICONTROL Name]** | Nombre del cliente |
   | **[!UICONTROL Email]** | La dirección de correo electrónico de un cliente registrado |
   | **[!UICONTROL Group]** | El grupo de clientes al que está asignado el cliente |
   | **[!UICONTROL Phone]** | El número de teléfono del cliente |
   | **[!UICONTROL ZIP]** | El código postal donde se encuentra el cliente |
   | **[!UICONTROL Country]** | El país donde se encuentra el cliente |
   | **[!UICONTROL State/Province]** | Estado o provincia donde se encuentra el cliente |
   | **[!UICONTROL Customer Since]** | La fecha y hora de creación de la cuenta del cliente |

   {style="table-layout:auto"}

1. El archivo generado se guarda automáticamente en el equipo local.
