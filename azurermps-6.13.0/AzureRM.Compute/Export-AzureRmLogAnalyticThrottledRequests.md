---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: 97f68475ab935df66b67f0cab92466e68732a735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511911"
---
# <span data-ttu-id="1efa3-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="1efa3-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="1efa3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1efa3-102">SYNOPSIS</span></span>
<span data-ttu-id="1efa3-103">Esportare i registri che mostrano le richieste di API a limitazione totale per l'abbonamento nella finestra del tempo specificata.</span><span class="sxs-lookup"><span data-stu-id="1efa3-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1efa3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1efa3-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1efa3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1efa3-105">DESCRIPTION</span></span>
<span data-ttu-id="1efa3-106">In questo articolo viene esportato il numero totale di chiamate API Microsoft. Compute limitate.</span><span class="sxs-lookup"><span data-stu-id="1efa3-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="1efa3-107">I registri possono essere ulteriormente aggregati da tre opzioni: GroupByOperationName, GroupByThrottlePolicy o GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="1efa3-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="1efa3-108">Tieni presente che questo cmdlet raccoglie solo i registri CRP.</span><span class="sxs-lookup"><span data-stu-id="1efa3-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="1efa3-109">Per una panoramica della limitazione delle API del provider di risorse di calcolo, vedere https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="1efa3-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="1efa3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1efa3-110">EXAMPLES</span></span>

### <span data-ttu-id="1efa3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1efa3-111">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="1efa3-112">Questo comando Archivia le chiamate dell'API Microsoft. Compute a limitazione totale tra 2018-02-20T17:54:14 e 2018-02-22T17:54:17 nell'URI SAS indicato, aggregato per nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1efa3-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="1efa3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1efa3-113">PARAMETERS</span></span>

### <span data-ttu-id="1efa3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1efa3-114">-AsJob</span></span>
<span data-ttu-id="1efa3-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1efa3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1efa3-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="1efa3-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="1efa3-117">URI SAS del contenitore di BLOB di registrazione a cui scrive l'API LogAnalytics in cui vengono scritti i registri di output.</span><span class="sxs-lookup"><span data-stu-id="1efa3-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="1efa3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1efa3-118">-DefaultProfile</span></span>
<span data-ttu-id="1efa3-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1efa3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1efa3-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="1efa3-120">-FromTime</span></span>
<span data-ttu-id="1efa3-121">Dall'ora della query</span><span class="sxs-lookup"><span data-stu-id="1efa3-121">From time of the query</span></span>

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

### <span data-ttu-id="1efa3-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="1efa3-122">-GroupByOperationName</span></span>
<span data-ttu-id="1efa3-123">Risultato della query di gruppo per nome operazione.</span><span class="sxs-lookup"><span data-stu-id="1efa3-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="1efa3-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="1efa3-124">-GroupByResourceName</span></span>
<span data-ttu-id="1efa3-125">Risultato della query di gruppo per nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="1efa3-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="1efa3-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="1efa3-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="1efa3-127">Risultato della query di gruppo per criteri di limitazione applicati.</span><span class="sxs-lookup"><span data-stu-id="1efa3-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="1efa3-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1efa3-128">-Location</span></span>
<span data-ttu-id="1efa3-129">Posizione in cui viene eseguita la query su analisi log.</span><span class="sxs-lookup"><span data-stu-id="1efa3-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="1efa3-130">-ToTime</span><span class="sxs-lookup"><span data-stu-id="1efa3-130">-ToTime</span></span>
<span data-ttu-id="1efa3-131">Per l'ora della query</span><span class="sxs-lookup"><span data-stu-id="1efa3-131">To time of the query</span></span>

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

### <span data-ttu-id="1efa3-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1efa3-132">-Confirm</span></span>
<span data-ttu-id="1efa3-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1efa3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1efa3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1efa3-134">-WhatIf</span></span>
<span data-ttu-id="1efa3-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1efa3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1efa3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1efa3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1efa3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1efa3-137">CommonParameters</span></span>
<span data-ttu-id="1efa3-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1efa3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1efa3-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1efa3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1efa3-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1efa3-140">INPUTS</span></span>

### <span data-ttu-id="1efa3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1efa3-141">System.String</span></span>

## <span data-ttu-id="1efa3-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1efa3-142">OUTPUTS</span></span>

### <span data-ttu-id="1efa3-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="1efa3-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="1efa3-144">Note</span><span class="sxs-lookup"><span data-stu-id="1efa3-144">NOTES</span></span>

## <span data-ttu-id="1efa3-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1efa3-145">RELATED LINKS</span></span>
