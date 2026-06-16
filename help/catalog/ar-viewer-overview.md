---
title: '[!DNL AR Viewer] para Adobe Commerce'
description: Descubra cómo  [!DNL AR Viewer] podría beneficiar a su instancia de Adobe Commerce y cómo incorporar y configurar correctamente la extensión.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
TQID: https://experienceleague.adobe.com/ofebqdDS0exPDKJMLB-mpE0eVjRKT5ck91Fm2-7CVjA
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a09a5a04-e30b-4d55-b031-38e6f5ec86dbid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# [!DNL AR Viewer] para Adobe Commerce

La realidad aumentada (RA) describe experiencias del usuario que agregan elementos 2D o 3D a la vista en vivo desde la cámara de un dispositivo de una manera que hace que esos elementos parezcan habitar el mundo real.

La extensión [!DNL AR Viewer] para Adobe Commerce ofrece una experiencia perfecta diseñada para mostrar gráficos 3D procesados para el usuario.

La información de esta guía proporciona una descripción general de la experiencia de incorporación de [!DNL AR Viewer] en Adobe Commerce y de cómo [!DNL AR Viewer] beneficia al usuario, así como las prácticas recomendadas a lo largo de ese recorrido.

Desarrollado por Pixar, [Universal Scene Description (USD)](https://openusd.org/release/index.html){target=_blank} es el primer software de código abierto que puede intercambiar de manera robusta y escalable escenas 3D que pueden estar compuestas de muchos recursos, fuentes y animaciones diferentes, a la vez que fomenta flujos de trabajo altamente colaborativos. Este USD se usa en `.USDZ` archivos. Este archivo de `.USDZ` entrega contenido AR y 3D a los dispositivos del usuario.

>[!NOTE]
>
> [!DNL AR Viewer] solo admite `.USDZ` archivos.

## [!DNL AR Viewer] requisitos

[!DNL AR Viewer] es compatible con [!DNL Magento Open Source] y Adobe Commerce. Consulte [Política del ciclo vital](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} para obtener más información sobre las versiones compatibles.

Consulte [Instalar la [!DNL AR Viewer] extensión](../catalog/ar-viewer-setup.md) para obtener más información.

Para usar [!DNL AR Viewer], debe tener disponible lo siguiente para su instancia:

* PHP 8.1.0
* Adobe Commerce versión 2.4.4 y posterior
* Magento Open Source (CE) versión 2.4.x

## Limitaciones de compatibilidad

[!DNL AR Viewer] limitaciones de compatibilidad existentes:

* Solo `.USDZ`: esta característica solo admite `.USDZ` archivos.
* `qr-code`: requiere `endroid/qr-code` versión 4.5.
* `Catalog module`: requiere `magento/module-catalog` versión 104.0.0.
