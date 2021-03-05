---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 9acaa8a562ffe88631a587703a3300ac13f73224
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973181"
---
# <span data-ttu-id="3b916-101">Modulo Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3b916-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="3b916-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b916-102">Description</span></span>
<span data-ttu-id="3b916-103">I cmdlet del modulo Sincronizzazione archiviazione consentono di gestire le operazioni relative a Azure File Sync in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3b916-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="3b916-104">Cmdlet Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3b916-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="3b916-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b916-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="3b916-106">Questo comando elenca tutti gli endpoint cloud all'interno di un determinato gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3b916-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="3b916-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3b916-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="3b916-108">Questo comando elenca tutti i gruppi di sincronizzazione all'interno di un determinato servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3b916-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="3b916-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="3b916-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="3b916-110">Questo comando elenca tutti i server registrati con un determinato servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3b916-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="3b916-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b916-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="3b916-112">Questo comando elenca tutti gli endpoint del server all'interno di un determinato gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3b916-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="3b916-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3b916-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="3b916-114">Questo comando elenca tutti i servizi di sincronizzazione di archiviazione in un determinato ambito della sottoscrizione o del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b916-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="3b916-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="3b916-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="3b916-116">Questo comando può essere usato per avviare manualmente il rilevamento delle modifiche agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3b916-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="3b916-117">Può essere indirizzato all'intera condivisione, sottocartella o set di file.</span><span class="sxs-lookup"><span data-stu-id="3b916-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="3b916-118">Possono essere rilevate al massimo 10.000 modifiche.</span><span class="sxs-lookup"><span data-stu-id="3b916-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="3b916-119">Se si conosce l'ambito delle modifiche, limitare l'esecuzione di questo comando a parti dello spazio dei nomi, in modo che il rilevamento delle modifiche finisca rapidamente e entro un limite di 10.000 modifiche.</span><span class="sxs-lookup"><span data-stu-id="3b916-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="3b916-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="3b916-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="3b916-121">Verifica la presenza di potenziali problemi di compatibilità tra il sistema e Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="3b916-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="3b916-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="3b916-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="3b916-123">Questo comando richiama tutti i file a più livelli nel disco locale.</span><span class="sxs-lookup"><span data-stu-id="3b916-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="3b916-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b916-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="3b916-125">Questo comando crea un endpoint cloud di Azure File Sync in un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3b916-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="3b916-126">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3b916-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="3b916-127">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="3b916-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="3b916-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b916-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="3b916-129">Questo comando crea un nuovo endpoint server in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="3b916-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="3b916-130">In questo modo il percorso specificato nel server può avviare la sincronizzazione dei file con gli altri endpoint del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3b916-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="3b916-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3b916-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="3b916-132">Questo comando crea un nuovo servizio di sincronizzazione di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b916-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="3b916-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3b916-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="3b916-134">Questo comando imposta un servizio di sincronizzazione dello spazio di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b916-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="3b916-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="3b916-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="3b916-136">Questo comando registra un server in un servizio di sincronizzazione di archiviazione che crea una relazione di trust.</span><span class="sxs-lookup"><span data-stu-id="3b916-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="3b916-137">PowerShell o il portale di Azure possono quindi essere usati per configurare la sincronizzazione in questo server.</span><span class="sxs-lookup"><span data-stu-id="3b916-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="3b916-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b916-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="3b916-139">Questo comando eliminerà l'endpoint cloud specificato da un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3b916-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="3b916-140">Senza almeno un endpoint cloud, nessun altro endpoint server di questo gruppo di sincronizzazione può eseguire la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3b916-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="3b916-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3b916-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="3b916-142">Questo comando eliminerà il gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="3b916-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="3b916-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b916-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="3b916-144">Questo comando eliminerà l'endpoint server specificato.</span><span class="sxs-lookup"><span data-stu-id="3b916-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="3b916-145">La sincronizzazione con questa posizione verrà interrotta immediatamente.</span><span class="sxs-lookup"><span data-stu-id="3b916-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="3b916-146">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3b916-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="3b916-147">Questo comando eliminerà il servizio di sincronizzazione di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="3b916-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="3b916-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="3b916-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="3b916-149">Da usare solo per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="3b916-149">Use for troubleshooting only.</span></span> <span data-ttu-id="3b916-150">Questo comando esegue il roll roll del certificato del server di sincronizzazione di archiviazione usato per descrivere l'identità del server nel servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3b916-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="3b916-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b916-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="3b916-152">Questo comando consente di apportare modifiche ai parametri modificabili di un endpoint server.</span><span class="sxs-lookup"><span data-stu-id="3b916-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="3b916-153">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="3b916-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="3b916-154">Avviso: l'annullamento della registrazione di un server comporterà eliminazioni a catena di tutti gli endpoint server su questo server.</span><span class="sxs-lookup"><span data-stu-id="3b916-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="3b916-155">Questo comando anregistrerà un server del servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3b916-155">This command will unregister a server from it's storage sync service.</span></span>

