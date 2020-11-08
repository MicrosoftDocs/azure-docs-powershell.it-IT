---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 79bd39616f33a50684827276c6af919990b269ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199777"
---
# <span data-ttu-id="d150e-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d150e-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="d150e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d150e-102">SYNOPSIS</span></span>
<span data-ttu-id="d150e-103">Aggiorna un pool di analisi delle sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="d150e-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d150e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d150e-104">SYNTAX</span></span>

### <span data-ttu-id="d150e-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d150e-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d150e-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d150e-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d150e-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d150e-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d150e-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d150e-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d150e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d150e-109">DESCRIPTION</span></span>
<span data-ttu-id="d150e-110">Il cmdlet **Update-AzSynapseSqlPool** aggiorna un pool di analisi SQL di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d150e-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d150e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d150e-111">EXAMPLES</span></span>

### <span data-ttu-id="d150e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d150e-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="d150e-113">Questo comando aggiorna un pool di analisi SQL di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d150e-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="d150e-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d150e-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="d150e-115">Questo comando aggiorna un pool SQL di analisi della sinapsi di Azure tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="d150e-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="d150e-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d150e-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="d150e-117">Questo comando aggiorna un pool SQL di analisi della sinapsi di Azure tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="d150e-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="d150e-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="d150e-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="d150e-119">Questo comando aggiorna un pool SQL di analisi delle sinapsi di Azure con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d150e-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="d150e-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d150e-120">PARAMETERS</span></span>

### <span data-ttu-id="d150e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d150e-121">-AsJob</span></span>
<span data-ttu-id="d150e-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d150e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d150e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d150e-123">-DefaultProfile</span></span>
<span data-ttu-id="d150e-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d150e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d150e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d150e-125">-InputObject</span></span>
<span data-ttu-id="d150e-126">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d150e-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d150e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d150e-127">-Name</span></span>
<span data-ttu-id="d150e-128">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="d150e-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d150e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d150e-129">-PassThru</span></span>
<span data-ttu-id="d150e-130">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d150e-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="d150e-131">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="d150e-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d150e-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="d150e-132">-PerformanceLevel</span></span>
<span data-ttu-id="d150e-133">Livello di prestazioni e livelli di servizio SQL da assegnare al pool SQL.</span><span class="sxs-lookup"><span data-stu-id="d150e-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="d150e-134">Ad esempio, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="d150e-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="d150e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d150e-135">-ResourceGroupName</span></span>
<span data-ttu-id="d150e-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d150e-136">Resource group name.</span></span>

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

### <span data-ttu-id="d150e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d150e-137">-ResourceId</span></span>
<span data-ttu-id="d150e-138">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="d150e-138">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="d150e-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="d150e-139">-Tag</span></span>
<span data-ttu-id="d150e-140">Una stringa, un dizionario di stringhe di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="d150e-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="d150e-141">-Versione</span><span class="sxs-lookup"><span data-stu-id="d150e-141">-Version</span></span>
<span data-ttu-id="d150e-142">Versione del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="d150e-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="d150e-143">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="d150e-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="d150e-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d150e-144">-WorkspaceName</span></span>
<span data-ttu-id="d150e-145">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d150e-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d150e-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d150e-146">-WorkspaceObject</span></span>
<span data-ttu-id="d150e-147">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d150e-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d150e-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d150e-148">-Confirm</span></span>
<span data-ttu-id="d150e-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d150e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d150e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d150e-150">-WhatIf</span></span>
<span data-ttu-id="d150e-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d150e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d150e-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d150e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d150e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d150e-153">CommonParameters</span></span>
<span data-ttu-id="d150e-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d150e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d150e-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d150e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d150e-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d150e-156">INPUTS</span></span>

### <span data-ttu-id="d150e-157">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d150e-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d150e-158">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d150e-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d150e-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d150e-159">OUTPUTS</span></span>

### <span data-ttu-id="d150e-160">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d150e-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d150e-161">Note</span><span class="sxs-lookup"><span data-stu-id="d150e-161">NOTES</span></span>

## <span data-ttu-id="d150e-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d150e-162">RELATED LINKS</span></span>
