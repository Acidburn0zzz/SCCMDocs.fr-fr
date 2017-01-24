---
title: Configurer un abonnement Intune | Microsoft Docs | Local
description: Configurez un abonnement Intune pour assurer le suivi des licences dans le cadre de la gestion des appareils mobiles locale dans System Center Configuration Manager.
ms.custom: na
ms.date: 11/18/2016
ms.prod: configuration-manager
ms.reviewer: na
ms.suite: na
ms.technology:
- configmgr-client
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: 1e42b1c1-3d58-481f-8647-5c7ae640c5f5
caps.latest.revision: 8
caps.handback.revision: 0
author: Mtillman
ms.author: mtillman
manager: angrobe
translationtype: Human Translation
ms.sourcegitcommit: 828e2ac9a3f9bcea1571d24145a1021fdf1091f3
ms.openlocfilehash: 2cc9f59d9d32d149aa477ba61afba0094f302fc4


---
# <a name="set-up-a-microsoft-intune-subscription-for-on-premises-mobile-device-management-in-system-center-configuration-manager"></a>Configurer un abonnement Microsoft Intune pour la gestion des appareils mobiles locale dans System Center Configuration Manager

*S’applique à : System Center Configuration Manager (Current Branch)*

La gestion des appareils mobiles locale dans System Center Configuration Manager nécessite un abonnement Microsoft Intune pour assurer le suivi des licences. Le service Intune ne permet pas de gérer les appareils ni de stocker des informations de gestion. Pour assurer une gestion locale de tous les appareils mobiles, vous devez vous appuyer sur l’infrastructure Configuration Manager.  

> [!NOTE]  
> À compter de la version 1610, Configuration Manager prend en charge l’utilisation simultanée de Microsoft Intune et de l’infrastructure Configuration Manager locale pour gérer les appareils mobiles.   

> [!TIP]  
>  Nous vous recommandons de configurer l’abonnement Intune pour la gestion des appareils mobiles locale avant d’installer les rôles de système de site nécessaires. Ainsi, les rôles de système de site nouvellement installés seront plus vite opérationnels.  

##  <a name="sign-up-for-microsoft-intune"></a>S’inscrire à Microsoft Intune  
 Intune est nécessaire pour que la gestion des appareils mobiles locale fonctionne. Il vous suffit de [souscrire](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/) un abonnement d’évaluation ou payant et de passer à l’étape suivante pour ajouter l’abonnement à Configuration Manager.  

##  <a name="add-the-intune-subscription-to-configuration-manager"></a>Ajouter l’abonnement Intune à Configuration Manager  
 Pour ajouter l’abonnement à Configuration Manager, vous devez suivre les mêmes étapes de base que la procédure d’ajout d’un abonnement pour la gestion des appareils mobiles avec Intune. Lisez les remarques ci-dessous qui décrivent les différences spécifiques, puis suivez les instructions fournies dans [Pour créer l’abonnement Microsoft Intune](../deploy-use/setup-hybrid-mdm.md#step-3-configure-intune-subscription).  

> [!NOTE]  
>  Au moment d’ajouter l’abonnement Intune, gardez à l’esprit les points suivants :  
>   
>  -   Le regroupement spécifié dans l’Assistant Ajouter un abonnement Microsoft Intune n’est pas utilisé pour la délégation des droits d’utilisateur de la gestion des appareils mobiles locale. Il est utilisé uniquement pour la gestion des appareils mobiles avec Intune. Toutefois, vous devez spécifier un regroupement pour que l’Assistant continue.  
> -   Le paramètre de code de site spécifié dans l’Assistant est ignoré pour la gestion des appareils mobiles locale. Le code de site utilisé est celui que vous spécifiez dans le profil d’inscription qui autorise les utilisateurs à inscrire des appareils.  
> -   N’activez pas l’authentification multifacteur. Elle n’est pas activée dans la gestion des appareils mobiles locale.  

##  <a name="configure-the-intune-subscription-for-on-premises-mobile-device-management"></a>Configurer l’abonnement Intune pour la Gestion locale des appareils mobiles  

1.  Dans la console Configuration Manager, cliquez avec le bouton droit sur **Abonnement à Microsoft Intune**, puis cliquez sur **Propriétés**.  

2.  Dans la zone Gestion des appareils mobiles locale, choisissez l’une des options suivantes :

  - Si vous prévoyez d’avoir uniquement des appareils gérés localement, cochez la case en regard de **Gérer uniquement les appareils locaux**, puis cliquez sur **OK**.  

      > [!NOTE]  
      >  En cochant cette case, vous configurez l’abonnement Intune de sorte que toutes les informations de gestion soient conservées localement et que les données ne soient pas répliquées dans le cloud.  

    - Si vous prévoyez d’avoir des appareils gérés à la fois par Intune et Configuration Manager au niveau local, ne cochez pas la case.

3.  Si vous prévoyez de gérer des appareils Windows 10 Mobile, cliquez sur **Abonnement à Microsoft Intune**, sur **Configurer des plateformes**, puis sur  **Windows Phone**.  

4.  Cochez la case en regard de **Windows Phone 8.1 et Windows 10 Mobile**, puis cliquez sur **OK**.  

5.  Si vous prévoyez de gérer des ordinateurs de bureau Windows 10, cliquez sur **Abonnement à Microsoft Intune**, sur **Configurer des plateformes**, puis sur **Activer l’inscription Windows**.  

6.  Cochez la case en regard de **Activer l’inscription Windows**, puis cliquez sur **OK**.  



<!--HONumber=Dec16_HO3-->


