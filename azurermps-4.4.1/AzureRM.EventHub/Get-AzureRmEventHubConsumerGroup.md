---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521676"
---
# <span data-ttu-id="6fa6f-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6fa6f-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="6fa6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6fa6f-102">SYNOPSIS</span></span>
<span data-ttu-id="6fa6f-103">Ottiene i dettagli di un gruppo di utenti hub di eventi specificato oppure ottiene un elenco di gruppi consumer in un hub eventi.</span><span class="sxs-lookup"><span data-stu-id="6fa6f-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fa6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fa6f-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## <span data-ttu-id="6fa6f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fa6f-105">DESCRIPTION</span></span>
<span data-ttu-id="6fa6f-106">Il cmdlet Get-AzureRmEventHubConsumerGroup ottiene i dettagli di un gruppo di utenti hub eventi specificato o un elenco di gruppi consumer in un hub di eventi specifico.</span><span class="sxs-lookup"><span data-stu-id="6fa6f-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="6fa6f-107">Se viene fornito il nome di un gruppo di utenti, vengono restituiti i dettagli di un singolo dettaglio del gruppo consumer.</span><span class="sxs-lookup"><span data-stu-id="6fa6f-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="6fa6f-108">Se il nome di un gruppo di utenti non è disponibile, viene restituito un elenco di gruppi consumer nell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="6fa6f-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="6fa6f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fa6f-109">EXAMPLES</span></span>

### <span data-ttu-id="6fa6f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6fa6f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="6fa6f-111">Ottiene il gruppo Consumer \` MyConsumerGroupName \` nell'hub dell'evento \` MyEventHubName \` , disponibile nello spazio dei nomi MyNamespace \` con il \` gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6fa6f-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6fa6f-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6fa6f-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="6fa6f-113">Ottiene un elenco di gruppi consumer nell'hub dell'evento \` MyEventHubName \` , disponibile nello spazio dei nomi MyNamespace \` con il \` gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6fa6f-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6fa6f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6fa6f-114">PARAMETERS</span></span>

### <span data-ttu-id="6fa6f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fa6f-115">-ResourceGroupName</span></span>
<span data-ttu-id="6fa6f-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6fa6f-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa6f-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6fa6f-117">-EventHub</span></span>
<span data-ttu-id="6fa6f-118">Nome EventHub.</span><span class="sxs-lookup"><span data-stu-id="6fa6f-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa6f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fa6f-119">-Name</span></span>
<span data-ttu-id="6fa6f-120">Nome ConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="6fa6f-120">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fa6f-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6fa6f-121">-Namespace</span></span>
<span data-ttu-id="6fa6f-122">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6fa6f-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="6fa6f-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6fa6f-123">INPUTS</span></span>

### <span data-ttu-id="6fa6f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6fa6f-124">System.String</span></span>

## <span data-ttu-id="6fa6f-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fa6f-125">OUTPUTS</span></span>

### <span data-ttu-id="6fa6f-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventHub. Models. ConsumerGroupAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6fa6f-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6fa6f-127">Note</span><span class="sxs-lookup"><span data-stu-id="6fa6f-127">NOTES</span></span>

## <span data-ttu-id="6fa6f-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fa6f-128">RELATED LINKS</span></span>

