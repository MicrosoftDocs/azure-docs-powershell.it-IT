---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195542"
---
# <span data-ttu-id="a3d82-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="a3d82-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="a3d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3d82-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d82-103">Annulla un processo spark di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a3d82-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="a3d82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3d82-104">SYNTAX</span></span>

### <span data-ttu-id="a3d82-105">StopSparkJobByIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a3d82-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d82-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3d82-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d82-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3d82-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3d82-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a3d82-108">DESCRIPTION</span></span>
<span data-ttu-id="a3d82-109">Il cmdlet **Stop-AzSynapseSparkJob** annulla un processo Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="a3d82-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="a3d82-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3d82-110">EXAMPLES</span></span>

### <span data-ttu-id="a3d82-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3d82-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="a3d82-112">Questo comando annulla un processo di Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="a3d82-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="a3d82-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a3d82-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="a3d82-114">Questo comando annulla un processo spark di Synapse Analytics tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="a3d82-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="a3d82-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a3d82-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="a3d82-116">Questo comando annulla un processo spark di Synapse Analytics tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="a3d82-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="a3d82-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3d82-117">PARAMETERS</span></span>

### <span data-ttu-id="a3d82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d82-118">-DefaultProfile</span></span>
<span data-ttu-id="a3d82-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3d82-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3d82-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a3d82-120">-Force</span></span>
<span data-ttu-id="a3d82-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a3d82-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a3d82-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="a3d82-122">-LivyId</span></span>
<span data-ttu-id="a3d82-123">Identificatore del processo Spark.</span><span class="sxs-lookup"><span data-stu-id="a3d82-123">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdParameterSet, StopSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3d82-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3d82-124">-PassThru</span></span>
<span data-ttu-id="a3d82-125">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a3d82-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="a3d82-126">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a3d82-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a3d82-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="a3d82-127">-SparkJobObject</span></span>
<span data-ttu-id="a3d82-128">Oggetto di input processo grafico spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a3d82-128">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3d82-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="a3d82-129">-SparkPoolName</span></span>
<span data-ttu-id="a3d82-130">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="a3d82-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3d82-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="a3d82-131">-SparkPoolObject</span></span>
<span data-ttu-id="a3d82-132">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a3d82-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: StopSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3d82-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a3d82-133">-WorkspaceName</span></span>
<span data-ttu-id="a3d82-134">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="a3d82-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3d82-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3d82-135">-Confirm</span></span>
<span data-ttu-id="a3d82-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3d82-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d82-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d82-137">-WhatIf</span></span>
<span data-ttu-id="a3d82-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3d82-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3d82-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3d82-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d82-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d82-140">CommonParameters</span></span>
<span data-ttu-id="a3d82-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d82-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d82-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3d82-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d82-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="a3d82-143">INPUTS</span></span>

### <span data-ttu-id="a3d82-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="a3d82-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="a3d82-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="a3d82-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="a3d82-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3d82-146">OUTPUTS</span></span>

### <span data-ttu-id="a3d82-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3d82-147">System.Boolean</span></span>

## <span data-ttu-id="a3d82-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="a3d82-148">NOTES</span></span>

## <span data-ttu-id="a3d82-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3d82-149">RELATED LINKS</span></span>
