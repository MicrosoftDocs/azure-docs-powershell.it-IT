---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: ceeb33615748b7cf11c13441399bbae6a934a56f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383361"
---
# <span data-ttu-id="9e9b6-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="9e9b6-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="9e9b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e9b6-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9b6-103">Elimina un punto di ripristino del pool di analisi di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="9e9b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e9b6-104">SYNTAX</span></span>

### <span data-ttu-id="9e9b6-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e9b6-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e9b6-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e9b6-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e9b6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e9b6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e9b6-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e9b6-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e9b6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e9b6-109">DESCRIPTION</span></span>
<span data-ttu-id="9e9b6-110">Il cmdlet **Remove-AzSynapseSqlPoolRestorePoint** Elimina definitivamente un punto di ripristino di Azure sinapsi di analisi del pool SQL.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="9e9b6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e9b6-111">EXAMPLES</span></span>

### <span data-ttu-id="9e9b6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e9b6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="9e9b6-113">Questo comando Elimina un punto di ripristino del pool SQL di Azure sinapsi Analytics.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="9e9b6-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9e9b6-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="9e9b6-115">Questo comando Elimina un punto di ripristino di un pool di analisi di Azure sinapsi per la pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="9e9b6-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9e9b6-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="9e9b6-117">Questo comando Elimina un punto di ripristino di un pool di analisi di Azure sinapsi per la pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="9e9b6-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="9e9b6-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="9e9b6-119">Questo comando Elimina un punto di ripristino del pool SQL di Azure sinapsi Analytics con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="9e9b6-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e9b6-120">PARAMETERS</span></span>

### <span data-ttu-id="9e9b6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e9b6-121">-AsJob</span></span>
<span data-ttu-id="9e9b6-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9e9b6-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e9b6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e9b6-123">-DefaultProfile</span></span>
<span data-ttu-id="9e9b6-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e9b6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9e9b6-125">-Force</span></span>
<span data-ttu-id="9e9b6-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9e9b6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e9b6-127">-InputObject</span></span>
<span data-ttu-id="9e9b6-128">Oggetto di input data di creazione del punto di ripristino di SQL pool, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e9b6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e9b6-129">-PassThru</span></span>
<span data-ttu-id="9e9b6-130">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9e9b6-131">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9e9b6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e9b6-132">-ResourceGroupName</span></span>
<span data-ttu-id="9e9b6-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-133">Resource group name.</span></span>

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

### <span data-ttu-id="9e9b6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e9b6-134">-ResourceId</span></span>
<span data-ttu-id="9e9b6-135">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="9e9b6-136">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="9e9b6-136">-RestorePointCreationDate</span></span>
<span data-ttu-id="9e9b6-137">Nome della data di creazione del punto di ripristino di SQL sinapsi.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-137">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9b6-138">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="9e9b6-138">-SqlPoolName</span></span>
<span data-ttu-id="9e9b6-139">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-139">Name of Synapse Sql pool.</span></span>

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

### <span data-ttu-id="9e9b6-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="9e9b6-140">-SqlPoolObject</span></span>
<span data-ttu-id="9e9b6-141">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-141">Sql Pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e9b6-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9e9b6-142">-WorkspaceName</span></span>
<span data-ttu-id="9e9b6-143">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9e9b6-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e9b6-144">-Confirm</span></span>
<span data-ttu-id="9e9b6-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e9b6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e9b6-146">-WhatIf</span></span>
<span data-ttu-id="9e9b6-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e9b6-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e9b6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9b6-149">CommonParameters</span></span>
<span data-ttu-id="9e9b6-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e9b6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9b6-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e9b6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9b6-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e9b6-152">INPUTS</span></span>

### <span data-ttu-id="9e9b6-153">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9e9b6-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9e9b6-154">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9e9b6-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="9e9b6-155">Microsoft. Azure. Commands. sinapsi. Models. PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="9e9b6-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="9e9b6-156">System. String</span><span class="sxs-lookup"><span data-stu-id="9e9b6-156">System.String</span></span>

## <span data-ttu-id="9e9b6-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e9b6-157">OUTPUTS</span></span>

### <span data-ttu-id="9e9b6-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e9b6-158">System.Boolean</span></span>

## <span data-ttu-id="9e9b6-159">Note</span><span class="sxs-lookup"><span data-stu-id="9e9b6-159">NOTES</span></span>

## <span data-ttu-id="9e9b6-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e9b6-160">RELATED LINKS</span></span>
