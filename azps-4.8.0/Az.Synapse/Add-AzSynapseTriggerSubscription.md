---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189989"
---
# <span data-ttu-id="94e62-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="94e62-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="94e62-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94e62-102">SYNOPSIS</span></span>
<span data-ttu-id="94e62-103">Sottoscrivere il trigger dell'evento per gli eventi del servizio esterno.</span><span class="sxs-lookup"><span data-stu-id="94e62-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="94e62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94e62-104">SYNTAX</span></span>

### <span data-ttu-id="94e62-105">AddByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94e62-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e62-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="94e62-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e62-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="94e62-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94e62-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94e62-108">DESCRIPTION</span></span>
<span data-ttu-id="94e62-109">Il cmdlet **Add-AzSynapseTriggerSubscription** sottoscrive il trigger di evento agli eventi del servizio esterno specificati dal trigger definizione.</span><span class="sxs-lookup"><span data-stu-id="94e62-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="94e62-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94e62-110">EXAMPLES</span></span>

### <span data-ttu-id="94e62-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94e62-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="94e62-112">Questo comando eseguirà la sottoscrizione del trigger denominato ContosoTrigger agli eventi specificati dal trigger definizione.</span><span class="sxs-lookup"><span data-stu-id="94e62-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="94e62-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="94e62-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="94e62-114">Questo comando eseguirà la sottoscrizione del trigger denominato ContosoTrigger agli eventi specificati dal trigger definizione tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="94e62-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="94e62-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="94e62-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="94e62-116">Questo comando eseguirà la sottoscrizione del trigger denominato ContosoTrigger agli eventi specificati dal trigger definizione tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="94e62-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="94e62-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94e62-117">PARAMETERS</span></span>

### <span data-ttu-id="94e62-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94e62-118">-AsJob</span></span>
<span data-ttu-id="94e62-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="94e62-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94e62-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e62-120">-DefaultProfile</span></span>
<span data-ttu-id="94e62-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94e62-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94e62-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94e62-122">-InputObject</span></span>
<span data-ttu-id="94e62-123">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="94e62-123">The trigger object.</span></span>

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

### <span data-ttu-id="94e62-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="94e62-124">-Name</span></span>
<span data-ttu-id="94e62-125">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="94e62-125">The trigger name.</span></span>

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

### <span data-ttu-id="94e62-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="94e62-126">-WorkspaceName</span></span>
<span data-ttu-id="94e62-127">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="94e62-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="94e62-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="94e62-128">-WorkspaceObject</span></span>
<span data-ttu-id="94e62-129">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="94e62-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="94e62-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="94e62-130">-Confirm</span></span>
<span data-ttu-id="94e62-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94e62-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e62-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e62-132">-WhatIf</span></span>
<span data-ttu-id="94e62-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94e62-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94e62-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94e62-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e62-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e62-135">CommonParameters</span></span>
<span data-ttu-id="94e62-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94e62-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e62-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94e62-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e62-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94e62-138">INPUTS</span></span>

### <span data-ttu-id="94e62-139">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="94e62-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="94e62-140">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="94e62-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="94e62-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94e62-141">OUTPUTS</span></span>

### <span data-ttu-id="94e62-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="94e62-142">System.Object</span></span>
## <span data-ttu-id="94e62-143">Note</span><span class="sxs-lookup"><span data-stu-id="94e62-143">NOTES</span></span>

## <span data-ttu-id="94e62-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94e62-144">RELATED LINKS</span></span>
