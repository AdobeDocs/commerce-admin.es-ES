---
title: Añadir vídeos del producto
description: Obtenga información sobre cómo configurar vídeos de productos para su tienda, lo que requiere una clave de API de datos de YouTube de una cuenta de Google, y añadir un vínculo de vídeo para un producto.
exl-id: 0cfcee67-a2e2-41cb-ac70-304452f5db6d
feature: Catalog Management, Products, Media
source-git-commit: e439c1082834cbc81f6ccc7ca99e240d649c8b81
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Añadir vídeos del producto

Para añadir un vídeo de producto, primero debe obtener una clave de API de su cuenta de Google e introducirla en la configuración de su tienda. A continuación, puede vincular al vídeo desde el producto.

## Paso 1: Obtención de la clave de API de YouTube

1. Inicie sesión en su cuenta de Google y visite [Google Developers Console][1].

1. En el campo de búsqueda en la parte superior, ingrese `YouTube Data API v3` y haga clic en el icono de búsqueda.

1. Cuando se muestre la página de la API, asegúrese de que esté activada.

1. En el panel izquierdo, elija **[!UICONTROL Credentials]**.

1. Dependiendo de si tiene credenciales o no, realice una de las siguientes acciones:

   - Si ya tiene las credenciales necesarias, copie la clave en la tabla _claves API_.

   - Si todavía no tiene credenciales para esta API, haga clic en **[!UICONTROL Create Credentials]** en la parte superior y siga las indicaciones para crear las credenciales necesarias. En _Obtener sus credenciales_, copie la clave de API y haga clic en **[!UICONTROL Done]**.

1. Copie la clave de API en el portapapeles.

1. Haga clic en el icono Editar de la derecha y establezca las restricciones para asegurarse de que la clave de API esté limitada a los referentes correctos.

1. Espere unos momentos mientras se genera la clave y, a continuación, cópiela en el portapapeles.

   En el siguiente paso, pegará la clave en la configuración de la tienda.

## Paso 2: Configuración de la clave en Commerce

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Catalog]** debajo.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Product Video]_y pegue su **[!UICONTROL YouTube API key]**.

   ![Configuración de vídeo del producto](../configuration-reference/catalog/assets/catalog-product-video.png){width="600" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

1. Cuando se le solicite, actualice la caché.

## Paso 3: vincular al vídeo

1. Abra un producto en modo de edición.

1. Desplácese hasta y expanda la sección _[!UICONTROL Images and Videos]_.

   ![Imágenes y vídeos](./assets/product-simple-images-videos.png){width="600" zoomable="yes"}

1. haga clic en **[!UICONTROL Add Video]**.

   Si todavía no ha configurado su clave de API de YouTube, haga clic en **[!UICONTROL OK]** para continuar. No puede vincular a un vídeo de YouTube, pero puede pasar por el proceso.

1. Para **[!UICONTROL Url]**, ingrese la URL del video de YouTube o Vimeo.

   ![Nuevo vídeo para el producto](./assets/product-video-add.png){width="600" zoomable="yes"}

1. Haga clic fuera del campo y espere comentarios sobre la clave de API o el vídeo.

   Si todo se desprotege, YouTube proporciona información básica del vídeo

1. Escriba **[!UICONTROL Title]** y **[!UICONTROL Description]** del vídeo.

1. Para cargar un(a) **[!UICONTROL Preview Image]**, busque la imagen y seleccione el archivo.

   >[!NOTE]
   >
   >Después de la carga, un proveedor de servicios de vídeo externo genera automáticamente la imagen de vista previa que se muestra. No puede editar la imagen desde el administrador de Adobe Commerce.

1. Si prefiere usar los metadatos del vídeo, haga clic en **[!UICONTROL Get Video Information]**.

1. Para determinar cómo se usa el vídeo en la tienda, active la casilla de verificación de cada **[!UICONTROL Role]** que corresponda:

   - `Base Image`
   - `Small Image`
   - `Swatch Image`
   - `Thumbnail`
   - `Hide from Product Page`

1. Una vez finalizado, haga clic en **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Si la opción de configuración _[!UICONTROL Autostart base video]_se establece en `Yes` pero el vídeo no empieza a reproducirse automáticamente, podría deberse a las políticas de reproducción automática que aplica el explorador y que Adobe Commerce no puede controlar. Cada navegador compatible tiene sus propias políticas de reproducción automática que pueden cambiar con el tiempo y es posible que el vídeo no se reproduzca automáticamente en el futuro. Como práctica recomendada, no debe depender de la reproducción automática para la funcionalidad empresarial crítica y debe probar el comportamiento de reproducción automática de vídeo en su tienda con cada explorador compatible.

## Mantener acceso a API

Según los [Términos y condiciones] del desarrollador de Google, YouTube puede deshabilitar el acceso a la API para cuentas que hayan estado inactivas durante más de 90 días. Esto podría provocar que sus vídeos no se muestren. Para mantener el acceso a la API actualizado, utilice un trabajo cron para hacer ping a la API a intervalos regulares:

```code
30 10 1 * * curl -i -G -e https://yourdomain.com/ -d "part=snippet&maxResults=1&q=test&key=YOUTUBEAPIKEY" https://www.googleapis.com/youtube/v3/search >/dev/null 2>&1
```

## Referencia de campo

| Campo | Descripción |
|--- |--- |
| [!UICONTROL URL] | La URL del vídeo asociado. |
| [!UICONTROL Title] | El título del vídeo. |
| [!UICONTROL Description] | La descripción del vídeo. |
| [!UICONTROL Preview Image] | Una imagen cargada que se utiliza como previsualización del vídeo en su tienda. |
| [!UICONTROL Get Video Information] | Recupera los metadatos de vídeo almacenados en el servidor host. Puede utilizar los datos originales o actualizarlos según sea necesario. |
| [!UICONTROL Role] | Determina cómo se utiliza la imagen de vista previa en la tienda. Puede elegir cualquier combinación de opciones: `Base Image`, `Small Image`, `Thumbnail`, `Swatch Image`, `Hide from Product Page` |

{style="table-layout:auto"}

[1]: https://console.developers.google.com/
[Términos y condiciones]: https://developers.google.com/youtube/terms/developer-policies#d.-accessing-youtube-api-services
