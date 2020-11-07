---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 2ed5d3345730e631b3f7668ca4b05f3decc04f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856169"
---
# <span data-ttu-id="af17d-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="af17d-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="af17d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af17d-102">SYNOPSIS</span></span>
<span data-ttu-id="af17d-103">Crea un abbonamento all'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="af17d-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="af17d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af17d-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af17d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af17d-105">DESCRIPTION</span></span>
<span data-ttu-id="af17d-106">Il cmdlet **New-AzServiceBusSubscription** crea un nuovo abbonamento all'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="af17d-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="af17d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af17d-107">EXAMPLES</span></span>

### <span data-ttu-id="af17d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="af17d-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="af17d-109">Crea la sottoscrizione `SB-TopicSubscription-Example1` per l'argomento Service Bus specificato `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="af17d-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="af17d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af17d-110">PARAMETERS</span></span>

### <span data-ttu-id="af17d-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="af17d-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="af17d-112">Specifica l'intervallo di inattività [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , dopo il quale l'abbonamento viene eliminato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="af17d-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="af17d-113">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="af17d-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="af17d-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="af17d-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="af17d-115">Valore che indica se un abbonamento ha il supporto di lettere morte per filtrare le eccezioni di valutazione.</span><span class="sxs-lookup"><span data-stu-id="af17d-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="af17d-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="af17d-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="af17d-117">Lettere morte nella scadenza del messaggio</span><span class="sxs-lookup"><span data-stu-id="af17d-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="af17d-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="af17d-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="af17d-119">TimeSpan in Live value.</span><span class="sxs-lookup"><span data-stu-id="af17d-119">Timespan to live value.</span></span>
<span data-ttu-id="af17d-120">Questa è la durata dopo la quale il messaggio scade, a partire da quando il messaggio viene inviato a Service Bus.</span><span class="sxs-lookup"><span data-stu-id="af17d-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="af17d-121">Questo è il valore predefinito usato quando TimeToLive non è impostato su un messaggio.</span><span class="sxs-lookup"><span data-stu-id="af17d-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="af17d-122">Per standard = TimeSpan. Max e Basic = 14 giorni</span><span class="sxs-lookup"><span data-stu-id="af17d-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="af17d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af17d-123">-DefaultProfile</span></span>
<span data-ttu-id="af17d-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af17d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af17d-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="af17d-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="af17d-126">Abilita operazioni in batch-valore che indica se le operazioni in batch sul lato server sono abilitate</span><span class="sxs-lookup"><span data-stu-id="af17d-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="af17d-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="af17d-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="af17d-128">Nome coda/argomento per inoltrare il messaggio di lettera morta</span><span class="sxs-lookup"><span data-stu-id="af17d-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="af17d-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="af17d-129">-ForwardTo</span></span>
<span data-ttu-id="af17d-130">Nome coda/argomento per inoltrare i messaggi</span><span class="sxs-lookup"><span data-stu-id="af17d-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="af17d-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="af17d-131">-LockDuration</span></span>
<span data-ttu-id="af17d-132">Durata del blocco</span><span class="sxs-lookup"><span data-stu-id="af17d-132">Lock Duration</span></span>

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

### <span data-ttu-id="af17d-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="af17d-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="af17d-134">MaxDeliveryCount-numero massimo di recapito.</span><span class="sxs-lookup"><span data-stu-id="af17d-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="af17d-135">Un messaggio viene automaticamente deadlettered dopo questo numero di consegne.</span><span class="sxs-lookup"><span data-stu-id="af17d-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="af17d-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="af17d-136">-Name</span></span>
<span data-ttu-id="af17d-137">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="af17d-137">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af17d-138">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af17d-138">-Namespace</span></span>
<span data-ttu-id="af17d-139">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af17d-139">Namespace Name</span></span>

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

### <span data-ttu-id="af17d-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="af17d-140">-RequiresSession</span></span>
<span data-ttu-id="af17d-141">RequiresSession: valore che indica se la coda richiede il rilevamento duplicato.</span><span class="sxs-lookup"><span data-stu-id="af17d-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="af17d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af17d-142">-ResourceGroupName</span></span>
<span data-ttu-id="af17d-143">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="af17d-143">The name of the resource group</span></span>

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

### <span data-ttu-id="af17d-144">-Topic</span><span class="sxs-lookup"><span data-stu-id="af17d-144">-Topic</span></span>
<span data-ttu-id="af17d-145">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="af17d-145">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af17d-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af17d-146">-Confirm</span></span>
<span data-ttu-id="af17d-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af17d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af17d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af17d-148">-WhatIf</span></span>
<span data-ttu-id="af17d-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af17d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af17d-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af17d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af17d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af17d-151">CommonParameters</span></span>
<span data-ttu-id="af17d-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af17d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af17d-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af17d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af17d-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af17d-154">INPUTS</span></span>

### <span data-ttu-id="af17d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="af17d-155">System.String</span></span>

### <span data-ttu-id="af17d-156">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af17d-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="af17d-157">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af17d-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="af17d-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af17d-158">OUTPUTS</span></span>

### <span data-ttu-id="af17d-159">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="af17d-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="af17d-160">Note</span><span class="sxs-lookup"><span data-stu-id="af17d-160">NOTES</span></span>

## <span data-ttu-id="af17d-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af17d-161">RELATED LINKS</span></span>
