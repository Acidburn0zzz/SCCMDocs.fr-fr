---
title: Fonctionnalités dépréciées
titleSuffix: Configuration Manager
description: Découvrez les fonctionnalités que System Center Configuration Manager ne prend plus en charge.
ms.date: 05/01/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
ms.assetid: 287a6324-ae65-4d38-b2ef-198d47c91231
author: aczechowski
ms.author: aaroncz
manager: dougeby
ms.openlocfilehash: 967c0ff71af5b3586568bf3f5d2fee7ed5b8bb06
ms.sourcegitcommit: 0b0c2735c4ed822731ae069b4cc1380e89e78933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32337732"
---
# <a name="removed-and-deprecated-features-for-system-center-configuration-manager"></a>Fonctionnalités supprimées et déconseillées dans System Center Configuration Manager

*S’applique à : System Center Configuration Manager (Current Branch)*

Cet article liste les fonctionnalités dépréciées ou supprimées du support de Configuration Manager. Les fonctionnalités dépréciées seront supprimées dans une prochaine mise à jour. Ces futurs changements risquent d’affecter votre utilisation de Configuration Manager.  

Ces informations sont susceptibles de changer dans les futures versions. Les fonctionnalités Configuration Manager dépréciées ne sont peut-être pas toutes listées ici.



## <a name="deprecated-features"></a>Fonctionnalités dépréciées  

|Fonctionnalité|Dépréciation annoncée|Prise en charge&nbsp;supprimée|  
|-----------|---|--------------|  
|Les applications à la disposition des utilisateurs qui figuraient uniquement dans le catalogue d’applications apparaissent maintenant dans le nouveau Centre logiciel. </br></br>Par conséquent, l’expérience de catalogue d’applications web ne sera pas disponible dans les prochains mois.|11 août 2017| Fin de la prise en charge de l’expérience utilisateur du site web du catalogue d’applications avec la première mise à jour publiée après le 1er juin 2018|
|Ancienne version du Centre logiciel.<br><br>Pour plus d’informations sur le nouveau Centre logiciel, consultez [Planifier et configurer la gestion des applications](/sccm/apps/plan-design/plan-for-and-configure-application-management#configure-software-center-and-the-application-catalog-windows-pcs-only).|13 décembre 2016|Version 1802|
|Gestion de disques durs virtuels avec Configuration Manager. </br></br>Cette dépréciation inclut la suppression des options permettant de créer un nouveau disque dur virtuel ou de gérer un disque dur virtuel à l’aide d’une séquence de tâches, ainsi que la suppression du nœud Disques durs virtuels dans la console Configuration Manager. </br></br>Les disques durs virtuels existants ne sont pas supprimés, mais ne sont plus accessibles à partir de la console Configuration Manager.  |6 janvier 2017 |Version 1710|
|Séquences de tâches : <br /> - Convertir en disque dynamique <br /> - Installer les outils de déploiement |18 novembre 2016|Version 1710|
|Outil d'évaluation de mise à niveau System Center Configuration Manager. </br></br>L’outil d’évaluation de mise à niveau dépend à la fois de System Center Configuration Manager et des outils d'analyse de compatibilité des applications (ACT) 6.x. La dernière version d’ACT a été intégrée à Windows 10 v1511 ADK. Comme il n’y a plus aucune mise à jour d’ACT, la prise en charge de l’outil d’évaluation de mise à niveau prend fin. </br></br>L’outil d’évaluation de mise à niveau est remplacé par la fonctionnalité [Disponibilité pour la mise à niveau](/sccm/core/clients/manage/upgrade/upgrade-analytics). Une note de dépréciation a été ajoutée à la [page de téléchargement UAT](https://www.microsoft.com/download/details.aspx?id=37145) le 12 septembre 2016. | 12 septembre 2016  | 11 juillet 2017 |
|Séquences de tâches : <br /> - OSDPreserveDriveLetter  <br /><br /> Lors d’un déploiement de système d’exploitation, par défaut, le programme d’installation Windows détermine désormais la meilleure lettre de lecteur à utiliser (généralement C:). Si vous souhaitez spécifier un autre lecteur à utiliser, vous pouvez modifier l’emplacement dans l’étape de séquence de tâches Appliquer le système d’exploitation. Accédez au paramètre **Sélectionnez l’emplacement où vous souhaitez appliquer ce système d'exploitation**. Sélectionnez **Lettre de lecteur logique spécifique** et choisissez le lecteur que vous souhaitez utiliser. |20 juin 2016 |Version 1606 |
|Protection d’accès réseau (NAP) : telle que dans System Center 2012 Configuration Manager|10 juillet 2015|Version 1511|  
|Gestion hors bande : telle que dans System Center 2012 Configuration Manager|16 octobre 2015|Version 1511|



## <a name="features-removed-in-version-1511"></a>Fonctionnalités supprimées dans la version 1511
Les sections suivantes contiennent des détails supplémentaires sur les fonctionnalités supprimées avec la version 1511 :

###  <a name="bkmk_amt"></a> Gestion hors bande  
 Avec Configuration Manager, la prise en charge native des ordinateurs AMT à partir de la console Configuration Manager est supprimée.  

-   Les ordinateurs AMT restent entièrement gérés quand vous utilisez le [module complémentaire Intel SCS pour Microsoft System Center Configuration Manager](http://www.intel.com/content/www/us/en/software/setup-configuration-software.html). Ce module complémentaire vous permet d’accéder aux dernières fonctionnalités permettant de gérer AMT tout en supprimant les limitations introduites jusqu’à ce que Configuration Manager puisse intégrer ces changements.  

-   La gestion hors bande dans System Center 2012 Configuration Manager n’est pas affectée par cette modification.  

###  <a name="bkmk_nap"></a> Protection d’accès au réseau  
 System Center Configuration Manager ne prend pas en charge la protection d’accès réseau. La fonctionnalité est dépréciée dans Windows Server 2012 R2 et a été supprimée dans Windows 10.  

 Pour les solutions de protection d'accès réseau, consultez la section *Fonctionnalités déconseillées* dans [Vue d'ensemble des services de stratégie et d'accès réseau](https://technet.microsoft.com/library/hh831683.aspx).



## <a name="more-information"></a>Plus d'informations
Pour plus d'informations, voir :
 - [Supprimé et déprécié](/sccm/core/plan-design/changes/deprecated/removed-and-deprecated)
 - [Politique de support Microsoft](https://support.microsoft.com/lifecycle)
 - [Prise en charge des versions Current Branch de System Center Configuration Manager](/sccm/core/servers/manage/current-branch-versions-supported).
