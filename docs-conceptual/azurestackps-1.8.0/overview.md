---
title: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack con istruzioni per l'installazione e la configurazione.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "78264411"
---
# <a name="azure-stack-module-180"></a>Modulo di Azure Stack 1.8.0

## <a name="requirements"></a>Requisiti:

La versione minima supportata di Azure Stack è la 1910.

Nota: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Installazione

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a>Note sulla versione

* Supportato con l'aggiornamento 1910
* Le modifiche includono:

    - **Nuovo modulo di amministrazione DRP**: DRP (Deployment Resource Provider) consente distribuzioni orchestrate di provider di risorse all'hub di Azure Stack. Questi comandi interagiscono con il livello di Azure Resource Manager per interagire con DRP.

    - **BRP**:
        - Supporto del ripristino del ruolo singolo per il backup dell'infrastruttura di Azure Stack.
        - Aggiunta del parametro `RoleName` al cmdlet R`estore-AzsBackup`.

    - **FRP**: Modifiche di rilievo per le risorse di tipo **Unità** e **Volume** con l'API versione 2019-05-01. Le funzionalità sono supportate dall'hub di Azure Stack 1910 e versioni successive:
        - Il valore di ID, `Name`, `HealthStatus` e `OperationalStatus` sono stati modificati.
        - Sono supportate le nuove proprietà `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` e `StoragePool` per le risorse di tipo **Unità**.
        - Le proprietà `CanPool` e `CannotPoolReason` delle risorse di tipo **Unità** sono state deprecate. In alternativa, usare `OperationalStatus`.
