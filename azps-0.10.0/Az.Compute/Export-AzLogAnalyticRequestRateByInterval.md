---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: bbf275b08421265130da898b670b46c95b15c34c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863833"
---
# <span data-ttu-id="dda48-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="dda48-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="dda48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dda48-102">SYNOPSIS</span></span>
<span data-ttu-id="dda48-103">Esportare i registri che mostrano le richieste API effettuate da questo abbonamento nella finestra del tempo specificata per visualizzare le attività di limitazione.</span><span class="sxs-lookup"><span data-stu-id="dda48-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="dda48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dda48-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval  [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins>
 [-GroupByOperationName] [-GroupByThrottlePolicy] [-GroupByResourceName] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dda48-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dda48-105">DESCRIPTION</span></span>
<span data-ttu-id="dda48-106">Questo Esporta i numeri aggregati delle chiamate API Microsoft. Compute separate da Success, Failure o Throttled visualizzati in intervalli di tempo.</span><span class="sxs-lookup"><span data-stu-id="dda48-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="dda48-107">I registri possono essere ulteriormente raggruppati per tre parametri: GroupByOperationName, GroupByThrottlePolicy o GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="dda48-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="dda48-108">Tieni presente che questo cmdlet raccoglie solo i registri CRP.</span><span class="sxs-lookup"><span data-stu-id="dda48-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="dda48-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dda48-109">EXAMPLES</span></span>

### <span data-ttu-id="dda48-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dda48-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="dda48-111">Questo comando Archivia i numeri aggregati delle chiamate API Microsoft. Compute separate da Success, Failure o Throttled tra 2018-02-20T17:54:14 e 2018-02-22T17:54:17 nell'URI SAS indicato, aggregato per nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dda48-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="dda48-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dda48-112">PARAMETERS</span></span>

### <span data-ttu-id="dda48-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dda48-113">-AsJob</span></span>
<span data-ttu-id="dda48-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dda48-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda48-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="dda48-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="dda48-116">URI SAS del contenitore di BLOB di registrazione a cui scrive l'API LogAnalytics in cui vengono scritti i registri di output.</span><span class="sxs-lookup"><span data-stu-id="dda48-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda48-117">-DefaultProfile</span></span>
<span data-ttu-id="dda48-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dda48-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dda48-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="dda48-119">-FromTime</span></span>
<span data-ttu-id="dda48-120">Dall'ora della query</span><span class="sxs-lookup"><span data-stu-id="dda48-120">From time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda48-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="dda48-121">-GroupByOperationName</span></span>
<span data-ttu-id="dda48-122">Risultato della query di gruppo per nome operazione.</span><span class="sxs-lookup"><span data-stu-id="dda48-122">Group query result by Operation Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda48-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="dda48-123">-GroupByResourceName</span></span>
<span data-ttu-id="dda48-124">Risultato della query di gruppo per nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="dda48-124">Group query result by Resource Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda48-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="dda48-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="dda48-126">Risultato della query di gruppo per criteri di limitazione applicati.</span><span class="sxs-lookup"><span data-stu-id="dda48-126">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda48-127">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="dda48-127">-IntervalLength</span></span>
<span data-ttu-id="dda48-128">Valore di intervallo in minuti usato per creare log delle tariffe di chiamata di LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="dda48-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: IntervalInMins
Parameter Sets: (All)
Aliases: 
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda48-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="dda48-129">-Location</span></span>
<span data-ttu-id="dda48-130">Posizione in cui viene eseguita la query su analisi log.</span><span class="sxs-lookup"><span data-stu-id="dda48-130">The location upon which log analytic is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dda48-131">-ToTime</span><span class="sxs-lookup"><span data-stu-id="dda48-131">-ToTime</span></span>
<span data-ttu-id="dda48-132">Per l'ora della query</span><span class="sxs-lookup"><span data-stu-id="dda48-132">To time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda48-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dda48-133">-Confirm</span></span>
<span data-ttu-id="dda48-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dda48-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda48-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda48-135">-WhatIf</span></span>
<span data-ttu-id="dda48-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dda48-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dda48-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dda48-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dda48-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda48-138">CommonParameters</span></span>
<span data-ttu-id="dda48-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda48-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda48-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dda48-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda48-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dda48-141">INPUTS</span></span>

### <span data-ttu-id="dda48-142">System. String</span><span class="sxs-lookup"><span data-stu-id="dda48-142">System.String</span></span>

## <span data-ttu-id="dda48-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dda48-143">OUTPUTS</span></span>

### <span data-ttu-id="dda48-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="dda48-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="dda48-145">Note</span><span class="sxs-lookup"><span data-stu-id="dda48-145">NOTES</span></span>

## <span data-ttu-id="dda48-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dda48-146">RELATED LINKS</span></span>

