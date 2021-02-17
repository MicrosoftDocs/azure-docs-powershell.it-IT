---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180679"
---
# <span data-ttu-id="e6cea-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e6cea-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="e6cea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6cea-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cea-103">Crea un nuovo gruppo consumer per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="e6cea-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="e6cea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6cea-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6cea-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6cea-105">DESCRIPTION</span></span>
<span data-ttu-id="e6cea-106">Crea un nuovo gruppo consumer per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="e6cea-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="e6cea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6cea-107">EXAMPLES</span></span>

### <span data-ttu-id="e6cea-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6cea-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="e6cea-109">Crea il gruppo consumer \` MyConsumerGroupName nell'hub eventi MyEventHubName, con ambito allo spazio dei nomi MyResourceName, con gruppo di \` \` risorse \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="e6cea-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e6cea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6cea-110">PARAMETERS</span></span>

### <span data-ttu-id="e6cea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cea-111">-DefaultProfile</span></span>
<span data-ttu-id="e6cea-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6cea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6cea-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e6cea-113">-EventHub</span></span>
<span data-ttu-id="e6cea-114">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="e6cea-114">EventHub Name</span></span>

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

### <span data-ttu-id="e6cea-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e6cea-115">-Name</span></span>
<span data-ttu-id="e6cea-116">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="e6cea-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="e6cea-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e6cea-117">-Namespace</span></span>
<span data-ttu-id="e6cea-118">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e6cea-118">Namespace Name</span></span>

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

### <span data-ttu-id="e6cea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6cea-119">-ResourceGroupName</span></span>
<span data-ttu-id="e6cea-120">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e6cea-120">Resource Group Name</span></span>

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

### <span data-ttu-id="e6cea-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="e6cea-121">-UserMetadata</span></span>
<span data-ttu-id="e6cea-122">Metadati utente per ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e6cea-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="e6cea-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6cea-123">-Confirm</span></span>
<span data-ttu-id="e6cea-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6cea-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6cea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6cea-125">-WhatIf</span></span>
<span data-ttu-id="e6cea-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6cea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6cea-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6cea-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6cea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cea-128">CommonParameters</span></span>
<span data-ttu-id="e6cea-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6cea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cea-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6cea-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cea-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6cea-131">INPUTS</span></span>

### <span data-ttu-id="e6cea-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e6cea-132">System.String</span></span>

## <span data-ttu-id="e6cea-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6cea-133">OUTPUTS</span></span>

### <span data-ttu-id="e6cea-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="e6cea-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="e6cea-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6cea-135">NOTES</span></span>

## <span data-ttu-id="e6cea-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6cea-136">RELATED LINKS</span></span>
