---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 938949ae1eada6d85bb6e01728f5be09655c3e06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674259"
---
# <span data-ttu-id="af5ba-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="af5ba-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="af5ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af5ba-102">SYNOPSIS</span></span>
<span data-ttu-id="af5ba-103">Crea un gruppo di consumi eventhub.</span><span class="sxs-lookup"><span data-stu-id="af5ba-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="af5ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af5ba-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af5ba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af5ba-105">DESCRIPTION</span></span>
<span data-ttu-id="af5ba-106">Crea un gruppo consumer in Eventhub associato al IotHub specificato.</span><span class="sxs-lookup"><span data-stu-id="af5ba-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="af5ba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af5ba-107">EXAMPLES</span></span>

### <span data-ttu-id="af5ba-108">Esempio 1: aggiungere un gruppo Consumer alla eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="af5ba-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="af5ba-109">Aggiunge una nuova consumergroup denominata "myconsumergroup" al eventhub per gli eventi di telemetria nella iothub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="af5ba-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="af5ba-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af5ba-110">PARAMETERS</span></span>

### <span data-ttu-id="af5ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af5ba-111">-DefaultProfile</span></span>
<span data-ttu-id="af5ba-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="af5ba-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af5ba-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="af5ba-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="af5ba-114">Nome del EventHub ConsumerGroup che si vuole aggiungere.</span><span class="sxs-lookup"><span data-stu-id="af5ba-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="af5ba-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="af5ba-115">-EventHubEndpointName</span></span>
<span data-ttu-id="af5ba-116">Nome dell'endpoint EventHub.</span><span class="sxs-lookup"><span data-stu-id="af5ba-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="af5ba-117">Eventi di valori possibili, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="af5ba-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="af5ba-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="af5ba-118">-Name</span></span>
<span data-ttu-id="af5ba-119">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="af5ba-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="af5ba-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af5ba-120">-ResourceGroupName</span></span>
<span data-ttu-id="af5ba-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af5ba-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="af5ba-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af5ba-122">-Confirm</span></span>
<span data-ttu-id="af5ba-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af5ba-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af5ba-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af5ba-124">-WhatIf</span></span>
<span data-ttu-id="af5ba-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af5ba-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af5ba-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af5ba-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af5ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af5ba-127">CommonParameters</span></span>
<span data-ttu-id="af5ba-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af5ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af5ba-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af5ba-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af5ba-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af5ba-130">INPUTS</span></span>

### <span data-ttu-id="af5ba-131">System. String</span><span class="sxs-lookup"><span data-stu-id="af5ba-131">System.String</span></span>

## <span data-ttu-id="af5ba-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af5ba-132">OUTPUTS</span></span>

### <span data-ttu-id="af5ba-133">System. String</span><span class="sxs-lookup"><span data-stu-id="af5ba-133">System.String</span></span>

## <span data-ttu-id="af5ba-134">Note</span><span class="sxs-lookup"><span data-stu-id="af5ba-134">NOTES</span></span>

## <span data-ttu-id="af5ba-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af5ba-135">RELATED LINKS</span></span>
