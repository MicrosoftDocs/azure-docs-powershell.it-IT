---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 0e0f6a824571ab529daa576e5f3f9a4cbff08264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510336"
---
# <span data-ttu-id="acf1e-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="acf1e-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="acf1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="acf1e-102">SYNOPSIS</span></span>
<span data-ttu-id="acf1e-103">Restituisce una descrizione dell'abbonamento per l'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="acf1e-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acf1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acf1e-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acf1e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acf1e-105">DESCRIPTION</span></span>
<span data-ttu-id="acf1e-106">Il cmdlet **Get-AzureRmServiceBusSubscription** restituisce una descrizione dell'abbonamento per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="acf1e-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="acf1e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acf1e-107">EXAMPLES</span></span>

### <span data-ttu-id="acf1e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="acf1e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="acf1e-109">Restituisce una descrizione dell'abbonamento per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="acf1e-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="acf1e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="acf1e-110">PARAMETERS</span></span>

### <span data-ttu-id="acf1e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf1e-111">-DefaultProfile</span></span>
<span data-ttu-id="acf1e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acf1e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acf1e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="acf1e-113">-Name</span></span>
<span data-ttu-id="acf1e-114">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="acf1e-114">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf1e-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="acf1e-115">-Namespace</span></span>
<span data-ttu-id="acf1e-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="acf1e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="acf1e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf1e-117">-ResourceGroupName</span></span>
<span data-ttu-id="acf1e-118">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="acf1e-118">The name of the resource group</span></span>

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

### <span data-ttu-id="acf1e-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="acf1e-119">-Topic</span></span>
<span data-ttu-id="acf1e-120">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="acf1e-120">Topic Name.</span></span>

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

### <span data-ttu-id="acf1e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf1e-121">CommonParameters</span></span>
<span data-ttu-id="acf1e-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf1e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf1e-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf1e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf1e-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="acf1e-124">INPUTS</span></span>

### <span data-ttu-id="acf1e-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="acf1e-125">-ResourceGroup</span></span>
 <span data-ttu-id="acf1e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="acf1e-126">System.String</span></span>
 

### <span data-ttu-id="acf1e-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="acf1e-127">-NamespaceName</span></span>
 <span data-ttu-id="acf1e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="acf1e-128">System.String</span></span>
 

### <span data-ttu-id="acf1e-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="acf1e-129">-TopicName</span></span>
 <span data-ttu-id="acf1e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="acf1e-130">System.String</span></span>
 

### <span data-ttu-id="acf1e-131">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="acf1e-131">-SubscriptionName</span></span>
 <span data-ttu-id="acf1e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="acf1e-132">System.String</span></span>
 

## <span data-ttu-id="acf1e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acf1e-133">OUTPUTS</span></span>

### <span data-ttu-id="acf1e-134">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="acf1e-134">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="acf1e-135">Nome: SB-TopicSubscription-esempio1 location: West US AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: false EnableBatchedOperations: true EntityAvailabilityStatus: available IsReadOnly: LockDuration: 00:01:00 MaxDeliveryCount: 10 MessageCount: 0 RequiresSession: false status: Active UpdatedAt: 1/20/2017 3:18:54 AM</span><span class="sxs-lookup"><span data-stu-id="acf1e-135">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="acf1e-136">Note</span><span class="sxs-lookup"><span data-stu-id="acf1e-136">NOTES</span></span>

## <span data-ttu-id="acf1e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acf1e-137">RELATED LINKS</span></span>

