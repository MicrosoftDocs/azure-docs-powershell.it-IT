---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: 1afa4776aa82dcfddab1709cf08dcfe8cd0ff71b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323117"
---
# <span data-ttu-id="d2d53-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="d2d53-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="d2d53-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2d53-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d53-103">Elimina un pool di scintille di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d2d53-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="d2d53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2d53-104">SYNTAX</span></span>

### <span data-ttu-id="d2d53-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2d53-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2d53-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2d53-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2d53-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2d53-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2d53-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2d53-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2d53-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2d53-109">DESCRIPTION</span></span>
<span data-ttu-id="d2d53-110">Il cmdlet **Remove-AzSynapseSparkPool** Elimina definitivamente un pool di Spark di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d2d53-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="d2d53-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2d53-111">EXAMPLES</span></span>

### <span data-ttu-id="d2d53-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d2d53-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="d2d53-113">Questo comando Elimina un pool di Spark di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d2d53-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="d2d53-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d2d53-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="d2d53-115">Questo comando Elimina un pool di scintille di analisi di Azure sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="d2d53-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="d2d53-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d2d53-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="d2d53-117">Questo comando Elimina un pool di scintille di analisi di Azure sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="d2d53-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="d2d53-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="d2d53-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="d2d53-119">Questo comando Elimina un pool di dati di analisi di Azure sinapsi con un ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d2d53-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="d2d53-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2d53-120">PARAMETERS</span></span>

### <span data-ttu-id="d2d53-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2d53-121">-AsJob</span></span>
<span data-ttu-id="d2d53-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d2d53-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2d53-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2d53-123">-DefaultProfile</span></span>
<span data-ttu-id="d2d53-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2d53-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2d53-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d2d53-125">-Force</span></span>
<span data-ttu-id="d2d53-126">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d2d53-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d2d53-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2d53-127">-InputObject</span></span>
<span data-ttu-id="d2d53-128">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d2d53-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d2d53-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2d53-129">-Name</span></span>
<span data-ttu-id="d2d53-130">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d2d53-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="d2d53-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2d53-131">-PassThru</span></span>
<span data-ttu-id="d2d53-132">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d2d53-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="d2d53-133">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="d2d53-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d2d53-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2d53-134">-ResourceGroupName</span></span>
<span data-ttu-id="d2d53-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d2d53-135">Resource group name.</span></span>

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

### <span data-ttu-id="d2d53-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2d53-136">-ResourceId</span></span>
<span data-ttu-id="d2d53-137">Identificatore delle risorse del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d2d53-137">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="d2d53-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d2d53-138">-WorkspaceName</span></span>
<span data-ttu-id="d2d53-139">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="d2d53-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d2d53-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d2d53-140">-WorkspaceObject</span></span>
<span data-ttu-id="d2d53-141">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d2d53-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d2d53-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2d53-142">-Confirm</span></span>
<span data-ttu-id="d2d53-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2d53-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2d53-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2d53-144">-WhatIf</span></span>
<span data-ttu-id="d2d53-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2d53-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2d53-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2d53-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2d53-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d53-147">CommonParameters</span></span>
<span data-ttu-id="d2d53-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2d53-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d53-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2d53-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d53-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2d53-150">INPUTS</span></span>

### <span data-ttu-id="d2d53-151">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2d53-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d2d53-152">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="d2d53-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="d2d53-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2d53-153">OUTPUTS</span></span>

### <span data-ttu-id="d2d53-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2d53-154">System.Boolean</span></span>

## <span data-ttu-id="d2d53-155">Note</span><span class="sxs-lookup"><span data-stu-id="d2d53-155">NOTES</span></span>

## <span data-ttu-id="d2d53-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2d53-156">RELATED LINKS</span></span>
