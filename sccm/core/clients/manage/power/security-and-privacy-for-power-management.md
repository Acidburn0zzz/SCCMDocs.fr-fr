---
title: Sécurité et confidentialité pour la gestion de l’alimentation
titleSuffix: Configuration Manager
description: Obtenir des informations de sécurité et de confidentialité pour la gestion de l’alimentation dans System Center Configuration Manager.
ms.date: 04/23/2017
ms.prod: configuration-manager
ms.technology: configmgr-client
ms.topic: conceptual
ms.assetid: 469ff35f-59a1-484d-902b-107dd6070baf
author: aczechowski
manager: dougeby
ms.author: aaroncz
ms.openlocfilehash: 47ddbf358426b7683dab42b4f7a6a89ad8e631de
ms.sourcegitcommit: 0b0c2735c4ed822731ae069b4cc1380e89e78933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32332785"
---
# <a name="security-and-privacy-for-power-management-in-system-center-configuration-manager"></a>Sécurité et confidentialité pour la gestion de l’alimentation dans System Center Configuration Manager

*S’applique à : System Center Configuration Manager (Current Branch)*

Cette section contient des informations de sécurité et de confidentialité pour la gestion de l’alimentation dans System Center Configuration Manager.  

## <a name="security-best-practices-for-power-management"></a>Meilleures pratiques de sécurité pour la gestion de l’alimentation  
 Il n'existe aucune meilleure pratique liée à la sécurité pour la gestion de l'alimentation.  

## <a name="privacy-information-for-power-management"></a>Informations de confidentialité pour la gestion de l’alimentation  
 Gestion de l'alimentation utilise des fonctionnalités qui sont intégrées à Windows pour surveiller la consommation d'énergie et pour appliquer les paramètres d'alimentation aux ordinateurs pendant les heures de bureau et les heures creuses. Configuration Manager collecte des informations sur la consommation d’énergie auprès des ordinateurs, incluant des données sur périodes d’utilisation des ordinateurs par les utilisateurs. Bien que Configuration Manager surveille la consommation d’énergie pour un regroupement plutôt que pour chaque ordinateur, un regroupement peut contenir un seul ordinateur. La gestion de l'alimentation n'est pas activée par défaut et doit être configurée par un administrateur.  

 Les informations sur la consommation d’énergie sont stockées dans la base de données Configuration Manager et ne sont pas envoyées à Microsoft. Les informations détaillées sont conservées dans la base de données pendant 31 jours et les informations résumées sont conservées pendant 13 mois. Vous ne pouvez pas configurer l'intervalle de suppression.  

 Avant de configurer la gestion de l'alimentation, pensez à vos besoins en matière de confidentialité.  
