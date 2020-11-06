---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: ea305b334e6efd4cb1c5af47db2a1b8817e7cab6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516008"
---
# <span data-ttu-id="d0b24-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="d0b24-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="d0b24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0b24-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b24-103">Crea un abbonamento all'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="d0b24-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0b24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0b24-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnFilterEvaluationExceptions <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>]
 [-EnableBatchedOperations <Boolean>] [-IsReadOnly <Boolean>] [-LockDuration <String>]
 [-MaxDeliveryCount <Int32>] [-RequiresSession <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0b24-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0b24-105">DESCRIPTION</span></span>
<span data-ttu-id="d0b24-106">Il cmdlet **New-AzureRmServiceBusSubscription** crea un nuovo abbonamento all'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="d0b24-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="d0b24-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0b24-107">EXAMPLES</span></span>

### <span data-ttu-id="d0b24-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d0b24-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="d0b24-109">Crea la sottoscrizione `SB-TopicSubscription-Example1` per l'argomento Service Bus specificato `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="d0b24-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="d0b24-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0b24-110">PARAMETERS</span></span>

### <span data-ttu-id="d0b24-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="d0b24-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="d0b24-112">Specifica l'intervallo di inattività [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , dopo il quale l'abbonamento viene eliminato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d0b24-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="d0b24-113">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="d0b24-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="d0b24-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="d0b24-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="d0b24-115">Indica se un abbonamento ha il supporto di lettere morte per filtrare le eccezioni di valutazione.</span><span class="sxs-lookup"><span data-stu-id="d0b24-115">Indicates if a subscription has dead letter support on Filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="d0b24-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="d0b24-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="d0b24-117">Indica se un abbonamento ha il supporto di DeadLetter quando scade un messaggio.</span><span class="sxs-lookup"><span data-stu-id="d0b24-117">Indicates if a subscription has deadletter support when a message expires.</span></span>

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

### <span data-ttu-id="d0b24-118">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="d0b24-118">-EnableBatchedOperations</span></span>
<span data-ttu-id="d0b24-119">Indica se le operazioni in batch sul lato server sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="d0b24-119">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="d0b24-120">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="d0b24-120">-IsReadOnly</span></span>
<span data-ttu-id="d0b24-121">Indica se la descrizione dell'entità è di sola lettura</span><span class="sxs-lookup"><span data-stu-id="d0b24-121">Indicates whether the entity description is read-only</span></span>

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

### <span data-ttu-id="d0b24-122">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="d0b24-122">-LockDuration</span></span>
<span data-ttu-id="d0b24-123">Specifica l'intervallo di tempo di blocco per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d0b24-123">Specifies the lock duration time span for the subscription.</span></span>

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

### <span data-ttu-id="d0b24-124">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="d0b24-124">-MaxDeliveryCount</span></span>
<span data-ttu-id="d0b24-125">Specifica il numero di consegne massime.</span><span class="sxs-lookup"><span data-stu-id="d0b24-125">Specifies the number of maximum deliveries.</span></span> <span data-ttu-id="d0b24-126">Un messaggio viene automaticamente deadlettered dopo questo numero di consegne.</span><span class="sxs-lookup"><span data-stu-id="d0b24-126">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="d0b24-127">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="d0b24-127">-RequiresSession</span></span>
<span data-ttu-id="d0b24-128">Specifica se un abbonamento supporta il concetto di sessioni.</span><span class="sxs-lookup"><span data-stu-id="d0b24-128">Specifies whether a subscription supports the concept of sessions.</span></span>

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

### <span data-ttu-id="d0b24-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0b24-129">-Confirm</span></span>
<span data-ttu-id="d0b24-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0b24-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0b24-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0b24-131">-WhatIf</span></span>
<span data-ttu-id="d0b24-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0b24-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0b24-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0b24-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0b24-134">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="d0b24-134">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="d0b24-135">TimeSpan in Live value.</span><span class="sxs-lookup"><span data-stu-id="d0b24-135">Timespan to live value.</span></span> <span data-ttu-id="d0b24-136">Questa è la durata dopo la quale il messaggio scade, a partire da quando il messaggio viene inviato a Service Bus.</span><span class="sxs-lookup"><span data-stu-id="d0b24-136">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span> <span data-ttu-id="d0b24-137">Questo è il valore predefinito usato quando TimeToLive non è impostato su un messaggio.</span><span class="sxs-lookup"><span data-stu-id="d0b24-137">This is the default value used when TimeToLive is not set on a message itself.</span></span> <span data-ttu-id="d0b24-138">Per standard = TimeSpan. Max e Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="d0b24-138">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="d0b24-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b24-139">-DefaultProfile</span></span>
<span data-ttu-id="d0b24-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b24-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0b24-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0b24-141">-Name</span></span>
<span data-ttu-id="d0b24-142">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="d0b24-142">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b24-143">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d0b24-143">-Namespace</span></span>
<span data-ttu-id="d0b24-144">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="d0b24-144">Namespace Name.</span></span>

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

### <span data-ttu-id="d0b24-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0b24-145">-ResourceGroupName</span></span>
<span data-ttu-id="d0b24-146">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d0b24-146">The name of the resource group</span></span>

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

### <span data-ttu-id="d0b24-147">-Topic</span><span class="sxs-lookup"><span data-stu-id="d0b24-147">-Topic</span></span>
<span data-ttu-id="d0b24-148">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="d0b24-148">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b24-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b24-149">CommonParameters</span></span>
<span data-ttu-id="d0b24-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b24-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b24-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0b24-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b24-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0b24-152">INPUTS</span></span>

### <span data-ttu-id="d0b24-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d0b24-153">-ResourceGroup</span></span>
 <span data-ttu-id="d0b24-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d0b24-154">System.String</span></span>
 

### <span data-ttu-id="d0b24-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d0b24-155">-NamespaceName</span></span>
 <span data-ttu-id="d0b24-156">System. String</span><span class="sxs-lookup"><span data-stu-id="d0b24-156">System.String</span></span>
 

### <span data-ttu-id="d0b24-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="d0b24-157">-TopicName</span></span>
 <span data-ttu-id="d0b24-158">System. String</span><span class="sxs-lookup"><span data-stu-id="d0b24-158">System.String</span></span>
 

### <span data-ttu-id="d0b24-159">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="d0b24-159">-SubscriptionName</span></span>
 <span data-ttu-id="d0b24-160">System. String</span><span class="sxs-lookup"><span data-stu-id="d0b24-160">System.String</span></span>

## <span data-ttu-id="d0b24-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0b24-161">OUTPUTS</span></span>

### <span data-ttu-id="d0b24-162">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="d0b24-162">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="d0b24-163">Nome: SB-TopicSubscription-esempio1 location: West US AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: false EnableBatchedOperations: true EntityAvailabilityStatus: available IsReadOnly: LockDuration: 00:01:00 MaxDeliveryCount: 10 MessageCount: 0 RequiresSession: false status: Active UpdatedAt: 1/20/2017 3:18:54 AM</span><span class="sxs-lookup"><span data-stu-id="d0b24-163">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="d0b24-164">Note</span><span class="sxs-lookup"><span data-stu-id="d0b24-164">NOTES</span></span>

## <span data-ttu-id="d0b24-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0b24-165">RELATED LINKS</span></span>

