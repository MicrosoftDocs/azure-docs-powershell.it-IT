---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: fbdca80b33dd15e34a958cb63a41377b400d03ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207618"
---
# <span data-ttu-id="75781-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="75781-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="75781-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75781-102">SYNOPSIS</span></span>
<span data-ttu-id="75781-103">Elimina un'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="75781-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="75781-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75781-104">SYNTAX</span></span>

### <span data-ttu-id="75781-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75781-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75781-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75781-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75781-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75781-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75781-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75781-108">DESCRIPTION</span></span>
<span data-ttu-id="75781-109">Il cmdlet **Remove-AzSynapseWorkspace** elimina definitivamente un'area di lavoro di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="75781-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="75781-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75781-110">EXAMPLES</span></span>

### <span data-ttu-id="75781-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75781-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="75781-112">Questo comando elimina un'area di lavoro di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="75781-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="75781-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="75781-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="75781-114">Questo comando elimina un'area di lavoro analisi di Azure Synapse tramite una pipeline.</span><span class="sxs-lookup"><span data-stu-id="75781-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="75781-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="75781-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="75781-116">Questo comando elimina un'area di lavoro Azure Synapse Analytics tramite pipeline con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="75781-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="75781-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75781-117">PARAMETERS</span></span>

### <span data-ttu-id="75781-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75781-118">-AsJob</span></span>
<span data-ttu-id="75781-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="75781-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75781-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75781-120">-DefaultProfile</span></span>
<span data-ttu-id="75781-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75781-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75781-122">-Force</span><span class="sxs-lookup"><span data-stu-id="75781-122">-Force</span></span>
<span data-ttu-id="75781-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="75781-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="75781-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75781-124">-InputObject</span></span>
<span data-ttu-id="75781-125">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="75781-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="75781-126">-Name</span><span class="sxs-lookup"><span data-stu-id="75781-126">-Name</span></span>
<span data-ttu-id="75781-127">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="75781-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="75781-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75781-128">-PassThru</span></span>
<span data-ttu-id="75781-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="75781-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="75781-130">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="75781-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="75781-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75781-131">-ResourceGroupName</span></span>
<span data-ttu-id="75781-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="75781-132">Resource group name.</span></span>

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

### <span data-ttu-id="75781-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75781-133">-ResourceId</span></span>
<span data-ttu-id="75781-134">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="75781-134">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="75781-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75781-135">-Confirm</span></span>
<span data-ttu-id="75781-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75781-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75781-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75781-137">-WhatIf</span></span>
<span data-ttu-id="75781-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75781-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75781-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75781-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75781-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75781-140">CommonParameters</span></span>
<span data-ttu-id="75781-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75781-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75781-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75781-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75781-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="75781-143">INPUTS</span></span>

### <span data-ttu-id="75781-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="75781-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="75781-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75781-145">OUTPUTS</span></span>

### <span data-ttu-id="75781-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="75781-146">System.Boolean</span></span>

## <span data-ttu-id="75781-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="75781-147">NOTES</span></span>

## <span data-ttu-id="75781-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75781-148">RELATED LINKS</span></span>
