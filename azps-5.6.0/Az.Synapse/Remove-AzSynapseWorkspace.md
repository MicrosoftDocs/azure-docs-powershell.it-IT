---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: f8fc68c94142f9c215a6662e7bf41423c1b5de40
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993143"
---
# <span data-ttu-id="807ad-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="807ad-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="807ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="807ad-102">SYNOPSIS</span></span>
<span data-ttu-id="807ad-103">Elimina un'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="807ad-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="807ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="807ad-104">SYNTAX</span></span>

### <span data-ttu-id="807ad-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="807ad-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ad-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ad-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807ad-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="807ad-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="807ad-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="807ad-108">DESCRIPTION</span></span>
<span data-ttu-id="807ad-109">Il cmdlet **Remove-AzSynapseWorkspace** elimina definitivamente un'area di lavoro di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="807ad-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="807ad-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="807ad-110">EXAMPLES</span></span>

### <span data-ttu-id="807ad-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="807ad-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="807ad-112">Questo comando elimina un'area di lavoro di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="807ad-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="807ad-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="807ad-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="807ad-114">Questo comando elimina un'area di lavoro analisi di Azure Synapse tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="807ad-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="807ad-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="807ad-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="807ad-116">Questo comando elimina un'area di lavoro di Azure Synapse Analytics tramite pipeline con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="807ad-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="807ad-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="807ad-117">PARAMETERS</span></span>

### <span data-ttu-id="807ad-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="807ad-118">-AsJob</span></span>
<span data-ttu-id="807ad-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="807ad-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="807ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="807ad-120">-DefaultProfile</span></span>
<span data-ttu-id="807ad-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="807ad-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="807ad-122">-Force</span><span class="sxs-lookup"><span data-stu-id="807ad-122">-Force</span></span>
<span data-ttu-id="807ad-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="807ad-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="807ad-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="807ad-124">-InputObject</span></span>
<span data-ttu-id="807ad-125">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="807ad-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="807ad-126">-Name</span><span class="sxs-lookup"><span data-stu-id="807ad-126">-Name</span></span>
<span data-ttu-id="807ad-127">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="807ad-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807ad-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="807ad-128">-PassThru</span></span>
<span data-ttu-id="807ad-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="807ad-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="807ad-130">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="807ad-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="807ad-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="807ad-131">-ResourceGroupName</span></span>
<span data-ttu-id="807ad-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="807ad-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807ad-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="807ad-133">-ResourceId</span></span>
<span data-ttu-id="807ad-134">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="807ad-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807ad-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="807ad-135">-Confirm</span></span>
<span data-ttu-id="807ad-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="807ad-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="807ad-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="807ad-137">-WhatIf</span></span>
<span data-ttu-id="807ad-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="807ad-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="807ad-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="807ad-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="807ad-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="807ad-140">CommonParameters</span></span>
<span data-ttu-id="807ad-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="807ad-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="807ad-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="807ad-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="807ad-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="807ad-143">INPUTS</span></span>

### <span data-ttu-id="807ad-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="807ad-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="807ad-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="807ad-145">OUTPUTS</span></span>

### <span data-ttu-id="807ad-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="807ad-146">System.Boolean</span></span>

## <span data-ttu-id="807ad-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="807ad-147">NOTES</span></span>

## <span data-ttu-id="807ad-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="807ad-148">RELATED LINKS</span></span>
