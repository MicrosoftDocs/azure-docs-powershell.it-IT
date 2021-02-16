---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 63c0dbc30557230f67e419bcde482e445f3df758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209019"
---
# <span data-ttu-id="c3599-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="c3599-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="c3599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3599-102">SYNOPSIS</span></span>
<span data-ttu-id="c3599-103">Elimina un punto di ripristino del pool SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c3599-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="c3599-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3599-104">SYNTAX</span></span>

### <span data-ttu-id="c3599-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3599-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3599-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3599-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3599-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3599-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3599-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3599-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3599-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3599-109">DESCRIPTION</span></span>
<span data-ttu-id="c3599-110">Il cmdlet **Remove-AzSynapseSqlPoolRestorePoint** elimina definitivamente un SQL di ripristino del pool azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c3599-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="c3599-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3599-111">EXAMPLES</span></span>

### <span data-ttu-id="c3599-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c3599-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="c3599-113">Questo comando elimina un punto di ripristino del pool SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c3599-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="c3599-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c3599-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="c3599-115">Questo comando elimina un punto di ripristino del pool SQL Azure Synapse Analytics tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3599-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="c3599-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c3599-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="c3599-117">Questo comando elimina un punto di ripristino del pool SQL Azure Synapse Analytics tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3599-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="c3599-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="c3599-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="c3599-119">Questo comando elimina un punto di ripristino del SQL azure Synapse Analytics con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="c3599-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="c3599-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3599-120">PARAMETERS</span></span>

### <span data-ttu-id="c3599-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3599-121">-AsJob</span></span>
<span data-ttu-id="c3599-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c3599-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3599-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3599-123">-DefaultProfile</span></span>
<span data-ttu-id="c3599-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3599-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3599-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c3599-125">-Force</span></span>
<span data-ttu-id="c3599-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c3599-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c3599-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3599-127">-InputObject</span></span>
<span data-ttu-id="c3599-128">SQL di input dell'ora di creazione del punto di ripristino del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3599-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c3599-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c3599-129">-Name</span></span>
<span data-ttu-id="c3599-130">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c3599-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3599-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3599-131">-PassThru</span></span>
<span data-ttu-id="c3599-132">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c3599-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="c3599-133">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c3599-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c3599-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3599-134">-ResourceGroupName</span></span>
<span data-ttu-id="c3599-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c3599-135">Resource group name.</span></span>

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

### <span data-ttu-id="c3599-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3599-136">-ResourceId</span></span>
<span data-ttu-id="c3599-137">Identificatore di risorsa dell'SQL pool.</span><span class="sxs-lookup"><span data-stu-id="c3599-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="c3599-138">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="c3599-138">-RestorePointCreationDate</span></span>
<span data-ttu-id="c3599-139">Nome della sinapse SQL data di creazione del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c3599-139">Name of Synapse SQL Restore Point Creation Date .</span></span>

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

### <span data-ttu-id="c3599-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="c3599-140">-SqlPoolObject</span></span>
<span data-ttu-id="c3599-141">Oggetto di input Pool Sql, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3599-141">Sql Pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c3599-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c3599-142">-WorkspaceName</span></span>
<span data-ttu-id="c3599-143">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="c3599-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c3599-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3599-144">-Confirm</span></span>
<span data-ttu-id="c3599-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3599-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3599-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3599-146">-WhatIf</span></span>
<span data-ttu-id="c3599-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3599-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3599-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3599-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3599-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3599-149">CommonParameters</span></span>
<span data-ttu-id="c3599-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3599-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3599-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c3599-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3599-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3599-152">INPUTS</span></span>

### <span data-ttu-id="c3599-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c3599-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c3599-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c3599-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="c3599-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="c3599-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="c3599-156">System.String</span><span class="sxs-lookup"><span data-stu-id="c3599-156">System.String</span></span>

## <span data-ttu-id="c3599-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3599-157">OUTPUTS</span></span>

### <span data-ttu-id="c3599-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c3599-158">System.Boolean</span></span>

## <span data-ttu-id="c3599-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3599-159">NOTES</span></span>

## <span data-ttu-id="c3599-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3599-160">RELATED LINKS</span></span>
