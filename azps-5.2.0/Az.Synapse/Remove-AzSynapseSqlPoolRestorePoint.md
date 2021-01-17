---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: e9c4c68f794b5ea0c20b0e1fe57677b329b02622
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343111"
---
# <span data-ttu-id="6b4a3-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="6b4a3-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="6b4a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="6b4a3-103">Elimina un punto di ripristino del pool di analisi di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="6b4a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b4a3-104">SYNTAX</span></span>

### <span data-ttu-id="6b4a3-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b4a3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String> -Name <String> 
[-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b4a3-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b4a3-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -Name <String> -SqlPoolObject <PSSynapseSqlPool> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b4a3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b4a3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b4a3-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b4a3-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b4a3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b4a3-109">DESCRIPTION</span></span>
<span data-ttu-id="6b4a3-110">Il cmdlet **Remove-AzSynapseSqlPoolRestorePoint** Elimina definitivamente un punto di ripristino di Azure sinapsi di analisi del pool SQL.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="6b4a3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b4a3-111">EXAMPLES</span></span>

### <span data-ttu-id="6b4a3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6b4a3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="6b4a3-113">Questo comando Elimina un punto di ripristino del pool SQL di Azure sinapsi Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="6b4a3-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6b4a3-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="6b4a3-115">Questo comando Elimina un punto di ripristino di un pool di analisi di Azure sinapsi per la pipeline.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="6b4a3-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6b4a3-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="6b4a3-117">Questo comando Elimina un punto di ripristino di un pool di analisi di Azure sinapsi per la pipeline.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="6b4a3-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="6b4a3-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="6b4a3-119">Questo comando Elimina un punto di ripristino del pool SQL di Azure sinapsi Analytics con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="6b4a3-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b4a3-120">PARAMETERS</span></span>

### <span data-ttu-id="6b4a3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b4a3-121">-AsJob</span></span>
<span data-ttu-id="6b4a3-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6b4a3-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b4a3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6b4a3-123">-Force</span></span>
<span data-ttu-id="6b4a3-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-124">Do not ask for confirmation.</span></span>

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


### <span data-ttu-id="6b4a3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b4a3-125">-InputObject</span></span>
<span data-ttu-id="6b4a3-126">Oggetto di input data di creazione del punto di ripristino di SQL pool, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-126">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b4a3-127">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="6b4a3-127">-RestorePointCreationDate</span></span>
<span data-ttu-id="6b4a3-128">Nome della data di creazione del punto di ripristino di SQL sinapsi.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-128">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b4a3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b4a3-129">-PassThru</span></span>
<span data-ttu-id="6b4a3-130">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="6b4a3-131">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6b4a3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b4a3-132">-ResourceGroupName</span></span>
<span data-ttu-id="6b4a3-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-133">Resource group name.</span></span>

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

### <span data-ttu-id="6b4a3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b4a3-134">-ResourceId</span></span>
<span data-ttu-id="6b4a3-135">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-135">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b4a3-136">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="6b4a3-136">-SqlPoolName</span></span>
<span data-ttu-id="6b4a3-137">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-137">Name of Synapse Sql pool.</span></span>

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

### <span data-ttu-id="6b4a3-138">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="6b4a3-138">-SqlPoolObject</span></span>
<span data-ttu-id="6b4a3-139">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-139">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b4a3-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6b4a3-140">-WorkspaceName</span></span>
<span data-ttu-id="6b4a3-141">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6b4a3-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6b4a3-142">-WorkspaceObject</span></span>
<span data-ttu-id="6b4a3-143">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6b4a3-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b4a3-144">-Confirm</span></span>
<span data-ttu-id="6b4a3-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b4a3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b4a3-146">-WhatIf</span></span>
<span data-ttu-id="6b4a3-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b4a3-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b4a3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b4a3-149">CommonParameters</span></span>
<span data-ttu-id="6b4a3-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b4a3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b4a3-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b4a3-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b4a3-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b4a3-152">INPUTS</span></span>

### <span data-ttu-id="6b4a3-153">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6b4a3-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6b4a3-154">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6b4a3-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="6b4a3-155">Microsoft. Azure. Commands. sinapsi. Models. PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="6b4a3-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="6b4a3-156">System. String</span><span class="sxs-lookup"><span data-stu-id="6b4a3-156">System.String</span></span>

## <span data-ttu-id="6b4a3-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b4a3-157">OUTPUTS</span></span>

### <span data-ttu-id="6b4a3-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b4a3-158">System.Boolean</span></span>

## <span data-ttu-id="6b4a3-159">Note</span><span class="sxs-lookup"><span data-stu-id="6b4a3-159">NOTES</span></span>

## <span data-ttu-id="6b4a3-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b4a3-160">RELATED LINKS</span></span>
