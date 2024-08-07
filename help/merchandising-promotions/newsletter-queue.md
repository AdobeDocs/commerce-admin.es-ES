---
title: Colas de newsletter
description: Obtenga información sobre cómo administrar las colas de la newsletter para enviar varios lotes de newsletter.
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Colas de newsletter

Para administrar la carga en el servidor, los boletines informativos con muchos suscriptores se envían en una cola de varios lotes. Puede comprobar la cola del boletín informativo periódicamente para comprobar el estado y ver cuántos se han procesado. Cualquier problema que ocurra durante la transmisión aparecerá en el informe _Problema de newsletter_.

## Enviar una newsletter

1. En el menú _Administrador_, vaya a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. En la cuadrícula, busque la [plantilla de newsletter](newsletter-template.md) que se va a enviar y establezca la columna **[!UICONTROL Action]** en `Queue Newsletter`.

1. Para **[!UICONTROL Queue Date Start]**, seleccione la fecha en la que la transmisión debe comenzar desde el calendario (![Icono del calendario](../assets/icon-calendar.png)).

1. Para **[!UICONTROL Subscribers From]**, seleccione cada vista de tienda que se va a incluir en la explosión de correo electrónico.

1. Rellene la información del encabezado del correo electrónico:

   - Escriba una breve descripción de la newsletter para la línea **[!UICONTROL Subject]** del encabezado del correo electrónico.

   - Escriba **[!UICONTROL Sender Name]**.

   - Para **[!UICONTROL Sender Email]**, escriba la dirección de correo electrónico del remitente.

     El nombre y la dirección de correo electrónico predeterminados del remitente se especifican en la configuración.

     ![Información de cola de newsletter](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. Si corresponde, escriba una nota en el cuadro **[!UICONTROL Message]** situado encima de las instrucciones para cancelar la suscripción.

   >[!NOTE]
   >
   >No elimine las instrucciones, que son requeridas por la ley en muchas jurisdicciones.

1. Para aplicar estilos personalizados a un boletín, agréguelos al campo **[!UICONTROL Newsletter Styles]**.

1. Una vez finalizado, haga clic en **[!UICONTROL Save and Resume]**.

   La newsletter aparece en la cola de espera para procesarse.

## Compruebe si hay problemas

En el menú _Administrador_, vaya a **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

## Barra de botones

| Botón | Descripción |
|--- |--- |
| **[!UICONTROL Back]** | Vuelve a la página Plantillas de newsletter sin guardar los cambios. |
| **[!UICONTROL Reset]** | Restablece cualquier cambio no guardado en el formulario de información de cola a sus valores anteriores. |
| **[!UICONTROL Preview Template]** | Abre una página de vista previa en una pestaña independiente. |
| **[!UICONTROL Save and Resume]** | Guarda todos los cambios realizados. Pone la newsletter en cola. |
| **[!UICONTROL Save Newsletter]** | Guarda todos los cambios realizados. Pone la newsletter en cola. |

{style="table-layout:auto"}

## Columnas

| Columna | Descripción |
|--- |--- |
| [!UICONTROL ID] | Identificador numérico único asignado a cada plantilla de boletín informativo. |
| [!UICONTROL Queue Start] | La fecha en la que se envió la newsletter. |
| [!UICONTROL Queue End] | La fecha en la que terminó de enviarse el boletín informativo. |
| [!UICONTROL Subject] | Asunto de la plantilla de la newsletter. |
| [!UICONTROL Status] | Indica el estado del correo del boletín informativo. Valores posibles: `Sent`, `Canceled`, `Not Sent`, `Sending` o `Paused`. |
| [!UICONTROL Processed] | Indica cuántos boletines se han enviado. |
| [!UICONTROL Recipients] | Indica cuántos boletines recibieron los suscriptores. |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**: abre una ventana independiente para obtener una vista previa de la plantilla. |

{style="table-layout:auto"}
