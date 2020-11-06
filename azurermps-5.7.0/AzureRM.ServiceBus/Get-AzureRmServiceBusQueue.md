---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 967bc5c3126a0976096b6c9d9b6b76af8f0ef43e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512280"
---
# <span data-ttu-id="88ee0-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="88ee0-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="88ee0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="88ee0-103">Restituisce una descrizione per la coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="88ee0-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88ee0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88ee0-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88ee0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88ee0-105">DESCRIPTION</span></span>
<span data-ttu-id="88ee0-106">Il cmdlet **Get-AzureRmServiceBusQueue** restituisce una descrizione della coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="88ee0-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="88ee0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88ee0-107">EXAMPLES</span></span>

### <span data-ttu-id="88ee0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88ee0-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:35 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S
                                      B-Queue_example1
Name                                : SB-Queue_example1
Type                                : Microsoft.ServiceBus/Queues

```

<span data-ttu-id="88ee0-109">Restituisce la descrizione della coda.</span><span class="sxs-lookup"><span data-stu-id="88ee0-109">Returns the description of the queue.</span></span>

## <span data-ttu-id="88ee0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88ee0-110">PARAMETERS</span></span>

### <span data-ttu-id="88ee0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ee0-111">-DefaultProfile</span></span>
<span data-ttu-id="88ee0-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88ee0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88ee0-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="88ee0-113">-Name</span></span>
<span data-ttu-id="88ee0-114">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="88ee0-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ee0-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="88ee0-115">-Namespace</span></span>
<span data-ttu-id="88ee0-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="88ee0-116">Namespace Name.</span></span>

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

### <span data-ttu-id="88ee0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ee0-117">-ResourceGroupName</span></span>
<span data-ttu-id="88ee0-118">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="88ee0-118">The name of the resource group</span></span>

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

### <span data-ttu-id="88ee0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ee0-119">CommonParameters</span></span>
<span data-ttu-id="88ee0-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ee0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ee0-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88ee0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ee0-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88ee0-122">INPUTS</span></span>

### <span data-ttu-id="88ee0-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88ee0-123">-ResourceGroup</span></span>
 <span data-ttu-id="88ee0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="88ee0-124">System.String</span></span>
 

### <span data-ttu-id="88ee0-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="88ee0-125">-NamespaceName</span></span>
 <span data-ttu-id="88ee0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="88ee0-126">System.String</span></span>
 

### <span data-ttu-id="88ee0-127">-QueueName</span><span class="sxs-lookup"><span data-stu-id="88ee0-127">-QueueName</span></span>
 <span data-ttu-id="88ee0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="88ee0-128">System.String</span></span> 

## <span data-ttu-id="88ee0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88ee0-129">OUTPUTS</span></span>

### <span data-ttu-id="88ee0-130">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="88ee0-130">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="88ee0-131">Note</span><span class="sxs-lookup"><span data-stu-id="88ee0-131">NOTES</span></span>

## <span data-ttu-id="88ee0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88ee0-132">RELATED LINKS</span></span>

