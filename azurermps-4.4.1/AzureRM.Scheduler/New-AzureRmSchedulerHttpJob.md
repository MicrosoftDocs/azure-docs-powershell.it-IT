---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: E00D42D6-707A-479E-9964-C5B80D3DAA6A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerHttpJob.md
ms.openlocfilehash: 5fc591ff5d24211b8af464dab46bfb81360f83e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687087"
---
# <span data-ttu-id="10017-101">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="10017-101">New-AzureRmSchedulerHttpJob</span></span>

## <span data-ttu-id="10017-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10017-102">SYNOPSIS</span></span>
<span data-ttu-id="10017-103">Crea un processo HTTP.</span><span class="sxs-lookup"><span data-stu-id="10017-103">Creates an HTTP job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10017-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10017-104">SYNTAX</span></span>

```
New-AzureRmSchedulerHttpJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -Method <String> -Uri <Uri> [-RequestBody <String>] [-Headers <Hashtable>] [-HttpAuthenticationType <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10017-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10017-105">DESCRIPTION</span></span>
<span data-ttu-id="10017-106">Il cmdlet **New-AzureRmSchedulerHttpJob** crea un processo http in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="10017-106">The **New-AzureRmSchedulerHttpJob** cmdlet creates an HTTP job in Azure Scheduler.</span></span>

<span data-ttu-id="10017-107">Questo cmdlet supporta i parametri dinamici basati sui parametri *ErrorActionType* e *HttpAuthenticationType* .</span><span class="sxs-lookup"><span data-stu-id="10017-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* and *HttpAuthenticationType* parameters.</span></span>
<span data-ttu-id="10017-108">I parametri dinamici diventano disponibili in base ad altri valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="10017-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="10017-109">Per individuare i nomi dei parametri dinamici dopo avere specificato gli altri parametri, digitare un segno meno (-) e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="10017-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="10017-110">Se si omette un parametro obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="10017-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="10017-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10017-111">EXAMPLES</span></span>

## <span data-ttu-id="10017-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10017-112">PARAMETERS</span></span>

### <span data-ttu-id="10017-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="10017-113">-EndTime</span></span>
<span data-ttu-id="10017-114">Specifica un'ora di fine, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="10017-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="10017-115">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="10017-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="10017-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="10017-116">-ErrorActionType</span></span>
<span data-ttu-id="10017-117">Specifica un'impostazione di azione di errore per il processo.</span><span class="sxs-lookup"><span data-stu-id="10017-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="10017-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="10017-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10017-119">Http</span><span class="sxs-lookup"><span data-stu-id="10017-119">Http</span></span> 
- <span data-ttu-id="10017-120">Https</span><span class="sxs-lookup"><span data-stu-id="10017-120">Https</span></span> 
- <span data-ttu-id="10017-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="10017-121">StorageQueue</span></span> 
- <span data-ttu-id="10017-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="10017-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="10017-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="10017-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="10017-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="10017-124">-ExecutionCount</span></span>
<span data-ttu-id="10017-125">Specifica il numero di volte in cui il processo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10017-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="10017-126">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="10017-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="10017-127">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="10017-127">-Frequency</span></span>
<span data-ttu-id="10017-128">Specifica una frequenza massima per il processo.</span><span class="sxs-lookup"><span data-stu-id="10017-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="10017-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="10017-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10017-130">Minuto</span><span class="sxs-lookup"><span data-stu-id="10017-130">Minute</span></span> 
- <span data-ttu-id="10017-131">Ora</span><span class="sxs-lookup"><span data-stu-id="10017-131">Hour</span></span> 
- <span data-ttu-id="10017-132">Giorno</span><span class="sxs-lookup"><span data-stu-id="10017-132">Day</span></span> 
- <span data-ttu-id="10017-133">Settimana</span><span class="sxs-lookup"><span data-stu-id="10017-133">Week</span></span> 
- <span data-ttu-id="10017-134">Mese</span><span class="sxs-lookup"><span data-stu-id="10017-134">Month</span></span>

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

### <span data-ttu-id="10017-135">-Intestazioni</span><span class="sxs-lookup"><span data-stu-id="10017-135">-Headers</span></span>
<span data-ttu-id="10017-136">Specifica una tabella hash che contiene le intestazioni.</span><span class="sxs-lookup"><span data-stu-id="10017-136">Specifies a hash table that contains headers.</span></span>

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

### <span data-ttu-id="10017-137">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="10017-137">-HttpAuthenticationType</span></span>
<span data-ttu-id="10017-138">Specifica il tipo di autenticazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="10017-138">Specifies the HTTP authentication type.</span></span>
<span data-ttu-id="10017-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="10017-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10017-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="10017-140">None</span></span> 
- <span data-ttu-id="10017-141">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="10017-141">ClientCertificate</span></span> 
- <span data-ttu-id="10017-142">ActiveDirectoryOAuth</span><span class="sxs-lookup"><span data-stu-id="10017-142">ActiveDirectoryOAuth</span></span> 
- <span data-ttu-id="10017-143">Base</span><span class="sxs-lookup"><span data-stu-id="10017-143">Basic</span></span>

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

### <span data-ttu-id="10017-144">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="10017-144">-Interval</span></span>
<span data-ttu-id="10017-145">Specifica un intervallo di ricorrenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="10017-145">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="10017-146">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="10017-146">-JobCollectionName</span></span>
<span data-ttu-id="10017-147">Specifica il nome della raccolta processi a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="10017-147">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="10017-148">-JobName</span><span class="sxs-lookup"><span data-stu-id="10017-148">-JobName</span></span>
<span data-ttu-id="10017-149">Specifica un nome per il processo.</span><span class="sxs-lookup"><span data-stu-id="10017-149">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="10017-150">-JobState</span><span class="sxs-lookup"><span data-stu-id="10017-150">-JobState</span></span>
<span data-ttu-id="10017-151">Specifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="10017-151">Specifies the state of the job.</span></span>
<span data-ttu-id="10017-152">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="10017-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10017-153">Abilitato</span><span class="sxs-lookup"><span data-stu-id="10017-153">Enabled</span></span> 
- <span data-ttu-id="10017-154">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="10017-154">Disabled</span></span>

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

### <span data-ttu-id="10017-155">-Method</span><span class="sxs-lookup"><span data-stu-id="10017-155">-Method</span></span>
<span data-ttu-id="10017-156">Specifica il metodo per i tipi di azione per il processo.</span><span class="sxs-lookup"><span data-stu-id="10017-156">Specifies the method for the action types for the job.</span></span>
<span data-ttu-id="10017-157">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="10017-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10017-158">Ottieni</span><span class="sxs-lookup"><span data-stu-id="10017-158">GET</span></span> 
- <span data-ttu-id="10017-159">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="10017-159">PUT</span></span> 
- <span data-ttu-id="10017-160">Inserisci</span><span class="sxs-lookup"><span data-stu-id="10017-160">POST</span></span> 
- <span data-ttu-id="10017-161">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="10017-161">DELETE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: GET, PUT, POST, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10017-162">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="10017-162">-RequestBody</span></span>
<span data-ttu-id="10017-163">Specifica il valore del corpo per le azioni di inserimento e POST-lavoro.</span><span class="sxs-lookup"><span data-stu-id="10017-163">Specifies the value of the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="10017-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10017-164">-ResourceGroupName</span></span>
<span data-ttu-id="10017-165">Specifica il gruppo di risorse a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="10017-165">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="10017-166">-StartTime</span><span class="sxs-lookup"><span data-stu-id="10017-166">-StartTime</span></span>
<span data-ttu-id="10017-167">Specifica l'ora di inizio, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="10017-167">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="10017-168">-URI</span><span class="sxs-lookup"><span data-stu-id="10017-168">-Uri</span></span>
<span data-ttu-id="10017-169">Specifica un URI per l'azione lavoro.</span><span class="sxs-lookup"><span data-stu-id="10017-169">Specifies a URI for the job action.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10017-170">-Confermare</span><span class="sxs-lookup"><span data-stu-id="10017-170">-Confirm</span></span>
<span data-ttu-id="10017-171">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10017-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10017-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10017-172">-WhatIf</span></span>
<span data-ttu-id="10017-173">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10017-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10017-174">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10017-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10017-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10017-175">-DefaultProfile</span></span>
<span data-ttu-id="10017-176">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10017-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10017-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10017-177">CommonParameters</span></span>
<span data-ttu-id="10017-178">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10017-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10017-179">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10017-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10017-180">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10017-180">INPUTS</span></span>

## <span data-ttu-id="10017-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10017-181">OUTPUTS</span></span>

### <span data-ttu-id="10017-182">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="10017-182">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="10017-183">Note</span><span class="sxs-lookup"><span data-stu-id="10017-183">NOTES</span></span>

## <span data-ttu-id="10017-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10017-184">RELATED LINKS</span></span>

[<span data-ttu-id="10017-185">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="10017-185">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="10017-186">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="10017-186">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="10017-187">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="10017-187">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="10017-188">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="10017-188">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="10017-189">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="10017-189">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="10017-190">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="10017-190">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="10017-191">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="10017-191">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="10017-192">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="10017-192">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="10017-193">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="10017-193">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


