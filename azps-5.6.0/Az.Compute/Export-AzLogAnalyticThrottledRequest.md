---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 02d78a36bcd2afc6eef037a0b043c5db89d37f0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969405"
---
# <span data-ttu-id="bf5f6-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="bf5f6-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="bf5f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf5f6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5f6-103">Esportare i log che mostrano il totale delle richieste Api limitate per la sottoscrizione nel periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="bf5f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf5f6-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf5f6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bf5f6-105">DESCRIPTION</span></span>
<span data-ttu-id="bf5f6-106">Viene esportato il numero totale di chiamate all'API Microsoft.Compute limitate.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="bf5f6-107">I log possono essere ulteriormente aggregati da cinque opzioni: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent o GroupByApplicationId.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-107">The logs can be further aggregated by five options: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="bf5f6-108">Tenere presente che questo cmdlet raccoglie solo log CRP.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="bf5f6-109">Per una panoramica della limitazione API del provider di risorse di calcolo, vedere https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="bf5f6-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="bf5f6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf5f6-110">EXAMPLES</span></span>

### <span data-ttu-id="bf5f6-111">Esempio 1: Esportare i record aggregati in base al nome dell'operazione</span><span class="sxs-lookup"><span data-stu-id="bf5f6-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="bf5f6-112">Questo comando archivia il totale delle chiamate all'API Microsoft.Compute limitate tra 2018-02-20T17:54:14 e 2018-02-22T17:54:17 nell'URI di firma di accesso condiviso specificato, aggregato in base al nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="bf5f6-113">Esempio 2: Esportare i record aggregati in base all'ID applicazione</span><span class="sxs-lookup"><span data-stu-id="bf5f6-113">Example 2: Export records aggregated by applicaiton id</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByApplicationId
```

<span data-ttu-id="bf5f6-114">Questo comando archivia il totale delle chiamate all'API Microsoft.Compute limitate tra 2018-02-20T17:54:14 e 2018-02-22T17:54:17 nell'URI di firma di accesso condiviso specificato, aggregato in base all'ID di applicazione.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-114">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by appliction id.</span></span>

### <span data-ttu-id="bf5f6-115">Esempio 3: Esportare i record aggregati per agente utente</span><span class="sxs-lookup"><span data-stu-id="bf5f6-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByUserAgent
```

<span data-ttu-id="bf5f6-116">Questo comando archivia il totale delle chiamate all'API Microsoft.Compute limitate tra 2018-02-20T17:54:14 e 2018-02-22T17:54:17 nell'URI di firma di accesso condiviso specificato, aggregato dall'agente utente.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-116">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span>

## <span data-ttu-id="bf5f6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf5f6-117">PARAMETERS</span></span>

### <span data-ttu-id="bf5f6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf5f6-118">-AsJob</span></span>
<span data-ttu-id="bf5f6-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bf5f6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf5f6-120">-BLOBContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="bf5f6-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="bf5f6-121">Uri di firma di accesso condiviso del contenitore BLOB di registrazione in cui l'Api LogAnalytics scrive i log di output.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="bf5f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5f6-122">-DefaultProfile</span></span>
<span data-ttu-id="bf5f6-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf5f6-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="bf5f6-124">-FromTime</span></span>
<span data-ttu-id="bf5f6-125">Dal momento della query</span><span class="sxs-lookup"><span data-stu-id="bf5f6-125">From time of the query</span></span>

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

### <span data-ttu-id="bf5f6-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="bf5f6-126">-GroupByApplicationId</span></span>
<span data-ttu-id="bf5f6-127">Risultato della query di raggruppamento in base all'ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="bf5f6-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="bf5f6-128">-GroupByOperationName</span></span>
<span data-ttu-id="bf5f6-129">Risultato della query di raggruppamento in base al nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="bf5f6-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="bf5f6-130">-GroupByResourceName</span></span>
<span data-ttu-id="bf5f6-131">Risultato della query di raggruppamento in base al nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="bf5f6-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="bf5f6-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="bf5f6-133">Risultato della query di gruppo con criteri di limitazione applicati.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="bf5f6-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="bf5f6-134">-GroupByUserAgent</span></span>
<span data-ttu-id="bf5f6-135">Risultato della query di gruppo per UserAgent.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="bf5f6-136">-Location</span><span class="sxs-lookup"><span data-stu-id="bf5f6-136">-Location</span></span>
<span data-ttu-id="bf5f6-137">Posizione in cui viene eseguita la query di analisi del log.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-137">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="bf5f6-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bf5f6-138">-NoWait</span></span>
<span data-ttu-id="bf5f6-139">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="bf5f6-140">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="bf5f6-141">-ToTime</span><span class="sxs-lookup"><span data-stu-id="bf5f6-141">-ToTime</span></span>
<span data-ttu-id="bf5f6-142">All'ora della query</span><span class="sxs-lookup"><span data-stu-id="bf5f6-142">To time of the query</span></span>

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

### <span data-ttu-id="bf5f6-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf5f6-143">-Confirm</span></span>
<span data-ttu-id="bf5f6-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf5f6-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf5f6-145">-WhatIf</span></span>
<span data-ttu-id="bf5f6-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf5f6-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf5f6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5f6-148">CommonParameters</span></span>
<span data-ttu-id="bf5f6-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5f6-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bf5f6-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5f6-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="bf5f6-151">INPUTS</span></span>

### <span data-ttu-id="bf5f6-152">System.String</span><span class="sxs-lookup"><span data-stu-id="bf5f6-152">System.String</span></span>

## <span data-ttu-id="bf5f6-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf5f6-153">OUTPUTS</span></span>

### <span data-ttu-id="bf5f6-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="bf5f6-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="bf5f6-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="bf5f6-155">NOTES</span></span>

## <span data-ttu-id="bf5f6-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf5f6-156">RELATED LINKS</span></span>
