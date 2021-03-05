---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: 6f16664eac63ab2bb543b2d032679d979f3c2122
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010061"
---
# <span data-ttu-id="0d88f-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="0d88f-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="0d88f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d88f-102">SYNOPSIS</span></span>
<span data-ttu-id="0d88f-103">Aggiornare il pool di nodi in un cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="0d88f-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="0d88f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d88f-104">SYNTAX</span></span>

### <span data-ttu-id="0d88f-105">defaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="0d88f-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d88f-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d88f-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d88f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d88f-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d88f-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d88f-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d88f-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0d88f-109">DESCRIPTION</span></span>
<span data-ttu-id="0d88f-110">Aggiornare il pool di nodi in un cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="0d88f-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="0d88f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d88f-111">EXAMPLES</span></span>

### <span data-ttu-id="0d88f-112">Impostare il numero di minimuni su 5 per il pool di nodi specificato</span><span class="sxs-lookup"><span data-stu-id="0d88f-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="0d88f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d88f-113">PARAMETERS</span></span>

### <span data-ttu-id="0d88f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d88f-114">-AsJob</span></span>
<span data-ttu-id="0d88f-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0d88f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d88f-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0d88f-116">-ClusterName</span></span>
<span data-ttu-id="0d88f-117">Nome della risorsa cluster gestita.</span><span class="sxs-lookup"><span data-stu-id="0d88f-117">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d88f-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="0d88f-118">-ClusterObject</span></span>
<span data-ttu-id="0d88f-119">Oggetto cluster</span><span class="sxs-lookup"><span data-stu-id="0d88f-119">The cluster object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d88f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d88f-120">-DefaultProfile</span></span>
<span data-ttu-id="0d88f-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d88f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d88f-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="0d88f-122">-EnableAutoScaling</span></span>
<span data-ttu-id="0d88f-123">Se abilitare o meno la scalabilità automatica</span><span class="sxs-lookup"><span data-stu-id="0d88f-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="0d88f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0d88f-124">-Force</span></span>
<span data-ttu-id="0d88f-125">Aggiornare il pool di nodi senza richiesta</span><span class="sxs-lookup"><span data-stu-id="0d88f-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="0d88f-126">-Id</span><span class="sxs-lookup"><span data-stu-id="0d88f-126">-Id</span></span>
<span data-ttu-id="0d88f-127">ID di un pool di nodi nel cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="0d88f-127">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d88f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d88f-128">-InputObject</span></span>
<span data-ttu-id="0d88f-129">Oggetto PSAgentPool, che in genere passa attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d88f-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d88f-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="0d88f-130">-KubernetesVersion</span></span>
<span data-ttu-id="0d88f-131">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="0d88f-131">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d88f-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0d88f-132">-MaxCount</span></span>
<span data-ttu-id="0d88f-133">Numero massimo di nodi per il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="0d88f-133">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d88f-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="0d88f-134">-MinCount</span></span>
<span data-ttu-id="0d88f-135">Numero minimo di nodi per il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="0d88f-135">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d88f-136">-Name</span><span class="sxs-lookup"><span data-stu-id="0d88f-136">-Name</span></span>
<span data-ttu-id="0d88f-137">Nome del pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="0d88f-137">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d88f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d88f-138">-ResourceGroupName</span></span>
<span data-ttu-id="0d88f-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d88f-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d88f-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d88f-140">-Confirm</span></span>
<span data-ttu-id="0d88f-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d88f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d88f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d88f-142">-WhatIf</span></span>
<span data-ttu-id="0d88f-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d88f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d88f-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d88f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d88f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d88f-145">CommonParameters</span></span>
<span data-ttu-id="0d88f-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d88f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d88f-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0d88f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d88f-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="0d88f-148">INPUTS</span></span>

### <span data-ttu-id="0d88f-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="0d88f-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="0d88f-150">System.String</span><span class="sxs-lookup"><span data-stu-id="0d88f-150">System.String</span></span>

## <span data-ttu-id="0d88f-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d88f-151">OUTPUTS</span></span>

### <span data-ttu-id="0d88f-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="0d88f-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="0d88f-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="0d88f-153">NOTES</span></span>

## <span data-ttu-id="0d88f-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d88f-154">RELATED LINKS</span></span>
