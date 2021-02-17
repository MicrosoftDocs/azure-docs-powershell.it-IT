---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205323"
---
# <span data-ttu-id="0eb24-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="0eb24-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="0eb24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eb24-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb24-103">Recupera lo stato delle attività di preparazione e rilascio dei processi batch.</span><span class="sxs-lookup"><span data-stu-id="0eb24-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="0eb24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0eb24-104">SYNTAX</span></span>

### <span data-ttu-id="0eb24-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0eb24-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0eb24-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0eb24-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0eb24-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0eb24-107">DESCRIPTION</span></span>
<span data-ttu-id="0eb24-108">Il cmdlet **Get-AzBatchJobPreparationAndReleaseTaskStatus** ottiene il cmdlet Azure Batch job preparation and release task status for a Batch job.</span><span class="sxs-lookup"><span data-stu-id="0eb24-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="0eb24-109">È necessario specificare il *parametro Id* o un'istanza **PSCloudJob** per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb24-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="0eb24-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0eb24-110">EXAMPLES</span></span>

### <span data-ttu-id="0eb24-111">Esempio 1: Ottenere lo stato di preparazione e rilascio di un processo</span><span class="sxs-lookup"><span data-stu-id="0eb24-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="0eb24-112">Questo comando recupera lo stato delle attività di preparazione e rilascio per il processo "Test".</span><span class="sxs-lookup"><span data-stu-id="0eb24-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="0eb24-113">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="0eb24-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0eb24-114">Esempio 2: Ottenere lo stato di preparazione e rilascio di un processo con filtro e selezione specificati</span><span class="sxs-lookup"><span data-stu-id="0eb24-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="0eb24-115">Questo comando recupera lo stato delle attività di preparazione e rilascio per il processo "Test" nel nodo "tvm-2316545714_1-20170613t201733z" e usa la clausola Select per specificare di restituire solo le informazioni su JobPreparationTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="0eb24-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="0eb24-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eb24-116">PARAMETERS</span></span>

### <span data-ttu-id="0eb24-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0eb24-117">-BatchContext</span></span>
<span data-ttu-id="0eb24-118">Istanza BatchAccountContext da usare quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0eb24-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="0eb24-119">Usare il cmdlet Get-AzBatchAccountKey batch per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="0eb24-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="0eb24-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb24-120">-DefaultProfile</span></span>
<span data-ttu-id="0eb24-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb24-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eb24-122">-Expand</span><span class="sxs-lookup"><span data-stu-id="0eb24-122">-Expand</span></span>
<span data-ttu-id="0eb24-123">Specifica una clausola di espansione OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="0eb24-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="0eb24-124">Specificare un valore per questo parametro per ottenere entità associate dell'entità principale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0eb24-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="0eb24-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="0eb24-125">-Filter</span></span>
<span data-ttu-id="0eb24-126">Specifica una clausola del filtro OData.</span><span class="sxs-lookup"><span data-stu-id="0eb24-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="0eb24-127">Se non si specifica un filtro, questo cmdlet restituisce tutti gli stati delle attività di preparazione e rilascio per il processo.</span><span class="sxs-lookup"><span data-stu-id="0eb24-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="0eb24-128">-Id</span><span class="sxs-lookup"><span data-stu-id="0eb24-128">-Id</span></span>
<span data-ttu-id="0eb24-129">Specifica l'ID del processo di cui recuperare le attività di preparazione e rilascio.</span><span class="sxs-lookup"><span data-stu-id="0eb24-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="0eb24-130">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="0eb24-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="0eb24-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eb24-131">-InputObject</span></span>
<span data-ttu-id="0eb24-132">Specifica un oggetto **PSCloudJob** che rappresenta il processo da cui recuperare lo stato di preparazione e rilascio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="0eb24-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="0eb24-133">Per ottenere un **oggetto PSCloudJob,** usare il cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="0eb24-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="0eb24-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0eb24-134">-MaxCount</span></span>
<span data-ttu-id="0eb24-135">Specifica il numero massimo di processi di preparazione e stato delle attività di rilascio da restituire.</span><span class="sxs-lookup"><span data-stu-id="0eb24-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="0eb24-136">Se si specifica un valore uguale o inferiore a zero (0), il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="0eb24-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="0eb24-137">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="0eb24-137">The default value is 1000.</span></span>

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

### <span data-ttu-id="0eb24-138">-Select</span><span class="sxs-lookup"><span data-stu-id="0eb24-138">-Select</span></span>
<span data-ttu-id="0eb24-139">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="0eb24-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="0eb24-140">Specificare un valore per questo parametro per ottenere proprietà specifiche invece di tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0eb24-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="0eb24-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb24-141">CommonParameters</span></span>
<span data-ttu-id="0eb24-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb24-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb24-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0eb24-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb24-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="0eb24-144">INPUTS</span></span>

### <span data-ttu-id="0eb24-145">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="0eb24-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="0eb24-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0eb24-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0eb24-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0eb24-147">OUTPUTS</span></span>

### <span data-ttu-id="0eb24-148">Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="0eb24-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="0eb24-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="0eb24-149">NOTES</span></span>

## <span data-ttu-id="0eb24-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0eb24-150">RELATED LINKS</span></span>

[<span data-ttu-id="0eb24-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0eb24-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="0eb24-152">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="0eb24-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
