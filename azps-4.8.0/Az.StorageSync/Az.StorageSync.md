---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188712"
---
# <span data-ttu-id="f1529-101">Modulo AZ. StorageSync</span><span class="sxs-lookup"><span data-stu-id="f1529-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="f1529-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1529-102">Description</span></span>
<span data-ttu-id="f1529-103">I cmdlet nel modulo di sincronizzazione dello storage consentono di gestire le operazioni relative alla sincronizzazione di file di Azure in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f1529-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="f1529-104">Cmdlet AZ. StorageSync</span><span class="sxs-lookup"><span data-stu-id="f1529-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="f1529-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1529-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="f1529-106">Questo comando elenca tutti gli endpoint del cloud all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="f1529-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="f1529-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f1529-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="f1529-108">Questo comando elenca tutti i gruppi di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="f1529-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="f1529-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="f1529-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="f1529-110">Questo comando elenca tutti i server registrati in un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="f1529-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="f1529-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1529-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="f1529-112">Questo comando elenca tutti gli endpoint del server all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="f1529-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="f1529-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f1529-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="f1529-114">Questo comando elenca tutti i servizi di sincronizzazione dello storage all'interno di un ambito specifico del gruppo sottoscrizione/risorsa.</span><span class="sxs-lookup"><span data-stu-id="f1529-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="f1529-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="f1529-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="f1529-116">Questo comando può essere usato per avviare manualmente il rilevamento delle modifiche agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f1529-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="f1529-117">Può essere destinata all'intera condivisione, sottocartella o set di file.</span><span class="sxs-lookup"><span data-stu-id="f1529-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="f1529-118">Può essere rilevato un massimo di 10.000 modifiche.</span><span class="sxs-lookup"><span data-stu-id="f1529-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="f1529-119">Se l'ambito delle modifiche è noto, limitare l'esecuzione di questo comando alle parti dello spazio dei nomi, in modo che il rilevamento della modifica possa terminare rapidamente e all'interno di un limite di modifiche di 10.000.</span><span class="sxs-lookup"><span data-stu-id="f1529-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="f1529-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="f1529-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="f1529-121">Controlla i potenziali problemi di compatibilità tra il sistema e la sincronizzazione di file Azure.</span><span class="sxs-lookup"><span data-stu-id="f1529-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="f1529-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="f1529-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="f1529-123">Questo comando richiama tutti i file di livello sul disco locale.</span><span class="sxs-lookup"><span data-stu-id="f1529-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="f1529-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1529-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="f1529-125">Questo comando crea un endpoint cloud di sincronizzazione di Azure file in un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f1529-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="f1529-126">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f1529-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="f1529-127">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="f1529-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="f1529-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1529-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="f1529-129">Questo comando crea un nuovo endpoint server in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="f1529-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="f1529-130">Questo consente al percorso specificato sul server di avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f1529-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="f1529-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f1529-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="f1529-132">Questo comando crea un nuovo servizio di sincronizzazione dello spazio di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f1529-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="f1529-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f1529-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="f1529-134">Questo comando imposta un servizio di sincronizzazione dello storage in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f1529-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="f1529-135">Registro-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="f1529-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="f1529-136">Questo comando registra un server in un servizio di sincronizzazione dello spazio di archiviazione che crea una relazione di trust.</span><span class="sxs-lookup"><span data-stu-id="f1529-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="f1529-137">PowerShell o Azure Portal possono quindi essere usati per configurare la sincronizzazione nel server.</span><span class="sxs-lookup"><span data-stu-id="f1529-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="f1529-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1529-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="f1529-139">Questo comando eliminerà l'endpoint cloud specificato da un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f1529-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="f1529-140">Senza almeno un endpoint nuvola, non è possibile sincronizzare altri endpoint del server in questo gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f1529-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="f1529-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f1529-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="f1529-142">Questo comando eliminerà il gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="f1529-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="f1529-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1529-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="f1529-144">Questo comando eliminerà l'endpoint server specificato.</span><span class="sxs-lookup"><span data-stu-id="f1529-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="f1529-145">La sincronizzazione con questa posizione si arresta immediatamente.</span><span class="sxs-lookup"><span data-stu-id="f1529-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="f1529-146">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f1529-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="f1529-147">Questo comando eliminerà il servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="f1529-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="f1529-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="f1529-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="f1529-149">Usare solo per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="f1529-149">Use for troubleshooting only.</span></span> <span data-ttu-id="f1529-150">Questo comando consente di eseguire il rollback del certificato del server di sincronizzazione dello storage usato per descrivere l'identità del server al servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f1529-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="f1529-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1529-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="f1529-152">Questo comando consente di modificare i parametri regolabili di un endpoint server.</span><span class="sxs-lookup"><span data-stu-id="f1529-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="f1529-153">Annullamento della registrazione-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="f1529-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="f1529-154">Avviso: l'annullamento della registrazione di un server comporterà l'eliminazione a cascata di tutti gli endpoint server nel server.</span><span class="sxs-lookup"><span data-stu-id="f1529-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="f1529-155">Questo comando Annulla la registrazione di un server dal servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f1529-155">This command will unregister a server from it's storage sync service.</span></span>

