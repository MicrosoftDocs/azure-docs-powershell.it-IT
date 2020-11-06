---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 445d20453b9f3d99e4ff5c72e118b287f0a83898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520456"
---
# <span data-ttu-id="06cc6-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="06cc6-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="06cc6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="06cc6-103">Ottiene i dettagli di un gruppo di utenti hub di eventi specificato oppure ottiene un elenco di gruppi consumer in un hub eventi.</span><span class="sxs-lookup"><span data-stu-id="06cc6-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06cc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06cc6-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06cc6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06cc6-105">DESCRIPTION</span></span>
<span data-ttu-id="06cc6-106">Il cmdlet Get-AzureRmEventHubConsumerGroup ottiene i dettagli di un gruppo di utenti hub eventi specificato o un elenco di gruppi consumer in un hub di eventi specifico.</span><span class="sxs-lookup"><span data-stu-id="06cc6-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="06cc6-107">Se viene fornito il nome di un gruppo di utenti, vengono restituiti i dettagli di un singolo dettaglio del gruppo consumer.</span><span class="sxs-lookup"><span data-stu-id="06cc6-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="06cc6-108">Se il nome di un gruppo di utenti non è disponibile, viene restituito un elenco di gruppi consumer nell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="06cc6-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="06cc6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06cc6-109">EXAMPLES</span></span>

### <span data-ttu-id="06cc6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06cc6-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="06cc6-111">Ottiene il gruppo Consumer \` MyConsumerGroupName \` nell'hub dell'evento \` MyEventHubName \` , disponibile nello spazio dei nomi MyNamespace \` con il \` gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="06cc6-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="06cc6-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="06cc6-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="06cc6-113">Ottiene un elenco di gruppi consumer nell'hub dell'evento \` MyEventHubName \` , disponibile nello spazio dei nomi MyNamespace \` con il \` gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="06cc6-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="06cc6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06cc6-114">PARAMETERS</span></span>

### <span data-ttu-id="06cc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06cc6-115">-DefaultProfile</span></span>
<span data-ttu-id="06cc6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06cc6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06cc6-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="06cc6-117">-EventHub</span></span>
<span data-ttu-id="06cc6-118">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="06cc6-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06cc6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="06cc6-119">-Name</span></span>
<span data-ttu-id="06cc6-120">Nome ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="06cc6-120">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06cc6-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06cc6-121">-Namespace</span></span>
<span data-ttu-id="06cc6-122">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06cc6-122">Namespace Name</span></span>

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

### <span data-ttu-id="06cc6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06cc6-123">-ResourceGroupName</span></span>
<span data-ttu-id="06cc6-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="06cc6-124">Resource Group Name</span></span>

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

### <span data-ttu-id="06cc6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06cc6-125">CommonParameters</span></span>
<span data-ttu-id="06cc6-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06cc6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="06cc6-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06cc6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06cc6-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06cc6-128">INPUTS</span></span>

### <span data-ttu-id="06cc6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="06cc6-129">System.String</span></span>


## <span data-ttu-id="06cc6-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06cc6-130">OUTPUTS</span></span>

### <span data-ttu-id="06cc6-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="06cc6-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="06cc6-132">Note</span><span class="sxs-lookup"><span data-stu-id="06cc6-132">NOTES</span></span>

## <span data-ttu-id="06cc6-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06cc6-133">RELATED LINKS</span></span>
