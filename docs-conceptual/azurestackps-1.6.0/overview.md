---
title: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack con istruzioni per l'installazione e la configurazione.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053316"
---
# <a name="azure-stack-module-160"></a>Modulo di Azure Stack 1.6.0

## <a name="requirements"></a>Requisiti:
La versione minima supportata di Azure Stack è 1811.

Nota: Se si usa una versione precedente, installare la versione 1.6.0

## <a name="install"></a>Installazione
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a>Note sulla versione
* Supportato con l'aggiornamento 1811
* Modulo Azs.Compute.Admin
    * Risoluzione del problema relativo al prefisso Azs mancante per New-DataDiskObject e aggiunta dell'alias con l'avviso di una futura deprecazione.
* Modulo Azs.Update.Admin
    * Aggiunta di un avviso per consigliare di eseguire Test-AzureStack prima di Install-AzsUpdate
* Azs.Fabric.Admin
    * Nuovo cmdlet (le funzionalità sono supportate da Azure Stack 1811+)
        * Get-AzsDrive
        * Get-AzsVolume
        * Get-AzsStorageSubSystem
    * Deprecazione
        * Get-AzsInfrastructureVolume è ora un alias per il cmdlet Get-AzsVolume
* Azs.InfrastructureInsights.Admin
    *  Aggiunta del nuovo cmdlet Repair-AzsAlert
* Azs.Storage.Admin
    * Correzione del bug in cui non vengono usati i valori di quota predefiniti
* Modulo Azs.Subscriptions.Admin
    * Risoluzione del problema relativo al prefisso Azs mancante per New-AddonPlanDefinitionObject e aggiunta dell'alias con l'avviso di una futura deprecazione.
