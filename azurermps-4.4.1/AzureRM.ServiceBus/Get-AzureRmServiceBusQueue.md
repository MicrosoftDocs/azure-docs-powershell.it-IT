---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: d90d93548e46f3586319b0acf96319fe24e298af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521141"
---
# <span data-ttu-id="8954c-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="8954c-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="8954c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8954c-102">SYNOPSIS</span></span>
<span data-ttu-id="8954c-103">Restituisce una descrizione per la coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="8954c-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8954c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8954c-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8954c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8954c-105">DESCRIPTION</span></span>
<span data-ttu-id="8954c-106">Il cmdlet **Get-AzureRmServiceBusQueue** restituisce una descrizione della coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="8954c-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="8954c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8954c-107">EXAMPLES</span></span>

### <span data-ttu-id="8954c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8954c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1
```

<span data-ttu-id="8954c-109">Restituisce la descrizione della coda.</span><span class="sxs-lookup"><span data-stu-id="8954c-109">Returns the description of the queue.</span></span> 

## <span data-ttu-id="8954c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8954c-110">PARAMETERS</span></span>

### <span data-ttu-id="8954c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8954c-111">-DefaultProfile</span></span>
<span data-ttu-id="8954c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8954c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8954c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8954c-113">-Name</span></span>
<span data-ttu-id="8954c-114">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="8954c-114">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8954c-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8954c-115">-Namespace</span></span>
<span data-ttu-id="8954c-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8954c-116">Namespace Name.</span></span>

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

### <span data-ttu-id="8954c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8954c-117">-ResourceGroupName</span></span>
<span data-ttu-id="8954c-118">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8954c-118">The name of the resource group</span></span>

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

### <span data-ttu-id="8954c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8954c-119">CommonParameters</span></span>
<span data-ttu-id="8954c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8954c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8954c-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8954c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8954c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8954c-122">INPUTS</span></span>

### <span data-ttu-id="8954c-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8954c-123">-ResourceGroup</span></span>
 <span data-ttu-id="8954c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8954c-124">System.String</span></span>
 

### <span data-ttu-id="8954c-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8954c-125">-NamespaceName</span></span>
 <span data-ttu-id="8954c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8954c-126">System.String</span></span>
 

### <span data-ttu-id="8954c-127">-QueueName</span><span class="sxs-lookup"><span data-stu-id="8954c-127">-QueueName</span></span>
 <span data-ttu-id="8954c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8954c-128">System.String</span></span> 

## <span data-ttu-id="8954c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8954c-129">OUTPUTS</span></span>

### <span data-ttu-id="8954c-130">Microsoft. Azure. Commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="8954c-130">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="8954c-131">LockDuration: AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:35 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false EnablePartitioning: true IsAnonymousAccessible: false MaxDeliveryCount: MaxSizeInMegabytes: 16384 MessageCount: CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails RequiresDuplicateDetection: false RequiresSession: false SizeInBytes: status: Active SupportOrdering: false UpdatedAt: 1/20/2017 2:51:37 AM ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S B-Queue_example1 nome: SB-Queue_example1 tipo: Microsoft. ServiceBus/Codes location: West US</span><span class="sxs-lookup"><span data-stu-id="8954c-131">LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:35 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S B-Queue_example1 Name                                : SB-Queue_example1 Type                                : Microsoft.ServiceBus/Queues Location                            : West US</span></span>

## <span data-ttu-id="8954c-132">Note</span><span class="sxs-lookup"><span data-stu-id="8954c-132">NOTES</span></span>

## <span data-ttu-id="8954c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8954c-133">RELATED LINKS</span></span>

