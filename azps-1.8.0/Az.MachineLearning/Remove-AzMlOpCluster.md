---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
ms.openlocfilehash: de297c94be69773d07efedfae42ccc029fc13414
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835276"
---
# <span data-ttu-id="dd4b3-101">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dd4b3-101">Remove-AzMlOpCluster</span></span>

## <span data-ttu-id="dd4b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd4b3-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4b3-103">Rimuove un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-103">Removes an operationalization cluster.</span></span>

## <span data-ttu-id="dd4b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd4b3-104">SYNTAX</span></span>

### <span data-ttu-id="dd4b3-105">RemoveByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd4b3-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd4b3-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="dd4b3-106">RemoveByInputObject</span></span>
```
Remove-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd4b3-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd4b3-107">RemoveByResourceId</span></span>
```
Remove-AzMlOpCluster -ResourceId <String> [-IncludeAllResources] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd4b3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd4b3-108">DESCRIPTION</span></span>
<span data-ttu-id="dd4b3-109">Rimuove un cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="dd4b3-110">Alcune risorse associate al cluster potrebbero non essere tutte rimosse.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="dd4b3-111">Ad esempio, il servizio contenitore di Azure verrà rimosso, ma le VM associate non vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="dd4b3-112">L'account di archiviazione, il registro dei contenitori e gli approfondimenti delle applicazioni non vengono rimossi per informazioni diagnostiche.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="dd4b3-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd4b3-113">EXAMPLES</span></span>

### <span data-ttu-id="dd4b3-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dd4b3-114">Example 1</span></span>
```
PS C:\> Remove-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="dd4b3-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dd4b3-115">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzMlOpCluster
```

## <span data-ttu-id="dd4b3-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd4b3-116">PARAMETERS</span></span>

### <span data-ttu-id="dd4b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4b3-117">-DefaultProfile</span></span>
<span data-ttu-id="dd4b3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4b3-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="dd4b3-119">-IncludeAllResources</span></span>
<span data-ttu-id="dd4b3-120">Rimuove tutte le risorse create con il cluster.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-120">Removes all resources that were created with the cluster.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4b3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd4b3-121">-InputObject</span></span>
<span data-ttu-id="dd4b3-122">Oggetto cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-122">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4b3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd4b3-123">-Name</span></span>
<span data-ttu-id="dd4b3-124">Nome del cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-124">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4b3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd4b3-125">-ResourceGroupName</span></span>
<span data-ttu-id="dd4b3-126">Nome del gruppo di risorse per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4b3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd4b3-127">-ResourceId</span></span>
<span data-ttu-id="dd4b3-128">ID risorsa Azure per il cluster di operatività.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4b3-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd4b3-129">-Confirm</span></span>
<span data-ttu-id="dd4b3-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4b3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd4b3-131">-WhatIf</span></span>
<span data-ttu-id="dd4b3-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd4b3-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4b3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4b3-134">CommonParameters</span></span>
<span data-ttu-id="dd4b3-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd4b3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4b3-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd4b3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4b3-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd4b3-137">INPUTS</span></span>

### <span data-ttu-id="dd4b3-138">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="dd4b3-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="dd4b3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dd4b3-139">System.String</span></span>

## <span data-ttu-id="dd4b3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd4b3-140">OUTPUTS</span></span>

### <span data-ttu-id="dd4b3-141">System. void</span><span class="sxs-lookup"><span data-stu-id="dd4b3-141">System.Void</span></span>

## <span data-ttu-id="dd4b3-142">Note</span><span class="sxs-lookup"><span data-stu-id="dd4b3-142">NOTES</span></span>

## <span data-ttu-id="dd4b3-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd4b3-143">RELATED LINKS</span></span>
