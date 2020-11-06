---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: e09e4f19a63eef1cd4b87760239d4456afee70fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510335"
---
# <span data-ttu-id="ae846-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="ae846-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="ae846-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae846-102">SYNOPSIS</span></span>
<span data-ttu-id="ae846-103">Ottiene una descrizione della regola specificata per una determinata sottoscrizione di argomenti.</span><span class="sxs-lookup"><span data-stu-id="ae846-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae846-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae846-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae846-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae846-105">DESCRIPTION</span></span>
<span data-ttu-id="ae846-106">Il cmdlet **Get-AzureRmServiceBusRule** ottiene la descrizione della regola specificata nell'abbonamento specificato di topic.</span><span class="sxs-lookup"><span data-stu-id="ae846-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="ae846-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae846-107">EXAMPLES</span></span>

### <span data-ttu-id="ae846-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ae846-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="ae846-109">Restituisce la descrizione della regola specificata per un abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="ae846-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="ae846-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae846-110">PARAMETERS</span></span>

### <span data-ttu-id="ae846-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae846-111">-Name</span></span>
<span data-ttu-id="ae846-112">Nome della regola.</span><span class="sxs-lookup"><span data-stu-id="ae846-112">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae846-113">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ae846-113">-Namespace</span></span>
<span data-ttu-id="ae846-114">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ae846-114">Namespace Name.</span></span>

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

### <span data-ttu-id="ae846-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae846-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae846-116">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ae846-116">The name of the resource group</span></span>

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

### <span data-ttu-id="ae846-117">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="ae846-117">-Subscription</span></span>
<span data-ttu-id="ae846-118">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ae846-118">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae846-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="ae846-119">-Topic</span></span>
<span data-ttu-id="ae846-120">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="ae846-120">Topic Name.</span></span>

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

### <span data-ttu-id="ae846-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae846-121">-DefaultProfile</span></span>
<span data-ttu-id="ae846-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae846-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae846-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae846-123">CommonParameters</span></span>
<span data-ttu-id="ae846-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae846-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae846-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae846-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae846-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae846-126">INPUTS</span></span>

### <span data-ttu-id="ae846-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ae846-127">System.String</span></span>

## <span data-ttu-id="ae846-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae846-128">OUTPUTS</span></span>

### <span data-ttu-id="ae846-129">Microsoft. Azure. Commands. ServiceBus. Models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="ae846-129">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="ae846-130">Note</span><span class="sxs-lookup"><span data-stu-id="ae846-130">NOTES</span></span>

## <span data-ttu-id="ae846-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae846-131">RELATED LINKS</span></span>

