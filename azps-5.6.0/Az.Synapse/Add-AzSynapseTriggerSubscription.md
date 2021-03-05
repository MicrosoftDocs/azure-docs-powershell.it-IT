---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: d9ff2e46b7b4ccf7b3d2fafd1aa8142efd0675b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981374"
---
# <span data-ttu-id="625f9-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="625f9-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="625f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="625f9-102">SYNOPSIS</span></span>
<span data-ttu-id="625f9-103">Sottoscrivere il trigger di evento per eventi di servizi esterni.</span><span class="sxs-lookup"><span data-stu-id="625f9-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="625f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="625f9-104">SYNTAX</span></span>

### <span data-ttu-id="625f9-105">AddByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="625f9-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="625f9-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="625f9-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="625f9-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="625f9-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="625f9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="625f9-108">DESCRIPTION</span></span>
<span data-ttu-id="625f9-109">Il cmdlet **Add-AzSynapseTriggerSubscription** sottoscrive il trigger di evento per gli eventi del servizio esterno specificati dall'affinamento del trigger.</span><span class="sxs-lookup"><span data-stu-id="625f9-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="625f9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="625f9-110">EXAMPLES</span></span>

### <span data-ttu-id="625f9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="625f9-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="625f9-112">Questo comando sottoscrive un trigger denominato ContosoTrigger per gli eventi specificati dall'affinamento del trigger.</span><span class="sxs-lookup"><span data-stu-id="625f9-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="625f9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="625f9-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="625f9-114">Questo comando sottoscrive un trigger denominato ContosoTrigger per gli eventi specificati dall'affinamento trigger alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="625f9-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="625f9-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="625f9-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="625f9-116">Questo comando sottoscrive un trigger denominato ContosoTrigger per gli eventi specificati dall'affinamento trigger alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="625f9-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="625f9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="625f9-117">PARAMETERS</span></span>

### <span data-ttu-id="625f9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="625f9-118">-AsJob</span></span>
<span data-ttu-id="625f9-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="625f9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="625f9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="625f9-120">-DefaultProfile</span></span>
<span data-ttu-id="625f9-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="625f9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="625f9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="625f9-122">-InputObject</span></span>
<span data-ttu-id="625f9-123">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="625f9-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: AddByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="625f9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="625f9-124">-Name</span></span>
<span data-ttu-id="625f9-125">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="625f9-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName, AddByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625f9-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="625f9-126">-WorkspaceName</span></span>
<span data-ttu-id="625f9-127">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="625f9-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625f9-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="625f9-128">-WorkspaceObject</span></span>
<span data-ttu-id="625f9-129">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="625f9-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: AddByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="625f9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="625f9-130">-Confirm</span></span>
<span data-ttu-id="625f9-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="625f9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="625f9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="625f9-132">-WhatIf</span></span>
<span data-ttu-id="625f9-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="625f9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="625f9-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="625f9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="625f9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="625f9-135">CommonParameters</span></span>
<span data-ttu-id="625f9-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="625f9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="625f9-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="625f9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="625f9-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="625f9-138">INPUTS</span></span>

### <span data-ttu-id="625f9-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="625f9-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="625f9-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="625f9-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="625f9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="625f9-141">OUTPUTS</span></span>

### <span data-ttu-id="625f9-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="625f9-142">System.Object</span></span>
## <span data-ttu-id="625f9-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="625f9-143">NOTES</span></span>

## <span data-ttu-id="625f9-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="625f9-144">RELATED LINKS</span></span>
