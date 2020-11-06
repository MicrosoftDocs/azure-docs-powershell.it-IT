---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerservicebustopicjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: 7da7382359202f3856309c24a3ea484bd9b3e9e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509640"
---
# <span data-ttu-id="60e63-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="60e63-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="60e63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60e63-102">SYNOPSIS</span></span>
<span data-ttu-id="60e63-103">Modifica il processo di un argomento di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="60e63-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60e63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60e63-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60e63-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60e63-105">DESCRIPTION</span></span>
<span data-ttu-id="60e63-106">Il cmdlet **set-AzureRmSchedulerServiceBusTopicJob** modifica un processo di argomento di Service Bus in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="60e63-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="60e63-107">Questo cmdlet supporta i parametri dinamici basati sul parametro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="60e63-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="60e63-108">I parametri dinamici diventano disponibili in base ad altri valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="60e63-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="60e63-109">Per individuare i nomi dei parametri dinamici dopo avere specificato gli altri parametri, digitare un segno meno (-) e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="60e63-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="60e63-110">Se si omette un parametro obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="60e63-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="60e63-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60e63-111">EXAMPLES</span></span>

## <span data-ttu-id="60e63-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60e63-112">PARAMETERS</span></span>

### <span data-ttu-id="60e63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e63-113">-DefaultProfile</span></span>
<span data-ttu-id="60e63-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60e63-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60e63-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="60e63-115">-EndTime</span></span>
<span data-ttu-id="60e63-116">Specifica un'ora di fine, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="60e63-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="60e63-117">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="60e63-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="60e63-118">-ErrorActionType</span></span>
<span data-ttu-id="60e63-119">Specifica un'impostazione di azione di errore per il processo.</span><span class="sxs-lookup"><span data-stu-id="60e63-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="60e63-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="60e63-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="60e63-121">Http</span><span class="sxs-lookup"><span data-stu-id="60e63-121">Http</span></span> 
- <span data-ttu-id="60e63-122">Https</span><span class="sxs-lookup"><span data-stu-id="60e63-122">Https</span></span> 
- <span data-ttu-id="60e63-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="60e63-123">StorageQueue</span></span> 
- <span data-ttu-id="60e63-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="60e63-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="60e63-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="60e63-125">ServiceBusTopic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="60e63-126">-ExecutionCount</span></span>
<span data-ttu-id="60e63-127">Specifica il numero di volte in cui il processo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60e63-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="60e63-128">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="60e63-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-129">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="60e63-129">-Frequency</span></span>
<span data-ttu-id="60e63-130">Specifica una frequenza massima per il processo.</span><span class="sxs-lookup"><span data-stu-id="60e63-130">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="60e63-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="60e63-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="60e63-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="60e63-132">Minute</span></span> 
- <span data-ttu-id="60e63-133">Ora</span><span class="sxs-lookup"><span data-stu-id="60e63-133">Hour</span></span> 
- <span data-ttu-id="60e63-134">Giorno</span><span class="sxs-lookup"><span data-stu-id="60e63-134">Day</span></span> 
- <span data-ttu-id="60e63-135">Settimana</span><span class="sxs-lookup"><span data-stu-id="60e63-135">Week</span></span> 
- <span data-ttu-id="60e63-136">Mese</span><span class="sxs-lookup"><span data-stu-id="60e63-136">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-137">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="60e63-137">-Interval</span></span>
<span data-ttu-id="60e63-138">Specifica un intervallo di ricorrenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="60e63-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="60e63-139">-JobCollectionName</span></span>
<span data-ttu-id="60e63-140">Specifica il nome della raccolta processi a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="60e63-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="60e63-141">-JobName</span></span>
<span data-ttu-id="60e63-142">Specifica il nome del processo modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60e63-142">Specifies the name of the job that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="60e63-143">-JobState</span></span>
<span data-ttu-id="60e63-144">Specifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="60e63-144">Specifies the state of the job.</span></span>
<span data-ttu-id="60e63-145">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="60e63-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="60e63-146">Abilitato</span><span class="sxs-lookup"><span data-stu-id="60e63-146">Enabled</span></span> 
- <span data-ttu-id="60e63-147">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="60e63-147">Disabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60e63-148">-ResourceGroupName</span></span>
<span data-ttu-id="60e63-149">Specifica il gruppo di risorse a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="60e63-149">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="60e63-150">-ServiceBusMessage</span></span>
<span data-ttu-id="60e63-151">Specifica un messaggio di argomento Service Bus.</span><span class="sxs-lookup"><span data-stu-id="60e63-151">Specifies a service bus topic message.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="60e63-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="60e63-153">Specifica uno spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="60e63-153">Specifies a service bus namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="60e63-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="60e63-155">Specifica un nome di chiave della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="60e63-155">Specifies a shared access signature key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="60e63-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="60e63-157">Specifica un valore di chiave della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="60e63-157">Specifies a shared access signature key value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-158">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="60e63-158">-ServiceBusTopicPath</span></span>
<span data-ttu-id="60e63-159">Specifica il percorso di un argomento di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="60e63-159">Specifies a service bus topic path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="60e63-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="60e63-161">Specifica un tipo di trasporto bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="60e63-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="60e63-162">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="60e63-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="60e63-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="60e63-163">NetMessaging</span></span>
- <span data-ttu-id="60e63-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="60e63-164">AMQP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="60e63-165">-StartTime</span></span>
<span data-ttu-id="60e63-166">Specifica l'ora di inizio, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="60e63-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-167">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60e63-167">-Confirm</span></span>
<span data-ttu-id="60e63-168">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60e63-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e63-169">-WhatIf</span></span>
<span data-ttu-id="60e63-170">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60e63-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60e63-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60e63-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e63-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e63-172">CommonParameters</span></span>
<span data-ttu-id="60e63-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60e63-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e63-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60e63-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e63-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60e63-175">INPUTS</span></span>

### <span data-ttu-id="60e63-176">Nessuno</span><span class="sxs-lookup"><span data-stu-id="60e63-176">None</span></span>
<span data-ttu-id="60e63-177">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="60e63-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60e63-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60e63-178">OUTPUTS</span></span>

### <span data-ttu-id="60e63-179">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="60e63-179">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="60e63-180">Note</span><span class="sxs-lookup"><span data-stu-id="60e63-180">NOTES</span></span>

## <span data-ttu-id="60e63-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60e63-181">RELATED LINKS</span></span>

[<span data-ttu-id="60e63-182">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="60e63-182">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="60e63-183">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="60e63-183">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="60e63-184">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="60e63-184">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="60e63-185">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="60e63-185">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="60e63-186">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="60e63-186">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="60e63-187">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="60e63-187">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="60e63-188">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="60e63-188">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="60e63-189">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="60e63-189">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="60e63-190">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="60e63-190">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


