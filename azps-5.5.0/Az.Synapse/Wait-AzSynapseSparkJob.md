---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182623"
---
# <span data-ttu-id="6a129-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="6a129-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="6a129-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a129-102">SYNOPSIS</span></span>
<span data-ttu-id="6a129-103">Attende il completamento di un processo spark di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="6a129-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="6a129-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a129-104">SYNTAX</span></span>

### <span data-ttu-id="6a129-105">WaitSparkJobByIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a129-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a129-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a129-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a129-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a129-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a129-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6a129-108">DESCRIPTION</span></span>
<span data-ttu-id="6a129-109">Il cmdlet **Wait-AzSynapseSparkJob** attende il completamento di un processo di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="6a129-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="6a129-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a129-110">EXAMPLES</span></span>

### <span data-ttu-id="6a129-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a129-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="6a129-112">Questo comando attende il completamento del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="6a129-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="6a129-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a129-113">PARAMETERS</span></span>

### <span data-ttu-id="6a129-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a129-114">-DefaultProfile</span></span>
<span data-ttu-id="6a129-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a129-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a129-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="6a129-116">-LivyId</span></span>
<span data-ttu-id="6a129-117">Identificatore del processo Spark.</span><span class="sxs-lookup"><span data-stu-id="6a129-117">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdParameterSet, WaitSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a129-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="6a129-118">-SparkJobObject</span></span>
<span data-ttu-id="6a129-119">Oggetto di input processo grafico spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a129-119">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a129-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="6a129-120">-SparkPoolName</span></span>
<span data-ttu-id="6a129-121">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="6a129-121">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a129-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="6a129-122">-SparkPoolObject</span></span>
<span data-ttu-id="6a129-123">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a129-123">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: WaitSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a129-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="6a129-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="6a129-125">La quantità massima di tempo di attesa prima dell'errore. Per impostazione predefinita, il timeout non viene mai impostato.</span><span class="sxs-lookup"><span data-stu-id="6a129-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="6a129-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6a129-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="6a129-127">L'intervallo di polling tra i controlli dello stato del processo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="6a129-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="6a129-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6a129-128">-WorkspaceName</span></span>
<span data-ttu-id="6a129-129">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="6a129-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a129-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a129-130">CommonParameters</span></span>
<span data-ttu-id="6a129-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a129-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a129-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a129-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a129-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="6a129-133">INPUTS</span></span>

### <span data-ttu-id="6a129-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="6a129-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="6a129-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="6a129-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="6a129-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a129-136">OUTPUTS</span></span>

### <span data-ttu-id="6a129-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a129-137">System.Boolean</span></span>

## <span data-ttu-id="6a129-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="6a129-138">NOTES</span></span>

## <span data-ttu-id="6a129-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a129-139">RELATED LINKS</span></span>
