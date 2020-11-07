---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 75AF57EE-C7C3-42DE-AFD7-4B5150EEDBB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: c752b4fd96ec001467e051fc01be24f592241182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687985"
---
# <span data-ttu-id="ce5e4-101">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ce5e4-101">Set-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="ce5e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="ce5e4-103">Modifica un processo di Accodamento archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-103">Modifies a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce5e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce5e4-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-StorageSASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce5e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce5e4-105">DESCRIPTION</span></span>
<span data-ttu-id="ce5e4-106">Il cmdlet **set-AzureRmSchedulerStorageQueueJob** modifica un processo di Accodamento archiviazione in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-106">The **Set-AzureRmSchedulerStorageQueueJob** cmdlet modifies a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="ce5e4-107">Questo cmdlet supporta i parametri dinamici basati sul parametro *ErrorActionType* .</span><span class="sxs-lookup"><span data-stu-id="ce5e4-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="ce5e4-108">I parametri dinamici diventano disponibili in base ad altri valori di parametro.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="ce5e4-109">Per individuare i nomi dei parametri dinamici dopo avere specificato gli altri parametri, digitare un segno meno (-) e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ce5e4-110">Se si omette un parametro obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ce5e4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce5e4-111">EXAMPLES</span></span>

## <span data-ttu-id="ce5e4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce5e4-112">PARAMETERS</span></span>

### <span data-ttu-id="ce5e4-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ce5e4-113">-EndTime</span></span>
<span data-ttu-id="ce5e4-114">Specifica un'ora di fine, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="ce5e4-115">Per ottenere un oggetto **DateTime** , usare il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="ce5e4-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="ce5e4-116">-ErrorActionType</span></span>
<span data-ttu-id="ce5e4-117">Specifica un'impostazione di azione di errore per il processo.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="ce5e4-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce5e4-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ce5e4-119">Http</span><span class="sxs-lookup"><span data-stu-id="ce5e4-119">Http</span></span> 
- <span data-ttu-id="ce5e4-120">Https</span><span class="sxs-lookup"><span data-stu-id="ce5e4-120">Https</span></span> 
- <span data-ttu-id="ce5e4-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="ce5e4-121">StorageQueue</span></span> 
- <span data-ttu-id="ce5e4-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ce5e4-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="ce5e4-123">ServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ce5e4-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="ce5e4-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="ce5e4-124">-ExecutionCount</span></span>
<span data-ttu-id="ce5e4-125">Specifica il numero di volte in cui il processo viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="ce5e4-126">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="ce5e4-127">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="ce5e4-127">-Frequency</span></span>
<span data-ttu-id="ce5e4-128">Specifica una frequenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="ce5e4-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce5e4-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ce5e4-130">Minuto</span><span class="sxs-lookup"><span data-stu-id="ce5e4-130">Minute</span></span> 
- <span data-ttu-id="ce5e4-131">Ora</span><span class="sxs-lookup"><span data-stu-id="ce5e4-131">Hour</span></span> 
- <span data-ttu-id="ce5e4-132">Giorno</span><span class="sxs-lookup"><span data-stu-id="ce5e4-132">Day</span></span> 
- <span data-ttu-id="ce5e4-133">Settimana</span><span class="sxs-lookup"><span data-stu-id="ce5e4-133">Week</span></span> 
- <span data-ttu-id="ce5e4-134">Mese</span><span class="sxs-lookup"><span data-stu-id="ce5e4-134">Month</span></span>

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

### <span data-ttu-id="ce5e4-135">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="ce5e4-135">-Interval</span></span>
<span data-ttu-id="ce5e4-136">Specifica un intervallo di ricorrenza per il processo.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="ce5e4-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ce5e4-137">-JobCollectionName</span></span>
<span data-ttu-id="ce5e4-138">Specifica il nome della raccolta processi a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="ce5e4-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="ce5e4-139">-JobName</span></span>
<span data-ttu-id="ce5e4-140">Specifica il nome del processo modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ce5e4-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="ce5e4-141">-JobState</span></span>
<span data-ttu-id="ce5e4-142">Specifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-142">Specifies the state of the job.</span></span>
<span data-ttu-id="ce5e4-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce5e4-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ce5e4-144">Abilitato</span><span class="sxs-lookup"><span data-stu-id="ce5e4-144">Enabled</span></span> 
- <span data-ttu-id="ce5e4-145">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="ce5e4-145">Disabled</span></span>

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

### <span data-ttu-id="ce5e4-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce5e4-146">-ResourceGroupName</span></span>
<span data-ttu-id="ce5e4-147">Specifica il gruppo di risorse a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="ce5e4-148">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ce5e4-148">-StartTime</span></span>
<span data-ttu-id="ce5e4-149">Specifica l'ora di inizio, come oggetto **DateTime** , per il processo.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-149">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="ce5e4-150">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="ce5e4-150">-StorageQueueAccount</span></span>
<span data-ttu-id="ce5e4-151">Specifica un nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-151">Specifies a storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce5e4-152">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="ce5e4-152">-StorageQueueMessage</span></span>
<span data-ttu-id="ce5e4-153">Specifica un messaggio di coda per il processo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-153">Specifies a queue message for storage job.</span></span>

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

### <span data-ttu-id="ce5e4-154">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="ce5e4-154">-StorageQueueName</span></span>
<span data-ttu-id="ce5e4-155">Specifica un nome di coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-155">Specifies a storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce5e4-156">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="ce5e4-156">-StorageSASToken</span></span>
<span data-ttu-id="ce5e4-157">Specifica un token della firma di accesso condiviso per una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-157">Specifies a shared access signature token for a storage queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce5e4-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce5e4-158">-Confirm</span></span>
<span data-ttu-id="ce5e4-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce5e4-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce5e4-160">-WhatIf</span></span>
<span data-ttu-id="ce5e4-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce5e4-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce5e4-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce5e4-163">-DefaultProfile</span></span>
<span data-ttu-id="ce5e4-164">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce5e4-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce5e4-165">CommonParameters</span></span>
<span data-ttu-id="ce5e4-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce5e4-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce5e4-167">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce5e4-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce5e4-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce5e4-168">INPUTS</span></span>

## <span data-ttu-id="ce5e4-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce5e4-169">OUTPUTS</span></span>

### <span data-ttu-id="ce5e4-170">Microsoft. Azure. Commands. Scheduler. Models. PSSchedulerJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ce5e4-170">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="ce5e4-171">Note</span><span class="sxs-lookup"><span data-stu-id="ce5e4-171">NOTES</span></span>

## <span data-ttu-id="ce5e4-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce5e4-172">RELATED LINKS</span></span>

[<span data-ttu-id="ce5e4-173">New-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ce5e4-173">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ce5e4-174">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ce5e4-174">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ce5e4-175">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ce5e4-175">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ce5e4-176">New-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ce5e4-176">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ce5e4-177">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ce5e4-177">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="ce5e4-178">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ce5e4-178">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ce5e4-179">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ce5e4-179">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ce5e4-180">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ce5e4-180">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ce5e4-181">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ce5e4-181">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)


