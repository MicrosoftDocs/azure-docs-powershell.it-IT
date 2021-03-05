---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: 22b006d096d1ab2457d53a97a6265bf950c4658e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963453"
---
# <span data-ttu-id="b4f11-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="b4f11-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="b4f11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4f11-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f11-103">Elimina un pool Spark spark di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b4f11-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="b4f11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4f11-104">SYNTAX</span></span>

### <span data-ttu-id="b4f11-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4f11-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f11-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4f11-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f11-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4f11-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f11-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4f11-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4f11-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b4f11-109">DESCRIPTION</span></span>
<span data-ttu-id="b4f11-110">Il cmdlet **Remove-AzSynapseSparkPool** elimina definitivamente un pool Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="b4f11-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="b4f11-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4f11-111">EXAMPLES</span></span>

### <span data-ttu-id="b4f11-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b4f11-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="b4f11-113">Questo comando elimina un pool sparker di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b4f11-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="b4f11-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b4f11-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="b4f11-115">Questo comando elimina un pool Spark spark di Azure Synapse tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4f11-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="b4f11-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b4f11-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="b4f11-117">Questo comando elimina un pool Spark spark di Azure Synapse tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4f11-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="b4f11-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b4f11-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="b4f11-119">Questo comando elimina un pool Spark di Azure Synapse Analytics con un ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b4f11-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="b4f11-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4f11-120">PARAMETERS</span></span>

### <span data-ttu-id="b4f11-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4f11-121">-AsJob</span></span>
<span data-ttu-id="b4f11-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b4f11-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4f11-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f11-123">-DefaultProfile</span></span>
<span data-ttu-id="b4f11-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4f11-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4f11-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b4f11-125">-Force</span></span>
<span data-ttu-id="b4f11-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b4f11-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b4f11-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4f11-127">-InputObject</span></span>
<span data-ttu-id="b4f11-128">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4f11-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b4f11-129">-Name</span><span class="sxs-lookup"><span data-stu-id="b4f11-129">-Name</span></span>
<span data-ttu-id="b4f11-130">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="b4f11-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="b4f11-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4f11-131">-PassThru</span></span>
<span data-ttu-id="b4f11-132">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b4f11-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="b4f11-133">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b4f11-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b4f11-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4f11-134">-ResourceGroupName</span></span>
<span data-ttu-id="b4f11-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4f11-135">Resource group name.</span></span>

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

### <span data-ttu-id="b4f11-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4f11-136">-ResourceId</span></span>
<span data-ttu-id="b4f11-137">Identificatore di risorsa del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="b4f11-137">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="b4f11-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b4f11-138">-WorkspaceName</span></span>
<span data-ttu-id="b4f11-139">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="b4f11-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b4f11-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b4f11-140">-WorkspaceObject</span></span>
<span data-ttu-id="b4f11-141">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4f11-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b4f11-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4f11-142">-Confirm</span></span>
<span data-ttu-id="b4f11-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4f11-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4f11-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4f11-144">-WhatIf</span></span>
<span data-ttu-id="b4f11-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4f11-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4f11-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4f11-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4f11-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f11-147">CommonParameters</span></span>
<span data-ttu-id="b4f11-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f11-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f11-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b4f11-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f11-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="b4f11-150">INPUTS</span></span>

### <span data-ttu-id="b4f11-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b4f11-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b4f11-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="b4f11-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="b4f11-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4f11-153">OUTPUTS</span></span>

### <span data-ttu-id="b4f11-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4f11-154">System.Boolean</span></span>

## <span data-ttu-id="b4f11-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="b4f11-155">NOTES</span></span>

## <span data-ttu-id="b4f11-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4f11-156">RELATED LINKS</span></span>
