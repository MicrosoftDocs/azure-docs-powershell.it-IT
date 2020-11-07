---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 54753001be0a754cf9416e1b2ec53fd81647d8d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686679"
---
# <span data-ttu-id="88116-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="88116-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="88116-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88116-102">SYNOPSIS</span></span>
<span data-ttu-id="88116-103">Crea un abbonamento all'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="88116-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88116-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88116-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88116-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88116-105">DESCRIPTION</span></span>
<span data-ttu-id="88116-106">Il cmdlet **New-AzureRmServiceBusSubscription** crea un nuovo abbonamento all'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="88116-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="88116-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88116-107">EXAMPLES</span></span>

### <span data-ttu-id="88116-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88116-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```
<span data-ttu-id="88116-109">Crea la sottoscrizione `SB-TopicSubscription-Example1` per l'argomento Service Bus specificato `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="88116-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="88116-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88116-110">PARAMETERS</span></span>

### <span data-ttu-id="88116-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="88116-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="88116-112">Specifica l'intervallo di inattività [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , dopo il quale l'abbonamento viene eliminato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="88116-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="88116-113">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="88116-113">The minimum duration is 5 minutes.</span></span>


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

### <span data-ttu-id="88116-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="88116-114">-Confirm</span></span>
<span data-ttu-id="88116-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88116-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88116-116">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="88116-116">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="88116-117">Valore che indica se un abbonamento ha il supporto di lettere morte per filtrare le eccezioni di valutazione.</span><span class="sxs-lookup"><span data-stu-id="88116-117">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="88116-118">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="88116-118">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="88116-119">Lettere morte nella scadenza del messaggio</span><span class="sxs-lookup"><span data-stu-id="88116-119">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="88116-120">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="88116-120">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="88116-121">TimeSpan in Live value.</span><span class="sxs-lookup"><span data-stu-id="88116-121">Timespan to live value.</span></span>
<span data-ttu-id="88116-122">Questa è la durata dopo la quale il messaggio scade, a partire da quando il messaggio viene inviato a Service Bus.</span><span class="sxs-lookup"><span data-stu-id="88116-122">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="88116-123">Questo è il valore predefinito usato quando TimeToLive non è impostato su un messaggio.</span><span class="sxs-lookup"><span data-stu-id="88116-123">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="88116-124">Per standard = TimeSpan. Max e Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="88116-124">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="88116-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88116-125">-DefaultProfile</span></span>
<span data-ttu-id="88116-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88116-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88116-127">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="88116-127">-EnableBatchedOperations</span></span>
<span data-ttu-id="88116-128">Abilita operazioni in batch-valore che indica se le operazioni in batch sul lato server sono abilitate</span><span class="sxs-lookup"><span data-stu-id="88116-128">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="88116-129">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="88116-129">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="88116-130">Nome coda/argomento per inoltrare il messaggio di lettera morta</span><span class="sxs-lookup"><span data-stu-id="88116-130">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="88116-131">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="88116-131">-ForwardTo</span></span>
<span data-ttu-id="88116-132">Nome coda/argomento per inoltrare i messaggi</span><span class="sxs-lookup"><span data-stu-id="88116-132">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="88116-133">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="88116-133">-LockDuration</span></span>
<span data-ttu-id="88116-134">Durata del blocco</span><span class="sxs-lookup"><span data-stu-id="88116-134">Lock Duration</span></span>

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

### <span data-ttu-id="88116-135">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="88116-135">-MaxDeliveryCount</span></span>
<span data-ttu-id="88116-136">MaxDeliveryCount-numero massimo di recapito.</span><span class="sxs-lookup"><span data-stu-id="88116-136">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="88116-137">Un messaggio viene automaticamente deadlettered dopo questo numero di consegne.</span><span class="sxs-lookup"><span data-stu-id="88116-137">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="88116-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="88116-138">-Name</span></span>
<span data-ttu-id="88116-139">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="88116-139">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88116-140">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88116-140">-Namespace</span></span>
<span data-ttu-id="88116-141">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88116-141">Namespace Name</span></span>

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

### <span data-ttu-id="88116-142">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="88116-142">-RequiresSession</span></span>
<span data-ttu-id="88116-143">RequiresSession: valore che indica se la coda richiede il rilevamento duplicato.</span><span class="sxs-lookup"><span data-stu-id="88116-143">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="88116-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88116-144">-ResourceGroupName</span></span>
<span data-ttu-id="88116-145">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="88116-145">The name of the resource group</span></span>

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

### <span data-ttu-id="88116-146">-Topic</span><span class="sxs-lookup"><span data-stu-id="88116-146">-Topic</span></span>
<span data-ttu-id="88116-147">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="88116-147">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88116-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88116-148">-WhatIf</span></span>
<span data-ttu-id="88116-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88116-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88116-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88116-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88116-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88116-151">CommonParameters</span></span>
<span data-ttu-id="88116-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88116-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="88116-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88116-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88116-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88116-154">INPUTS</span></span>

### <span data-ttu-id="88116-155">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88116-155">-ResourceGroup</span></span>
 <span data-ttu-id="88116-156">System. String</span><span class="sxs-lookup"><span data-stu-id="88116-156">System.String</span></span>
 

### <span data-ttu-id="88116-157">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="88116-157">-NamespaceName</span></span>
 <span data-ttu-id="88116-158">System. String</span><span class="sxs-lookup"><span data-stu-id="88116-158">System.String</span></span>
 

### <span data-ttu-id="88116-159">-TopicName</span><span class="sxs-lookup"><span data-stu-id="88116-159">-TopicName</span></span>
 <span data-ttu-id="88116-160">System. String</span><span class="sxs-lookup"><span data-stu-id="88116-160">System.String</span></span>
 

### <span data-ttu-id="88116-161">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="88116-161">-SubscriptionName</span></span>
 <span data-ttu-id="88116-162">System. String</span><span class="sxs-lookup"><span data-stu-id="88116-162">System.String</span></span>


## <span data-ttu-id="88116-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88116-163">OUTPUTS</span></span>

### <span data-ttu-id="88116-164">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="88116-164">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>


## <span data-ttu-id="88116-165">Note</span><span class="sxs-lookup"><span data-stu-id="88116-165">NOTES</span></span>

## <span data-ttu-id="88116-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88116-166">RELATED LINKS</span></span>
