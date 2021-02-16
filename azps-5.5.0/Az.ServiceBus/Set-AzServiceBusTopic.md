---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 8e8fe04476e66db6b45372879ac3176f9d492acc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183487"
---
# <span data-ttu-id="8158f-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="8158f-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="8158f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8158f-102">SYNOPSIS</span></span>
<span data-ttu-id="8158f-103">Aggiorna la descrizione di un argomento Bus di servizio nello spazio dei nomi dei bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="8158f-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8158f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8158f-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8158f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8158f-105">DESCRIPTION</span></span>
<span data-ttu-id="8158f-106">Il cmdlet **Set-AzServiceBusTopic** aggiorna un oggetto descrizione per un argomento Bus di servizio nello spazio dei nomi dei bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="8158f-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8158f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8158f-107">EXAMPLES</span></span>

### <span data-ttu-id="8158f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8158f-108">Example 1</span></span>
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

<span data-ttu-id="8158f-109">Aggiorna l'argomento specificato con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="8158f-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="8158f-110">Questo esempio aggiorna la **proprietà EnableExpress** a **true.**</span><span class="sxs-lookup"><span data-stu-id="8158f-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="8158f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8158f-111">PARAMETERS</span></span>

### <span data-ttu-id="8158f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8158f-112">-DefaultProfile</span></span>
<span data-ttu-id="8158f-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8158f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8158f-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8158f-114">-InputObject</span></span>
<span data-ttu-id="8158f-115">Definizione di argomento ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="8158f-115">ServiceBus Topic definition.</span></span>

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

### <span data-ttu-id="8158f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8158f-116">-Name</span></span>
<span data-ttu-id="8158f-117">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="8158f-117">Topic Name.</span></span>

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

### <span data-ttu-id="8158f-118">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8158f-118">-Namespace</span></span>
<span data-ttu-id="8158f-119">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8158f-119">Namespace Name.</span></span>

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

### <span data-ttu-id="8158f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8158f-120">-ResourceGroupName</span></span>
<span data-ttu-id="8158f-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8158f-121">The name of the resource group</span></span>

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

### <span data-ttu-id="8158f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8158f-122">-Confirm</span></span>
<span data-ttu-id="8158f-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8158f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8158f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8158f-124">-WhatIf</span></span>
<span data-ttu-id="8158f-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8158f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8158f-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8158f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8158f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8158f-127">CommonParameters</span></span>
<span data-ttu-id="8158f-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8158f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8158f-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8158f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8158f-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="8158f-130">INPUTS</span></span>

### <span data-ttu-id="8158f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8158f-131">System.String</span></span>

### <span data-ttu-id="8158f-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="8158f-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="8158f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8158f-133">OUTPUTS</span></span>

### <span data-ttu-id="8158f-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="8158f-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="8158f-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="8158f-135">NOTES</span></span>

## <span data-ttu-id="8158f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8158f-136">RELATED LINKS</span></span>
