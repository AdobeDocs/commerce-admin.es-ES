---
title: '[!DNL AR Viewer] para la configuración de Adobe Commerce'
description: Obtenga información acerca de la administración de recursos de modelos 3D mediante la extensión  [!DNL AR Viewer] para sus listados de productos.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '293'
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
> Para ver una serie de vídeos de demostración en los que un usuario agrega un modelo 3d a un producto, consulta la página [Visor de AR para Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html?lang=es) en _Vídeos y Tutorials de Commerce_.
