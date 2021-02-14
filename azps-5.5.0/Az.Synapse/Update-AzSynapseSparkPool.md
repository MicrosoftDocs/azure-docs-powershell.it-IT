---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197295"
---
# <span data-ttu-id="fdb8c-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="fdb8c-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="fdb8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdb8c-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb8c-103">Aggiorna un pool Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="fdb8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdb8c-104">SYNTAX</span></span>

### <span data-ttu-id="fdb8c-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fdb8c-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb8c-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb8c-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb8c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb8c-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb8c-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb8c-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb8c-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fdb8c-109">DESCRIPTION</span></span>
<span data-ttu-id="fdb8c-110">Il cmdlet **Update-AzSynapseSparkPool** aggiorna un pool Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="fdb8c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdb8c-111">EXAMPLES</span></span>

### <span data-ttu-id="fdb8c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fdb8c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="fdb8c-113">Questo comando aggiorna un pool Spark di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="fdb8c-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fdb8c-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="fdb8c-115">Questo comando aggiorna un pool Spark spark di Azure Synapse tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="fdb8c-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="fdb8c-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="fdb8c-117">Questo comando aggiorna un pool Spark spark di Azure Synapse tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="fdb8c-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="fdb8c-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="fdb8c-119">Questo comando aggiorna un pool Spark spark di Azure Synapse Analytics con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="fdb8c-120">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="fdb8c-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="fdb8c-121">Questo comando abilita il ridimensionamento automatico per un pool Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="fdb8c-122">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="fdb8c-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="fdb8c-123">Questo comando disabilita il ridimensionamento automatico per un pool Spark di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="fdb8c-124">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="fdb8c-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="fdb8c-125">Questo comando abilita la pausa automatica per un pool Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="fdb8c-126">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="fdb8c-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="fdb8c-127">Questo comando disabilita la pausa automatica per un pool Spark di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="fdb8c-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdb8c-128">PARAMETERS</span></span>

### <span data-ttu-id="fdb8c-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdb8c-129">-AsJob</span></span>
<span data-ttu-id="fdb8c-130">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fdb8c-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdb8c-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="fdb8c-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="fdb8c-132">Numero di minuti di inattività.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-132">Number of minutes idle.</span></span> <span data-ttu-id="fdb8c-133">Questo parametro deve essere specificato quando è abilitata la pausa automatica.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-133">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="fdb8c-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="fdb8c-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="fdb8c-135">Numero massimo di nodi da allocare nel pool spark specificato.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="fdb8c-136">Questo parametro deve essere specificato quando è abilitata la scala automatica.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-136">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="fdb8c-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="fdb8c-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="fdb8c-138">Numero minimo di nodi da allocare nel pool spark specificato.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="fdb8c-139">Questo parametro deve essere specificato quando è abilitata la scala automatica.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-139">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="fdb8c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb8c-140">-DefaultProfile</span></span>
<span data-ttu-id="fdb8c-141">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdb8c-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="fdb8c-142">-EnableAutoPause</span></span>
<span data-ttu-id="fdb8c-143">Indica se la pausa automatica deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-143">Indicates whether Auto-pause should be enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb8c-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="fdb8c-144">-EnableAutoScale</span></span>
<span data-ttu-id="fdb8c-145">Indica se la scala automatica deve essere abilitata</span><span class="sxs-lookup"><span data-stu-id="fdb8c-145">Indicates whether Auto-scale should be enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb8c-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdb8c-146">-InputObject</span></span>
<span data-ttu-id="fdb8c-147">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-147">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb8c-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="fdb8c-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="fdb8c-149">File di configurazione dell'ambiente ("Output PIP freeze").</span><span class="sxs-lookup"><span data-stu-id="fdb8c-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="fdb8c-150">-Name</span><span class="sxs-lookup"><span data-stu-id="fdb8c-150">-Name</span></span>
<span data-ttu-id="fdb8c-151">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-151">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb8c-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="fdb8c-152">-NodeCount</span></span>
<span data-ttu-id="fdb8c-153">Numero di nodi da allocare nel pool Spark specificato.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="fdb8c-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="fdb8c-154">-NodeSize</span></span>
<span data-ttu-id="fdb8c-155">Numero di core e memoria da usare per i nodi allocati nel pool Spark specificato.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="fdb8c-156">Questo parametro deve essere specificato quando la scala automatica è disabilitata</span><span class="sxs-lookup"><span data-stu-id="fdb8c-156">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb8c-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb8c-157">-ResourceGroupName</span></span>
<span data-ttu-id="fdb8c-158">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb8c-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdb8c-159">-ResourceId</span></span>
<span data-ttu-id="fdb8c-160">Identificatore di risorsa del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-160">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb8c-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="fdb8c-161">-SparkVersion</span></span>
<span data-ttu-id="fdb8c-162">Versione Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-162">Apache Spark version.</span></span>
<span data-ttu-id="fdb8c-163">Valori consentiti: 2,4</span><span class="sxs-lookup"><span data-stu-id="fdb8c-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="fdb8c-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="fdb8c-164">-Tag</span></span>
<span data-ttu-id="fdb8c-165">Stringa, dizionario stringa di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-165">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="fdb8c-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fdb8c-166">-WorkspaceName</span></span>
<span data-ttu-id="fdb8c-167">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-167">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb8c-168">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fdb8c-168">-WorkspaceObject</span></span>
<span data-ttu-id="fdb8c-169">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-169">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb8c-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdb8c-170">-Confirm</span></span>
<span data-ttu-id="fdb8c-171">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb8c-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb8c-172">-WhatIf</span></span>
<span data-ttu-id="fdb8c-173">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdb8c-174">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb8c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb8c-175">CommonParameters</span></span>
<span data-ttu-id="fdb8c-176">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb8c-177">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fdb8c-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb8c-178">INPUT</span><span class="sxs-lookup"><span data-stu-id="fdb8c-178">INPUTS</span></span>

### <span data-ttu-id="fdb8c-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fdb8c-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fdb8c-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="fdb8c-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="fdb8c-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdb8c-181">OUTPUTS</span></span>

### <span data-ttu-id="fdb8c-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="fdb8c-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="fdb8c-183">NOTE</span><span class="sxs-lookup"><span data-stu-id="fdb8c-183">NOTES</span></span>

## <span data-ttu-id="fdb8c-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdb8c-184">RELATED LINKS</span></span>
