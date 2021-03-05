---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 23f6c4b7d40f0ec2e02541f82d5d517019bd15fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997875"
---
# <span data-ttu-id="0f17d-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0f17d-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="0f17d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f17d-102">SYNOPSIS</span></span>
<span data-ttu-id="0f17d-103">Crea un gruppo consumer eventhub.</span><span class="sxs-lookup"><span data-stu-id="0f17d-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="0f17d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f17d-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f17d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f17d-105">DESCRIPTION</span></span>
<span data-ttu-id="0f17d-106">Crea un gruppo di utenti consumer in Eventhub associato all'oggetto IotHub specificato.</span><span class="sxs-lookup"><span data-stu-id="0f17d-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="0f17d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f17d-107">EXAMPLES</span></span>

### <span data-ttu-id="0f17d-108">Esempio 1: Aggiungere un gruppo consumer all'eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="0f17d-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="0f17d-109">Aggiunge un nuovo gruppo consumer denominato "myconsumergroup" all'eventhub per gli eventi di telemetria nel iothub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="0f17d-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="0f17d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f17d-110">PARAMETERS</span></span>

### <span data-ttu-id="0f17d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f17d-111">-DefaultProfile</span></span>
<span data-ttu-id="0f17d-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0f17d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f17d-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="0f17d-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="0f17d-114">Nome del gruppo ConsumerGroup di EventHub che si vuole aggiungere.</span><span class="sxs-lookup"><span data-stu-id="0f17d-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f17d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0f17d-115">-Name</span></span>
<span data-ttu-id="0f17d-116">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="0f17d-116">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f17d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f17d-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f17d-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f17d-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="0f17d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f17d-119">-Confirm</span></span>
<span data-ttu-id="0f17d-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f17d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f17d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f17d-121">-WhatIf</span></span>
<span data-ttu-id="0f17d-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f17d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f17d-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f17d-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f17d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f17d-124">CommonParameters</span></span>
<span data-ttu-id="0f17d-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f17d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f17d-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f17d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f17d-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f17d-127">INPUTS</span></span>

### <span data-ttu-id="0f17d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0f17d-128">System.String</span></span>

## <span data-ttu-id="0f17d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f17d-129">OUTPUTS</span></span>

### <span data-ttu-id="0f17d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0f17d-130">System.String</span></span>

## <span data-ttu-id="0f17d-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f17d-131">NOTES</span></span>

## <span data-ttu-id="0f17d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f17d-132">RELATED LINKS</span></span>
