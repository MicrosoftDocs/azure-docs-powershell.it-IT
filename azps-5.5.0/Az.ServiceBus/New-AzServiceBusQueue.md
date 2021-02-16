---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 16a7de817250170cf39a02200cee67c028249e1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201655"
---
# <span data-ttu-id="fe5c6-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="fe5c6-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="fe5c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5c6-103">Crea una coda di bus di servizio nello spazio dei nomi del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fe5c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe5c6-104">SYNTAX</span></span>

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

## <span data-ttu-id="fe5c6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fe5c6-105">DESCRIPTION</span></span>
<span data-ttu-id="fe5c6-106">Il cmdlet **New-AzServiceBusQueue** crea una coda di bus di servizio nello spazio dei nomi del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fe5c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe5c6-107">EXAMPLES</span></span>

### <span data-ttu-id="fe5c6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fe5c6-108">Example 1</span></span>
```powershell
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

<span data-ttu-id="fe5c6-109">Crea una nuova coda di bus di `SB-Queue_example1` servizio nello spazio dei nomi dei bus di servizio `SB-Example1` specificato.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="fe5c6-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fe5c6-110">Example 2</span></span>

<span data-ttu-id="fe5c6-111">Crea una coda di bus di servizio nello spazio dei nomi del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-111">Creates a Service Bus queue in the specified Service Bus namespace.</span></span> <span data-ttu-id="fe5c6-112">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="fe5c6-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzServiceBusQueue -EnablePartitioning $true -MaxSizeInMegabytes <Int64> -Name SB-Queue_example1 -Namespace SB-Example1 -ResourceGroupName Default-ServiceBus-WestUS
```

## <span data-ttu-id="fe5c6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe5c6-113">PARAMETERS</span></span>

### <span data-ttu-id="fe5c6-114">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="fe5c6-114">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="fe5c6-115">Specifica l'intervallo di inattività di [TimeSpan,](https://msdn.microsoft.com/library/system.timespan.aspx) dopo il quale la coda viene eliminata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-115">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="fe5c6-116">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-116">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="fe5c6-117">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="fe5c6-117">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="fe5c6-118">Lettere erre alla scadenza del messaggio</span><span class="sxs-lookup"><span data-stu-id="fe5c6-118">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="fe5c6-119">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="fe5c6-119">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="fe5c6-120">Timespan to live value.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-120">Timespan to live value.</span></span>
<span data-ttu-id="fe5c6-121">Si tratta della durata dopo la quale il messaggio scade, a partire dal momento in cui viene inviato al bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-121">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="fe5c6-122">Si tratta del valore predefinito usato quando TimeToLive non è impostato su un messaggio stesso.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-122">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="fe5c6-123">Per Standard = Timespan.Max e Basic = 14 giorni</span><span class="sxs-lookup"><span data-stu-id="fe5c6-123">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="fe5c6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5c6-124">-DefaultProfile</span></span>
<span data-ttu-id="fe5c6-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe5c6-126">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="fe5c6-126">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="fe5c6-127">Specifica il periodo di tempo della cronologia di rilevamento duplicato, un [valore TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) che definisce la durata della cronologia di rilevamento duplicati.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-127">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="fe5c6-128">Il valore predefinito è 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-128">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="fe5c6-129">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="fe5c6-129">-EnableBatchedOperations</span></span>
<span data-ttu-id="fe5c6-130">Enable Batched Operations: valore che indica se le operazioni in batch sul lato server sono abilitate</span><span class="sxs-lookup"><span data-stu-id="fe5c6-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="fe5c6-131">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="fe5c6-131">-EnableExpress</span></span>
<span data-ttu-id="fe5c6-132">EnableExpress: valore che indica se le entità Express sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-132">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="fe5c6-133">Una coda rapida conserva temporaneamente un messaggio in memoria prima di scriverlo nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-133">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="fe5c6-134">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="fe5c6-134">-EnablePartitioning</span></span>
<span data-ttu-id="fe5c6-135">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="fe5c6-135">EnablePartitioning</span></span>

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

