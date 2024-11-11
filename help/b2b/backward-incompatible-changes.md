---
title: Cambios incompatibles con versiones anteriores de Adobe Commerce B2B
description: Obtenga información sobre los cambios en las versiones de Adobe Commerce B2B que pueden requerir la actualización del código personalizado.
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Cambios incompatibles con versiones anteriores de Adobe Commerce B2B

Revise la información de referencia de alto nivel para todos los cambios incompatibles con versiones anteriores en B2B para versiones de Adobe Commerce. Consulte la sección de elementos destacados para ver los cambios incompatibles que tienen un impacto importante y que requieren una explicación detallada e instrucciones especiales.

## Características destacadas

### 1.4.2 a 1.5.0

Con la adición de la asignación de varias empresas, las cuentas de usuario de la empresa ahora pueden tener varios valores de `company_id`. `Magento\Company\Api\Data\CompanyCustomerInterface` se actualizó para establecer el valor predeterminado `company_id` de un usuario. El valor predeterminado se establece en la primera compañía asignada a la cuenta de usuario de la compañía.

Si está actualizando desde una versión anterior, Adobe recomienda implementar los siguientes métodos en las clases que usan `Magento\Company\Api\Data\CompanyCustomerInterface`.

- Magento\Company\Api\Data\CompanyCustomerInterface::getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface::setIsDefault

## Referencia

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
