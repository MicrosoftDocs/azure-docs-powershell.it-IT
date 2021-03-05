---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: b35ba1bcd976bbc563dd8e3ad6640279a5a8a1dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963629"
---
# <span data-ttu-id="2bcb6-101">Modulo Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2bcb6-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="2bcb6-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bcb6-102">Description</span></span>
<span data-ttu-id="2bcb6-103">Modulo Azure Service Fabric che consente di automatizzare le operazioni di fine 2, come la creazione di un cluster sicuro, il rolling over di certificati cluster, l'aggiunta o la rimozione di nodi dal cluster e così via. Di seguito è riportato l'elenco completo di tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="2bcb6-104">Cmdlet Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2bcb6-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="2bcb6-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2bcb6-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="2bcb6-106">Aggiungere il nome comune o l'immagine thumbprint al cluster ai fini dell'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="2bcb6-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2bcb6-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="2bcb6-108">Aggiungere un certificato cluster secondario al cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="2bcb6-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2bcb6-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="2bcb6-110">Aggiungere il nome comune del certificato o l'immagine thumbprint al cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="2bcb6-111">Il certificato verrà registrato di nuovo nel cluster ai fini dell'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="2bcb6-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="2bcb6-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="2bcb6-113">Aggiungere l'estensione della macchina virtuale al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="2bcb6-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="2bcb6-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="2bcb6-115">Aggiungere il segreto certificato al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="2bcb6-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2bcb6-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="2bcb6-117">Aggiungere i nodi al tipo di nodo specifico nel cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="2bcb6-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2bcb6-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="2bcb6-119">Aggiungere un nuovo tipo di nodo al cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="2bcb6-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2bcb6-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="2bcb6-121">Ottenere i dettagli dell'applicazione Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="2bcb6-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2bcb6-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="2bcb6-123">Ottenere i dettagli sul tipo di applicazione Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="2bcb6-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2bcb6-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="2bcb6-125">Ottenere i dettagli della versione del tipo di applicazione Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="2bcb6-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2bcb6-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="2bcb6-127">Informazioni dettagliate sulle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="2bcb6-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2bcb6-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="2bcb6-129">Ottenere i dettagli delle risorse del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="2bcb6-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2bcb6-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="2bcb6-131">Ottenere i dettagli delle risorse per il tipo di nodo gestito.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="2bcb6-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2bcb6-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="2bcb6-133">Ottenere i dettagli del servizio Service Fabric nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="2bcb6-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2bcb6-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="2bcb6-135">Creare una nuova applicazione di tessuto di servizio nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="2bcb6-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2bcb6-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="2bcb6-137">Creare un nuovo tipo di applicazione tessuto di servizio nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="2bcb6-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2bcb6-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="2bcb6-139">Creare una nuova versione del tipo di applicazione nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="2bcb6-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2bcb6-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="2bcb6-141">Questo comando usa i certificati forniti dall'utente o i certificati autofirmati generati dal sistema per configurare un nuovo cluster di tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="2bcb6-142">Può usare un modello predefinito o un modello personalizzato specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="2bcb6-143">È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dal vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="2bcb6-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2bcb6-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="2bcb6-145">Creare un nuovo cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="2bcb6-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2bcb6-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="2bcb6-147">Creare una nuova risorsa tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-147">Create new node type resource.</span></span>

### [<span data-ttu-id="2bcb6-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2bcb6-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="2bcb6-149">Creare un nuovo servizio di tessuto di servizio nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="2bcb6-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2bcb6-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="2bcb6-151">Rimuovere un'applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-151">Remove an application from the cluster.</span></span> <span data-ttu-id="2bcb6-152">Tutti i servizi dell'applicazione verranno così rimosso.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="2bcb6-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2bcb6-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="2bcb6-154">Rimuovere un tipo di applicazione da un tipo di applicazione del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="2bcb6-155">In questo modo verranno rimuovono tutte le versioni dei tipi in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="2bcb6-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2bcb6-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="2bcb6-157">Rimuovere la versione service fabric di un tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="2bcb6-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2bcb6-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="2bcb6-159">Rimuovere uno o più certificati client o i nomi degli oggetto del certificato usati per l'autenticazione client nel cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="2bcb6-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="2bcb6-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="2bcb6-161">Rimuovere un certificato cluster da usare per la sicurezza dei cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="2bcb6-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2bcb6-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="2bcb6-163">Rimuovere la risorsa cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="2bcb6-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="2bcb6-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="2bcb6-165">Certificato client di remvoe in base all'immagine thumbprint o al nome comune.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="2bcb6-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2bcb6-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="2bcb6-167">Rimuovere il tipo di nodo o nodi specifici all'interno del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="2bcb6-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="2bcb6-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="2bcb6-169">Rimuovere l'estensione della macchina virtuale dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="2bcb6-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2bcb6-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="2bcb6-171">Rimuovere i nodi dal tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="2bcb6-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="2bcb6-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="2bcb6-173">Rimuovere un tipo di nodo completo da un cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="2bcb6-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2bcb6-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="2bcb6-175">Rimuovere un servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="2bcb6-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2bcb6-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="2bcb6-177">Rimuovere una o più impostazioni di Tessuto di servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="2bcb6-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2bcb6-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="2bcb6-179">Riavviare nodi specifici dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="2bcb6-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2bcb6-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="2bcb6-181">Impostare le proprietà delle risorse cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="2bcb6-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="2bcb6-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="2bcb6-183">Imposta le proprietà delle risorse del tipo di nodo o esegue azioni di reimage su specifici tipi di nodo con il parametro -Reimage.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="2bcb6-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="2bcb6-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="2bcb6-185">Aggiungere o aggiornare una o più impostazioni di Tessuto di servizio al cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="2bcb6-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="2bcb6-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="2bcb6-187">Modificare il tipo di aggiornamento Service Fabric del cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="2bcb6-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2bcb6-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="2bcb6-189">Aggiornare un'applicazione di tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-189">Update a service fabric application.</span></span> <span data-ttu-id="2bcb6-190">In questo modo è possibile aggiornare i parametri dell'applicazione e/o aggiornare la versione del tipo di applicazione che attiverà l'aggiornamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="2bcb6-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="2bcb6-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="2bcb6-192">Aggiornare il livello di durabilità o VmSKU di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="2bcb6-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="2bcb6-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="2bcb6-194">Aggiornare il livello di affidabilità del tipo di nodo primario in un cluster.</span><span class="sxs-lookup"><span data-stu-id="2bcb6-194">Update the reliability tier of the primary node type in a cluster.</span></span>

