---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 13e221c0205f07be81d01fd5011fa2d937b020a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687976"
---
# <span data-ttu-id="50b41-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="50b41-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="50b41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50b41-102">SYNOPSIS</span></span>
<span data-ttu-id="50b41-103">Aggiorna una descrizione dell'abbonamento per un argomento di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="50b41-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50b41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50b41-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -InputObject <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50b41-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50b41-105">DESCRIPTION</span></span>
<span data-ttu-id="50b41-106">Il cmdlet **set-AzureRmServiceBusSubscription** aggiorna la descrizione della sottoscrizione per l'argomento Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="50b41-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="50b41-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50b41-107">EXAMPLES</span></span>

### <span data-ttu-id="50b41-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50b41-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="50b41-109">Aggiorna la descrizione per la sottoscrizione specificata all'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="50b41-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="50b41-110">Questo esempio aggiorna la proprietà **DeadLetteringOnMessageExpiration** su **true** e **MaxDeliveryCount** su 9.</span><span class="sxs-lookup"><span data-stu-id="50b41-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="50b41-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50b41-111">PARAMETERS</span></span>

### <span data-ttu-id="50b41-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50b41-112">-Confirm</span></span>
<span data-ttu-id="50b41-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50b41-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50b41-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50b41-114">-WhatIf</span></span>
<span data-ttu-id="50b41-115">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50b41-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50b41-116">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50b41-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50b41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b41-117">-DefaultProfile</span></span>
<span data-ttu-id="50b41-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50b41-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50b41-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50b41-119">-InputObject</span></span>
<span data-ttu-id="50b41-120">Definizione dell'abbonamento a ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="50b41-120">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50b41-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="50b41-121">-Namespace</span></span>
<span data-ttu-id="50b41-122">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="50b41-122">Namespace Name.</span></span>

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

### <span data-ttu-id="50b41-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50b41-123">-ResourceGroupName</span></span>
<span data-ttu-id="50b41-124">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="50b41-124">The name of the resource group</span></span>

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

### <span data-ttu-id="50b41-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="50b41-125">-Topic</span></span>
<span data-ttu-id="50b41-126">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="50b41-126">Topic Name.</span></span>

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

### <span data-ttu-id="50b41-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b41-127">CommonParameters</span></span>
<span data-ttu-id="50b41-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50b41-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b41-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50b41-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b41-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50b41-130">INPUTS</span></span>

### <span data-ttu-id="50b41-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50b41-131">-ResourceGroup</span></span>
 <span data-ttu-id="50b41-132">System. String</span><span class="sxs-lookup"><span data-stu-id="50b41-132">System.String</span></span>

### <span data-ttu-id="50b41-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="50b41-133">-NamespaceName</span></span>
 <span data-ttu-id="50b41-134">System. String</span><span class="sxs-lookup"><span data-stu-id="50b41-134">System.String</span></span>

### <span data-ttu-id="50b41-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="50b41-135">-TopicName</span></span>
 <span data-ttu-id="50b41-136">System. String</span><span class="sxs-lookup"><span data-stu-id="50b41-136">System.String</span></span>

### <span data-ttu-id="50b41-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="50b41-137">-SubscriptionObj</span></span>
 <span data-ttu-id="50b41-138">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="50b41-138">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>

## <span data-ttu-id="50b41-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50b41-139">OUTPUTS</span></span>

### <span data-ttu-id="50b41-140">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="50b41-140">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="50b41-141">Nome: SB-TopicSubscription-esempio1 location: West US AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: CreatedAt: 1/20/2017 9:59:15 PM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: true EnableBatchedOperations: true EntityAvailabilityStatus: available IsReadOnly: LockDuration: 00:01:00 MaxDeliveryCount: 9 MessageCount: 0 RequiresSession: false status: Active UpdatedAt: 1/20/2017 9:59:15 PM</span><span class="sxs-lookup"><span data-stu-id="50b41-141">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : CreatedAt                                 : 1/20/2017 9:59:15 PM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : True EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 9 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 9:59:15 PM</span></span>

## <span data-ttu-id="50b41-142">Note</span><span class="sxs-lookup"><span data-stu-id="50b41-142">NOTES</span></span>

## <span data-ttu-id="50b41-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50b41-143">RELATED LINKS</span></span>

