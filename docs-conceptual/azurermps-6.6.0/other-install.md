---
title: Altre modalità di installazione di Azure PowerShell
description: Come installare Azure PowerShell senza PowerShellGet usando un programma di installazione MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: add4d1843cf3fe791f3a734f43b0fb065629e899
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368348"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installare Azure PowerShell in Windows con un programma di installazione MSI

Questo articolo illustra come installare Azure PowerShell in Windows con un programma di installazione MSI.  
Usare questi metodi di installazione solo se sono necessari per il sistema. È consigliabile installare Azure PowerShell in Windows con PowerShellGet. Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-azurerm-ps.md).

> [!NOTE]
> Il metodo Installazione guidata piattaforma Web non è più disponibile a partire dalla versione 6 di Azure PowerShell. Se si richiede l'uso dell'Installazione guidata piattaforma Web, prendere invece in considerazione un programma di installazione MSI oppure installare una versione precedente di Azure PowerShell.

Per eseguire Azure PowerShell in un contenitore Docker, vedere [Eseguire Azure PowerShell in Docker](azurerm-ps-in-docker.md).

Per l'installazione in ambienti Linux o macOS, vedere [Installare Azure PowerShell in macOS o Linux ](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI

Azure PowerShell può essere installato usando il file MSI disponibile su [GitHub](https://github.com/Azure/azure-powershell/releases/latest). Se le versioni precedenti dei moduli di Azure sono state installate come pacchetto MSI, il programma di installazione le rimuove automaticamente. Il pacchetto MSI installa i moduli in `${env:ProgramFiles}\WindowsPowerShell\Modules`. Vengono installati sia il modulo `AzureRM` che il modulo `Azure`.

> [!NOTE]
> Usare il modulo `Azure` solo se si usa il modello di distribuzione classica di Azure.

Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata. L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).
Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).