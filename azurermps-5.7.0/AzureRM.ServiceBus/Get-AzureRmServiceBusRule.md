---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 3eb629665f8bc4ed030b5c616410fb47455136e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520378"
---
# <span data-ttu-id="64dc3-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="64dc3-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="64dc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="64dc3-103">Ottiene una descrizione della regola specificata per una determinata sottoscrizione di argomenti.</span><span class="sxs-lookup"><span data-stu-id="64dc3-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64dc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64dc3-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64dc3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64dc3-105">DESCRIPTION</span></span>
<span data-ttu-id="64dc3-106">Il cmdlet **Get-AzureRmServiceBusRule** ottiene la descrizione della regola specificata nell'abbonamento specificato di topic.</span><span class="sxs-lookup"><span data-stu-id="64dc3-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="64dc3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64dc3-107">EXAMPLES</span></span>

### <span data-ttu-id="64dc3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="64dc3-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="64dc3-109">Restituisce la descrizione della regola specificata per un abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="64dc3-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="64dc3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64dc3-110">PARAMETERS</span></span>

### <span data-ttu-id="64dc3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64dc3-111">-DefaultProfile</span></span>
<span data-ttu-id="64dc3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64dc3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64dc3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="64dc3-113">-Name</span></span>
<span data-ttu-id="64dc3-114">Nome della regola.</span><span class="sxs-lookup"><span data-stu-id="64dc3-114">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64dc3-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="64dc3-115">-Namespace</span></span>
<span data-ttu-id="64dc3-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="64dc3-116">Namespace Name.</span></span>

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

### <span data-ttu-id="64dc3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64dc3-117">-ResourceGroupName</span></span>
<span data-ttu-id="64dc3-118">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="64dc3-118">The name of the resource group</span></span>

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

### <span data-ttu-id="64dc3-119">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="64dc3-119">-Subscription</span></span>
<span data-ttu-id="64dc3-120">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="64dc3-120">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64dc3-121">-Topic</span><span class="sxs-lookup"><span data-stu-id="64dc3-121">-Topic</span></span>
<span data-ttu-id="64dc3-122">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="64dc3-122">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64dc3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64dc3-123">CommonParameters</span></span>
<span data-ttu-id="64dc3-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64dc3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64dc3-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64dc3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64dc3-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64dc3-126">INPUTS</span></span>

### <span data-ttu-id="64dc3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="64dc3-127">System.String</span></span>

## <span data-ttu-id="64dc3-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64dc3-128">OUTPUTS</span></span>

### <span data-ttu-id="64dc3-129">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="64dc3-129">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="64dc3-130">Note</span><span class="sxs-lookup"><span data-stu-id="64dc3-130">NOTES</span></span>

## <span data-ttu-id="64dc3-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64dc3-131">RELATED LINKS</span></span>

