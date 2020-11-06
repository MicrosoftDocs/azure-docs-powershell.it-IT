---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
ms.openlocfilehash: 4f985859cb26372a6ffc68b8521d08033fdc6670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521995"
---
# <span data-ttu-id="7e97c-101">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="7e97c-101">Get-AzureBatchPoolUsageMetrics</span></span>

## <span data-ttu-id="7e97c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e97c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e97c-103">Ottiene le metriche per l'utilizzo del pool per un account batch.</span><span class="sxs-lookup"><span data-stu-id="7e97c-103">Gets pool usage metrics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e97c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e97c-104">SYNTAX</span></span>

```
Get-AzureBatchPoolUsageMetrics [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e97c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e97c-105">DESCRIPTION</span></span>
<span data-ttu-id="7e97c-106">Il cmdlet **Get-AzureBatchPoolUsageMetrics** ottiene le metriche di utilizzo, aggregate in base al pool tra intervalli di tempo individuali, per l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="7e97c-106">The **Get-AzureBatchPoolUsageMetrics** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="7e97c-107">Puoi ottenere le statistiche per un pool specifico e per un intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="7e97c-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="7e97c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e97c-108">EXAMPLES</span></span>

### <span data-ttu-id="7e97c-109">Esempio 1: ottenere le metriche per l'utilizzo del pool per un intervallo di tempo</span><span class="sxs-lookup"><span data-stu-id="7e97c-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzureBatchPoolUsageMetrics -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

<span data-ttu-id="7e97c-110">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="7e97c-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="7e97c-111">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="7e97c-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="7e97c-112">I due comandi successivi creano oggetti **DateTime** usando il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="7e97c-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="7e97c-113">I comandi archiviano questi valori nelle variabili $StartTime e $EndTime per l'utilizzo con il comando finale.</span><span class="sxs-lookup"><span data-stu-id="7e97c-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>

<span data-ttu-id="7e97c-114">Il comando finale restituisce tutte le metriche di utilizzo del pool, aggregate in base al pool, nell'intervallo di tempo compreso tra gli orari di inizio e di fine specificati.</span><span class="sxs-lookup"><span data-stu-id="7e97c-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="7e97c-115">Esempio 2: ottenere le metriche di utilizzo del pool utilizzando un filtro</span><span class="sxs-lookup"><span data-stu-id="7e97c-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzureBatchPoolUsageMetrics -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="7e97c-116">Questo comando restituisce le metriche di utilizzo per il pool denominato ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="7e97c-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="7e97c-117">Il comando specifica una stringa di filtro per specificare il pool e usa lo stesso valore $Context dell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="7e97c-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="7e97c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e97c-118">PARAMETERS</span></span>

### <span data-ttu-id="7e97c-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7e97c-119">-BatchContext</span></span>
<span data-ttu-id="7e97c-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="7e97c-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7e97c-121">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="7e97c-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="7e97c-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7e97c-122">-EndTime</span></span>
<span data-ttu-id="7e97c-123">Specifica la fine di un intervallo di tempo per cui questo cmdlet ottiene le metriche di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="7e97c-123">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="7e97c-124">Specificare un'ora almeno due ore prima.</span><span class="sxs-lookup"><span data-stu-id="7e97c-124">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="7e97c-125">Se non si specifica un'ora di fine, questo cmdlet usa l'ultimo intervallo di aggregazione attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="7e97c-125">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e97c-126">-Filtro</span><span class="sxs-lookup"><span data-stu-id="7e97c-126">-Filter</span></span>
<span data-ttu-id="7e97c-127">Specifica una clausola di filtro OData da usare per filtrare le metriche che il cmdlet retruns.</span><span class="sxs-lookup"><span data-stu-id="7e97c-127">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="7e97c-128">L'unica proprietà valida è **poolId** con un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="7e97c-128">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="7e97c-129">Le operazioni possibili sono le seguenti: EQ, GE, gt, le, LT, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="7e97c-129">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="7e97c-130">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7e97c-130">-StartTime</span></span>
<span data-ttu-id="7e97c-131">Specifica l'inizio di un intervallo di tempo per cui questo cmdlet ottiene le metriche di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="7e97c-131">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="7e97c-132">Specificare un periodo di tempo di almeno due ore e mezzo prima.</span><span class="sxs-lookup"><span data-stu-id="7e97c-132">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="7e97c-133">Se non si specifica un'ora di inizio, questo cmdlet usa l'ultimo intervallo di aggregazione attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="7e97c-133">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e97c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e97c-134">-DefaultProfile</span></span>
<span data-ttu-id="7e97c-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e97c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e97c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e97c-136">CommonParameters</span></span>
<span data-ttu-id="7e97c-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e97c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e97c-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e97c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e97c-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e97c-139">INPUTS</span></span>

### <span data-ttu-id="7e97c-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7e97c-140">BatchAccountContext</span></span>
<span data-ttu-id="7e97c-141">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7e97c-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="7e97c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e97c-142">OUTPUTS</span></span>

### <span data-ttu-id="7e97c-143">PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="7e97c-143">PSPoolUsageMetrics</span></span>

## <span data-ttu-id="7e97c-144">Note</span><span class="sxs-lookup"><span data-stu-id="7e97c-144">NOTES</span></span>

## <span data-ttu-id="7e97c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e97c-145">RELATED LINKS</span></span>

[<span data-ttu-id="7e97c-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7e97c-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7e97c-147">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="7e97c-147">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="7e97c-148">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="7e97c-148">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


