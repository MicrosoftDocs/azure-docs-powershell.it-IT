---
title: Altre modalità di installazione di Azure PowerShell
description: Come installare Azure PowerShell senza PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: aaba0ce38129b96e3d691f1a9d9cfdc929188ffd
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "75722408"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a>Installare Azure PowerShell in Windows con il pacchetto MSI o l'Installazione guidata piattaforma Web

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Questo articolo illustra come installare Azure PowerShell in Windows usando un pacchetto MSI o l'Installazione guidata piattaforma Web (WebPI).  
Usare questi metodi di installazione solo se sono necessari per il sistema. È consigliabile installare Azure PowerShell in Windows con PowerShellGet. Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-azurerm-ps.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI

Azure PowerShell può essere installato usando il file MSI disponibile su [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018). Se le versioni precedenti dei moduli di Azure sono state installate come pacchetto MSI, il programma di installazione le rimuove automaticamente. Il pacchetto MSI installa i moduli in `${env:ProgramFiles}\WindowsPowerShell\Modules`. Vengono installati sia il modulo `AzureRM` che il modulo `Azure`.

> [!NOTE]
> Usare il modulo `Azure` solo se si usa il modello di distribuzione classica di Azure.

Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata. L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).
Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Eseguire l'installazione o l'aggiornamento in Windows con Installazione guidata piattaforma Web

Scaricare il [pacchetto per l'Installazione guidata piattaforma Web di Azure PowerShell](https://aka.ms/webpi-azps) e avviare l'installazione. Se le versioni precedenti dei moduli di Azure sono state installate da un pacchetto MSI o con l'Installazione guidata piattaforma Web, il programma di installazione le rimuove automaticamente. I moduli vengono installati in `${env:ProgramFiles}\WindowsPowerShell\Modules`. Vengono installati sia il modulo `AzureRM` che il modulo `Azure`.

> [!NOTE]
> Usare il modulo `Azure` solo se si usa il modello di distribuzione classica di Azure.

Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata. L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).
Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).