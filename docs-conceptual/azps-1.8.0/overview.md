---
title: Panoramica di Azure PowerShell
description: Panoramica del modulo Az di Azure PowerShell con informazioni su come installare e iniziare a usare il modulo.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 45ab083dd133c8c7b8dbe902484c92564bc216b9
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068813"
---
# <a name="overview-of-azure-powershell"></a>Panoramica di Azure PowerShell

Azure PowerShell offre un set di cmdlet che usano il modello [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) per la gestione delle risorse di Azure. Azure PowerShell usa .NET Standard, rendendolo disponibile per Windows, macOS e Linux.
Azure PowerShell è disponibile anche in Azure Cloud Shell.

## <a name="about-the-new-az-module"></a>Informazioni sul nuovo modulo Az

Questa documentazione descrive il nuovo modulo Az per Azure PowerShell. Questo nuovo modulo è scritto da zero in .NET Standard. L'uso di .NET Standard consente di eseguire Azure PowerShell in PowerShell 5 con Windows oppure PowerShell 6 in qualsiasi piattaforma. Il modulo Az è ora la modalità desiderata per interagire con Azure tramite PowerShell.
AzureRM continuerà a ottenere le correzioni di bug, ma non riceverà più le nuove funzionalità.

Per tutti i dettagli sul nuovo modulo, compreso il modo in cui sono stati rinominati i comandi e i piani di manutenzione per AzureRM, vedere [Introduzione del modulo Az di Azure PowerShell](new-azureps-module-az.md). Se si vuole iniziare a usare immediatamente il nuovo modulo, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).

È anche disponibile la [documentazione di AzureRM](/powershell/azure/azurerm).

> [!IMPORTANT]
>
> Mentre la documentazione di Azure è in fase di aggiornamento per riflettere i nuovi nomi dei cmdlet del modulo, gli articoli possono ancora usare i comandi di AzureRM. Dopo aver installato il modulo Az, è consigliabile abilitare gli alias dei cmdlet di AzureRM con `Enable-AzureRmAlias`. Per altri dettagli, vedere l'articolo [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).

## <a name="run-or-install"></a>Esecuzione o installazione

È possibile installare Azure PowerShell in PowerShell 5.1 o versione successiva con Windows, PowerShell 6 in qualsiasi piattaforma oppure eseguirlo in Azure Cloud Shell.

* Per l'esecuzione nel browser con Azure Cloud Shell, vedere [Guida introduttiva a PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
* Per l'installazione di Azure PowerShell nel sistema, vedere [Installare Azure PowerShell](install-az-ps.md).

Per informazioni sulla versione più recente di Azure PowerShell, vedere le [note sulla versione](release-notes-azureps.md).

## <a name="get-started"></a>Attività iniziali

Per apprendere le nozioni di base di Azure PowerShell, vedere l'articolo [Guida introduttiva ad Azure PowerShell](get-started-azureps.md). Se non si ha familiarità con PowerShell, potrebbe essere utile un'introduzione a PowerShell:

* [Installare PowerShell](/powershell/scripting/install/installing-powershell)
* [Creazione di script con PowerShell](/powershell/scripting/powershell-scripting)
* [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)
* Corso di [introduzione a PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) di Microsoft Virtual Academy

Gli esempi seguenti possono essere utili per alcuni usi comuni di Azure:

* [Macchine virtuali Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Macchine virtuali Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [App Web](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [Database SQL](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a>Sviluppare le proprie competenze con Microsoft Learn

- [Automatizzare le attività di Azure usando gli script con PowerShell](/learn/modules/automate-azure-tasks-with-powershell/)
- [Altre risorse di apprendimento interattivo](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Altri moduli di Azure PowerShell

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
