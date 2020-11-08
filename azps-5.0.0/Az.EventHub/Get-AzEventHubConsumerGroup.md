---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: fc108c633b70cc1eed32bcc0574ad25109a065fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202155"
---
# <span data-ttu-id="68035-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="68035-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="68035-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68035-102">SYNOPSIS</span></span>
<span data-ttu-id="68035-103">Ottiene i dettagli di un gruppo di utenti hub di eventi specificato oppure ottiene un elenco di gruppi consumer in un hub eventi.</span><span class="sxs-lookup"><span data-stu-id="68035-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="68035-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68035-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68035-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68035-105">DESCRIPTION</span></span>
<span data-ttu-id="68035-106">Il cmdlet Get-AzEventHubConsumerGroup ottiene i dettagli di un gruppo di utenti hub eventi specificato o un elenco di gruppi consumer in un hub di eventi specifico.</span><span class="sxs-lookup"><span data-stu-id="68035-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="68035-107">Se viene fornito il nome di un gruppo di utenti, vengono restituiti i dettagli di un singolo dettaglio del gruppo consumer.</span><span class="sxs-lookup"><span data-stu-id="68035-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="68035-108">Se il nome di un gruppo di utenti non è disponibile, viene restituito un elenco di gruppi consumer nell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="68035-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="68035-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68035-109">EXAMPLES</span></span>

### <span data-ttu-id="68035-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="68035-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="68035-111">Ottiene il gruppo Consumer \` MyConsumerGroupName \` nell'hub dell'evento \` MyEventHubName \` , disponibile nello spazio dei nomi MyNamespace \` con il \` gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="68035-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="68035-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="68035-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="68035-113">Ottiene un elenco di gruppi consumer nell'hub dell'evento \` MyEventHubName \` , disponibile nello spazio dei nomi MyNamespace \` con il \` gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="68035-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="68035-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68035-114">PARAMETERS</span></span>

### <span data-ttu-id="68035-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68035-115">-DefaultProfile</span></span>
<span data-ttu-id="68035-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68035-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68035-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="68035-117">-EventHub</span></span>
<span data-ttu-id="68035-118">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="68035-118">EventHub Name</span></span>

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

### <span data-ttu-id="68035-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="68035-119">-MaxCount</span></span>
<span data-ttu-id="68035-120">Determinare il numero massimo di ConsumerGroups da restituire.</span><span class="sxs-lookup"><span data-stu-id="68035-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="68035-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="68035-121">-Name</span></span>
<span data-ttu-id="68035-122">Nome ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="68035-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="68035-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="68035-123">-Namespace</span></span>
<span data-ttu-id="68035-124">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="68035-124">Namespace Name</span></span>

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

### <span data-ttu-id="68035-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68035-125">-ResourceGroupName</span></span>
<span data-ttu-id="68035-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="68035-126">Resource Group Name</span></span>

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

### <span data-ttu-id="68035-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68035-127">CommonParameters</span></span>
<span data-ttu-id="68035-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68035-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68035-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68035-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68035-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68035-130">INPUTS</span></span>

### <span data-ttu-id="68035-131">System. String</span><span class="sxs-lookup"><span data-stu-id="68035-131">System.String</span></span>

## <span data-ttu-id="68035-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68035-132">OUTPUTS</span></span>

### <span data-ttu-id="68035-133">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="68035-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="68035-134">Note</span><span class="sxs-lookup"><span data-stu-id="68035-134">NOTES</span></span>

## <span data-ttu-id="68035-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68035-135">RELATED LINKS</span></span>
