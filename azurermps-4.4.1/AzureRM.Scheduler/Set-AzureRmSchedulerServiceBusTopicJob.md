---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: a12cf84d90ecbcc948ac13745b38438766582aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521140"
---
# <span data-ttu-id="d4c95-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d4c95-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="d4c95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4c95-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c95-103">Modifica il processo di un argomento di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="d4c95-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4c95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4c95-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4c95-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4c95-105">DESCRIPTION</span></span>
<span data-ttu-id="d4c95-106">Il cmdlet **set-AzureRmSchedulerServiceBusTopicJob** modifica un processo di argomento di Service Bus in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="d4c95-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="d4c95-107">Questo cmdlet supporta i parametri dinamici basati sul parametro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="d4c95-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="d4c95-108">I parametri dinamici diventano disponibili in base ad altri valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="d4c95-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="d4c95-109">Per individuare i nomi dei parametri dinamici dopo avere specificato gli altri parametri, digitare un segno meno (-) e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="d4c95-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d4c95-110">Se si omette un parametro obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="d4c95-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d4c95-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4c95-111">EXAMPLES</span></span>

## <span data-ttu-id="d4c95-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4c95-112">PARAMETERS</span></span>

### <span data-ttu-id="d4c95-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d4c95-113">-EndTime</span></span>
<span data-ttu-id="d4c95-114">Specifica un'ora di fine, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="d4c95-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="d4c95-115">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="d4c95-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="d4c95-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="d4c95-116">-ErrorActionType</span></span>
<span data-ttu-id="d4c95-117">Specifica un'impostazione di azione di errore per il processo.</span><span class="sxs-lookup"><span data-stu-id="d4c95-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="d4c95-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4c95-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4c95-119">Http</span><span class="sxs-lookup"><span data-stu-id="d4c95-119">Http</span></span> 
- <span data-ttu-id="d4c95-120">Https</span><span class="sxs-lookup"><span data-stu-id="d4c95-120">Https</span></span> 
- <span data-ttu-id="d4c95-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="d4c95-121">StorageQueue</span></span> 
- <span data-ttu-id="d4c95-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d4c95-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="d4c95-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="d4c95-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="d4c95-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="d4c95-124">-ExecutionCount</span></span>
<span data-ttu-id="d4c95-125">Specifica il numero di volte in cui il processo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4c95-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="d4c95-126">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="d4c95-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="d4c95-127">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="d4c95-127">-Frequency</span></span>
<span data-ttu-id="d4c95-128">Specifica una frequenza massima per il processo.</span><span class="sxs-lookup"><span data-stu-id="d4c95-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="d4c95-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4c95-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4c95-130">Minuto</span><span class="sxs-lookup"><span data-stu-id="d4c95-130">Minute</span></span> 
- <span data-ttu-id="d4c95-131">Ora</span><span class="sxs-lookup"><span data-stu-id="d4c95-131">Hour</span></span> 
- <span data-ttu-id="d4c95-132">Giorno</span><span class="sxs-lookup"><span data-stu-id="d4c95-132">Day</span></span> 
- <span data-ttu-id="d4c95-133">Settimana</span><span class="sxs-lookup"><span data-stu-id="d4c95-133">Week</span></span> 
- <span data-ttu-id="d4c95-134">Mese</span><span class="sxs-lookup"><span data-stu-id="d4c95-134">Month</span></span>

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

### <span data-ttu-id="d4c95-135">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="d4c95-135">-Interval</span></span>
<span data-ttu-id="d4c95-136">Specifica un intervallo di ricorrenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="d4c95-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="d4c95-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="d4c95-137">-JobCollectionName</span></span>
<span data-ttu-id="d4c95-138">Specifica il nome della raccolta processi a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="d4c95-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="d4c95-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="d4c95-139">-JobName</span></span>
<span data-ttu-id="d4c95-140">Specifica il nome del processo modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4c95-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d4c95-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="d4c95-141">-JobState</span></span>
<span data-ttu-id="d4c95-142">Specifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="d4c95-142">Specifies the state of the job.</span></span>
<span data-ttu-id="d4c95-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4c95-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4c95-144">Abilitato</span><span class="sxs-lookup"><span data-stu-id="d4c95-144">Enabled</span></span> 
- <span data-ttu-id="d4c95-145">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="d4c95-145">Disabled</span></span>

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

### <span data-ttu-id="d4c95-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c95-146">-ResourceGroupName</span></span>
<span data-ttu-id="d4c95-147">Specifica il gruppo di risorse a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="d4c95-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="d4c95-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="d4c95-148">-ServiceBusMessage</span></span>
<span data-ttu-id="d4c95-149">Specifica un messaggio di argomento Service Bus.</span><span class="sxs-lookup"><span data-stu-id="d4c95-149">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="d4c95-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="d4c95-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="d4c95-151">Specifica uno spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="d4c95-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="d4c95-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="d4c95-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="d4c95-153">Specifica un nome di chiave della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="d4c95-153">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="d4c95-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="d4c95-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="d4c95-155">Specifica un valore di chiave della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="d4c95-155">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="d4c95-156">-ServiceBusTopicPath</span><span class="sxs-lookup"><span data-stu-id="d4c95-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="d4c95-157">Specifica il percorso di un argomento di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="d4c95-157">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="d4c95-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="d4c95-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="d4c95-159">Specifica un tipo di trasporto bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="d4c95-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="d4c95-160">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d4c95-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4c95-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="d4c95-161">NetMessaging</span></span>
- <span data-ttu-id="d4c95-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="d4c95-162">AMQP</span></span>

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

### <span data-ttu-id="d4c95-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d4c95-163">-StartTime</span></span>
<span data-ttu-id="d4c95-164">Specifica l'ora di inizio, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="d4c95-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="d4c95-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d4c95-165">-Confirm</span></span>
<span data-ttu-id="d4c95-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4c95-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4c95-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4c95-167">-WhatIf</span></span>
<span data-ttu-id="d4c95-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4c95-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4c95-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4c95-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4c95-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c95-170">-DefaultProfile</span></span>
<span data-ttu-id="d4c95-171">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c95-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4c95-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c95-172">CommonParameters</span></span>
<span data-ttu-id="d4c95-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4c95-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c95-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4c95-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c95-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4c95-175">INPUTS</span></span>

## <span data-ttu-id="d4c95-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4c95-176">OUTPUTS</span></span>

### <span data-ttu-id="d4c95-177">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d4c95-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="d4c95-178">Note</span><span class="sxs-lookup"><span data-stu-id="d4c95-178">NOTES</span></span>

## <span data-ttu-id="d4c95-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4c95-179">RELATED LINKS</span></span>

[<span data-ttu-id="d4c95-180">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d4c95-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d4c95-181">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d4c95-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d4c95-182">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d4c95-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d4c95-183">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="d4c95-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="d4c95-184">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d4c95-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="d4c95-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="d4c95-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="d4c95-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="d4c95-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="d4c95-187">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="d4c95-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="d4c95-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="d4c95-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


