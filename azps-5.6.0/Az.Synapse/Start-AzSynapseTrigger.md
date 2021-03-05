---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: 39801db0d1cd400fa88868b87098260c9148daa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992009"
---
# <span data-ttu-id="da431-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="da431-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="da431-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da431-102">SYNOPSIS</span></span>
<span data-ttu-id="da431-103">Avvia un trigger in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="da431-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="da431-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da431-104">SYNTAX</span></span>

### <span data-ttu-id="da431-105">StartByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da431-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da431-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="da431-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da431-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="da431-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da431-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da431-108">DESCRIPTION</span></span>
<span data-ttu-id="da431-109">Il cmdlet **Start-AzSynapseTrigger** avvia un trigger in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="da431-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="da431-110">Se il trigger è in stato "Arrestato", il cmdlet avvia il trigger e alla fine richiama pipeline in base alla relativa definizione.</span><span class="sxs-lookup"><span data-stu-id="da431-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="da431-111">Se il trigger è già in stato "Avviato", questo cmdlet non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="da431-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="da431-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da431-112">EXAMPLES</span></span>

### <span data-ttu-id="da431-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="da431-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="da431-114">Avvia un trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="da431-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="da431-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="da431-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="da431-116">Avvia un trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="da431-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="da431-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="da431-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="da431-118">Avvia un trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="da431-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="da431-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da431-119">PARAMETERS</span></span>

### <span data-ttu-id="da431-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da431-120">-AsJob</span></span>
<span data-ttu-id="da431-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="da431-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da431-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da431-122">-DefaultProfile</span></span>
<span data-ttu-id="da431-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da431-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da431-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da431-124">-InputObject</span></span>
<span data-ttu-id="da431-125">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="da431-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StartByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da431-126">-Name</span><span class="sxs-lookup"><span data-stu-id="da431-126">-Name</span></span>
<span data-ttu-id="da431-127">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="da431-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName, StartByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da431-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da431-128">-PassThru</span></span>
<span data-ttu-id="da431-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="da431-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="da431-130">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="da431-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="da431-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="da431-131">-WorkspaceName</span></span>
<span data-ttu-id="da431-132">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="da431-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da431-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="da431-133">-WorkspaceObject</span></span>
<span data-ttu-id="da431-134">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="da431-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StartByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da431-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da431-135">-Confirm</span></span>
<span data-ttu-id="da431-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da431-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da431-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da431-137">-WhatIf</span></span>
<span data-ttu-id="da431-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da431-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da431-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da431-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da431-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da431-140">CommonParameters</span></span>
<span data-ttu-id="da431-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da431-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da431-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da431-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da431-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="da431-143">INPUTS</span></span>

### <span data-ttu-id="da431-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="da431-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="da431-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="da431-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="da431-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da431-146">OUTPUTS</span></span>

### <span data-ttu-id="da431-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da431-147">System.Boolean</span></span>

## <span data-ttu-id="da431-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="da431-148">NOTES</span></span>

## <span data-ttu-id="da431-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da431-149">RELATED LINKS</span></span>
