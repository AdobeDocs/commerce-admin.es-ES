---
title: '[!DNL AR Viewer] para la configuración de Adobe Commerce'
description: Obtenga información acerca de la administración de recursos de modelos 3D mediante [!DNL AR Viewer] extensión para sus listados de productos.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Administre modelos 3D de productos con [!DNL AR Viewer] para Adobe Commerce

Para cada producto, puede cargar un `.USDZ` que permite utilizar modelos AR y 3D en su lista de productos.

El [!DNL AR Viewer] solo admite `.USDZ` archivos.

## Instalación de la extensión

[!DNL AR Viewer] se instala como una extensión desde el [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Consulte la [_Guía de instalación_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) para obtener más información sobre el proceso de instalación de la extensión.

Después del [!DNL AR Viewer] Una vez instalada y configurada la extensión, los usuarios administradores pueden configurar, personalizar y administrar listas de productos para incluir modelos 3D.

## Adición de un modelo 3D

1. Abra el producto en modo de edición.

1. Para trabajar con una vista de tienda específica, establezca el **[!UICONTROL Store View]** Seleccione la vista aplicable.

   >[!NOTE]
   >
   >Los nuevos modelos 3D de producto son _siempre_ cargado y visible en _todo_ vistas de la tienda, incluso si la variable `All Store Views` el ámbito no se utiliza para la carga. <br/><br/>Para ocultar cualquier modelo 3D de producto de una vista de tienda específica, debe cambiar a esa vista de tienda y seleccionar **[!UICONTROL Hide from Product Page]** para el modelo 3D y haga clic en **[!UICONTROL Save]**.

1. Desplácese hacia abajo y expanda _[!UICONTROL Product 3D Model]_sección.

   ![Menú emergente](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Añadir el modelo 3D (`.USDZ` archivo) del producto.

1. Haga clic **[!UICONTROL Save]**.

### Eliminación de un modelo 3D

Para eliminar un modelo 3D de los detalles del producto:

1. Haga clic **[!UICONTROL Delete]**.

1. Haga clic **[!UICONTROL Save]**.

## Ver modelos 3D del producto

Cuando los detalles del producto se actualizan con el modelo 3D:

1. El [!DNL AR Viewer] genera un código QR en la descripción del producto que codifica el archivo AR.

1. Un cliente puede ver este código QR en la página del producto.

1. Cuando los clientes escanean el código QR con sus dispositivos móviles, se procesa una experiencia de AR en el dispositivo móvil.

>[!NOTE]
>
> Para ver una serie de vídeos de demostración de cómo un usuario agrega un modelo 3d a un producto, consulte los [Visor de AR para Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) página en _Vídeos y Tutorials de Commerce_.
