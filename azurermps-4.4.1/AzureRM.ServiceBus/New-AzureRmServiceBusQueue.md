---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 4538bb39c085a2e7152a146d5e93e08a0c09f5de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510323"
---
# <span data-ttu-id="3a749-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="3a749-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="3a749-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a749-102">SYNOPSIS</span></span>
<span data-ttu-id="3a749-103">Crea una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="3a749-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a749-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a749-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-EnableBatchedOperations <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableExpress <Boolean>]
 [-IsAnonymousAccessible <Boolean>] [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>]
 [-MessageCount <Int64>] [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a749-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a749-105">DESCRIPTION</span></span>
<span data-ttu-id="3a749-106">Il cmdlet **New-AzureRmServiceBusQueue** crea una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="3a749-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="3a749-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a749-107">EXAMPLES</span></span>

### <span data-ttu-id="3a749-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a749-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="3a749-109">Crea una nuova coda di Service Bus `SB-Queue_exampl1` nello spazio dei nomi Service Bus specificato `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="3a749-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="3a749-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a749-110">PARAMETERS</span></span>

### <span data-ttu-id="3a749-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="3a749-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="3a749-112">Specifica l'intervallo di inattività [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , dopo il quale la coda viene eliminata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3a749-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="3a749-113">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="3a749-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="3a749-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="3a749-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="3a749-115">Specifica se i messaggi sono deadlettered alla scadenza.</span><span class="sxs-lookup"><span data-stu-id="3a749-115">Specifies whether messages are deadlettered on expiration.</span></span>

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

### <span data-ttu-id="3a749-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="3a749-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="3a749-117">Specifica il TTL (time-to-Live) del messaggio predefinito.</span><span class="sxs-lookup"><span data-stu-id="3a749-117">Specifies the default message time-to-live (TTL).</span></span>

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

### <span data-ttu-id="3a749-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="3a749-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="3a749-119">Specifica la finestra temporale della cronologia di rilevamento duplicato, un [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) simbolicoche definisce la durata della cronologia dei rilevamenti duplicati.</span><span class="sxs-lookup"><span data-stu-id="3a749-119">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="3a749-120">Il valore predefinito è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="3a749-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="3a749-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="3a749-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="3a749-122">Specifica se le operazioni in batch sul lato server sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="3a749-122">Specifies whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="3a749-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="3a749-123">-EnableExpress</span></span>
<span data-ttu-id="3a749-124">Specifica se le entità espresse sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="3a749-124">Specifies whether Express Entities are enabled.</span></span> <span data-ttu-id="3a749-125">Una coda espressa contiene temporaneamente un messaggio in memoria prima di scriverlo nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="3a749-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="3a749-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="3a749-126">-EnablePartitioning</span></span>
<span data-ttu-id="3a749-127">Specifica se EnablePartitioning è abilitato.</span><span class="sxs-lookup"><span data-stu-id="3a749-127">Specifies whether EnablePartitioning is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a749-128">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="3a749-128">-IsAnonymousAccessible</span></span>
<span data-ttu-id="3a749-129">Specifica se il messaggio è accessibile in forma anonima.</span><span class="sxs-lookup"><span data-stu-id="3a749-129">Specifies whether the message is anonymously accessible.</span></span>

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

### <span data-ttu-id="3a749-130">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="3a749-130">-LockDuration</span></span>
<span data-ttu-id="3a749-131">Specifica la durata del blocco.</span><span class="sxs-lookup"><span data-stu-id="3a749-131">Specifies the lock duration.</span></span>

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

### <span data-ttu-id="3a749-132">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="3a749-132">-MaxDeliveryCount</span></span>
<span data-ttu-id="3a749-133">Specifica il numero massimo di recapito.</span><span class="sxs-lookup"><span data-stu-id="3a749-133">Specifies the maximum delivery count.</span></span> <span data-ttu-id="3a749-134">Un messaggio viene automaticamente deadlettered dopo questo numero di consegne.</span><span class="sxs-lookup"><span data-stu-id="3a749-134">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="3a749-135">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="3a749-135">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="3a749-136">Specifica la dimensione massima della coda in megabyte, ovvero le dimensioni della memoria allocata per la coda.</span><span class="sxs-lookup"><span data-stu-id="3a749-136">Specifies the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="3a749-137">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="3a749-137">-MessageCount</span></span>
<span data-ttu-id="3a749-138">Specifica il numero di messaggi nella coda.</span><span class="sxs-lookup"><span data-stu-id="3a749-138">Specifies the number of messages in the queue.</span></span>

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

### <span data-ttu-id="3a749-139">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="3a749-139">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="3a749-140">Specifica se la coda richiede il rilevamento duplicato.</span><span class="sxs-lookup"><span data-stu-id="3a749-140">Specifies whether the queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="3a749-141">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="3a749-141">-RequiresSession</span></span>
<span data-ttu-id="3a749-142">Specifica se questa coda supporta le sessioni.</span><span class="sxs-lookup"><span data-stu-id="3a749-142">Specifies whether this queue supports sessions.</span></span>

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

### <span data-ttu-id="3a749-143">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="3a749-143">-SizeInBytes</span></span>
<span data-ttu-id="3a749-144">Dimensioni della coda in byte.</span><span class="sxs-lookup"><span data-stu-id="3a749-144">The size of the queue in bytes.</span></span>

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

### <span data-ttu-id="3a749-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3a749-145">-Confirm</span></span>
<span data-ttu-id="3a749-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a749-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a749-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a749-147">-WhatIf</span></span>
<span data-ttu-id="3a749-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a749-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a749-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a749-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a749-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a749-150">-DefaultProfile</span></span>
<span data-ttu-id="3a749-151">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a749-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a749-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a749-152">-Name</span></span>
<span data-ttu-id="3a749-153">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="3a749-153">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a749-154">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3a749-154">-Namespace</span></span>
<span data-ttu-id="3a749-155">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3a749-155">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a749-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a749-156">-ResourceGroupName</span></span>
<span data-ttu-id="3a749-157">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3a749-157">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a749-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a749-158">CommonParameters</span></span>
<span data-ttu-id="3a749-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a749-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a749-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a749-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a749-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a749-161">INPUTS</span></span>

### <span data-ttu-id="3a749-162">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a749-162">-ResourceGroup</span></span>
 <span data-ttu-id="3a749-163">System. String</span><span class="sxs-lookup"><span data-stu-id="3a749-163">System.String</span></span>

### <span data-ttu-id="3a749-164">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="3a749-164">-NamespaceName</span></span>
 <span data-ttu-id="3a749-165">System. String</span><span class="sxs-lookup"><span data-stu-id="3a749-165">System.String</span></span>

### <span data-ttu-id="3a749-166">-QueueName</span><span class="sxs-lookup"><span data-stu-id="3a749-166">-QueueName</span></span>
 <span data-ttu-id="3a749-167">System. String</span><span class="sxs-lookup"><span data-stu-id="3a749-167">System.String</span></span>

### <span data-ttu-id="3a749-168">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="3a749-168">-EnablePartitioning</span></span>
 <span data-ttu-id="3a749-169">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="3a749-169">System.Boolean?</span></span>

## <span data-ttu-id="3a749-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a749-170">OUTPUTS</span></span>

### <span data-ttu-id="3a749-171">Microsoft. Azure. Commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="3a749-171">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="3a749-172">Nome: SB-Queue_exampl1 località: West US LockDuration: AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:36 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false EnablePartitioning: true IsAnonymousAccessible: false MaxDeliveryCount: MaxSizeInMegabytes: 16384 MessageCount: CountDetails: RequiresDuplicateDetection: false RequiresSession: false SizeInBytes: status: Active SupportOrdering: false UpdatedAt: 1/20/2017 2:51:37 AM</span><span class="sxs-lookup"><span data-stu-id="3a749-172">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:36 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM</span></span>

## <span data-ttu-id="3a749-173">Note</span><span class="sxs-lookup"><span data-stu-id="3a749-173">NOTES</span></span>

## <span data-ttu-id="3a749-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a749-174">RELATED LINKS</span></span>

