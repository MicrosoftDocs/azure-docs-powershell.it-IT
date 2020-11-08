---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: cabef75fb55cc3b8409edb3425de84531209b479
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030641"
---
# <span data-ttu-id="e84eb-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="e84eb-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="e84eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e84eb-102">SYNOPSIS</span></span>
<span data-ttu-id="e84eb-103">Ottiene le metriche per l'utilizzo del pool per un account batch.</span><span class="sxs-lookup"><span data-stu-id="e84eb-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="e84eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e84eb-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e84eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e84eb-105">DESCRIPTION</span></span>
<span data-ttu-id="e84eb-106">Il cmdlet **Get-AzBatchPoolUsageMetric** ottiene le metriche di utilizzo, aggregate in base al pool tra intervalli di tempo individuali, per l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="e84eb-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="e84eb-107">Puoi ottenere le statistiche per un pool specifico e per un intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="e84eb-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="e84eb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e84eb-108">EXAMPLES</span></span>

### <span data-ttu-id="e84eb-109">Esempio 1: ottenere le metriche per l'utilizzo del pool per un intervallo di tempo</span><span class="sxs-lookup"><span data-stu-id="e84eb-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzBatchPoolUsageMetric -StartTime $StartTime -EndTime $EndTime -BatchContext $context
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

<span data-ttu-id="e84eb-110">Il primo comando crea un riferimento a un oggetto alle chiavi dell'account per l'account batch denominato ContosoBatchAccount tramite **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="e84eb-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="e84eb-111">Il comando Archivia il riferimento all'oggetto nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="e84eb-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="e84eb-112">I due comandi successivi creano oggetti **DateTime** usando il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="e84eb-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="e84eb-113">I comandi archiviano questi valori nelle variabili $StartTime e $EndTime per l'utilizzo con il comando finale.</span><span class="sxs-lookup"><span data-stu-id="e84eb-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="e84eb-114">Il comando finale restituisce tutte le metriche di utilizzo del pool, aggregate in base al pool, nell'intervallo di tempo compreso tra gli orari di inizio e di fine specificati.</span><span class="sxs-lookup"><span data-stu-id="e84eb-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="e84eb-115">Esempio 2: ottenere le metriche di utilizzo del pool utilizzando un filtro</span><span class="sxs-lookup"><span data-stu-id="e84eb-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzBatchPoolUsageMetric -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="e84eb-116">Questo comando restituisce le metriche di utilizzo per il pool denominato ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="e84eb-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="e84eb-117">Il comando specifica una stringa di filtro per specificare il pool e usa lo stesso valore $Context dell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="e84eb-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="e84eb-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e84eb-118">PARAMETERS</span></span>

### <span data-ttu-id="e84eb-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e84eb-119">-BatchContext</span></span>
<span data-ttu-id="e84eb-120">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="e84eb-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e84eb-121">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="e84eb-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e84eb-122">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="e84eb-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e84eb-123">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e84eb-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e84eb-124">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e84eb-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e84eb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e84eb-125">-DefaultProfile</span></span>
<span data-ttu-id="e84eb-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e84eb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e84eb-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e84eb-127">-EndTime</span></span>
<span data-ttu-id="e84eb-128">Specifica la fine di un intervallo di tempo per cui questo cmdlet ottiene le metriche di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e84eb-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="e84eb-129">Specificare un'ora almeno due ore prima.</span><span class="sxs-lookup"><span data-stu-id="e84eb-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="e84eb-130">Se non si specifica un'ora di fine, questo cmdlet usa l'ultimo intervallo di aggregazione attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="e84eb-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="e84eb-131">-Filtro</span><span class="sxs-lookup"><span data-stu-id="e84eb-131">-Filter</span></span>
<span data-ttu-id="e84eb-132">Specifica una clausola di filtro OData da usare per filtrare le metriche restituite da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e84eb-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="e84eb-133">L'unica proprietà valida è **poolId** con un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="e84eb-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="e84eb-134">Le operazioni possibili sono le seguenti: EQ, GE, gt, le, LT, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="e84eb-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="e84eb-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e84eb-135">-StartTime</span></span>
<span data-ttu-id="e84eb-136">Specifica l'inizio di un intervallo di tempo per cui questo cmdlet ottiene le metriche di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e84eb-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="e84eb-137">Specificare un periodo di tempo di almeno due ore e mezzo prima.</span><span class="sxs-lookup"><span data-stu-id="e84eb-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="e84eb-138">Se non si specifica un'ora di inizio, questo cmdlet usa l'ultimo intervallo di aggregazione attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="e84eb-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="e84eb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e84eb-139">CommonParameters</span></span>
<span data-ttu-id="e84eb-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e84eb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e84eb-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e84eb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e84eb-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e84eb-142">INPUTS</span></span>

### <span data-ttu-id="e84eb-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e84eb-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e84eb-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e84eb-144">OUTPUTS</span></span>

### <span data-ttu-id="e84eb-145">Microsoft.Azure.Commands.Batch. Models. PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="e84eb-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="e84eb-146">Note</span><span class="sxs-lookup"><span data-stu-id="e84eb-146">NOTES</span></span>

## <span data-ttu-id="e84eb-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e84eb-147">RELATED LINKS</span></span>

[<span data-ttu-id="e84eb-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e84eb-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e84eb-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="e84eb-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="e84eb-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="e84eb-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)


