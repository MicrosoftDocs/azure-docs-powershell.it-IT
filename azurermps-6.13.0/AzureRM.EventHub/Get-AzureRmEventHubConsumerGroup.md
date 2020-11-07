---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 205dc883f8f6e0481f88438137ca45ad7a99c4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686401"
---
# <span data-ttu-id="1c606-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1c606-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="1c606-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c606-102">SYNOPSIS</span></span>
<span data-ttu-id="1c606-103">Ottiene i dettagli di un gruppo di utenti hub di eventi specificato oppure ottiene un elenco di gruppi consumer in un hub eventi.</span><span class="sxs-lookup"><span data-stu-id="1c606-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c606-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c606-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c606-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c606-105">DESCRIPTION</span></span>
<span data-ttu-id="1c606-106">Il cmdlet Get-AzureRmEventHubConsumerGroup ottiene i dettagli di un gruppo di utenti hub eventi specificato o un elenco di gruppi consumer in un hub di eventi specifico.</span><span class="sxs-lookup"><span data-stu-id="1c606-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="1c606-107">Se viene fornito il nome di un gruppo di utenti, vengono restituiti i dettagli di un singolo dettaglio del gruppo consumer.</span><span class="sxs-lookup"><span data-stu-id="1c606-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="1c606-108">Se il nome di un gruppo di utenti non è disponibile, viene restituito un elenco di gruppi consumer nell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="1c606-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="1c606-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c606-109">EXAMPLES</span></span>

### <span data-ttu-id="1c606-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1c606-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="1c606-111">Ottiene il gruppo Consumer \` MyConsumerGroupName \` nell'hub dell'evento \` MyEventHubName \` , disponibile nello spazio dei nomi MyNamespace \` con il \` gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="1c606-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1c606-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1c606-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="1c606-113">Ottiene un elenco di gruppi consumer nell'hub dell'evento \` MyEventHubName \` , disponibile nello spazio dei nomi MyNamespace \` con il \` gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="1c606-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="1c606-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c606-114">PARAMETERS</span></span>

### <span data-ttu-id="1c606-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c606-115">-DefaultProfile</span></span>
<span data-ttu-id="1c606-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c606-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c606-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="1c606-117">-EventHub</span></span>
<span data-ttu-id="1c606-118">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="1c606-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c606-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1c606-119">-MaxCount</span></span>
<span data-ttu-id="1c606-120">Determinare il numero massimo di ConsumerGroups da restituire.</span><span class="sxs-lookup"><span data-stu-id="1c606-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="1c606-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c606-121">-Name</span></span>
<span data-ttu-id="1c606-122">Nome ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1c606-122">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c606-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1c606-123">-Namespace</span></span>
<span data-ttu-id="1c606-124">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1c606-124">Namespace Name</span></span>

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

### <span data-ttu-id="1c606-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c606-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c606-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1c606-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c606-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c606-127">CommonParameters</span></span>
<span data-ttu-id="1c606-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c606-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c606-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c606-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c606-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c606-130">INPUTS</span></span>

### <span data-ttu-id="1c606-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1c606-131">System.String</span></span>

## <span data-ttu-id="1c606-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c606-132">OUTPUTS</span></span>

### <span data-ttu-id="1c606-133">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="1c606-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="1c606-134">Note</span><span class="sxs-lookup"><span data-stu-id="1c606-134">NOTES</span></span>

## <span data-ttu-id="1c606-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c606-135">RELATED LINKS</span></span>
