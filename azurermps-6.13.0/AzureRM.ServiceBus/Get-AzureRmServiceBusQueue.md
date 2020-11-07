---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 25a64b352622cf9c057ce0e3f38bc3e4e122e22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686360"
---
# <span data-ttu-id="b4119-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="b4119-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="b4119-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4119-102">SYNOPSIS</span></span>
<span data-ttu-id="b4119-103">Restituisce una descrizione per la coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="b4119-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4119-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4119-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4119-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4119-105">DESCRIPTION</span></span>
<span data-ttu-id="b4119-106">Restituisce una descrizione per la coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="b4119-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="b4119-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4119-107">EXAMPLES</span></span>

### <span data-ttu-id="b4119-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b4119-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:11 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="b4119-109">Restituisce la descrizione della coda.</span><span class="sxs-lookup"><span data-stu-id="b4119-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="b4119-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b4119-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="b4119-111">Restituisce l'elenco delle code per lo spazio dei nomi specificato, per impostazione predefinita verranno restituite le code di 100, se vengono restituite più di 100 code, usare il parametro-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="b4119-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="b4119-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b4119-112">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="b4119-113">Restituisce l'elenco delle prime code di 150 per lo spazio dei nomi specificato</span><span class="sxs-lookup"><span data-stu-id="b4119-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="b4119-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4119-114">PARAMETERS</span></span>

### <span data-ttu-id="b4119-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4119-115">-DefaultProfile</span></span>
<span data-ttu-id="b4119-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4119-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4119-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b4119-117">-MaxCount</span></span>
<span data-ttu-id="b4119-118">Determinare il numero massimo di code da restituire.</span><span class="sxs-lookup"><span data-stu-id="b4119-118">Determine the maximum number of Queues to return.</span></span>

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

### <span data-ttu-id="b4119-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4119-119">-Name</span></span>
<span data-ttu-id="b4119-120">Nome coda</span><span class="sxs-lookup"><span data-stu-id="b4119-120">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4119-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b4119-121">-Namespace</span></span>
<span data-ttu-id="b4119-122">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b4119-122">Namespace Name</span></span>

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

### <span data-ttu-id="b4119-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4119-123">-ResourceGroupName</span></span>
<span data-ttu-id="b4119-124">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b4119-124">The name of the resource group</span></span>

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

### <span data-ttu-id="b4119-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4119-125">CommonParameters</span></span>
<span data-ttu-id="b4119-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4119-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4119-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4119-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4119-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4119-128">INPUTS</span></span>

### <span data-ttu-id="b4119-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b4119-129">System.String</span></span>

## <span data-ttu-id="b4119-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4119-130">OUTPUTS</span></span>

### <span data-ttu-id="b4119-131">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="b4119-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="b4119-132">Note</span><span class="sxs-lookup"><span data-stu-id="b4119-132">NOTES</span></span>

## <span data-ttu-id="b4119-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4119-133">RELATED LINKS</span></span>
