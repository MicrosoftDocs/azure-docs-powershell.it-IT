---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 749bd1329537d165cb7c31850fd15ca23f38db2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189923"
---
# <span data-ttu-id="4d49f-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="4d49f-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="4d49f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d49f-102">SYNOPSIS</span></span>
<span data-ttu-id="4d49f-103">Crea un gruppo di consumi eventhub.</span><span class="sxs-lookup"><span data-stu-id="4d49f-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="4d49f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d49f-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d49f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d49f-105">DESCRIPTION</span></span>
<span data-ttu-id="4d49f-106">Crea un gruppo consumer in Eventhub associato al IotHub specificato.</span><span class="sxs-lookup"><span data-stu-id="4d49f-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="4d49f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d49f-107">EXAMPLES</span></span>

### <span data-ttu-id="4d49f-108">Esempio 1: aggiungere un gruppo Consumer alla eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="4d49f-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="4d49f-109">Aggiunge una nuova consumergroup denominata "myconsumergroup" al eventhub per gli eventi di telemetria nella iothub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="4d49f-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="4d49f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d49f-110">PARAMETERS</span></span>

### <span data-ttu-id="4d49f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d49f-111">-DefaultProfile</span></span>
<span data-ttu-id="4d49f-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4d49f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d49f-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="4d49f-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="4d49f-114">Nome del EventHub ConsumerGroup che si vuole aggiungere.</span><span class="sxs-lookup"><span data-stu-id="4d49f-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="4d49f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d49f-115">-Name</span></span>
<span data-ttu-id="4d49f-116">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="4d49f-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4d49f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d49f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d49f-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4d49f-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="4d49f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d49f-119">-Confirm</span></span>
<span data-ttu-id="4d49f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d49f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d49f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d49f-121">-WhatIf</span></span>
<span data-ttu-id="4d49f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d49f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d49f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d49f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d49f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d49f-124">CommonParameters</span></span>
<span data-ttu-id="4d49f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d49f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d49f-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d49f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d49f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d49f-127">INPUTS</span></span>

### <span data-ttu-id="4d49f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4d49f-128">System.String</span></span>

## <span data-ttu-id="4d49f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d49f-129">OUTPUTS</span></span>

### <span data-ttu-id="4d49f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4d49f-130">System.String</span></span>

## <span data-ttu-id="4d49f-131">Note</span><span class="sxs-lookup"><span data-stu-id="4d49f-131">NOTES</span></span>

## <span data-ttu-id="4d49f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d49f-132">RELATED LINKS</span></span>
