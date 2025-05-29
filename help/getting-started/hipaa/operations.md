---
title: Operaciones
description: Directrices para migrar a una oferta compatible con HIPAA y utilizar el entorno de ensayo secundario para la resolución de problemas.
exl-id: 058b43de-1cee-4557-b2e3-87ee7422bf9b
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Se aplica solo a proyectos de Adobe Commerce en la nube (infraestructura PaaS administrada por Adobe) y a proyectos locales."
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Operaciones

Utilice estas directrices para obtener más información acerca de la migración a la oferta compatible con HIPAA para Adobe Commerce y el uso del entorno `staging_for_support` para la solución de problemas.

## Migración

Los clientes que migran de una oferta de Commerce que no es compatible con HIPAA a una oferta compatible con HIPAA deben cumplir las siguientes directrices:

1. **Eliminar espacios de datos existentes**: antes de la migración, todos los espacios de datos existentes deben eliminarse para evitar la combinación de datos confidenciales y no confidenciales en la capa SaaS de Adobe Commerce. Cree un vale de soporte técnico para eliminar los espacios de datos.
1. **Configurar nuevo entorno**: la configuración de [Conector de servicios de Commerce](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas) en la nueva instancia de Commerce de HIPAA solo debe realizarse después de que se hayan eliminado los espacios de datos. El nuevo entorno de SaaS de HIPAA solo debe utilizarse después de eliminar los espacios de datos antiguos. La configuración de Commerce Services Connector déclencheur automáticamente la creación de nuevos espacios de datos SaaS.
1. **Estrategia de migración**: la eliminación de los espacios de datos SaaS es un proceso irreversible y elimina todos los datos del catálogo y las configuraciones relacionadas. Si desea transferir cualquiera de los datos o configuraciones anteriores, debe disponer de una estrategia de migración. Esta estrategia es responsabilidad del comerciante. Solo se debe crear un vale de soporte para eliminar los espacios de datos existentes una vez realizada la copia de seguridad de los datos de migración (si corresponde).

>[!NOTE]
>Para eliminar los espacios de datos existentes, los clientes deben crear un vale de soporte de Adobe Commerce con el título &quot;Migración HIPAA: Eliminar espacios de datos SaaS&quot;, proporcionar sus `MAGEID` y proporcionar los ID de proyecto SaaS que deben eliminarse.

## Solución de problemas con la asistencia de Adobe Commerce

La oferta compatible con HIPAA de Adobe Commerce viene con un entorno `staging_for_support` adicional que utilizará el equipo de soporte de Adobe Commerce para solucionar problemas.

Los clientes deben asegurarse de que el entorno `staging_for_support`:

- No contiene datos confidenciales, como, entre otros, Información médica protegida (PHI).
- No debe utilizarse para ninguna actividad de producción.
- No se debe asignar un nombre diferente de `staging_for_support` para evitar confusiones.
- Se mantiene actualizado con el código y la configuración del entorno de producción para garantizar que la resolución de problemas se realice en un entorno lo más cerca posible de la producción.

## Servicios de Commerce

- **Servicios de Commerce no preparados para HIPAA**: los clientes no deben utilizar los servicios de Adobe Commerce, como Live Search, Product Recommendations, Payment Services, Sales Channels o Commerce Intelligence porque no están preparados para HIPAA. Los clientes solo deben usar [servicios preparados para HIPAA](overview.md).

- **Conexión de datos**: solo el recopilador de back-office de la extensión [Conexión de datos](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview) está preparado para HIPAA. Los clientes no deben enviar PHI a servicios de conexión de datos no preparados para HIPAA, como eventos de tienda y Audience Activation. Los clientes deben asegurarse de que la recopilación de datos de la tienda esté deshabilitada.

- **Servicio de catálogo**: por diseño, [Servicio de catálogo](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/overview) no procesa la PHI, por lo que está fuera de ámbito para la auditoría de preparación y el cumplimiento de HIPAA. Los clientes son responsables de garantizar que utilizan este servicio en base a su propia evaluación de casos de uso y en consulta con el asesor legal. Los clientes tampoco deben utilizar el Servicio de catálogo a través del servicio federado para evitar el riesgo de pasar la PHI a servicios no preparados para HIPAA.

- **Exportación De Datos SaaS**: El servicio [Exportación De Datos SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview) debe configurarse para enviar datos solo para componentes preparados para HIPAA en Adobe Commerce.
