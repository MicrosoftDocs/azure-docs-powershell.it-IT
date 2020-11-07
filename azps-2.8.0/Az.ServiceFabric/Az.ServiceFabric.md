---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: d94e7001df730b22fb900b284c6fac47b5d81b8b
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/15/2019
ms.locfileid: "93673562"
---
# <span data-ttu-id="25b8e-101">Modulo AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="25b8e-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="25b8e-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25b8e-102">Description</span></span>
<span data-ttu-id="25b8e-103">Modulo tessuto di Azure Service che consente di automatizzare le operazioni di fine-2-fine come la creazione di un cluster sicuro, il rollforward dei certificati cluster, l'aggiunta o la rimozione di nodi dal cluster e così via. L'elenco completo di tutte le operazioni è elencato di seguito.</span><span class="sxs-lookup"><span data-stu-id="25b8e-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="25b8e-104">Cmdlet AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="25b8e-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="25b8e-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="25b8e-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="25b8e-106">Aggiungere un nuovo certificato ai set di scale della macchina virtuale che compongono il cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="25b8e-107">Il certificato è destinato a essere usato come certificato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25b8e-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="25b8e-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="25b8e-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="25b8e-109">Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.</span><span class="sxs-lookup"><span data-stu-id="25b8e-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="25b8e-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="25b8e-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="25b8e-111">Aggiungere un certificato di cluster secondario al cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="25b8e-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="25b8e-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="25b8e-113">Aggiungere nodi al tipo di nodo specifico nel cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="25b8e-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="25b8e-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="25b8e-115">Aggiungere un nuovo tipo di nodo al cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="25b8e-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="25b8e-116">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="25b8e-116">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="25b8e-117">Ottenere i dettagli delle applicazioni in tessuto di servizio.</span><span class="sxs-lookup"><span data-stu-id="25b8e-117">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="25b8e-118">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="25b8e-118">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="25b8e-119">Ottenere i dettagli del tipo di applicazione tessuto servizio.</span><span class="sxs-lookup"><span data-stu-id="25b8e-119">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="25b8e-120">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="25b8e-120">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="25b8e-121">Ottenere i dettagli della versione del tipo di servizio in tessuto.</span><span class="sxs-lookup"><span data-stu-id="25b8e-121">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="25b8e-122">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="25b8e-122">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="25b8e-123">Ottenere i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-123">Get the cluster resource details.</span></span>

### [<span data-ttu-id="25b8e-124">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="25b8e-124">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="25b8e-125">Ottenere i dettagli del servizio Fabric servizio nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="25b8e-125">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="25b8e-126">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="25b8e-126">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="25b8e-127">Creare un'applicazione nuova in tessuto del servizio in un gruppo di risorse e un cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="25b8e-127">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="25b8e-128">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="25b8e-128">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="25b8e-129">Creare un nuovo tipo di applicazione in tessuto del servizio sotto il gruppo e il cluster di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="25b8e-129">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="25b8e-130">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="25b8e-130">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="25b8e-131">Creare una nuova versione del tipo di applicazione sotto il gruppo e il cluster di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="25b8e-131">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="25b8e-132">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="25b8e-132">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="25b8e-133">Questo comando usa i certificati forniti dai certificati autofirmati o generati dal sistema per configurare un nuovo cluster di servizi in tessuto.</span><span class="sxs-lookup"><span data-stu-id="25b8e-133">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="25b8e-134">Può usare un modello predefinito o un modello personalizzato che fornisci.</span><span class="sxs-lookup"><span data-stu-id="25b8e-134">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="25b8e-135">È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dall'archivio chiavi.</span><span class="sxs-lookup"><span data-stu-id="25b8e-135">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="25b8e-136">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="25b8e-136">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="25b8e-137">Creare un nuovo servizio tessuto servizio nell'applicazione e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="25b8e-137">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="25b8e-138">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="25b8e-138">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="25b8e-139">Rimuovere un'applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-139">Remove an application from the cluster.</span></span> <span data-ttu-id="25b8e-140">Verranno rimossi tutti i servizi sotto l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25b8e-140">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="25b8e-141">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="25b8e-141">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="25b8e-142">Rimuovere il tessuto del servizio un tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-142">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="25b8e-143">In questo modo verranno rimosse tutte le versioni di tipo in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="25b8e-143">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="25b8e-144">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="25b8e-144">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="25b8e-145">Rimuovere il tessuto di servizio una versione del tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-145">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="25b8e-146">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="25b8e-146">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="25b8e-147">Rimuovere il nome o i nomi dei certificati client o degli argomenti del certificato da usare per l'autenticazione del client nel cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-147">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="25b8e-148">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="25b8e-148">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="25b8e-149">Rimuovere un certificato cluster da usare per la sicurezza del cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-149">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="25b8e-150">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="25b8e-150">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="25b8e-151">Rimuovere i nodi dal tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-151">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="25b8e-152">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="25b8e-152">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="25b8e-153">Rimuovere un tipo di nodo completo da un cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-153">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="25b8e-154">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="25b8e-154">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="25b8e-155">Rimuovere un servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-155">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="25b8e-156">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="25b8e-156">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="25b8e-157">Rimuovere una o più impostazioni del tessuto del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-157">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="25b8e-158">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="25b8e-158">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="25b8e-159">Aggiungere o aggiornare una o più impostazioni del tessuto del servizio al cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-159">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="25b8e-160">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="25b8e-160">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="25b8e-161">Modificare il tipo di aggiornamento del tessuto di servizio del cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-161">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="25b8e-162">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="25b8e-162">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="25b8e-163">Aggiornare un'applicazione fabric di servizi.</span><span class="sxs-lookup"><span data-stu-id="25b8e-163">Update a service fabric application.</span></span> <span data-ttu-id="25b8e-164">Questo consente di aggiornare i parametri dell'applicazione e/o aggiornare la versione del tipo di applicazione che attiverà un aggiornamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25b8e-164">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="25b8e-165">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="25b8e-165">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="25b8e-166">Aggiornare il livello di durabilità o VmSku di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-166">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="25b8e-167">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="25b8e-167">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="25b8e-168">Aggiornare il livello di affidabilità del tipo di nodo principale in un cluster.</span><span class="sxs-lookup"><span data-stu-id="25b8e-168">Update the reliability tier of the primary node type in a cluster.</span></span>

