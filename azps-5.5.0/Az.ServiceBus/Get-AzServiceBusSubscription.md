---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: a2a535dd9607b3018b7fe215f152bbeeb01b8858
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208155"
---
# <span data-ttu-id="ed6db-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="ed6db-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="ed6db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed6db-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6db-103">Restituisce una descrizione della sottoscrizione per l'argomento specificato.</span><span class="sxs-lookup"><span data-stu-id="ed6db-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="ed6db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed6db-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed6db-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ed6db-105">DESCRIPTION</span></span>
<span data-ttu-id="ed6db-106">Il cmdlet **Get-AzServiceBusSubscription** restituisce una descrizione della sottoscrizione per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="ed6db-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="ed6db-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed6db-107">EXAMPLES</span></span>

### <span data-ttu-id="ed6db-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed6db-108">Example 1</span></span>
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

<span data-ttu-id="ed6db-109">Restituisce una descrizione della sottoscrizione per l'argomento Bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="ed6db-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="ed6db-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ed6db-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="ed6db-111">Restituisce l'elenco delle sottoscrizioni per l'argomento del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="ed6db-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="ed6db-112">Per impostazione predefinita vengono restituiti 100 abbonamenti, per il numero di abbonamenti usa il parametro -MaxCount</span><span class="sxs-lookup"><span data-stu-id="ed6db-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="ed6db-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ed6db-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="ed6db-114">Restituisce l'elenco dei primi 150 abbonamenti per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="ed6db-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="ed6db-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed6db-115">PARAMETERS</span></span>

### <span data-ttu-id="ed6db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6db-116">-DefaultProfile</span></span>
<span data-ttu-id="ed6db-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed6db-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed6db-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ed6db-118">-MaxCount</span></span>
<span data-ttu-id="ed6db-119">Determinare il numero massimo di sottoscrizioni da restituire.</span><span class="sxs-lookup"><span data-stu-id="ed6db-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="ed6db-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ed6db-120">-Name</span></span>
<span data-ttu-id="ed6db-121">Nome abbonamento</span><span class="sxs-lookup"><span data-stu-id="ed6db-121">Subscription Name</span></span>

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

### <span data-ttu-id="ed6db-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed6db-122">-Namespace</span></span>
<span data-ttu-id="ed6db-123">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed6db-123">Namespace Name</span></span>

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

### <span data-ttu-id="ed6db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed6db-124">-ResourceGroupName</span></span>
<span data-ttu-id="ed6db-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ed6db-125">The name of the resource group</span></span>

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

### <span data-ttu-id="ed6db-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="ed6db-126">-Topic</span></span>
<span data-ttu-id="ed6db-127">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="ed6db-127">Topic Name</span></span>

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

### <span data-ttu-id="ed6db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6db-128">CommonParameters</span></span>
<span data-ttu-id="ed6db-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed6db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6db-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed6db-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6db-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="ed6db-131">INPUTS</span></span>

### <span data-ttu-id="ed6db-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ed6db-132">System.String</span></span>

## <span data-ttu-id="ed6db-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed6db-133">OUTPUTS</span></span>

### <span data-ttu-id="ed6db-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="ed6db-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="ed6db-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="ed6db-135">NOTES</span></span>

## <span data-ttu-id="ed6db-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed6db-136">RELATED LINKS</span></span>
