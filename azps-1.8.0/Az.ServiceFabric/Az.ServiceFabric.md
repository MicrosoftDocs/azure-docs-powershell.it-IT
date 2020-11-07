---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93673371"
---
# <span data-ttu-id="dcf11-101">Modulo AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcf11-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="dcf11-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcf11-102">Description</span></span>
<span data-ttu-id="dcf11-103">Modulo tessuto di Azure Service che consente di automatizzare le operazioni di fine-2-fine come la creazione di un cluster sicuro, il rollforward dei certificati cluster, l'aggiunta o la rimozione di nodi dal cluster e così via. L'elenco completo di tutte le operazioni è elencato di seguito.</span><span class="sxs-lookup"><span data-stu-id="dcf11-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="dcf11-104">Cmdlet AZ. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcf11-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="dcf11-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="dcf11-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="dcf11-106">Aggiungere un nuovo certificato ai set di scale della macchina virtuale che compongono il cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="dcf11-107">Il certificato è destinato a essere usato come certificato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dcf11-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="dcf11-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="dcf11-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="dcf11-109">Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.</span><span class="sxs-lookup"><span data-stu-id="dcf11-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="dcf11-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="dcf11-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="dcf11-111">Aggiungere un certificato di cluster secondario al cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="dcf11-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="dcf11-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="dcf11-113">Aggiungere nodi al tipo di nodo specifico nel cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="dcf11-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="dcf11-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="dcf11-115">Aggiungere un nuovo tipo di nodo al cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="dcf11-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="dcf11-116">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="dcf11-116">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="dcf11-117">Ottenere i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="dcf11-118">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="dcf11-118">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="dcf11-119">Questo comando usa i certificati forniti dai certificati autofirmati o generati dal sistema per configurare un nuovo cluster di servizi in tessuto.</span><span class="sxs-lookup"><span data-stu-id="dcf11-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="dcf11-120">Può usare un modello predefinito o un modello personalizzato che fornisci.</span><span class="sxs-lookup"><span data-stu-id="dcf11-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="dcf11-121">È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dall'archivio chiavi.</span><span class="sxs-lookup"><span data-stu-id="dcf11-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="dcf11-122">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="dcf11-122">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="dcf11-123">Rimuovere il nome o i nomi dei certificati client o degli argomenti del certificato da usare per l'autenticazione del client nel cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="dcf11-124">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="dcf11-124">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="dcf11-125">Rimuovere un certificato cluster da usare per la sicurezza del cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="dcf11-126">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="dcf11-126">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="dcf11-127">Rimuovere i nodi dal tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="dcf11-128">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="dcf11-128">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="dcf11-129">Rimuovere un tipo di nodo completo da un cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="dcf11-130">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="dcf11-130">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="dcf11-131">Rimuovere una o più impostazioni del tessuto del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="dcf11-132">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="dcf11-132">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="dcf11-133">Aggiungere o aggiornare una o più impostazioni del tessuto del servizio al cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="dcf11-134">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="dcf11-134">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="dcf11-135">Modificare il tipo di aggiornamento del tessuto di servizio del cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="dcf11-136">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="dcf11-136">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="dcf11-137">Aggiornare il livello di durabilità o VmSku di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="dcf11-138">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="dcf11-138">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="dcf11-139">Aggiornare il livello di affidabilità del tipo di nodo principale in un cluster.</span><span class="sxs-lookup"><span data-stu-id="dcf11-139">Update the reliability tier of the primary node type in a cluster.</span></span>

