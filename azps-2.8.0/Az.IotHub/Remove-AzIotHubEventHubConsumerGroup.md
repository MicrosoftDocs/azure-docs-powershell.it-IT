---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: d321892ef2ebbe8e50908a5d519f1990ebb875ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674205"
---
# <span data-ttu-id="2898b-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2898b-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="2898b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2898b-102">SYNOPSIS</span></span>
<span data-ttu-id="2898b-103">Elimina un consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="2898b-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="2898b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2898b-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2898b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2898b-105">DESCRIPTION</span></span>
<span data-ttu-id="2898b-106">Elimina un consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="2898b-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="2898b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2898b-107">EXAMPLES</span></span>

### <span data-ttu-id="2898b-108">Esempio 1 rimuovere eventhub consumergroup dalla eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="2898b-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="2898b-109">Rimuove il consumergroup denominato myconsumergroup dal IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="2898b-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2898b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2898b-110">PARAMETERS</span></span>

### <span data-ttu-id="2898b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2898b-111">-DefaultProfile</span></span>
<span data-ttu-id="2898b-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2898b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2898b-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="2898b-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="2898b-114">EventHub ConsumerGroup nome.</span><span class="sxs-lookup"><span data-stu-id="2898b-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2898b-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="2898b-115">-EventHubEndpointName</span></span>
<span data-ttu-id="2898b-116">Nome dell'endpoint EventHub.</span><span class="sxs-lookup"><span data-stu-id="2898b-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="2898b-117">Eventi di valori possibili, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="2898b-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="2898b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2898b-118">-Name</span></span>
<span data-ttu-id="2898b-119">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="2898b-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="2898b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2898b-120">-ResourceGroupName</span></span>
<span data-ttu-id="2898b-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="2898b-121">Resource Group Name</span></span>

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

### <span data-ttu-id="2898b-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2898b-122">-Confirm</span></span>
<span data-ttu-id="2898b-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2898b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2898b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2898b-124">-WhatIf</span></span>
<span data-ttu-id="2898b-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2898b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2898b-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2898b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2898b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2898b-127">CommonParameters</span></span>
<span data-ttu-id="2898b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2898b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2898b-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2898b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2898b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2898b-130">INPUTS</span></span>

### <span data-ttu-id="2898b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2898b-131">System.String</span></span>

## <span data-ttu-id="2898b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2898b-132">OUTPUTS</span></span>

### <span data-ttu-id="2898b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2898b-133">System.String</span></span>

## <span data-ttu-id="2898b-134">Note</span><span class="sxs-lookup"><span data-stu-id="2898b-134">NOTES</span></span>

## <span data-ttu-id="2898b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2898b-135">RELATED LINKS</span></span>
