---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 9c71788abd7707931df2c25279c265bbe9967bbf
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490329"
---
# <span data-ttu-id="e281d-101">Modulo AzureRM. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e281d-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="e281d-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e281d-102">Description</span></span>
<span data-ttu-id="e281d-103">Modulo tessuto di Azure Service che consente di automatizzare le operazioni di fine-2-fine come la creazione di un cluster sicuro, il rollforward dei certificati cluster, l'aggiunta o la rimozione di nodi dal cluster e così via. L'elenco completo di tutte le operazioni è elencato di seguito.</span><span class="sxs-lookup"><span data-stu-id="e281d-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="e281d-104">Cmdlet AzureRM. ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e281d-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="e281d-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="e281d-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="e281d-106">Aggiungere un certificato che verrà usato come certificato dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="e281d-106">Add a certificate that will be used as application certificate</span></span>

### [<span data-ttu-id="e281d-107">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e281d-107">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="e281d-108">Aggiungere il nome o l'identificazione personale comune alle impostazioni del cluster per l'autenticazione del client</span><span class="sxs-lookup"><span data-stu-id="e281d-108">Add common name or thumbprint to the cluster settings for client authentication</span></span>

### [<span data-ttu-id="e281d-109">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e281d-109">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="e281d-110">Aggiungere un certificato di cluster secondario al cluster per il rollforward del certificato esistente</span><span class="sxs-lookup"><span data-stu-id="e281d-110">Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span> 

### [<span data-ttu-id="e281d-111">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e281d-111">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="e281d-112">Aggiungere nodi/VM a un tipo di nodo specifico a un cluster</span><span class="sxs-lookup"><span data-stu-id="e281d-112">Add nodes/VMs to a specific node type to a cluster</span></span>

### [<span data-ttu-id="e281d-113">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="e281d-113">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="e281d-114">Aggiungere un tipo di nodo/VM a un cluster esistente</span><span class="sxs-lookup"><span data-stu-id="e281d-114">Add a node type/VMs to an existing cluster</span></span>

### [<span data-ttu-id="e281d-115">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e281d-115">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="e281d-116">Ottenere i dettagli della risorsa cluster</span><span class="sxs-lookup"><span data-stu-id="e281d-116">Get the details of the cluster resource</span></span> 

### [<span data-ttu-id="e281d-117">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e281d-117">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="e281d-118">Creare un nuovo cluster di ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="e281d-118">Create an new ServiceFabric cluster.</span></span> <span data-ttu-id="e281d-119">Questo comando include molti overload per coprire diversi scenari</span><span class="sxs-lookup"><span data-stu-id="e281d-119">This command has many overloads to cover various scenarios</span></span>

### [<span data-ttu-id="e281d-120">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e281d-120">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="e281d-121">Rimuovere il certificato client dall'uso per accedere al cluster</span><span class="sxs-lookup"><span data-stu-id="e281d-121">Remove client certificate from being used to access the cluster</span></span>

### [<span data-ttu-id="e281d-122">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="e281d-122">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="e281d-123">Rimuovere il certificato di cluster da usare per la sicurezza del cluster</span><span class="sxs-lookup"><span data-stu-id="e281d-123">Remove cluster certificate from being used for cluster security</span></span>

### [<span data-ttu-id="e281d-124">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e281d-124">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="e281d-125">Rimuovere nodi dal tipo di nodo specifico da un cluster</span><span class="sxs-lookup"><span data-stu-id="e281d-125">Remove nodes from the specific node type from a cluster</span></span>

### [<span data-ttu-id="e281d-126">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="e281d-126">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="e281d-127">Rimuovere un tipo di nodo da un cluster</span><span class="sxs-lookup"><span data-stu-id="e281d-127">Remove a node type from a cluster</span></span>

### [<span data-ttu-id="e281d-128">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="e281d-128">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="e281d-129">Rimuovere una o più impostazioni di ServiceFabric dal cluster</span><span class="sxs-lookup"><span data-stu-id="e281d-129">Remove one or more ServiceFabric settings from the cluster</span></span>

### [<span data-ttu-id="e281d-130">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="e281d-130">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="e281d-131">Aggiungere o aggiornare una o più impostazioni di ServiceFabric al cluster</span><span class="sxs-lookup"><span data-stu-id="e281d-131">Add or update one or more ServiceFabric settings to the cluster</span></span>

### [<span data-ttu-id="e281d-132">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="e281d-132">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="e281d-133">Modificare il tipo di aggiornamento di ServiceFabric di un cluster</span><span class="sxs-lookup"><span data-stu-id="e281d-133">Change the ServiceFabric upgrade type of a cluster</span></span>

### [<span data-ttu-id="e281d-134">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="e281d-134">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="e281d-135">Modificare il livello di durabilità di un cluster</span><span class="sxs-lookup"><span data-stu-id="e281d-135">Change the durability tier of a cluster</span></span>

### [<span data-ttu-id="e281d-136">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="e281d-136">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="e281d-137">Modificare il livello di affidabilità di un cluster</span><span class="sxs-lookup"><span data-stu-id="e281d-137">Change the reliability tier of a cluster</span></span>
