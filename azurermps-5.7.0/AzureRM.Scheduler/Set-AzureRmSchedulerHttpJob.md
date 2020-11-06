---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 9f43780cc7684c897b7b6d42e381e47f6ff8e106
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519861"
---
# <span data-ttu-id="aaf6b-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="aaf6b-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="aaf6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aaf6b-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf6b-103">Modifica un processo HTTP dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaf6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaf6b-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaf6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaf6b-105">DESCRIPTION</span></span>
<span data-ttu-id="aaf6b-106">Il cmdlet **set-AzureRmSchedulerHttpJob** modifica un processo http in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="aaf6b-107">Questo cmdlet supporta i parametri dinamici basati sui parametri *ErrorActionType* e *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="aaf6b-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="aaf6b-108">I parametri dinamici diventano disponibili in base ad altri valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="aaf6b-109">Per individuare i nomi dei parametri dinamici dopo avere specificato gli altri parametri, digitare un segno meno (-) e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="aaf6b-110">Se si omette un parametro obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="aaf6b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaf6b-111">EXAMPLES</span></span>

## <span data-ttu-id="aaf6b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aaf6b-112">PARAMETERS</span></span>

### <span data-ttu-id="aaf6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf6b-113">-DefaultProfile</span></span>
<span data-ttu-id="aaf6b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaf6b-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="aaf6b-115">-EndTime</span></span>
<span data-ttu-id="aaf6b-116">Specifica un'ora di fine, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="aaf6b-117">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="aaf6b-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="aaf6b-118">-ErrorActionType</span></span>
<span data-ttu-id="aaf6b-119">Specifica un'impostazione di azione di errore per il processo.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="aaf6b-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="aaf6b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aaf6b-121">Http</span><span class="sxs-lookup"><span data-stu-id="aaf6b-121">Http</span></span> 
- <span data-ttu-id="aaf6b-122">Https</span><span class="sxs-lookup"><span data-stu-id="aaf6b-122">Https</span></span> 
- <span data-ttu-id="aaf6b-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="aaf6b-123">StorageQueue</span></span> 
- <span data-ttu-id="aaf6b-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="aaf6b-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="aaf6b-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="aaf6b-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="aaf6b-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="aaf6b-126">-ExecutionCount</span></span>
<span data-ttu-id="aaf6b-127">Specifica il numero di volte in cui il processo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="aaf6b-128">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="aaf6b-129">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="aaf6b-129">-Frequency</span></span>
<span data-ttu-id="aaf6b-130">Specifica la frequenza massima per il processo.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-130">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="aaf6b-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="aaf6b-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aaf6b-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="aaf6b-132">Minute</span></span> 
- <span data-ttu-id="aaf6b-133">Ora</span><span class="sxs-lookup"><span data-stu-id="aaf6b-133">Hour</span></span> 
- <span data-ttu-id="aaf6b-134">Giorno</span><span class="sxs-lookup"><span data-stu-id="aaf6b-134">Day</span></span> 
- <span data-ttu-id="aaf6b-135">Settimana</span><span class="sxs-lookup"><span data-stu-id="aaf6b-135">Week</span></span> 
- <span data-ttu-id="aaf6b-136">Mese</span><span class="sxs-lookup"><span data-stu-id="aaf6b-136">Month</span></span>

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

