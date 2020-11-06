---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: c4008e9b6587e0b6c5b8ed56057490b0aad8764f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519746"
---
# <span data-ttu-id="07e47-101">Export-AzureRmLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="07e47-101">Export-AzureRmLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="07e47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07e47-102">SYNOPSIS</span></span>
<span data-ttu-id="07e47-103">Esportare i registri che mostrano le richieste API effettuate da questo abbonamento nella finestra del tempo specificata per visualizzare le attività di limitazione.</span><span class="sxs-lookup"><span data-stu-id="07e47-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07e47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07e47-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticRequestRateByInterval [-FromTime] <DateTime> [-GroupByOperationName]
 [-IntervalLength] <IntervalInMins> [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String>
 [-GroupByResourceName] [-ToTime] <DateTime> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07e47-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07e47-105">DESCRIPTION</span></span>
<span data-ttu-id="07e47-106">Esporta i dati statistici sulle chiamate dell'abbonamento all'API Microsoft. COMPUTE per successo, errore o stato strozzato, in intervalli di tempo predefiniti.</span><span class="sxs-lookup"><span data-stu-id="07e47-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="07e47-107">I registri possono essere ulteriormente raggruppati per tre parametri: GroupByOperationName, GroupByThrottlePolicy o GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="07e47-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="07e47-108">Tieni presente che questo cmdlet raccoglie solo i registri del provider di risorse COMPUTE; Inoltre, i dati relativi ai tipi di risorsa disco e snapshot non sono ancora disponibili.</span><span class="sxs-lookup"><span data-stu-id="07e47-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="07e47-109">Per una panoramica della limitazione delle API del provider di risorse di calcolo, vedere https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="07e47-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="07e47-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07e47-110">EXAMPLES</span></span>

### <span data-ttu-id="07e47-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07e47-111">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="07e47-112">Questo comando Archivia i numeri aggregati delle chiamate API Microsoft. Compute separate da Success, Failure o Throttled tra 2018-02-20T17:54:14 e 2018-02-22T17:54:17 nell'URI SAS indicato, aggregato per nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="07e47-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="07e47-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07e47-113">PARAMETERS</span></span>

### <span data-ttu-id="07e47-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07e47-114">-AsJob</span></span>
<span data-ttu-id="07e47-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="07e47-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e47-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="07e47-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="07e47-117">URI SAS del contenitore di BLOB di registrazione a cui scrive l'API LogAnalytics in cui vengono scritti i registri di output.</span><span class="sxs-lookup"><span data-stu-id="07e47-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e47-118">-DefaultProfile</span></span>
<span data-ttu-id="07e47-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07e47-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07e47-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="07e47-120">-FromTime</span></span>
<span data-ttu-id="07e47-121">Dall'ora della query</span><span class="sxs-lookup"><span data-stu-id="07e47-121">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e47-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="07e47-122">-GroupByOperationName</span></span>
<span data-ttu-id="07e47-123">Risultato della query di gruppo per nome operazione.</span><span class="sxs-lookup"><span data-stu-id="07e47-123">Group query result by Operation Name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e47-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="07e47-124">-GroupByResourceName</span></span>
<span data-ttu-id="07e47-125">Risultato della query di gruppo per nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="07e47-125">Group query result by Resource Name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e47-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="07e47-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="07e47-127">Risultato della query di gruppo per criteri di limitazione applicati.</span><span class="sxs-lookup"><span data-stu-id="07e47-127">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e47-128">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="07e47-128">-IntervalLength</span></span>
<span data-ttu-id="07e47-129">Valore di intervallo in minuti usato per creare log delle tariffe di chiamata di LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="07e47-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e47-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="07e47-130">-Location</span></span>
<span data-ttu-id="07e47-131">Posizione in cui viene eseguita la query su analisi log.</span><span class="sxs-lookup"><span data-stu-id="07e47-131">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e47-132">-ToTime</span><span class="sxs-lookup"><span data-stu-id="07e47-132">-ToTime</span></span>
<span data-ttu-id="07e47-133">Per l'ora della query</span><span class="sxs-lookup"><span data-stu-id="07e47-133">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e47-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07e47-134">-Confirm</span></span>
<span data-ttu-id="07e47-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07e47-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e47-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07e47-136">-WhatIf</span></span>
<span data-ttu-id="07e47-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07e47-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07e47-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07e47-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e47-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e47-139">CommonParameters</span></span>
<span data-ttu-id="07e47-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07e47-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e47-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e47-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e47-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07e47-142">INPUTS</span></span>

### <span data-ttu-id="07e47-143">System. String</span><span class="sxs-lookup"><span data-stu-id="07e47-143">System.String</span></span>

## <span data-ttu-id="07e47-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07e47-144">OUTPUTS</span></span>

### <span data-ttu-id="07e47-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="07e47-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="07e47-146">Note</span><span class="sxs-lookup"><span data-stu-id="07e47-146">NOTES</span></span>

## <span data-ttu-id="07e47-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07e47-147">RELATED LINKS</span></span>