### <span data-ttu-id="fe5c6-136">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="fe5c6-136">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="fe5c6-137">Queue/Topic name to forward the Dead Letter message</span><span class="sxs-lookup"><span data-stu-id="fe5c6-137">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="fe5c6-138">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="fe5c6-138">-ForwardTo</span></span>
<span data-ttu-id="fe5c6-139">Nome della coda/argomento per inoltrare i messaggi</span><span class="sxs-lookup"><span data-stu-id="fe5c6-139">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="fe5c6-140">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="fe5c6-140">-LockDuration</span></span>
<span data-ttu-id="fe5c6-141">Durata blocco</span><span class="sxs-lookup"><span data-stu-id="fe5c6-141">Lock Duration</span></span>

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

### <span data-ttu-id="fe5c6-142">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="fe5c6-142">-MaxDeliveryCount</span></span>
<span data-ttu-id="fe5c6-143">MaxDeliveryCount: numero massimo di consegne.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-143">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="fe5c6-144">Un messaggio viene automaticamente recapitato dopo questo numero di consegne.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-144">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="fe5c6-145">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="fe5c6-145">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="fe5c6-146">MaxSizeInMegabytes: dimensione massima della coda in megabyte, ovvero le dimensioni della memoria allocata per la coda. L'impostazione predefinita è 1024.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-146">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="fe5c6-147">Il valore massimo per SKU standard è 5120 e per SKU Premium è 81920, i valori consentiti sono 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="fe5c6-147">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="fe5c6-148">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="fe5c6-148">-MessageCount</span></span>
<span data-ttu-id="fe5c6-149">MessageCount: numero di messaggi in coda</span><span class="sxs-lookup"><span data-stu-id="fe5c6-149">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="fe5c6-150">-Name</span><span class="sxs-lookup"><span data-stu-id="fe5c6-150">-Name</span></span>
<span data-ttu-id="fe5c6-151">Nome coda</span><span class="sxs-lookup"><span data-stu-id="fe5c6-151">Queue Name</span></span>

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

### <span data-ttu-id="fe5c6-152">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fe5c6-152">-Namespace</span></span>
<span data-ttu-id="fe5c6-153">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fe5c6-153">Namespace Name</span></span>

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

### <span data-ttu-id="fe5c6-154">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="fe5c6-154">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="fe5c6-155">RequiresDuplicateDetection: valore che indica se la coda supporta il concetto di sessione</span><span class="sxs-lookup"><span data-stu-id="fe5c6-155">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="fe5c6-156">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="fe5c6-156">-RequiresSession</span></span>
<span data-ttu-id="fe5c6-157">RequiresSession: valore che indica se questa coda usa sessioni</span><span class="sxs-lookup"><span data-stu-id="fe5c6-157">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="fe5c6-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe5c6-158">-ResourceGroupName</span></span>
<span data-ttu-id="fe5c6-159">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fe5c6-159">The name of the resource group</span></span>

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

### <span data-ttu-id="fe5c6-160">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="fe5c6-160">-SizeInBytes</span></span>
<span data-ttu-id="fe5c6-161">SizeInBytes: dimensione della coda in byte</span><span class="sxs-lookup"><span data-stu-id="fe5c6-161">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="fe5c6-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe5c6-162">-Confirm</span></span>
<span data-ttu-id="fe5c6-163">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe5c6-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe5c6-164">-WhatIf</span></span>
<span data-ttu-id="fe5c6-165">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe5c6-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe5c6-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5c6-167">CommonParameters</span></span>
<span data-ttu-id="fe5c6-168">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5c6-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5c6-169">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe5c6-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5c6-170">INPUT</span><span class="sxs-lookup"><span data-stu-id="fe5c6-170">INPUTS</span></span>

### <span data-ttu-id="fe5c6-171">System.String</span><span class="sxs-lookup"><span data-stu-id="fe5c6-171">System.String</span></span>

### <span data-ttu-id="fe5c6-172">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fe5c6-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fe5c6-173">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fe5c6-173">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fe5c6-174">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fe5c6-174">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fe5c6-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe5c6-175">OUTPUTS</span></span>

### <span data-ttu-id="fe5c6-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="fe5c6-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="fe5c6-177">NOTE</span><span class="sxs-lookup"><span data-stu-id="fe5c6-177">NOTES</span></span>

## <span data-ttu-id="fe5c6-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe5c6-178">RELATED LINKS</span></span>
