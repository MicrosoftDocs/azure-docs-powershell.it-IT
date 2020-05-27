---
title: guida introduttiva ad Azure PowerShell
description: ''
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/17/2020
ms.openlocfilehash: c47395e4291ba61e929511db1273cafac9d289f0
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387854"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="4daad-102">guida introduttiva ad Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4daad-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="4daad-103">Azure PowerShell è progettato per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4daad-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="4daad-104">Usare Azure PowerShell quando si vogliono creare strumenti automatizzati che usano il modello di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4daad-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="4daad-105">È possibile provarlo nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure installarlo nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="4daad-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="4daad-106">Questo articolo consente di iniziare a usare Azure PowerShell e ne illustra i concetti fondamentali.</span><span class="sxs-lookup"><span data-stu-id="4daad-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="4daad-107">Installazione o esecuzione in Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="4daad-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="4daad-108">Il modo più semplice per iniziare a usare Azure PowerShell è provarlo in un ambiente Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="4daad-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="4daad-109">Per iniziare subito a usare Azure Cloud Shell, vedere [Guida introduttiva a PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="4daad-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="4daad-110">Cloud Shell esegue PowerShell 6 in un contenitore Linux, per cui le funzionalità specifiche di Windows non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="4daad-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="4daad-111">Quando si è pronti per installare Azure PowerShell nel computer locale, seguire le istruzioni in [Installare il modulo Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="4daad-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="4daad-112">Accedere ad Azure</span><span class="sxs-lookup"><span data-stu-id="4daad-112">Sign in to Azure</span></span>

