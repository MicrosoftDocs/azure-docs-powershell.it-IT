---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192638"
---
# <span data-ttu-id="39543-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="39543-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="39543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39543-102">SYNOPSIS</span></span>
<span data-ttu-id="39543-103">Aggiornare il pool di nodi in un cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="39543-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="39543-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39543-104">SYNTAX</span></span>

### <span data-ttu-id="39543-105">defaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="39543-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39543-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39543-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39543-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39543-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39543-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39543-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39543-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39543-109">DESCRIPTION</span></span>
<span data-ttu-id="39543-110">Aggiornare il pool di nodi in un cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="39543-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="39543-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39543-111">EXAMPLES</span></span>

### <span data-ttu-id="39543-112">Impostare il numero di minimuni su 5 per il pool di nodi specificato</span><span class="sxs-lookup"><span data-stu-id="39543-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="39543-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39543-113">PARAMETERS</span></span>

### <span data-ttu-id="39543-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39543-114">-AsJob</span></span>
<span data-ttu-id="39543-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="39543-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39543-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="39543-116">-ClusterName</span></span>
<span data-ttu-id="39543-117">Nome della risorsa cluster gestita.</span><span class="sxs-lookup"><span data-stu-id="39543-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="39543-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="39543-118">-ClusterObject</span></span>
<span data-ttu-id="39543-119">Oggetto cluster</span><span class="sxs-lookup"><span data-stu-id="39543-119">The cluster object</span></span>

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

### <span data-ttu-id="39543-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39543-120">-DefaultProfile</span></span>
<span data-ttu-id="39543-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39543-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39543-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="39543-122">-EnableAutoScaling</span></span>
<span data-ttu-id="39543-123">Se abilitare o meno la scalabilità automatica</span><span class="sxs-lookup"><span data-stu-id="39543-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="39543-124">-Force</span><span class="sxs-lookup"><span data-stu-id="39543-124">-Force</span></span>
<span data-ttu-id="39543-125">Aggiornare il pool di nodi senza richiesta</span><span class="sxs-lookup"><span data-stu-id="39543-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="39543-126">-Id</span><span class="sxs-lookup"><span data-stu-id="39543-126">-Id</span></span>
<span data-ttu-id="39543-127">ID di un pool di nodi nel cluster Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="39543-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="39543-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39543-128">-InputObject</span></span>
<span data-ttu-id="39543-129">Oggetto PSAgentPool, che in genere passa attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="39543-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="39543-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="39543-130">-KubernetesVersion</span></span>
<span data-ttu-id="39543-131">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="39543-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="39543-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="39543-132">-MaxCount</span></span>
<span data-ttu-id="39543-133">Numero massimo di nodi per il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="39543-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="39543-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="39543-134">-MinCount</span></span>
<span data-ttu-id="39543-135">Numero minimo di nodi per il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="39543-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="39543-136">-Name</span><span class="sxs-lookup"><span data-stu-id="39543-136">-Name</span></span>
<span data-ttu-id="39543-137">Nome del pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="39543-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="39543-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39543-138">-ResourceGroupName</span></span>
<span data-ttu-id="39543-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39543-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="39543-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39543-140">-Confirm</span></span>
<span data-ttu-id="39543-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39543-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39543-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39543-142">-WhatIf</span></span>
<span data-ttu-id="39543-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39543-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39543-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39543-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39543-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39543-145">CommonParameters</span></span>
<span data-ttu-id="39543-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39543-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39543-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39543-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39543-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="39543-148">INPUTS</span></span>

### <span data-ttu-id="39543-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="39543-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="39543-150">System.String</span><span class="sxs-lookup"><span data-stu-id="39543-150">System.String</span></span>

## <span data-ttu-id="39543-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39543-151">OUTPUTS</span></span>

### <span data-ttu-id="39543-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="39543-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="39543-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="39543-153">NOTES</span></span>

## <span data-ttu-id="39543-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39543-154">RELATED LINKS</span></span>
