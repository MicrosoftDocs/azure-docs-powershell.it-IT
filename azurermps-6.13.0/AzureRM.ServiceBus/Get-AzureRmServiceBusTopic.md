---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: ddccdb907dac89466a81be62e104202a3e59a672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519694"
---
# <span data-ttu-id="08414-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="08414-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="08414-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08414-102">SYNOPSIS</span></span>
<span data-ttu-id="08414-103">Restituisce una descrizione per l'argomento Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="08414-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08414-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08414-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08414-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08414-105">DESCRIPTION</span></span>
<span data-ttu-id="08414-106">Il cmdlet **Get-AzureRmServiceBusTopic** restituisce una descrizione dell'argomento per lo spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="08414-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="08414-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08414-107">EXAMPLES</span></span>

### <span data-ttu-id="08414-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08414-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="08414-109">Restituisce la descrizione dell'argomento specificato per lo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="08414-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="08414-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="08414-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="08414-111">Restituisce un elenco di argomenti per lo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="08414-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="08414-112">Per impostazione predefinita verranno restituiti gli argomenti di 100, se sono più di 100 argomenti da restituire, usare il parametro-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="08414-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="08414-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="08414-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="08414-114">Restituisce l'elenco dei primi argomenti di 150 per lo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="08414-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="08414-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08414-115">PARAMETERS</span></span>

### <span data-ttu-id="08414-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08414-116">-DefaultProfile</span></span>
<span data-ttu-id="08414-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08414-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08414-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="08414-118">-MaxCount</span></span>
<span data-ttu-id="08414-119">Determinare il numero massimo di argomenti da restituire.</span><span class="sxs-lookup"><span data-stu-id="08414-119">Determine the maximum number of Topics to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08414-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="08414-120">-Name</span></span>
<span data-ttu-id="08414-121">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="08414-121">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08414-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="08414-122">-Namespace</span></span>
<span data-ttu-id="08414-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="08414-123">Namespace Name</span></span>

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

### <span data-ttu-id="08414-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08414-124">-ResourceGroupName</span></span>
<span data-ttu-id="08414-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="08414-125">The name of the resource group</span></span>

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

### <span data-ttu-id="08414-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08414-126">CommonParameters</span></span>
<span data-ttu-id="08414-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08414-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08414-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08414-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08414-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08414-129">INPUTS</span></span>

### <span data-ttu-id="08414-130">System. String</span><span class="sxs-lookup"><span data-stu-id="08414-130">System.String</span></span>

## <span data-ttu-id="08414-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08414-131">OUTPUTS</span></span>

### <span data-ttu-id="08414-132">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="08414-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="08414-133">Note</span><span class="sxs-lookup"><span data-stu-id="08414-133">NOTES</span></span>

## <span data-ttu-id="08414-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08414-134">RELATED LINKS</span></span>
