---
title: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack con istruzioni per l'installazione e la configurazione.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: af34497f243ce8f4f718e88312f6ad54eb6ad848
ms.sourcegitcommit: 993db64e68b222acbcfdeef2e81eb3316b160858
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2019
ms.locfileid: "56240532"
---
# <a name="azure-stack-module-170"></a>Modulo di Azure Stack 1.7.0

## <a name="requirements"></a>Requirements:
La versione minima supportata di Azure Stack è 1901.

Note: se si usa una versione precedente, installare la versione 1.7.0

## <a name="install"></a>Installa
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.0
```
## <a name="release-notes"></a>Note sulla versione
* Supportato con l'aggiornamento 1901
* Questa è una versione con modifiche che causano interruzioni. Per informazioni dettagliate, fare riferimento a https://aka.ms/azspshmigration170
* Azs.Backup.Admin Module * Modifica che causa un'interruzione: passaggio dal backup alla modalità di crittografia basata su certificato. Il supporto delle chiavi simmetriche è deprecato.
* Azs.Fabric.Admin Module       * Deprecato           * Get-AzsInfrastructureVolume è deprecato; ora è fornito il nuovo Get-AzsVolume           * Get-AzsStorageSystem è deprecato; ora è fornito il nuovo cmdlet Get-AzsStorageSubSystem           * Get-AzsStoragePool è deprecato; l'oggetto StorageSubSystem ha la proprietà di capacità
* Azs.Compute.Admin Module           * Correzione dei bug: Add-AzsPlatformImage, Get-AzsPlatformImage : Chiamata a ConvertTo-PlatformImageObject solo nel percorso di riuscita           * Correzione dei bug: Add-AzsVmExtension, Get-AzsVmExtension : Chiamata a ConvertTo-VmExtensionObject solo nel percorso di riuscita
* Modulo Azs.Storage.Admin           * Correzione dei bug - In assenza di valori, la nuova quota di archiviazione usa quelli predefiniti.'

