---
title: Eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell
description: Informazioni su come eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/18/2020
ms.openlocfilehash: 57218c130f172bc359334b83db16e5790fa5562c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893791"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>Avvio rapido: Eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell

In questo articolo verrà illustrato come usare il modulo Az.Tools.Migration di PowerShell per aggiornare automaticamente gli script di PowerShell e i moduli di script dal modulo AzureRM al modulo Az PowerShell. Per altre opzioni sulla migrazione, vedere [Eseguire la migrazione di Azure PowerShell da AzureRM ad Az](/powershell/azure/migrate-from-azurerm-to-az).

## <a name="requirements"></a>Requisiti

* Aggiornare gli script di PowerShell alla versione più recente del [modulo AzureRM di PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).
* Installare il modulo Az.Tools.Migration di PowerShell.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>Passaggio 1: Generare un piano di aggiornamento

Usare il cmdlet **`New-AzUpgradeModulePlan`** per generare un piano di aggiornamento per la migrazione di script e moduli al modulo Az di PowerShell. Questo cmdlet non consente di apportare modifiche agli script esistenti. Usare il parametro **`FilePath`** per scegliere uno script specifico come destinazione oppure il parametro **`DirectoryPath`** per scegliere tutti gli script di una specifica cartella.

> [!NOTE]
> Il cmdlet **`New-AzUpgradeModulePlan`** non esegue il piano, ma genera solo i passaggi di aggiornamento.

L'esempio seguente genera un piano per tutti gli script della cartella _`C:\Scripts`_ . Viene specificato il parametro **`OutVariable`** in modo che i risultati vengano restituiti e archiviati simultaneamente in una variabile denominata **`Plan`** .

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 5.2.0 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

Come illustrato nell'output seguente, il piano di aggiornamento illustra in modo dettagliato il file e i punti di offset specifici che necessitano di modifiche per lo spostamento dai cmdlet AzureRM ai cmdlet Az di PowerShell.

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

Prima di eseguire l'aggiornamento, è necessario visualizzare i risultati del piano per verificare la presenza di problemi. L'esempio seguente restituisce un elenco di script e degli elementi al loro interno che ne eviteranno l'aggiornamento automatico.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

Gli elementi visualizzati nell'output seguente non verranno aggiornati automaticamente senza prima correggere manualmente i problemi.

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a>Passaggio 2: Eseguire l'aggiornamento

> [!CAUTION]
> Non è disponibile alcuna operazione di annullamento. Assicurarsi sempre che sia disponibile una copia di backup degli script e dei moduli di PowerShell che si sta provando ad aggiornare.

Quando si è soddisfatti del piano, l'aggiornamento viene eseguito con il cmdlet **`Invoke-AzUpgradeModulePlan`** . Specificare **`SaveChangesToNewFiles`** per il valore del parametro **`FileEditMode`** per impedire che vengano apportate modifiche agli script originali. In questa modalità l'aggiornamento viene eseguito creando una copia di ogni script di destinazione con _`_az_upgraded`_ aggiunto alla fine dei nomi file.

> [!WARNING]
> Il cmdlet **`Invoke-AzUpgradeModulePlan`** è distruttivo se si specifica l'opzione **`-FileEditMode ModifyExistingFiles`** . Modifica gli script e le funzioni sul posto in base al piano di aggiornamento del modulo generato dal cmdlet **`New-AzUpgradeModulePlan`** . Per l'opzione non distruttiva specificare invece **`-FileEditMode SaveChangesToNewFiles`** .

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

Se vengono restituiti errori, è possibile esaminare in modo più dettagliato i risultati dell'errore con il comando seguente:

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a>Limitazioni

* Le operazioni di I/O del file usano la codifica predefinita. Le situazioni insolite per la codifica del file possono provocare problemi.
* I cmdlet di AzureRM passati come argomenti alle istruzioni fittizie degli unit test Pester non vengono rilevati.
* Attualmente, come destinazione è supportato solo il modulo Az di PowerShell versione 5.2.0.

## <a name="how-to-report-issues"></a>Come segnalare i problemi

Inviare feedback e segnalare problemi sul modulo Az.Tools.Migration di PowerShell tramite un [problema di GitHub](https://github.com/Azure/azure-powershell-migration/issues) nel repository `azure-powershell-migration`.

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sul modulo Az PowerShell, vedere la [documentazione di Azure PowerShell](/powershell/azure/)
