---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ac0606b73145a0d72a5776ede00a24bb802642e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190582"
---
# <span data-ttu-id="5d644-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="5d644-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="5d644-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d644-102">SYNOPSIS</span></span>
<span data-ttu-id="5d644-103">Annullare la sottoscrizione del trigger di evento agli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="5d644-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="5d644-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d644-104">SYNTAX</span></span>

### <span data-ttu-id="5d644-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d644-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d644-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="5d644-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d644-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d644-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d644-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d644-108">DESCRIPTION</span></span>
<span data-ttu-id="5d644-109">Il cmdlet **Remove-AzSynapseTriggerSubscription** annulla la sottoscrizione del trigger di evento agli eventi del servizio esterno specificati dalla ridefinizione del trigger.</span><span class="sxs-lookup"><span data-stu-id="5d644-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="5d644-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d644-110">EXAMPLES</span></span>

### <span data-ttu-id="5d644-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d644-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="5d644-112">Questo comando annulla la sottoscrizione del trigger denominato ContosoTrigger per gli eventi specificati dalla ridefinzione del trigger.</span><span class="sxs-lookup"><span data-stu-id="5d644-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="5d644-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5d644-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="5d644-114">Questo comando annulla la sottoscrizione del trigger denominato ContosoTrigger per gli eventi specificati dalla ridefinizione del trigger tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="5d644-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="5d644-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5d644-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="5d644-116">Questo comando annulla la sottoscrizione del trigger denominato ContosoTrigger per gli eventi specificati dalla ridefinizione del trigger tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="5d644-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="5d644-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d644-117">PARAMETERS</span></span>

### <span data-ttu-id="5d644-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d644-118">-AsJob</span></span>
<span data-ttu-id="5d644-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5d644-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d644-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d644-120">-DefaultProfile</span></span>
<span data-ttu-id="5d644-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d644-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d644-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5d644-122">-Force</span></span>
<span data-ttu-id="5d644-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="5d644-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5d644-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d644-124">-InputObject</span></span>
<span data-ttu-id="5d644-125">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="5d644-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d644-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5d644-126">-Name</span></span>
<span data-ttu-id="5d644-127">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="5d644-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d644-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d644-128">-PassThru</span></span>
<span data-ttu-id="5d644-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5d644-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5d644-130">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5d644-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5d644-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5d644-131">-WorkspaceName</span></span>
<span data-ttu-id="5d644-132">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="5d644-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5d644-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5d644-133">-WorkspaceObject</span></span>
<span data-ttu-id="5d644-134">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="5d644-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5d644-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d644-135">-Confirm</span></span>
<span data-ttu-id="5d644-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d644-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d644-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d644-137">-WhatIf</span></span>
<span data-ttu-id="5d644-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d644-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d644-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d644-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d644-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d644-140">CommonParameters</span></span>
<span data-ttu-id="5d644-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d644-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d644-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d644-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d644-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d644-143">INPUTS</span></span>

### <span data-ttu-id="5d644-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d644-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5d644-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="5d644-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="5d644-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d644-146">OUTPUTS</span></span>

### <span data-ttu-id="5d644-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d644-147">System.Boolean</span></span>

## <span data-ttu-id="5d644-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d644-148">NOTES</span></span>

## <span data-ttu-id="5d644-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d644-149">RELATED LINKS</span></span>
