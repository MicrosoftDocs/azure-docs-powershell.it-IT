---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 2C8C98B8-7A3B-4F24-BDF1-0B7B81049956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 6928347ab5d78a25d53636f73413f772b9beea4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521528"
---
# <span data-ttu-id="a0d99-101">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a0d99-101">Set-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="a0d99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0d99-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d99-103">Modifica un processo di Accodamento bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="a0d99-103">Modifies a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0d99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0d99-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> [-ServiceBusQueueName <String>] -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0d99-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0d99-105">DESCRIPTION</span></span>
<span data-ttu-id="a0d99-106">Il cmdlet **set-AzureRmSchedulerServiceBusQueueJob** modifica un processo in coda di Service Bus in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="a0d99-106">The **Set-AzureRmSchedulerServiceBusQueueJob** cmdlet modifies a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="a0d99-107">Questo cmdlet supporta i parametri dinamici basati sul parametro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="a0d99-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="a0d99-108">I parametri dinamici diventano disponibili in base ad altri valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="a0d99-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="a0d99-109">Per individuare i nomi dei parametri dinamici dopo avere specificato gli altri parametri, digitare un segno meno (-) e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="a0d99-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a0d99-110">Se si omette un parametro obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="a0d99-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a0d99-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0d99-111">EXAMPLES</span></span>

## <span data-ttu-id="a0d99-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0d99-112">PARAMETERS</span></span>

### <span data-ttu-id="a0d99-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a0d99-113">-EndTime</span></span>
<span data-ttu-id="a0d99-114">Specifica un'ora di fine, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="a0d99-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="a0d99-115">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="a0d99-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="a0d99-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="a0d99-116">-ErrorActionType</span></span>
<span data-ttu-id="a0d99-117">Specifica un'impostazione di azione di errore per il processo.</span><span class="sxs-lookup"><span data-stu-id="a0d99-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="a0d99-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0d99-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0d99-119">Http</span><span class="sxs-lookup"><span data-stu-id="a0d99-119">Http</span></span> 
- <span data-ttu-id="a0d99-120">Https</span><span class="sxs-lookup"><span data-stu-id="a0d99-120">Https</span></span> 
- <span data-ttu-id="a0d99-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="a0d99-121">StorageQueue</span></span> 
- <span data-ttu-id="a0d99-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="a0d99-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="a0d99-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="a0d99-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="a0d99-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="a0d99-124">-ExecutionCount</span></span>
<span data-ttu-id="a0d99-125">Specifica il numero di volte in cui il processo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d99-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="a0d99-126">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="a0d99-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="a0d99-127">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="a0d99-127">-Frequency</span></span>
<span data-ttu-id="a0d99-128">Specifica una frequenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="a0d99-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="a0d99-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0d99-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0d99-130">Minuto</span><span class="sxs-lookup"><span data-stu-id="a0d99-130">Minute</span></span> 
- <span data-ttu-id="a0d99-131">Ora</span><span class="sxs-lookup"><span data-stu-id="a0d99-131">Hour</span></span> 
- <span data-ttu-id="a0d99-132">Giorno</span><span class="sxs-lookup"><span data-stu-id="a0d99-132">Day</span></span> 
- <span data-ttu-id="a0d99-133">Settimana</span><span class="sxs-lookup"><span data-stu-id="a0d99-133">Week</span></span> 
- <span data-ttu-id="a0d99-134">Mese</span><span class="sxs-lookup"><span data-stu-id="a0d99-134">Month</span></span>

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

### <span data-ttu-id="a0d99-135">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="a0d99-135">-Interval</span></span>
<span data-ttu-id="a0d99-136">Specifica un intervallo di ricorrenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="a0d99-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="a0d99-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="a0d99-137">-JobCollectionName</span></span>
<span data-ttu-id="a0d99-138">Specifica il nome della raccolta processi a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="a0d99-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="a0d99-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="a0d99-139">-JobName</span></span>
<span data-ttu-id="a0d99-140">Specifica il nome del processo modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0d99-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a0d99-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="a0d99-141">-JobState</span></span>
<span data-ttu-id="a0d99-142">Specifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="a0d99-142">Specifies the state of the job.</span></span>
<span data-ttu-id="a0d99-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0d99-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0d99-144">Abilitato</span><span class="sxs-lookup"><span data-stu-id="a0d99-144">Enabled</span></span> 
- <span data-ttu-id="a0d99-145">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="a0d99-145">Disabled</span></span>

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

### <span data-ttu-id="a0d99-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d99-146">-ResourceGroupName</span></span>
<span data-ttu-id="a0d99-147">Specifica il gruppo di risorse a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="a0d99-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="a0d99-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="a0d99-148">-ServiceBusMessage</span></span>
<span data-ttu-id="a0d99-149">Specifica un messaggio della coda di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="a0d99-149">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="a0d99-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="a0d99-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="a0d99-151">Specifica uno spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="a0d99-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="a0d99-152">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="a0d99-152">-ServiceBusQueueName</span></span>
<span data-ttu-id="a0d99-153">Specifica un nome di coda di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="a0d99-153">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="a0d99-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="a0d99-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="a0d99-155">Specifica un nome di chiave della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="a0d99-155">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="a0d99-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="a0d99-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="a0d99-157">Specifica un valore di chiave della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="a0d99-157">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="a0d99-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="a0d99-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="a0d99-159">Specifica un tipo di trasporto bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="a0d99-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="a0d99-160">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0d99-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a0d99-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="a0d99-161">NetMessaging</span></span> 
- <span data-ttu-id="a0d99-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="a0d99-162">AMQP</span></span>

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

### <span data-ttu-id="a0d99-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a0d99-163">-StartTime</span></span>
<span data-ttu-id="a0d99-164">Specifica l'ora di inizio, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="a0d99-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="a0d99-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0d99-165">-Confirm</span></span>
<span data-ttu-id="a0d99-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0d99-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0d99-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d99-167">-WhatIf</span></span>
<span data-ttu-id="a0d99-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d99-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d99-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d99-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0d99-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d99-170">-DefaultProfile</span></span>
<span data-ttu-id="a0d99-171">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d99-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0d99-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d99-172">CommonParameters</span></span>
<span data-ttu-id="a0d99-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d99-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d99-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d99-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d99-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0d99-175">INPUTS</span></span>

## <span data-ttu-id="a0d99-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0d99-176">OUTPUTS</span></span>

### <span data-ttu-id="a0d99-177">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a0d99-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="a0d99-178">Note</span><span class="sxs-lookup"><span data-stu-id="a0d99-178">NOTES</span></span>

## <span data-ttu-id="a0d99-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0d99-179">RELATED LINKS</span></span>

[<span data-ttu-id="a0d99-180">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a0d99-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="a0d99-181">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a0d99-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a0d99-182">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="a0d99-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="a0d99-183">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a0d99-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a0d99-184">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a0d99-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="a0d99-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="a0d99-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="a0d99-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="a0d99-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="a0d99-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="a0d99-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="a0d99-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="a0d99-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


