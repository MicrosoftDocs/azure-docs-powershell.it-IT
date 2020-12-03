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
ms.locfileid: "96427022"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="0cfa8-103">Avvio rapido: Eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell</span><span class="sxs-lookup"><span data-stu-id="0cfa8-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="0cfa8-104">In questo articolo verrà illustrato come usare il modulo Az.Tools.Migration di PowerShell per aggiornare automaticamente gli script di PowerShell e i moduli di script dal modulo AzureRM al modulo Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0cfa8-105">Il modulo Az.Tools.Migration di PowerShell è attualmente disponibile in anteprima pubblica.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="0cfa8-106">Questa versione in anteprima viene fornita senza un contratto di servizio.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="0cfa8-107">Non è la scelta consigliata per carichi di lavoro di produzione.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="0cfa8-108">Alcune funzionalità potrebbero non essere supportate o potrebbero presentare funzionalità limitate.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="0cfa8-109">Per altre informazioni, vedere [Condizioni supplementari per l'utilizzo delle anteprime di Microsoft Azure](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span><span class="sxs-lookup"><span data-stu-id="0cfa8-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

<span data-ttu-id="0cfa8-110">Inviare feedback e segnalare problemi sul modulo Az.Tools.Migration di PowerShell tramite un [problema di GitHub](https://github.com/Azure/azure-powershell-migration/issues) nel repository `azure-powershell-migration`.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-110">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cfa8-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cfa8-111">Requirements</span></span>

* <span data-ttu-id="0cfa8-112">Aggiornare gli script di PowerShell alla versione più recente del [modulo AzureRM di PowerShell (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="0cfa8-112">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="0cfa8-113">Installare il modulo Az.Tools.Migration di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-113">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="0cfa8-114">Passaggio 1: Generare un piano di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0cfa8-114">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="0cfa8-115">Usare il cmdlet `New-AzUpgradeModulePlan` per generare un piano di aggiornamento per la migrazione degli script e dei moduli al modulo Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-115">You use the `New-AzUpgradeModulePlan` cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="0cfa8-116">Il piano di aggiornamento illustra in modo dettagliato il file e i punti di offset specifici che necessitano di modifiche durante lo spostamento dai cmdlet di AzureRM ai cmdlet di Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-116">The upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

> [!NOTE]
> <span data-ttu-id="0cfa8-117">Il cmdlet `New-AzUpgradeModulePlan` non esegue il piano e genera solo i passaggi di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-117">The `New-AzUpgradeModulePlan` cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

<span data-ttu-id="0cfa8-118">Esaminare i risultati del piano di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-118">Review the results of the upgrade plan.</span></span>

```powershell
# Show the entire upgrade plan
$Plan
```

<span data-ttu-id="0cfa8-119">Eseguire il comando seguente per filtrare i risultati in modo da visualizzare i comandi con avvisi o errori.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-119">Run the following command to filter the results to commands that have warnings or errors.</span></span> <span data-ttu-id="0cfa8-120">Questo approccio può risultare utile nei set di risultati di grandi dimensioni per identificare rapidamente gli errori prima di eseguire l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-120">This may be helpful on large result sets to quickly identify errors before performing the upgrade.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="0cfa8-121">Passaggio 2: Eseguire l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0cfa8-121">Step 2: Perform the upgrade</span></span>

<span data-ttu-id="0cfa8-122">Il piano di aggiornamento viene eseguito quando si esegue il cmdlet `Invoke-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-122">The upgrade plan is executed when you run the `Invoke-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="0cfa8-123">Questo comando esegue un aggiornamento del file o delle cartelle specificate, ad eccezione di eventuali errori identificati dal cmdlet `New-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-123">This command performs an upgrade of the specified file or folders except for any errors that were identified by the `New-AzUpgradeModulePlan` cmdlet.</span></span>

<span data-ttu-id="0cfa8-124">Questo comando richiede di specificare se i file devono essere modificati sul posto o se è necessario salvare nuovi file insieme ai file originali, senza modificare i file originali.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-124">This command requires you to specify if the files should be modified in place or if new files should be saved alongside your original files (leaving originals unmodified).</span></span>

> [!CAUTION]
> <span data-ttu-id="0cfa8-125">Non è disponibile alcuna operazione di annullamento.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-125">There is no undo operation.</span></span> <span data-ttu-id="0cfa8-126">Assicurarsi sempre che sia disponibile una copia di backup degli script e dei moduli di PowerShell che si sta provando ad aggiornare.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-126">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

> [!WARNING]
> <span data-ttu-id="0cfa8-127">Il cmdlet `Invoke-AzUpgradeModulePlan` è distruttivo quando viene specificata l'opzione `-FileEditMode ModifyExistingFiles`.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-127">The `Invoke-AzUpgradeModulePlan` cmdlet is destructive when the `-FileEditMode ModifyExistingFiles` option is specified!</span></span> <span data-ttu-id="0cfa8-128">Modifica gli script e le funzioni sul posto in base al piano di aggiornamento del modulo generato dal cmdlet `New-AzUpgradeModulePlan`.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the `New-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="0cfa8-129">Per l'opzione non distruttiva specificare invece `-FileEditMode SaveChangesToNewFiles`.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-129">For the non-destructive option specify `-FileEditMode SaveChangesToNewFiles` instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

<span data-ttu-id="0cfa8-130">Esaminare i risultati dell'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-130">Review the results of the upgrade operation.</span></span>

```powershell
# Show the results for the entire upgrade operation
$Results
```

<span data-ttu-id="0cfa8-131">Se vengono restituiti errori, è possibile esaminare in modo più dettagliato i risultati dell'errore con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="0cfa8-131">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a><span data-ttu-id="0cfa8-132">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="0cfa8-132">Limitations</span></span>

* <span data-ttu-id="0cfa8-133">Gli aggiornamenti automatici dei nomi dei parametri a parametri "splatted" non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-133">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="0cfa8-134">Se vengono rilevati durante la generazione del piano di aggiornamento, viene restituito un avviso.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-134">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="0cfa8-135">Le operazioni di I/O del file usano la codifica predefinita.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-135">File I/O operations use default encoding.</span></span> <span data-ttu-id="0cfa8-136">Le situazioni insolite per la codifica del file possono provocare problemi.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-136">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="0cfa8-137">I cmdlet di AzureRM passati come argomenti alle istruzioni fittizie degli unit test Pester non vengono rilevati.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-137">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="0cfa8-138">È attualmente supportata come destinazione solo la versione 4.6.1 del modulo Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0cfa8-138">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0cfa8-139">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="0cfa8-139">Next steps</span></span>

<span data-ttu-id="0cfa8-140">Per altre informazioni sul modulo Az PowerShell, vedere la [documentazione di Azure PowerShell](/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="0cfa8-140">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>