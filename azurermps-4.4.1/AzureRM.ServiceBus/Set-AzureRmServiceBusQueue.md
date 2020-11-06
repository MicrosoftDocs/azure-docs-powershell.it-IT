---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: cd291e6c33dd08668c7a78f2c739f65c576e2f0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521133"
---
# <span data-ttu-id="62135-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="62135-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="62135-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62135-102">SYNOPSIS</span></span>
<span data-ttu-id="62135-103">Aggiorna la descrizione di una coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="62135-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62135-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62135-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62135-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62135-105">DESCRIPTION</span></span>
<span data-ttu-id="62135-106">Il cmdlet **set-AzureRmServiceBusQueue** aggiorna la descrizione della coda di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="62135-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="62135-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62135-107">EXAMPLES</span></span>

### <span data-ttu-id="62135-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62135-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj
```

<span data-ttu-id="62135-109">Aggiorna la coda specificata con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="62135-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="62135-110">Questo esempio aggiorna la proprietà **DeadLetteringOnMessageExpiration** su **true** e **SupportOrdering** su **true**.</span><span class="sxs-lookup"><span data-stu-id="62135-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="62135-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62135-111">PARAMETERS</span></span>

### <span data-ttu-id="62135-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62135-112">-Confirm</span></span>
<span data-ttu-id="62135-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62135-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62135-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62135-114">-WhatIf</span></span>
<span data-ttu-id="62135-115">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62135-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62135-116">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62135-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62135-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62135-117">-DefaultProfile</span></span>
<span data-ttu-id="62135-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62135-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62135-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62135-119">-InputObject</span></span>
<span data-ttu-id="62135-120">Definizione di ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="62135-120">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62135-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="62135-121">-Name</span></span>
<span data-ttu-id="62135-122">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="62135-122">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62135-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="62135-123">-Namespace</span></span>
<span data-ttu-id="62135-124">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="62135-124">Namespace Name.</span></span>

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

### <span data-ttu-id="62135-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62135-125">-ResourceGroupName</span></span>
<span data-ttu-id="62135-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="62135-126">The name of the resource group</span></span>

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

### <span data-ttu-id="62135-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62135-127">CommonParameters</span></span>
<span data-ttu-id="62135-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62135-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62135-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62135-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62135-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62135-130">INPUTS</span></span>

### <span data-ttu-id="62135-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="62135-131">-ResourceGroup</span></span>
 <span data-ttu-id="62135-132">System. String</span><span class="sxs-lookup"><span data-stu-id="62135-132">System.String</span></span>

### <span data-ttu-id="62135-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="62135-133">-NamespaceName</span></span>
 <span data-ttu-id="62135-134">System. String</span><span class="sxs-lookup"><span data-stu-id="62135-134">System.String</span></span>

### <span data-ttu-id="62135-135">-QueueName</span><span class="sxs-lookup"><span data-stu-id="62135-135">-QueueName</span></span>
 <span data-ttu-id="62135-136">System. String</span><span class="sxs-lookup"><span data-stu-id="62135-136">System.String</span></span>

### <span data-ttu-id="62135-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="62135-137">-QueueObj</span></span>
 <span data-ttu-id="62135-138">Microsoft. Azure. Commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="62135-138">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>

## <span data-ttu-id="62135-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62135-139">OUTPUTS</span></span>

### <span data-ttu-id="62135-140">Microsoft. Azure. Commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="62135-140">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="62135-141">Nome: SB-Queue_exampl1 località: West US LockDuration: AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:34 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false EnablePartitioning: true IsAnonymousAccessible: MaxDeliveryCount: false MaxSizeInMegabytes: MessageCount: 16384 CountDetails: MessageCountDetails: Microsoft. Azure. Management. ServiceBus. Models. RequiresDuplicateDetection RequiresSession: false sizeInBytes: false SupportOrdering: status: Active UpdatedAt 1/20/2017 6:16:18</span><span class="sxs-lookup"><span data-stu-id="62135-141">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:34 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 6:16:18 PM</span></span>

## <span data-ttu-id="62135-142">Note</span><span class="sxs-lookup"><span data-stu-id="62135-142">NOTES</span></span>

## <span data-ttu-id="62135-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62135-143">RELATED LINKS</span></span>

