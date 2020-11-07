---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: c4378b156d17759c180ee3bf966bc20d06d00b41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835928"
---
# <span data-ttu-id="e0512-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e0512-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="e0512-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0512-102">SYNOPSIS</span></span>
<span data-ttu-id="e0512-103">Crea un gruppo di consumi eventhub.</span><span class="sxs-lookup"><span data-stu-id="e0512-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="e0512-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0512-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0512-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0512-105">DESCRIPTION</span></span>
<span data-ttu-id="e0512-106">Crea un gruppo consumer in Eventhub associato al IotHub specificato.</span><span class="sxs-lookup"><span data-stu-id="e0512-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="e0512-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0512-107">EXAMPLES</span></span>

### <span data-ttu-id="e0512-108">Esempio 1: aggiungere un gruppo Consumer alla eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="e0512-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="e0512-109">Aggiunge una nuova consumergroup denominata "myconsumergroup" al eventhub per gli eventi di telemetria nella iothub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e0512-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="e0512-110">Esempio 2: aggiungere un gruppo consumer al monitoraggio delle operazioni eventhub</span><span class="sxs-lookup"><span data-stu-id="e0512-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="e0512-111">Aggiunge una nuova consumergroup denominata "myconsumergroup" agli eventi di monitoraggio delle operazioni di eventhub in iothub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e0512-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="e0512-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0512-112">PARAMETERS</span></span>

### <span data-ttu-id="e0512-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0512-113">-DefaultProfile</span></span>
<span data-ttu-id="e0512-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e0512-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0512-115">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="e0512-115">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="e0512-116">Nome del EventHub ConsumerGroup che si vuole aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e0512-116">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="e0512-117">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="e0512-117">-EventHubEndpointName</span></span>
<span data-ttu-id="e0512-118">Nome dell'endpoint EventHub.</span><span class="sxs-lookup"><span data-stu-id="e0512-118">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="e0512-119">Eventi di valori possibili, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="e0512-119">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0512-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0512-120">-Name</span></span>
<span data-ttu-id="e0512-121">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="e0512-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e0512-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0512-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0512-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e0512-123">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="e0512-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0512-124">-Confirm</span></span>
<span data-ttu-id="e0512-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0512-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0512-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0512-126">-WhatIf</span></span>
<span data-ttu-id="e0512-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0512-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0512-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0512-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0512-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0512-129">CommonParameters</span></span>
<span data-ttu-id="e0512-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0512-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0512-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0512-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0512-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0512-132">INPUTS</span></span>

### <span data-ttu-id="e0512-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e0512-133">System.String</span></span>

## <span data-ttu-id="e0512-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0512-134">OUTPUTS</span></span>

### <span data-ttu-id="e0512-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e0512-135">System.String</span></span>

## <span data-ttu-id="e0512-136">Note</span><span class="sxs-lookup"><span data-stu-id="e0512-136">NOTES</span></span>

## <span data-ttu-id="e0512-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0512-137">RELATED LINKS</span></span>
