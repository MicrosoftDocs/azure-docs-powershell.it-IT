---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: a555e269fd02cb02d420426fed99888b19214f52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019270"
---
# <span data-ttu-id="24edc-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="24edc-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="24edc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24edc-102">SYNOPSIS</span></span>
<span data-ttu-id="24edc-103">Crea una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="24edc-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="24edc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24edc-104">SYNTAX</span></span>

```
New-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24edc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24edc-105">DESCRIPTION</span></span>
<span data-ttu-id="24edc-106">Il cmdlet **New-AzServiceBusQueue** crea una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="24edc-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="24edc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24edc-107">EXAMPLES</span></span>

### <span data-ttu-id="24edc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="24edc-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:12 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="24edc-109">Crea una nuova coda di Service Bus `SB-Queue_example1` nello spazio dei nomi Service Bus specificato `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="24edc-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="24edc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24edc-110">PARAMETERS</span></span>

### <span data-ttu-id="24edc-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="24edc-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="24edc-112">Specifica l'intervallo di inattività [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , dopo il quale la coda viene eliminata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="24edc-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="24edc-113">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="24edc-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="24edc-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="24edc-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="24edc-115">Lettere morte nella scadenza del messaggio</span><span class="sxs-lookup"><span data-stu-id="24edc-115">Dead Lettering On Message Expiration</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="24edc-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="24edc-117">TimeSpan in Live value.</span><span class="sxs-lookup"><span data-stu-id="24edc-117">Timespan to live value.</span></span>
<span data-ttu-id="24edc-118">Questa è la durata dopo la quale il messaggio scade, a partire da quando il messaggio viene inviato a Service Bus.</span><span class="sxs-lookup"><span data-stu-id="24edc-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="24edc-119">Questo è il valore predefinito usato quando TimeToLive non è impostato su un messaggio.</span><span class="sxs-lookup"><span data-stu-id="24edc-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="24edc-120">Per standard = TimeSpan. Max e Basic = 14 giorni</span><span class="sxs-lookup"><span data-stu-id="24edc-120">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="24edc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24edc-121">-DefaultProfile</span></span>
<span data-ttu-id="24edc-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24edc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24edc-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="24edc-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="24edc-124">Specifica la finestra temporale della cronologia di rilevamento duplicato, un valore [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) che definisce la durata della cronologia dei rilevamenti duplicati.</span><span class="sxs-lookup"><span data-stu-id="24edc-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="24edc-125">Il valore predefinito è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="24edc-125">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="24edc-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="24edc-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="24edc-127">Abilita operazioni in batch-valore che indica se le operazioni in batch sul lato server sono abilitate</span><span class="sxs-lookup"><span data-stu-id="24edc-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="24edc-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="24edc-128">-EnableExpress</span></span>
<span data-ttu-id="24edc-129">EnableExpress: valore che indica se le entità espresse sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="24edc-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="24edc-130">Una coda espressa contiene temporaneamente un messaggio in memoria prima di scriverlo nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="24edc-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="24edc-131">-EnablePartitioning</span></span>
<span data-ttu-id="24edc-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="24edc-132">EnablePartitioning</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="24edc-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="24edc-134">Nome coda/argomento per inoltrare il messaggio di lettera morta</span><span class="sxs-lookup"><span data-stu-id="24edc-134">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="24edc-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="24edc-135">-ForwardTo</span></span>
<span data-ttu-id="24edc-136">Nome coda/argomento per inoltrare i messaggi</span><span class="sxs-lookup"><span data-stu-id="24edc-136">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="24edc-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="24edc-137">-LockDuration</span></span>
<span data-ttu-id="24edc-138">Durata del blocco</span><span class="sxs-lookup"><span data-stu-id="24edc-138">Lock Duration</span></span>

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

### <span data-ttu-id="24edc-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="24edc-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="24edc-140">MaxDeliveryCount-numero massimo di recapito.</span><span class="sxs-lookup"><span data-stu-id="24edc-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="24edc-141">Un messaggio viene automaticamente deadlettered dopo questo numero di consegne.</span><span class="sxs-lookup"><span data-stu-id="24edc-141">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="24edc-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="24edc-143">MaxSizeInMegabytes-dimensione massima della coda in megabyte, che corrisponde alla dimensione della memoria allocata per la coda. Il valore predefinito è 1024.</span><span class="sxs-lookup"><span data-stu-id="24edc-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="24edc-144">Max per SKU standard è 5120 e per il codice SKU Premium è 81920, valori consentiti: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="24edc-144">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-145">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="24edc-145">-MessageCount</span></span>
<span data-ttu-id="24edc-146">MessageCount-numero di messaggi nella coda</span><span class="sxs-lookup"><span data-stu-id="24edc-146">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="24edc-147">-Name</span></span>
<span data-ttu-id="24edc-148">Nome coda</span><span class="sxs-lookup"><span data-stu-id="24edc-148">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-149">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="24edc-149">-Namespace</span></span>
<span data-ttu-id="24edc-150">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="24edc-150">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-151">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="24edc-151">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="24edc-152">RequiresDuplicateDetection-valore che indica se la coda supporta il concetto di sessione</span><span class="sxs-lookup"><span data-stu-id="24edc-152">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-153">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="24edc-153">-RequiresSession</span></span>
<span data-ttu-id="24edc-154">RequiresSession-valore che indica se la coda usa le sessioni</span><span class="sxs-lookup"><span data-stu-id="24edc-154">RequiresSession - the value indicating if this queue uses sessions</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24edc-155">-ResourceGroupName</span></span>
<span data-ttu-id="24edc-156">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="24edc-156">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-157">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="24edc-157">-SizeInBytes</span></span>
<span data-ttu-id="24edc-158">SizeInBytes-dimensione della coda in byte</span><span class="sxs-lookup"><span data-stu-id="24edc-158">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24edc-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24edc-159">-Confirm</span></span>
<span data-ttu-id="24edc-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24edc-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24edc-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24edc-161">-WhatIf</span></span>
<span data-ttu-id="24edc-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24edc-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24edc-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24edc-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24edc-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24edc-164">CommonParameters</span></span>
<span data-ttu-id="24edc-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24edc-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24edc-166">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24edc-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24edc-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24edc-167">INPUTS</span></span>

### <span data-ttu-id="24edc-168">System. String</span><span class="sxs-lookup"><span data-stu-id="24edc-168">System.String</span></span>

### <span data-ttu-id="24edc-169">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="24edc-169">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="24edc-170">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="24edc-170">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="24edc-171">System. Nullable ' 1 [[System. Int64, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="24edc-171">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="24edc-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24edc-172">OUTPUTS</span></span>

### <span data-ttu-id="24edc-173">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="24edc-173">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="24edc-174">Note</span><span class="sxs-lookup"><span data-stu-id="24edc-174">NOTES</span></span>

## <span data-ttu-id="24edc-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24edc-175">RELATED LINKS</span></span>
