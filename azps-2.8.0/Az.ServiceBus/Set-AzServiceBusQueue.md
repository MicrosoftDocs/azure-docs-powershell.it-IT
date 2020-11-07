---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: 4206e29ad56e1d7b48b9d87a66b8a85960c4707e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854601"
---
# <span data-ttu-id="af439-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="af439-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="af439-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af439-102">SYNOPSIS</span></span>
<span data-ttu-id="af439-103">Aggiorna la descrizione di una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="af439-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="af439-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af439-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af439-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af439-105">DESCRIPTION</span></span>
<span data-ttu-id="af439-106">Il cmdlet **set-AzServiceBusQueue** aggiorna la descrizione della coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="af439-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="af439-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af439-107">EXAMPLES</span></span>

### <span data-ttu-id="af439-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="af439-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

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

<span data-ttu-id="af439-109">Aggiorna la coda specificata con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="af439-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="af439-110">Questo esempio aggiorna la proprietà **DeadLetteringOnMessageExpiration** su **true** e **SupportOrdering** su **true**.</span><span class="sxs-lookup"><span data-stu-id="af439-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="af439-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af439-111">PARAMETERS</span></span>

### <span data-ttu-id="af439-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af439-112">-DefaultProfile</span></span>
<span data-ttu-id="af439-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af439-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af439-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af439-114">-InputObject</span></span>
<span data-ttu-id="af439-115">Definizione di ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="af439-115">ServiceBus definition.</span></span>

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

### <span data-ttu-id="af439-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="af439-116">-Name</span></span>
<span data-ttu-id="af439-117">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="af439-117">Queue Name.</span></span>

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

### <span data-ttu-id="af439-118">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af439-118">-Namespace</span></span>
<span data-ttu-id="af439-119">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="af439-119">Namespace Name.</span></span>

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

### <span data-ttu-id="af439-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af439-120">-ResourceGroupName</span></span>
<span data-ttu-id="af439-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="af439-121">The name of the resource group</span></span>

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

### <span data-ttu-id="af439-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af439-122">-Confirm</span></span>
<span data-ttu-id="af439-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af439-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af439-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af439-124">-WhatIf</span></span>
<span data-ttu-id="af439-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af439-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af439-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af439-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af439-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af439-127">CommonParameters</span></span>
<span data-ttu-id="af439-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af439-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af439-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af439-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af439-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af439-130">INPUTS</span></span>

### <span data-ttu-id="af439-131">System. String</span><span class="sxs-lookup"><span data-stu-id="af439-131">System.String</span></span>

### <span data-ttu-id="af439-132">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="af439-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="af439-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af439-133">OUTPUTS</span></span>

### <span data-ttu-id="af439-134">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="af439-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="af439-135">Note</span><span class="sxs-lookup"><span data-stu-id="af439-135">NOTES</span></span>

## <span data-ttu-id="af439-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af439-136">RELATED LINKS</span></span>
