---
title: Clients et appareils pris en charge
titleSuffix: Configuration Manager
description: Découvrez les versions de système d’exploitation que Configuration Manager prend en charge pour les clients et les appareils.
ms.date: 08/21/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
ms.assetid: 87f4e041-67df-4c61-aa98-7444faffe565
author: aczechowski
ms.author: aaroncz
manager: dougeby
ms.openlocfilehash: 8abe612272dd8a48a23ffdcb945aa7b6766afdb9
ms.sourcegitcommit: 7eebd112a9862bf98359c1914bb0c86affc5dbc0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42586400"
---
# <a name="supported-os-versions-for-clients-and-devices-for-configuration-manager"></a>Versions de système d’exploitation prises en charge par Configuration Manager pour les clients et les appareils

*S’applique à : System Center Configuration Manager (Current Branch)*

 Configuration Manager prend en charge l’installation de logiciels clients sur des ordinateurs Windows, Mac, Linux et UNIX.  

#### <a name="requirements-and-limitations-for-all-clients"></a>Conditions requises et limitations pour tous les clients  

-   Vous ne pouvez pas modifier le type de démarrage ou les paramètres **d’ouverture de session** pour un service Configuration Manager. Cette modification peut empêcher l’exécution correcte de certains services clés.    

-   L’installation ou l’exécution du client Configuration Manager pour Linux ou UNIX, ou du client pour Mac sur des ordinateurs sous un autre compte que le compte racine n’est pas prise en charge. Cela peut empêcher l’exécution correcte de certains services clés.  



##  <a name="windows-computers"></a>Ordinateurs Windows  

 Utilisez le client fourni avec Configuration Manager pour gérer les versions de système d’exploitation Windows suivantes. Pour plus d’informations, consultez [Comment déployer des clients sur des ordinateurs Windows](/sccm/core/clients/deploy/deploy-clients-to-windows-computers).  


### <a name="supported-os-versions"></a>Versions du système d'exploitation prises en charge  

