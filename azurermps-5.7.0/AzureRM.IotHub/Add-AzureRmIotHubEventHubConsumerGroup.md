---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 192a20ee3d49bd79dff833a05ffd3ff98bcc30ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521044"
---
# <span data-ttu-id="201dd-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="201dd-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="201dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="201dd-102">SYNOPSIS</span></span>
<span data-ttu-id="201dd-103">Crea un gruppo di consumi eventhub.</span><span class="sxs-lookup"><span data-stu-id="201dd-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="201dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="201dd-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="201dd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="201dd-105">DESCRIPTION</span></span>
<span data-ttu-id="201dd-106">Crea un gruppo consumer in Eventhub associato al IotHub specificato.</span><span class="sxs-lookup"><span data-stu-id="201dd-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="201dd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="201dd-107">EXAMPLES</span></span>

### <span data-ttu-id="201dd-108">Esempio 1: aggiungere un gruppo Consumer alla eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="201dd-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="201dd-109">Aggiunge una nuova consumergroup denominata "myconsumergroup" al eventhub per gli eventi di telemetria nella iothub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="201dd-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="201dd-110">Esempio 2: aggiungere un gruppo consumer al monitoraggio delle operazioni eventhub</span><span class="sxs-lookup"><span data-stu-id="201dd-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="201dd-111">Aggiunge una nuova consumergroup denominata "myconsumergroup" agli eventi di monitoraggio delle operazioni di eventhub in iothub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="201dd-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="201dd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="201dd-112">PARAMETERS</span></span>

### <span data-ttu-id="201dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201dd-113">-DefaultProfile</span></span>
<span data-ttu-id="201dd-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="201dd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="201dd-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="201dd-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="201dd-116">Nome del EventHub ConsumerGroup che si vuole aggiungere.</span><span class="sxs-lookup"><span data-stu-id="201dd-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201dd-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="201dd-117">-EventHubEndpointName</span></span>
<span data-ttu-id="201dd-118">Nome dell'endpoint EventHub.</span><span class="sxs-lookup"><span data-stu-id="201dd-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="201dd-119">Eventi di valori possibili, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="201dd-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201dd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="201dd-120">-Name</span></span>
<span data-ttu-id="201dd-121">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="201dd-121">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="201dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="201dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="201dd-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="201dd-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="201dd-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="201dd-124">-Confirm</span></span>
<span data-ttu-id="201dd-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="201dd-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201dd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="201dd-126">-WhatIf</span></span>
<span data-ttu-id="201dd-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="201dd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="201dd-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="201dd-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201dd-129">CommonParameters</span></span>
<span data-ttu-id="201dd-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="201dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201dd-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="201dd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201dd-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="201dd-132">INPUTS</span></span>

### <span data-ttu-id="201dd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="201dd-133">System.String</span></span>

## <span data-ttu-id="201dd-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="201dd-134">OUTPUTS</span></span>

### <span data-ttu-id="201dd-135">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="201dd-135">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="201dd-136">Note</span><span class="sxs-lookup"><span data-stu-id="201dd-136">NOTES</span></span>

## <span data-ttu-id="201dd-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="201dd-137">RELATED LINKS</span></span>

