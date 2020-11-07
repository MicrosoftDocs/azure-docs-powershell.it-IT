---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 9836856ffd663939de8ca0e28635d81785c9c898
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93688670"
---
# <span data-ttu-id="61abf-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="61abf-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="61abf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61abf-102">SYNOPSIS</span></span>
<span data-ttu-id="61abf-103">Rimuove un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61abf-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61abf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61abf-104">SYNTAX</span></span>

### <span data-ttu-id="61abf-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="61abf-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61abf-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="61abf-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61abf-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="61abf-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeAllResources] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61abf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61abf-108">DESCRIPTION</span></span>
<span data-ttu-id="61abf-109">Rimuove un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61abf-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="61abf-110">Alcune risorse associate al cluster potrebbero non essere tutte rimosse.</span><span class="sxs-lookup"><span data-stu-id="61abf-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="61abf-111">Ad esempio, il servizio contenitore di Azure verrà rimosso, ma le VM associate non vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="61abf-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="61abf-112">L'account di archiviazione, il registro dei contenitori e gli approfondimenti delle applicazioni non vengono rimossi per informazioni diagnostiche.</span><span class="sxs-lookup"><span data-stu-id="61abf-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="61abf-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61abf-113">EXAMPLES</span></span>

### <span data-ttu-id="61abf-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61abf-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="61abf-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="61abf-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="61abf-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61abf-116">PARAMETERS</span></span>

### <span data-ttu-id="61abf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61abf-117">-DefaultProfile</span></span>
<span data-ttu-id="61abf-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61abf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61abf-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="61abf-119">-IncludeAllResources</span></span>
<span data-ttu-id="61abf-120">Rimuove tutte le risorse create con il cluster.</span><span class="sxs-lookup"><span data-stu-id="61abf-120">Removes all resources that were created with the cluster.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61abf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61abf-121">-InputObject</span></span>
<span data-ttu-id="61abf-122">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61abf-122">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61abf-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="61abf-123">-Name</span></span>
<span data-ttu-id="61abf-124">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61abf-124">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61abf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61abf-125">-ResourceGroupName</span></span>
<span data-ttu-id="61abf-126">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61abf-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61abf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61abf-127">-ResourceId</span></span>
<span data-ttu-id="61abf-128">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="61abf-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61abf-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61abf-129">-Confirm</span></span>
<span data-ttu-id="61abf-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61abf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61abf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61abf-131">-WhatIf</span></span>
<span data-ttu-id="61abf-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61abf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61abf-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61abf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61abf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61abf-134">CommonParameters</span></span>
<span data-ttu-id="61abf-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61abf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61abf-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61abf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61abf-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61abf-137">INPUTS</span></span>

### <span data-ttu-id="61abf-138">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="61abf-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="61abf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="61abf-139">System.String</span></span>

## <span data-ttu-id="61abf-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61abf-140">OUTPUTS</span></span>

### <span data-ttu-id="61abf-141">System. void</span><span class="sxs-lookup"><span data-stu-id="61abf-141">System.Void</span></span>

## <span data-ttu-id="61abf-142">Note</span><span class="sxs-lookup"><span data-stu-id="61abf-142">NOTES</span></span>

## <span data-ttu-id="61abf-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61abf-143">RELATED LINKS</span></span>

