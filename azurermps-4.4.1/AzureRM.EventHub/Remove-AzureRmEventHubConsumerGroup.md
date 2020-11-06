---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c8684e9af0bca55dca52f336a458f4c428ca67a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519186"
---
# <span data-ttu-id="e2d9b-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e2d9b-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="e2d9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d9b-103">Elimina il gruppo di utenti hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2d9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2d9b-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e2d9b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2d9b-105">DESCRIPTION</span></span>
<span data-ttu-id="e2d9b-106">Il cmdlet Remove-AzureRmEventHubConsumerGroup rimuove ed Elimina il gruppo di utenti specificato dall'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="e2d9b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2d9b-107">EXAMPLES</span></span>

### <span data-ttu-id="e2d9b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e2d9b-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="e2d9b-109">Elimina il gruppo Consumer \` MyConsumerGroupName \` dall'hub eventi \` MyEventHubName \` , ambito dello \` \` spazio dei nomi MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="e2d9b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2d9b-110">PARAMETERS</span></span>

### <span data-ttu-id="e2d9b-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d9b-111">-ResourceGroupName</span></span>
<span data-ttu-id="e2d9b-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-112">Resource group name.</span></span>

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

### <span data-ttu-id="e2d9b-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2d9b-113">-Confirm</span></span>
<span data-ttu-id="e2d9b-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d9b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d9b-115">-WhatIf</span></span>
<span data-ttu-id="e2d9b-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2d9b-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d9b-118">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e2d9b-118">-EventHub</span></span>
<span data-ttu-id="e2d9b-119">Nome EventHub.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-119">EventHub Name.</span></span>

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

### <span data-ttu-id="e2d9b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2d9b-120">-Name</span></span>
<span data-ttu-id="e2d9b-121">Nome ConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-121">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d9b-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e2d9b-122">-Namespace</span></span>
<span data-ttu-id="e2d9b-123">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e2d9b-123">Namespace Name.</span></span>

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

## <span data-ttu-id="e2d9b-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2d9b-124">INPUTS</span></span>

### <span data-ttu-id="e2d9b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e2d9b-125">System.String</span></span>

## <span data-ttu-id="e2d9b-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2d9b-126">OUTPUTS</span></span>

### <span data-ttu-id="e2d9b-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="e2d9b-127">System.Object</span></span>

## <span data-ttu-id="e2d9b-128">Note</span><span class="sxs-lookup"><span data-stu-id="e2d9b-128">NOTES</span></span>

## <span data-ttu-id="e2d9b-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2d9b-129">RELATED LINKS</span></span>

