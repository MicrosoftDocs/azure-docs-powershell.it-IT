---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188263"
---
# <span data-ttu-id="e0e82-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e0e82-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="e0e82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0e82-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e82-103">Crea un gruppo consumer eventhub.</span><span class="sxs-lookup"><span data-stu-id="e0e82-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="e0e82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0e82-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0e82-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e0e82-105">DESCRIPTION</span></span>
<span data-ttu-id="e0e82-106">Crea un gruppo di utenti consumer in Eventhub associato all'oggetto IotHub specificato.</span><span class="sxs-lookup"><span data-stu-id="e0e82-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="e0e82-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0e82-107">EXAMPLES</span></span>

### <span data-ttu-id="e0e82-108">Esempio 1: Aggiungere un gruppo consumer all'eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="e0e82-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="e0e82-109">Aggiunge un nuovo gruppo consumer denominato "gruppoconsumer" all'eventhub per gli eventi di telemetria nell'iothub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e0e82-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="e0e82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0e82-110">PARAMETERS</span></span>

### <span data-ttu-id="e0e82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e82-111">-DefaultProfile</span></span>
<span data-ttu-id="e0e82-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e0e82-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0e82-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e82-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="e0e82-114">Nome del gruppo ConsumerGroup di EventHub che si vuole aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e0e82-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="e0e82-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e0e82-115">-Name</span></span>
<span data-ttu-id="e0e82-116">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="e0e82-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e0e82-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e82-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0e82-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e0e82-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="e0e82-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0e82-119">-Confirm</span></span>
<span data-ttu-id="e0e82-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e82-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0e82-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e82-121">-WhatIf</span></span>
<span data-ttu-id="e0e82-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0e82-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0e82-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0e82-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0e82-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e82-124">CommonParameters</span></span>
<span data-ttu-id="e0e82-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e82-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e82-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e82-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e82-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="e0e82-127">INPUTS</span></span>

### <span data-ttu-id="e0e82-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e0e82-128">System.String</span></span>

## <span data-ttu-id="e0e82-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0e82-129">OUTPUTS</span></span>

### <span data-ttu-id="e0e82-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e0e82-130">System.String</span></span>

## <span data-ttu-id="e0e82-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="e0e82-131">NOTES</span></span>

## <span data-ttu-id="e0e82-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0e82-132">RELATED LINKS</span></span>
