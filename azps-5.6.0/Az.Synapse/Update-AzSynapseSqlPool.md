---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: fe13a82a6662b0f8e9578f4f0fd5143b350538c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959950"
---
# <span data-ttu-id="00797-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="00797-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="00797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00797-102">SYNOPSIS</span></span>
<span data-ttu-id="00797-103">Aggiorna un pool di SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="00797-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="00797-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00797-104">SYNTAX</span></span>

### <span data-ttu-id="00797-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00797-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00797-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00797-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00797-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00797-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00797-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00797-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00797-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="00797-109">DESCRIPTION</span></span>
<span data-ttu-id="00797-110">Il cmdlet **Update-AzSynapseSqlPool** aggiorna un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="00797-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="00797-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00797-111">EXAMPLES</span></span>

### <span data-ttu-id="00797-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="00797-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="00797-113">Questo comando aggiorna un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="00797-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="00797-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="00797-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="00797-115">Questo comando aggiorna un pool di SQL Azure Synapse Analytics tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="00797-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="00797-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="00797-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="00797-117">Questo comando aggiorna un pool di SQL Azure Synapse Analytics tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="00797-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="00797-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="00797-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="00797-119">Questo comando aggiorna un pool di SQL Azure Synapse Analytics con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="00797-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="00797-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00797-120">PARAMETERS</span></span>

### <span data-ttu-id="00797-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00797-121">-AsJob</span></span>
<span data-ttu-id="00797-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="00797-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00797-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00797-123">-DefaultProfile</span></span>
<span data-ttu-id="00797-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00797-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00797-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00797-125">-InputObject</span></span>
<span data-ttu-id="00797-126">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="00797-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00797-127">-Name</span><span class="sxs-lookup"><span data-stu-id="00797-127">-Name</span></span>
<span data-ttu-id="00797-128">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="00797-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00797-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00797-129">-PassThru</span></span>
<span data-ttu-id="00797-130">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="00797-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="00797-131">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="00797-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="00797-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="00797-132">-PerformanceLevel</span></span>
<span data-ttu-id="00797-133">Il SQL servizio e il livello di prestazioni da assegnare al pool SQL locale.</span><span class="sxs-lookup"><span data-stu-id="00797-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="00797-134">Ad esempio, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="00797-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00797-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00797-135">-ResourceGroupName</span></span>
<span data-ttu-id="00797-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="00797-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00797-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00797-137">-ResourceId</span></span>
<span data-ttu-id="00797-138">Identificatore di risorsa del pool SQL synapse.</span><span class="sxs-lookup"><span data-stu-id="00797-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00797-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="00797-139">-Tag</span></span>
<span data-ttu-id="00797-140">Stringa, dizionario stringa di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="00797-140">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00797-141">-Version</span><span class="sxs-lookup"><span data-stu-id="00797-141">-Version</span></span>
<span data-ttu-id="00797-142">Versione di Synapse SQL pool.</span><span class="sxs-lookup"><span data-stu-id="00797-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="00797-143">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="00797-143">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00797-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="00797-144">-WorkspaceName</span></span>
<span data-ttu-id="00797-145">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="00797-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00797-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="00797-146">-WorkspaceObject</span></span>
<span data-ttu-id="00797-147">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="00797-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00797-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00797-148">-Confirm</span></span>
<span data-ttu-id="00797-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00797-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00797-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00797-150">-WhatIf</span></span>
<span data-ttu-id="00797-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00797-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00797-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00797-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00797-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00797-153">CommonParameters</span></span>
<span data-ttu-id="00797-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00797-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00797-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00797-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00797-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="00797-156">INPUTS</span></span>

### <span data-ttu-id="00797-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="00797-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="00797-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="00797-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="00797-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00797-159">OUTPUTS</span></span>

### <span data-ttu-id="00797-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="00797-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="00797-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="00797-161">NOTES</span></span>

## <span data-ttu-id="00797-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00797-162">RELATED LINKS</span></span>