-  **Windows Server 2016** : Standard, Datacenter <sup>[Remarque 1](#bkmk_note1)</sup>  

-   **Windows Storage Server 2016** : Workgroup, Standard  

-   **Windows Server 2012 R2** (x64) : Standard, Datacenter <sup>[Remarque 1](#bkmk_note1)</sup>    

-   **Windows Storage Server 2012 R2** (x64)    

-   **Windows Server 2012** (x64) : Standard, Datacenter <sup>[Remarque 1](#bkmk_note1)</sup>    

-   **Windows Storage Server 2012** (x64)    

-   **Windows Server 2008 R2 with SP1** (x64) : Standard, Enterprise, Datacenter <sup>[Remarque 1](#bkmk_note1)</sup>    

-   **Windows Storage Server 2008 R2** (x86, x64) : Workgroup, Standard, Enterprise    

-   **Windows Server 2008 with SP2** (x86, x64) : Standard, Enterprise, Datacenter <sup>[Remarque 1](#bkmk_note1)</sup>    

-   **Windows 10**  

    Pour plus d’informations sur les différentes versions commerciales de Windows 10 qui sont prises en charge par les différentes versions de Configuration Manager, consultez [Prise en charge des versions de Windows 10](/sccm/core/plan-design/configs/support-for-windows-10).  

-   **Windows 8.1** (x86, x64) : Professionnel, Entreprise    

-   **Windows 7 avec SP1** (x86, x64) : Professionnel, Entreprise et Édition Intégrale    

-   **Installation minimale de Windows Server, version 1709** (x64) <sup>[Remarque 2](#bkmk_note2)</sup> <sup>[Remarque 3](#bkmk_note3)</sup>  
    Cette version du système d’exploitation est prise en charge à compter de Configuration Manager version 1710.  

-   **Installation minimale de Windows Server 2016** (x64) <sup>[Remarque 2](#bkmk_note2)</sup> <sup>[Remarque 3](#bkmk_note3)</sup>  

-   **Installation minimale de Windows Server 2012 R2** (x64) <sup>[Remarque 2](#bkmk_note2)</sup> <sup>[Remarque 3](#bkmk_note3)</sup>    

-   **Installation minimale de Windows Server 2012** (x64) <sup>[Remarque 2](#bkmk_note2)</sup> <sup>[Remarque 3](#bkmk_note3)</sup>    

-   **Installation minimale de Windows Server 2008 R2** (sans Service Pack, ou avec SP1) (x64) <sup>[Remarque 3](#bkmk_note3)</sup>    

-   **Installation minimale de Windows Server 2008 SP2** (x86, x64) <sup>[Remarque 3](#bkmk_note3)</sup>  

#### <a name="bkmk_note1"></a> Remarque 1
 Les versions Datacenter sont prises en charge, mais ne sont pas certifiées pour Configuration Manager. Les correctifs ne sont pas pris en charge pour résoudre les problèmes spécifiques de l’édition Windows Server Datacenter.  

#### <a name="bkmk_note2"></a> Remarque 2
 Pour prendre en charge l’installation Push du client, l’ordinateur exécutant cette version du système d’exploitation doit exécuter le service de rôle Serveur de fichiers pour le rôle serveur Services de fichiers et de stockage. Pour plus d’informations sur l’installation des fonctionnalités Windows sur un ordinateur Server Core, consultez [Installer des rôles, des services de rôle et des fonctionnalités à l’aide des applets de commande Windows PowerShell](https://docs.microsoft.com/windows-server/administration/server-manager/install-or-uninstall-roles-role-services-or-features#BKMK_installwps).  

#### <a name="bkmk_note3"></a> Remarque 3
 La nouvelle application Centre logiciel n’est prise en charge sur aucune version de Windows Server Core.<!--SCCMDocs issue 683-->



##  <a name="windows-embedded-computers"></a>Ordinateurs Windows Embedded  

 Gérez les appareils Windows Embedded en installant le client Configuration Manager sur ceux-ci. Pour plus d’informations, consultez [Planification du déploiement de clients sur des appareils Windows Embedded](/sccm/core/clients/deploy/plan/planning-for-client-deployment-to-windows-embedded-devices).  


### <a name="requirements-and-limitations"></a>Conditions requises et limitations :

-   Toutes les fonctionnalités du client sont prises en charge sur les systèmes Windows Embedded qui ne disposent pas de filtres d’écriture activés.  

-   Les clients qui utilisent l’un des éléments suivants sont pris en charge pour toutes les fonctionnalités, à l’exception de la gestion de l’alimentation :  

    -   Filtres d’écriture améliorés (EWF)    

    -   Filtres d’écriture basés sur des fichiers RAM (FBWF)    

    -   Filtres d’écriture unifiés (UWF)  

-   Le catalogue d’applications n’est pris en charge pour aucun appareil Windows Embedded.  

-   Pour pouvoir surveiller les programmes malveillants détectés sur les appareils Windows Embedded basés sur Windows XP, vous devez installer le package de script Microsoft Windows WMI sur l’appareil. Utilisez Windows Embedded Target Designer pour installer ce package. Les fichiers **WBEMDISP.DLL** et **WBEMDISP.TLB** doivent exister et être inscrits dans le dossier **%windir%\System32\WBEM** sur l’appareil intégré pour garantir que les programmes malveillants sont signalés.  


### <a name="supported-os-versions"></a>Versions du système d'exploitation prises en charge  

-   **Windows 10 Entreprise** (x86, x64)  

-   **Windows 10 IoT Entreprise** (x86, x64)  
    Cette version inclut le canal de maintenance à long terme (LTSC). Pour plus d'informations, consultez [Présentation de Windows 10 IoT Enterprise](https://docs.microsoft.com/windows/iot-core/windows-iot-enterprise).<!--SCCMDocs issue 560-->  

-   **Windows Embedded 8.1 Industry** (x86, x64)    

-   **Windows Embedded 8 Standard** (x86, x64)    

-   **Windows Thin PC** (x86, x64)    

-   **Windows Embedded POSReady 7** (x86, x64)    

-   **Windows Embedded Standard 7 avec SP1** (x86, x64)    


### <a name="unsupported-os-versions"></a>Versions du système d'exploitation non prises en charge

Les versions de système d’exploitation suivantes sont basées sur Windows XP Embedded. A compter de la version 1702, ces versions de système d'exploitation incorporées ne sont pas prises en charge. Pour plus d’informations, consultez [Systèmes d’exploitation client dépréciés](/sccm/core/plan-design/changes/deprecated/removed-and-deprecated-client#deprecated-client-operating-systems).  

-   **WEPOS 1.1 avec SP3** (x86)    

-   **Windows Embedded POSReady 2009** (x86, x64)    

-   **Windows Fundamentals for Legacy PCs (WinFLP)** (x86)    

-   **Windows XP Embedded SP3** (x86)    

-   **Windows Embedded Standard 2009** (x86)  



## <a name="windows-ce-computers"></a>Ordinateurs Windows CE

 Gérez les appareils Windows CE avec le client hérité d’appareil mobile Configuration Manager inclus dans Configuration Manager.  


### <a name="requirements-and-limitations"></a>Conditions requises et limitations :  

-   L’installation du client d’appareil mobile nécessite 0,78 Mo d’espace de stockage. La connexion peut nécessiter jusqu’à 256 Ko d’espace de stockage supplémentaire.    

-   Les fonctionnalités de ces appareils mobiles varient selon la plateforme et le type de client. Pour plus d’informations sur les fonctions de gestion prises en charge, consultez [Choisir une solution de gestion d’appareils](/sccm/core/plan-design/choose-a-device-management-solution).  


### <a name="supported-os-versions"></a>Versions du système d'exploitation prises en charge  

-   Windows CE 7.0 (processeurs ARM et x86)  

#### <a name="supported-languages-include"></a>Langues prises en charge :

-   Chinois (simplifié et traditionnel)    

-   Anglais (États-Unis)    

-   Français (France)    

-   Allemand    

-   Italien    

-   Japonais  

-   Coréen  

-   Portugais (Brésil)  

-   Russe  

-   Espagnol (Espagne)  



## <a name="mac-computers"></a>Ordinateurs Mac  

 Gérez les ordinateurs macOS à l’aide du client Configuration Manager pour Mac.  

 Le package d’installation de client Mac n’est pas fourni avec le support d’installation de Configuration Manager. Téléchargez les **clients pour d’autres systèmes d’exploitation** à partir du [Centre de téléchargement Microsoft](http://go.microsoft.com/fwlink/?LinkID=525184).  

 Pour plus d'informations, consultez [Guide pratique pour déployer des clients sur des Mac](/sccm/core/clients/deploy/deploy-clients-to-macs).  


### <a name="supported-versions"></a>Versions prises en charge

-   **Mac OS X 10.6** (Snow Leopard)

-   **Mac OS X 10.7** (Lion)

-   **Mac OS X 10.8** (Mountain Lion)

-   **Mac OS X 10.9** (Mavericks)

-   **Mac OS X 10.10** (Yosemite)  

-   **Mac OS X 10.11** (El Capitan)  

-   **Mac OS X 10.12** (macOS Sierra)

-   **Mac OS X 10.13** (macOS High Sierra)



##  <a name="linux-and-unix-servers"></a>Serveurs Linux et UNIX  

> [!Important]  
> Depuis le 22 mars 2018, les clients Linux et UNIX pour Configuration Manager sont déconseillés. Pour plus d’informations, consultez [Annonce de la dépréciation de la prise en charge des clients Linux et Unix](/sccm/core/plan-design/changes/whats-new-in-version-1802#deprecation-announcement-for-linux-and-unix-client-support).  

 Gérez les serveurs Linux et UNIX avec le client Configuration Manager pour Linux et UNIX.  

 Les packages d’installation du client Linux et UNIX ne sont pas fournis avec le média Configuration Manager. Téléchargez les **clients pour d’autres systèmes d’exploitation** à partir du [Centre de téléchargement Microsoft](http://go.microsoft.com/fwlink/?LinkID=525184). En plus des packages d’installation de client, le téléchargement du client comprend le script qui gère l’installation du client sur chaque ordinateur.  


### <a name="requirements-and-limitations"></a>Conditions requises et limitations :

-   Pour vérifier les dépendances des fichiers du système d’exploitation pour le client pour Linux et UNIX, consultez [Conditions préalables pour le déploiement du client pour les serveurs Linux et UNIX](/sccm/core/clients/deploy/plan/planning-for-client-deployment-to-linux-and-unix-computers#BKMK_ClientDeployPrereqforLnU).  

-   Pour obtenir une vue d’ensemble des fonctionnalités de gestion prises en charge sur Linux ou UNIX, consultez [Guide pratique pour déployer des clients sur des serveurs UNIX et Linux](/sccm/core/clients/deploy/deploy-clients-to-unix-and-linux-servers).  

-   Pour versions prises en charge de Linux et UNIX, la version répertoriée inclut toutes les versions mineures suivantes. Par exemple, CentOS version 6 inclut CentOS 6.3. De même, la prise en charge d’un système d’exploitation qui utilise des Service Packs (comme SUSE Linux Enterprise Server 11 SP1), inclut les Service Packs suivants pour cette version du système d’exploitation.  

-   Pour plus d’informations sur les packages d’installation client et l’agent universel, consultez [Guide pratique pour déployer des clients sur des serveurs UNIX et Linux dans System Center Configuration Manager](/sccm/core/clients/deploy/deploy-clients-to-unix-and-linux-servers).  


### <a name="supported-versions"></a>Versions prises en charge

Les versions suivantes sont prises en charge à l’aide du fichier .tar indiqué.  

#### <a name="aix"></a>AIX  

|Version|Fichier TAR|  
|-|-|  
|Version 6.1 (Power)|ccm-Aix61ppc.&lt;version\>.tar|  
|Version 7.1 (Power)|ccm-Aix71ppc.&lt;version\>.tar|  

#### <a name="centos"></a>CentOS  

|Version|Fichier TAR|  
|-|-|  
|Version 5 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 5 x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 6 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 6 x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 7 x64|ccm-Universalx64.&lt;version\>.tar|  

#### <a name="debian"></a>Debian  

|Version|Fichier TAR|  
|-|-|  
|Version 5 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 5 x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 6 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 6 x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 7 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 7 x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 8 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 8 x64|ccm-Universalx64.&lt;version\>.tar|  

#### <a name="hp-ux"></a>HP-UX  

|Version|Fichier TAR|  
|-|-|  
|Version 11iv3 IA64|ccm-HpuxB.11.31i64.&lt;version\>.tar|  

#### <a name="oracle-linux"></a>Oracle Linux  

|Version|Fichier TAR|  
|-|-|  
|Version 5 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 5 x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 6 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 6 x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 7 x64|ccm-Universalx64.&lt;version\>.tar|  

#### <a name="red-hat-enterprise-linux-rhel"></a>Red Hat Enterprise Linux (RHEL)  

|Version|Fichier TAR|  
|-|-|  
|Version 5 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 5 x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 6 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 6 x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 7 x64|ccm-Universalx64.&lt;version\>.tar|  

#### <a name="solaris"></a>Solaris  

|Version|Fichier TAR|  
|-|-|  
|Version 10 x86|ccm-Sol10x86.&lt;version\>.tar|  
|SPARC version 10|ccm-Sol10sparc.&lt;version\>.tar|  
|Version 11 x86|ccm-Sol11x86.&lt;version\>.tar|  
|SPARC version 11|ccm-Sol11sparc.&lt;version\>.tar|  

#### <a name="suse-linux-enterprise-server-sles"></a>SUSE Linux Enterprise Server (SLES)  

|Version|Fichier TAR|  
|-|-|  
|Version 10 SP1 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 10 SP1 x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 11 SP1 x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 11 SP1 x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 12 x64|ccm-Universalx64.&lt;version\>.tar|  

#### <a name="ubuntu"></a>Ubuntu  

|Version|Fichier TAR|  
|-|-|  
|Version 10.04 LTS x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 10.04 LTS x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 12.04 LTS x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 12.04 LTS x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 14.04 LTS x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 14.04 LTS x64|ccm-Universalx64.&lt;version\>.tar|  
|Version 16.04 LTS x86|ccm-Universalx86.&lt;version\>.tar|  
|Version 16.04 LTS x64|ccm-Universalx64.&lt;version\>.tar|  



##  <a name="mobile-devices-enrolled-by-microsoft-intune"></a>Appareils mobiles inscrits par Microsoft Intune  

 Pour plus d’informations sur les ordinateurs et les appareils que vous pouvez gérer quand vous intégrez Microsoft Intune à Configuration Manager, consultez les deux articles suivants dans la bibliothèque de la documentation Microsoft Intune :  

-   [Fonctionnalités de gestion des appareils mobiles dans Microsoft Intune](https://docs.microsoft.com/intune/get-started/choose-how-to-manage-devices)  
-   [Fonctionnalités de gestion des PC Windows dans Microsoft Intune](https://docs.microsoft.com/intune/get-started/windows-pc-management-capabilities-in-microsoft-intune)  



##  <a name="bkmk_OnpremOS"></a> Gestion des appareils mobiles locale  

 Configuration Manager offre des fonctionnalités intégrées permettant de gérer des appareils locaux sans devoir installer de logiciel client. Pour plus d'informations, consultez [Gérer des appareils mobiles avec une infrastructure locale](/sccm/mdm/understand/manage-mobile-devices-with-on-premises-infrastructure).  


### <a name="requirements-and-limitations"></a>Conditions requises et limitations :

-   Configurez le **point de connexion de service** sur le site de plus haut niveau de votre hiérarchie.  


### <a name="supported-operating-systems"></a>Systèmes d'exploitation pris en charge

- **Windows 10 Professionnel** (x86, x64)  

- **Windows 10 Entreprise** (x86, x64)  

- **Windows 10 IoT Entreprise** (x86, x64)  
    Cette version inclut le canal de maintenance à long terme (LTSC). Pour plus d'informations, consultez [Présentation de Windows 10 IoT Enterprise](https://docs.microsoft.com/windows/iot-core/windows-iot-enterprise).<!--SCCMDocs issue 560-->  

- **Windows 10 Mobile**  

- **Windows 10 Mobile Entreprise**  

- **Windows 10 IoT Mobile Entreprise**  

- **Windows 10 Collaboration pour Surface Hub**  



##  <a name="bkmk_ExSrvConOS"></a> Connecteur Exchange Server  

Configuration Manager prend en charge une gestion limitée des appareils qui se connectent à Exchange Server, sans installation du client Configuration Manager. Pour plus d’informations, consultez [Gérer des appareils mobiles à l’aide de Configuration Manager et d’Exchange](/sccm/mdm/deploy-use/manage-mobile-devices-with-exchange-activesync).  


### <a name="supported-versions-of-exchange-server"></a>Versions d’Exchange Server prises en charge

-   **Exchange Server 2010 SP1**  

-   **Exchange Server 2010 SP2**  

-   **Exchange Server 2013**  

-   **Exchange Online (Office 365)**  : cette version inclut Business Productivity Online Standard Suite  
