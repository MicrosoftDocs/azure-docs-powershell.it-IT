---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
ms.openlocfilehash: e98819ab7de961dacefea673ac43690ad260ac3b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866148"
---
# <span data-ttu-id="d7ce9-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="d7ce9-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="d7ce9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ce9-103">Esportare i registri che mostrano le richieste di API a limitazione totale per l'abbonamento nella finestra del tempo specificata.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7ce9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7ce9-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String>
 [-GroupByOperationName]  [-GroupByThrottlePolicy] [-GroupByResourceName] 
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7ce9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7ce9-105">DESCRIPTION</span></span>
<span data-ttu-id="d7ce9-106">In questo articolo viene esportato il numero totale di chiamate API Microsoft. Compute limitate.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="d7ce9-107">I registri possono essere ulteriormente aggregati da tre opzioni: GroupByOperationName, GroupByThrottlePolicy o GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="d7ce9-108">Tieni presente che questo cmdlet raccoglie solo i registri CRP.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="d7ce9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7ce9-109">EXAMPLES</span></span>

### <span data-ttu-id="d7ce9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d7ce9-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="d7ce9-111">Questo comando Archivia le chiamate dell'API Microsoft. Compute a limitazione totale tra 2018-02-20T17:54:14 e 2018-02-22T17:54:17 nell'URI SAS indicato, aggregato per nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="d7ce9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7ce9-112">PARAMETERS</span></span>

### <span data-ttu-id="d7ce9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7ce9-113">-AsJob</span></span>
<span data-ttu-id="d7ce9-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d7ce9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7ce9-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="d7ce9-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="d7ce9-116">URI SAS del contenitore di BLOB di registrazione a cui scrive l'API LogAnalytics in cui vengono scritti i registri di output.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="d7ce9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ce9-117">-DefaultProfile</span></span>
<span data-ttu-id="d7ce9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7ce9-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="d7ce9-119">-FromTime</span></span>
<span data-ttu-id="d7ce9-120">Dall'ora della query</span><span class="sxs-lookup"><span data-stu-id="d7ce9-120">From time of the query</span></span>

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

### <span data-ttu-id="d7ce9-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="d7ce9-121">-GroupByOperationName</span></span>
<span data-ttu-id="d7ce9-122">Risultato della query di gruppo per nome operazione.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="d7ce9-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="d7ce9-123">-GroupByResourceName</span></span>
<span data-ttu-id="d7ce9-124">Risultato della query di gruppo per nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="d7ce9-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="d7ce9-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="d7ce9-126">Risultato della query di gruppo per criteri di limitazione applicati.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="d7ce9-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d7ce9-127">-Location</span></span>
<span data-ttu-id="d7ce9-128">Posizione in cui viene eseguita la query su analisi log.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="d7ce9-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="d7ce9-129">-ToTime</span></span>
<span data-ttu-id="d7ce9-130">Per l'ora della query</span><span class="sxs-lookup"><span data-stu-id="d7ce9-130">To time of the query</span></span>

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

### <span data-ttu-id="d7ce9-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d7ce9-131">-Confirm</span></span>
<span data-ttu-id="d7ce9-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7ce9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7ce9-133">-WhatIf</span></span>
<span data-ttu-id="d7ce9-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7ce9-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7ce9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ce9-136">CommonParameters</span></span>
<span data-ttu-id="d7ce9-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7ce9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ce9-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ce9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ce9-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7ce9-139">INPUTS</span></span>

### <span data-ttu-id="d7ce9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d7ce9-140">System.String</span></span>

## <span data-ttu-id="d7ce9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7ce9-141">OUTPUTS</span></span>

### <span data-ttu-id="d7ce9-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="d7ce9-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="d7ce9-143">Note</span><span class="sxs-lookup"><span data-stu-id="d7ce9-143">NOTES</span></span>

## <span data-ttu-id="d7ce9-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7ce9-144">RELATED LINKS</span></span>

