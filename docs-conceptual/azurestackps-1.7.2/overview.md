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
ms.openlocfilehash: 1b3d707e862dd0c21e9e6b0a89f429ff21b1a99d
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "68861335"
---
# <a name="azure-stack-module-172"></a>Modulo di Azure Stack 1.7.2

## <a name="requirements"></a>Requisiti:

La versione minima supportata di Azure Stack è la 1904.

Nota: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Installazione

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a>Note sulla versione

* Supportato con l'aggiornamento 1904
* Questa è una versione con modifiche che causano interruzioni. Per informazioni dettagliate, fare riferimento a <https://aka.ms/azspshmigration170>
* Modifica che causa un'interruzione: passaggio dal backup alla modalità di crittografia basata su certificato. Il supporto delle chiavi simmetriche è deprecato.
* Per informazioni dettagliate, fare riferimento a https://aka.ms/azspshmigration170
* Modulo Azs.Storage.Admin 
* Correzione dei bug - In assenza di valori, la nuova quota di archiviazione usa quelli predefiniti.
