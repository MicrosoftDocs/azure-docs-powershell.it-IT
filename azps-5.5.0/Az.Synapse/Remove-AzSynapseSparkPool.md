---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: 1afa4776aa82dcfddab1709cf08dcfe8cd0ff71b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182719"
---
# <span data-ttu-id="ced4d-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="ced4d-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="ced4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ced4d-102">SYNOPSIS</span></span>
<span data-ttu-id="ced4d-103">Elimina un pool Spark spark di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ced4d-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="ced4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ced4d-104">SYNTAX</span></span>

### <span data-ttu-id="ced4d-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ced4d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced4d-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced4d-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced4d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced4d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced4d-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced4d-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ced4d-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ced4d-109">DESCRIPTION</span></span>
<span data-ttu-id="ced4d-110">Il cmdlet **Remove-AzSynapseSparkPool** elimina definitivamente un pool Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="ced4d-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="ced4d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ced4d-111">EXAMPLES</span></span>

### <span data-ttu-id="ced4d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ced4d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="ced4d-113">Questo comando elimina un pool Spark spark di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ced4d-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="ced4d-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ced4d-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="ced4d-115">Questo comando elimina un pool Spark spark di Azure Synapse tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="ced4d-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="ced4d-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ced4d-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="ced4d-117">Questo comando elimina un pool Spark spark di Azure Synapse tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="ced4d-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="ced4d-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="ced4d-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="ced4d-119">Questo comando elimina un pool Spark di Azure Synapse Analytics con un ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ced4d-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="ced4d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ced4d-120">PARAMETERS</span></span>

### <span data-ttu-id="ced4d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ced4d-121">-AsJob</span></span>
<span data-ttu-id="ced4d-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ced4d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ced4d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced4d-123">-DefaultProfile</span></span>
<span data-ttu-id="ced4d-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ced4d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced4d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ced4d-125">-Force</span></span>
<span data-ttu-id="ced4d-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ced4d-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ced4d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ced4d-127">-InputObject</span></span>
<span data-ttu-id="ced4d-128">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="ced4d-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ced4d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ced4d-129">-Name</span></span>
<span data-ttu-id="ced4d-130">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="ced4d-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced4d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ced4d-131">-PassThru</span></span>
<span data-ttu-id="ced4d-132">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ced4d-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="ced4d-133">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ced4d-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ced4d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced4d-134">-ResourceGroupName</span></span>
<span data-ttu-id="ced4d-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ced4d-135">Resource group name.</span></span>

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

### <span data-ttu-id="ced4d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ced4d-136">-ResourceId</span></span>
<span data-ttu-id="ced4d-137">Identificatore di risorsa del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="ced4d-137">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="ced4d-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ced4d-138">-WorkspaceName</span></span>
<span data-ttu-id="ced4d-139">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="ced4d-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced4d-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ced4d-140">-WorkspaceObject</span></span>
<span data-ttu-id="ced4d-141">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="ced4d-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ced4d-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ced4d-142">-Confirm</span></span>
<span data-ttu-id="ced4d-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ced4d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ced4d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ced4d-144">-WhatIf</span></span>
<span data-ttu-id="ced4d-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ced4d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ced4d-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ced4d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ced4d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced4d-147">CommonParameters</span></span>
<span data-ttu-id="ced4d-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced4d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced4d-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ced4d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced4d-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="ced4d-150">INPUTS</span></span>

### <span data-ttu-id="ced4d-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ced4d-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ced4d-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="ced4d-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="ced4d-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ced4d-153">OUTPUTS</span></span>

### <span data-ttu-id="ced4d-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ced4d-154">System.Boolean</span></span>

## <span data-ttu-id="ced4d-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="ced4d-155">NOTES</span></span>

## <span data-ttu-id="ced4d-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ced4d-156">RELATED LINKS</span></span>
