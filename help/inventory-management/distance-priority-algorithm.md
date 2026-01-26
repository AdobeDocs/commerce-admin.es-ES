---
title: Configuración del algoritmo de prioridad de distancia
description: Establezca la configuración para comparar la ubicación de la dirección de destino de envío con las ubicaciones de origen para determinar el origen más cercano para satisfacer los envíos.
exl-id: 4dec179a-25ac-48db-a84b-4974798272b0
feature: Inventory, Configuration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Configuración del algoritmo de prioridad de distancia

El algoritmo de prioridad de distancia compara la ubicación de la dirección de destino de envío con las ubicaciones de origen para determinar el origen más cercano para realizar envíos. La distancia puede determinarse por la distancia física o el tiempo que se pasa viajando de un lugar a otro, usando datos de la base de datos o direcciones para conducir, caminar o andar en bicicleta. Use este [algoritmo de selección de Source](selection-reservations.md) para recomendar el origen más cercano a las direcciones de destino de envío.

>[!NOTE]
>
>Si usas el algoritmo de prioridad de distancia, es recomendable que introduzcas la dirección de la calle completa y las coordenadas GPS de tus [orígenes](sources-add.md).

Tiene dos opciones para calcular la distancia y el tiempo para encontrar el origen más cercano para la satisfacción del envío:

