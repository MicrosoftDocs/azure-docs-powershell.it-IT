---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 53f91cb6904cb8c481a5379d5499805ffe82ce33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208130"
---
# <span data-ttu-id="ae6bf-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="ae6bf-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="ae6bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6bf-103">Crea una sottoscrizione all'argomento bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="ae6bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae6bf-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae6bf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ae6bf-105">DESCRIPTION</span></span>
<span data-ttu-id="ae6bf-106">Il cmdlet **New-AzServiceBusSubscription** crea una nuova sottoscrizione all'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="ae6bf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae6bf-107">EXAMPLES</span></span>

### <span data-ttu-id="ae6bf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ae6bf-108">Example 1</span></span>
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

<span data-ttu-id="ae6bf-109">Crea la sottoscrizione `SB-TopicSubscription-Example1` per l'argomento bus di servizio `SB-Topic_exampl1` specificato.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="ae6bf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae6bf-110">PARAMETERS</span></span>

### <span data-ttu-id="ae6bf-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="ae6bf-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="ae6bf-112">Specifica l'intervallo di inattività di [TimeSpan,](https://msdn.microsoft.com/library/system.timespan.aspx) dopo il quale la sottoscrizione viene eliminata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="ae6bf-113">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="ae6bf-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="ae6bf-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="ae6bf-115">Valore che indica se un abbonamento supporta la lettera non recapitata alle eccezioni di valutazione del filtro.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="ae6bf-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="ae6bf-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="ae6bf-117">Lettere erre alla scadenza del messaggio</span><span class="sxs-lookup"><span data-stu-id="ae6bf-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="ae6bf-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="ae6bf-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="ae6bf-119">Timespan to live value.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-119">Timespan to live value.</span></span>
<span data-ttu-id="ae6bf-120">Si tratta della durata dopo la quale il messaggio scade, a partire dal momento in cui viene inviato al bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="ae6bf-121">Si tratta del valore predefinito usato quando TimeToLive non è impostato su un messaggio stesso.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="ae6bf-122">Per Standard = Timespan.Max e Basic = 14 giorni</span><span class="sxs-lookup"><span data-stu-id="ae6bf-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="ae6bf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6bf-123">-DefaultProfile</span></span>
<span data-ttu-id="ae6bf-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae6bf-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="ae6bf-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="ae6bf-126">Enable Batched Operations: valore che indica se le operazioni in batch sul lato server sono abilitate</span><span class="sxs-lookup"><span data-stu-id="ae6bf-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="ae6bf-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="ae6bf-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="ae6bf-128">Queue/Topic name to forward the Dead Letter message</span><span class="sxs-lookup"><span data-stu-id="ae6bf-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="ae6bf-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="ae6bf-129">-ForwardTo</span></span>
<span data-ttu-id="ae6bf-130">Nome della coda/argomento per inoltrare i messaggi</span><span class="sxs-lookup"><span data-stu-id="ae6bf-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="ae6bf-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="ae6bf-131">-LockDuration</span></span>
<span data-ttu-id="ae6bf-132">Durata blocco</span><span class="sxs-lookup"><span data-stu-id="ae6bf-132">Lock Duration</span></span>

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

### <span data-ttu-id="ae6bf-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="ae6bf-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="ae6bf-134">MaxDeliveryCount: numero massimo di consegne.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="ae6bf-135">Un messaggio viene automaticamente recapitato dopo questo numero di consegne.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="ae6bf-136">-Name</span><span class="sxs-lookup"><span data-stu-id="ae6bf-136">-Name</span></span>
<span data-ttu-id="ae6bf-137">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="ae6bf-137">Subscription Name</span></span>

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

### <span data-ttu-id="ae6bf-138">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ae6bf-138">-Namespace</span></span>
<span data-ttu-id="ae6bf-139">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ae6bf-139">Namespace Name</span></span>

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

### <span data-ttu-id="ae6bf-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="ae6bf-140">-RequiresSession</span></span>
<span data-ttu-id="ae6bf-141">RequiresSession: valore che indica se questa coda richiede il rilevamento di duplicati.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="ae6bf-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae6bf-142">-ResourceGroupName</span></span>
<span data-ttu-id="ae6bf-143">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ae6bf-143">The name of the resource group</span></span>

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

### <span data-ttu-id="ae6bf-144">-Topic</span><span class="sxs-lookup"><span data-stu-id="ae6bf-144">-Topic</span></span>
<span data-ttu-id="ae6bf-145">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="ae6bf-145">Topic Name</span></span>

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

### <span data-ttu-id="ae6bf-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae6bf-146">-Confirm</span></span>
<span data-ttu-id="ae6bf-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae6bf-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae6bf-148">-WhatIf</span></span>
<span data-ttu-id="ae6bf-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae6bf-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae6bf-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6bf-151">CommonParameters</span></span>
<span data-ttu-id="ae6bf-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae6bf-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6bf-153">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae6bf-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6bf-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="ae6bf-154">INPUTS</span></span>

### <span data-ttu-id="ae6bf-155">System.String</span><span class="sxs-lookup"><span data-stu-id="ae6bf-155">System.String</span></span>

### <span data-ttu-id="ae6bf-156">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ae6bf-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ae6bf-157">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ae6bf-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ae6bf-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae6bf-158">OUTPUTS</span></span>

### <span data-ttu-id="ae6bf-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="ae6bf-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="ae6bf-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="ae6bf-160">NOTES</span></span>

## <span data-ttu-id="ae6bf-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae6bf-161">RELATED LINKS</span></span>
