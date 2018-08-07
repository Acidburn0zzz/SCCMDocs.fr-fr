---
title: Données d’utilisation et de diagnostics
titleSuffix: Configuration Manager
description: Découvrez quelles données d’utilisation et de diagnostic System Center Configuration Manager collecte à son sujet.
ms.date: 07/30/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
ms.assetid: 88ac4e55-d47b-4c94-b9c3-704c6a48b845
author: aczechowski
ms.author: aaroncz
manager: dougeby
ms.openlocfilehash: 031815e741128d605bf7ee50079338eba7aa720b
ms.sourcegitcommit: 1826664216c61691292ea2a79e836b11e1e8a118
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/31/2018
ms.locfileid: "39384107"
---
# <a name="diagnostics-and-usage-data-for-system-center-configuration-manager"></a>Données d’utilisation et de diagnostic pour System Center Configuration Manager

*S’applique à : System Center Configuration Manager (Current Branch)*

Configuration Manager collecte les données d’utilisation et de diagnostic qui le concernent. Microsoft utilise ensuite ces données pour améliorer le processus d’installation, la qualité et la sécurité des versions ultérieures.  

 Les données d’utilisation et de diagnostic sont collectées pour chaque hiérarchie Configuration Manager. Elle consistent en requêtes SQL Server qui s’exécutent chaque semaine sur chaque site principal et sur le site d’administration centrale. Quand la hiérarchie utilise un site d’administration centrale, les données provenant des sites principaux sont répliquées sur ce site. Sur le site de niveau supérieur de votre hiérarchie, le point de connexion de service soumet ces informations quand il recherche des mises à jour. Si le point de connexion de service est en mode hors connexion, les informations sont transférées à l’aide de l’outil de connexion de service.  

> [!NOTE]  
>  Configuration Manager collecte uniquement les données de la base de données SQL Server du site. Il ne collecte pas de données directement à partir des clients ni des serveurs de site.  

 Pour plus d’informations, consultez la [Déclaration de confidentialité de Microsoft](https://go.microsoft.com/fwlink/?LinkID=626527).  

## <a name="articles"></a>Articles
 Pour en savoir plus sur les données d’utilisation et de diagnostic de Configuration Manager, consultez les articles suivants :  

-   [Utilisation des données de diagnostic et d’utilisation](../../../core/plan-design/diagnostics/how-diagnostics-and-usage-data-is-used.md)  

-   Niveaux de collecte des données d’utilisation et de diagnostic :
    - [Données de diagnostic pour 1806](/sccm/core/plan-design/diagnostics/levels-of-diagnostic-usage-data-collection-1806)  

    - [Données de diagnostic pour 1802](/sccm/core/plan-design/diagnostics/levels-of-diagnostic-usage-data-collection-1802)  

    - [Données de diagnostic pour 1710](/sccm/core/plan-design/diagnostics/levels-of-diagnostic-usage-data-collection-1710)  
    
-   [Mode de collecte des données de diagnostic et d’utilisation](../../../core/plan-design/diagnostics/how-diagnostics-and-usage-data-is-collected.md)  

-   [Mode d’affichage des données de diagnostic et d’utilisation](../../../core/plan-design/diagnostics/view-diagnostics-and-usage-data.md)  

-   [Programme d’amélioration de l’expérience utilisateur (CEIP)](../../../core/plan-design/diagnostics/customer-experience-improvement-program-ceip.md)  

     > [!Note]  
     > À compter de Configuration Manager version 1802, la fonctionnalité CEIP ne figure plus dans le produit.  


-   [Forum aux questions sur les données de diagnostic et d’utilisation](../../../core/understand/frequently-asked-questions-about-diagnostics-and-usage-data.md)  



## <a name="see-also"></a>Voir aussi  
 [À propos du point de connexion de service](../../../core/servers/deploy/configure/about-the-service-connection-point.md)