- **Google MAP**: utiliza los servicios de [Google Maps Platform](https://cloud.google.com/maps-platform/) para calcular la distancia y el tiempo entre la dirección de destino de envío y las ubicaciones de origen. Esta opción utiliza la latitud y longitud de la fuente (coordenadas GPS) y puede utilizar la dirección de la calle según el modo de cálculo. Se requiere una clave de API de Google con [Geocoding API](https://developers.google.com/maps/documentation/geocoding/start) y [Distance Matrix API](https://developers.google.com/maps/documentation/distance-matrix/start) habilitadas, y es posible que se te cobre a través de Google.

- **Cálculo sin conexión**: calcula la distancia usando datos de geocódigo descargados e importados usando códigos postales y coordenadas GPS para determinar el origen más cercano a la dirección de destino de envío. Para configurar esta opción, es posible que necesite asistencia del desarrollador para descargar e importar inicialmente geocódigos mediante instrucciones de la línea de comandos.

>[!NOTE]
>
>Para sitios web de varias tiendas con varios países, configure [destino de impuestos predeterminado](../stores-purchase/tax-class.md#default-tax-destination){target="_blank"} para cada país.

## Uso de mapas de Google

No necesita una cuenta de Google para empezar. El proceso incluye la creación de cuentas de Google y proyectos, si es necesario. Esta opción requiere que se agregue una cuenta de facturación y un método de pago a la cuenta de Google para completar las configuraciones y utilizar el algoritmo.
Sin embargo, se recomienda utilizar un algoritmo basado en la distancia MAP de Google como más avanzado y preciso en comparación con el cálculo sin conexión.

### Paso 1: Crear la clave de API de Google

La clave es de [Google Maps Platform](https://cloud.google.com/maps-platform/) y debe tener habilitados [Geocoding API](https://developers.google.com/maps/documentation/geocoding/start) y [Distance Matrix API](https://developers.google.com/maps/documentation/distance-matrix/start). Para obtener más información, consulte [Configuración del algoritmo de prioridad de distancia](distance-priority-algorithm.md).

1. Visite [Google Maps Platform](https://cloud.google.com/maps-platform/) y haga clic en **[!UICONTROL Get Started]**.

1. Para habilitar la plataforma, seleccione **[!UICONTROL Maps, Routes, and Places]** y haga clic en **[!UICONTROL Continue]**.

   ![Plataforma de Google Maps para tu clave](assets/inventory-google-key1.png){width="350" zoomable="yes"}

1. Inicie sesión con una cuenta de Google o cree una cuenta.

1. Configurar un proyecto:

   - Seleccione un proyecto o escriba un nombre nuevo.

   - Para aceptar los términos, seleccione `Yes`.

   - Haga clic en **[!UICONTROL Next]**.

1. Introduzca una cuenta de facturación o cree una. Puede omitir y agregar una cuenta de facturación más adelante.

   Se requiere una cuenta de facturación para utilizar este servicio.

1. Para abrir y configurar las opciones de Google Cloud Platform, haga clic en **[!UICONTROL Console]**.

   - Abra el proyecto.

   - Expanda el menú y haga clic en **[!UICONTROL APIs & Services]** > **[!UICONTROL Library]**.

     ![Servicios de API de Google](assets/inventory-google-key2.png){width="350" zoomable="yes"}

   - Busque [API de geocodificación](https://developers.google.com/maps/documentation/geocoding/start) y [API de matriz de distancia](https://developers.google.com/maps/documentation/distance-matrix/start). Seleccione y habilite cada servicio.

1. Expanda el menú, haga clic en **[!UICONTROL APIs & Services]** > **[!UICONTROL Credentials]** y copie la clave de API de Google.

   ![Copia de clave de API de Google](assets/inventory-google-key3.png){width="350" zoomable="yes"}

### Paso 2: Configuración del proveedor de Google MAP

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Inventory]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Distance Provider for Distance Based SSA]_&#x200B;y establezca **[!UICONTROL Provider]**&#x200B;en `Google MAP`.

   ![Proveedores para SSA basado en distancia](assets/config-catalog-inventory-distance-provider.png){width="350" zoomable="yes"}

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Google Distance Provider]_&#x200B;y configure las opciones:

   - Para **[!UICONTROL Google API Key]**, ingrese la clave copiada de su cuenta de Google.

   - Para **[!UICONTROL Computation mode]**, seleccione una configuración.

     >[!NOTE]
     >
     >Cuando se utiliza este algoritmo para el envío, si las rutas y los datos no se devuelven para el modo de cálculo seleccionado (conducir, montar en bicicleta o caminar) para un envío, el SSA utiliza de forma predeterminada la prioridad de Source. Se recomienda establecer la prioridad [para orígenes por existencia](stocks-prioritize-sources.md).

     | Opción | Descripción |
     | ----- | ----- |
     | `Driving` | (Predeterminado) Solicita las indicaciones de conducción estándar a través de la red de carreteras. |
     | `Walking` | Solicita indicaciones para caminar usando senderos peatonales y aceras (cuando estén disponibles). |
     | `Bicycling` | Solicita direcciones de ciclismo usando rutas de bicicleta y calles preferidas (cuando estén disponibles). El [Servicio de matriz a distancia](https://developers.google.com/maps/documentation/javascript/distancematrix#travel_modes) sólo está disponible en EE.UU. y en algunas ciudades canadienses. |

   - Para **[!UICONTROL Value]**, seleccione un tipo de valor:

     | Opción | Descripción |
     | ----- | ----- |
     | `Distance` | (Predeterminado) Devuelve la distancia entre puntos en métricas (kilómetros y metros) o imperiales (millas y pies). |
     | `Time to Destination` | Devuelve el tiempo necesario para viajar desde las ubicaciones de origen a la dirección de envío en horas y minutos. |

   ![Proveedor de distancia de Google](assets/config-catalog-inventory-distance-provider-settings.png){width="350" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.

## Usar cálculo sin conexión

Los cálculos sin conexión utilizan códigos de país para determinar la distancia entre el destino de envío y las direcciones de origen. Esta opción puede requerir la asistencia del desarrollador para configurarla. Use un comando CLI [!DNL Inventory Management] para descargar e importar datos de [geonames.org](https://www.geonames.org/).

>[!NOTE]
>
>Los códigos geográficos importados de [geonames.org](https://www.geonames.org/) tienen limitaciones en algunos países, como Canadá e Irlanda. Consulte [Archivos de código postal con nombres geográficos](https://download.geonames.org/export/zip/readme.txt) para obtener más información.

### Paso 1: Descargar e importar códigos geográficos

Configuración completa de la línea de comandos para descargar e importar códigos geográficos de países a los que realizar envíos y ubicaciones de origen en. Este paso puede requerir la ayuda del desarrollador para las tareas de línea de comandos. Consulte [Importar códigos geográficos](cli.md#import-geocodes).

Complete estos comandos siempre que desee agregar más geocódigos.

### Paso 2: Configurar el cálculo

1. En la barra lateral _Admin_, vaya a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. En el panel izquierdo, expanda **[!UICONTROL Catalog]** y elija **[!UICONTROL Inventory]**.

1. Expanda ![Selector de expansión](../assets/icon-display-expand.png) en la sección _[!UICONTROL Distance Provider for Distance Based SSA]_.

1. Anule la selección de la casilla de verificación **[!UICONTROL Use system value]** y establezca **[!UICONTROL Provider]** en `Offline Calculation`.

   ![Proveedores de distancia para SSA basado en distancia](assets/inventory-distance-offline.png){width="350" zoomable="yes"}

1. Una vez finalizado, haga clic en **[!UICONTROL Save Config]**.
