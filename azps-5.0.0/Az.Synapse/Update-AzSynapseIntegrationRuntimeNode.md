---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193105"
---
# <span data-ttu-id="b9e8d-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b9e8d-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="b9e8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e8d-103">Aggiorna il nodo runtime di Integration self-hosted.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="b9e8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9e8d-104">SYNTAX</span></span>

### <span data-ttu-id="b9e8d-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9e8d-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e8d-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9e8d-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9e8d-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9e8d-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9e8d-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9e8d-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9e8d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9e8d-109">DESCRIPTION</span></span>
<span data-ttu-id="b9e8d-110">Il cmdlet **Update-AzSynapseIntegrationRuntimeNode** aggiorna le proprietà del nodo runtime di integrazione ospitata in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="b9e8d-111">Attualmente supporta solo l'aggiornamento di "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="b9e8d-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="b9e8d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9e8d-112">EXAMPLES</span></span>

### <span data-ttu-id="b9e8d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b9e8d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="b9e8d-114">Il cmdlet aggiorna "ConcurrentJobsLimit" in 3 per il nodo "Node_1" in self-hosted Integration Runtime "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="b9e8d-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="b9e8d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9e8d-115">PARAMETERS</span></span>

### <span data-ttu-id="b9e8d-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="b9e8d-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="b9e8d-117">Numero di processi simultanei consentiti per l'esecuzione nel nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="b9e8d-118">I valori compresi tra 1 e maxConcurrentJobs sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="b9e8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e8d-119">-DefaultProfile</span></span>
<span data-ttu-id="b9e8d-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9e8d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9e8d-121">-InputObject</span></span>
<span data-ttu-id="b9e8d-122">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="b9e8d-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b9e8d-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b9e8d-124">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="b9e8d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9e8d-125">-Name</span></span>
<span data-ttu-id="b9e8d-126">Nome del nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="b9e8d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e8d-127">-ResourceGroupName</span></span>
<span data-ttu-id="b9e8d-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-128">Resource group name.</span></span>

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

### <span data-ttu-id="b9e8d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9e8d-129">-ResourceId</span></span>
<span data-ttu-id="b9e8d-130">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="b9e8d-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9e8d-131">-WorkspaceName</span></span>
<span data-ttu-id="b9e8d-132">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b9e8d-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b9e8d-133">-WorkspaceObject</span></span>
<span data-ttu-id="b9e8d-134">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b9e8d-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9e8d-135">-Confirm</span></span>
<span data-ttu-id="b9e8d-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e8d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e8d-137">-WhatIf</span></span>
<span data-ttu-id="b9e8d-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e8d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e8d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e8d-140">CommonParameters</span></span>
<span data-ttu-id="b9e8d-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e8d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e8d-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9e8d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e8d-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9e8d-143">INPUTS</span></span>

### <span data-ttu-id="b9e8d-144">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b9e8d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b9e8d-145">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b9e8d-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b9e8d-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9e8d-146">OUTPUTS</span></span>

### <span data-ttu-id="b9e8d-147">Microsoft. Azure. Commands. sinapsi. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="b9e8d-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="b9e8d-148">Note</span><span class="sxs-lookup"><span data-stu-id="b9e8d-148">NOTES</span></span>

## <span data-ttu-id="b9e8d-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9e8d-149">RELATED LINKS</span></span>