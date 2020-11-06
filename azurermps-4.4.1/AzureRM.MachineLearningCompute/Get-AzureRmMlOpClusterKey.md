---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520050"
---
# <span data-ttu-id="d7c48-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="d7c48-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="d7c48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7c48-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c48-103">Ottiene i tasti di scelta associati a un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="d7c48-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7c48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7c48-104">SYNTAX</span></span>

### <span data-ttu-id="d7c48-105">Ottenere le chiavi del cluster di operatività dai parametri di input dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7c48-105">Get operationalization cluster's keys from cmdlet input parameters.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="d7c48-106">Ottenere le chiavi del cluster di operatività da una definizione di istanza di OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="d7c48-106">Get operationalization cluster's keys from an OperationalizationCluster instance definition.</span></span>
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### <span data-ttu-id="d7c48-107">Ottenere le chiavi del cluster di operatività da un ID di risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="d7c48-107">Get operationalization cluster's keys from an Azure resource id.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## <span data-ttu-id="d7c48-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7c48-108">DESCRIPTION</span></span>
<span data-ttu-id="d7c48-109">Quando si ottengono le proprietà del cluster, le chiavi per l'account di archiviazione, il registro dei contenitori e altri servizi associati al cluster di operatività non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="d7c48-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="d7c48-110">Una chiamata specifica per recuperare le chiavi deve essere eseguita perché sono informazioni riservate.</span><span class="sxs-lookup"><span data-stu-id="d7c48-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="d7c48-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7c48-111">EXAMPLES</span></span>

### <span data-ttu-id="d7c48-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d7c48-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="d7c48-113">Restituisce le chiavi segrete per i servizi associati al cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="d7c48-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="d7c48-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7c48-114">PARAMETERS</span></span>

### <span data-ttu-id="d7c48-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7c48-115">-InputObject</span></span>
<span data-ttu-id="d7c48-116">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="d7c48-116">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c48-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7c48-117">-Name</span></span>
<span data-ttu-id="d7c48-118">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="d7c48-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c48-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7c48-119">-ResourceGroupName</span></span>
<span data-ttu-id="d7c48-120">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="d7c48-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7c48-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7c48-121">-ResourceId</span></span>
<span data-ttu-id="d7c48-122">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="d7c48-122">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="d7c48-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7c48-123">INPUTS</span></span>

### <span data-ttu-id="d7c48-124">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="d7c48-124">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="d7c48-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d7c48-125">System.String</span></span>


## <span data-ttu-id="d7c48-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7c48-126">OUTPUTS</span></span>

### <span data-ttu-id="d7c48-127">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="d7c48-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>


## <span data-ttu-id="d7c48-128">Note</span><span class="sxs-lookup"><span data-stu-id="d7c48-128">NOTES</span></span>

## <span data-ttu-id="d7c48-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7c48-129">RELATED LINKS</span></span>

