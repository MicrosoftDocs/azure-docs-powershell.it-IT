---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686569"
---
# <span data-ttu-id="b8818-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="b8818-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="b8818-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8818-102">SYNOPSIS</span></span>
<span data-ttu-id="b8818-103">Rimuove un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="b8818-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8818-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8818-104">SYNTAX</span></span>

### <span data-ttu-id="b8818-105">Rimuovere un cluster di operatività dai parametri di input del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8818-105">Remove an operationalization cluster from cmdlet input parameters.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b8818-106">Rimuovere un cluster di operatività da una definizione di istanza di OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="b8818-106">Remove an operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b8818-107">Rimuovere un cluster di operatività da un ID di Azure resouce.</span><span class="sxs-lookup"><span data-stu-id="b8818-107">Remove an operationalization cluster from an Azure resouce id.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b8818-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8818-108">DESCRIPTION</span></span>
<span data-ttu-id="b8818-109">Rimuove un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="b8818-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="b8818-110">Alcune risorse associate al cluster potrebbero non essere tutte rimosse.</span><span class="sxs-lookup"><span data-stu-id="b8818-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="b8818-111">Ad esempio, il servizio contenitore di Azure verrà rimosso, ma le VM associate non vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="b8818-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="b8818-112">L'account di archiviazione, il registro dei contenitori e gli approfondimenti delle applicazioni non vengono rimossi per informazioni diagnostiche.</span><span class="sxs-lookup"><span data-stu-id="b8818-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="b8818-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8818-113">EXAMPLES</span></span>

### <span data-ttu-id="b8818-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b8818-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="b8818-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b8818-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## <span data-ttu-id="b8818-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8818-116">PARAMETERS</span></span>

### <span data-ttu-id="b8818-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8818-117">-InputObject</span></span>
<span data-ttu-id="b8818-118">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="b8818-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8818-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b8818-119">-Confirm</span></span>
<span data-ttu-id="b8818-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8818-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8818-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8818-121">-Name</span></span>
<span data-ttu-id="b8818-122">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="b8818-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8818-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8818-123">-ResourceGroupName</span></span>
<span data-ttu-id="b8818-124">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="b8818-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8818-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8818-125">-ResourceId</span></span>
<span data-ttu-id="b8818-126">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="b8818-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8818-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8818-127">-WhatIf</span></span>
<span data-ttu-id="b8818-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8818-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8818-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8818-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="b8818-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8818-130">INPUTS</span></span>

### <span data-ttu-id="b8818-131">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="b8818-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="b8818-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b8818-132">System.String</span></span>


## <span data-ttu-id="b8818-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8818-133">OUTPUTS</span></span>

### <span data-ttu-id="b8818-134">System. void</span><span class="sxs-lookup"><span data-stu-id="b8818-134">System.Void</span></span>


## <span data-ttu-id="b8818-135">Note</span><span class="sxs-lookup"><span data-stu-id="b8818-135">NOTES</span></span>

## <span data-ttu-id="b8818-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8818-136">RELATED LINKS</span></span>

