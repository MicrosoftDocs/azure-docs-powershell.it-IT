---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8e1b1cd39e30bcbe2ccc9f46b5ab39511e4de58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686680"
---
# <span data-ttu-id="77cdd-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="77cdd-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="77cdd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="77cdd-103">Crea una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="77cdd-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77cdd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77cdd-104">SYNTAX</span></span>

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

## <span data-ttu-id="77cdd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77cdd-105">DESCRIPTION</span></span>
<span data-ttu-id="77cdd-106">Il cmdlet **New-AzureRmServiceBusQueue** crea una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="77cdd-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="77cdd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77cdd-107">EXAMPLES</span></span>

### <span data-ttu-id="77cdd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77cdd-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:36 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : 
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
```
<span data-ttu-id="77cdd-109">Crea una nuova coda di Service Bus `SB-Queue_exampl1` nello spazio dei nomi Service Bus specificato `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="77cdd-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="77cdd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77cdd-110">PARAMETERS</span></span>

### <span data-ttu-id="77cdd-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="77cdd-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="77cdd-112">Specifica l'intervallo di inattività [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , dopo il quale la coda viene eliminata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="77cdd-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="77cdd-113">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="77cdd-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="77cdd-114">-Confirm</span></span>
<span data-ttu-id="77cdd-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77cdd-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="77cdd-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="77cdd-117">Lettere morte nella scadenza del messaggio</span><span class="sxs-lookup"><span data-stu-id="77cdd-117">Dead Lettering On Message Expiration</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="77cdd-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="77cdd-119">TimeSpan in Live value.</span><span class="sxs-lookup"><span data-stu-id="77cdd-119">Timespan to live value.</span></span>
<span data-ttu-id="77cdd-120">Questa è la durata dopo la quale il messaggio scade, a partire da quando il messaggio viene inviato a Service Bus.</span><span class="sxs-lookup"><span data-stu-id="77cdd-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="77cdd-121">Questo è il valore predefinito usato quando TimeToLive non è impostato su un messaggio.</span><span class="sxs-lookup"><span data-stu-id="77cdd-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="77cdd-122">Per standard = TimeSpan. Max e Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="77cdd-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77cdd-123">-DefaultProfile</span></span>
<span data-ttu-id="77cdd-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77cdd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77cdd-125">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="77cdd-125">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="77cdd-126">Specifica la finestra temporale della cronologia di rilevamento duplicato, un [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) simbolicoche definisce la durata della cronologia dei rilevamenti duplicati.</span><span class="sxs-lookup"><span data-stu-id="77cdd-126">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="77cdd-127">Il valore predefinito è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="77cdd-127">The default value is 10 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-128">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="77cdd-128">-EnableBatchedOperations</span></span>
<span data-ttu-id="77cdd-129">Abilita operazioni in batch-valore che indica se le operazioni in batch sul lato server sono abilitate</span><span class="sxs-lookup"><span data-stu-id="77cdd-129">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-130">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="77cdd-130">-EnableExpress</span></span>
<span data-ttu-id="77cdd-131">EnableExpress: valore che indica se le entità espresse sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="77cdd-131">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="77cdd-132">Una coda espressa contiene temporaneamente un messaggio in memoria prima di scriverlo nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="77cdd-132">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-133">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="77cdd-133">-EnablePartitioning</span></span>
<span data-ttu-id="77cdd-134">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="77cdd-134">EnablePartitioning</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-135">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="77cdd-135">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="77cdd-136">Nome coda/argomento per inoltrare il messaggio di lettera morta</span><span class="sxs-lookup"><span data-stu-id="77cdd-136">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-137">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="77cdd-137">-ForwardTo</span></span>
<span data-ttu-id="77cdd-138">Nome coda/argomento per inoltrare i messaggi</span><span class="sxs-lookup"><span data-stu-id="77cdd-138">Queue/Topic name to forward the messages</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-139">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="77cdd-139">-LockDuration</span></span>
<span data-ttu-id="77cdd-140">Durata del blocco</span><span class="sxs-lookup"><span data-stu-id="77cdd-140">Lock Duration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-141">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="77cdd-141">-MaxDeliveryCount</span></span>
<span data-ttu-id="77cdd-142">MaxDeliveryCount-numero massimo di recapito.</span><span class="sxs-lookup"><span data-stu-id="77cdd-142">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="77cdd-143">Un messaggio viene automaticamente deadlettered dopo questo numero di consegne.</span><span class="sxs-lookup"><span data-stu-id="77cdd-143">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-144">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="77cdd-144">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="77cdd-145">MaxSizeInMegabytes-dimensione massima della coda in megabyte, che corrisponde alla dimensione della memoria allocata per la coda.</span><span class="sxs-lookup"><span data-stu-id="77cdd-145">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-146">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="77cdd-146">-MessageCount</span></span>
<span data-ttu-id="77cdd-147">MessageCount-numero di messaggi nella coda</span><span class="sxs-lookup"><span data-stu-id="77cdd-147">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="77cdd-148">-Name</span></span>
<span data-ttu-id="77cdd-149">Nome coda</span><span class="sxs-lookup"><span data-stu-id="77cdd-149">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-150">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="77cdd-150">-Namespace</span></span>
<span data-ttu-id="77cdd-151">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="77cdd-151">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-152">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="77cdd-152">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="77cdd-153">RequiresDuplicateDetection-valore che indica se la coda supporta il concetto di sessione</span><span class="sxs-lookup"><span data-stu-id="77cdd-153">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-154">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="77cdd-154">-RequiresSession</span></span>
<span data-ttu-id="77cdd-155">RequiresSession-valore che indica se la coda richiede il rilevamento duplicato</span><span class="sxs-lookup"><span data-stu-id="77cdd-155">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77cdd-156">-ResourceGroupName</span></span>
<span data-ttu-id="77cdd-157">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="77cdd-157">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-158">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="77cdd-158">-SizeInBytes</span></span>
<span data-ttu-id="77cdd-159">SizeInBytes-dimensione della coda in byte</span><span class="sxs-lookup"><span data-stu-id="77cdd-159">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77cdd-160">-WhatIf</span></span>
<span data-ttu-id="77cdd-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77cdd-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77cdd-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="77cdd-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77cdd-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77cdd-163">CommonParameters</span></span>
<span data-ttu-id="77cdd-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77cdd-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="77cdd-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77cdd-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77cdd-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77cdd-166">INPUTS</span></span>

