---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 2bd84d8e5d0f48c5b9a3af65944ece99369270c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510148"
---
# <span data-ttu-id="a9ab7-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="a9ab7-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="a9ab7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ab7-103">Ottiene i pool batch sotto l'account batch specificato.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9ab7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9ab7-104">SYNTAX</span></span>

### <span data-ttu-id="a9ab7-105">ODataFilter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9ab7-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9ab7-106">ID</span><span class="sxs-lookup"><span data-stu-id="a9ab7-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9ab7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9ab7-107">DESCRIPTION</span></span>
<span data-ttu-id="a9ab7-108">Il cmdlet **Get-AzureBatchPool** ottiene i pool di batch di Azure sotto l'account batch specificato con il parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="a9ab7-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="a9ab7-109">Puoi usare il parametro *ID* per ottenere un singolo pool oppure puoi usare il parametro *Filter* per ottenere i pool che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="a9ab7-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="a9ab7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9ab7-110">EXAMPLES</span></span>

### <span data-ttu-id="a9ab7-111">Esempio 1: ottenere un pool per ID</span><span class="sxs-lookup"><span data-stu-id="a9ab7-111">Example 1: Get a pool by ID</span></span>
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

<span data-ttu-id="a9ab7-112">Questo comando consente di ottenere il pool con ID pool.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="a9ab7-113">Esempio 2: ottenere tutti i pool con un filtro OData</span><span class="sxs-lookup"><span data-stu-id="a9ab7-113">Example 2: Get all pools using an OData filter</span></span>
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

<span data-ttu-id="a9ab7-114">Questo comando consente di ottenere i pool i cui ID iniziano con la mia usando il parametro *Filter* .</span><span class="sxs-lookup"><span data-stu-id="a9ab7-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="a9ab7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9ab7-115">PARAMETERS</span></span>

### <span data-ttu-id="a9ab7-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a9ab7-116">-BatchContext</span></span>
<span data-ttu-id="a9ab7-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a9ab7-118">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a9ab7-119">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a9ab7-120">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a9ab7-121">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a9ab7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ab7-122">-DefaultProfile</span></span>
<span data-ttu-id="a9ab7-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9ab7-124">-Espandi</span><span class="sxs-lookup"><span data-stu-id="a9ab7-124">-Expand</span></span>
<span data-ttu-id="a9ab7-125">Specifica una clausola di espansione OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="a9ab7-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="a9ab7-126">Specifica un valore per questo parametro per ottenere le entità associate dell'entità principale che ottieni.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="a9ab7-127">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a9ab7-127">-Filter</span></span>
<span data-ttu-id="a9ab7-128">Specifica la clausola di filtro OData da usare quando si esegue una query per i pool.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="a9ab7-129">Se non specifichi un filtro, verranno restituiti tutti i pool sotto l'account batch specificato con il parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="a9ab7-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ab7-130">-ID</span><span class="sxs-lookup"><span data-stu-id="a9ab7-130">-Id</span></span>
<span data-ttu-id="a9ab7-131">Specifica l'ID del pool da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="a9ab7-132">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-132">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ab7-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a9ab7-133">-MaxCount</span></span>
<span data-ttu-id="a9ab7-134">Specifica il numero massimo di pool da restituire.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="a9ab7-135">Se specifichi un valore pari a zero (0) o meno, il cmdlet non usa un limite superiore.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="a9ab7-136">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-136">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ab7-137">-Selezionare</span><span class="sxs-lookup"><span data-stu-id="a9ab7-137">-Select</span></span>
<span data-ttu-id="a9ab7-138">Specifica una clausola di selezione OData.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="a9ab7-139">Specifica un valore per questo parametro per ottenere proprietà specifiche anziché tutte le proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="a9ab7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ab7-140">CommonParameters</span></span>
<span data-ttu-id="a9ab7-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ab7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ab7-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9ab7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ab7-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9ab7-143">INPUTS</span></span>

### <span data-ttu-id="a9ab7-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a9ab7-144">BatchAccountContext</span></span>
<span data-ttu-id="a9ab7-145">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a9ab7-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a9ab7-146">Stringa</span><span class="sxs-lookup"><span data-stu-id="a9ab7-146">String</span></span>
<span data-ttu-id="a9ab7-147">Il parametro "ID" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a9ab7-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a9ab7-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9ab7-148">OUTPUTS</span></span>

### <span data-ttu-id="a9ab7-149">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="a9ab7-149">PSCloudPool</span></span>

## <span data-ttu-id="a9ab7-150">Note</span><span class="sxs-lookup"><span data-stu-id="a9ab7-150">NOTES</span></span>

## <span data-ttu-id="a9ab7-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9ab7-151">RELATED LINKS</span></span>

[<span data-ttu-id="a9ab7-152">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a9ab7-152">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a9ab7-153">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="a9ab7-153">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="a9ab7-154">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="a9ab7-154">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="a9ab7-155">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="a9ab7-155">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


