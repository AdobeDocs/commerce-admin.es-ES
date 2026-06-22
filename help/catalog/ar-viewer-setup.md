---
title: '[!DNL AR Viewer] para la configuración de Adobe Commerce'
description: Obtenga información acerca de la administración de recursos de modelos 3D mediante la extensión  [!DNL AR Viewer] para sus listados de productos.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
TQID: https://experienceleague.adobe.com/6OlcZ4Psm3INgVm7f-Y9JvqfUdmR6Rg48tcigLAHiaE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 313
ht-degree: 0%

---

# Administrar modelos 3D de producto con [!DNL AR Viewer] para Adobe Commerce

Para cada producto, puede cargar un archivo de `.USDZ` que permita utilizar modelos AR y 3D en su lista de productos.

[!DNL AR Viewer] solo admite `.USDZ` archivos.

## Instalación de la extensión

[!DNL AR Viewer] está instalado como una extensión desde [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Consulte la [_Guía de instalación_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html?lang=es) para obtener más información sobre el proceso de instalación de la extensión.

Una vez instalada y configurada la extensión [!DNL AR Viewer], los usuarios administradores pueden configurar, personalizar y administrar listas de productos para incluir modelos 3D.

## Adición de un modelo 3D

1. Abra el producto en modo de edición.

1. Para trabajar con una vista de almacén específica, establezca el selector **[!UICONTROL Store View]** en la vista aplicable.

   >[!NOTE]
   >
   >Los nuevos modelos 3D de productos están _siempre_ cargados y son visibles en _todas_ las vistas de tiendas, incluso si el ámbito `All Store Views` no se usa para la carga. <br/><br/>Para ocultar cualquier modelo 3D de producto de una vista de tienda específica, debe cambiar a esa vista de tienda, seleccionar la casilla **[!UICONTROL Hide from Product Page]** del modelo 3D y hacer clic en **[!UICONTROL Save]**.

1. Desplácese hacia abajo y expanda la sección _[!UICONTROL Product 3D Model]_.

   ![Menú emergente](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Agregue el modelo 3D (archivo `.USDZ`) del producto.

1. Haga clic en **[!UICONTROL Save]**.

### Eliminación de un modelo 3D

Para eliminar un modelo 3D de los detalles del producto:

1. Haga clic en **[!UICONTROL Delete]**.

1. Haga clic en **[!UICONTROL Save]**.

## Ver modelos 3D del producto

Cuando los detalles del producto se actualizan con el modelo 3D:

1. [!DNL AR Viewer] genera un código QR en la descripción del producto que codifica el archivo AR.

1. Un cliente puede ver este código QR en la página del producto.

1. Cuando los clientes escanean el código QR con sus dispositivos móviles, se procesa una experiencia de AR en el dispositivo móvil.

>[!NOTE]
>
> Para ver una serie de vídeos de demostración de cómo un usuario agrega un modelo 3d a un producto, consulte la página [Visor de AR para Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html?lang=es) en _Vídeos y tutoriales de Commerce_.

