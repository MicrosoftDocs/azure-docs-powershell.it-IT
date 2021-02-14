---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusTopic.md
ms.openlocfilehash: 3d688362932f61bdea9d685b98f2cba757288da2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208147"
---
# <span data-ttu-id="718a5-101">Get-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="718a5-101">Get-AzServiceBusTopic</span></span>

## <span data-ttu-id="718a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="718a5-102">SYNOPSIS</span></span>
<span data-ttu-id="718a5-103">Restituisce una descrizione per l'argomento Bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="718a5-103">Returns a description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="718a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="718a5-104">SYNTAX</span></span>

```
Get-AzServiceBusTopic [-ResourceGroupName <String>] [-Namespace <String>] [-Name <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="718a5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="718a5-105">DESCRIPTION</span></span>
<span data-ttu-id="718a5-106">Il **cmdlet Get-AzServiceBusTopic** restituisce una descrizione dell'argomento per lo spazio dei nomi del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="718a5-106">The **Get-AzServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="718a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="718a5-107">EXAMPLES</span></span>

### <span data-ttu-id="718a5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="718a5-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

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

<span data-ttu-id="718a5-109">Restituisce la descrizione dell'argomento specificato per lo spazio dei nomi del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="718a5-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

### <span data-ttu-id="718a5-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="718a5-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="718a5-111">Restituisce l'elenco di argomenti per lo spazio dei nomi del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="718a5-111">Returns list of topics for given Service Bus namespace.</span></span> <span data-ttu-id="718a5-112">Per impostazione predefinita vengono restituiti 100 argomenti, se devono essere restituiti più di 100 argomenti, usare il parametro -MaxCount.</span><span class="sxs-lookup"><span data-stu-id="718a5-112">By default 100 topics will be returned, if more than 100 topics to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="718a5-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="718a5-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="718a5-114">Restituisce l'elenco dei primi 150 argomenti per lo spazio dei nomi dei bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="718a5-114">Returns list of first 150 topics for given Service Bus namespace.</span></span>

## <span data-ttu-id="718a5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="718a5-115">PARAMETERS</span></span>

### <span data-ttu-id="718a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718a5-116">-DefaultProfile</span></span>
<span data-ttu-id="718a5-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="718a5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="718a5-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="718a5-118">-MaxCount</span></span>
<span data-ttu-id="718a5-119">Determinare il numero massimo di argomenti da restituire.</span><span class="sxs-lookup"><span data-stu-id="718a5-119">Determine the maximum number of Topics to return.</span></span>

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

### <span data-ttu-id="718a5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="718a5-120">-Name</span></span>
<span data-ttu-id="718a5-121">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="718a5-121">Topic Name</span></span>

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

### <span data-ttu-id="718a5-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="718a5-122">-Namespace</span></span>
<span data-ttu-id="718a5-123">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="718a5-123">Namespace Name</span></span>

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

### <span data-ttu-id="718a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="718a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="718a5-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="718a5-125">The name of the resource group</span></span>

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

### <span data-ttu-id="718a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718a5-126">CommonParameters</span></span>
<span data-ttu-id="718a5-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="718a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718a5-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="718a5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718a5-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="718a5-129">INPUTS</span></span>

### <span data-ttu-id="718a5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="718a5-130">System.String</span></span>

## <span data-ttu-id="718a5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="718a5-131">OUTPUTS</span></span>

### <span data-ttu-id="718a5-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="718a5-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="718a5-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="718a5-133">NOTES</span></span>

## <span data-ttu-id="718a5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="718a5-134">RELATED LINKS</span></span>
