---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: fc108c633b70cc1eed32bcc0574ad25109a065fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185943"
---
# <span data-ttu-id="985ff-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="985ff-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="985ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="985ff-102">SYNOPSIS</span></span>
<span data-ttu-id="985ff-103">Recupera i dettagli di un gruppo consumer di hub eventi specificato o ottiene un elenco di gruppi consumer in un hub eventi.</span><span class="sxs-lookup"><span data-stu-id="985ff-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="985ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="985ff-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="985ff-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="985ff-105">DESCRIPTION</span></span>
<span data-ttu-id="985ff-106">Il Get-AzEventHubConsumerGroup cmdlet ottiene i dettagli di un determinato gruppo di utenti consumer Hub eventi oppure un elenco di gruppi consumer in un determinato Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="985ff-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="985ff-107">Se viene fornito il nome di un gruppo consumer, vengono restituiti i dettagli di un singolo gruppo consumer.</span><span class="sxs-lookup"><span data-stu-id="985ff-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="985ff-108">Se non viene fornito il nome di un gruppo consumer, viene restituito un elenco di gruppi consumer nell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="985ff-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="985ff-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="985ff-109">EXAMPLES</span></span>

### <span data-ttu-id="985ff-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="985ff-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="985ff-111">Ottiene il gruppo consumer \` MyConsumerGroupName nell'hub eventi MyEventHubName, che si trova nello spazio dei nomi MyResourceName con il gruppo \` \` di risorse \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="985ff-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="985ff-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="985ff-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="985ff-113">Ottiene un elenco di gruppi consumer nell'hub eventi MyEventHubName, che si trova nello spazio dei nomi \` \` \` MyResourceName \` con il gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="985ff-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="985ff-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="985ff-114">PARAMETERS</span></span>

### <span data-ttu-id="985ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="985ff-115">-DefaultProfile</span></span>
<span data-ttu-id="985ff-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="985ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="985ff-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="985ff-117">-EventHub</span></span>
<span data-ttu-id="985ff-118">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="985ff-118">EventHub Name</span></span>

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

### <span data-ttu-id="985ff-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="985ff-119">-MaxCount</span></span>
<span data-ttu-id="985ff-120">Determinare il numero massimo di Gruppi Consumer da restituire.</span><span class="sxs-lookup"><span data-stu-id="985ff-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="985ff-121">-Name</span><span class="sxs-lookup"><span data-stu-id="985ff-121">-Name</span></span>
<span data-ttu-id="985ff-122">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="985ff-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="985ff-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="985ff-123">-Namespace</span></span>
<span data-ttu-id="985ff-124">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="985ff-124">Namespace Name</span></span>

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

### <span data-ttu-id="985ff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="985ff-125">-ResourceGroupName</span></span>
<span data-ttu-id="985ff-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="985ff-126">Resource Group Name</span></span>

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

### <span data-ttu-id="985ff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985ff-127">CommonParameters</span></span>
<span data-ttu-id="985ff-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="985ff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985ff-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="985ff-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985ff-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="985ff-130">INPUTS</span></span>

### <span data-ttu-id="985ff-131">System.String</span><span class="sxs-lookup"><span data-stu-id="985ff-131">System.String</span></span>

## <span data-ttu-id="985ff-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="985ff-132">OUTPUTS</span></span>

### <span data-ttu-id="985ff-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="985ff-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="985ff-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="985ff-134">NOTES</span></span>

## <span data-ttu-id="985ff-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="985ff-135">RELATED LINKS</span></span>
