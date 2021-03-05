---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: 844b8a08a54409e4eb10cde9f063b65cb5587bae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009149"
---
# <span data-ttu-id="f57d8-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f57d8-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="f57d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f57d8-102">SYNOPSIS</span></span>
<span data-ttu-id="f57d8-103">Aggiorna il gruppo consumer hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="f57d8-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="f57d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f57d8-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f57d8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f57d8-105">DESCRIPTION</span></span>
<span data-ttu-id="f57d8-106">Il Set-AzEventHubConsumerGroup cmdlet aggiorna il gruppo consumer Hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="f57d8-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="f57d8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f57d8-107">EXAMPLES</span></span>

### <span data-ttu-id="f57d8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f57d8-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="f57d8-109">Imposta i metadati utente del gruppo consumer \` MyConsumerGroupName \` su "Test".</span><span class="sxs-lookup"><span data-stu-id="f57d8-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="f57d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f57d8-110">PARAMETERS</span></span>

### <span data-ttu-id="f57d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f57d8-111">-DefaultProfile</span></span>
<span data-ttu-id="f57d8-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f57d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f57d8-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f57d8-113">-EventHub</span></span>
<span data-ttu-id="f57d8-114">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="f57d8-114">EventHub Name</span></span>

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

### <span data-ttu-id="f57d8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f57d8-115">-Name</span></span>
<span data-ttu-id="f57d8-116">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="f57d8-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f57d8-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f57d8-117">-Namespace</span></span>
<span data-ttu-id="f57d8-118">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f57d8-118">Namespace Name</span></span>

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

### <span data-ttu-id="f57d8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f57d8-119">-ResourceGroupName</span></span>
<span data-ttu-id="f57d8-120">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f57d8-120">Resource Group Name</span></span>

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

### <span data-ttu-id="f57d8-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="f57d8-121">-UserMetadata</span></span>
<span data-ttu-id="f57d8-122">Metadati utente per ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="f57d8-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f57d8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f57d8-123">-Confirm</span></span>
<span data-ttu-id="f57d8-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57d8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57d8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f57d8-125">-WhatIf</span></span>
<span data-ttu-id="f57d8-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f57d8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f57d8-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f57d8-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f57d8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f57d8-128">CommonParameters</span></span>
<span data-ttu-id="f57d8-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f57d8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f57d8-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f57d8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f57d8-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="f57d8-131">INPUTS</span></span>

### <span data-ttu-id="f57d8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f57d8-132">System.String</span></span>

## <span data-ttu-id="f57d8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f57d8-133">OUTPUTS</span></span>

### <span data-ttu-id="f57d8-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="f57d8-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="f57d8-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="f57d8-135">NOTES</span></span>

## <span data-ttu-id="f57d8-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f57d8-136">RELATED LINKS</span></span>
