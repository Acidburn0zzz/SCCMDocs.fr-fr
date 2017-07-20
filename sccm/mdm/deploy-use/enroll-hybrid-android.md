---
title: Configurer la gestion des appareils mobiles hybride Android avec System Center Configuration Manager et Microsoft Intune | Microsoft Docs
description: "Préparez la gestion des appareils mobiles Android avec Configuration Manager et Intune."
ms.custom: na
ms.date: 03/27/2017
ms.prod: configuration-manager
ms.reviewer: na
ms.suite: na
ms.technology:
- configmgr-hybrid
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: c517fe34-0130-465b-a020-bdb555878778
caps.latest.revision: 9
caps.handback.revision: 0
author: nathbarn
ms.author: nathbarn
manager: angrobe
ms.translationtype: Human Translation
ms.sourcegitcommit: 86620254897aa9a775dc433de7010b5814c1ec3e
ms.openlocfilehash: af6fa2dfae5549e89c46d05d0cef1e24342558f9
ms.contentlocale: fr-fr
ms.lasthandoff: 07/06/2017


---
# <a name="set-up-android-hybrid-device-management-with-system-center-configuration-manager-and-microsoft-intune"></a>Configurer la gestion hybride des appareils mobiles Android avec System Center Configuration Manager et Microsoft Intune

*S’applique à : System Center Configuration Manager (Current Branch)*

Cette rubrique aide l’administrateur informatique à activer l’inscription hybride des appareils Android et Android for Work. L’administrateur informatique peut ensuite utiliser System Center Configuration Manager pour gérer les appareils dans le cadre d’un abonnement Microsoft Intune configuré. À partir de Google Play, les utilisateurs peuvent télécharger l’application de portail d’entreprise Android qui leur permet d’inscrire des appareils Android (notamment Samsung KNOX Standard) et Android for Work.

En tant qu’administrateur de Configuration Manager, vous pouvez gérer les paramètres de conformité, réinitialiser ou supprimer des appareils Android, déployer des applications et collecter l’inventaire matériel et logiciel. Sans l’application de portail d’entreprise Android installée sur l’appareil, vous ne disposez pas des fonctions de gestion (telles que les paramètres de conformité et d’inventaire), mais vous pouvez quand même déployer des applications sur des appareils Android.  

## <a name="enable-android-enrollment"></a>Activer l’inscription Android  
Les étapes suivantes permettent à Configuration Manager de gérer des appareils Android sans profil professionnel (autrement dit, par une inscription « Android classique »).

