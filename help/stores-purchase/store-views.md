---
title: Vistas de tienda
description: Obtenga información sobre cómo agregar y editar una vista de tienda.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
TQID: https://experienceleague.adobe.com/2VMBTnzG3lqsNEyx-e46rqDs1wHofaDeHL3j3SuqxOE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 284
ht-degree: 0%

---

# Vistas de tienda

Las vistas de tienda se suelen utilizar para que la tienda esté disponible en diferentes configuraciones regionales. Los compradores pueden utilizar el selector de idioma en el encabezado de la tienda para cambiar la vista de la tienda.

![Ámbito: vistas de varias tiendas](./assets/scope-multiview.svg){width="550"}

## Agregar una vista de tienda

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![Todas las tiendas](./assets/stores-all.png){width="700" zoomable="yes"}

1. Haga clic en **[!UICONTROL Create Store View]**.

   ![Crear vista de tienda](./assets/create-store-view.png){width="600" zoomable="yes"}

1. Establezca **[!UICONTROL Store]** en el almacén principal de esta vista.

1. Escriba un **[!UICONTROL Name]** para esta vista de tienda.

   El nombre aparece en el selector de idioma del encabezado de la tienda. Por ejemplo: `Spanish`.

1. Para **[!UICONTROL Code]**, escriba el código que identifica la vista (en caracteres en minúsculas).

   Por ejemplo: `spanish`.

1. Para activar la vista, establezca **[!UICONTROL Status]** en `Enabled`.

1. (Opcional) Escriba un número **[!UICONTROL Sort Order]** para determinar la secuencia en la que esta vista se muestra con otras vistas.

1. Haga clic en **[!UICONTROL Save Store View]**.

## Editar una vista de tienda

Dado que el nombre de la vista aparece en el selector de idioma, puede que desee cambiar el nombre de la vista predeterminada por otro más descriptivo. El campo _Name_ es simplemente una etiqueta y se puede cambiar fácilmente.

Si la instalación de Adobe Commerce o Magento Open Source tiene una instalación de varios sitios o de varias tiendas, no cambie el campo Código de almacén sin comprobar que no se hace referencia al valor en el archivo `index.php`. Si no tiene acceso al servidor para examinar el archivo, pida ayuda a un desarrollador.

| Campo | Valor original | Valor actualizado |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. En la columna _[!UICONTROL Store View]_de la cuadrícula, haga clic en el nombre de la vista que desee editar.

   Al editar la vista predeterminada, los campos _[!UICONTROL Store]_y_[!UICONTROL Status]_ no están disponibles.

   ![Vista de tienda - editar vista predeterminada](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. Actualice los campos siguientes según sea necesario:

   - **[!UICONTROL Store]** (solo vistas no predeterminadas)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (solo si no se usa en `index.php`)
   - **[!UICONTROL Status]** (solo vistas no predeterminadas)
   - **[!UICONTROL Sort Order]**

1. Haga clic en **[!UICONTROL Save Store View]**.
