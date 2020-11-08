---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193701"
---
# <span data-ttu-id="3a203-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="3a203-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="3a203-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a203-102">SYNOPSIS</span></span>
<span data-ttu-id="3a203-103">Annulla un processo Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3a203-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="3a203-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a203-104">SYNTAX</span></span>

### <span data-ttu-id="3a203-105">StopSparkJobByIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3a203-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a203-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a203-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a203-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a203-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a203-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a203-108">DESCRIPTION</span></span>
<span data-ttu-id="3a203-109">Il cmdlet **Stop-AzSynapseSparkJob** Annulla un processo Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3a203-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="3a203-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a203-110">EXAMPLES</span></span>

### <span data-ttu-id="3a203-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a203-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="3a203-112">Questo comando Annulla un processo Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3a203-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="3a203-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3a203-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="3a203-114">Questo comando Annulla un processo Spark analisi sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="3a203-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="3a203-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3a203-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="3a203-116">Questo comando Annulla un processo Spark analisi sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="3a203-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="3a203-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a203-117">PARAMETERS</span></span>

### <span data-ttu-id="3a203-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a203-118">-DefaultProfile</span></span>
<span data-ttu-id="3a203-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a203-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a203-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3a203-120">-Force</span></span>
<span data-ttu-id="3a203-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3a203-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3a203-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="3a203-122">-LivyId</span></span>
<span data-ttu-id="3a203-123">Identificatore del processo Spark.</span><span class="sxs-lookup"><span data-stu-id="3a203-123">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="3a203-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a203-124">-PassThru</span></span>
<span data-ttu-id="3a203-125">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3a203-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="3a203-126">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="3a203-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3a203-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="3a203-127">-SparkJobObject</span></span>
<span data-ttu-id="3a203-128">Oggetto di input processo Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="3a203-128">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3a203-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="3a203-129">-SparkPoolName</span></span>
<span data-ttu-id="3a203-130">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3a203-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="3a203-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="3a203-131">-SparkPoolObject</span></span>
<span data-ttu-id="3a203-132">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="3a203-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3a203-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a203-133">-WorkspaceName</span></span>
<span data-ttu-id="3a203-134">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3a203-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3a203-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3a203-135">-Confirm</span></span>
<span data-ttu-id="3a203-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a203-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a203-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a203-137">-WhatIf</span></span>
<span data-ttu-id="3a203-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a203-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a203-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a203-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a203-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a203-140">CommonParameters</span></span>
<span data-ttu-id="3a203-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a203-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a203-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a203-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a203-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a203-143">INPUTS</span></span>

### <span data-ttu-id="3a203-144">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="3a203-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="3a203-145">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="3a203-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="3a203-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a203-146">OUTPUTS</span></span>

### <span data-ttu-id="3a203-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a203-147">System.Boolean</span></span>

## <span data-ttu-id="3a203-148">Note</span><span class="sxs-lookup"><span data-stu-id="3a203-148">NOTES</span></span>

## <span data-ttu-id="3a203-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a203-149">RELATED LINKS</span></span>
