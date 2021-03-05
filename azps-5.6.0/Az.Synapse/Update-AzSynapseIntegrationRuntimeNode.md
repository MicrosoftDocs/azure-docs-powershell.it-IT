---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5c2d7c8aa81cb45b6b49898c95b27256aa504b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963437"
---
# <span data-ttu-id="383b2-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="383b2-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="383b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="383b2-102">SYNOPSIS</span></span>
<span data-ttu-id="383b2-103">Aggiorna il nodo di runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="383b2-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="383b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="383b2-104">SYNTAX</span></span>

### <span data-ttu-id="383b2-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="383b2-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="383b2-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="383b2-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="383b2-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="383b2-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="383b2-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="383b2-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="383b2-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="383b2-109">DESCRIPTION</span></span>
<span data-ttu-id="383b2-110">Il cmdlet **Update-AzSynapseIntegrationRuntimeNode** aggiorna le proprietà del nodo di runtime di integrazione self-hosted in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="383b2-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="383b2-111">Attualmente supporta solo l'aggiornamento di 'ConcurrentJobsLimit'.</span><span class="sxs-lookup"><span data-stu-id="383b2-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="383b2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="383b2-112">EXAMPLES</span></span>

### <span data-ttu-id="383b2-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="383b2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="383b2-114">Il cmdlet aggiorna 'ConcurrentJobsLimit' a 3 per il nodo "Node_1" nel runtime di integrazione self-hosted 'test-selfhost-ir'.</span><span class="sxs-lookup"><span data-stu-id="383b2-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="383b2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="383b2-115">PARAMETERS</span></span>

### <span data-ttu-id="383b2-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="383b2-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="383b2-117">Numero di processi simultanei consentiti nel nodo di runtime dell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="383b2-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="383b2-118">Sono consentiti valori compresi tra 1 e maxConcurrentJobs.</span><span class="sxs-lookup"><span data-stu-id="383b2-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383b2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="383b2-119">-DefaultProfile</span></span>
<span data-ttu-id="383b2-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="383b2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="383b2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="383b2-121">-InputObject</span></span>
<span data-ttu-id="383b2-122">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="383b2-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="383b2-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="383b2-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="383b2-124">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="383b2-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383b2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="383b2-125">-Name</span></span>
<span data-ttu-id="383b2-126">Nome del nodo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="383b2-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383b2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="383b2-127">-ResourceGroupName</span></span>
<span data-ttu-id="383b2-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="383b2-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383b2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="383b2-129">-ResourceId</span></span>
<span data-ttu-id="383b2-130">Identificatore di risorsa del runtime di integrazione di Synapse.</span><span class="sxs-lookup"><span data-stu-id="383b2-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383b2-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="383b2-131">-WorkspaceName</span></span>
<span data-ttu-id="383b2-132">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="383b2-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383b2-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="383b2-133">-WorkspaceObject</span></span>
<span data-ttu-id="383b2-134">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="383b2-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="383b2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="383b2-135">-Confirm</span></span>
<span data-ttu-id="383b2-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="383b2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="383b2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="383b2-137">-WhatIf</span></span>
<span data-ttu-id="383b2-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="383b2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="383b2-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="383b2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="383b2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="383b2-140">CommonParameters</span></span>
<span data-ttu-id="383b2-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="383b2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="383b2-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="383b2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="383b2-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="383b2-143">INPUTS</span></span>

### <span data-ttu-id="383b2-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="383b2-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="383b2-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="383b2-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="383b2-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="383b2-146">OUTPUTS</span></span>

### <span data-ttu-id="383b2-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="383b2-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="383b2-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="383b2-148">NOTES</span></span>

## <span data-ttu-id="383b2-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="383b2-149">RELATED LINKS</span></span>
