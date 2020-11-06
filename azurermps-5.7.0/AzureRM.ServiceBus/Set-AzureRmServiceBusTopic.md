---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 92c26b2b92257de7cdd3bbbb0d602d45d8ea1d1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512272"
---
# <span data-ttu-id="4d7c3-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="4d7c3-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="4d7c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d7c3-102">SYNOPSIS</span></span>
<span data-ttu-id="4d7c3-103">Aggiorna la descrizione di un argomento di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d7c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d7c3-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d7c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d7c3-105">DESCRIPTION</span></span>
<span data-ttu-id="4d7c3-106">Il cmdlet **set-AzureRmServiceBusTopic** aggiorna un oggetto Description per un argomento di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="4d7c3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d7c3-107">EXAMPLES</span></span>

### <span data-ttu-id="4d7c3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d7c3-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-
                                      Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : True
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 7:12:16 PM
```
<span data-ttu-id="4d7c3-109">Aggiorna l'argomento specificato con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="4d7c3-110">Questo esempio aggiorna la proprietà **EnableExpress** su **true**.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="4d7c3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d7c3-111">PARAMETERS</span></span>

### <span data-ttu-id="4d7c3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d7c3-112">-DefaultProfile</span></span>
<span data-ttu-id="4d7c3-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d7c3-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d7c3-114">-InputObject</span></span>
<span data-ttu-id="4d7c3-115">Definizione dell'argomento ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-115">ServiceBus Topic definition.</span></span>

```yaml
Type: PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7c3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d7c3-116">-Name</span></span>
<span data-ttu-id="4d7c3-117">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-117">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7c3-118">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4d7c3-118">-Namespace</span></span>
<span data-ttu-id="4d7c3-119">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-119">Namespace Name.</span></span>

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

### <span data-ttu-id="4d7c3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d7c3-120">-ResourceGroupName</span></span>
<span data-ttu-id="4d7c3-121">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4d7c3-121">The name of the resource group</span></span>

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

### <span data-ttu-id="4d7c3-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d7c3-122">-Confirm</span></span>
<span data-ttu-id="4d7c3-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7c3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d7c3-124">-WhatIf</span></span>
<span data-ttu-id="4d7c3-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d7c3-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7c3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d7c3-127">CommonParameters</span></span>
<span data-ttu-id="4d7c3-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d7c3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d7c3-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d7c3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d7c3-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d7c3-130">INPUTS</span></span>

### <span data-ttu-id="4d7c3-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d7c3-131">-ResourceGroup</span></span>
 <span data-ttu-id="4d7c3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4d7c3-132">System.String</span></span>

### <span data-ttu-id="4d7c3-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4d7c3-133">-NamespaceName</span></span>
 <span data-ttu-id="4d7c3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4d7c3-134">System.String</span></span>

### <span data-ttu-id="4d7c3-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="4d7c3-135">-TopicName</span></span>
 <span data-ttu-id="4d7c3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4d7c3-136">System.String</span></span>

### <span data-ttu-id="4d7c3-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="4d7c3-137">-TopicObj</span></span>
 <span data-ttu-id="4d7c3-138">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="4d7c3-138">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="4d7c3-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d7c3-139">OUTPUTS</span></span>

### <span data-ttu-id="4d7c3-140">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="4d7c3-140">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="4d7c3-141">Note</span><span class="sxs-lookup"><span data-stu-id="4d7c3-141">NOTES</span></span>

## <span data-ttu-id="4d7c3-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d7c3-142">RELATED LINKS</span></span>

