---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 0882789e230c012fe9f23dcdbeeb5378e9b91781
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200597"
---
# <span data-ttu-id="3df74-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="3df74-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="3df74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3df74-102">SYNOPSIS</span></span>
<span data-ttu-id="3df74-103">Rimuove un trigger da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3df74-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="3df74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3df74-104">SYNTAX</span></span>

### <span data-ttu-id="3df74-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3df74-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3df74-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3df74-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3df74-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="3df74-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3df74-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3df74-108">DESCRIPTION</span></span>
<span data-ttu-id="3df74-109">Il cmdlet **Remove-AzSynapseTrigger** rimuove un trigger da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3df74-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="3df74-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3df74-110">EXAMPLES</span></span>

### <span data-ttu-id="3df74-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3df74-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="3df74-112">Rimuovere un trigger denominato ContosoTrigger dall'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3df74-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="3df74-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3df74-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="3df74-114">Rimuovere un trigger denominato ContosoTrigger dall'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="3df74-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="3df74-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3df74-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="3df74-116">Rimuovere un trigger denominato ContosoTrigger dall'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="3df74-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="3df74-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3df74-117">PARAMETERS</span></span>

### <span data-ttu-id="3df74-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3df74-118">-AsJob</span></span>
<span data-ttu-id="3df74-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3df74-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3df74-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df74-120">-DefaultProfile</span></span>
<span data-ttu-id="3df74-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3df74-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3df74-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3df74-122">-InputObject</span></span>
<span data-ttu-id="3df74-123">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="3df74-123">The trigger object.</span></span>

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

### <span data-ttu-id="3df74-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3df74-124">-Name</span></span>
<span data-ttu-id="3df74-125">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="3df74-125">The trigger name.</span></span>

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

### <span data-ttu-id="3df74-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3df74-126">-PassThru</span></span>
<span data-ttu-id="3df74-127">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3df74-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3df74-128">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="3df74-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3df74-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3df74-129">-WorkspaceName</span></span>
<span data-ttu-id="3df74-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3df74-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3df74-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3df74-131">-WorkspaceObject</span></span>
<span data-ttu-id="3df74-132">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="3df74-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3df74-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3df74-133">-Confirm</span></span>
<span data-ttu-id="3df74-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3df74-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df74-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df74-135">-WhatIf</span></span>
<span data-ttu-id="3df74-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3df74-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3df74-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3df74-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3df74-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df74-138">CommonParameters</span></span>
<span data-ttu-id="3df74-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3df74-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df74-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3df74-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df74-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3df74-141">INPUTS</span></span>

### <span data-ttu-id="3df74-142">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3df74-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3df74-143">Microsoft. Azure. Commands. sinapsi. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="3df74-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="3df74-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3df74-144">OUTPUTS</span></span>

### <span data-ttu-id="3df74-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3df74-145">System.Boolean</span></span>

## <span data-ttu-id="3df74-146">Note</span><span class="sxs-lookup"><span data-stu-id="3df74-146">NOTES</span></span>

## <span data-ttu-id="3df74-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3df74-147">RELATED LINKS</span></span>