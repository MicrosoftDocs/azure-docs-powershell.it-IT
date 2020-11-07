---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: a9447c745ddf60c4a2adcb2a55c824b65d96efd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687486"
---
# <span data-ttu-id="47a6d-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="47a6d-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="47a6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="47a6d-103">Crea un nuovo gruppo consumer per l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="47a6d-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47a6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47a6d-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47a6d-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47a6d-105">EXAMPLES</span></span>

### <span data-ttu-id="47a6d-106">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="47a6d-106">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="47a6d-107">Crea il gruppo Consumer \` MyConsumerGroupName \` nell'hub eventi \` MyEventHubName \` , con ambito nello spazio dei nomi MyNamespace \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="47a6d-107">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="47a6d-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47a6d-108">PARAMETERS</span></span>

### <span data-ttu-id="47a6d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a6d-109">-DefaultProfile</span></span>
<span data-ttu-id="47a6d-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47a6d-110">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47a6d-111">-EventHub</span><span class="sxs-lookup"><span data-stu-id="47a6d-111">-EventHub</span></span>
<span data-ttu-id="47a6d-112">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="47a6d-112">EventHub Name</span></span>

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

### <span data-ttu-id="47a6d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="47a6d-113">-Name</span></span>
<span data-ttu-id="47a6d-114">Nome ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="47a6d-114">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47a6d-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="47a6d-115">-Namespace</span></span>
<span data-ttu-id="47a6d-116">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="47a6d-116">Namespace Name</span></span>

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

### <span data-ttu-id="47a6d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47a6d-117">-ResourceGroupName</span></span>
<span data-ttu-id="47a6d-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="47a6d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="47a6d-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="47a6d-119">-UserMetadata</span></span>
<span data-ttu-id="47a6d-120">Metadati utente per ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="47a6d-120">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="47a6d-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47a6d-121">-Confirm</span></span>
<span data-ttu-id="47a6d-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47a6d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a6d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a6d-123">-WhatIf</span></span>
<span data-ttu-id="47a6d-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47a6d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47a6d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47a6d-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a6d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a6d-126">CommonParameters</span></span>
<span data-ttu-id="47a6d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a6d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="47a6d-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47a6d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a6d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47a6d-129">INPUTS</span></span>

### <span data-ttu-id="47a6d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="47a6d-130">System.String</span></span>


## <span data-ttu-id="47a6d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47a6d-131">OUTPUTS</span></span>

### <span data-ttu-id="47a6d-132">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="47a6d-132">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="47a6d-133">Note</span><span class="sxs-lookup"><span data-stu-id="47a6d-133">NOTES</span></span>

## <span data-ttu-id="47a6d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47a6d-134">RELATED LINKS</span></span>
