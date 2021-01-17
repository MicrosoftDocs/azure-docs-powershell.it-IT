---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ac0606b73145a0d72a5776ede00a24bb802642e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346075"
---
# <span data-ttu-id="7c2b5-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="7c2b5-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="7c2b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c2b5-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2b5-103">Annullare la sottoscrizione del trigger dell'evento agli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="7c2b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c2b5-104">SYNTAX</span></span>

### <span data-ttu-id="7c2b5-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c2b5-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c2b5-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7c2b5-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c2b5-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7c2b5-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c2b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c2b5-108">DESCRIPTION</span></span>
<span data-ttu-id="7c2b5-109">Il cmdlet **Remove-AzSynapseTriggerSubscription** Annulla la sottoscrizione del trigger di evento agli eventi del servizio esterno specificati dal trigger definizione.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="7c2b5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c2b5-110">EXAMPLES</span></span>

### <span data-ttu-id="7c2b5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c2b5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="7c2b5-112">Questo comando consente di annullare la sottoscrizione del trigger denominato ContosoTrigger agli eventi specificati dal trigger definizione.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="7c2b5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7c2b5-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="7c2b5-114">Questo comando Annulla la sottoscrizione del trigger denominato ContosoTrigger agli eventi specificati dal trigger definizione tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="7c2b5-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7c2b5-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="7c2b5-116">Questo comando Annulla la sottoscrizione del trigger denominato ContosoTrigger agli eventi specificati dal trigger definizione tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="7c2b5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c2b5-117">PARAMETERS</span></span>

### <span data-ttu-id="7c2b5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c2b5-118">-AsJob</span></span>
<span data-ttu-id="7c2b5-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7c2b5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c2b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2b5-120">-DefaultProfile</span></span>
<span data-ttu-id="7c2b5-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c2b5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7c2b5-122">-Force</span></span>
<span data-ttu-id="7c2b5-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7c2b5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c2b5-124">-InputObject</span></span>
<span data-ttu-id="7c2b5-125">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-125">The trigger object.</span></span>

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

### <span data-ttu-id="7c2b5-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c2b5-126">-Name</span></span>
<span data-ttu-id="7c2b5-127">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-127">The trigger name.</span></span>

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

### <span data-ttu-id="7c2b5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c2b5-128">-PassThru</span></span>
<span data-ttu-id="7c2b5-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7c2b5-130">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7c2b5-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7c2b5-131">-WorkspaceName</span></span>
<span data-ttu-id="7c2b5-132">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7c2b5-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7c2b5-133">-WorkspaceObject</span></span>
<span data-ttu-id="7c2b5-134">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7c2b5-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c2b5-135">-Confirm</span></span>
<span data-ttu-id="7c2b5-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c2b5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c2b5-137">-WhatIf</span></span>
<span data-ttu-id="7c2b5-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c2b5-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c2b5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2b5-140">CommonParameters</span></span>
<span data-ttu-id="7c2b5-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c2b5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2b5-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c2b5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2b5-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c2b5-143">INPUTS</span></span>

### <span data-ttu-id="7c2b5-144">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7c2b5-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7c2b5-145">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="7c2b5-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="7c2b5-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c2b5-146">OUTPUTS</span></span>

### <span data-ttu-id="7c2b5-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c2b5-147">System.Boolean</span></span>

## <span data-ttu-id="7c2b5-148">Note</span><span class="sxs-lookup"><span data-stu-id="7c2b5-148">NOTES</span></span>

## <span data-ttu-id="7c2b5-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c2b5-149">RELATED LINKS</span></span>
