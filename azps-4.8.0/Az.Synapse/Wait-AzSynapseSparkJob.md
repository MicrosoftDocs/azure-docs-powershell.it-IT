---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191412"
---
# <span data-ttu-id="23c96-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="23c96-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="23c96-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23c96-102">SYNOPSIS</span></span>
<span data-ttu-id="23c96-103">Attende il completamento di un processo di scintilla di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="23c96-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="23c96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23c96-104">SYNTAX</span></span>

### <span data-ttu-id="23c96-105">WaitSparkJobByIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23c96-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23c96-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23c96-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23c96-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23c96-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23c96-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23c96-108">DESCRIPTION</span></span>
<span data-ttu-id="23c96-109">Il cmdlet **wait-AzSynapseSparkJob** attende il completamento di un processo di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c96-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="23c96-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23c96-110">EXAMPLES</span></span>

### <span data-ttu-id="23c96-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23c96-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="23c96-112">Questo comando attende il completamento del processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="23c96-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="23c96-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23c96-113">PARAMETERS</span></span>

### <span data-ttu-id="23c96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c96-114">-DefaultProfile</span></span>
<span data-ttu-id="23c96-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23c96-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23c96-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="23c96-116">-LivyId</span></span>
<span data-ttu-id="23c96-117">Identificatore del processo Spark.</span><span class="sxs-lookup"><span data-stu-id="23c96-117">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="23c96-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="23c96-118">-SparkJobObject</span></span>
<span data-ttu-id="23c96-119">Oggetto di input processo Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="23c96-119">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="23c96-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="23c96-120">-SparkPoolName</span></span>
<span data-ttu-id="23c96-121">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="23c96-121">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="23c96-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="23c96-122">-SparkPoolObject</span></span>
<span data-ttu-id="23c96-123">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="23c96-123">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="23c96-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="23c96-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="23c96-125">Intervallo di tempo massimo per l'attesa prima che venga visualizzato un errore. Il valore predefinito è mai timeout.</span><span class="sxs-lookup"><span data-stu-id="23c96-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

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

### <span data-ttu-id="23c96-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="23c96-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="23c96-127">L'intervallo di polling tra i controlli per lo stato del processo, in secondi.</span><span class="sxs-lookup"><span data-stu-id="23c96-127">The polling interval between checks for the job status, in seconds.</span></span>

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

### <span data-ttu-id="23c96-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="23c96-128">-WorkspaceName</span></span>
<span data-ttu-id="23c96-129">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="23c96-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="23c96-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c96-130">CommonParameters</span></span>
<span data-ttu-id="23c96-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23c96-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c96-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23c96-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c96-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23c96-133">INPUTS</span></span>

### <span data-ttu-id="23c96-134">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="23c96-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="23c96-135">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="23c96-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="23c96-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23c96-136">OUTPUTS</span></span>

### <span data-ttu-id="23c96-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23c96-137">System.Boolean</span></span>

## <span data-ttu-id="23c96-138">Note</span><span class="sxs-lookup"><span data-stu-id="23c96-138">NOTES</span></span>

## <span data-ttu-id="23c96-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23c96-139">RELATED LINKS</span></span>
