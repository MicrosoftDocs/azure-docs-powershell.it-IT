---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 4b346d1ef4757d74ac9c663f5c72a134d5c48153
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516003"
---
# <span data-ttu-id="ca112-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ca112-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="ca112-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca112-102">SYNOPSIS</span></span>
<span data-ttu-id="ca112-103">Aggiorna la descrizione di un argomento di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="ca112-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca112-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca112-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -InputObject <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca112-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca112-105">DESCRIPTION</span></span>
<span data-ttu-id="ca112-106">Il cmdlet **set-AzureRmServiceBusTopic** aggiorna un oggetto Description per un argomento di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="ca112-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ca112-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca112-107">EXAMPLES</span></span>

### <span data-ttu-id="ca112-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ca112-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj
```

<span data-ttu-id="ca112-109">Aggiorna l'argomento specificato con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="ca112-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="ca112-110">Questo esempio aggiorna la proprietà **EnableExpress** su **true**.</span><span class="sxs-lookup"><span data-stu-id="ca112-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="ca112-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca112-111">PARAMETERS</span></span>

### <span data-ttu-id="ca112-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca112-112">-Confirm</span></span>
<span data-ttu-id="ca112-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca112-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca112-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca112-114">-WhatIf</span></span>
<span data-ttu-id="ca112-115">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca112-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca112-116">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca112-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca112-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca112-117">-DefaultProfile</span></span>
<span data-ttu-id="ca112-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca112-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca112-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca112-119">-InputObject</span></span>
<span data-ttu-id="ca112-120">Definizione dell'argomento ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="ca112-120">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca112-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca112-121">-Name</span></span>
<span data-ttu-id="ca112-122">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="ca112-122">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca112-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca112-123">-Namespace</span></span>
<span data-ttu-id="ca112-124">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ca112-124">Namespace Name.</span></span>

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

### <span data-ttu-id="ca112-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca112-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca112-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ca112-126">The name of the resource group</span></span>

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

### <span data-ttu-id="ca112-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca112-127">CommonParameters</span></span>
<span data-ttu-id="ca112-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca112-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca112-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca112-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca112-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca112-130">INPUTS</span></span>

### <span data-ttu-id="ca112-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca112-131">-ResourceGroup</span></span>
 <span data-ttu-id="ca112-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ca112-132">System.String</span></span>

### <span data-ttu-id="ca112-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ca112-133">-NamespaceName</span></span>
 <span data-ttu-id="ca112-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ca112-134">System.String</span></span>

### <span data-ttu-id="ca112-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ca112-135">-TopicName</span></span>
 <span data-ttu-id="ca112-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ca112-136">System.String</span></span>

### <span data-ttu-id="ca112-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="ca112-137">-TopicObj</span></span>
 <span data-ttu-id="ca112-138">Microsoft. Azure. Commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ca112-138">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>

## <span data-ttu-id="ca112-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca112-139">OUTPUTS</span></span>

### <span data-ttu-id="ca112-140">Microsoft. Azure. Commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ca112-140">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="ca112-141">Nome: SB-Topic_exampl1 posizione: ID ovest degli Stati Uniti:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1 tipo: Microsoft. ServiceBus/topic AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 AM CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: true EnablePartitioning: true EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: false IsAnonymousAccessible: false Express: false MaxSizeInMegabytes: 16384 RequiresDuplicateDetection: false SizeInBytes: 0 status: Active SubscriptionCount: 1 SupportOrdering: false UpdatedAt: 1/20/2017 7:12:16 PM</span><span class="sxs-lookup"><span data-stu-id="ca112-141">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB- Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : True EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 7:12:16 PM</span></span>

## <span data-ttu-id="ca112-142">Note</span><span class="sxs-lookup"><span data-stu-id="ca112-142">NOTES</span></span>

## <span data-ttu-id="ca112-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca112-143">RELATED LINKS</span></span>

