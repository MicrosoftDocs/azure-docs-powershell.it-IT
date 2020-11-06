---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobSchedule.md
ms.openlocfilehash: c8b51f3822ce52fd21aa1d2b8df45d11108d713a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513936"
---
# <span data-ttu-id="a6216-101">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a6216-101">Get-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="a6216-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6216-102">SYNOPSIS</span></span>
<span data-ttu-id="a6216-103">Ottiene le pianificazioni dei processi batch.</span><span class="sxs-lookup"><span data-stu-id="a6216-103">Gets Batch job schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6216-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6216-104">SYNTAX</span></span>

### <span data-ttu-id="a6216-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6216-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6216-106">ID</span><span class="sxs-lookup"><span data-stu-id="a6216-106">Id</span></span>
```
Get-AzureBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6216-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6216-107">DESCRIPTION</span></span>
<span data-ttu-id="a6216-108">Il cmdlet **Get-AzureBatchJobSchedule** ottiene le pianificazioni dei processi batch di Azure per l'account batch specificato dal parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="a6216-108">The **Get-AzureBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="a6216-109">Specificare un ID per ottenere una singola pianificazione del processo.</span><span class="sxs-lookup"><span data-stu-id="a6216-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="a6216-110">Specifica il parametro *Filter* per ottenere le pianificazioni dei processi che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="a6216-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="a6216-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6216-111">EXAMPLES</span></span>

### <span data-ttu-id="a6216-112">Esempio 1: ottenere una pianificazione del processo specificando un ID</span><span class="sxs-lookup"><span data-stu-id="a6216-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

<span data-ttu-id="a6216-113">Questo comando consente di ottenere la pianificazione del processo con ID JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="a6216-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="a6216-114">Usa il cmdlet Get-AzureRmBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="a6216-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a6216-115">Esempio 2: ottenere le pianificazioni dei processi usando un filtro</span><span class="sxs-lookup"><span data-stu-id="a6216-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 : 
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

<span data-ttu-id="a6216-116">Questo comando consente di ottenere tutte le pianificazioni dei processi con ID che iniziano con Job specificando il parametro *Filter* .</span><span class="sxs-lookup"><span data-stu-id="a6216-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="a6216-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6216-117">PARAMETERS</span></span>

### <span data-ttu-id="a6216-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a6216-118">-BatchContext</span></span>
<span data-ttu-id="a6216-119">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a6216-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a6216-120">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a6216-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a6216-121">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="a6216-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a6216-122">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a6216-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a6216-123">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a6216-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a6216-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6216-124">-DefaultProfile</span></span>
<span data-ttu-id="a6216-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6216-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6216-126">-Espandi</span><span class="sxs-lookup"><span data-stu-id="a6216-126">-Expand</span></span>
<span data-ttu-id="a6216-127">Specifica una clausola di espansione OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="a6216-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="a6216-128">Specifica un valore per questo parametro per ottenere le entità associate dell'entità principale che ottieni.</span><span class="sxs-lookup"><span data-stu-id="a6216-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="a6216-129">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a6216-129">-Filter</span></span>
<span data-ttu-id="a6216-130">Specifica una clausola di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="a6216-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="a6216-131">Questo cmdlet restituisce le pianificazioni dei processi che corrispondono al filtro specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a6216-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="a6216-132">Se non specifichi un filtro, questo cmdlet restituisce tutte le pianificazioni dei processi per il contesto batch.</span><span class="sxs-lookup"><span data-stu-id="a6216-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6216-133">-ID</span><span class="sxs-lookup"><span data-stu-id="a6216-133">-Id</span></span>
<span data-ttu-id="a6216-134">Specifica l'ID della pianificazione del processo ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6216-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="a6216-135">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="a6216-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6216-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a6216-136">-MaxCount</span></span>
<span data-ttu-id="a6216-137">Specifica il numero massimo di pianificazioni di lavoro da restituire.</span><span class="sxs-lookup"><span data-stu-id="a6216-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="a6216-138">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="a6216-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="a6216-139">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="a6216-139">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6216-140">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="a6216-140">-Select</span></span>
<span data-ttu-id="a6216-141">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="a6216-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="a6216-142">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a6216-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="a6216-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6216-143">CommonParameters</span></span>
<span data-ttu-id="a6216-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6216-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6216-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6216-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6216-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6216-146">INPUTS</span></span>

### <span data-ttu-id="a6216-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a6216-147">System.String</span></span>

### <span data-ttu-id="a6216-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a6216-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a6216-149">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a6216-149">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a6216-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6216-150">OUTPUTS</span></span>

### <span data-ttu-id="a6216-151">Microsoft.Azure.Commands.Batch. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a6216-151">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="a6216-152">Note</span><span class="sxs-lookup"><span data-stu-id="a6216-152">NOTES</span></span>

## <span data-ttu-id="a6216-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6216-153">RELATED LINKS</span></span>

[<span data-ttu-id="a6216-154">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a6216-154">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="a6216-155">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a6216-155">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="a6216-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a6216-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a6216-157">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a6216-157">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="a6216-158">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a6216-158">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="a6216-159">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a6216-159">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="a6216-160">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="a6216-160">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