<span data-ttu-id="4daad-113">Accedere in modo interattivo con il cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="4daad-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="4daad-114">Ignorare questo passaggio se si usa Cloud Shell: La sessione di Azure Cloud Shell è già autenticata per l'ambiente, la sottoscrizione e il tenant che ha avviato la sessione Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="4daad-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="4daad-115">Se si risiede in un'area non degli Stati Uniti, usare il parametro `-Environment` per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="4daad-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="4daad-116">Recuperare il nome dell'ambiente per la propria area con il cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="4daad-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="4daad-117">Ad esempio, per accedere ad Azure Cina 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="4daad-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="4daad-118">Negli ambienti di PowerShell 5.1 verrà visualizzata una finestra di dialogo di accesso in cui specificare un nome utente e una password per l'account Azure.</span><span class="sxs-lookup"><span data-stu-id="4daad-118">In PowerShell 5.1 environments, you'll get a sign-in dialog to provide a username and password for your Azure account.</span></span> <span data-ttu-id="4daad-119">In tutte le altre versioni di PowerShell si otterrà un token da usare in [https://microsoft.com/devicelogin ].</span><span class="sxs-lookup"><span data-stu-id="4daad-119">On every other version of PowerShell, you'll get a token to use on [https://microsoft.com/devicelogin].</span></span>
<span data-ttu-id="4daad-120">Aprire questa pagina nel browser e immettere il token, quindi accedere con le credenziali dell'account Azure e autorizzare Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4daad-120">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span>

<span data-ttu-id="4daad-121">Dopo aver effettuato l'accesso, verrà visualizzato un messaggio indicante quale sottoscrizione di Azure è attiva.</span><span class="sxs-lookup"><span data-stu-id="4daad-121">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="4daad-122">Se l'account include più sottoscrizioni di Azure e se ne vuole selezionare una diversa, recuperare le sottoscrizioni disponibili con [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) e usare il cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext) con l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4daad-122">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="4daad-123">Per altre informazioni sulla gestione delle sottoscrizioni di Azure in Azure PowerShell, vedere [Usare più sottoscrizioni di Azure](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="4daad-123">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="4daad-124">Dopo aver effettuato l'accesso è possibile usare i cmdlet di Azure PowerShell per l'accesso e la gestione delle risorse nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4daad-124">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="4daad-125">Per altre informazioni sul processo di accesso e i metodi di autenticazione, vedere [Accedere con Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="4daad-125">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="4daad-126">Trovare i comandi</span><span class="sxs-lookup"><span data-stu-id="4daad-126">Find commands</span></span>

<span data-ttu-id="4daad-127">I cmdlet di Azure PowerShell seguono una convenzione di denominazione standard per PowerShell, `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="4daad-127">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="4daad-128">Il verbo descrive l'azione (alcuni esempi includono `New`, `Get`, `Set`, `Remove`) e il nome descrive il tipo di risorsa (alcuni esempi includono `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="4daad-128">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="4daad-129">I nomi in Azure PowerShell iniziano sempre con il prefisso `Az`.</span><span class="sxs-lookup"><span data-stu-id="4daad-129">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="4daad-130">Per l'elenco completo dei verbi standard, vedere [Verbi approvati per i comandi di PowerShell](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="4daad-130">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="4daad-131">Conoscere i nomi, i verbi e i moduli di Azure PowerShell disponibili consente di trovare i comandi con il cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="4daad-131">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="4daad-132">Ad esempio, per trovare tutti i comandi correlati alla macchina virtuale che usano il verbo `Get`:</span><span class="sxs-lookup"><span data-stu-id="4daad-132">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="4daad-133">Per facilitare la ricerca di comandi comuni, questa tabella elenca il tipo di risorsa, il modulo di Azure PowerShell corrispondente e il prefisso del nome da usare con `Get-Command`:</span><span class="sxs-lookup"><span data-stu-id="4daad-133">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="4daad-134">Tipo di risorsa</span><span class="sxs-lookup"><span data-stu-id="4daad-134">Resource type</span></span> | <span data-ttu-id="4daad-135">Modulo di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4daad-135">Azure PowerShell module</span></span> | <span data-ttu-id="4daad-136">Prefisso del nome</span><span class="sxs-lookup"><span data-stu-id="4daad-136">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="4daad-137">Gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4daad-137">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="4daad-138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4daad-138">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="4daad-139">Macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="4daad-139">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="4daad-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4daad-140">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="4daad-141">Account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4daad-141">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="4daad-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4daad-142">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="4daad-143">Insieme di credenziali di chiave</span><span class="sxs-lookup"><span data-stu-id="4daad-143">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="4daad-144">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4daad-144">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="4daad-145">Applicazioni Web</span><span class="sxs-lookup"><span data-stu-id="4daad-145">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="4daad-146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4daad-146">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="4daad-147">Database SQL</span><span class="sxs-lookup"><span data-stu-id="4daad-147">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="4daad-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4daad-148">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="4daad-149">Per un elenco completo dei moduli di Azure PowerShell, vedere l'[elenco di moduli di Azure PowerShell](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) ospitato in GitHub.</span><span class="sxs-lookup"><span data-stu-id="4daad-149">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="4daad-150">Modelli di avvio rapido ed esercitazioni per apprendere le nozioni di base di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4daad-150">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="4daad-151">Per iniziare a usare Azure PowerShell, provare un'esercitazione dettagliata per la configurazione delle macchine virtuali e per imparare a eseguire query nelle stesse.</span><span class="sxs-lookup"><span data-stu-id="4daad-151">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="4daad-152">Creare macchine virtuali con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4daad-152">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="4daad-153">Sono disponibili anche guide introduttive di Azure PowerShell per altri servizi di Azure più diffusi:</span><span class="sxs-lookup"><span data-stu-id="4daad-153">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="4daad-154">Creare un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4daad-154">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="4daad-155">Trasferire oggetti da e verso Archiviazione BLOB di Azure</span><span class="sxs-lookup"><span data-stu-id="4daad-155">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="4daad-156">Creare e recuperare segreti da Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="4daad-156">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="4daad-157">Creare un database SQL di Azure e un firewall</span><span class="sxs-lookup"><span data-stu-id="4daad-157">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="4daad-158">Eseguire un contenitore in Istanze di Azure Container</span><span class="sxs-lookup"><span data-stu-id="4daad-158">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="4daad-159">Creare un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="4daad-159">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="4daad-160">Creare un'istanza di Load Balancer Standard</span><span class="sxs-lookup"><span data-stu-id="4daad-160">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="4daad-161">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="4daad-161">Next steps</span></span>

* [<span data-ttu-id="4daad-162">Accedere con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4daad-162">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="4daad-163">Gestire le sottoscrizioni di Azure con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4daad-163">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="4daad-164">Creare entità servizio di Azure con Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4daad-164">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="4daad-165">Ottenere informazioni dalla community:</span><span class="sxs-lookup"><span data-stu-id="4daad-165">Get help from the community:</span></span>
  * [<span data-ttu-id="4daad-166">Forum Azure su MSDN</span><span class="sxs-lookup"><span data-stu-id="4daad-166">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="4daad-167">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="4daad-167">Stack Overflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
