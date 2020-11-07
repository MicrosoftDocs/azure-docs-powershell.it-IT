---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 1ab1690d3c5fccca2994abc4958f3cf7e6a4e52d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93673324"
---
# <span data-ttu-id="c9ee7-101">Modulo AZ. StorageSync</span><span class="sxs-lookup"><span data-stu-id="c9ee7-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="c9ee7-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9ee7-102">Description</span></span>
<span data-ttu-id="c9ee7-103">I cmdlet nel modulo di sincronizzazione dello storage consentono di gestire le operazioni relative alla sincronizzazione di file di Azure in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="c9ee7-104">Cmdlet AZ. StorageSync</span><span class="sxs-lookup"><span data-stu-id="c9ee7-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="c9ee7-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9ee7-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="c9ee7-106">Questo comando elenca tutti gli endpoint del cloud all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="c9ee7-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c9ee7-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="c9ee7-108">Questo comando elenca tutti i gruppi di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="c9ee7-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="c9ee7-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="c9ee7-110">Questo comando elenca tutti i server registrati in un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="c9ee7-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9ee7-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="c9ee7-112">Questo comando elenca tutti gli endpoint del server all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="c9ee7-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c9ee7-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="c9ee7-114">Questo comando elenca tutti i servizi di sincronizzazione dello storage all'interno di un ambito specifico del gruppo sottoscrizione/risorsa.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="c9ee7-115">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="c9ee7-115">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="c9ee7-116">Controlla i potenziali problemi di compatibilità tra il sistema e la sincronizzazione di file Azure.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-116">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="c9ee7-117">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="c9ee7-117">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="c9ee7-118">Questo comando richiama tutti i file di livello sul disco locale.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-118">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="c9ee7-119">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9ee7-119">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="c9ee7-120">Questo comando crea un endpoint cloud di sincronizzazione di Azure file in un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-120">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="c9ee7-121">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c9ee7-121">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="c9ee7-122">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-122">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="c9ee7-123">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9ee7-123">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="c9ee7-124">Questo comando crea un nuovo endpoint server in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-124">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="c9ee7-125">Questo consente al percorso specificato sul server di avviare la sincronizzazione dei file con altri endpoint nel gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-125">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="c9ee7-126">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c9ee7-126">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="c9ee7-127">Questo comando crea un nuovo servizio di sincronizzazione dello spazio di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-127">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="c9ee7-128">Registro-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="c9ee7-128">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="c9ee7-129">Questo comando registra un server in un servizio di sincronizzazione dello spazio di archiviazione che crea una relazione di trust.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-129">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="c9ee7-130">PowerShell o Azure Portal possono quindi essere usati per configurare la sincronizzazione nel server.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-130">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="c9ee7-131">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9ee7-131">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="c9ee7-132">Questo comando eliminerà l'endpoint cloud specificato da un gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-132">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="c9ee7-133">Senza almeno un endpoint nuvola, non è possibile sincronizzare altri endpoint del server in questo gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-133">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="c9ee7-134">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="c9ee7-134">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="c9ee7-135">Questo comando eliminerà il gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-135">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="c9ee7-136">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9ee7-136">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="c9ee7-137">Questo comando eliminerà l'endpoint server specificato.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-137">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="c9ee7-138">La sincronizzazione con questa posizione si arresta immediatamente.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-138">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="c9ee7-139">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c9ee7-139">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="c9ee7-140">Questo comando eliminerà il servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-140">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="c9ee7-141">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="c9ee7-141">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="c9ee7-142">Usare solo per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-142">Use for troubleshooting only.</span></span> <span data-ttu-id="c9ee7-143">Questo comando consente di eseguire il rollback del certificato del server di sincronizzazione dello storage usato per descrivere l'identità del server al servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-143">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="c9ee7-144">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9ee7-144">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="c9ee7-145">Questo comando consente di modificare i parametri regolabili di un endpoint server.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-145">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="c9ee7-146">Annullamento della registrazione-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="c9ee7-146">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="c9ee7-147">Avviso: l'annullamento della registrazione di un server comporterà l'eliminazione a cascata di tutti gli endpoint server nel server.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-147">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="c9ee7-148">Questo comando Annulla la registrazione di un server dal servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c9ee7-148">This command will unregister a server from it's storage sync service.</span></span>