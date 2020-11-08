---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: 2bff80a8f04dada3625eaa5b0a16287bb37c6a13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202604"
---
# <span data-ttu-id="8f071-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="8f071-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="8f071-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f071-102">SYNOPSIS</span></span>
<span data-ttu-id="8f071-103">Aggiorna una descrizione dell'abbonamento per un argomento di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="8f071-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8f071-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f071-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f071-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f071-105">DESCRIPTION</span></span>
<span data-ttu-id="8f071-106">Il cmdlet **set-AzServiceBusSubscription** aggiorna la descrizione della sottoscrizione per l'argomento Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="8f071-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8f071-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f071-107">EXAMPLES</span></span>

### <span data-ttu-id="8f071-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8f071-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : 
CreatedAt                                 : 1/20/2017 9:59:15 PM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : True
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 9
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 9:59:15 PM
PS C:\> Set-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="8f071-109">Aggiorna la descrizione per la sottoscrizione specificata all'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="8f071-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="8f071-110">Questo esempio aggiorna la proprietà **DeadLetteringOnMessageExpiration** su **true** e **MaxDeliveryCount** su 9.</span><span class="sxs-lookup"><span data-stu-id="8f071-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="8f071-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f071-111">PARAMETERS</span></span>

### <span data-ttu-id="8f071-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f071-112">-DefaultProfile</span></span>
<span data-ttu-id="8f071-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f071-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f071-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f071-114">-InputObject</span></span>
<span data-ttu-id="8f071-115">Definizione dell'abbonamento a ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="8f071-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f071-116">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8f071-116">-Namespace</span></span>
<span data-ttu-id="8f071-117">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8f071-117">Namespace Name.</span></span>

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

### <span data-ttu-id="8f071-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f071-118">-ResourceGroupName</span></span>
<span data-ttu-id="8f071-119">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8f071-119">The name of the resource group</span></span>

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

### <span data-ttu-id="8f071-120">-Topic</span><span class="sxs-lookup"><span data-stu-id="8f071-120">-Topic</span></span>
<span data-ttu-id="8f071-121">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="8f071-121">Topic Name.</span></span>

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

### <span data-ttu-id="8f071-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8f071-122">-Confirm</span></span>
<span data-ttu-id="8f071-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f071-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f071-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f071-124">-WhatIf</span></span>
<span data-ttu-id="8f071-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f071-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f071-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f071-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f071-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f071-127">CommonParameters</span></span>
<span data-ttu-id="8f071-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f071-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f071-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f071-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f071-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f071-130">INPUTS</span></span>

### <span data-ttu-id="8f071-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8f071-131">System.String</span></span>

### <span data-ttu-id="8f071-132">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="8f071-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="8f071-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f071-133">OUTPUTS</span></span>

### <span data-ttu-id="8f071-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="8f071-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="8f071-135">Note</span><span class="sxs-lookup"><span data-stu-id="8f071-135">NOTES</span></span>

## <span data-ttu-id="8f071-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f071-136">RELATED LINKS</span></span>
