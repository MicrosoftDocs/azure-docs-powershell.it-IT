---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327412"
---
# <span data-ttu-id="0d263-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="0d263-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="0d263-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d263-102">SYNOPSIS</span></span>
<span data-ttu-id="0d263-103">Arresta un trigger in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0d263-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="0d263-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d263-104">SYNTAX</span></span>

### <span data-ttu-id="0d263-105">StopByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0d263-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d263-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="0d263-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d263-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="0d263-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d263-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d263-108">DESCRIPTION</span></span>
<span data-ttu-id="0d263-109">Il cmdlet **Stop-AzSynapseTrigger** arresta un trigger in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0d263-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="0d263-110">Se il trigger si trova nello stato "iniziato", il cmdlet interrompe il trigger e non richiama più le pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d263-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="0d263-111">Se il trigger è già nello stato "Stopped", questo cmdlet non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="0d263-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="0d263-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d263-112">EXAMPLES</span></span>

### <span data-ttu-id="0d263-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d263-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="0d263-114">Interrompe un trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0d263-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="0d263-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0d263-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="0d263-116">Interrompe un trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d263-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="0d263-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0d263-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="0d263-118">Interrompere un trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d263-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="0d263-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d263-119">PARAMETERS</span></span>

### <span data-ttu-id="0d263-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d263-120">-AsJob</span></span>
<span data-ttu-id="0d263-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0d263-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d263-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d263-122">-DefaultProfile</span></span>
<span data-ttu-id="0d263-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d263-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d263-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d263-124">-InputObject</span></span>
<span data-ttu-id="0d263-125">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="0d263-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d263-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d263-126">-Name</span></span>
<span data-ttu-id="0d263-127">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="0d263-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName, StopByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d263-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d263-128">-PassThru</span></span>
<span data-ttu-id="0d263-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0d263-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0d263-130">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="0d263-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0d263-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0d263-131">-WorkspaceName</span></span>
<span data-ttu-id="0d263-132">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="0d263-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d263-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0d263-133">-WorkspaceObject</span></span>
<span data-ttu-id="0d263-134">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d263-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d263-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d263-135">-Confirm</span></span>
<span data-ttu-id="0d263-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d263-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d263-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d263-137">-WhatIf</span></span>
<span data-ttu-id="0d263-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d263-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d263-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d263-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d263-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d263-140">CommonParameters</span></span>
<span data-ttu-id="0d263-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d263-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d263-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d263-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d263-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d263-143">INPUTS</span></span>

### <span data-ttu-id="0d263-144">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0d263-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0d263-145">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="0d263-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="0d263-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d263-146">OUTPUTS</span></span>

### <span data-ttu-id="0d263-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d263-147">System.Boolean</span></span>

## <span data-ttu-id="0d263-148">Note</span><span class="sxs-lookup"><span data-stu-id="0d263-148">NOTES</span></span>

## <span data-ttu-id="0d263-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d263-149">RELATED LINKS</span></span>
