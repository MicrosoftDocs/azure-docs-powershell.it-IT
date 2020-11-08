---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: 69e7c17d28c94ce00f054a0e5b71eadc4d8ade76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190447"
---
# <span data-ttu-id="c0424-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="c0424-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="c0424-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0424-102">SYNOPSIS</span></span>
<span data-ttu-id="c0424-103">Annullare la sottoscrizione del trigger dell'evento agli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="c0424-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="c0424-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0424-104">SYNTAX</span></span>

### <span data-ttu-id="c0424-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0424-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0424-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="c0424-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0424-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0424-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0424-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0424-108">DESCRIPTION</span></span>
<span data-ttu-id="c0424-109">Il cmdlet **Remove-AzSynapseTriggerSubscription** Annulla la sottoscrizione del trigger di evento agli eventi del servizio esterno specificati dal trigger definizione.</span><span class="sxs-lookup"><span data-stu-id="c0424-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="c0424-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0424-110">EXAMPLES</span></span>

### <span data-ttu-id="c0424-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c0424-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="c0424-112">Questo comando consente di annullare la sottoscrizione del trigger denominato ContosoTrigger agli eventi specificati dal trigger definizione.</span><span class="sxs-lookup"><span data-stu-id="c0424-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="c0424-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c0424-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="c0424-114">Questo comando Annulla la sottoscrizione del trigger denominato ContosoTrigger agli eventi specificati dal trigger definizione tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0424-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="c0424-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c0424-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="c0424-116">Questo comando Annulla la sottoscrizione del trigger denominato ContosoTrigger agli eventi specificati dal trigger definizione tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0424-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="c0424-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0424-117">PARAMETERS</span></span>

### <span data-ttu-id="c0424-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0424-118">-AsJob</span></span>
<span data-ttu-id="c0424-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c0424-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0424-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0424-120">-DefaultProfile</span></span>
<span data-ttu-id="c0424-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0424-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0424-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0424-122">-InputObject</span></span>
<span data-ttu-id="c0424-123">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="c0424-123">The trigger object.</span></span>

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

### <span data-ttu-id="c0424-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0424-124">-Name</span></span>
<span data-ttu-id="c0424-125">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="c0424-125">The trigger name.</span></span>

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

### <span data-ttu-id="c0424-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0424-126">-PassThru</span></span>
<span data-ttu-id="c0424-127">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c0424-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c0424-128">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="c0424-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c0424-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0424-129">-WorkspaceName</span></span>
<span data-ttu-id="c0424-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="c0424-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c0424-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c0424-131">-WorkspaceObject</span></span>
<span data-ttu-id="c0424-132">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0424-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c0424-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c0424-133">-Confirm</span></span>
<span data-ttu-id="c0424-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0424-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0424-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0424-135">-WhatIf</span></span>
<span data-ttu-id="c0424-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0424-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0424-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0424-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0424-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0424-138">CommonParameters</span></span>
<span data-ttu-id="c0424-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0424-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0424-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0424-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0424-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0424-141">INPUTS</span></span>

### <span data-ttu-id="c0424-142">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0424-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c0424-143">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="c0424-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="c0424-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0424-144">OUTPUTS</span></span>

### <span data-ttu-id="c0424-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0424-145">System.Boolean</span></span>

## <span data-ttu-id="c0424-146">Note</span><span class="sxs-lookup"><span data-stu-id="c0424-146">NOTES</span></span>

## <span data-ttu-id="c0424-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0424-147">RELATED LINKS</span></span>
