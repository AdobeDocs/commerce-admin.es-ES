---
title: 'Medios: mapa'
description: Obtenga información acerca del tipo de contenido Mapa, utilizado para agregar un mapa desde [!DNL Google Maps] Plataforma a la [!DNL Page Builder] escenario.
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 0%

---

# Medios: mapa

Utilice el _Mapa_ tipo de contenido desde el que añadir un mapa [[!DNL Google Maps] Plataforma][1] a la [[!DNL Page Builder] stage](workspace.md#stage). Por ejemplo, puede agregar una asignación a un bloque y, a continuación, agregar el bloque al [Acerca de nosotros](../content-design/pages.md#about-us) y [Contáctenos.](../getting-started/store-details.md#contact-us-form) páginas.

Para sacar el máximo partido a [!DNL Google Maps] Platform, puede personalizar el mapa, resaltar las ubicaciones de las tiendas y utilizar Google [Places][2] para agregar información enriquecida acerca de su tienda a todos [!DNL Google Maps].

## Ventajas de incrustar un mapa de Google

1. Ofrece a los compradores toda una gama de información sobre tu negocio (número de teléfono, sitio web, opiniones, valoraciones por estrellas, etc.) directamente en tu sitio.

1. Un mapa de Google suele resaltar atracciones, parques, restaurantes, etc. cercanos. Esta información ayuda a sus clientes a determinar su ubicación física y a planificar su viaje.

1. Facilita a los clientes encontrar la dirección de su tienda física sin necesidad de abrir una nueva ventana del explorador y abandonar el sitio.

1. Si tiene una cadena de tiendas físicas, añadir un Google Map en el sitio ayuda a aumentar la imagen de marca y la credibilidad en forma de elementos destacados.

![Ejemplo de tienda: mapa con ubicación](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Cuadro de herramientas Mapa

El cuadro de herramientas de asignación aparece cuando pasa el ratón por encima del contenedor de asignación.

| Herramienta | Icono | Descripción |
|--- |--- |--- |
| Mover | ![Icono Mover](./assets/pb-icon-move.png){width="25"} | Mueve el mapa a otra posición en el escenario. |
| (etiqueta) | [!UICONTROL Map] | Identifica el contenedor de contenido actual como un mapa. Pase el ratón sobre el contenedor del mapa para ver el cuadro de herramientas. |
| Configuración | ![Icono de configuración](./assets/pb-icon-settings.png){width="25"} | Abre la página Editar mapa, donde puede cambiar las propiedades del mapa y del contenedor. |
| Hide | ![Icono Ocultar](./assets/pb-icon-hide.png){width="25"} | Oculta el mapa actual. |
| Mostrar | ![Mostrar icono](./assets/pb-icon-show.png){width="25"} | Muestra el mapa oculto. |
| Duplicar | ![Icono Duplicar](./assets/pb-icon-duplicate.png){width="25"} | Realiza una copia del mapa. |
| Eliminar | ![Icono Eliminar](./assets/pb-icon-remove.png){width="25"} | Elimina el mapa de la fase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Configurar [!DNL Google Maps] para su administrador

Antes de añadir un mapa, primero debe abrir un [account][3] para una prueba gratuita de [!DNL Google Maps] Plataforma. La prueba gratuita dura 12 meses e incluye un crédito de $300. Si usas tu crédito, Google no factura tu cuenta sin tu permiso.

### Paso 1: Obtenga su [!DNL Google Maps] Clave de API

Dependiendo de si ya tiene un [!DNL Google Maps] utilice uno de los siguientes procedimientos para obtener la clave de API necesaria para la configuración. Para configurar un [!DNL Google Maps] clave, debe ser un administrador del sitio autorizado para habilitar la facturación para su cuenta. Si no está listo para configurar una [!DNL Google Maps] En la cuenta de Platform, puede omitir este paso y utilizar el mapa de marcador de posición por ahora.

1. Vaya a la [Consola de Google Cloud Platform](https://cloud.google.com/console/google/maps-apis/overview).

1. Haga clic en el menú desplegable del proyecto y seleccione o cree el proyecto para el que desea agregar una clave de API.

1. Para configurar las credenciales de la API, siga los [instrucciones][4] en el [!DNL Google Maps] documentaciones.

1. Copie la clave API en el portapapeles.

### Paso 2: Configuración [!DNL Google Maps] in [!DNL Commerce]

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, debajo de _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Herramientas de contenido avanzadas](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Para obtener más información sobre las opciones de configuración de las Herramientas avanzadas de administración de contenido, consulte la [Guía de referencia de configuración](../configuration-reference/general/content-management.md).

1. Para **[!UICONTROL Google Maps API Key]**, pegue la clave copiada en el paso 1.

1. Haga clic **[!UICONTROL Test Key]**.

   Si hay algún problema con la clave, vuelva al [!DNL Google Maps] Sitio de Platform para resolver el problema. A continuación, inténtelo de nuevo.

1. Tras comprobar la clave, haga clic en **[!UICONTROL Save Config]**.

## Añadir un mapa al escenario

1. Abra la página, el bloque o el bloque dinámico en [!DNL Page Builder] workspace.

1. En el [!DNL Page Builder] panel, expandir **[!UICONTROL Media]** y arrastre un **[!UICONTROL Map]** marcador de posición al escenario.

   ![Arrastrar un mapa al escenario](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   If [!DNL Google Maps] Platform está configurado para su tienda y aparece un mapa para su ubicación.

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   If [!DNL Google Maps] Platform aún no se ha configurado para su tienda; en su lugar, aparecerá un mapa de marcador de posición.

   ![[!DNL Google Maps] Marcador](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## Añadir una ubicación de mapa personalizada

1. Pase el ratón sobre el contenedor de mapas para mostrar el cuadro de herramientas y elegir la _Configuración_ ( ![Icono de configuración](./assets/pb-icon-settings.png){width="20"} ) icono.

1. En la esquina superior derecha de la _[!UICONTROL Edit Map]_página, haga clic en **[!UICONTROL Add Location]**.

1. Introduzca el **[!UICONTROL Location Name]** que desea que se asocie con el pin del mapa.

1. Recopile las coordenadas de ubicación que desee utilizar para la ubicación personalizada.

   Alternativamente, en la variable **[!UICONTROL Position]** , puede arrastrar el pin en el mapa mostrado.

   Si es necesario, vaya a [[!DNL Google Maps]][5] en una nueva ventana del explorador y utilice uno de los siguientes métodos para obtener las coordenadas:

   ![Coordenadas de mapa](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **Método 1:** Copiar desde URL

   - En la esquina superior izquierda, introduzca la dirección en la **[!UICONTROL Search]** y haga clic en el _Buscar_ ( ![Icono de búsqueda](../assets/icon-magnify-search.png){width="20"} ) icono.

   - Copie las coordenadas en la dirección URL y péguelas en un bloc de notas.

   **Método 2:** Copia de &quot;¿Qué hay aquí?&quot;

   - Haga clic con el botón derecho en el pin rojo que marca la ubicación en el mapa y elija **[!UICONTROL What's here?]** en el menú.

   - En la etiqueta mostrada, copie el texto, incluidas las coordenadas, y péguelo en un bloc de notas.

1. Introduzca los números, sin comas, en cada una de las **[!UICONTROL Coordinates]** cajas.

   También puede introducir la mayor parte de la información restante que desee que esté disponible en el mapa.

1. Complete cualquier otra información que desee asociar con la ubicación del mapa:

   | Opción | Descripción |
   | ------ | ----------- |
   | [!UICONTROL Phone Number] | Número de teléfono de la ubicación. |
   | [!UICONTROL Street Address] | La dirección de la ubicación. |
   | [!UICONTROL City] | La ciudad de la ubicación. |
   | [!UICONTROL Region/State] | La región o el estado de la ubicación. |
   | [!UICONTROL Zip/Postal Code] | El código postal de la ubicación. |
   | [!UICONTROL Country] | El país de la ubicación. |
   | [!UICONTROL Comment] | Los comentarios que desee incluir. |

   {style="table-layout:auto"}

1. Cuando termine, haga clic en **[!UICONTROL Save]**.

   La nueva ubicación aparece en el mapa y en la cuadrícula de ubicación del mapa, en la _[!UICONTROL Edit Map]_página.

   ![[!DNL Page Builder] - asigna la cuadrícula de ubicación](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## Aplicar estilo al mapa {#styling}

Utilice el [!DNL Google Maps] Asistente para estilos de plataforma para aplicar una de las seis temáticas predefinidas o para crear una temática personalizada. Puede generar un archivo JSON con las propiedades de estilo de asignación o un vínculo al mapa con estilo.

### Cambio del estilo del mapa

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, debajo de _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. En el **[!UICONTROL Google Maps Style]** , haga clic en [Crear estilo de mapa][6].

   Esta acción abre el [[!DNL Google Maps] Asistente de estilo de plataforma][6] en una pestaña independiente, donde puede definir un estilo para su [!DNL Google Maps] Proyecto de plataforma.

1. Clic **[!UICONTROL Create a Style]** y siga las instrucciones proporcionadas.

   Cuando termine, haga clic en **[!UICONTROL Finish]**.

1. Exporte el estilo completado como código JSON o como URL para poder agregarlo al [!DNL Commerce] configuración.

   - **JSON**: Debajo del cuadro con el código JSON generado, haga clic en **[!UICONTROL Copy JSON]**.

   - **[!UICONTROL URL]**: Debajo del cuadro con la dirección URL generada, haga clic en **[!UICONTROL Copy URL]**.

1. Vuelva a la pestaña del explorador de administración y pegue el código o la dirección URL generados en la **Estilo de mapas de Google** cuadro.

   Si utiliza una dirección URL, sustituya el `YOUR_API_KEY` marcador de posición con [!DNL Google Maps] Clave de API. Esta dirección URL está vinculada al mapa de Google con estilo.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Save Config]**.

### Cambio de la configuración del mapa

1. Pase el ratón sobre el contenedor del mapa para mostrar el cuadro de herramientas y elija la _Configuración_ ( ![Icono de configuración](./assets/pb-icon-settings.png){width="20"} ) icono.

1. Cambie la configuración básica según sea necesario:

   | Opción | Descripción |
   | ------ | ----------- |
   | [!UICONTROL Height] | Especifica la altura del mapa mostrado en píxeles. |
   | [!UICONTROL Show Controls] | Determina si aparecen los controles estándar de Google Map. |

   {style="table-layout:auto"}

1. Modifique la _[!UICONTROL Advanced]_ajustes según sea necesario:

   - Para controlar la posición horizontal del contenido del mapa que se ha agregado al contenedor, elija un **[!UICONTROL Alignment]**:

     | Opción | Descripción |
     | ------ | ----------- |
     | `Default` | Aplica la configuración predeterminada de alineación especificada en la hoja de estilos de la temática actual. |
     | `Left` | Alinea el contenido a lo largo del borde izquierdo del contenedor de mapas, con margen para cualquier relleno que se especifique. |
     | `Center` | Alinea el contenido en el centro del contenedor de mapas, con margen para cualquier relleno que se especifique. |
     | `Right` | Alinea el contenido a lo largo del borde derecho del contenedor de mapas, con margen para cualquier relleno que se especifique. |

     {style="table-layout:auto"}

   - Configure las variables **[!UICONTROL Border]** estilo aplicado a los cuatro lados del contenedor de mapas:

     | Opción | Descripción |
     | ------ | ----------- |
     | `Default` | Aplica el estilo de borde predeterminado especificado por la hoja de estilos asociada. |
     | `None` | No proporciona ninguna indicación visible de los bordes del contenedor. |
     | `Dotted` | El borde del contenedor aparece como una línea de puntos. |
     | `Dashed` | El borde del contenedor aparece como una línea discontinua. |
     | `Solid` | El borde del contenedor aparece como una línea sólida. |
     | `Double` | El borde del contenedor aparece como una línea doble. |
     | `Groove` | El borde del contenedor aparece como una línea ranurada. |
     | `Ridge` | El borde del contenedor aparece como una línea discontinua. |
     | `Inset` | El borde del contenedor aparece como una línea de margen. |
     | `Outset` | El borde del contenedor aparece como una línea de inicio. |

     {style="table-layout:auto"}

   - Si establece un estilo de borde distinto de `None`, complete las opciones de visualización de bordes:

     ![Color del borde](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

     | Opción | Descripción |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Especifique el color seleccionando una muestra, haciendo clic en el selector de color o introduciendo un nombre de color válido o un valor hexadecimal equivalente. |
     | [!UICONTROL Border Width] | Introduzca el número de píxeles de la anchura de la línea del borde. |
     | [!UICONTROL Border Radius] | Introduzca el número de píxeles para definir el tamaño del radio que se utiliza para redondear cada esquina del borde. |

     {style="table-layout:auto"}

   - (Opcional) Especifique los nombres de **[!UICONTROL CSS classes]** de la hoja de estilos actual para aplicarla al contenedor de mapas.

     Separe los distintos nombres de clase con un espacio.

   - Introduzca valores, en píxeles, para **[!UICONTROL Margins and Padding]** para especificar los márgenes externos y el relleno interno del contenedor de mapas.

     Introduzca cada valor correspondiente en el diagrama del contenedor de asignaciones.

     | Área del contenedor | Descripción |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Cantidad de espacio en blanco que se aplica al borde exterior de todos los lados del contenedor. |
     | [!UICONTROL Padding] | Cantidad de espacio en blanco que se aplica al borde interior de todos los lados del contenedor. |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >El relleno no está disponible para el tipo de contenido Asignar.

1. Cuando termine, haga clic en **[!UICONTROL Save]** para aplicar la configuración de y volver a [!DNL Page Builder] workspace.

### Cambiar el tamaño de la cuadrícula

El tamaño de la cuadrícula determina el tamaño del mapa relacionado con una [columna](column.md) en el [!DNL Page Builder] escenario. De forma predeterminada, el mapa tiene 12 columnas de ancho, con un máximo de 16 columnas.

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, debajo de _[!UICONTROL General]_, elija **[!UICONTROL Content Management]**.

1. Expandir ![Selector de expansión](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Actualice las opciones de cuadrícula según sea necesario:

   >[!NOTE]
   >
   >Si es necesario, borre la **[!UICONTROL Use system value]** para modificar esta configuración.

   - Para **[!UICONTROL Default Column Grid Size]**, introduzca un nuevo valor para el tamaño predeterminado de la cuadrícula.

   - Para **[!UICONTROL Maximum Column Grid Size]**, introduzca un nuevo valor para el tamaño máximo de cuadrícula predeterminado.

   ![Configuración de tamaño de cuadrícula de columna](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. Cuando termine, haga clic en **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://cloud.google.com/maps-platform/places/
[3]: https://cloud.google.com/maps-platform/user-guide/
[4]: https://developers.google.com/maps/documentation/javascript/get-api-key
[5]: https://www.google.com/maps
[6]: https://mapstyle.withgoogle.com/
