---
title: Altre modalità di installazione di Azure PowerShell
description: Come installare Azure PowerShell senza PowerShellGet usando un programma di installazione MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 0976fd51b26010702d200cee445d93269405416c
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153840"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installare Azure PowerShell in Windows con un programma di installazione MSI

Questo articolo illustra come installare Azure PowerShell in Windows con un programma di installazione MSI.  
Usare questi metodi di installazione solo se sono necessari per il sistema. È consigliabile installare Azure PowerShell in Windows con PowerShellGet. Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-azurerm-ps.md).

> [!NOTE]
> Il metodo Installazione guidata piattaforma Web non è più disponibile a partire dalla versione 6 di Azure PowerShell. Se si richiede l'uso dell'Installazione guidata piattaforma Web, prendere invece in considerazione un programma di installazione MSI oppure installare una versione precedente di Azure PowerShell.

Per l'installazione in ambienti Linux o macOS, vedere [Installare Azure PowerShell in macOS o Linux ](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI

Azure PowerShell per Windows PowerShell 5.x può essere installato usando il file MSI disponibile su [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018). Se le versioni precedenti dei moduli di Azure sono state installate come pacchetto MSI, il programma di installazione le rimuove automaticamente. Il pacchetto MSI installa i moduli in `${env:ProgramFiles}\WindowsPowerShell\Modules`. Vengono installati sia il modulo `AzureRM` che il modulo `Azure`.

> [!NOTE]
> Usare il modulo `Azure` solo se si usa il modello di distribuzione classica di Azure.

Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Se il caricamento automatico dei moduli è stato disabilitato, è necessario importare manualmente il modulo con `Import-Module AzureRM`. L'operazione potrebbe richiedere qualche secondo a causa del modo in cui è strutturato il modulo.

È necessario ripetere questo passaggio per ogni nuova sessione di PowerShell avviata. Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).
