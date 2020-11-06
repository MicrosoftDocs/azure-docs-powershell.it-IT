---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: b08b4d9bd201f8a29ef878a4aaa73c926eb47151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516475"
---
# <span data-ttu-id="fa830-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="fa830-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="fa830-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa830-102">SYNOPSIS</span></span>
<span data-ttu-id="fa830-103">Aggiorna la descrizione di un argomento di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="fa830-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa830-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa830-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa830-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa830-105">DESCRIPTION</span></span>
<span data-ttu-id="fa830-106">Il cmdlet **set-AzureRmServiceBusTopic** aggiorna un oggetto Description per un argomento di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="fa830-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fa830-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa830-107">EXAMPLES</span></span>

### <span data-ttu-id="fa830-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fa830-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-ExampleStandard/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/12/2018 12:01:28 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : False
UpdatedAt                           : 10/12/2018 12:01:29 AM
```

<span data-ttu-id="fa830-109">Aggiorna l'argomento specificato con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="fa830-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="fa830-110">Questo esempio aggiorna la proprietà **EnableExpress** su **true**.</span><span class="sxs-lookup"><span data-stu-id="fa830-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="fa830-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa830-111">PARAMETERS</span></span>

### <span data-ttu-id="fa830-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa830-112">-DefaultProfile</span></span>
<span data-ttu-id="fa830-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa830-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa830-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa830-114">-InputObject</span></span>
<span data-ttu-id="fa830-115">Definizione dell'argomento ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="fa830-115">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa830-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa830-116">-Name</span></span>
<span data-ttu-id="fa830-117">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="fa830-117">Topic Name.</span></span>

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

### <span data-ttu-id="fa830-118">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fa830-118">-Namespace</span></span>
<span data-ttu-id="fa830-119">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fa830-119">Namespace Name.</span></span>

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

### <span data-ttu-id="fa830-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa830-120">-ResourceGroupName</span></span>
<span data-ttu-id="fa830-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fa830-121">The name of the resource group</span></span>

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

### <span data-ttu-id="fa830-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fa830-122">-Confirm</span></span>
<span data-ttu-id="fa830-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa830-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa830-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa830-124">-WhatIf</span></span>
<span data-ttu-id="fa830-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa830-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa830-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa830-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa830-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa830-127">CommonParameters</span></span>
<span data-ttu-id="fa830-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa830-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa830-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa830-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa830-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa830-130">INPUTS</span></span>

### <span data-ttu-id="fa830-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fa830-131">System.String</span></span>

### <span data-ttu-id="fa830-132">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="fa830-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="fa830-133">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fa830-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fa830-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa830-134">OUTPUTS</span></span>

### <span data-ttu-id="fa830-135">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="fa830-135">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="fa830-136">Note</span><span class="sxs-lookup"><span data-stu-id="fa830-136">NOTES</span></span>

## <span data-ttu-id="fa830-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa830-137">RELATED LINKS</span></span>
