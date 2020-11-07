---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8c02c596b1b1eecb8654b07a2392d2336c0b0215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685908"
---
# <span data-ttu-id="9799a-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="9799a-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="9799a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9799a-102">SYNOPSIS</span></span>
<span data-ttu-id="9799a-103">Aggiorna la descrizione di una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="9799a-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9799a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9799a-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9799a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9799a-105">DESCRIPTION</span></span>
<span data-ttu-id="9799a-106">Il cmdlet **set-AzureRmServiceBusQueue** aggiorna la descrizione della coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="9799a-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9799a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9799a-107">EXAMPLES</span></span>

### <span data-ttu-id="9799a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9799a-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1
Name                                : SB-Queue_exampl1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 1/1/0001 12:00:00 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : True
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
UpdatedAt                           : 1/1/0001 12:00:00 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="9799a-109">Aggiorna la coda specificata con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="9799a-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="9799a-110">Questo esempio aggiorna la proprietà **DeadLetteringOnMessageExpiration** su **true** e **SupportOrdering** su **true**.</span><span class="sxs-lookup"><span data-stu-id="9799a-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="9799a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9799a-111">PARAMETERS</span></span>

### <span data-ttu-id="9799a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9799a-112">-DefaultProfile</span></span>
<span data-ttu-id="9799a-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9799a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9799a-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9799a-114">-InputObject</span></span>
<span data-ttu-id="9799a-115">Definizione di ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="9799a-115">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9799a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9799a-116">-Name</span></span>
<span data-ttu-id="9799a-117">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="9799a-117">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9799a-118">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9799a-118">-Namespace</span></span>
<span data-ttu-id="9799a-119">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9799a-119">Namespace Name.</span></span>

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

### <span data-ttu-id="9799a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9799a-120">-ResourceGroupName</span></span>
<span data-ttu-id="9799a-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9799a-121">The name of the resource group</span></span>

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

### <span data-ttu-id="9799a-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9799a-122">-Confirm</span></span>
<span data-ttu-id="9799a-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9799a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9799a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9799a-124">-WhatIf</span></span>
<span data-ttu-id="9799a-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9799a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9799a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9799a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9799a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9799a-127">CommonParameters</span></span>
<span data-ttu-id="9799a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9799a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9799a-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9799a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9799a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9799a-130">INPUTS</span></span>

### <span data-ttu-id="9799a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9799a-131">System.String</span></span>

### <span data-ttu-id="9799a-132">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="9799a-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="9799a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9799a-133">OUTPUTS</span></span>

### <span data-ttu-id="9799a-134">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="9799a-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="9799a-135">Note</span><span class="sxs-lookup"><span data-stu-id="9799a-135">NOTES</span></span>

## <span data-ttu-id="9799a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9799a-136">RELATED LINKS</span></span>
