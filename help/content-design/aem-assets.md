---
title: Integración de Experience Manager Assets para Commerce
description: Aprenda a integrar Experience Manager Assets con su instancia  [!DNL Commerce] para acceder a innumerables recursos multimedia para usarlos en su tienda.
feature: CMS, Media, Configuration, Integration
source-git-commit: 8588973f265c6bd3dfdd41e574f27f653cc9da0e
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Integración de Experience Manager Assets para Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

La integración entre Commerce y Adobe Experience Manager AEM () Assets AEM combina las sólidas capacidades de un sistema de administración de activos digitales (DAM) de la marca de datos, el de la empresa, con el de Adobe Commerce, para mejorar las experiencias de comercio electrónico de los clientes. AEM Esta integración aprovecha las potentes funciones de administración de recursos de los que dispone el usuario para proporcionar una forma sencilla, escalable y eficaz de administrar y ofrecer recursos en las tiendas de comercio.

**Características principales**

- **Administración centralizada de recursos**

   - **AEM Assets as the Single Source of Truth**-AEM Assets sirve como repositorio central para todos los recursos digitales, lo que garantiza que todas las plataformas de comercio electrónico tengan acceso a recursos aprobados que no pertenecen a la marca.

   - AEM **Administración masiva de recursos**: las organizaciones pueden administrar grandes volúmenes de recursos de manera eficiente, gracias a las sólidas capacidades de administración de recursos que ofrece el usuario. Esto permite a los especialistas en marketing y comercialización asignar grandes conjuntos de imágenes para nuevas líneas de productos de forma eficaz.

- **Experiencias de Commerce AEM personalizadas**: Al usar los servicios GenAI en las organizaciones, las organizaciones pueden generar millones de variaciones de productos para experiencias de comercio electrónico personalizadas. Los especialistas en marketing y los comerciantes pueden utilizar estas imágenes para crear tiendas dinámicas para los lanzamientos de productos y las campañas de temporada, lo que mejora la participación y aumenta las tasas de conversión.

- AEM **Coincidencia automatizada de recursos**: la integración incluye un servicio de motor de reglas que hace coincidir automáticamente los recursos de los productos de Adobe Commerce en función de la SKU u otros atributos clave. El servicio garantiza que los recursos y las variaciones de productos más recientes siempre estén disponibles en las tiendas de comercio electrónico. También reduce el esfuerzo manual necesario para administrar los activos, lo que libera tiempo para actividades más estratégicas.

- **Procesos optimizados**
   - **Habilite y configure la integración desde el administrador de Commerce**: los administradores y desarrolladores pueden instalar y configurar la integración desde Adobe Commerce con herramientas y procesos conocidos.
   - **Actualizaciones dinámicas**: mantenga las imágenes de los productos actualizadas con los cambios más recientes en el sistema de administración de recursos. Estas actualizaciones automatizadas garantizan que las tiendas de comercio siempre tengan la información de producto más actualizada.
   - **Administración eficiente del catálogo**: simplifica el mantenimiento del catálogo de productos al automatizar la limpieza y actualización de los recursos.

## Integración de Commerce y Experience Manager Assets

>[!BEGINSHADEBOX]

**Requisitos previos**

- Adobe Commerce debe configurarse con la [integración de administración de Commerce con Adobe ID](/help/getting-started/adobe-ims-config.md) con un identificador de organización asignado.
- Experience Manager Assets debe asignarse como producto al mismo ID de organización.
- El usuario que configura la integración debe tener una cuenta en la misma organización con derechos administrativos para acceder a Adobe Commerce y Experience Manager Assets.

>[!ENDSHADEBOX]

Para habilitar la integración de Commerce con Experience Manager Assets, complete las siguientes tareas:

1. [Configuración del proyecto de Experience Manager Assets para administrar los recursos de Commerce](aem-assets-configure-aem.md)

1. [Instalación de la extensión de integración de Experience Manager Assets y configuración de Adobe Commerce](aem-assets-configure-commerce.md)

1. [Configurar servicios de sincronización](aem-assets-setup-synchronization.md)
