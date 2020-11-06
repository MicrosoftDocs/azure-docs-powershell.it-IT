---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 3d99b261dc65af5d19a93acb575116a91c8a97fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520377"
---
# <span data-ttu-id="823a8-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="823a8-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="823a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="823a8-102">SYNOPSIS</span></span>
<span data-ttu-id="823a8-103">Restituisce una descrizione dell'abbonamento per l'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="823a8-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="823a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="823a8-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="823a8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="823a8-105">DESCRIPTION</span></span>
<span data-ttu-id="823a8-106">Il cmdlet **Get-AzureRmServiceBusSubscription** restituisce una descrizione dell'abbonamento per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="823a8-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="823a8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="823a8-107">EXAMPLES</span></span>

### <span data-ttu-id="823a8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="823a8-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="823a8-109">Restituisce una descrizione dell'abbonamento per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="823a8-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="823a8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="823a8-110">PARAMETERS</span></span>

### <span data-ttu-id="823a8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="823a8-111">-DefaultProfile</span></span>
<span data-ttu-id="823a8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="823a8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="823a8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="823a8-113">-Name</span></span>
<span data-ttu-id="823a8-114">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="823a8-114">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="823a8-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="823a8-115">-Namespace</span></span>
<span data-ttu-id="823a8-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="823a8-116">Namespace Name.</span></span>

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

### <span data-ttu-id="823a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="823a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="823a8-118">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="823a8-118">The name of the resource group</span></span>

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

### <span data-ttu-id="823a8-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="823a8-119">-Topic</span></span>
<span data-ttu-id="823a8-120">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="823a8-120">Topic Name.</span></span>

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

### <span data-ttu-id="823a8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="823a8-121">CommonParameters</span></span>
<span data-ttu-id="823a8-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="823a8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="823a8-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="823a8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="823a8-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="823a8-124">INPUTS</span></span>

### <span data-ttu-id="823a8-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="823a8-125">-ResourceGroup</span></span>
 <span data-ttu-id="823a8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="823a8-126">System.String</span></span>
 

### <span data-ttu-id="823a8-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="823a8-127">-NamespaceName</span></span>
 <span data-ttu-id="823a8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="823a8-128">System.String</span></span>
 

### <span data-ttu-id="823a8-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="823a8-129">-TopicName</span></span>
 <span data-ttu-id="823a8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="823a8-130">System.String</span></span>
 

### <span data-ttu-id="823a8-131">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="823a8-131">-SubscriptionName</span></span>
 <span data-ttu-id="823a8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="823a8-132">System.String</span></span>
 

## <span data-ttu-id="823a8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="823a8-133">OUTPUTS</span></span>

### <span data-ttu-id="823a8-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="823a8-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="823a8-135">Note</span><span class="sxs-lookup"><span data-stu-id="823a8-135">NOTES</span></span>

## <span data-ttu-id="823a8-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="823a8-136">RELATED LINKS</span></span>

