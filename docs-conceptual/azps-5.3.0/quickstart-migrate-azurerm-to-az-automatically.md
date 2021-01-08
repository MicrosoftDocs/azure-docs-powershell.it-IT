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
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="d5e1f-103">Avvio rapido: Eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell</span><span class="sxs-lookup"><span data-stu-id="d5e1f-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="d5e1f-104">In questo articolo verrà illustrato come usare il modulo Az.Tools.Migration di PowerShell per aggiornare automaticamente gli script di PowerShell e i moduli di script dal modulo AzureRM al modulo Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span> <span data-ttu-id="d5e1f-105">Per altre opzioni sulla migrazione, vedere [Eseguire la migrazione di Azure PowerShell da AzureRM ad Az](/powershell/azure/migrate-from-azurerm-to-az).</span><span class="sxs-lookup"><span data-stu-id="d5e1f-105">For additional migration options, see [Migrate Azure PowerShell from AzureRM to Az](/powershell/azure/migrate-from-azurerm-to-az).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e1f-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5e1f-106">Requirements</span></span>

* <span data-ttu-id="d5e1f-107">Aggiornare gli script di PowerShell alla versione più recente del [modulo AzureRM di PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="d5e1f-107">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="d5e1f-108">Installare il modulo Az.Tools.Migration di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-108">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="d5e1f-109">Passaggio 1: Generare un piano di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d5e1f-109">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="d5e1f-110">Usare il cmdlet **`New-AzUpgradeModulePlan`** per generare un piano di aggiornamento per la migrazione di script e moduli al modulo Az di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-110">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="d5e1f-111">Questo cmdlet non consente di apportare modifiche agli script esistenti.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-111">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="d5e1f-112">Usare il parametro **`FilePath`** per scegliere uno script specifico come destinazione oppure il parametro **`DirectoryPath`** per scegliere tutti gli script di una specifica cartella.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-112">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="d5e1f-113">Il cmdlet **`New-AzUpgradeModulePlan`** non esegue il piano, ma genera solo i passaggi di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-113">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="d5e1f-114">L'esempio seguente genera un piano per tutti gli script della cartella _`C:\Scripts`_ .</span><span class="sxs-lookup"><span data-stu-id="d5e1f-114">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="d5e1f-115">Viene specificato il parametro **`OutVariable`** in modo che i risultati vengano restituiti e archiviati simultaneamente in una variabile denominata **`Plan`** .</span><span class="sxs-lookup"><span data-stu-id="d5e1f-115">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 5.2.0 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="d5e1f-116">Come illustrato nell'output seguente, il piano di aggiornamento illustra in modo dettagliato il file e i punti di offset specifici che necessitano di modifiche per lo spostamento dai cmdlet AzureRM ai cmdlet Az di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-116">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

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

<span data-ttu-id="d5e1f-117">Prima di eseguire l'aggiornamento, è necessario visualizzare i risultati del piano per verificare la presenza di problemi.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-117">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="d5e1f-118">L'esempio seguente restituisce un elenco di script e degli elementi al loro interno che ne eviteranno l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-118">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="d5e1f-119">Gli elementi visualizzati nell'output seguente non verranno aggiornati automaticamente senza prima correggere manualmente i problemi.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-119">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span>

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

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="d5e1f-120">Passaggio 2: Eseguire l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d5e1f-120">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="d5e1f-121">Non è disponibile alcuna operazione di annullamento.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-121">There is no undo operation.</span></span> <span data-ttu-id="d5e1f-122">Assicurarsi sempre che sia disponibile una copia di backup degli script e dei moduli di PowerShell che si sta provando ad aggiornare.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-122">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="d5e1f-123">Quando si è soddisfatti del piano, l'aggiornamento viene eseguito con il cmdlet **`Invoke-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="d5e1f-123">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="d5e1f-124">Specificare **`SaveChangesToNewFiles`** per il valore del parametro **`FileEditMode`** per impedire che vengano apportate modifiche agli script originali.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-124">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="d5e1f-125">In questa modalità l'aggiornamento viene eseguito creando una copia di ogni script di destinazione con _`_az_upgraded`_ aggiunto alla fine dei nomi file.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-125">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="d5e1f-126">Il cmdlet **`Invoke-AzUpgradeModulePlan`** è distruttivo se si specifica l'opzione **`-FileEditMode ModifyExistingFiles`** .</span><span class="sxs-lookup"><span data-stu-id="d5e1f-126">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="d5e1f-127">Modifica gli script e le funzioni sul posto in base al piano di aggiornamento del modulo generato dal cmdlet **`New-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="d5e1f-127">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="d5e1f-128">Per l'opzione non distruttiva specificare invece **`-FileEditMode SaveChangesToNewFiles`** .</span><span class="sxs-lookup"><span data-stu-id="d5e1f-128">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

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

<span data-ttu-id="d5e1f-129">Se vengono restituiti errori, è possibile esaminare in modo più dettagliato i risultati dell'errore con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="d5e1f-129">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

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

## <a name="limitations"></a><span data-ttu-id="d5e1f-130">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="d5e1f-130">Limitations</span></span>

* <span data-ttu-id="d5e1f-131">Le operazioni di I/O del file usano la codifica predefinita.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-131">File I/O operations use default encoding.</span></span> <span data-ttu-id="d5e1f-132">Le situazioni insolite per la codifica del file possono provocare problemi.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-132">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="d5e1f-133">I cmdlet di AzureRM passati come argomenti alle istruzioni fittizie degli unit test Pester non vengono rilevati.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-133">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="d5e1f-134">Attualmente, come destinazione è supportato solo il modulo Az di PowerShell versione 5.2.0.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-134">Currently, only Az PowerShell module version 5.2.0 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="d5e1f-135">Come segnalare i problemi</span><span class="sxs-lookup"><span data-stu-id="d5e1f-135">How to report issues</span></span>

<span data-ttu-id="d5e1f-136">Inviare feedback e segnalare problemi sul modulo Az.Tools.Migration di PowerShell tramite un [problema di GitHub](https://github.com/Azure/azure-powershell-migration/issues) nel repository `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="d5e1f-136">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d5e1f-137">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="d5e1f-137">Next steps</span></span>

<span data-ttu-id="d5e1f-138">Per altre informazioni sul modulo Az PowerShell, vedere la [documentazione di Azure PowerShell](/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="d5e1f-138">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>
