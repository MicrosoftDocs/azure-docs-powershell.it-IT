---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: 5f24e55042a8be7f36b1a9946c4bd5b87209a0f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520471"
---
# <span data-ttu-id="ff812-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="ff812-101">Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="ff812-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff812-102">SYNOPSIS</span></span>
<span data-ttu-id="ff812-103">Ottiene la preparazione del processo batch e lo stato dell'attività di rilascio.</span><span class="sxs-lookup"><span data-stu-id="ff812-103">Gets Batch job preparation and release task status.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff812-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff812-104">SYNTAX</span></span>

### <span data-ttu-id="ff812-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff812-105">Id (Default)</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff812-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ff812-106">InputObject</span></span>
```
Get-AzureBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff812-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff812-107">DESCRIPTION</span></span>
<span data-ttu-id="ff812-108">Il cmdlet **Get-AzureBatchJobPreparationAndReleaseTaskStatus** ottiene la preparazione del processo batch di Azure e lo stato dell'attività di rilascio per un processo batch.</span><span class="sxs-lookup"><span data-stu-id="ff812-108">The **Get-AzureBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="ff812-109">Devi specificare il parametro *ID* o un'istanza di **PSCloudJob** per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff812-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="ff812-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff812-110">EXAMPLES</span></span>

### <span data-ttu-id="ff812-111">Esempio 1: ottenere la preparazione del processo e lo stato di rilascio di un processo</span><span class="sxs-lookup"><span data-stu-id="ff812-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="ff812-112">Questo comando consente di ottenere la preparazione del processo e lo stato dell'attività di rilascio per il processo "test".</span><span class="sxs-lookup"><span data-stu-id="ff812-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="ff812-113">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="ff812-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ff812-114">Esempio 2: ottenere la preparazione del processo e lo stato di rilascio di un processo con filtro e selezionare specificato</span><span class="sxs-lookup"><span data-stu-id="ff812-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzureBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="ff812-115">Questo comando ottiene lo stato dell'attività di preparazione e rilascio del processo per il processo "test" nel nodo "TVM-2316545714_1-20170613t201733z" e usa la clausola SELECT per specificare di restituire solo le informazioni di JobPreparationTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="ff812-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="ff812-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff812-116">PARAMETERS</span></span>

### <span data-ttu-id="ff812-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ff812-117">-BatchContext</span></span>
<span data-ttu-id="ff812-118">Istanza di BatchAccountContext da usare per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="ff812-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="ff812-119">Usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="ff812-119">Use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff812-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff812-120">-DefaultProfile</span></span>
<span data-ttu-id="ff812-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff812-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff812-122">-Espandi</span><span class="sxs-lookup"><span data-stu-id="ff812-122">-Expand</span></span>
<span data-ttu-id="ff812-123">Specifica una clausola di espansione OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="ff812-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="ff812-124">Specifica un valore per questo parametro per ottenere le entità associate dell'entità principale che ottieni.</span><span class="sxs-lookup"><span data-stu-id="ff812-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff812-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="ff812-125">-Filter</span></span>
<span data-ttu-id="ff812-126">Specifica una clausola di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="ff812-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="ff812-127">Se non specifichi un filtro, questo cmdlet restituisce tutti i processi di preparazione e rilascio dell'attività per il processo.</span><span class="sxs-lookup"><span data-stu-id="ff812-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff812-128">-ID</span><span class="sxs-lookup"><span data-stu-id="ff812-128">-Id</span></span>
<span data-ttu-id="ff812-129">Specifica l'ID del processo di cui devono essere recuperate le attività di preparazione e rilascio.</span><span class="sxs-lookup"><span data-stu-id="ff812-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="ff812-130">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="ff812-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff812-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff812-131">-InputObject</span></span>
<span data-ttu-id="ff812-132">Specifica un oggetto **PSCloudJob** che rappresenta il processo per ottenere la preparazione e il rilascio dello stato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="ff812-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="ff812-133">Per ottenere un oggetto **PSCloudJob** , usa il cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="ff812-133">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: PSCloudJob
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff812-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ff812-134">-MaxCount</span></span>
<span data-ttu-id="ff812-135">Specifica il numero massimo di operazioni di preparazione e rilascio dello stato dell'attività da restituire.</span><span class="sxs-lookup"><span data-stu-id="ff812-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="ff812-136">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="ff812-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ff812-137">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="ff812-137">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff812-138">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="ff812-138">-Select</span></span>
<span data-ttu-id="ff812-139">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="ff812-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="ff812-140">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ff812-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff812-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff812-141">CommonParameters</span></span>
<span data-ttu-id="ff812-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff812-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff812-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff812-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff812-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff812-144">INPUTS</span></span>

### <span data-ttu-id="ff812-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ff812-145">System.String</span></span>
<span data-ttu-id="ff812-146">Microsoft.Azure.Commands.Batch. Models. PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ff812-146">Microsoft.Azure.Commands.Batch.Models.PSCloudJob Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ff812-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff812-147">OUTPUTS</span></span>

### <span data-ttu-id="ff812-148">Microsoft.Azure.Commands.Batch. Models. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="ff812-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="ff812-149">Note</span><span class="sxs-lookup"><span data-stu-id="ff812-149">NOTES</span></span>

## <span data-ttu-id="ff812-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff812-150">RELATED LINKS</span></span>

[<span data-ttu-id="ff812-151">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ff812-151">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="ff812-152">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="ff812-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)