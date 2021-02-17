---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: 9daa0e1a1b1bc6ec980f3c3f65d79840648fdaf8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205306"
---
# <span data-ttu-id="f9399-101">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f9399-101">Get-AzBatchJobSchedule</span></span>

## <span data-ttu-id="f9399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9399-102">SYNOPSIS</span></span>
<span data-ttu-id="f9399-103">Recupera le pianificazioni dei processi batch.</span><span class="sxs-lookup"><span data-stu-id="f9399-103">Gets Batch job schedules.</span></span>

## <span data-ttu-id="f9399-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9399-104">SYNTAX</span></span>

### <span data-ttu-id="f9399-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9399-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9399-106">ID</span><span class="sxs-lookup"><span data-stu-id="f9399-106">Id</span></span>
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9399-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f9399-107">DESCRIPTION</span></span>
<span data-ttu-id="f9399-108">Il cmdlet **Get-AzBatchJobSchedule** ottiene le pianificazioni dei processi batch di Azure per l'account batch specificato dal *parametro BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="f9399-108">The **Get-AzBatchJobSchedule** cmdlet gets Azure Batch job schedules for the Batch account specified by the *BatchContext* parameter.</span></span>
<span data-ttu-id="f9399-109">Specificare un ID per ottenere una pianificazione per un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="f9399-109">Specify an ID to get a single job schedule.</span></span>
<span data-ttu-id="f9399-110">Specificare il *parametro Filter* per ottenere le pianificazioni dei processi corrispondenti a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="f9399-110">Specify the *Filter* parameter to get the job schedules that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="f9399-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9399-111">EXAMPLES</span></span>

### <span data-ttu-id="f9399-112">Esempio 1: Ottenere la pianificazione di un processo specificando un ID</span><span class="sxs-lookup"><span data-stu-id="f9399-112">Example 1: Get a job schedule by specifying an ID</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
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

<span data-ttu-id="f9399-113">Questo comando recupera la pianificazione del processo con l'ID JobSchedule23.</span><span class="sxs-lookup"><span data-stu-id="f9399-113">This command gets the job schedule that has the ID JobSchedule23.</span></span>
<span data-ttu-id="f9399-114">Usare il cmdlet Get-AzBatchAccountKey per assegnare un contesto alla $Context variabile.</span><span class="sxs-lookup"><span data-stu-id="f9399-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f9399-115">Esempio 2: Ottenere le pianificazioni dei processi con un filtro</span><span class="sxs-lookup"><span data-stu-id="f9399-115">Example 2: Get job schedules by using a filter</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
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

<span data-ttu-id="f9399-116">Questo comando recupera tutte le pianificazioni di processo che hanno ID che iniziano con Job specificando il *parametro Filter.*</span><span class="sxs-lookup"><span data-stu-id="f9399-116">This command gets all job schedules that have IDs that start with Job by specifying the *Filter* parameter.</span></span>

## <span data-ttu-id="f9399-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9399-117">PARAMETERS</span></span>

### <span data-ttu-id="f9399-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f9399-118">-BatchContext</span></span>
<span data-ttu-id="f9399-119">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f9399-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f9399-120">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="f9399-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f9399-121">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="f9399-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f9399-122">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="f9399-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f9399-123">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f9399-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f9399-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9399-124">-DefaultProfile</span></span>
<span data-ttu-id="f9399-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9399-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9399-126">-Expand</span><span class="sxs-lookup"><span data-stu-id="f9399-126">-Expand</span></span>
<span data-ttu-id="f9399-127">Specifica una clausola di espansione OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="f9399-127">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="f9399-128">Specificare un valore per questo parametro per ottenere entità associate dell'entità principale da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f9399-128">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="f9399-129">-Filter</span><span class="sxs-lookup"><span data-stu-id="f9399-129">-Filter</span></span>
<span data-ttu-id="f9399-130">Specifica una clausola del filtro OData.</span><span class="sxs-lookup"><span data-stu-id="f9399-130">Specifies an OData filter clause.</span></span>
<span data-ttu-id="f9399-131">Questo cmdlet restituisce le pianificazioni dei processi che corrispondono al filtro specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f9399-131">This cmdlet returns job schedules that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="f9399-132">Se non si specifica un filtro, questo cmdlet restituisce tutte le pianificazioni dei processi per il contesto Batch.</span><span class="sxs-lookup"><span data-stu-id="f9399-132">If you do not specify a filter, this cmdlet returns all job schedules for the Batch context.</span></span>

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

### <span data-ttu-id="f9399-133">-Id</span><span class="sxs-lookup"><span data-stu-id="f9399-133">-Id</span></span>
<span data-ttu-id="f9399-134">Specifica l'ID della pianificazione del processo che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9399-134">Specifies the ID of the job schedule that this cmdlet gets.</span></span>
<span data-ttu-id="f9399-135">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="f9399-135">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="f9399-136">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f9399-136">-MaxCount</span></span>
<span data-ttu-id="f9399-137">Specifica il numero massimo di pianificazioni di processi da restituire.</span><span class="sxs-lookup"><span data-stu-id="f9399-137">Specifies the maximum number of job schedules to return.</span></span>
<span data-ttu-id="f9399-138">Se si specifica un valore uguale o inferiore a zero (0), il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="f9399-138">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="f9399-139">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="f9399-139">The default value is 1000.</span></span>

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

### <span data-ttu-id="f9399-140">-Select</span><span class="sxs-lookup"><span data-stu-id="f9399-140">-Select</span></span>
<span data-ttu-id="f9399-141">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="f9399-141">Specifies an OData select clause.</span></span>
<span data-ttu-id="f9399-142">Specificare un valore per questo parametro per ottenere proprietà specifiche invece di tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f9399-142">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="f9399-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9399-143">CommonParameters</span></span>
<span data-ttu-id="f9399-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9399-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9399-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9399-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9399-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="f9399-146">INPUTS</span></span>

### <span data-ttu-id="f9399-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f9399-147">System.String</span></span>

### <span data-ttu-id="f9399-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f9399-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f9399-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9399-149">OUTPUTS</span></span>

### <span data-ttu-id="f9399-150">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f9399-150">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

## <span data-ttu-id="f9399-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="f9399-151">NOTES</span></span>

## <span data-ttu-id="f9399-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9399-152">RELATED LINKS</span></span>

[<span data-ttu-id="f9399-153">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f9399-153">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="f9399-154">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f9399-154">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="f9399-155">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f9399-155">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f9399-156">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f9399-156">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="f9399-157">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f9399-157">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="f9399-158">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f9399-158">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="f9399-159">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="f9399-159">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
