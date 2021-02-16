---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 648d215066fb7bd827d43ec9d063a7994ada82f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182702"
---
# <span data-ttu-id="cb27a-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="cb27a-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="cb27a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb27a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb27a-103">Rimuove un trigger da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="cb27a-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="cb27a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb27a-104">SYNTAX</span></span>

### <span data-ttu-id="cb27a-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb27a-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb27a-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="cb27a-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb27a-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb27a-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb27a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cb27a-108">DESCRIPTION</span></span>
<span data-ttu-id="cb27a-109">Il cmdlet **Remove-AzSynapseTrigger** rimuove un trigger da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="cb27a-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="cb27a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb27a-110">EXAMPLES</span></span>

### <span data-ttu-id="cb27a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cb27a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="cb27a-112">Rimuovere un trigger denominato ContosoTrigger dall'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cb27a-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="cb27a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cb27a-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="cb27a-114">Rimuovere un trigger denominato ContosoTrigger dall'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb27a-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="cb27a-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="cb27a-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="cb27a-116">Rimuovere un trigger denominato ContosoTrigger dall'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb27a-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cb27a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb27a-117">PARAMETERS</span></span>

### <span data-ttu-id="cb27a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb27a-118">-AsJob</span></span>
<span data-ttu-id="cb27a-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cb27a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb27a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb27a-120">-DefaultProfile</span></span>
<span data-ttu-id="cb27a-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb27a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb27a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cb27a-122">-Force</span></span>
<span data-ttu-id="cb27a-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cb27a-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cb27a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb27a-124">-InputObject</span></span>
<span data-ttu-id="cb27a-125">Oggetto trigger.</span><span class="sxs-lookup"><span data-stu-id="cb27a-125">The trigger object.</span></span>

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

### <span data-ttu-id="cb27a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="cb27a-126">-Name</span></span>
<span data-ttu-id="cb27a-127">Nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="cb27a-127">The trigger name.</span></span>

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

### <span data-ttu-id="cb27a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb27a-128">-PassThru</span></span>
<span data-ttu-id="cb27a-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cb27a-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cb27a-130">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="cb27a-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cb27a-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cb27a-131">-WorkspaceName</span></span>
<span data-ttu-id="cb27a-132">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="cb27a-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cb27a-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cb27a-133">-WorkspaceObject</span></span>
<span data-ttu-id="cb27a-134">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb27a-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cb27a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb27a-135">-Confirm</span></span>
<span data-ttu-id="cb27a-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb27a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb27a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb27a-137">-WhatIf</span></span>
<span data-ttu-id="cb27a-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb27a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb27a-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb27a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb27a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb27a-140">CommonParameters</span></span>
<span data-ttu-id="cb27a-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb27a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb27a-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb27a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb27a-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="cb27a-143">INPUTS</span></span>

### <span data-ttu-id="cb27a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cb27a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cb27a-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="cb27a-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="cb27a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb27a-146">OUTPUTS</span></span>

### <span data-ttu-id="cb27a-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb27a-147">System.Boolean</span></span>

## <span data-ttu-id="cb27a-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="cb27a-148">NOTES</span></span>

## <span data-ttu-id="cb27a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb27a-149">RELATED LINKS</span></span>
