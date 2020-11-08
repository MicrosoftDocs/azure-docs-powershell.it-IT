---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200484"
---
# <span data-ttu-id="f8551-101">Modulo AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f8551-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="f8551-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8551-102">Description</span></span>
<span data-ttu-id="f8551-103">Modulo tessuto di Azure Service che consente di automatizzare le operazioni di fine-2-fine come la creazione di un cluster sicuro, il rollforward dei certificati cluster, l'aggiunta o la rimozione di nodi dal cluster e così via. L'elenco completo di tutte le operazioni è elencato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f8551-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="f8551-104">Cmdlet AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f8551-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="f8551-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f8551-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="f8551-106">Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.</span><span class="sxs-lookup"><span data-stu-id="f8551-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="f8551-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f8551-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="f8551-108">Aggiungere un certificato di cluster secondario al cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="f8551-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f8551-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="f8551-110">Aggiungere al cluster il nome comune o l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="f8551-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="f8551-111">Verrà registrato di nuovo il certificato per scopi di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="f8551-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="f8551-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="f8551-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="f8551-113">Aggiungere l'estensione VM al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="f8551-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="f8551-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="f8551-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="f8551-115">Aggiungere il segreto del certificato al tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="f8551-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="f8551-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f8551-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="f8551-117">Aggiungere nodi al tipo di nodo specifico nel cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="f8551-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f8551-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="f8551-119">Aggiungere un nuovo tipo di nodo al cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="f8551-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="f8551-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f8551-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="f8551-121">Ottenere i dettagli delle applicazioni in tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="f8551-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="f8551-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f8551-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="f8551-123">Ottenere i dettagli del tipo di applicazione tessuto servizio.</span><span class="sxs-lookup"><span data-stu-id="f8551-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="f8551-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f8551-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="f8551-125">Ottenere i dettagli della versione del tipo di servizio in tessuto.</span><span class="sxs-lookup"><span data-stu-id="f8551-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="f8551-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f8551-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="f8551-127">Ottenere i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="f8551-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f8551-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="f8551-129">Ottenere i dettagli delle risorse del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="f8551-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="f8551-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="f8551-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="f8551-131">Ottenere i dettagli delle risorse del tipo di nodo gestito.</span><span class="sxs-lookup"><span data-stu-id="f8551-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="f8551-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f8551-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="f8551-133">Ottenere i dettagli del servizio Fabric servizio nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="f8551-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="f8551-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f8551-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="f8551-135">Creare un'applicazione nuova in tessuto del servizio in un gruppo di risorse e un cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="f8551-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="f8551-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f8551-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="f8551-137">Creare un nuovo tipo di applicazione in tessuto del servizio sotto il gruppo e il cluster di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="f8551-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="f8551-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f8551-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="f8551-139">Creare una nuova versione del tipo di applicazione sotto il gruppo e il cluster di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="f8551-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="f8551-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f8551-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="f8551-141">Questo comando usa i certificati forniti dai certificati autofirmati o generati dal sistema per configurare un nuovo cluster di servizi in tessuto.</span><span class="sxs-lookup"><span data-stu-id="f8551-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="f8551-142">Può usare un modello predefinito o un modello personalizzato che fornisci.</span><span class="sxs-lookup"><span data-stu-id="f8551-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="f8551-143">È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dall'archivio chiavi.</span><span class="sxs-lookup"><span data-stu-id="f8551-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="f8551-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f8551-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="f8551-145">Creare un nuovo cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="f8551-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="f8551-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="f8551-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="f8551-147">Creare una nuova risorsa tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="f8551-147">Create new node type resource.</span></span>

### [<span data-ttu-id="f8551-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f8551-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="f8551-149">Creare un nuovo servizio tessuto servizio nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="f8551-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="f8551-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f8551-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="f8551-151">Rimuovere un'applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-151">Remove an application from the cluster.</span></span> <span data-ttu-id="f8551-152">Verranno rimossi tutti i servizi sotto l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8551-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="f8551-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f8551-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="f8551-154">Rimuovere il tessuto del servizio un tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="f8551-155">In questo modo verranno rimosse tutte le versioni di tipo in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="f8551-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="f8551-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f8551-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="f8551-157">Rimuovere il tessuto di servizio una versione del tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="f8551-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f8551-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="f8551-159">Rimuovere il nome o i nomi dei certificati client o degli argomenti del certificato da usare per l'autenticazione del client nel cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="f8551-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f8551-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="f8551-161">Rimuovere un certificato cluster da usare per la sicurezza del cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="f8551-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f8551-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="f8551-163">Rimuovi risorsa cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="f8551-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f8551-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="f8551-165">Remvoe certificato client per identificazione personale o nome comune.</span><span class="sxs-lookup"><span data-stu-id="f8551-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="f8551-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="f8551-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="f8551-167">Rimuovere il tipo di nodo o i nodi specifici all'interno del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="f8551-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="f8551-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="f8551-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="f8551-169">Rimuovere l'estensione VM dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="f8551-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="f8551-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f8551-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="f8551-171">Rimuovere i nodi dal tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="f8551-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f8551-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="f8551-173">Rimuovere un tipo di nodo completo da un cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="f8551-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f8551-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="f8551-175">Rimuovere un servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="f8551-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="f8551-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="f8551-177">Rimuovere una o più impostazioni del tessuto del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="f8551-178">Riavviare-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="f8551-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="f8551-179">Riavviare nodi specifici dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="f8551-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="f8551-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f8551-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="f8551-181">Impostare le proprietà delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="f8551-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="f8551-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="f8551-183">Imposta le proprietà delle risorse del tipo di nodo o esegue le azioni di riimmagine su specifiche Registrazione dispositivi del parametro tipo di nodo con-reimage.</span><span class="sxs-lookup"><span data-stu-id="f8551-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="f8551-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="f8551-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="f8551-185">Aggiungere o aggiornare una o più impostazioni del tessuto del servizio al cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="f8551-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="f8551-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="f8551-187">Modificare il tipo di aggiornamento del tessuto di servizio del cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="f8551-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f8551-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="f8551-189">Aggiornare un'applicazione fabric di servizi.</span><span class="sxs-lookup"><span data-stu-id="f8551-189">Update a service fabric application.</span></span> <span data-ttu-id="f8551-190">Questo consente di aggiornare i parametri dell'applicazione e/o aggiornare la versione del tipo di applicazione che attiverà un aggiornamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8551-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="f8551-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="f8551-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="f8551-192">Aggiornare il livello di durabilità o VmSku di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="f8551-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="f8551-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="f8551-194">Aggiornare il livello di affidabilità del tipo di nodo principale in un cluster.</span><span class="sxs-lookup"><span data-stu-id="f8551-194">Update the reliability tier of the primary node type in a cluster.</span></span>

