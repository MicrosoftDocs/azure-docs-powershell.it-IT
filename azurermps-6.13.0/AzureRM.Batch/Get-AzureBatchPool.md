---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 8f5a4aee0087f34769f099b6e9b44d249b53f7d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519308"
---
# <span data-ttu-id="cbb28-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cbb28-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="cbb28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cbb28-102">SYNOPSIS</span></span>
<span data-ttu-id="cbb28-103">Ottiene i pool batch sotto l'account batch specificato.</span><span class="sxs-lookup"><span data-stu-id="cbb28-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbb28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbb28-104">SYNTAX</span></span>

### <span data-ttu-id="cbb28-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cbb28-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbb28-106">ID</span><span class="sxs-lookup"><span data-stu-id="cbb28-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbb28-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbb28-107">DESCRIPTION</span></span>
<span data-ttu-id="cbb28-108">Il cmdlet **Get-AzureBatchPool** ottiene i pool di batch di Azure sotto l'account batch specificato con il parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="cbb28-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="cbb28-109">Puoi usare il parametro *ID* per ottenere un singolo pool oppure puoi usare il parametro *Filter* per ottenere i pool che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="cbb28-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="cbb28-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbb28-110">EXAMPLES</span></span>

### <span data-ttu-id="cbb28-111">Esempio 1: ottenere un pool per ID</span><span class="sxs-lookup"><span data-stu-id="cbb28-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzureBatchPool -Id "MyPool" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="cbb28-112">Questo comando consente di ottenere il pool con ID pool.</span><span class="sxs-lookup"><span data-stu-id="cbb28-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="cbb28-113">Esempio 2: ottenere tutti i pool con un filtro OData</span><span class="sxs-lookup"><span data-stu-id="cbb28-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzureBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="cbb28-114">Questo comando consente di ottenere i pool i cui ID iniziano con la mia usando il parametro *Filter* .</span><span class="sxs-lookup"><span data-stu-id="cbb28-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="cbb28-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cbb28-115">PARAMETERS</span></span>

### <span data-ttu-id="cbb28-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cbb28-116">-BatchContext</span></span>
<span data-ttu-id="cbb28-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cbb28-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cbb28-118">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="cbb28-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cbb28-119">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="cbb28-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cbb28-120">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cbb28-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cbb28-121">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cbb28-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cbb28-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbb28-122">-DefaultProfile</span></span>
<span data-ttu-id="cbb28-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cbb28-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbb28-124">-Espandi</span><span class="sxs-lookup"><span data-stu-id="cbb28-124">-Expand</span></span>
<span data-ttu-id="cbb28-125">Specifica una clausola di espansione OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="cbb28-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="cbb28-126">Specifica un valore per questo parametro per ottenere le entità associate dell'entità principale che ottieni.</span><span class="sxs-lookup"><span data-stu-id="cbb28-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="cbb28-127">-Filtro</span><span class="sxs-lookup"><span data-stu-id="cbb28-127">-Filter</span></span>
<span data-ttu-id="cbb28-128">Specifica la clausola di filtro OData da usare quando si esegue una query per i pool.</span><span class="sxs-lookup"><span data-stu-id="cbb28-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="cbb28-129">Se non specifichi un filtro, verranno restituiti tutti i pool sotto l'account batch specificato con il parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="cbb28-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="cbb28-130">-ID</span><span class="sxs-lookup"><span data-stu-id="cbb28-130">-Id</span></span>
<span data-ttu-id="cbb28-131">Specifica l'ID del pool da ottenere.</span><span class="sxs-lookup"><span data-stu-id="cbb28-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="cbb28-132">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="cbb28-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="cbb28-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="cbb28-133">-MaxCount</span></span>
<span data-ttu-id="cbb28-134">Specifica il numero massimo di pool da restituire.</span><span class="sxs-lookup"><span data-stu-id="cbb28-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="cbb28-135">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="cbb28-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="cbb28-136">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="cbb28-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="cbb28-137">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="cbb28-137">-Select</span></span>
<span data-ttu-id="cbb28-138">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="cbb28-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="cbb28-139">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cbb28-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="cbb28-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbb28-140">CommonParameters</span></span>
<span data-ttu-id="cbb28-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbb28-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbb28-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbb28-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbb28-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cbb28-143">INPUTS</span></span>

### <span data-ttu-id="cbb28-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cbb28-144">System.String</span></span>

### <span data-ttu-id="cbb28-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cbb28-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="cbb28-146">Parametri: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cbb28-146">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="cbb28-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbb28-147">OUTPUTS</span></span>

### <span data-ttu-id="cbb28-148">Microsoft.Azure.Commands.Batch. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="cbb28-148">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="cbb28-149">Note</span><span class="sxs-lookup"><span data-stu-id="cbb28-149">NOTES</span></span>

## <span data-ttu-id="cbb28-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbb28-150">RELATED LINKS</span></span>

[<span data-ttu-id="cbb28-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cbb28-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="cbb28-152">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cbb28-152">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="cbb28-153">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="cbb28-153">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="cbb28-154">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="cbb28-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


