---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 2C8C98B8-7A3B-4F24-BDF1-0B7B81049956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 2142c0f70379b646cb671ae95e2b6bbdd45e21a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511456"
---
# <span data-ttu-id="7c8f3-101">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="7c8f3-101">Set-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="7c8f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8f3-103">Modifica un processo di Accodamento bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-103">Modifies a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c8f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c8f3-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> [-ServiceBusQueueName <String>] -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c8f3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c8f3-105">DESCRIPTION</span></span>
<span data-ttu-id="7c8f3-106">Il cmdlet **set-AzureRmSchedulerServiceBusQueueJob** modifica un processo in coda di Service Bus in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-106">The **Set-AzureRmSchedulerServiceBusQueueJob** cmdlet modifies a service bus queue job in Azure Scheduler.</span></span>
<span data-ttu-id="7c8f3-107">Questo cmdlet supporta i parametri dinamici basati sul parametro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="7c8f3-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="7c8f3-108">I parametri dinamici diventano disponibili in base ad altri valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="7c8f3-109">Per individuare i nomi dei parametri dinamici dopo avere specificato gli altri parametri, digitare un segno meno (-) e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7c8f3-110">Se si omette un parametro obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7c8f3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c8f3-111">EXAMPLES</span></span>

## <span data-ttu-id="7c8f3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c8f3-112">PARAMETERS</span></span>

### <span data-ttu-id="7c8f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8f3-113">-DefaultProfile</span></span>
<span data-ttu-id="7c8f3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c8f3-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7c8f3-115">-EndTime</span></span>
<span data-ttu-id="7c8f3-116">Specifica un'ora di fine, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="7c8f3-117">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="7c8f3-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="7c8f3-118">-ErrorActionType</span></span>
<span data-ttu-id="7c8f3-119">Specifica un'impostazione di azione di errore per il processo.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="7c8f3-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c8f3-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c8f3-121">Http</span><span class="sxs-lookup"><span data-stu-id="7c8f3-121">Http</span></span> 
- <span data-ttu-id="7c8f3-122">Https</span><span class="sxs-lookup"><span data-stu-id="7c8f3-122">Https</span></span> 
- <span data-ttu-id="7c8f3-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="7c8f3-123">StorageQueue</span></span> 
- <span data-ttu-id="7c8f3-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="7c8f3-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="7c8f3-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="7c8f3-125">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="7c8f3-126">-ExecutionCount</span></span>
<span data-ttu-id="7c8f3-127">Specifica il numero di volte in cui il processo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="7c8f3-128">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-129">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="7c8f3-129">-Frequency</span></span>
<span data-ttu-id="7c8f3-130">Specifica una frequenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="7c8f3-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c8f3-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c8f3-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="7c8f3-132">Minute</span></span> 
- <span data-ttu-id="7c8f3-133">Ora</span><span class="sxs-lookup"><span data-stu-id="7c8f3-133">Hour</span></span> 
- <span data-ttu-id="7c8f3-134">Giorno</span><span class="sxs-lookup"><span data-stu-id="7c8f3-134">Day</span></span> 
- <span data-ttu-id="7c8f3-135">Settimana</span><span class="sxs-lookup"><span data-stu-id="7c8f3-135">Week</span></span> 
- <span data-ttu-id="7c8f3-136">Mese</span><span class="sxs-lookup"><span data-stu-id="7c8f3-136">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-137">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="7c8f3-137">-Interval</span></span>
<span data-ttu-id="7c8f3-138">Specifica un intervallo di ricorrenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="7c8f3-139">-JobCollectionName</span></span>
<span data-ttu-id="7c8f3-140">Specifica il nome della raccolta processi a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="7c8f3-141">-JobName</span></span>
<span data-ttu-id="7c8f3-142">Specifica il nome del processo modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-142">Specifies the name of the job that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="7c8f3-143">-JobState</span></span>
<span data-ttu-id="7c8f3-144">Specifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-144">Specifies the state of the job.</span></span>
<span data-ttu-id="7c8f3-145">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c8f3-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c8f3-146">Abilitato</span><span class="sxs-lookup"><span data-stu-id="7c8f3-146">Enabled</span></span> 
- <span data-ttu-id="7c8f3-147">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="7c8f3-147">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c8f3-148">-ResourceGroupName</span></span>
<span data-ttu-id="7c8f3-149">Specifica il gruppo di risorse a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-149">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="7c8f3-150">-ServiceBusMessage</span></span>
<span data-ttu-id="7c8f3-151">Specifica un messaggio della coda di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-151">Specifies a service bus queue message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="7c8f3-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="7c8f3-153">Specifica uno spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-153">Specifies a service bus namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="7c8f3-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="7c8f3-155">Specifica un nome di coda di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-155">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="7c8f3-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="7c8f3-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="7c8f3-157">Specifica un nome di chiave della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-157">Specifies a shared access signature key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="7c8f3-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="7c8f3-159">Specifica un valore di chiave della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-159">Specifies a shared access signature key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="7c8f3-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="7c8f3-161">Specifica un tipo di trasporto bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="7c8f3-162">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c8f3-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7c8f3-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="7c8f3-163">NetMessaging</span></span> 
- <span data-ttu-id="7c8f3-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="7c8f3-164">AMQP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7c8f3-165">-StartTime</span></span>
<span data-ttu-id="7c8f3-166">Specifica l'ora di inizio, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="7c8f3-167">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c8f3-167">-Confirm</span></span>
<span data-ttu-id="7c8f3-168">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c8f3-169">-WhatIf</span></span>
<span data-ttu-id="7c8f3-170">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c8f3-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-171">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8f3-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8f3-172">CommonParameters</span></span>
<span data-ttu-id="7c8f3-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c8f3-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8f3-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c8f3-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8f3-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c8f3-175">INPUTS</span></span>

### <span data-ttu-id="7c8f3-176">System. String</span><span class="sxs-lookup"><span data-stu-id="7c8f3-176">System.String</span></span>

## <span data-ttu-id="7c8f3-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c8f3-177">OUTPUTS</span></span>

### <span data-ttu-id="7c8f3-178">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="7c8f3-178">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="7c8f3-179">Note</span><span class="sxs-lookup"><span data-stu-id="7c8f3-179">NOTES</span></span>

## <span data-ttu-id="7c8f3-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c8f3-180">RELATED LINKS</span></span>

[<span data-ttu-id="7c8f3-181">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="7c8f3-181">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="7c8f3-182">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7c8f3-182">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7c8f3-183">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="7c8f3-183">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="7c8f3-184">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="7c8f3-184">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="7c8f3-185">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="7c8f3-185">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="7c8f3-186">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="7c8f3-186">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="7c8f3-187">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="7c8f3-187">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="7c8f3-188">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="7c8f3-188">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="7c8f3-189">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="7c8f3-189">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


