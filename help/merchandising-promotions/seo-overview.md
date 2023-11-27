---
title: Optimización del motor de búsqueda
description: Obtenga información acerca de las herramientas de optimización de los motores de búsqueda (SEO) para sitios de Commerce y prácticas recomendadas para una SEO óptima.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Información general de SEO

_Optimización del motor de búsqueda_ (SEO) es la práctica de ajustar el contenido y la presentación de un sitio para mejorar la forma en que los motores de búsqueda indexan las páginas. Commerce incluye varias funciones para apoyar tu esfuerzo continuo de SEO.

## Metadatos

Más información sobre cómo añadir y mejorar elementos enriquecidos con palabras clave [metadatos](meta-data.md) para su sitio y tienda.

## Uso de un mapa del sitio

A [mapa del sitio](sitemap-xml.md) mejora la forma en que los motores de búsqueda indexan su tienda y está diseñada para encontrar páginas que los rastreadores web podrían pasar por alto. Se puede configurar un mapa del sitio para indexar todas las páginas e imágenes.

## Reescrituras de URL

El [Reescritura de URL](url-rewrite.md) Esta herramienta permite cambiar cualquier dirección URL asociada a un producto, categoría o página de CMS.

## Robots de motor de búsqueda

La configuración de Commerce incluye opciones para generar y administrar instrucciones para los rastreadores web y bots que indexan el sitio. Si la solicitud de `robots.txt` llega a Commerce (en lugar de un archivo físico) y se dirige dinámicamente al controlador de robots. Las instrucciones son directivas que la mayoría de los motores de búsqueda reconoce y sigue.

De forma predeterminada, el archivo robots.txt generado por Commerce contiene instrucciones para el rastreador web a fin de evitar la indexación de determinadas partes del sitio que contienen archivos que el sistema utiliza internamente. Puede utilizar la configuración predeterminada o definir sus propias instrucciones personalizadas para todos o para motores de búsqueda específicos. Hay muchos artículos en línea que exploran el tema en detalle.

### Ejemplo de instrucciones personalizadas

**Permite acceso completo**

    User-agent:*
    No permitir:

**No permite el acceso a todas las carpetas**

    User-agent:*
    No permitir: /

**Instrucciones predeterminadas**

    User-agent: *
    No permitir: /index.php/
    No permitir: /*?
    No permitir: /checkout/
    No permitir: /app/
    No permitir: /lib/
    No permitir: /*.php$
    No permitir: /pkginfo/
    No permitir: /report/
    No permitir: /var/
    No permitir: /catalog/
    No permitir: /customer/
    No permitir: /sendfriend/
    No permitir: /review/
    No permitir: /*SID=

### Configurar `robots.txt`

1. En el _Administrador_ barra lateral, vaya a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Busque el **[!UICONTROL Global]** en la primera fila de la cuadrícula y haga clic en **[!UICONTROL Edit]**.

   ![Configuración de diseño global](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Desplazarse hacia abajo y expandir ![Selector de expansión](../assets/icon-display-expand.png) el **[!UICONTROL Search Engine Robots]** y haga lo siguiente:

   ![Configuración de diseño: robots de motor de búsqueda](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Establecer **[!UICONTROL Default Robots]** a uno de los siguientes:

     | Opción | Descripción |
     |------|------------|
     | `INDEX, FOLLOW` | Indica a los rastreadores web que indexen el sitio y que vuelvan más tarde para ver si hay cambios. |
     | `NOINDEX, FOLLOW` | Indica a los rastreadores web que eviten indizar el sitio, pero que vuelvan más tarde para ver si hay cambios. |
     | `INDEX, NOFOLLOW` | Indica a los rastreadores web que indiquen el sitio una vez, pero que no vuelvan más tarde para ver si hay cambios. |
     | `NOINDEX, NOFOLLOW` | Indica a los rastreadores web que eviten indizar el sitio y que no vuelvan más tarde para ver si hay cambios. |

     {style="table-layout:auto"}

   - Si es necesario, introduzca instrucciones personalizadas en la **[!UICONTROL Edit Custom instruction of robots.txt file]** cuadro. Por ejemplo, mientras un sitio está en desarrollo, es posible que desee impedir el acceso a todas las carpetas.

   - Para restaurar las instrucciones predeterminadas, haga clic en **[!UICONTROL Reset to Default]**.

1. Cuando termine, haga clic en **[!UICONTROL Save Configuration]**.
