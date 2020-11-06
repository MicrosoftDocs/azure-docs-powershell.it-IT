---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: D9FA686C-48BB-48A1-926C-56B8151F8F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/set-azurermschedulerhttpjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 2810a73e54151d8227a115aa71f486d09811def8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511468"
---
# <span data-ttu-id="4d42e-101">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4d42e-101">Set-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="4d42e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d42e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d42e-103">Modifica un processo HTTP dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4d42e-103">Modifies a Scheduler HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d42e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d42e-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-Method <String>] [-Uri <Uri>] [-RequestBody <String>] [-Headers <Hashtable>]
 [-HttpAuthenticationType <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d42e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d42e-105">DESCRIPTION</span></span>
<span data-ttu-id="4d42e-106">Il cmdlet **set-AzureRmSchedulerHttpJob** modifica un processo http in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="4d42e-106">The **Set-AzureRmSchedulerHttpJob** cmdlet modifies an HTTP job in Azure Scheduler.</span></span>
<span data-ttu-id="4d42e-107">Questo cmdlet supporta i parametri dinamici basati sui parametri *ErrorActionType* e *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="4d42e-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="4d42e-108">I parametri dinamici diventano disponibili in base ad altri valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="4d42e-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="4d42e-109">Per individuare i nomi dei parametri dinamici dopo avere specificato gli altri parametri, digitare un segno meno (-) e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="4d42e-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4d42e-110">Se si omette un parametro obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="4d42e-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4d42e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d42e-111">EXAMPLES</span></span>

## <span data-ttu-id="4d42e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d42e-112">PARAMETERS</span></span>

### <span data-ttu-id="4d42e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d42e-113">-DefaultProfile</span></span>
<span data-ttu-id="4d42e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d42e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d42e-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4d42e-115">-EndTime</span></span>
<span data-ttu-id="4d42e-116">Specifica un'ora di fine, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="4d42e-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="4d42e-117">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="4d42e-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="4d42e-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="4d42e-118">-ErrorActionType</span></span>
<span data-ttu-id="4d42e-119">Specifica un'impostazione di azione di errore per il processo.</span><span class="sxs-lookup"><span data-stu-id="4d42e-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="4d42e-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d42e-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d42e-121">Http</span><span class="sxs-lookup"><span data-stu-id="4d42e-121">Http</span></span> 
- <span data-ttu-id="4d42e-122">Https</span><span class="sxs-lookup"><span data-stu-id="4d42e-122">Https</span></span> 
- <span data-ttu-id="4d42e-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="4d42e-123">StorageQueue</span></span> 
- <span data-ttu-id="4d42e-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="4d42e-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="4d42e-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="4d42e-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="4d42e-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="4d42e-126">-ExecutionCount</span></span>
<span data-ttu-id="4d42e-127">Specifica il numero di volte in cui il processo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d42e-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="4d42e-128">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="4d42e-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="4d42e-129">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="4d42e-129">-Frequency</span></span>
<span data-ttu-id="4d42e-130">Specifica la frequenza massima per il processo.</span><span class="sxs-lookup"><span data-stu-id="4d42e-130">Specifies the maximum frequency for the job.</span></span>
<span data-ttu-id="4d42e-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d42e-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d42e-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="4d42e-132">Minute</span></span> 
- <span data-ttu-id="4d42e-133">Ora</span><span class="sxs-lookup"><span data-stu-id="4d42e-133">Hour</span></span> 
- <span data-ttu-id="4d42e-134">Giorno</span><span class="sxs-lookup"><span data-stu-id="4d42e-134">Day</span></span> 
- <span data-ttu-id="4d42e-135">Settimana</span><span class="sxs-lookup"><span data-stu-id="4d42e-135">Week</span></span> 
- <span data-ttu-id="4d42e-136">Mese</span><span class="sxs-lookup"><span data-stu-id="4d42e-136">Month</span></span>

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

### <span data-ttu-id="4d42e-137">-Intestazioni</span><span class="sxs-lookup"><span data-stu-id="4d42e-137">-Headers</span></span>
<span data-ttu-id="4d42e-138">Specifica una tabella hash che contiene le intestazioni.</span><span class="sxs-lookup"><span data-stu-id="4d42e-138">Specifies a hash table that contains headers.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d42e-139">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="4d42e-139">-HttpAuthenticationType</span></span>
<span data-ttu-id="4d42e-140">Specifica il tipo di autenticazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d42e-140">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="4d42e-141">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d42e-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d42e-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4d42e-142">None</span></span> 
- <span data-ttu-id="4d42e-143">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4d42e-143">ClientCertificate</span></span> 
- <span data-ttu-id="4d42e-144">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="4d42e-144">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="4d42e-145">Base</span><span class="sxs-lookup"><span data-stu-id="4d42e-145">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, ClientCertificate, ActiveDirectoryOAuth, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d42e-146">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="4d42e-146">-Interval</span></span>
<span data-ttu-id="4d42e-147">Specifica un intervallo di ricorrenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="4d42e-147">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="4d42e-148">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="4d42e-148">-JobCollectionName</span></span>
<span data-ttu-id="4d42e-149">Specifica il nome della raccolta processi a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="4d42e-149">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="4d42e-150">-JobName</span><span class="sxs-lookup"><span data-stu-id="4d42e-150">-JobName</span></span>
<span data-ttu-id="4d42e-151">Specifica il nome del processo modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d42e-151">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4d42e-152">-JobState</span><span class="sxs-lookup"><span data-stu-id="4d42e-152">-JobState</span></span>
<span data-ttu-id="4d42e-153">Specifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="4d42e-153">Specifies the state of the job.</span></span>
<span data-ttu-id="4d42e-154">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d42e-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d42e-155">Abilitato</span><span class="sxs-lookup"><span data-stu-id="4d42e-155">Enabled</span></span> 
- <span data-ttu-id="4d42e-156">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="4d42e-156">Disabled</span></span>

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

### <span data-ttu-id="4d42e-157">-Method</span><span class="sxs-lookup"><span data-stu-id="4d42e-157">-Method</span></span>
<span data-ttu-id="4d42e-158">Specifica il metodo per i tipi di azione per questo processo.</span><span class="sxs-lookup"><span data-stu-id="4d42e-158">Specifies the method for the action types for this job.</span></span>
<span data-ttu-id="4d42e-159">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d42e-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4d42e-160">Ottieni</span><span class="sxs-lookup"><span data-stu-id="4d42e-160">GET</span></span> 
- <span data-ttu-id="4d42e-161">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="4d42e-161">PUT</span></span> 
- <span data-ttu-id="4d42e-162">Inserisci</span><span class="sxs-lookup"><span data-stu-id="4d42e-162">POST</span></span> 
- <span data-ttu-id="4d42e-163">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="4d42e-163">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, PUT, POST, DELETE

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d42e-164">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="4d42e-164">-RequestBody</span></span>
<span data-ttu-id="4d42e-165">Specifica il valore del corpo per le azioni di inserimento e POST-lavoro.</span><span class="sxs-lookup"><span data-stu-id="4d42e-165">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="4d42e-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d42e-166">-ResourceGroupName</span></span>
<span data-ttu-id="4d42e-167">Specifica il gruppo di risorse a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="4d42e-167">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="4d42e-168">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4d42e-168">-StartTime</span></span>
<span data-ttu-id="4d42e-169">Specifica l'ora di inizio, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="4d42e-169">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="4d42e-170">-URI</span><span class="sxs-lookup"><span data-stu-id="4d42e-170">-Uri</span></span>
<span data-ttu-id="4d42e-171">Specifica un URI per l'azione lavoro.</span><span class="sxs-lookup"><span data-stu-id="4d42e-171">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d42e-172">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d42e-172">-Confirm</span></span>
<span data-ttu-id="4d42e-173">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d42e-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d42e-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d42e-174">-WhatIf</span></span>
<span data-ttu-id="4d42e-175">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d42e-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d42e-176">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d42e-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d42e-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d42e-177">CommonParameters</span></span>
<span data-ttu-id="4d42e-178">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d42e-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d42e-179">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d42e-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d42e-180">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d42e-180">INPUTS</span></span>

### <span data-ttu-id="4d42e-181">System. String</span><span class="sxs-lookup"><span data-stu-id="4d42e-181">System.String</span></span>

### <span data-ttu-id="4d42e-182">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4d42e-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4d42e-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d42e-183">OUTPUTS</span></span>

### <span data-ttu-id="4d42e-184">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="4d42e-184">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="4d42e-185">Note</span><span class="sxs-lookup"><span data-stu-id="4d42e-185">NOTES</span></span>

## <span data-ttu-id="4d42e-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d42e-186">RELATED LINKS</span></span>

[<span data-ttu-id="4d42e-187">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4d42e-187">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4d42e-188">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4d42e-188">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4d42e-189">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4d42e-189">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4d42e-190">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4d42e-190">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="4d42e-191">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4d42e-191">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="4d42e-192">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4d42e-192">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4d42e-193">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4d42e-193">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4d42e-194">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4d42e-194">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="4d42e-195">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4d42e-195">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


