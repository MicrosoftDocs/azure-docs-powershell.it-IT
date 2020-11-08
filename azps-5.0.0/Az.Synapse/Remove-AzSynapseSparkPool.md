---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: d9e3160d5ba0620ff881c940bf8383a7046136a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200601"
---
# <span data-ttu-id="7d81a-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="7d81a-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="7d81a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d81a-102">SYNOPSIS</span></span>
<span data-ttu-id="7d81a-103">Elimina un pool di scintille di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="7d81a-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="7d81a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d81a-104">SYNTAX</span></span>

### <span data-ttu-id="7d81a-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d81a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d81a-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d81a-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d81a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d81a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d81a-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d81a-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d81a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d81a-109">DESCRIPTION</span></span>
<span data-ttu-id="7d81a-110">Il cmdlet **Remove-AzSynapseSparkPool** Elimina definitivamente un pool di Spark di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="7d81a-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="7d81a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d81a-111">EXAMPLES</span></span>

### <span data-ttu-id="7d81a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d81a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="7d81a-113">Questo comando Elimina un pool di Spark di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="7d81a-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="7d81a-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7d81a-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="7d81a-115">Questo comando Elimina un pool di scintille di analisi di Azure sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="7d81a-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="7d81a-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7d81a-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="7d81a-117">Questo comando Elimina un pool di scintille di analisi di Azure sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="7d81a-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="7d81a-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="7d81a-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="7d81a-119">Questo comando Elimina un pool di dati di analisi di Azure sinapsi con un ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7d81a-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="7d81a-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d81a-120">PARAMETERS</span></span>

### <span data-ttu-id="7d81a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d81a-121">-AsJob</span></span>
<span data-ttu-id="7d81a-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7d81a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d81a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d81a-123">-DefaultProfile</span></span>
<span data-ttu-id="7d81a-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d81a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d81a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d81a-125">-InputObject</span></span>
<span data-ttu-id="7d81a-126">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="7d81a-126">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d81a-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d81a-127">-Name</span></span>
<span data-ttu-id="7d81a-128">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="7d81a-128">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d81a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d81a-129">-PassThru</span></span>
<span data-ttu-id="7d81a-130">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7d81a-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="7d81a-131">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="7d81a-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7d81a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d81a-132">-ResourceGroupName</span></span>
<span data-ttu-id="7d81a-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d81a-133">Resource group name.</span></span>

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

### <span data-ttu-id="7d81a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d81a-134">-ResourceId</span></span>
<span data-ttu-id="7d81a-135">Identificatore delle risorse del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="7d81a-135">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d81a-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7d81a-136">-WorkspaceName</span></span>
<span data-ttu-id="7d81a-137">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="7d81a-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7d81a-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7d81a-138">-WorkspaceObject</span></span>
<span data-ttu-id="7d81a-139">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="7d81a-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7d81a-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d81a-140">-Confirm</span></span>
<span data-ttu-id="7d81a-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d81a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d81a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d81a-142">-WhatIf</span></span>
<span data-ttu-id="7d81a-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d81a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d81a-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d81a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d81a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d81a-145">CommonParameters</span></span>
<span data-ttu-id="7d81a-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d81a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d81a-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d81a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d81a-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d81a-148">INPUTS</span></span>

### <span data-ttu-id="7d81a-149">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7d81a-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7d81a-150">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="7d81a-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="7d81a-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d81a-151">OUTPUTS</span></span>

### <span data-ttu-id="7d81a-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d81a-152">System.Boolean</span></span>

## <span data-ttu-id="7d81a-153">Note</span><span class="sxs-lookup"><span data-stu-id="7d81a-153">NOTES</span></span>

## <span data-ttu-id="7d81a-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d81a-154">RELATED LINKS</span></span>
