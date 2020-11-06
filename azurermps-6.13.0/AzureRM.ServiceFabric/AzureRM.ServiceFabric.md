---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 6d93775a028e7a590a8da9cc008640fb8484bdf2
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490114"
---
# <span data-ttu-id="5f511-101">Modulo AzureRM. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5f511-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="5f511-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f511-102">Description</span></span>
<span data-ttu-id="5f511-103">Modulo tessuto di Azure Service che consente di automatizzare le operazioni di fine-2-fine come la creazione di un cluster sicuro, il rollforward dei certificati cluster, l'aggiunta o la rimozione di nodi dal cluster e così via. L'elenco completo di tutte le operazioni è elencato di seguito.</span><span class="sxs-lookup"><span data-stu-id="5f511-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="5f511-104">Cmdlet AzureRM. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5f511-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="5f511-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="5f511-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="5f511-106">Aggiungere un nuovo certificato ai set di scale della macchina virtuale che compongono il cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="5f511-107">Il certificato è destinato a essere usato come certificato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f511-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="5f511-108">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5f511-108">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="5f511-109">Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.</span><span class="sxs-lookup"><span data-stu-id="5f511-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="5f511-110">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="5f511-110">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="5f511-111">Aggiungere un certificato di cluster secondario al cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="5f511-112">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5f511-112">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="5f511-113">Aggiungere nodi al tipo di nodo specifico nel cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="5f511-114">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="5f511-114">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="5f511-115">Aggiungere un nuovo tipo di nodo al cluster esistente.</span><span class="sxs-lookup"><span data-stu-id="5f511-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="5f511-116">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="5f511-116">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="5f511-117">Ottenere i dettagli delle risorse del cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="5f511-118">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="5f511-118">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="5f511-119">Questo comando usa i certificati forniti dai certificati autofirmati o generati dal sistema per configurare un nuovo cluster di servizi in tessuto.</span><span class="sxs-lookup"><span data-stu-id="5f511-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="5f511-120">Può usare un modello predefinito o un modello personalizzato che fornisci.</span><span class="sxs-lookup"><span data-stu-id="5f511-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="5f511-121">È possibile specificare una cartella in cui esportare i certificati autofirmati o recuperarli in un secondo momento dall'archivio chiavi.</span><span class="sxs-lookup"><span data-stu-id="5f511-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="5f511-122">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5f511-122">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="5f511-123">Rimuovere il nome o i nomi dei certificati client o degli argomenti del certificato da usare per l'autenticazione del client nel cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="5f511-124">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="5f511-124">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="5f511-125">Rimuovere un certificato cluster da usare per la sicurezza del cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="5f511-126">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5f511-126">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="5f511-127">Rimuovere i nodi dal tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="5f511-128">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="5f511-128">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="5f511-129">Rimuovere un tipo di nodo completo da un cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="5f511-130">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="5f511-130">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="5f511-131">Rimuovere una o più impostazioni del tessuto del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="5f511-132">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="5f511-132">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="5f511-133">Aggiungere o aggiornare una o più impostazioni del tessuto del servizio al cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="5f511-134">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="5f511-134">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="5f511-135">Modificare il tipo di aggiornamento del tessuto di servizio del cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="5f511-136">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="5f511-136">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="5f511-137">Aggiornare il livello di durabilità o VmSku di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="5f511-138">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="5f511-138">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="5f511-139">Aggiornare il livello di affidabilità del tipo di nodo principale in un cluster.</span><span class="sxs-lookup"><span data-stu-id="5f511-139">Update the reliability tier of the primary node type in a cluster.</span></span>

