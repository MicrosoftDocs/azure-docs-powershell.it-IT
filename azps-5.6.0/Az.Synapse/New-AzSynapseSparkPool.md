---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c41c6afdda39843afa985a53eb572b64f8bcfe19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976062"
---
# <span data-ttu-id="e03f4-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="e03f4-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="e03f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e03f4-102">SYNOPSIS</span></span>
<span data-ttu-id="e03f4-103">Crea un pool Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="e03f4-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="e03f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e03f4-104">SYNTAX</span></span>

### <span data-ttu-id="e03f4-105">CreateByNameAndEnableAutoScaleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e03f4-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e03f4-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="e03f4-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e03f4-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="e03f4-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e03f4-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="e03f4-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e03f4-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e03f4-109">DESCRIPTION</span></span>
<span data-ttu-id="e03f4-110">Il cmdlet **New-AzSynapseSparkPool** crea un pool Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="e03f4-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="e03f4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e03f4-111">EXAMPLES</span></span>

### <span data-ttu-id="e03f4-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e03f4-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="e03f4-113">Questo comando crea un pool Spark spark di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e03f4-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="e03f4-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e03f4-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="e03f4-115">Questo comando crea un pool Spark spark di Azure Synapse Analytics con la scalabilità automatica abilitata.</span><span class="sxs-lookup"><span data-stu-id="e03f4-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="e03f4-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e03f4-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="e03f4-117">Questo comando crea un pool Spark spark di Azure Synapse Tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="e03f4-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="e03f4-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="e03f4-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="e03f4-119">Questo comando crea un pool Spark spark di Azure Synapse Analytics con la scala automatica abilitata tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="e03f4-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="e03f4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e03f4-120">PARAMETERS</span></span>

### <span data-ttu-id="e03f4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e03f4-121">-AsJob</span></span>
<span data-ttu-id="e03f4-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e03f4-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e03f4-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="e03f4-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="e03f4-124">Numero di minuti di inattività.</span><span class="sxs-lookup"><span data-stu-id="e03f4-124">Number of minutes idle.</span></span> <span data-ttu-id="e03f4-125">Questo parametro deve essere specificato quando è abilitata la pausa automatica.</span><span class="sxs-lookup"><span data-stu-id="e03f4-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="e03f4-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="e03f4-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="e03f4-127">Numero massimo di nodi da allocare nel pool spark specificato.</span><span class="sxs-lookup"><span data-stu-id="e03f4-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="e03f4-128">Questo parametro deve essere specificato quando l'opzione Scala automatica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="e03f4-128">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e03f4-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="e03f4-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="e03f4-130">Numero minimo di nodi da allocare nel pool spark specificato.</span><span class="sxs-lookup"><span data-stu-id="e03f4-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="e03f4-131">Questo parametro deve essere specificato quando l'opzione Scala automatica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="e03f4-131">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e03f4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e03f4-132">-DefaultProfile</span></span>
<span data-ttu-id="e03f4-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e03f4-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e03f4-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="e03f4-134">-EnableAutoPause</span></span>
<span data-ttu-id="e03f4-135">Indica se la pausa automatica deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="e03f4-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="e03f4-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="e03f4-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="e03f4-137">File di configurazione dell'ambiente ("Output PIP freeze").</span><span class="sxs-lookup"><span data-stu-id="e03f4-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="e03f4-138">-Name</span><span class="sxs-lookup"><span data-stu-id="e03f4-138">-Name</span></span>
<span data-ttu-id="e03f4-139">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="e03f4-139">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e03f4-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="e03f4-140">-NodeCount</span></span>
<span data-ttu-id="e03f4-141">Numero di nodi da allocare nel pool Spark specificato.</span><span class="sxs-lookup"><span data-stu-id="e03f4-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndDisableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e03f4-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="e03f4-142">-NodeSize</span></span>
<span data-ttu-id="e03f4-143">Numero di core e memoria da usare per i nodi allocati nel pool Spark specificato.</span><span class="sxs-lookup"><span data-stu-id="e03f4-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="e03f4-144">Questo parametro deve essere specificato quando l'opzione Ridimensionamento automatico è disabilitata</span><span class="sxs-lookup"><span data-stu-id="e03f4-144">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e03f4-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e03f4-145">-ResourceGroupName</span></span>
<span data-ttu-id="e03f4-146">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e03f4-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e03f4-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="e03f4-147">-SparkVersion</span></span>
<span data-ttu-id="e03f4-148">Versione Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="e03f4-148">Apache Spark version.</span></span>
<span data-ttu-id="e03f4-149">Valori consentiti: 2,4</span><span class="sxs-lookup"><span data-stu-id="e03f4-149">Allowed values: 2.4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e03f4-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="e03f4-150">-Tag</span></span>
<span data-ttu-id="e03f4-151">Stringa, dizionario stringa di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="e03f4-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="e03f4-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e03f4-152">-WorkspaceName</span></span>
<span data-ttu-id="e03f4-153">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="e03f4-153">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e03f4-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e03f4-154">-WorkspaceObject</span></span>
<span data-ttu-id="e03f4-155">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="e03f4-155">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectAndEnableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e03f4-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e03f4-156">-Confirm</span></span>
<span data-ttu-id="e03f4-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e03f4-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e03f4-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e03f4-158">-WhatIf</span></span>
<span data-ttu-id="e03f4-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e03f4-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e03f4-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e03f4-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e03f4-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e03f4-161">CommonParameters</span></span>
<span data-ttu-id="e03f4-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e03f4-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e03f4-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e03f4-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e03f4-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="e03f4-164">INPUTS</span></span>

### <span data-ttu-id="e03f4-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e03f4-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e03f4-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e03f4-166">OUTPUTS</span></span>

### <span data-ttu-id="e03f4-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="e03f4-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="e03f4-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="e03f4-168">NOTES</span></span>

## <span data-ttu-id="e03f4-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e03f4-169">RELATED LINKS</span></span>
