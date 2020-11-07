---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 19a3098eff598c223014b65381e524d063f7d425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686828"
---
# <span data-ttu-id="39ac1-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="39ac1-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="39ac1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="39ac1-103">Crea un gruppo di consumi eventhub.</span><span class="sxs-lookup"><span data-stu-id="39ac1-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39ac1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39ac1-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39ac1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39ac1-105">DESCRIPTION</span></span>
<span data-ttu-id="39ac1-106">Crea un gruppo consumer in Eventhub associato al IotHub specificato.</span><span class="sxs-lookup"><span data-stu-id="39ac1-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="39ac1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39ac1-107">EXAMPLES</span></span>

### <span data-ttu-id="39ac1-108">Esempio 1: aggiungere un gruppo Consumer alla eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="39ac1-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="39ac1-109">Aggiunge una nuova consumergroup denominata "myconsumergroup" al eventhub per gli eventi di telemetria nella iothub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="39ac1-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="39ac1-110">Esempio 2: aggiungere un gruppo consumer al monitoraggio delle operazioni eventhub</span><span class="sxs-lookup"><span data-stu-id="39ac1-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="39ac1-111">Aggiunge una nuova consumergroup denominata "myconsumergroup" agli eventi di monitoraggio delle operazioni di eventhub in iothub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="39ac1-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="39ac1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39ac1-112">PARAMETERS</span></span>

### <span data-ttu-id="39ac1-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="39ac1-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="39ac1-114">Nome del EventHub ConsumerGroup che si vuole aggiungere.</span><span class="sxs-lookup"><span data-stu-id="39ac1-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39ac1-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="39ac1-115">-EventHubEndpointName</span></span>
<span data-ttu-id="39ac1-116">Nome dell'endpoint EventHub.</span><span class="sxs-lookup"><span data-stu-id="39ac1-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="39ac1-117">Eventi di valori possibili, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="39ac1-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="39ac1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="39ac1-118">-Name</span></span>
<span data-ttu-id="39ac1-119">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="39ac1-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="39ac1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ac1-120">-ResourceGroupName</span></span>
<span data-ttu-id="39ac1-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39ac1-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="39ac1-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39ac1-122">-Confirm</span></span>
<span data-ttu-id="39ac1-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39ac1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39ac1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ac1-124">-WhatIf</span></span>
<span data-ttu-id="39ac1-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39ac1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39ac1-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39ac1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39ac1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ac1-127">-DefaultProfile</span></span>
<span data-ttu-id="39ac1-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39ac1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39ac1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ac1-129">CommonParameters</span></span>
<span data-ttu-id="39ac1-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39ac1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ac1-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ac1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ac1-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39ac1-132">INPUTS</span></span>

### <span data-ttu-id="39ac1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="39ac1-133">System.String</span></span>

## <span data-ttu-id="39ac1-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39ac1-134">OUTPUTS</span></span>

### <span data-ttu-id="39ac1-135">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="39ac1-135">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="39ac1-136">Note</span><span class="sxs-lookup"><span data-stu-id="39ac1-136">NOTES</span></span>

## <span data-ttu-id="39ac1-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39ac1-137">RELATED LINKS</span></span>

