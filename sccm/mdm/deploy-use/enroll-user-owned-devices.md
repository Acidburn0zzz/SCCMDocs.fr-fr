---
title: Inscrire des appareils appartenant aux utilisateurs pour les déploiements hybride
titleSuffix: Configuration Manager
description: Découvrez les différentes méthodes d’inscription des appareils appartenant aux utilisateurs pour les déploiements hybrides avec Configuration Manager.
ms.date: 09/08/2017
ms.prod: configuration-manager
ms.technology: configmgr-hybrid
ms.topic: conceptual
ms.assetid: 2bdaa8a7-6a64-4b0e-b617-309dcd912c45
author: aczechowski
ms.author: aaroncz
manager: dougeby
ms.openlocfilehash: 198e5b65b85e10a1aa64f06361f1ba425e156662
ms.sourcegitcommit: 0b0c2735c4ed822731ae069b4cc1380e89e78933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32345719"
---
# <a name="enroll-user-owned-devices-for-hybrid-deployments-with-configuration-manager"></a>Inscrire des appareils appartenant aux utilisateurs pour les déploiements hybrides avec Configuration Manager

*S’applique à : System Center Configuration Manager (Current Branch)*

Les appareils appartenant à l’utilisateur peuvent être soumis à la gestion en les inscrivant, un processus souvent appelé « BYOD » ou « Apportez votre propre appareil ». Les utilisateurs effectuent ceci en installant l’application Portail d’entreprise et en se connectant sur l’appareil (iOS, Mac OS et Android), ou en ajoutant un compte professionnel ou scolaire à l’appareil et en se joignant à un domaine (Windows). Ce processus inscrit l’appareil auprès d’Intune, ce qui donne à l’utilisateur l’accès aux ressources gérées par Intune et laisse Intune gérer certains paramètres de l’appareil, comme demander un code PIN.

Pour soumettre des appareils à la gestion, vous devez d’abord, en tant qu’administrateur, [configurer la gestion des appareils mobiles](setup-hybrid-mdm.md) et [activer l’inscription](enable-platform-enrollment.md). Une fois l’inscription activée, les utilisateurs peuvent inscrire leurs propres appareils. Consultez [Guide pratique pour informer vos utilisateurs finaux sur Microsoft Intune](https://docs.microsoft.com/intune/end-user-educate) pour des considérations et des procédures à partager avec vos utilisateurs.

Les entreprises ou les établissements scolaires qui achètent des appareils peuvent bénéficier de programmes qui vous permettent de [gérer des appareils d’entreprise](enroll-company-owned-devices.md).
