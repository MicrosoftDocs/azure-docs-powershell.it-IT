---
title: guida introduttiva ad Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 0c3b749cb2ac7f11dacafca76b65944f523f727d
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498155"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="16fac-102">guida introduttiva ad Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="16fac-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="16fac-103">Azure PowerShell è progettato per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="16fac-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="16fac-104">Usare Azure PowerShell quando si vogliono creare strumenti automatizzati che usano il modello di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="16fac-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="16fac-105">È possibile provarlo nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure installarlo nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="16fac-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="16fac-106">Questo articolo consente di iniziare a usare Azure PowerShell e ne illustra i concetti fondamentali.</span><span class="sxs-lookup"><span data-stu-id="16fac-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="16fac-107">Installazione o esecuzione in Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="16fac-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="16fac-108">Il modo più semplice per iniziare a usare Azure PowerShell è provarlo in un ambiente Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="16fac-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="16fac-109">Per iniziare subito a usare Azure Cloud Shell, vedere [Guida introduttiva a PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="16fac-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="16fac-110">Cloud Shell esegue PowerShell 6 in un contenitore Linux, per cui le funzionalità specifiche di Windows non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="16fac-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="16fac-111">Quando si è pronti per installare Azure PowerShell nel computer locale, seguire le istruzioni in [Installare il modulo Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="16fac-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="16fac-112">Accedere ad Azure</span><span class="sxs-lookup"><span data-stu-id="16fac-112">Sign in to Azure</span></span>

<span data-ttu-id="16fac-113">Accedere in modo interattivo con il cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="16fac-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="16fac-114">Ignorare questo passaggio se si usa Cloud Shell: La sessione di Azure Cloud Shell è già autenticata per l'ambiente, la sottoscrizione e il tenant che ha avviato la sessione Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="16fac-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="16fac-115">Se si risiede in un'area non degli Stati Uniti, usare il parametro `-Environment` per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="16fac-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="16fac-116">Recuperare il nome dell'ambiente per la propria area con il cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="16fac-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="16fac-117">Ad esempio, per accedere ad Azure Cina 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="16fac-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="16fac-118">Si otterrà un token da usare in https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="16fac-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="16fac-119">Aprire questa pagina nel browser e immettere il token, quindi accedere con le credenziali dell'account Azure e autorizzare Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="16fac-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="16fac-120">Dopo aver effettuato l'accesso, verrà visualizzato un messaggio indicante quale sottoscrizione di Azure è attiva.</span><span class="sxs-lookup"><span data-stu-id="16fac-120">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="16fac-121">Se l'account include più sottoscrizioni di Azure e se ne vuole selezionare una diversa, recuperare le sottoscrizioni disponibili con [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) e usare il cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext) con l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="16fac-121">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="16fac-122">Per altre informazioni sulla gestione delle sottoscrizioni di Azure in Azure PowerShell, vedere [Usare più sottoscrizioni di Azure](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="16fac-122">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="16fac-123">Dopo aver effettuato l'accesso è possibile usare i cmdlet di Azure PowerShell per l'accesso e la gestione delle risorse nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="16fac-123">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="16fac-124">Per altre informazioni sul processo di accesso e i metodi di autenticazione, vedere [Accedere con Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="16fac-124">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="16fac-125">Trovare i comandi</span><span class="sxs-lookup"><span data-stu-id="16fac-125">Find commands</span></span>

<span data-ttu-id="16fac-126">I cmdlet di Azure PowerShell seguono una convenzione di denominazione standard per PowerShell, `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="16fac-126">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="16fac-127">Il verbo descrive l'azione (alcuni esempi includono `Create`, `Get`, `Set`, `Delete`) e il nome descrive il tipo di risorsa (alcuni esempi includono `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="16fac-127">The verb describes the action (examples include `Create`, `Get`, `Set`, `Delete`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="16fac-128">I nomi in Azure PowerShell iniziano sempre con il prefisso `Az`.</span><span class="sxs-lookup"><span data-stu-id="16fac-128">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="16fac-129">Per l'elenco completo dei verbi standard, vedere [Verbi approvati per i comandi di PowerShell](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="16fac-129">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="16fac-130">Conoscere i nomi, i verbi e i moduli di Azure PowerShell disponibili consente di trovare i comandi con il cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="16fac-130">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="16fac-131">Ad esempio, per trovare tutti i comandi correlati alla macchina virtuale che usano il verbo `Get`:</span><span class="sxs-lookup"><span data-stu-id="16fac-131">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="16fac-132">Per facilitare la ricerca di comandi comuni, questa tabella elenca il tipo di risorsa, il modulo di Azure PowerShell corrispondente e il prefisso del nome da usare con `Get-Command`:</span><span class="sxs-lookup"><span data-stu-id="16fac-132">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="16fac-133">Tipo di risorsa</span><span class="sxs-lookup"><span data-stu-id="16fac-133">Resource type</span></span> | <span data-ttu-id="16fac-134">Modulo di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="16fac-134">Azure PowerShell module</span></span> | <span data-ttu-id="16fac-135">Prefisso del nome</span><span class="sxs-lookup"><span data-stu-id="16fac-135">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="16fac-136">Gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="16fac-136">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="16fac-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="16fac-137">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="16fac-138">Macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="16fac-138">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="16fac-139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="16fac-139">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="16fac-140">Account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="16fac-140">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="16fac-141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="16fac-141">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="16fac-142">Insieme di credenziali di chiave</span><span class="sxs-lookup"><span data-stu-id="16fac-142">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="16fac-143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="16fac-143">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="16fac-144">Applicazioni Web</span><span class="sxs-lookup"><span data-stu-id="16fac-144">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="16fac-145">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="16fac-145">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="16fac-146">Database SQL</span><span class="sxs-lookup"><span data-stu-id="16fac-146">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="16fac-147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="16fac-147">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="16fac-148">Per un elenco completo dei moduli di Azure PowerShell, vedere l'[elenco di moduli di Azure PowerShell](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) ospitato in GitHub.</span><span class="sxs-lookup"><span data-stu-id="16fac-148">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="16fac-149">Modelli di avvio rapido ed esercitazioni per apprendere le nozioni di base di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="16fac-149">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="16fac-150">Per iniziare a usare Azure PowerShell, provare un'esercitazione dettagliata per la configurazione delle macchine virtuali e per imparare a eseguire query nelle stesse.</span><span class="sxs-lookup"><span data-stu-id="16fac-150">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="16fac-151">Creare macchine virtuali con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="16fac-151">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="16fac-152">Sono disponibili anche guide introduttive di Azure PowerShell per altri servizi di Azure più diffusi:</span><span class="sxs-lookup"><span data-stu-id="16fac-152">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="16fac-153">Creare un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="16fac-153">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="16fac-154">Trasferire oggetti da e verso Archiviazione BLOB di Azure</span><span class="sxs-lookup"><span data-stu-id="16fac-154">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="16fac-155">Creare e recuperare segreti da Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="16fac-155">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="16fac-156">Creare un database SQL di Azure e un firewall</span><span class="sxs-lookup"><span data-stu-id="16fac-156">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="16fac-157">Eseguire un contenitore in Istanze di Azure Container</span><span class="sxs-lookup"><span data-stu-id="16fac-157">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="16fac-158">Creare un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="16fac-158">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="16fac-159">Creare un'istanza di Load Balancer Standard</span><span class="sxs-lookup"><span data-stu-id="16fac-159">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="16fac-160">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="16fac-160">Next steps</span></span>

* [<span data-ttu-id="16fac-161">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="16fac-161">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="16fac-162">Gestire le sottoscrizioni di Azure con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="16fac-162">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="16fac-163">Creare entità servizio di Azure con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="16fac-163">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="16fac-164">Ottenere informazioni dalla community:</span><span class="sxs-lookup"><span data-stu-id="16fac-164">Get help from the community:</span></span>
  * [<span data-ttu-id="16fac-165">Forum Azure su MSDN</span><span class="sxs-lookup"><span data-stu-id="16fac-165">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="16fac-166">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="16fac-166">Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
