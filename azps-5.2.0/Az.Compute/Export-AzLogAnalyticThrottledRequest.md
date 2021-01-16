---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 79bf599b22796181c2f433f186e0e4bde8094773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330136"
---
# <span data-ttu-id="19d24-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="19d24-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="19d24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19d24-102">SYNOPSIS</span></span>
<span data-ttu-id="19d24-103">Esportare i registri che mostrano le richieste di API a limitazione totale per l'abbonamento nella finestra del tempo specificata.</span><span class="sxs-lookup"><span data-stu-id="19d24-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="19d24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19d24-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19d24-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19d24-105">DESCRIPTION</span></span>
<span data-ttu-id="19d24-106">In questo articolo viene esportato il numero totale di chiamate API Microsoft. Compute limitate.</span><span class="sxs-lookup"><span data-stu-id="19d24-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="19d24-107">I registri possono essere ulteriormente aggregati da tre opzioni: GroupByOperationName, GroupByThrottlePolicy o GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="19d24-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="19d24-108">Tieni presente che questo cmdlet raccoglie solo i registri CRP.</span><span class="sxs-lookup"><span data-stu-id="19d24-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="19d24-109">Per una panoramica della limitazione delle API del provider di risorse di calcolo, vedere https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="19d24-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="19d24-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19d24-110">EXAMPLES</span></span>

### <span data-ttu-id="19d24-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="19d24-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="19d24-112">Questo comando Archivia le chiamate dell'API Microsoft. Compute a limitazione totale tra 2018-02-20T17:54:14 e 2018-02-22T17:54:17 nell'URI SAS indicato, aggregato per nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="19d24-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="19d24-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19d24-113">PARAMETERS</span></span>

### <span data-ttu-id="19d24-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19d24-114">-AsJob</span></span>
<span data-ttu-id="19d24-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="19d24-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19d24-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="19d24-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="19d24-117">URI SAS del contenitore di BLOB di registrazione a cui scrive l'API LogAnalytics in cui vengono scritti i registri di output.</span><span class="sxs-lookup"><span data-stu-id="19d24-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="19d24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d24-118">-DefaultProfile</span></span>
<span data-ttu-id="19d24-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19d24-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19d24-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="19d24-120">-FromTime</span></span>
<span data-ttu-id="19d24-121">Dall'ora della query</span><span class="sxs-lookup"><span data-stu-id="19d24-121">From time of the query</span></span>

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

### <span data-ttu-id="19d24-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="19d24-122">-GroupByOperationName</span></span>
<span data-ttu-id="19d24-123">Risultato della query di gruppo per nome operazione.</span><span class="sxs-lookup"><span data-stu-id="19d24-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="19d24-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="19d24-124">-GroupByResourceName</span></span>
<span data-ttu-id="19d24-125">Risultato della query di gruppo per nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="19d24-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="19d24-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="19d24-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="19d24-127">Risultato della query di gruppo per criteri di limitazione applicati.</span><span class="sxs-lookup"><span data-stu-id="19d24-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="19d24-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="19d24-128">-Location</span></span>
<span data-ttu-id="19d24-129">Posizione in cui viene eseguita la query su analisi log.</span><span class="sxs-lookup"><span data-stu-id="19d24-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="19d24-130">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="19d24-130">-NoWait</span></span>
<span data-ttu-id="19d24-131">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="19d24-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="19d24-132">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="19d24-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="19d24-133">-ToTime</span><span class="sxs-lookup"><span data-stu-id="19d24-133">-ToTime</span></span>
<span data-ttu-id="19d24-134">Per l'ora della query</span><span class="sxs-lookup"><span data-stu-id="19d24-134">To time of the query</span></span>

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

### <span data-ttu-id="19d24-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19d24-135">-Confirm</span></span>
<span data-ttu-id="19d24-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19d24-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19d24-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19d24-137">-WhatIf</span></span>
<span data-ttu-id="19d24-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19d24-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19d24-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19d24-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19d24-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d24-140">CommonParameters</span></span>
<span data-ttu-id="19d24-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19d24-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d24-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19d24-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d24-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19d24-143">INPUTS</span></span>

### <span data-ttu-id="19d24-144">System. String</span><span class="sxs-lookup"><span data-stu-id="19d24-144">System.String</span></span>

## <span data-ttu-id="19d24-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19d24-145">OUTPUTS</span></span>

### <span data-ttu-id="19d24-146">Microsoft. Azure. Commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="19d24-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="19d24-147">Note</span><span class="sxs-lookup"><span data-stu-id="19d24-147">NOTES</span></span>

## <span data-ttu-id="19d24-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19d24-148">RELATED LINKS</span></span>
