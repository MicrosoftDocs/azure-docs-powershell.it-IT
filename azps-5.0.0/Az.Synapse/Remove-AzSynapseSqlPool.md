---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cd715bed20477fae4cbb17d033fd67fefa4e1cdc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200599"
---
# <span data-ttu-id="f8676-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f8676-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="f8676-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8676-102">SYNOPSIS</span></span>
<span data-ttu-id="f8676-103">Elimina un pool SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f8676-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f8676-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8676-104">SYNTAX</span></span>

### <span data-ttu-id="f8676-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8676-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8676-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8676-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8676-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8676-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8676-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8676-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8676-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8676-109">DESCRIPTION</span></span>
<span data-ttu-id="f8676-110">Il cmdlet **Remove-AzSynapseSqlPool** Elimina definitivamente un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8676-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f8676-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8676-111">EXAMPLES</span></span>

### <span data-ttu-id="f8676-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8676-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="f8676-113">Questo comando Elimina un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8676-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="f8676-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f8676-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="f8676-115">Questo comando Elimina un pool SQL di analisi delle sinapsi di Azure tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="f8676-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="f8676-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f8676-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="f8676-117">Questo comando Elimina un pool SQL di analisi delle sinapsi di Azure tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="f8676-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="f8676-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="f8676-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="f8676-119">Questo comando Elimina un pool SQL di analisi delle sinapsi di Azure con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="f8676-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="f8676-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8676-120">PARAMETERS</span></span>

### <span data-ttu-id="f8676-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8676-121">-AsJob</span></span>
<span data-ttu-id="f8676-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f8676-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8676-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8676-123">-DefaultProfile</span></span>
<span data-ttu-id="f8676-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8676-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8676-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8676-125">-InputObject</span></span>
<span data-ttu-id="f8676-126">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f8676-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f8676-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8676-127">-Name</span></span>
<span data-ttu-id="f8676-128">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="f8676-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="f8676-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8676-129">-PassThru</span></span>
<span data-ttu-id="f8676-130">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f8676-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="f8676-131">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="f8676-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f8676-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8676-132">-ResourceGroupName</span></span>
<span data-ttu-id="f8676-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f8676-133">Resource group name.</span></span>

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

### <span data-ttu-id="f8676-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8676-134">-ResourceId</span></span>
<span data-ttu-id="f8676-135">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="f8676-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="f8676-136">-Versione</span><span class="sxs-lookup"><span data-stu-id="f8676-136">-Version</span></span>
<span data-ttu-id="f8676-137">Versione del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="f8676-137">Version of Synapse SQL pool.</span></span> <span data-ttu-id="f8676-138">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="f8676-138">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="f8676-139">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f8676-139">-WorkspaceName</span></span>
<span data-ttu-id="f8676-140">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f8676-140">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f8676-141">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f8676-141">-WorkspaceObject</span></span>
<span data-ttu-id="f8676-142">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f8676-142">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f8676-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f8676-143">-Confirm</span></span>
<span data-ttu-id="f8676-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8676-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8676-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8676-145">-WhatIf</span></span>
<span data-ttu-id="f8676-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8676-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8676-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8676-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8676-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8676-148">CommonParameters</span></span>
<span data-ttu-id="f8676-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8676-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8676-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8676-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8676-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8676-151">INPUTS</span></span>

### <span data-ttu-id="f8676-152">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f8676-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f8676-153">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f8676-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="f8676-154">System. String</span><span class="sxs-lookup"><span data-stu-id="f8676-154">System.String</span></span>

## <span data-ttu-id="f8676-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8676-155">OUTPUTS</span></span>

### <span data-ttu-id="f8676-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8676-156">System.Boolean</span></span>

## <span data-ttu-id="f8676-157">Note</span><span class="sxs-lookup"><span data-stu-id="f8676-157">NOTES</span></span>

## <span data-ttu-id="f8676-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8676-158">RELATED LINKS</span></span>