1. Avant de pouvoir configurer l’inscription pour une plateforme, tenez compte des prérequis et effectuez les procédures décrites dans [Configurer la gestion hybride des appareils mobiles](setup-hybrid-mdm.md).  
2. Dans la console Configuration Manager, dans l’espace de travail **Administration**, choisissez **Vue d’ensemble** > **Services cloud** > **Abonnements Microsoft Intune**, puis choisissez votre abonnement Intune.  
3. Sous l’onglet **Accueil**, dans le groupe **Abonnement** , choisissez **Configurer des plateformes** > **Android**.  
4. Dans la boîte de dialogue **Propriétés d’abonnement Microsoft Intune**, choisissez l’onglet **Android** et cochez la case **Activer l’inscription Android** .  

 Une fois la configuration terminée, vous devez indiquer aux utilisateurs comment inscrire leurs appareils. Consultez [Ce qu’il faut dire aux utilisateurs sur l’inscription de leurs appareils](https://docs.microsoft.com/intune/deploy-use/what-to-tell-your-end-users-about-using-microsoft-intune). Ces informations s’appliquent aux appareils mobiles gérés par Microsoft Intune et Configuration Manager.

## <a name="enable-android-for-work-enrollment"></a>Activer l’inscription Android for Work
Les étapes suivantes permettent à Configuration Manager de gérer des appareils Android avec un profil professionnel.

1. Créez un compte Google sur https://accounts.google.com/SignUp, que vous utiliserez comme compte d’administrateur Android for Work. Ou bien connectez-vous avec le compte associé à toutes les tâches de gestion Android for Work pour ce client Intune. Ce compte Google peut être partagé par les administrateurs qui gèrent des appareils Android. Il s’agit du compte Google utilisé par votre organisation pour gérer et publier des applications dans la console Play for Work. Vous utilisez ce compte pour approuver les applications dans le magasin Play for Work. Veillez donc à prendre note du nom du compte et du mot de passe.
2. Activez l’inscription Android en liant le compte Google au client Intune géré dans Configuration Manager :
   1. Dans la console Configuration Manager, dans l’espace de travail **Administration**, choisissez **Vue d’ensemble** > **Services cloud** > **Abonnements Microsoft Intune**, puis choisissez votre abonnement Intune.
   2. Sous l’onglet **Accueil**, dans le groupe **Abonnement**, choisissez **Configurer des plateformes** > **Android for Work**.
   3. Dans la boîte de dialogue, choisissez **Configurer Android for Work dans la console Intune**. La console Intune s’ouvre dans votre navigateur web.
   4. Utilisez vos informations d’identification d’administrateur Intune pour vous connecter au portail Intune.
   5. Choisissez **Configurer** pour ouvrir le site web Android for Work de Google Play.
   6. Dans la page de connexion de Google, entrez les informations d’identification du compte Google de l’étape 1, puis fournissez les informations relatives à votre société.
3. Quand vous revenez au portail Intune, Android for Work est activé et vous avez trois options d’inscription pour les appareils Android for Work :
   - **Gérer tous les appareils comme Android** (désactivé). Tous les appareils Android, notamment ceux qui prennent en charge Android for Work, sont inscrits comme appareils Android conventionnels.
   - **Gérer les appareils pris en charge comme Android for Work** (activé). Tous les appareils qui prennent en charge Android for Work sont inscrits comme appareils Android for Work. Tout appareil Android qui ne prend pas en charge Android for Work est inscrit comme appareil Android conventionnel.
   - **Gérer les appareils pris en charge pour les utilisateurs uniquement dans ces groupes comme Android for Work** (activé pour certains groupes uniquement). Vous permet de cibler la gestion Android for Work sur un ensemble limité d’utilisateurs. Les appareils qui prennent en charge Android for Work sont inscrits comme appareils Android for Work uniquement quand des membres des groupes sélectionnés les inscrivent. Tous les autres appareils sont inscrits comme appareils Android.

> [!NOTE]
> Un problème connu empêche le bon fonctionnement de l’option **Gérer les appareils pris en charge pour les utilisateurs uniquement dans ces groupes comme Android for Work**. Les appareils des utilisateurs dans les groupes Azure AD spécifiés sont inscrits en tant qu’appareils Android et non Android for Work. Pour activer Android for Work, vous devez utiliser l’option **Gérer les appareils pris en charge comme Android for Work**.


Une fois la configuration terminée, vous devez indiquer aux utilisateurs comment inscrire leurs appareils. Consultez [Ce qu’il faut dire aux utilisateurs sur l’inscription de leurs appareils](https://docs.microsoft.com/intune/deploy-use/what-to-tell-your-end-users-about-using-microsoft-intune). Ces informations s’appliquent aux appareils mobiles gérés par Microsoft Intune et Configuration Manager.

Lorsque la liaison est établie, vous voyez le nom du compte et le nom de l’organisation dans le portail Intune. À ce stade, vous pouvez fermer les deux navigateurs.

### <a name="enroll-an-android-for-work-device"></a>Inscrire un appareil Android for Work
L’inscription des appareils Android for Work par vos utilisateurs est similaire à celles des appareils Android. Les utilisateurs peuvent télécharger et installer l’application Portail d’entreprise pour Android sur leurs appareils mobiles. L’application les invite à créer un profil professionnel dans le cadre du processus d’inscription. Une fois le profil professionnel créé, les utilisateurs doivent basculer vers la version gérée du portail d’entreprise. Le portail d’entreprise géré est marqué d’un petit porte-documents orange dans le coin inférieur droit.

### <a name="manage-android-for-work-devices"></a>Gérer des appareils Android for Work
Après avoir activé l’inscription Android for Work, vous pouvez effectuer les tâches de gestion suivantes pour les appareils Android for Work :
- [Approuver les applications](/sccm/mdm/deploy-use/creating-android-applications#approve-and-deploy-android-for-work-apps)
- [Créer des éléments de configuration](/sccm/mdm/deploy-use/create-configuration-items-for-android-for-work-devices-managed-without-the-client)
- [Gérer les paramètres de conformité](/sccm/mdm/deploy-use/create-configuration-items-for-android-for-work-devices-managed-without-the-client)
- [Gérer les profils de messagerie](/sccm/mdm/deploy-use/create-exchange-activesync-profiles)
- [Réinitialiser de façon sélective le profil professionnel](/sccm/mdm/deploy-use/wipe-lock-reset-devices#selective-wipe)

> [!div class="button"]
[< Étape précédente](create-service-connection-point.md) [Étape suivante >](set-up-additional-management.md)

