---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 9949757f82d6aa48d3981a10fa23eb32526dba8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988817"
---
# <span data-ttu-id="320aa-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="320aa-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="320aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="320aa-102">SYNOPSIS</span></span>
<span data-ttu-id="320aa-103">Aggiorna la descrizione di un argomento Bus di servizio nello spazio dei nomi dei bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="320aa-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="320aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="320aa-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="320aa-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="320aa-105">DESCRIPTION</span></span>
<span data-ttu-id="320aa-106">Il cmdlet **Set-AzServiceBusTopic** aggiorna un oggetto descrizione per un argomento Bus di servizio nello spazio dei nomi dei bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="320aa-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="320aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="320aa-107">EXAMPLES</span></span>

### <span data-ttu-id="320aa-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="320aa-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

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

<span data-ttu-id="320aa-109">Aggiorna l'argomento specificato con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="320aa-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="320aa-110">Questo esempio aggiorna la **proprietà EnableExpress** a **true.**</span><span class="sxs-lookup"><span data-stu-id="320aa-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="320aa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="320aa-111">PARAMETERS</span></span>

### <span data-ttu-id="320aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320aa-112">-DefaultProfile</span></span>
<span data-ttu-id="320aa-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="320aa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="320aa-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="320aa-114">-InputObject</span></span>
<span data-ttu-id="320aa-115">Definizione di argomento ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="320aa-115">ServiceBus Topic definition.</span></span>

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

### <span data-ttu-id="320aa-116">-Name</span><span class="sxs-lookup"><span data-stu-id="320aa-116">-Name</span></span>
<span data-ttu-id="320aa-117">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="320aa-117">Topic Name.</span></span>

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

### <span data-ttu-id="320aa-118">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="320aa-118">-Namespace</span></span>
<span data-ttu-id="320aa-119">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="320aa-119">Namespace Name.</span></span>

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

### <span data-ttu-id="320aa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320aa-120">-ResourceGroupName</span></span>
<span data-ttu-id="320aa-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="320aa-121">The name of the resource group</span></span>

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

### <span data-ttu-id="320aa-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="320aa-122">-Confirm</span></span>
<span data-ttu-id="320aa-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="320aa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320aa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320aa-124">-WhatIf</span></span>
<span data-ttu-id="320aa-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="320aa-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320aa-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="320aa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320aa-127">CommonParameters</span></span>
<span data-ttu-id="320aa-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320aa-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="320aa-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320aa-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="320aa-130">INPUTS</span></span>

### <span data-ttu-id="320aa-131">System.String</span><span class="sxs-lookup"><span data-stu-id="320aa-131">System.String</span></span>

### <span data-ttu-id="320aa-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="320aa-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="320aa-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="320aa-133">OUTPUTS</span></span>

### <span data-ttu-id="320aa-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="320aa-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="320aa-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="320aa-135">NOTES</span></span>

## <span data-ttu-id="320aa-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="320aa-136">RELATED LINKS</span></span>
