---
title: Eseguire la migrazione di script di Azure PowerShell da AzureRM ad Az
description: Informazioni sui passaggi e gli strumenti per eseguire la migrazione di script dal modulo AzureRM al nuovo modulo Az.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753614"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="91f3f-103">Eseguire la migrazione di Azure PowerShell da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="91f3f-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="91f3f-104">Tutte le versioni del modulo AzureRM PowerShell non vengono più aggiornate, ma il supporto è ancora disponibile.</span><span class="sxs-lookup"><span data-stu-id="91f3f-104">All versions of the AzureRM PowerShell module are outdated, but not out of support.</span></span> <span data-ttu-id="91f3f-105">Il [modulo Az PowerShell](install-az-ps.md) è ora il modulo di PowerShell consigliato per l'interazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91f3f-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

<span data-ttu-id="91f3f-106">Gli script scritti per i cmdlet di AzureRM non funzioneranno automaticamente con il nuovo modulo.</span><span class="sxs-lookup"><span data-stu-id="91f3f-106">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="91f3f-107">Per semplificare la transizione, è stato sviluppato il [toolkit di migrazione da AzureRM ad Az](https://github.com/Azure/azure-powershell-migration).</span><span class="sxs-lookup"><span data-stu-id="91f3f-107">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="91f3f-108">Per quanto nessuna migrazione a un nuovo set di comandi sia immediata, questo articolo consentirà di iniziare la transizione al modulo Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91f3f-108">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="91f3f-109">Per altre informazioni sui motivi per cui il modulo Az PowerShell è stato creato, vedere [Introduzione del nuovo modulo Az di Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="91f3f-109">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="91f3f-110">Per visualizzare l'elenco completo delle modifiche di rilievo tra AzureRM e Az, vedere [Modifiche di rilievo della migrazione da AzureRM ad Az](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="91f3f-110">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="91f3f-111">Verificare il funzionamento degli script esistenti con l'ultima versione di AzureRM</span><span class="sxs-lookup"><span data-stu-id="91f3f-111">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="91f3f-112">Prima di eseguire i passaggi di migrazione, verificare quali versioni di AzureRM sono installate nel sistema.</span><span class="sxs-lookup"><span data-stu-id="91f3f-112">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="91f3f-113">In questo modo è possibile assicurarsi che gli script siano già in esecuzione nella versione più recente e sapere quali versioni di AzureRM devono essere disinstallate.</span><span class="sxs-lookup"><span data-stu-id="91f3f-113">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="91f3f-114">Per controllare quale versione di AzureRM è stata installata, eseguire questo esempio:</span><span class="sxs-lookup"><span data-stu-id="91f3f-114">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="91f3f-115">La versione **più recente** disponibile di AzureRM è la **6.13.1** .</span><span class="sxs-lookup"><span data-stu-id="91f3f-115">The **latest** available release of AzureRM is **6.13.1** .</span></span> <span data-ttu-id="91f3f-116">Se questa versione non è installata, per poter usare gli script esistenti con il modulo Az, può essere necessario apportare altre modifiche oltre a quelle descritte in questo articolo e nell'[elenco di modifiche che causano un'interruzione](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="91f3f-116">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="91f3f-117">Se gli script non funzionano con AzureRM 6.13.1, aggiornarli in base alle indicazioni della [guida alla migrazione di AzureRM dalla versione 5.x alla versione 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).</span><span class="sxs-lookup"><span data-stu-id="91f3f-117">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="91f3f-118">Se si usa una versione precedente del modulo AzureRM, sono disponibili guide alla migrazione per ogni versione principale.</span><span class="sxs-lookup"><span data-stu-id="91f3f-118">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="91f3f-119">Installare il toolkit di migrazione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="91f3f-119">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="91f3f-120">Eseguire automaticamente la migrazione degli script di PowerShell</span><span class="sxs-lookup"><span data-stu-id="91f3f-120">Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="91f3f-121">Grazie al toolkit di migrazione da AzureRM ad Az, è possibile generare un piano per determinare quali modifiche verranno eseguite sugli script prima di apportare modifiche agli script e prima di installare il modulo Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91f3f-121">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="91f3f-122">L'avvio rapido [Eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) illustra in modo dettagliato l'intero processo di aggiornamento automatico degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91f3f-122">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="next-steps"></a><span data-ttu-id="91f3f-123">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="91f3f-123">Next steps</span></span>

<span data-ttu-id="91f3f-124">[Installare Azure PowerShell](install-az-ps.md)
[Disinstallare AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="91f3f-124">[Install Azure PowerShell](install-az-ps.md)
[Uninstall AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span></span>
