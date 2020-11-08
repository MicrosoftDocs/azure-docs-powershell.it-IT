---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 62b1e0ef03d52337c03506d3bddc8bbfd3d5512d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191415"
---
# <span data-ttu-id="19f35-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="19f35-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="19f35-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19f35-102">SYNOPSIS</span></span>
<span data-ttu-id="19f35-103">Aggiorna un pool di analisi delle sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="19f35-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="19f35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19f35-104">SYNTAX</span></span>

### <span data-ttu-id="19f35-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19f35-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f35-106">PauseByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f35-106">PauseByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Suspend] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19f35-107">ResumeByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f35-107">ResumeByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Resume] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19f35-108">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f35-108">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f35-109">PauseByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f35-109">PauseByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Suspend] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f35-110">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f35-110">ResumeByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Resume] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f35-111">PauseByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f35-111">PauseByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f35-112">PauseByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f35-112">PauseByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f35-113">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f35-113">ResumeByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f35-114">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f35-114">ResumeByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f35-115">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f35-115">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19f35-116">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f35-116">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19f35-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19f35-117">DESCRIPTION</span></span>
<span data-ttu-id="19f35-118">Il cmdlet **Update-AzSynapseSqlPool** aggiorna un pool di analisi SQL di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="19f35-118">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="19f35-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19f35-119">EXAMPLES</span></span>

### <span data-ttu-id="19f35-120">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="19f35-120">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="19f35-121">Questo comando aggiorna un pool di analisi SQL di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="19f35-121">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="19f35-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="19f35-122">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="19f35-123">Questo comando aggiorna un pool SQL di analisi della sinapsi di Azure tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="19f35-123">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="19f35-124">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="19f35-124">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="19f35-125">Questo comando aggiorna un pool SQL di analisi della sinapsi di Azure tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="19f35-125">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="19f35-126">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="19f35-126">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="19f35-127">Questo comando aggiorna un pool SQL di analisi delle sinapsi di Azure con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="19f35-127">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="19f35-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19f35-128">PARAMETERS</span></span>

### <span data-ttu-id="19f35-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19f35-129">-AsJob</span></span>
<span data-ttu-id="19f35-130">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="19f35-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19f35-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19f35-131">-DefaultProfile</span></span>
<span data-ttu-id="19f35-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19f35-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19f35-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19f35-133">-InputObject</span></span>
<span data-ttu-id="19f35-134">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="19f35-134">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: PauseByInputObjectParameterSet, ResumeByInputObjectParameterSet, UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19f35-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="19f35-135">-Name</span></span>
<span data-ttu-id="19f35-136">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="19f35-136">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet, UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f35-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19f35-137">-PassThru</span></span>
<span data-ttu-id="19f35-138">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="19f35-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="19f35-139">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="19f35-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="19f35-140">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="19f35-140">-PerformanceLevel</span></span>
<span data-ttu-id="19f35-141">Livello di prestazioni e livelli di servizio SQL da assegnare al pool SQL.</span><span class="sxs-lookup"><span data-stu-id="19f35-141">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="19f35-142">Ad esempio, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="19f35-142">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f35-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19f35-143">-ResourceGroupName</span></span>
<span data-ttu-id="19f35-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="19f35-144">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f35-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19f35-145">-ResourceId</span></span>
<span data-ttu-id="19f35-146">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="19f35-146">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: PauseByResourceIdParameterSet, ResumeByResourceIdParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f35-147">-Curriculum vitae</span><span class="sxs-lookup"><span data-stu-id="19f35-147">-Resume</span></span>
<span data-ttu-id="19f35-148">Indica la ripresa del pool SQL</span><span class="sxs-lookup"><span data-stu-id="19f35-148">Indicates to resume the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet, ResumeByInputObjectParameterSet, ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f35-149">-Suspend</span><span class="sxs-lookup"><span data-stu-id="19f35-149">-Suspend</span></span>
<span data-ttu-id="19f35-150">Indica di sospendere il pool SQL</span><span class="sxs-lookup"><span data-stu-id="19f35-150">Indicates to pause the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PauseByNameParameterSet, PauseByParentObjectParameterSet, PauseByInputObjectParameterSet, PauseByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f35-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="19f35-151">-Tag</span></span>
<span data-ttu-id="19f35-152">Una stringa, un dizionario di stringhe di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="19f35-152">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f35-153">-Versione</span><span class="sxs-lookup"><span data-stu-id="19f35-153">-Version</span></span>
<span data-ttu-id="19f35-154">Versione del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="19f35-154">Version of Synapse SQL pool.</span></span> <span data-ttu-id="19f35-155">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="19f35-155">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="19f35-156">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="19f35-156">-WorkspaceName</span></span>
<span data-ttu-id="19f35-157">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="19f35-157">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f35-158">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="19f35-158">-WorkspaceObject</span></span>
<span data-ttu-id="19f35-159">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="19f35-159">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19f35-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19f35-160">-Confirm</span></span>
<span data-ttu-id="19f35-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19f35-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19f35-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19f35-162">-WhatIf</span></span>
<span data-ttu-id="19f35-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19f35-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19f35-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19f35-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19f35-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f35-165">CommonParameters</span></span>
<span data-ttu-id="19f35-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19f35-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f35-167">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19f35-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f35-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19f35-168">INPUTS</span></span>

### <span data-ttu-id="19f35-169">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="19f35-169">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="19f35-170">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="19f35-170">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="19f35-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19f35-171">OUTPUTS</span></span>

### <span data-ttu-id="19f35-172">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="19f35-172">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="19f35-173">Note</span><span class="sxs-lookup"><span data-stu-id="19f35-173">NOTES</span></span>

## <span data-ttu-id="19f35-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19f35-174">RELATED LINKS</span></span>
