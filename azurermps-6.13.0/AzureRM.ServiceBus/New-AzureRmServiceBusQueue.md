---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 29e2c0f04dff07e76907ee67c3e012c2b67c1582
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518551"
---
# <span data-ttu-id="573d1-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="573d1-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="573d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="573d1-102">SYNOPSIS</span></span>
<span data-ttu-id="573d1-103">Crea una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="573d1-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="573d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="573d1-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="573d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="573d1-105">DESCRIPTION</span></span>
<span data-ttu-id="573d1-106">Il cmdlet **New-AzureRmServiceBusQueue** crea una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="573d1-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="573d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="573d1-107">EXAMPLES</span></span>

### <span data-ttu-id="573d1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="573d1-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

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

<span data-ttu-id="573d1-109">Crea una nuova coda di Service Bus `SB-Queue_example1` nello spazio dei nomi Service Bus specificato `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="573d1-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="573d1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="573d1-110">PARAMETERS</span></span>

### <span data-ttu-id="573d1-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="573d1-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="573d1-112">Specifica l'intervallo di inattività [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , dopo il quale la coda viene eliminata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="573d1-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="573d1-113">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="573d1-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="573d1-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="573d1-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="573d1-115">Lettere morte nella scadenza del messaggio</span><span class="sxs-lookup"><span data-stu-id="573d1-115">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="573d1-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="573d1-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="573d1-117">TimeSpan in Live value.</span><span class="sxs-lookup"><span data-stu-id="573d1-117">Timespan to live value.</span></span>
<span data-ttu-id="573d1-118">Questa è la durata dopo la quale il messaggio scade, a partire da quando il messaggio viene inviato a Service Bus.</span><span class="sxs-lookup"><span data-stu-id="573d1-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="573d1-119">Questo è il valore predefinito usato quando TimeToLive non è impostato su un messaggio.</span><span class="sxs-lookup"><span data-stu-id="573d1-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="573d1-120">Per standard = TimeSpan. Max e Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="573d1-120">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="573d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573d1-121">-DefaultProfile</span></span>
<span data-ttu-id="573d1-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="573d1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="573d1-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="573d1-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="573d1-124">Specifica la finestra temporale della cronologia di rilevamento duplicato, un [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) simbolicoche definisce la durata della cronologia dei rilevamenti duplicati.</span><span class="sxs-lookup"><span data-stu-id="573d1-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="573d1-125">Il valore predefinito è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="573d1-125">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="573d1-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="573d1-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="573d1-127">Abilita operazioni in batch-valore che indica se le operazioni in batch sul lato server sono abilitate</span><span class="sxs-lookup"><span data-stu-id="573d1-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="573d1-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="573d1-128">-EnableExpress</span></span>
<span data-ttu-id="573d1-129">EnableExpress: valore che indica se le entità espresse sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="573d1-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="573d1-130">Una coda espressa contiene temporaneamente un messaggio in memoria prima di scriverlo nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="573d1-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="573d1-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="573d1-131">-EnablePartitioning</span></span>
<span data-ttu-id="573d1-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="573d1-132">EnablePartitioning</span></span>

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

### <span data-ttu-id="573d1-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="573d1-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="573d1-134">Nome coda/argomento per inoltrare il messaggio di lettera morta</span><span class="sxs-lookup"><span data-stu-id="573d1-134">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="573d1-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="573d1-135">-ForwardTo</span></span>
<span data-ttu-id="573d1-136">Nome coda/argomento per inoltrare i messaggi</span><span class="sxs-lookup"><span data-stu-id="573d1-136">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="573d1-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="573d1-137">-LockDuration</span></span>
<span data-ttu-id="573d1-138">Durata del blocco</span><span class="sxs-lookup"><span data-stu-id="573d1-138">Lock Duration</span></span>

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

### <span data-ttu-id="573d1-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="573d1-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="573d1-140">MaxDeliveryCount-numero massimo di recapito.</span><span class="sxs-lookup"><span data-stu-id="573d1-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="573d1-141">Un messaggio viene automaticamente deadlettered dopo questo numero di consegne.</span><span class="sxs-lookup"><span data-stu-id="573d1-141">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="573d1-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="573d1-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="573d1-143">MaxSizeInMegabytes-dimensione massima della coda in megabyte, che corrisponde alla dimensione della memoria allocata per la coda.</span><span class="sxs-lookup"><span data-stu-id="573d1-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="573d1-144">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="573d1-144">-MessageCount</span></span>
<span data-ttu-id="573d1-145">MessageCount-numero di messaggi nella coda</span><span class="sxs-lookup"><span data-stu-id="573d1-145">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="573d1-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="573d1-146">-Name</span></span>
<span data-ttu-id="573d1-147">Nome coda</span><span class="sxs-lookup"><span data-stu-id="573d1-147">Queue Name</span></span>

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

### <span data-ttu-id="573d1-148">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="573d1-148">-Namespace</span></span>
<span data-ttu-id="573d1-149">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="573d1-149">Namespace Name</span></span>

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

### <span data-ttu-id="573d1-150">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="573d1-150">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="573d1-151">RequiresDuplicateDetection-valore che indica se la coda supporta il concetto di sessione</span><span class="sxs-lookup"><span data-stu-id="573d1-151">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="573d1-152">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="573d1-152">-RequiresSession</span></span>
<span data-ttu-id="573d1-153">RequiresSession-valore che indica se la coda richiede il rilevamento duplicato</span><span class="sxs-lookup"><span data-stu-id="573d1-153">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

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

### <span data-ttu-id="573d1-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="573d1-154">-ResourceGroupName</span></span>
<span data-ttu-id="573d1-155">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="573d1-155">The name of the resource group</span></span>

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

### <span data-ttu-id="573d1-156">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="573d1-156">-SizeInBytes</span></span>
<span data-ttu-id="573d1-157">SizeInBytes-dimensione della coda in byte</span><span class="sxs-lookup"><span data-stu-id="573d1-157">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="573d1-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="573d1-158">-Confirm</span></span>
<span data-ttu-id="573d1-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="573d1-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="573d1-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="573d1-160">-WhatIf</span></span>
<span data-ttu-id="573d1-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="573d1-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="573d1-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="573d1-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="573d1-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573d1-163">CommonParameters</span></span>
<span data-ttu-id="573d1-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="573d1-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573d1-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="573d1-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573d1-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="573d1-166">INPUTS</span></span>

### <span data-ttu-id="573d1-167">System. String</span><span class="sxs-lookup"><span data-stu-id="573d1-167">System.String</span></span>

### <span data-ttu-id="573d1-168">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="573d1-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="573d1-169">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="573d1-169">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="573d1-170">System. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="573d1-170">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="573d1-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="573d1-171">OUTPUTS</span></span>

### <span data-ttu-id="573d1-172">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="573d1-172">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="573d1-173">Note</span><span class="sxs-lookup"><span data-stu-id="573d1-173">NOTES</span></span>

## <span data-ttu-id="573d1-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="573d1-174">RELATED LINKS</span></span>
