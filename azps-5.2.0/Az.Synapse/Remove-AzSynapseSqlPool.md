---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cce6c35fa1186829760bab7c69d9e149cedfc015
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337180"
---
# <span data-ttu-id="b6f1c-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b6f1c-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="b6f1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f1c-103">Elimina un pool SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b6f1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6f1c-104">SYNTAX</span></span>

### <span data-ttu-id="b6f1c-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6f1c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6f1c-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6f1c-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f1c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6f1c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f1c-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6f1c-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6f1c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6f1c-109">DESCRIPTION</span></span>
<span data-ttu-id="b6f1c-110">Il cmdlet **Remove-AzSynapseSqlPool** Elimina definitivamente un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b6f1c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6f1c-111">EXAMPLES</span></span>

### <span data-ttu-id="b6f1c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6f1c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="b6f1c-113">Questo comando Elimina un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="b6f1c-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b6f1c-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="b6f1c-115">Questo comando Elimina un pool SQL di analisi delle sinapsi di Azure tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="b6f1c-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b6f1c-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="b6f1c-117">Questo comando Elimina un pool SQL di analisi delle sinapsi di Azure tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="b6f1c-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b6f1c-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="b6f1c-119">Questo comando Elimina un pool SQL di analisi delle sinapsi di Azure con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="b6f1c-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6f1c-120">PARAMETERS</span></span>

### <span data-ttu-id="b6f1c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6f1c-121">-AsJob</span></span>
<span data-ttu-id="b6f1c-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b6f1c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6f1c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f1c-123">-DefaultProfile</span></span>
<span data-ttu-id="b6f1c-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f1c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b6f1c-125">-Force</span></span>
<span data-ttu-id="b6f1c-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b6f1c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6f1c-127">-InputObject</span></span>
<span data-ttu-id="b6f1c-128">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-128">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b6f1c-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6f1c-129">-Name</span></span>
<span data-ttu-id="b6f1c-130">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="b6f1c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6f1c-131">-PassThru</span></span>
<span data-ttu-id="b6f1c-132">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="b6f1c-133">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b6f1c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f1c-134">-ResourceGroupName</span></span>
<span data-ttu-id="b6f1c-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-135">Resource group name.</span></span>

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

### <span data-ttu-id="b6f1c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6f1c-136">-ResourceId</span></span>
<span data-ttu-id="b6f1c-137">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="b6f1c-138">-Versione</span><span class="sxs-lookup"><span data-stu-id="b6f1c-138">-Version</span></span>
<span data-ttu-id="b6f1c-139">Versione del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="b6f1c-140">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="b6f1c-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b6f1c-141">-WorkspaceName</span></span>
<span data-ttu-id="b6f1c-142">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b6f1c-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b6f1c-143">-WorkspaceObject</span></span>
<span data-ttu-id="b6f1c-144">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b6f1c-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b6f1c-145">-Confirm</span></span>
<span data-ttu-id="b6f1c-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f1c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f1c-147">-WhatIf</span></span>
<span data-ttu-id="b6f1c-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f1c-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f1c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f1c-150">CommonParameters</span></span>
<span data-ttu-id="b6f1c-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6f1c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f1c-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6f1c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f1c-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6f1c-153">INPUTS</span></span>

### <span data-ttu-id="b6f1c-154">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b6f1c-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b6f1c-155">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b6f1c-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="b6f1c-156">System. String</span><span class="sxs-lookup"><span data-stu-id="b6f1c-156">System.String</span></span>

## <span data-ttu-id="b6f1c-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6f1c-157">OUTPUTS</span></span>

### <span data-ttu-id="b6f1c-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6f1c-158">System.Boolean</span></span>

## <span data-ttu-id="b6f1c-159">Note</span><span class="sxs-lookup"><span data-stu-id="b6f1c-159">NOTES</span></span>

## <span data-ttu-id="b6f1c-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6f1c-160">RELATED LINKS</span></span>
