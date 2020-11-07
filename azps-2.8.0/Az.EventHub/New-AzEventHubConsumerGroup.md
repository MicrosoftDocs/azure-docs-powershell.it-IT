---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: c887aab15e0874357ec32d9c815a9a9b1dd1227a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674435"
---
# <span data-ttu-id="5c293-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5c293-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="5c293-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c293-102">SYNOPSIS</span></span>
<span data-ttu-id="5c293-103">Crea un nuovo gruppo consumer per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="5c293-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="5c293-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c293-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c293-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c293-105">DESCRIPTION</span></span>
<span data-ttu-id="5c293-106">Crea un nuovo gruppo consumer per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="5c293-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="5c293-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c293-107">EXAMPLES</span></span>

### <span data-ttu-id="5c293-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5c293-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="5c293-109">Crea il gruppo Consumer \` MyConsumerGroupName \` nell'hub eventi \` MyEventHubName \` , con ambito nello spazio dei nomi MyNamespace \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5c293-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="5c293-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c293-110">PARAMETERS</span></span>

### <span data-ttu-id="5c293-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c293-111">-DefaultProfile</span></span>
<span data-ttu-id="5c293-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c293-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c293-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5c293-113">-EventHub</span></span>
<span data-ttu-id="5c293-114">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="5c293-114">EventHub Name</span></span>

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

### <span data-ttu-id="5c293-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c293-115">-Name</span></span>
<span data-ttu-id="5c293-116">Nome ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5c293-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="5c293-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c293-117">-Namespace</span></span>
<span data-ttu-id="5c293-118">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c293-118">Namespace Name</span></span>

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

### <span data-ttu-id="5c293-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c293-119">-ResourceGroupName</span></span>
<span data-ttu-id="5c293-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5c293-120">Resource Group Name</span></span>

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

### <span data-ttu-id="5c293-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="5c293-121">-UserMetadata</span></span>
<span data-ttu-id="5c293-122">Metadati utente per ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5c293-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="5c293-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5c293-123">-Confirm</span></span>
<span data-ttu-id="5c293-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c293-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c293-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c293-125">-WhatIf</span></span>
<span data-ttu-id="5c293-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c293-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c293-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c293-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c293-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c293-128">CommonParameters</span></span>
<span data-ttu-id="5c293-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c293-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c293-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c293-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c293-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c293-131">INPUTS</span></span>

### <span data-ttu-id="5c293-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5c293-132">System.String</span></span>

## <span data-ttu-id="5c293-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c293-133">OUTPUTS</span></span>

### <span data-ttu-id="5c293-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="5c293-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="5c293-135">Note</span><span class="sxs-lookup"><span data-stu-id="5c293-135">NOTES</span></span>

## <span data-ttu-id="5c293-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c293-136">RELATED LINKS</span></span>
