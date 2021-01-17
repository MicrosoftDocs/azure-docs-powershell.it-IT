---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476559"
---
# <span data-ttu-id="ce183-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="ce183-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="ce183-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce183-102">SYNOPSIS</span></span>
<span data-ttu-id="ce183-103">Crea un trigger in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce183-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="ce183-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce183-104">SYNTAX</span></span>

### <span data-ttu-id="ce183-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce183-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce183-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="ce183-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce183-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce183-107">DESCRIPTION</span></span>
<span data-ttu-id="ce183-108">Il cmdlet **set-AzSynapseTrigger** crea un trigger in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce183-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="ce183-109">I trigger vengono creati nello stato "Stopped", quindi non iniziano immediatamente a richiamare pipeline a cui fanno riferimento.</span><span class="sxs-lookup"><span data-stu-id="ce183-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="ce183-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce183-110">EXAMPLES</span></span>

### <span data-ttu-id="ce183-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce183-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="ce183-112">Creare un nuovo trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ce183-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="ce183-113">Il trigger viene creato nello stato "Stopped", quindi non si avvia immediatamente.</span><span class="sxs-lookup"><span data-stu-id="ce183-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="ce183-114">È possibile avviare un trigger usando il `Start-AzDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce183-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="ce183-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ce183-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="ce183-116">Creare un nuovo trigger denominato ContosoTrigger nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce183-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="ce183-117">Il trigger viene creato nello stato "Stopped", quindi non si avvia immediatamente.</span><span class="sxs-lookup"><span data-stu-id="ce183-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="ce183-118">È possibile avviare un trigger usando il `Start-AzDataFactoryV2Trigger` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce183-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="ce183-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce183-119">PARAMETERS</span></span>

### <span data-ttu-id="ce183-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce183-120">-AsJob</span></span>
<span data-ttu-id="ce183-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ce183-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce183-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce183-122">-DefaultProfile</span></span>
<span data-ttu-id="ce183-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce183-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce183-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ce183-124">-DefinitionFile</span></span>
<span data-ttu-id="ce183-125">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="ce183-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce183-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce183-126">-Name</span></span>
<span data-ttu-id="ce183-127">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="ce183-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce183-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce183-128">-WorkspaceName</span></span>
<span data-ttu-id="ce183-129">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="ce183-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce183-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ce183-130">-WorkspaceObject</span></span>
<span data-ttu-id="ce183-131">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce183-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce183-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce183-132">-Confirm</span></span>
<span data-ttu-id="ce183-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce183-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce183-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce183-134">-WhatIf</span></span>
<span data-ttu-id="ce183-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce183-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce183-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce183-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce183-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce183-137">CommonParameters</span></span>
<span data-ttu-id="ce183-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce183-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce183-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce183-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce183-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce183-140">INPUTS</span></span>

### <span data-ttu-id="ce183-141">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce183-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ce183-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce183-142">OUTPUTS</span></span>

### <span data-ttu-id="ce183-143">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="ce183-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="ce183-144">Note</span><span class="sxs-lookup"><span data-stu-id="ce183-144">NOTES</span></span>

## <span data-ttu-id="ce183-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce183-145">RELATED LINKS</span></span>
