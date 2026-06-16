---
title: Permisos de administración
description: Obtenga información acerca de las cuentas de usuario de administración y cómo se utilizan los roles para otorgar acceso a las funciones de administración de tiendas.
exl-id: 54e4a322-4747-4472-b60b-cfe84c109f86
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
TQID: https://experienceleague.adobe.com/7xyouYohAbOKbwVCxZPamD-7gEiqGrqEAAg9FDm8z-U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# Permisos de administración

Adobe Commerce y Magento Open Source usan funciones y permisos para crear diferentes niveles de acceso al administrador. Cuando se configura el almacén por primera vez, recibe un conjunto de credenciales de inicio de sesión para la función Administrador que tiene permisos completos. Sin embargo, puede restringir el nivel de permisos según la &quot;necesidad de saber&quot; para otras personas que trabajen en el sitio. Por ejemplo, a un miembro del equipo de diseño se le puede dar acceso solo a las herramientas de diseño de contenido, pero no a las áreas con información de clientes y pedidos.

Además, puede restringir aún más el acceso de administrador solo a un sitio específico o a un conjunto de sitios y sus datos asociados. Si tiene varias marcas o unidades empresariales con tiendas independientes en la misma instalación de Commerce, puede proporcionar acceso de administrador a cada unidad empresarial, pero ocultar y proteger sus datos de otros usuarios administradores.

Cuando el acceso de un usuario administrador está restringido a un sitio web o tienda específicos, aquellos en los que no están autorizados no son visibles o aparecen atenuados. Solo se muestran al usuario los datos de ventas y otros datos de sitios web y tiendas permitidos.

- ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) De manera predeterminada, el sistema registra (registra) todas las acciones realizadas por un usuario cuando aplica los cambios a una tienda. Las acciones de administrador se pueden revisar en [Informe de registros de acciones](action-log-report.md). Configure el inicio de sesión en [Registro de acciones de administración](action-log.md) en la configuración de administración avanzada de su tienda.

![Administrador - todas las cuentas de usuario](./assets/users-all.png){width="700" zoomable="yes"}
