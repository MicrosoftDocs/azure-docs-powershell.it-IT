---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: f1c3019b7d79330b1e4b0a26bd16f469eb794224
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339352"
---
# <span data-ttu-id="f7c28-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="f7c28-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="f7c28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7c28-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c28-103">Aggiorna la descrizione di una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="f7c28-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f7c28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7c28-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7c28-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7c28-105">DESCRIPTION</span></span>
<span data-ttu-id="f7c28-106">Il cmdlet **set-AzServiceBusQueue** aggiorna la descrizione della coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="f7c28-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f7c28-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7c28-107">EXAMPLES</span></span>

### <span data-ttu-id="f7c28-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7c28-108">Example 1</span></span>
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

<span data-ttu-id="f7c28-109">Aggiorna la coda specificata con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="f7c28-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="f7c28-110">Questo esempio aggiorna la proprietà **DeadLetteringOnMessageExpiration** su **true** e **SupportOrdering** su **true**.</span><span class="sxs-lookup"><span data-stu-id="f7c28-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="f7c28-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7c28-111">PARAMETERS</span></span>

### <span data-ttu-id="f7c28-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c28-112">-DefaultProfile</span></span>
<span data-ttu-id="f7c28-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7c28-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7c28-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7c28-114">-InputObject</span></span>
<span data-ttu-id="f7c28-115">Definizione di ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="f7c28-115">ServiceBus definition.</span></span>

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

### <span data-ttu-id="f7c28-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7c28-116">-Name</span></span>
<span data-ttu-id="f7c28-117">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="f7c28-117">Queue Name.</span></span>

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

### <span data-ttu-id="f7c28-118">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f7c28-118">-Namespace</span></span>
<span data-ttu-id="f7c28-119">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f7c28-119">Namespace Name.</span></span>

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

### <span data-ttu-id="f7c28-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7c28-120">-ResourceGroupName</span></span>
<span data-ttu-id="f7c28-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f7c28-121">The name of the resource group</span></span>

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

### <span data-ttu-id="f7c28-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7c28-122">-Confirm</span></span>
<span data-ttu-id="f7c28-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7c28-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7c28-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7c28-124">-WhatIf</span></span>
<span data-ttu-id="f7c28-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7c28-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7c28-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7c28-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7c28-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c28-127">CommonParameters</span></span>
<span data-ttu-id="f7c28-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7c28-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c28-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7c28-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c28-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7c28-130">INPUTS</span></span>

### <span data-ttu-id="f7c28-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f7c28-131">System.String</span></span>

### <span data-ttu-id="f7c28-132">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="f7c28-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="f7c28-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7c28-133">OUTPUTS</span></span>

### <span data-ttu-id="f7c28-134">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="f7c28-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="f7c28-135">Note</span><span class="sxs-lookup"><span data-stu-id="f7c28-135">NOTES</span></span>

## <span data-ttu-id="f7c28-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7c28-136">RELATED LINKS</span></span>
