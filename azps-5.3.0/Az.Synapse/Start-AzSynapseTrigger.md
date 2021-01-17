---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476556"
---
# <span data-ttu-id="2acd3-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="2acd3-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="2acd3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2acd3-102">SYNOPSIS</span></span>
<span data-ttu-id="2acd3-103">Avvia un trigger in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2acd3-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="2acd3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2acd3-104">SYNTAX</span></span>

### <span data-ttu-id="2acd3-105">StartByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2acd3-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2acd3-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="2acd3-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2acd3-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="2acd3-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2acd3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2acd3-108">DESCRIPTION</span></span>
<span data-ttu-id="2acd3-109">Il cmdlet **Start-AzSynapseTrigger** avvia un trigger in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2acd3-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="2acd3-110">Se il trigger si trova nello stato "Stopped", il cmdlet avvia il trigger e infine richiama le pipeline in base alla relativa definizione.</span><span class="sxs-lookup"><span data-stu-id="2acd3-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="2acd3-111">Se il trigger è già nello stato "Started", questo cmdlet non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="2acd3-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="2acd3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2acd3-112">EXAMPLES</span></span>

### <span data-ttu-id="2acd3-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2acd3-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="2acd3-114">Avvia un trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2acd3-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="2acd3-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2acd3-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="2acd3-116">Avvia un trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="2acd3-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="2acd3-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="2acd3-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="2acd3-118">Avvia un trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="2acd3-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2acd3-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2acd3-119">PARAMETERS</span></span>

### <span data-ttu-id="2acd3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2acd3-120">-AsJob</span></span>
<span data-ttu-id="2acd3-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2acd3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2acd3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2acd3-122">-DefaultProfile</span></span>
<span data-ttu-id="2acd3-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2acd3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2acd3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2acd3-124">-InputObject</span></span>
<span data-ttu-id="2acd3-125">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="2acd3-125">The trigger object.</span></span>

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

### <span data-ttu-id="2acd3-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2acd3-126">-Name</span></span>
<span data-ttu-id="2acd3-127">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="2acd3-127">The trigger name.</span></span>

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

### <span data-ttu-id="2acd3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2acd3-128">-PassThru</span></span>
<span data-ttu-id="2acd3-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2acd3-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2acd3-130">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="2acd3-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2acd3-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2acd3-131">-WorkspaceName</span></span>
<span data-ttu-id="2acd3-132">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="2acd3-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2acd3-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2acd3-133">-WorkspaceObject</span></span>
<span data-ttu-id="2acd3-134">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="2acd3-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2acd3-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2acd3-135">-Confirm</span></span>
<span data-ttu-id="2acd3-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2acd3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2acd3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2acd3-137">-WhatIf</span></span>
<span data-ttu-id="2acd3-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2acd3-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2acd3-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2acd3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2acd3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2acd3-140">CommonParameters</span></span>
<span data-ttu-id="2acd3-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2acd3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2acd3-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2acd3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2acd3-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2acd3-143">INPUTS</span></span>

### <span data-ttu-id="2acd3-144">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2acd3-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2acd3-145">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="2acd3-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="2acd3-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2acd3-146">OUTPUTS</span></span>

### <span data-ttu-id="2acd3-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2acd3-147">System.Boolean</span></span>

## <span data-ttu-id="2acd3-148">Note</span><span class="sxs-lookup"><span data-stu-id="2acd3-148">NOTES</span></span>

## <span data-ttu-id="2acd3-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2acd3-149">RELATED LINKS</span></span>
