---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 52038de3d0bb8f07fdfe5abf0978e306a1959a94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515347"
---
# <span data-ttu-id="a0a7b-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a0a7b-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="a0a7b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a7b-103">Aggiorna il gruppo di utenti hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="a0a7b-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0a7b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0a7b-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0a7b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0a7b-105">DESCRIPTION</span></span>
<span data-ttu-id="a0a7b-106">Il cmdlet Set-AzureRmEventHubConsumerGroup aggiorna il gruppo di utenti hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="a0a7b-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="a0a7b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0a7b-107">EXAMPLES</span></span>

### <span data-ttu-id="a0a7b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0a7b-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="a0a7b-109">Imposta i metadati utente del gruppo Consumer \` MyConsumerGroupName \` su "testing".</span><span class="sxs-lookup"><span data-stu-id="a0a7b-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="a0a7b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0a7b-110">PARAMETERS</span></span>

### <span data-ttu-id="a0a7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a7b-111">-DefaultProfile</span></span>
<span data-ttu-id="a0a7b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a7b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0a7b-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a0a7b-113">-EventHub</span></span>
<span data-ttu-id="a0a7b-114">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="a0a7b-114">EventHub Name</span></span>

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

### <span data-ttu-id="a0a7b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0a7b-115">-Name</span></span>
<span data-ttu-id="a0a7b-116">Nome ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a0a7b-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="a0a7b-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a0a7b-117">-Namespace</span></span>
<span data-ttu-id="a0a7b-118">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a0a7b-118">Namespace Name</span></span>

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

### <span data-ttu-id="a0a7b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a7b-119">-ResourceGroupName</span></span>
<span data-ttu-id="a0a7b-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a0a7b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="a0a7b-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="a0a7b-121">-UserMetadata</span></span>
<span data-ttu-id="a0a7b-122">Metadati utente per ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a0a7b-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="a0a7b-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0a7b-123">-Confirm</span></span>
<span data-ttu-id="a0a7b-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0a7b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0a7b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a7b-125">-WhatIf</span></span>
<span data-ttu-id="a0a7b-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0a7b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0a7b-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0a7b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0a7b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a7b-128">CommonParameters</span></span>
<span data-ttu-id="a0a7b-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a7b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a7b-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0a7b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a7b-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0a7b-131">INPUTS</span></span>

### <span data-ttu-id="a0a7b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a0a7b-132">System.String</span></span>

## <span data-ttu-id="a0a7b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0a7b-133">OUTPUTS</span></span>

### <span data-ttu-id="a0a7b-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="a0a7b-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="a0a7b-135">Note</span><span class="sxs-lookup"><span data-stu-id="a0a7b-135">NOTES</span></span>

## <span data-ttu-id="a0a7b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0a7b-136">RELATED LINKS</span></span>
