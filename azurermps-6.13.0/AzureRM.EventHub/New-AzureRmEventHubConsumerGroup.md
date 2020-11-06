---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 34a59f0530ed036397523e3810d68175e7ee2d3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509224"
---
# <span data-ttu-id="7fb83-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7fb83-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="7fb83-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7fb83-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb83-103">Crea un nuovo gruppo consumer per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="7fb83-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fb83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fb83-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fb83-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fb83-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb83-106">Crea un nuovo gruppo consumer per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="7fb83-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="7fb83-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fb83-107">EXAMPLES</span></span>

### <span data-ttu-id="7fb83-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7fb83-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="7fb83-109">Crea il gruppo Consumer \` MyConsumerGroupName \` nell'hub eventi \` MyEventHubName \` , con ambito nello spazio dei nomi MyNamespace \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7fb83-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7fb83-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7fb83-110">PARAMETERS</span></span>

### <span data-ttu-id="7fb83-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb83-111">-DefaultProfile</span></span>
<span data-ttu-id="7fb83-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb83-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb83-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7fb83-113">-EventHub</span></span>
<span data-ttu-id="7fb83-114">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="7fb83-114">EventHub Name</span></span>

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

### <span data-ttu-id="7fb83-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7fb83-115">-Name</span></span>
<span data-ttu-id="7fb83-116">Nome ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7fb83-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="7fb83-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7fb83-117">-Namespace</span></span>
<span data-ttu-id="7fb83-118">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7fb83-118">Namespace Name</span></span>

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

### <span data-ttu-id="7fb83-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb83-119">-ResourceGroupName</span></span>
<span data-ttu-id="7fb83-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7fb83-120">Resource Group Name</span></span>

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

### <span data-ttu-id="7fb83-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="7fb83-121">-UserMetadata</span></span>
<span data-ttu-id="7fb83-122">Metadati utente per ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7fb83-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="7fb83-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7fb83-123">-Confirm</span></span>
<span data-ttu-id="7fb83-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fb83-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb83-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb83-125">-WhatIf</span></span>
<span data-ttu-id="7fb83-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fb83-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb83-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fb83-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb83-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb83-128">CommonParameters</span></span>
<span data-ttu-id="7fb83-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb83-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb83-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb83-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb83-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7fb83-131">INPUTS</span></span>

### <span data-ttu-id="7fb83-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7fb83-132">System.String</span></span>

## <span data-ttu-id="7fb83-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fb83-133">OUTPUTS</span></span>

### <span data-ttu-id="7fb83-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="7fb83-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="7fb83-135">Note</span><span class="sxs-lookup"><span data-stu-id="7fb83-135">NOTES</span></span>

## <span data-ttu-id="7fb83-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fb83-136">RELATED LINKS</span></span>
