---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 4951fbe707dbae8c1fdff34e828e468a2d3168bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383386"
---
# <span data-ttu-id="1dee0-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dee0-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="1dee0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dee0-102">SYNOPSIS</span></span>
<span data-ttu-id="1dee0-103">Elimina un database SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="1dee0-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="1dee0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dee0-104">SYNTAX</span></span>

### <span data-ttu-id="1dee0-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1dee0-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dee0-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dee0-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dee0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dee0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dee0-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dee0-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dee0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dee0-109">DESCRIPTION</span></span>
<span data-ttu-id="1dee0-110">Il cmdlet **Remove-AzSynapseSqlPool** Elimina definitivamente un database SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="1dee0-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="1dee0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dee0-111">EXAMPLES</span></span>

### <span data-ttu-id="1dee0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1dee0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="1dee0-113">Questo comando Elimina un database SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="1dee0-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="1dee0-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1dee0-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="1dee0-115">Questo comando Elimina un database SQL di analisi di dati di Azure sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="1dee0-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="1dee0-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1dee0-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="1dee0-117">Questo comando Elimina un database SQL di analisi di dati di Azure sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="1dee0-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="1dee0-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="1dee0-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="1dee0-119">Questo comando Elimina un database SQL di analisi delle sinapsi di Azure con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="1dee0-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="1dee0-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dee0-120">PARAMETERS</span></span>

### <span data-ttu-id="1dee0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dee0-121">-AsJob</span></span>
<span data-ttu-id="1dee0-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1dee0-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dee0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dee0-123">-DefaultProfile</span></span>
<span data-ttu-id="1dee0-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dee0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dee0-125">-Force</span><span class="sxs-lookup"><span data-stu-id="1dee0-125">-Force</span></span>
<span data-ttu-id="1dee0-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1dee0-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1dee0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dee0-127">-InputObject</span></span>
<span data-ttu-id="1dee0-128">Oggetto di input di database SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1dee0-128">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dee0-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dee0-129">-Name</span></span>
<span data-ttu-id="1dee0-130">Nome del database SQL di sinapsi.</span><span class="sxs-lookup"><span data-stu-id="1dee0-130">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="1dee0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dee0-131">-PassThru</span></span>
<span data-ttu-id="1dee0-132">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1dee0-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1dee0-133">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="1dee0-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1dee0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dee0-134">-ResourceGroupName</span></span>
<span data-ttu-id="1dee0-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1dee0-135">Resource group name.</span></span>

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

### <span data-ttu-id="1dee0-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dee0-136">-ResourceId</span></span>
<span data-ttu-id="1dee0-137">Identificatore delle risorse del database SQL di sinapsi.</span><span class="sxs-lookup"><span data-stu-id="1dee0-137">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="1dee0-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1dee0-138">-WorkspaceName</span></span>
<span data-ttu-id="1dee0-139">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="1dee0-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1dee0-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1dee0-140">-WorkspaceObject</span></span>
<span data-ttu-id="1dee0-141">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1dee0-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1dee0-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1dee0-142">-Confirm</span></span>
<span data-ttu-id="1dee0-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dee0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dee0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dee0-144">-WhatIf</span></span>
<span data-ttu-id="1dee0-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dee0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dee0-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dee0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dee0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dee0-147">CommonParameters</span></span>
<span data-ttu-id="1dee0-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dee0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dee0-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dee0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dee0-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dee0-150">INPUTS</span></span>

### <span data-ttu-id="1dee0-151">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1dee0-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1dee0-152">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dee0-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="1dee0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1dee0-153">System.String</span></span>

## <span data-ttu-id="1dee0-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dee0-154">OUTPUTS</span></span>

### <span data-ttu-id="1dee0-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1dee0-155">System.Boolean</span></span>

## <span data-ttu-id="1dee0-156">Note</span><span class="sxs-lookup"><span data-stu-id="1dee0-156">NOTES</span></span>

## <span data-ttu-id="1dee0-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dee0-157">RELATED LINKS</span></span>
