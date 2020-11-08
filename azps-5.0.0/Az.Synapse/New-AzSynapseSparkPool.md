---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199778"
---
# <span data-ttu-id="12d85-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="12d85-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="12d85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12d85-102">SYNOPSIS</span></span>
<span data-ttu-id="12d85-103">Crea un pool di scintille di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="12d85-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="12d85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12d85-104">SYNTAX</span></span>

### <span data-ttu-id="12d85-105">CreateByNameAndEnableAutoScaleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12d85-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d85-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="12d85-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d85-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="12d85-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d85-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="12d85-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12d85-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12d85-109">DESCRIPTION</span></span>
<span data-ttu-id="12d85-110">Il cmdlet **New-AzSynapseSparkPool** crea un pool di Spark di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="12d85-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="12d85-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12d85-111">EXAMPLES</span></span>

### <span data-ttu-id="12d85-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12d85-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="12d85-113">Questo comando crea un pool di Spark di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="12d85-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="12d85-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="12d85-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="12d85-115">Questo comando crea un pool di Spark di analisi di Azure sinapsi con scala automatica abilitata.</span><span class="sxs-lookup"><span data-stu-id="12d85-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="12d85-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="12d85-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="12d85-117">Questo comando crea un pool di scintille di analisi di Azure sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="12d85-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="12d85-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="12d85-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="12d85-119">Questo comando crea un pool di Spark di analisi di Azure sinapsi con scala automatica abilitata tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="12d85-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="12d85-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12d85-120">PARAMETERS</span></span>

### <span data-ttu-id="12d85-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12d85-121">-AsJob</span></span>
<span data-ttu-id="12d85-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="12d85-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12d85-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="12d85-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="12d85-124">Numero di minuti di inattività.</span><span class="sxs-lookup"><span data-stu-id="12d85-124">Number of minutes idle.</span></span> <span data-ttu-id="12d85-125">Questo parametro deve essere specificato quando è abilitata la pausa automatica.</span><span class="sxs-lookup"><span data-stu-id="12d85-125">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="12d85-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="12d85-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="12d85-127">Numero massimo di nodi da allocare nel pool di scintille specificato.</span><span class="sxs-lookup"><span data-stu-id="12d85-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="12d85-128">Questo parametro deve essere specificato quando è abilitata la scala automatica.</span><span class="sxs-lookup"><span data-stu-id="12d85-128">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="12d85-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="12d85-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="12d85-130">Numero minimo di nodi da allocare nel pool di scintille specificato.</span><span class="sxs-lookup"><span data-stu-id="12d85-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="12d85-131">Questo parametro deve essere specificato quando è abilitata la scala automatica.</span><span class="sxs-lookup"><span data-stu-id="12d85-131">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="12d85-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d85-132">-DefaultProfile</span></span>
<span data-ttu-id="12d85-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12d85-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12d85-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="12d85-134">-EnableAutoPause</span></span>
<span data-ttu-id="12d85-135">Indica se deve essere abilitata la pausa automatica.</span><span class="sxs-lookup"><span data-stu-id="12d85-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="12d85-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="12d85-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="12d85-137">File di configurazione dell'ambiente (output "Freeze PIP").</span><span class="sxs-lookup"><span data-stu-id="12d85-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="12d85-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="12d85-138">-Name</span></span>
<span data-ttu-id="12d85-139">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="12d85-139">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="12d85-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="12d85-140">-NodeCount</span></span>
<span data-ttu-id="12d85-141">Numero di nodi da allocare nel pool di scintille specificato.</span><span class="sxs-lookup"><span data-stu-id="12d85-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="12d85-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="12d85-142">-NodeSize</span></span>
<span data-ttu-id="12d85-143">Numero di core e memoria da usare per i nodi allocati nel pool di scintille specificato.</span><span class="sxs-lookup"><span data-stu-id="12d85-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="12d85-144">Questo parametro deve essere specificato quando la scala automatica è disabilitata</span><span class="sxs-lookup"><span data-stu-id="12d85-144">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="12d85-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d85-145">-ResourceGroupName</span></span>
<span data-ttu-id="12d85-146">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12d85-146">Resource group name.</span></span>

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

### <span data-ttu-id="12d85-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="12d85-147">-SparkVersion</span></span>
<span data-ttu-id="12d85-148">Versione Spark di Apache.</span><span class="sxs-lookup"><span data-stu-id="12d85-148">Apache Spark version.</span></span>
<span data-ttu-id="12d85-149">Valori consentiti: 2,4</span><span class="sxs-lookup"><span data-stu-id="12d85-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="12d85-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="12d85-150">-Tag</span></span>
<span data-ttu-id="12d85-151">Una stringa, un dizionario di stringhe di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="12d85-151">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="12d85-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="12d85-152">-WorkspaceName</span></span>
<span data-ttu-id="12d85-153">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="12d85-153">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="12d85-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="12d85-154">-WorkspaceObject</span></span>
<span data-ttu-id="12d85-155">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="12d85-155">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="12d85-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12d85-156">-Confirm</span></span>
<span data-ttu-id="12d85-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12d85-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12d85-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12d85-158">-WhatIf</span></span>
<span data-ttu-id="12d85-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12d85-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12d85-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12d85-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12d85-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d85-161">CommonParameters</span></span>
<span data-ttu-id="12d85-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d85-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d85-163">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12d85-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d85-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12d85-164">INPUTS</span></span>

### <span data-ttu-id="12d85-165">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="12d85-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="12d85-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12d85-166">OUTPUTS</span></span>

### <span data-ttu-id="12d85-167">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="12d85-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="12d85-168">Note</span><span class="sxs-lookup"><span data-stu-id="12d85-168">NOTES</span></span>

## <span data-ttu-id="12d85-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12d85-169">RELATED LINKS</span></span>
