---
title: Eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell
description: Informazioni su come eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: 5945b573d467f1ff64e327c52124ffed1e4305aa
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427837"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Avvio rapido: Eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell

In questo articolo verrà illustrato come usare il modulo Az.Tools.Migration di PowerShell per aggiornare automaticamente gli script di PowerShell e i moduli di script dal modulo AzureRM al modulo Az PowerShell.

> [!IMPORTANT]
> Il modulo Az.Tools.Migration di PowerShell è attualmente disponibile in anteprima pubblica. Questa versione in anteprima viene fornita senza un contratto di servizio. Non è la scelta consigliata per carichi di lavoro di produzione. Alcune funzionalità potrebbero non essere supportate o potrebbero presentare funzionalità limitate. Per altre informazioni, vedere [Condizioni supplementari per l'utilizzo delle anteprime di Microsoft Azure](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).

Inviare feedback e segnalare problemi sul modulo Az.Tools.Migration di PowerShell tramite un [problema di GitHub](https://github.com/Azure/azure-powershell-migration/issues) nel repository `azure-powershell-migration`.

## <a name="requirements"></a>Requisiti

* Aggiornare gli script di PowerShell alla versione più recente del [modulo AzureRM di PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Installare il modulo Az.Tools.Migration di PowerShell.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Passaggio 1: Generare un piano di aggiornamento

Usare il cmdlet `New-AzUpgradeModulePlan` per generare un piano di aggiornamento per la migrazione degli script e dei moduli al modulo Az PowerShell. Il piano di aggiornamento illustra in modo dettagliato il file e i punti di offset specifici che necessitano di modifiche durante lo spostamento dai cmdlet di AzureRM ai cmdlet di Az PowerShell.

> [!NOTE]
> Il cmdlet `New-AzUpgradeModulePlan` non esegue il piano e genera solo i passaggi di aggiornamento.

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

Esaminare i risultati del piano di aggiornamento.

```powershell
# Show the entire upgrade plan
$Plan
```

Eseguire il comando seguente per filtrare i risultati in modo da visualizzare i comandi con avvisi o errori. Questo approccio può risultare utile nei set di risultati di grandi dimensioni per identificare rapidamente gli errori prima di eseguire l'aggiornamento.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a>Passaggio 2: Eseguire l'aggiornamento

Il piano di aggiornamento viene eseguito quando si esegue il cmdlet `Invoke-AzUpgradeModulePlan`. Questo comando esegue un aggiornamento del file o delle cartelle specificate, ad eccezione di eventuali errori identificati dal cmdlet `New-AzUpgradeModulePlan`.

Questo comando richiede di specificare se i file devono essere modificati sul posto o se è necessario salvare nuovi file insieme ai file originali, senza modificare i file originali.

> [!CAUTION]
> Non è disponibile alcuna operazione di annullamento. Assicurarsi sempre che sia disponibile una copia di backup degli script e dei moduli di PowerShell che si sta provando ad aggiornare.

> [!WARNING]
> Il cmdlet `Invoke-AzUpgradeModulePlan` è distruttivo quando viene specificata l'opzione `-FileEditMode ModifyExistingFiles`. Modifica gli script e le funzioni sul posto in base al piano di aggiornamento del modulo generato dal cmdlet `New-AzUpgradeModulePlan`. Per l'opzione non distruttiva specificare invece `-FileEditMode SaveChangesToNewFiles`.

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

Esaminare i risultati dell'operazione di aggiornamento.

```powershell
# Show the results for the entire upgrade operation
$Results
```

Se vengono restituiti errori, è possibile esaminare in modo più dettagliato i risultati dell'errore con il comando seguente:

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a>Limitazioni

* Gli aggiornamenti automatici dei nomi dei parametri a parametri "splatted" non sono supportati. Se vengono rilevati durante la generazione del piano di aggiornamento, viene restituito un avviso.
* Le operazioni di I/O del file usano la codifica predefinita. Le situazioni insolite per la codifica del file possono provocare problemi.
* I cmdlet di AzureRM passati come argomenti alle istruzioni fittizie degli unit test Pester non vengono rilevati.
* È attualmente supportata come destinazione solo la versione 4.6.1 del modulo Az PowerShell.

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sul modulo Az PowerShell, vedere la [documentazione di Azure PowerShell](/powershell/azure/)