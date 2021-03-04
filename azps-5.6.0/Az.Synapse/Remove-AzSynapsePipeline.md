---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: b7bd7866ec6c6ff41a6ef7474b71cfc880e28f49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981805"
---
# <span data-ttu-id="16ff7-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="16ff7-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="16ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="16ff7-103">Rimuove una pipeline dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="16ff7-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="16ff7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16ff7-104">SYNTAX</span></span>

### <span data-ttu-id="16ff7-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16ff7-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ff7-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="16ff7-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ff7-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="16ff7-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16ff7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="16ff7-108">DESCRIPTION</span></span>
<span data-ttu-id="16ff7-109">Il cmdlet **Remove-AzSynapsePipeline** rimuove una pipeline dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="16ff7-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="16ff7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16ff7-110">EXAMPLES</span></span>

### <span data-ttu-id="16ff7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16ff7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="16ff7-112">Questo cmdlet rimuove la pipeline denominata ContosoPipeline dall'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="16ff7-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="16ff7-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="16ff7-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="16ff7-114">Questo cmdlet rimuove la pipeline denominata ContosoPipeline dall'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="16ff7-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="16ff7-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="16ff7-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="16ff7-116">Questo cmdlet rimuove la pipeline denominata ContosoPipeline dall'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="16ff7-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="16ff7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16ff7-117">PARAMETERS</span></span>

### <span data-ttu-id="16ff7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16ff7-118">-AsJob</span></span>
<span data-ttu-id="16ff7-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="16ff7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16ff7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ff7-120">-DefaultProfile</span></span>
<span data-ttu-id="16ff7-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16ff7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16ff7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="16ff7-122">-Force</span></span>
<span data-ttu-id="16ff7-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="16ff7-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="16ff7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16ff7-124">-InputObject</span></span>
<span data-ttu-id="16ff7-125">Oggetto pipeline.</span><span class="sxs-lookup"><span data-stu-id="16ff7-125">The pipeline object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16ff7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="16ff7-126">-Name</span></span>
<span data-ttu-id="16ff7-127">Nome della pipeline.</span><span class="sxs-lookup"><span data-stu-id="16ff7-127">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ff7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16ff7-128">-PassThru</span></span>
<span data-ttu-id="16ff7-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="16ff7-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="16ff7-130">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="16ff7-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="16ff7-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="16ff7-131">-WorkspaceName</span></span>
<span data-ttu-id="16ff7-132">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="16ff7-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ff7-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="16ff7-133">-WorkspaceObject</span></span>
<span data-ttu-id="16ff7-134">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="16ff7-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16ff7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16ff7-135">-Confirm</span></span>
<span data-ttu-id="16ff7-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16ff7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ff7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ff7-137">-WhatIf</span></span>
<span data-ttu-id="16ff7-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16ff7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16ff7-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16ff7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ff7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ff7-140">CommonParameters</span></span>
<span data-ttu-id="16ff7-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ff7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ff7-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16ff7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ff7-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="16ff7-143">INPUTS</span></span>

### <span data-ttu-id="16ff7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="16ff7-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="16ff7-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="16ff7-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="16ff7-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16ff7-146">OUTPUTS</span></span>

### <span data-ttu-id="16ff7-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16ff7-147">System.Boolean</span></span>

## <span data-ttu-id="16ff7-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="16ff7-148">NOTES</span></span>

## <span data-ttu-id="16ff7-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16ff7-149">RELATED LINKS</span></span>