### <span data-ttu-id="77cdd-167">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="77cdd-167">-ResourceGroup</span></span>
 <span data-ttu-id="77cdd-168">System. String</span><span class="sxs-lookup"><span data-stu-id="77cdd-168">System.String</span></span>

### <span data-ttu-id="77cdd-169">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="77cdd-169">-NamespaceName</span></span>
 <span data-ttu-id="77cdd-170">System. String</span><span class="sxs-lookup"><span data-stu-id="77cdd-170">System.String</span></span>

### <span data-ttu-id="77cdd-171">-QueueName</span><span class="sxs-lookup"><span data-stu-id="77cdd-171">-QueueName</span></span>
 <span data-ttu-id="77cdd-172">System. String</span><span class="sxs-lookup"><span data-stu-id="77cdd-172">System.String</span></span>

### <span data-ttu-id="77cdd-173">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="77cdd-173">-EnablePartitioning</span></span>
 <span data-ttu-id="77cdd-174">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="77cdd-174">System.Boolean?</span></span>


## <span data-ttu-id="77cdd-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77cdd-175">OUTPUTS</span></span>

### <span data-ttu-id="77cdd-176">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="77cdd-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>


## <span data-ttu-id="77cdd-177">Note</span><span class="sxs-lookup"><span data-stu-id="77cdd-177">NOTES</span></span>

## <span data-ttu-id="77cdd-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77cdd-178">RELATED LINKS</span></span>