### <span data-ttu-id="aaf6b-137">-Intestazioni</span><span class="sxs-lookup"><span data-stu-id="aaf6b-137">-Headers</span></span>
<span data-ttu-id="aaf6b-138">Specifica una tabella hash che contiene le intestazioni.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaf6b-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="aaf6b-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="aaf6b-140">Specifica il tipo di autenticazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="aaf6b-141">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="aaf6b-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aaf6b-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aaf6b-142">None</span></span> 
- <span data-ttu-id="aaf6b-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="aaf6b-143">ClientCertificate</span></span> 
- <span data-ttu-id="aaf6b-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="aaf6b-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="aaf6b-145">Base</span><span class="sxs-lookup"><span data-stu-id="aaf6b-145">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf6b-146">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="aaf6b-146">-Interval</span></span>
<span data-ttu-id="aaf6b-147">Specifica un intervallo di ricorrenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="aaf6b-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="aaf6b-148">-JobCollectionName</span></span>
<span data-ttu-id="aaf6b-149">Specifica il nome della raccolta processi a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="aaf6b-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="aaf6b-150">-JobName</span></span>
<span data-ttu-id="aaf6b-151">Specifica il nome del processo modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-151">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="aaf6b-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="aaf6b-152">-JobState</span></span>
<span data-ttu-id="aaf6b-153">Specifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-153">Specifies the state of the job.</span></span>
<span data-ttu-id="aaf6b-154">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="aaf6b-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aaf6b-155">Abilitato</span><span class="sxs-lookup"><span data-stu-id="aaf6b-155">Enabled</span></span> 
- <span data-ttu-id="aaf6b-156">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="aaf6b-156">Disabled</span></span>

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

### <span data-ttu-id="aaf6b-157">-Method</span><span class="sxs-lookup"><span data-stu-id="aaf6b-157">-Method</span></span>
<span data-ttu-id="aaf6b-158">Specifica il metodo per i tipi di azione per questo processo.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-158">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="aaf6b-159">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="aaf6b-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aaf6b-160">Ottieni</span><span class="sxs-lookup"><span data-stu-id="aaf6b-160">GET</span></span> 
- <span data-ttu-id="aaf6b-161">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="aaf6b-161">PUT</span></span> 
- <span data-ttu-id="aaf6b-162">Inserisci</span><span class="sxs-lookup"><span data-stu-id="aaf6b-162">POST</span></span> 
- <span data-ttu-id="aaf6b-163">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="aaf6b-163">DELETE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf6b-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="aaf6b-164">-RequestBody</span></span>
<span data-ttu-id="aaf6b-165">Specifica il valore del corpo per le azioni di inserimento e POST-lavoro.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-165">Specifies the value of the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf6b-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf6b-166">-ResourceGroupName</span></span>
<span data-ttu-id="aaf6b-167">Specifica il gruppo di risorse a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="aaf6b-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="aaf6b-168">-StartTime</span></span>
<span data-ttu-id="aaf6b-169">Specifica l'ora di inizio, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="aaf6b-170">-URI</span><span class="sxs-lookup"><span data-stu-id="aaf6b-170">-Uri</span></span>
<span data-ttu-id="aaf6b-171">Specifica un URI per l'azione lavoro.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-171">Specifies a URI for the job action.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf6b-172">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aaf6b-172">-Confirm</span></span>
<span data-ttu-id="aaf6b-173">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaf6b-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaf6b-174">-WhatIf</span></span>
<span data-ttu-id="aaf6b-175">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaf6b-176">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaf6b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf6b-177">CommonParameters</span></span>
<span data-ttu-id="aaf6b-178">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf6b-179">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf6b-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf6b-180">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aaf6b-180">INPUTS</span></span>

### <span data-ttu-id="aaf6b-181">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aaf6b-181">None</span></span>
<span data-ttu-id="aaf6b-182">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="aaf6b-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aaf6b-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaf6b-183">OUTPUTS</span></span>

### <span data-ttu-id="aaf6b-184">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="aaf6b-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="aaf6b-185">Note</span><span class="sxs-lookup"><span data-stu-id="aaf6b-185">NOTES</span></span>

## <span data-ttu-id="aaf6b-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaf6b-186">RELATED LINKS</span></span>

[<span data-ttu-id="aaf6b-187">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="aaf6b-187">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="aaf6b-188">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="aaf6b-188">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="aaf6b-189">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="aaf6b-189">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="aaf6b-190">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="aaf6b-190">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="aaf6b-191">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="aaf6b-191">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="aaf6b-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="aaf6b-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="aaf6b-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="aaf6b-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="aaf6b-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="aaf6b-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="aaf6b-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="aaf6b-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


