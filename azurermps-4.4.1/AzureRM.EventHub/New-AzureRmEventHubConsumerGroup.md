---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bcd20fc9c6f0c08af2ae735558a6fccc6c9814d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688317"
---
# <span data-ttu-id="4195a-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4195a-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="4195a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4195a-102">SYNOPSIS</span></span>
<span data-ttu-id="4195a-103">Crea un nuovo gruppo consumer per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="4195a-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4195a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4195a-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4195a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4195a-105">DESCRIPTION</span></span>
<span data-ttu-id="4195a-106">Il cmdlet New-AzureRmEventHubConsumerGroup crea un nuovo gruppo consumer per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="4195a-106">The New-AzureRmEventHubConsumerGroup cmdlet creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="4195a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4195a-107">EXAMPLES</span></span>

### <span data-ttu-id="4195a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4195a-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="4195a-109">Crea il gruppo Consumer \` MyConsumerGroupName \` nell'hub eventi \` MyEventHubName \` , con ambito nello spazio dei nomi MyNamespace \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4195a-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4195a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4195a-110">PARAMETERS</span></span>

### <span data-ttu-id="4195a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4195a-111">-ResourceGroupName</span></span>
<span data-ttu-id="4195a-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4195a-112">Resource group name.</span></span>

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

### <span data-ttu-id="4195a-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="4195a-113">-UserMetadata</span></span>
<span data-ttu-id="4195a-114">Metadati utente per il gruppo consumer.</span><span class="sxs-lookup"><span data-stu-id="4195a-114">User metadata for the consumer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4195a-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4195a-115">-Confirm</span></span>
<span data-ttu-id="4195a-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4195a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4195a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4195a-117">-WhatIf</span></span>
<span data-ttu-id="4195a-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4195a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4195a-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4195a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4195a-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4195a-120">-EventHub</span></span>
<span data-ttu-id="4195a-121">Nome EventHub.</span><span class="sxs-lookup"><span data-stu-id="4195a-121">EventHub Name.</span></span>

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

### <span data-ttu-id="4195a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4195a-122">-Name</span></span>
<span data-ttu-id="4195a-123">Nome ConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="4195a-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="4195a-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4195a-124">-Namespace</span></span>
<span data-ttu-id="4195a-125">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4195a-125">Namespace Name.</span></span>

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

## <span data-ttu-id="4195a-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4195a-126">INPUTS</span></span>

### <span data-ttu-id="4195a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4195a-127">System.String</span></span>

## <span data-ttu-id="4195a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4195a-128">OUTPUTS</span></span>

### <span data-ttu-id="4195a-129">Microsoft. Azure. Commands. EventHub. Models. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="4195a-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="4195a-130">Note</span><span class="sxs-lookup"><span data-stu-id="4195a-130">NOTES</span></span>

## <span data-ttu-id="4195a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4195a-131">RELATED LINKS</span></span>

