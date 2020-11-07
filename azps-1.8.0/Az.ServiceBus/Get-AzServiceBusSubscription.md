---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: bf6bd96314c8baf9e4d46b977b3f00457342db96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677153"
---
# <span data-ttu-id="841d0-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="841d0-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="841d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="841d0-102">SYNOPSIS</span></span>
<span data-ttu-id="841d0-103">Restituisce una descrizione dell'abbonamento per l'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="841d0-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="841d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="841d0-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="841d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="841d0-105">DESCRIPTION</span></span>
<span data-ttu-id="841d0-106">Il cmdlet **Get-AzServiceBusSubscription** restituisce una descrizione dell'abbonamento per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="841d0-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="841d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="841d0-107">EXAMPLES</span></span>

### <span data-ttu-id="841d0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="841d0-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="841d0-109">Restituisce una descrizione dell'abbonamento per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="841d0-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="841d0-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="841d0-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="841d0-111">Restituisce un elenco di abbonamenti per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="841d0-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="841d0-112">Per impostazione predefinita verranno restituiti gli abbonamenti a 100, per il numero di abbonamenti usare il parametro-MaxCount</span><span class="sxs-lookup"><span data-stu-id="841d0-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="841d0-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="841d0-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="841d0-114">Restituisce l'elenco dei primi abbonamenti a 150 per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="841d0-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="841d0-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="841d0-115">PARAMETERS</span></span>

### <span data-ttu-id="841d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="841d0-116">-DefaultProfile</span></span>
<span data-ttu-id="841d0-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="841d0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="841d0-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="841d0-118">-MaxCount</span></span>
<span data-ttu-id="841d0-119">Determinare il numero massimo di abbonamenti da restituire.</span><span class="sxs-lookup"><span data-stu-id="841d0-119">Determine the maximum number of Subscriptions to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="841d0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="841d0-120">-Name</span></span>
<span data-ttu-id="841d0-121">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="841d0-121">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="841d0-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="841d0-122">-Namespace</span></span>
<span data-ttu-id="841d0-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="841d0-123">Namespace Name</span></span>

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

### <span data-ttu-id="841d0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="841d0-124">-ResourceGroupName</span></span>
<span data-ttu-id="841d0-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="841d0-125">The name of the resource group</span></span>

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

### <span data-ttu-id="841d0-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="841d0-126">-Topic</span></span>
<span data-ttu-id="841d0-127">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="841d0-127">Topic Name</span></span>

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

### <span data-ttu-id="841d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="841d0-128">CommonParameters</span></span>
<span data-ttu-id="841d0-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="841d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="841d0-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="841d0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="841d0-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="841d0-131">INPUTS</span></span>

### <span data-ttu-id="841d0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="841d0-132">System.String</span></span>

## <span data-ttu-id="841d0-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="841d0-133">OUTPUTS</span></span>

### <span data-ttu-id="841d0-134">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="841d0-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="841d0-135">Note</span><span class="sxs-lookup"><span data-stu-id="841d0-135">NOTES</span></span>

## <span data-ttu-id="841d0-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="841d0-136">RELATED LINKS</span></span>