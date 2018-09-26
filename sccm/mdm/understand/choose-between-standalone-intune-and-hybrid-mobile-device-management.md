---
title: Choisir entre Intune autonome et la gestion MDM hybride
titleSuffix: Configuration Manager
description: Choisissez de déployer la gestion des appareils mobiles hybride avec Intune et Configuration Manager ou d’exécuter Intune de façon autonome.
ms.date: 08/14/2018
ms.prod: configuration-manager
ms.technology: configmgr-hybrid
ms.topic: conceptual
ms.assetid: 73ff9bb9-e605-4b68-92a1-487684fed42d
author: aczechowski
ms.author: aaroncz
manager: dougeby
robots: noindex,nofollow
ms.openlocfilehash: 153c1208cef8a940cc06412322e8112d53d17e58
ms.sourcegitcommit: 98c3f7848dc9014de05541aefa09f36d49174784
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2018
ms.locfileid: "42584591"
---
# <a name="choose-between-microsoft-intune-standalone-and-hybrid-mdm-with-configuration-manager"></a>Choisir entre Microsoft Intune en mode autonome et la gestion hybride des appareils mobiles avec Configuration Manager

*S’applique à : System Center Configuration Manager (Current Branch)*

L’une des questions les plus fréquentes relatives à la gestion des appareils mobiles avec Microsoft Intune est la suivante : « Dois-je intégrer Intune à Configuration Manager (gestion des appareils mobiles hybride) ou exécuter Intune autonome dans la configuration cloud ? ». 

Intune sur Azure est la solution MDM recommandée de Microsoft.     


> [!Important]  
> Depuis le 14 août 2018, la gestion hybride des appareils mobiles est une [fonctionnalité déconseillée](/sccm/core/plan-design/changes/deprecated/removed-and-deprecated-cmfeatures). Pour plus d’informations, consultez [Qu’est-ce que la gestion hybride des appareils mobiles ?](/sccm/mdm/understand/hybrid-mobile-device-management).<!--Intune feature 2683117-->  


 
## <a name="intune-standalone"></a>Intune autonome

Intune autonome est la topologie de déploiement recommandée par Microsoft. Intune autonome est une solution cloud de gestion des appareils mobiles qui est gérée à l’aide d’une console web accessible n’importe où dans le monde. Les centres de données Intune sont hébergés en Amérique du Nord, en Europe et en Asie. Intune étant un service cloud, vous pouvez déployer rapidement la gestion Intune sur vos appareils.

Il est généralement plus rapide et plus facile pour les clients de déployer la topologie autonome, car il n’existe aucune dépendance pour les composants locaux. Intune autonome est désormais disponible sur la plateforme cloud de Microsoft Azure et fournit de nombreuses fonctionnalités avancées, telles que :  

- Plateforme de gestion Enterprise Mobility intégrée : plateforme cloud avec expérience administrateur intégrée dans le portail Azure pour Intune, Azure AD Premium et Azure Information Protection  

- Gestion des appareils mobiles : fonctionnalités riches de protection des informations et de gestion des appareils mobiles  

- Mise à l’échelle : déployez et gérez des appareils mobiles sans vous préoccuper de la mise à l’échelle  

- Contrôle d’accès basé sur les rôles : restriction de l’accès aux fonctions d’administration en fonction des rôles affectés et des étendues  

- Accès par programmation (API) : prise en charge de l’API Microsoft Graph, options de gestion SDK et PowerShell  

- Console Web : console HTML 5 reposant sur des normes web prenant en charge la plupart des navigateurs web les plus récents  

- Création de rapports avancée : fonctionnalité permettant de créer des rapports personnalisés  

- Agilité : installation simple et livraison rapide de nouvelles fonctionnalités  



## <a name="hybrid-mdm-with-configuration-manager"></a>Gestion des périphériques mobiles (GPM) hybride avec Configuration Manager

> [!Important]  
> Depuis le 14 août 2018, la gestion hybride des appareils mobiles est une [fonctionnalité déconseillée](/sccm/core/plan-design/changes/deprecated/removed-and-deprecated-cmfeatures). Pour plus d’informations, consultez [Qu’est-ce que la gestion hybride des appareils mobiles ?](/sccm/mdm/understand/hybrid-mobile-device-management)  

La gestion des périphériques mobiles (GPM) hybride est une solution qui intègre les fonctionnalités de gestion des périphériques mobiles d’Intune à Configuration Manager. Elle utilise Intune comme canal de remise des stratégies, profils et applications aux appareils. En revanche, elle utilise l’infrastructure locale de Configuration Manager pour administrer le contenu et gérer les appareils. Une implémentation hybride vous offre un « contrôle unifié ». Ce qui signifie que vous pouvez utiliser la même infrastructure locale et la même console d’administration pour gérer d’une part des appareils mobiles avec Intune et, d’autre part, des PC et des serveurs avec le client Configuration Manager traditionnel. 

Vous pouvez choisir la gestion des périphériques mobiles (GPM) hybride pour les raisons suivantes :  

- Vous voulez gérer les appareils mobiles inscrits dans Intune et les appareils gérés avec le client Configuration Manager à partir de la même console d’administration  

- Votre infrastructure nécessite que vous disposiez de plusieurs serveurs NDES pour la remise de certificat aux appareils mobiles  

- Votre infrastructure nécessite que vous disposiez de plusieurs connecteurs Exchange Server  

- Vous avez besoin de la prise en charge du chiffrement S/MIME

> [!Note]  
> Si vous installez la gestion hybride des appareils mobiles dans Configuration Manager pour un accès conditionnel avec Exchange sur site, les utilisateurs peuvent toujours accéder aux e-mails dans Outlook pour iOS et Android. Cette même configuration avec Intune autonome bloque les e-mails de ces clients.<!--Intune bug 2285890-->  



## <a name="change-the-mdm-authority"></a>Modifier l’autorité de gestion des appareils mobiles

Si vous voulez modifier le paramètre d’autorité de gestion des périphériques mobiles, vous pouvez le faire sans avoir à contacter le Support Microsoft et sans devoir annuler l’inscription de vos appareils gérés existants et les réinscrire. Pour plus d’informations, consultez [Changer d’autorité MDM](/sccm/mdm/deploy-use/change-mdm-authority).

