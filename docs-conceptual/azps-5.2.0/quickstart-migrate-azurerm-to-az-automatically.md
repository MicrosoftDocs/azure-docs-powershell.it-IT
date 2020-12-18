---
title: Eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell
description: Informazioni su come eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/10/2020
ms.openlocfilehash: 6752fa0376c2f8887511455f56add0859f8961c8
ms.sourcegitcommit: 076ff98abc48e072eb1727532817487bac7507c6
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/15/2020
ms.locfileid: "97488530"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="9993c-103">Avvio rapido: Eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell</span><span class="sxs-lookup"><span data-stu-id="9993c-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="9993c-104">In questo articolo verrà illustrato come usare il modulo Az.Tools.Migration di PowerShell per aggiornare automaticamente gli script di PowerShell e i moduli di script dal modulo AzureRM al modulo Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9993c-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9993c-105">Il modulo Az.Tools.Migration di PowerShell è attualmente disponibile in anteprima pubblica.</span><span class="sxs-lookup"><span data-stu-id="9993c-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="9993c-106">Questa versione in anteprima viene fornita senza un contratto di servizio.</span><span class="sxs-lookup"><span data-stu-id="9993c-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="9993c-107">Non è la scelta consigliata per carichi di lavoro di produzione.</span><span class="sxs-lookup"><span data-stu-id="9993c-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="9993c-108">Alcune funzionalità potrebbero non essere supportate o potrebbero presentare funzionalità limitate.</span><span class="sxs-lookup"><span data-stu-id="9993c-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="9993c-109">Per altre informazioni, vedere [Condizioni supplementari per l'utilizzo delle anteprime di Microsoft Azure](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span><span class="sxs-lookup"><span data-stu-id="9993c-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

## <a name="requirements"></a><span data-ttu-id="9993c-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9993c-110">Requirements</span></span>

* <span data-ttu-id="9993c-111">Aggiornare gli script di PowerShell alla versione più recente del [modulo AzureRM di PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="9993c-111">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="9993c-112">Installare il modulo Az.Tools.Migration di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9993c-112">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="9993c-113">Passaggio 1: Generare un piano di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9993c-113">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="9993c-114">Usare il cmdlet **`New-AzUpgradeModulePlan`** per generare un piano di aggiornamento per la migrazione di script e moduli al modulo Az di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9993c-114">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="9993c-115">Questo cmdlet non consente di apportare modifiche agli script esistenti.</span><span class="sxs-lookup"><span data-stu-id="9993c-115">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="9993c-116">Usare il parametro **`FilePath`** per scegliere uno script specifico come destinazione oppure il parametro **`DirectoryPath`** per scegliere tutti gli script di una specifica cartella.</span><span class="sxs-lookup"><span data-stu-id="9993c-116">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="9993c-117">Il cmdlet **`New-AzUpgradeModulePlan`** non esegue il piano, ma genera solo i passaggi di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="9993c-117">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="9993c-118">L'esempio seguente genera un piano per tutti gli script della cartella _`C:\Scripts`_ .</span><span class="sxs-lookup"><span data-stu-id="9993c-118">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="9993c-119">Viene specificato il parametro **`OutVariable`** in modo che i risultati vengano restituiti e archiviati simultaneamente in una variabile denominata **`Plan`** .</span><span class="sxs-lookup"><span data-stu-id="9993c-119">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="9993c-120">Come illustrato nell'output seguente, il piano di aggiornamento illustra in modo dettagliato il file e i punti di offset specifici che necessitano di modifiche per lo spostamento dai cmdlet AzureRM ai cmdlet Az di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9993c-120">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

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

<span data-ttu-id="9993c-121">Prima di eseguire l'aggiornamento, è necessario visualizzare i risultati del piano per verificare la presenza di problemi.</span><span class="sxs-lookup"><span data-stu-id="9993c-121">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="9993c-122">L'esempio seguente restituisce un elenco di script e degli elementi al loro interno che ne eviteranno l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="9993c-122">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="9993c-123">Gli elementi visualizzati nell'output seguente non verranno aggiornati automaticamente senza prima correggere manualmente i problemi.</span><span class="sxs-lookup"><span data-stu-id="9993c-123">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span> <span data-ttu-id="9993c-124">I problemi noti che non possono essere aggiornati automaticamente includono i comandi che usano splatting.</span><span class="sxs-lookup"><span data-stu-id="9993c-124">Known issues that can’t be upgraded automatically include any commands that use splatting.</span></span>

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

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="9993c-125">Passaggio 2: Eseguire l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="9993c-125">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="9993c-126">Non è disponibile alcuna operazione di annullamento.</span><span class="sxs-lookup"><span data-stu-id="9993c-126">There is no undo operation.</span></span> <span data-ttu-id="9993c-127">Assicurarsi sempre che sia disponibile una copia di backup degli script e dei moduli di PowerShell che si sta provando ad aggiornare.</span><span class="sxs-lookup"><span data-stu-id="9993c-127">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="9993c-128">Quando si è soddisfatti del piano, l'aggiornamento viene eseguito con il cmdlet **`Invoke-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="9993c-128">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="9993c-129">Specificare **`SaveChangesToNewFiles`** per il valore del parametro **`FileEditMode`** per impedire che vengano apportate modifiche agli script originali.</span><span class="sxs-lookup"><span data-stu-id="9993c-129">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="9993c-130">In questa modalità l'aggiornamento viene eseguito creando una copia di ogni script di destinazione con _`_az_upgraded`_ aggiunto alla fine dei nomi file.</span><span class="sxs-lookup"><span data-stu-id="9993c-130">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="9993c-131">Il cmdlet **`Invoke-AzUpgradeModulePlan`** è distruttivo se si specifica l'opzione **`-FileEditMode ModifyExistingFiles`** .</span><span class="sxs-lookup"><span data-stu-id="9993c-131">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="9993c-132">Modifica gli script e le funzioni sul posto in base al piano di aggiornamento del modulo generato dal cmdlet **`New-AzUpgradeModulePlan`** .</span><span class="sxs-lookup"><span data-stu-id="9993c-132">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="9993c-133">Per l'opzione non distruttiva specificare invece **`-FileEditMode SaveChangesToNewFiles`** .</span><span class="sxs-lookup"><span data-stu-id="9993c-133">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

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

<span data-ttu-id="9993c-134">Se vengono restituiti errori, è possibile esaminare in modo più dettagliato i risultati dell'errore con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="9993c-134">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

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

## <a name="limitations"></a><span data-ttu-id="9993c-135">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="9993c-135">Limitations</span></span>

* <span data-ttu-id="9993c-136">Gli aggiornamenti automatici dei nomi dei parametri a parametri "splatted" non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="9993c-136">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="9993c-137">Se vengono rilevati durante la generazione del piano di aggiornamento, viene restituito un avviso.</span><span class="sxs-lookup"><span data-stu-id="9993c-137">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="9993c-138">Le operazioni di I/O del file usano la codifica predefinita.</span><span class="sxs-lookup"><span data-stu-id="9993c-138">File I/O operations use default encoding.</span></span> <span data-ttu-id="9993c-139">Le situazioni insolite per la codifica del file possono provocare problemi.</span><span class="sxs-lookup"><span data-stu-id="9993c-139">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="9993c-140">I cmdlet di AzureRM passati come argomenti alle istruzioni fittizie degli unit test Pester non vengono rilevati.</span><span class="sxs-lookup"><span data-stu-id="9993c-140">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="9993c-141">È attualmente supportata come destinazione solo la versione 4.6.1 del modulo Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9993c-141">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="9993c-142">Come segnalare i problemi</span><span class="sxs-lookup"><span data-stu-id="9993c-142">How to report issues</span></span>

<span data-ttu-id="9993c-143">Inviare feedback e segnalare problemi sul modulo Az.Tools.Migration di PowerShell tramite un [problema di GitHub](https://github.com/Azure/azure-powershell-migration/issues) nel repository `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="9993c-143">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9993c-144">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="9993c-144">Next steps</span></span>

<span data-ttu-id="9993c-145">Per altre informazioni sul modulo Az PowerShell, vedere la [documentazione di Azure PowerShell](/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="9993c-145">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>