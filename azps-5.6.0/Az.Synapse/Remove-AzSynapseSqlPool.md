---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 298077ced1b7cb308bae4a8a5d27e13893c4b4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999164"
---
# <span data-ttu-id="401d5-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="401d5-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="401d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="401d5-102">SYNOPSIS</span></span>
<span data-ttu-id="401d5-103">Elimina un pool di SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="401d5-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="401d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="401d5-104">SYNTAX</span></span>

### <span data-ttu-id="401d5-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="401d5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="401d5-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="401d5-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="401d5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="401d5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="401d5-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="401d5-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="401d5-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="401d5-109">DESCRIPTION</span></span>
<span data-ttu-id="401d5-110">Il cmdlet **Remove-AzSynapseSqlPool** elimina definitivamente un SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="401d5-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="401d5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="401d5-111">EXAMPLES</span></span>

### <span data-ttu-id="401d5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="401d5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="401d5-113">Questo comando elimina un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="401d5-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="401d5-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="401d5-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="401d5-115">Questo comando elimina un pool di SQL Azure Synapse Analytics tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="401d5-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="401d5-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="401d5-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="401d5-117">Questo comando elimina un pool di SQL Azure Synapse Analytics tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="401d5-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="401d5-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="401d5-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="401d5-119">Questo comando elimina un pool di SQL Azure Synapse Analytics con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="401d5-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="401d5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="401d5-120">PARAMETERS</span></span>

### <span data-ttu-id="401d5-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="401d5-121">-AsJob</span></span>
<span data-ttu-id="401d5-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="401d5-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="401d5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="401d5-123">-DefaultProfile</span></span>
<span data-ttu-id="401d5-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="401d5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="401d5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="401d5-125">-Force</span></span>
<span data-ttu-id="401d5-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="401d5-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="401d5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="401d5-127">-InputObject</span></span>
<span data-ttu-id="401d5-128">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="401d5-128">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="401d5-129">-Name</span><span class="sxs-lookup"><span data-stu-id="401d5-129">-Name</span></span>
<span data-ttu-id="401d5-130">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="401d5-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="401d5-131">-PassThru</span></span>
<span data-ttu-id="401d5-132">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="401d5-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="401d5-133">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="401d5-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="401d5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="401d5-134">-ResourceGroupName</span></span>
<span data-ttu-id="401d5-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="401d5-135">Resource group name.</span></span>

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

### <span data-ttu-id="401d5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="401d5-136">-ResourceId</span></span>
<span data-ttu-id="401d5-137">Identificatore di risorsa del pool SQL synapse.</span><span class="sxs-lookup"><span data-stu-id="401d5-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="401d5-138">-Version</span><span class="sxs-lookup"><span data-stu-id="401d5-138">-Version</span></span>
<span data-ttu-id="401d5-139">Versione di Synapse SQL pool.</span><span class="sxs-lookup"><span data-stu-id="401d5-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="401d5-140">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="401d5-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="401d5-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="401d5-141">-WorkspaceName</span></span>
<span data-ttu-id="401d5-142">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="401d5-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="401d5-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="401d5-143">-WorkspaceObject</span></span>
<span data-ttu-id="401d5-144">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="401d5-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="401d5-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="401d5-145">-Confirm</span></span>
<span data-ttu-id="401d5-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="401d5-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="401d5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="401d5-147">-WhatIf</span></span>
<span data-ttu-id="401d5-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="401d5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="401d5-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="401d5-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="401d5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="401d5-150">CommonParameters</span></span>
<span data-ttu-id="401d5-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="401d5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="401d5-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="401d5-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="401d5-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="401d5-153">INPUTS</span></span>

### <span data-ttu-id="401d5-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="401d5-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="401d5-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="401d5-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="401d5-156">System.String</span><span class="sxs-lookup"><span data-stu-id="401d5-156">System.String</span></span>

## <span data-ttu-id="401d5-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="401d5-157">OUTPUTS</span></span>

### <span data-ttu-id="401d5-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="401d5-158">System.Boolean</span></span>

## <span data-ttu-id="401d5-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="401d5-159">NOTES</span></span>

## <span data-ttu-id="401d5-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="401d5-160">RELATED LINKS</span></span>
