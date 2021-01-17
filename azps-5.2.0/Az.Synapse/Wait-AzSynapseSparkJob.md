---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372679"
---
# <span data-ttu-id="01242-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="01242-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="01242-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01242-102">SYNOPSIS</span></span>
<span data-ttu-id="01242-103">Attende il completamento di un processo di scintilla di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="01242-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="01242-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01242-104">SYNTAX</span></span>

### <span data-ttu-id="01242-105">WaitSparkJobByIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="01242-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01242-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01242-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01242-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01242-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01242-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01242-108">DESCRIPTION</span></span>
<span data-ttu-id="01242-109">Il cmdlet **wait-AzSynapseSparkJob** attende il completamento di un processo di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="01242-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="01242-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01242-110">EXAMPLES</span></span>

### <span data-ttu-id="01242-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="01242-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="01242-112">Questo comando attende il completamento del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="01242-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="01242-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01242-113">PARAMETERS</span></span>

### <span data-ttu-id="01242-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01242-114">-DefaultProfile</span></span>
<span data-ttu-id="01242-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01242-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01242-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="01242-116">-LivyId</span></span>
<span data-ttu-id="01242-117">Identificatore del processo Spark.</span><span class="sxs-lookup"><span data-stu-id="01242-117">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="01242-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="01242-118">-SparkJobObject</span></span>
<span data-ttu-id="01242-119">Oggetto di input processo Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="01242-119">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="01242-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="01242-120">-SparkPoolName</span></span>
<span data-ttu-id="01242-121">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="01242-121">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="01242-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="01242-122">-SparkPoolObject</span></span>
<span data-ttu-id="01242-123">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="01242-123">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="01242-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="01242-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="01242-125">Intervallo di tempo massimo per l'attesa prima che venga visualizzato un errore. Il valore predefinito è mai timeout.</span><span class="sxs-lookup"><span data-stu-id="01242-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="01242-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="01242-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="01242-127">L'intervallo di polling tra i controlli per lo stato del processo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="01242-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="01242-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="01242-128">-WorkspaceName</span></span>
<span data-ttu-id="01242-129">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="01242-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="01242-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01242-130">CommonParameters</span></span>
<span data-ttu-id="01242-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01242-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01242-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01242-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01242-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01242-133">INPUTS</span></span>

### <span data-ttu-id="01242-134">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="01242-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="01242-135">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="01242-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="01242-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01242-136">OUTPUTS</span></span>

### <span data-ttu-id="01242-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01242-137">System.Boolean</span></span>

## <span data-ttu-id="01242-138">Note</span><span class="sxs-lookup"><span data-stu-id="01242-138">NOTES</span></span>

## <span data-ttu-id="01242-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01242-139">RELATED LINKS</span></span>
