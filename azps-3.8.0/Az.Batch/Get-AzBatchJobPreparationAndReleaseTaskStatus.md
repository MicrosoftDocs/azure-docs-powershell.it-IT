---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 2b53d9baf6461024f22cf2f44d75c071b57fb618
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030769"
---
# <span data-ttu-id="a1ab7-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="a1ab7-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="a1ab7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ab7-103">Ottiene la preparazione del processo batch e lo stato dell'attività di rilascio.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="a1ab7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1ab7-104">SYNTAX</span></span>

### <span data-ttu-id="a1ab7-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1ab7-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ab7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a1ab7-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1ab7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1ab7-107">DESCRIPTION</span></span>
<span data-ttu-id="a1ab7-108">Il cmdlet **Get-AzBatchJobPreparationAndReleaseTaskStatus** ottiene la preparazione del processo batch di Azure e lo stato dell'attività di rilascio per un processo batch.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="a1ab7-109">Devi specificare il parametro *ID* o un'istanza di **PSCloudJob** per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="a1ab7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1ab7-110">EXAMPLES</span></span>

### <span data-ttu-id="a1ab7-111">Esempio 1: ottenere la preparazione del processo e lo stato di rilascio di un processo</span><span class="sxs-lookup"><span data-stu-id="a1ab7-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="a1ab7-112">Questo comando consente di ottenere la preparazione del processo e lo stato dell'attività di rilascio per il processo "test".</span><span class="sxs-lookup"><span data-stu-id="a1ab7-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="a1ab7-113">Usa il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a1ab7-114">Esempio 2: ottenere la preparazione del processo e lo stato di rilascio di un processo con filtro e selezionare specificato</span><span class="sxs-lookup"><span data-stu-id="a1ab7-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="a1ab7-115">Questo comando ottiene lo stato dell'attività di preparazione e rilascio del processo per il processo "test" nel nodo "TVM-2316545714_1-20170613t201733z" e usa la clausola SELECT per specificare di restituire solo le informazioni di JobPreparationTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="a1ab7-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="a1ab7-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1ab7-116">PARAMETERS</span></span>

### <span data-ttu-id="a1ab7-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a1ab7-117">-BatchContext</span></span>
<span data-ttu-id="a1ab7-118">Istanza di BatchAccountContext da usare per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="a1ab7-119">Usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1ab7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ab7-120">-DefaultProfile</span></span>
<span data-ttu-id="a1ab7-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1ab7-122">-Espandi</span><span class="sxs-lookup"><span data-stu-id="a1ab7-122">-Expand</span></span>
<span data-ttu-id="a1ab7-123">Specifica una clausola di espansione OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="a1ab7-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="a1ab7-124">Specifica un valore per questo parametro per ottenere le entità associate dell'entità principale che ottieni.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="a1ab7-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a1ab7-125">-Filter</span></span>
<span data-ttu-id="a1ab7-126">Specifica una clausola di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="a1ab7-127">Se non specifichi un filtro, questo cmdlet restituisce tutti i processi di preparazione e rilascio dell'attività per il processo.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="a1ab7-128">-ID</span><span class="sxs-lookup"><span data-stu-id="a1ab7-128">-Id</span></span>
<span data-ttu-id="a1ab7-129">Specifica l'ID del processo di cui devono essere recuperate le attività di preparazione e rilascio.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="a1ab7-130">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1ab7-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1ab7-131">-InputObject</span></span>
<span data-ttu-id="a1ab7-132">Specifica un oggetto **PSCloudJob** che rappresenta il processo per ottenere la preparazione e il rilascio dello stato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="a1ab7-133">Per ottenere un oggetto **PSCloudJob** , usa il cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1ab7-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a1ab7-134">-MaxCount</span></span>
<span data-ttu-id="a1ab7-135">Specifica il numero massimo di operazioni di preparazione e rilascio dello stato dell'attività da restituire.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="a1ab7-136">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="a1ab7-137">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-137">The default value is 1000.</span></span>

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

### <span data-ttu-id="a1ab7-138">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="a1ab7-138">-Select</span></span>
<span data-ttu-id="a1ab7-139">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="a1ab7-140">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="a1ab7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ab7-141">CommonParameters</span></span>
<span data-ttu-id="a1ab7-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1ab7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ab7-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1ab7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ab7-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1ab7-144">INPUTS</span></span>

### <span data-ttu-id="a1ab7-145">Microsoft.Azure.Commands.Batch. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="a1ab7-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="a1ab7-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a1ab7-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a1ab7-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1ab7-147">OUTPUTS</span></span>

### <span data-ttu-id="a1ab7-148">Microsoft.Azure.Commands.Batch. Models. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="a1ab7-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="a1ab7-149">Note</span><span class="sxs-lookup"><span data-stu-id="a1ab7-149">NOTES</span></span>

## <span data-ttu-id="a1ab7-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1ab7-150">RELATED LINKS</span></span>

[<span data-ttu-id="a1ab7-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a1ab7-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="a1ab7-152">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="a1ab7-152">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
