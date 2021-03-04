---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: feae2282f6b989b8d595b2a51cd147975e689174
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969406"
---
# <span data-ttu-id="8cc6b-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="8cc6b-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="8cc6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cc6b-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc6b-103">Log di esportazione che mostrano le richieste Api effettuate da questa sottoscrizione nel periodo di tempo specificato per mostrare le attività di limitazione.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="8cc6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cc6b-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cc6b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8cc6b-105">DESCRIPTION</span></span>
<span data-ttu-id="8cc6b-106">Esporta i dati statistici sulle chiamate dell'abbonamento all'API Microsoft.Compute per stato Operazione completata, Operazione non riuscita o Limitazione, in intervalli di tempo predefiniti.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="8cc6b-107">I log possono essere ulteriormente raggruppati in base a cinque parametri: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent o GroupByApplicationId.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-107">The logs can be further grouped by five parameters: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="8cc6b-108">Si noti che questo cmdlet raccoglie solo i log del provider di risorse di calcolo; Inoltre, i dati relativi ai tipi di risorsa Disco e Snapshot non sono ancora disponibili.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="8cc6b-109">Per una panoramica della limitazione API del provider di risorse di calcolo, vedere https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="8cc6b-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="8cc6b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cc6b-110">EXAMPLES</span></span>

### <span data-ttu-id="8cc6b-111">Esempio 1: Esportare i record aggregati in base al nome dell'operazione</span><span class="sxs-lookup"><span data-stu-id="8cc6b-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             operationName   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <operationName> 10            10                 0
2/21/2018  7:30:00 PM <operationName> 8             8                  0
2/21/2018  9:00:00 PM <operationName> 9             9                  0

```

<span data-ttu-id="8cc6b-112">Questo comando archivia i numeri aggregati delle chiamate all'API Microsoft.Compute separate da Success, Failure o Throttled between 2018-02-20T17:54:14 e 2018-02-22T17:54:17 nell'URI di firma di accesso condiviso specificato, aggregato in base al nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="8cc6b-113">Esempio 2: Esportare i record aggregati in base all'ID applicazione</span><span class="sxs-lookup"><span data-stu-id="8cc6b-113">Example 2: Export records aggregated by application id</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByApplicationId

This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             clientApplicationId   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <clientApplicationId> 10            10                 0
2/21/2018  7:30:00 PM <clientApplicationId> 8             8                  0
2/21/2018  9:00:00 PM <clientApplicationId> 9             9                  0

```

<span data-ttu-id="8cc6b-114">Questo comando archivia i numeri aggregati delle chiamate all'API Microsoft.Compute separate da Success, Failure o Throttled between 2018-02-20T17:54:14 e 2018-02-22T17:54:17 nell'URI di firma di accesso condiviso specificato, aggregato in base all'ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-114">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by application id.</span></span> 

### <span data-ttu-id="8cc6b-115">Esempio 3: Esportare i record aggregati per agente utente</span><span class="sxs-lookup"><span data-stu-id="8cc6b-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByUserAgent
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             userAgent   TotalRequests SuccessfulRequests ThrottledRequests
---------             ---------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <userAgent> 10            10                 0
2/21/2018  7:30:00 PM <userAgent> 8             8                  0
2/21/2018  9:00:00 PM <userAgent> 9             9                  0

```

<span data-ttu-id="8cc6b-116">Questo comando archivia i numeri aggregati delle chiamate all'API Microsoft.Compute separate da Success, Failure o Throttled between 2018-02-20T17:54:14 e 2018-02-22T17:54:17 nell'URI di firma di accesso condiviso specificato, aggregato dall'agente utente.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-116">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span> 

## <span data-ttu-id="8cc6b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cc6b-117">PARAMETERS</span></span>

### <span data-ttu-id="8cc6b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cc6b-118">-AsJob</span></span>
<span data-ttu-id="8cc6b-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8cc6b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cc6b-120">-BLOBContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="8cc6b-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="8cc6b-121">Uri di firma di accesso condiviso del contenitore BLOB di registrazione in cui l'Api LogAnalytics scrive i log di output.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc6b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc6b-122">-DefaultProfile</span></span>
<span data-ttu-id="8cc6b-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc6b-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="8cc6b-124">-FromTime</span></span>
<span data-ttu-id="8cc6b-125">Dal momento della query</span><span class="sxs-lookup"><span data-stu-id="8cc6b-125">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc6b-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="8cc6b-126">-GroupByApplicationId</span></span>
<span data-ttu-id="8cc6b-127">Risultato della query di raggruppamento in base all'ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="8cc6b-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="8cc6b-128">-GroupByOperationName</span></span>
<span data-ttu-id="8cc6b-129">Risultato della query di raggruppamento in base al nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="8cc6b-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="8cc6b-130">-GroupByResourceName</span></span>
<span data-ttu-id="8cc6b-131">Risultato della query di raggruppamento in base al nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="8cc6b-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="8cc6b-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="8cc6b-133">Risultato della query di gruppo con criteri di limitazione applicati.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="8cc6b-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="8cc6b-134">-GroupByUserAgent</span></span>
<span data-ttu-id="8cc6b-135">Risultato della query di gruppo per UserAgent.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="8cc6b-136">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="8cc6b-136">-IntervalLength</span></span>
<span data-ttu-id="8cc6b-137">Valore dell'intervallo in minuti usato per creare i registri delle frequenze delle chiamate di LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-137">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc6b-138">-Location</span><span class="sxs-lookup"><span data-stu-id="8cc6b-138">-Location</span></span>
<span data-ttu-id="8cc6b-139">Posizione in cui viene eseguita la query di analisi del log.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-139">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc6b-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8cc6b-140">-NoWait</span></span>
<span data-ttu-id="8cc6b-141">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8cc6b-142">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8cc6b-143">-ToTime</span><span class="sxs-lookup"><span data-stu-id="8cc6b-143">-ToTime</span></span>
<span data-ttu-id="8cc6b-144">All'ora della query</span><span class="sxs-lookup"><span data-stu-id="8cc6b-144">To time of the query</span></span>

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

### <span data-ttu-id="8cc6b-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cc6b-145">-Confirm</span></span>
<span data-ttu-id="8cc6b-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cc6b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc6b-147">-WhatIf</span></span>
<span data-ttu-id="8cc6b-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc6b-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cc6b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc6b-150">CommonParameters</span></span>
<span data-ttu-id="8cc6b-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc6b-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8cc6b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc6b-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="8cc6b-153">INPUTS</span></span>

### <span data-ttu-id="8cc6b-154">System.String</span><span class="sxs-lookup"><span data-stu-id="8cc6b-154">System.String</span></span>

## <span data-ttu-id="8cc6b-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cc6b-155">OUTPUTS</span></span>

### <span data-ttu-id="8cc6b-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="8cc6b-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="8cc6b-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="8cc6b-157">NOTES</span></span>

## <span data-ttu-id="8cc6b-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cc6b-158">RELATED LINKS</span></span>
