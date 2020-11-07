---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5563B6E8-805B-463B-AF78-4F5750F5CDEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: eb72b64576524d85730e89f6eece094591a12158
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520382"
---
# <span data-ttu-id="3665d-101">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="3665d-101">New-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="3665d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3665d-102">SYNOPSIS</span></span>
<span data-ttu-id="3665d-103">Crea un processo di Accodamento dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3665d-103">Creates a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3665d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3665d-104">SYNTAX</span></span>

```
New-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -StorageSASToken <String>
 -StorageQueueMessage <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3665d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3665d-105">DESCRIPTION</span></span>
<span data-ttu-id="3665d-106">Il cmdlet **New-AzureRmSchedulerStorageQueueJob** crea un processo di Accodamento dello spazio di archiviazione in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="3665d-106">The **New-AzureRmSchedulerStorageQueueJob** cmdlet creates a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="3665d-107">Questo cmdlet supporta i parametri dinamici basati sul parametro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="3665d-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="3665d-108">I parametri dinamici diventano disponibili in base ad altri valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="3665d-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="3665d-109">Per individuare i nomi dei parametri dinamici dopo avere specificato gli altri parametri, digitare un segno meno (-) e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="3665d-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3665d-110">Se si omette un parametro obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="3665d-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3665d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3665d-111">EXAMPLES</span></span>

## <span data-ttu-id="3665d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3665d-112">PARAMETERS</span></span>

### <span data-ttu-id="3665d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3665d-113">-DefaultProfile</span></span>
<span data-ttu-id="3665d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3665d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3665d-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3665d-115">-EndTime</span></span>
<span data-ttu-id="3665d-116">Specifica un'ora di fine, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="3665d-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="3665d-117">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="3665d-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="3665d-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="3665d-118">-ErrorActionType</span></span>
<span data-ttu-id="3665d-119">Specifica un'impostazione di azione di errore per il processo.</span><span class="sxs-lookup"><span data-stu-id="3665d-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="3665d-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3665d-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3665d-121">Http</span><span class="sxs-lookup"><span data-stu-id="3665d-121">Http</span></span> 
- <span data-ttu-id="3665d-122">Https</span><span class="sxs-lookup"><span data-stu-id="3665d-122">Https</span></span> 
- <span data-ttu-id="3665d-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="3665d-123">StorageQueue</span></span> 
- <span data-ttu-id="3665d-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="3665d-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="3665d-125">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="3665d-125">ServiceBusTopic</span></span>

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

### <span data-ttu-id="3665d-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="3665d-126">-ExecutionCount</span></span>
<span data-ttu-id="3665d-127">Specifica il numero di volte in cui il processo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3665d-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="3665d-128">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="3665d-128">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="3665d-129">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="3665d-129">-Frequency</span></span>
<span data-ttu-id="3665d-130">Specifica una frequenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="3665d-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="3665d-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3665d-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3665d-132">Minuto</span><span class="sxs-lookup"><span data-stu-id="3665d-132">Minute</span></span> 
- <span data-ttu-id="3665d-133">Ora</span><span class="sxs-lookup"><span data-stu-id="3665d-133">Hour</span></span> 
- <span data-ttu-id="3665d-134">Giorno</span><span class="sxs-lookup"><span data-stu-id="3665d-134">Day</span></span> 
- <span data-ttu-id="3665d-135">Settimana</span><span class="sxs-lookup"><span data-stu-id="3665d-135">Week</span></span> 
- <span data-ttu-id="3665d-136">Mese</span><span class="sxs-lookup"><span data-stu-id="3665d-136">Month</span></span>

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

### <span data-ttu-id="3665d-137">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="3665d-137">-Interval</span></span>
<span data-ttu-id="3665d-138">Specifica un intervallo di ricorrenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="3665d-138">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="3665d-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="3665d-139">-JobCollectionName</span></span>
<span data-ttu-id="3665d-140">Specifica il nome della raccolta processi a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="3665d-140">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="3665d-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="3665d-141">-JobName</span></span>
<span data-ttu-id="3665d-142">Specifica un nome per il processo.</span><span class="sxs-lookup"><span data-stu-id="3665d-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="3665d-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="3665d-143">-JobState</span></span>
<span data-ttu-id="3665d-144">Specifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="3665d-144">Specifies the state of the job.</span></span>
<span data-ttu-id="3665d-145">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3665d-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3665d-146">Abilitato</span><span class="sxs-lookup"><span data-stu-id="3665d-146">Enabled</span></span> 
- <span data-ttu-id="3665d-147">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="3665d-147">Disabled</span></span>

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

### <span data-ttu-id="3665d-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3665d-148">-ResourceGroupName</span></span>
<span data-ttu-id="3665d-149">Specifica il gruppo di risorse a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="3665d-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="3665d-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3665d-150">-StartTime</span></span>
<span data-ttu-id="3665d-151">Specifica l'ora di inizio, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="3665d-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="3665d-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="3665d-152">-StorageQueueAccount</span></span>
<span data-ttu-id="3665d-153">Specifica un nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3665d-153">Specifies a storage account name.</span></span>

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

### <span data-ttu-id="3665d-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="3665d-154">-StorageQueueMessage</span></span>
<span data-ttu-id="3665d-155">Specifica un messaggio di coda per il processo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3665d-155">Specifies a queue message for the storage job.</span></span>

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

### <span data-ttu-id="3665d-156">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="3665d-156">-StorageQueueName</span></span>
<span data-ttu-id="3665d-157">Specifica un nome di coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3665d-157">Specifies a storage queue name.</span></span>

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

### <span data-ttu-id="3665d-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="3665d-158">-StorageSASToken</span></span>
<span data-ttu-id="3665d-159">Specifica un token della firma di accesso condiviso per una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3665d-159">Specifies a shared access signature token for a storage queue.</span></span>

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

### <span data-ttu-id="3665d-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3665d-160">-Confirm</span></span>
<span data-ttu-id="3665d-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3665d-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3665d-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3665d-162">-WhatIf</span></span>
<span data-ttu-id="3665d-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3665d-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3665d-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3665d-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3665d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3665d-165">CommonParameters</span></span>
<span data-ttu-id="3665d-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3665d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3665d-167">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3665d-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3665d-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3665d-168">INPUTS</span></span>

### <span data-ttu-id="3665d-169">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3665d-169">None</span></span>
<span data-ttu-id="3665d-170">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3665d-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3665d-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3665d-171">OUTPUTS</span></span>

### <span data-ttu-id="3665d-172">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3665d-172">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="3665d-173">Note</span><span class="sxs-lookup"><span data-stu-id="3665d-173">NOTES</span></span>

## <span data-ttu-id="3665d-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3665d-174">RELATED LINKS</span></span>

[<span data-ttu-id="3665d-175">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="3665d-175">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="3665d-176">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3665d-176">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="3665d-177">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="3665d-177">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="3665d-178">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="3665d-178">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="3665d-179">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="3665d-179">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="3665d-180">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="3665d-180">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="3665d-181">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="3665d-181">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="3665d-182">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="3665d-182">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="3665d-183">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="3665d-183">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)

