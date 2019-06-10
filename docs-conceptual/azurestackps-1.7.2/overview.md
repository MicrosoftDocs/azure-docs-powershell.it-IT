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
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855789"
---
# <a name="azure-stack-module-172"></a>Modulo di Azure Stack 1.7.2

## <a name="requirements"></a>Requirements:

La versione minima supportata di Azure Stack è la 1904.

Note: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install-powershell-for-azure-stack"></a>Installare PowerShell per Azure Stack

L'installazione prevede tre passaggi:

1. Installare PowerShell per Azure Stack in base alla versione di Azure Stack
2. Abilitare funzionalità aggiuntive di archiviazione
3. Verificare l'installazione di PowerShell

### <a name="install-azure-stack-powershell"></a>Installare PowerShell per Azure Stack

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a>Abilitare funzionalità aggiuntive di archiviazione

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a>Note sulla versione

* Supportato con l'aggiornamento 1904
* Questa è una versione con modifiche che causano interruzioni. Per informazioni dettagliate, fare riferimento a <https://aka.ms/azspshmigration170>
* Azs.Backup.Admin Module * Modifica che causa un'interruzione: passaggio dal backup alla modalità di crittografia basata su certificato. Il supporto delle chiavi simmetriche è deprecato.
* Azs.Fabric.Admin Module       * Deprecato           * Get-AzsInfrastructureVolume è deprecato; ora è fornito il nuovo Get-AzsVolume           * Get-AzsStorageSystem è deprecato; ora è fornito il nuovo cmdlet Get-AzsStorageSubSystem           * Get-AzsStoragePool è deprecato; l'oggetto StorageSubSystem ha la proprietà di capacità
* Azs.Compute.Admin Module           * Correzione dei bug: Add-AzsPlatformImage, Get-AzsPlatformImage : Chiamata a ConvertTo-PlatformImageObject solo nel percorso di riuscita           * Correzione dei bug: Add-AzsVmExtension, Get-AzsVmExtension : Chiamata a ConvertTo-VmExtensionObject solo nel percorso di riuscita
* Modulo Azs.Storage.Admin           * Correzione dei bug - In assenza di valori, la nuova quota di archiviazione usa quelli predefiniti.'
