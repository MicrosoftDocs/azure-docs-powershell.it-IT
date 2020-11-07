---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 065c2e185be1a9cdc0f495b61104f659076b54b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835896"
---
# <span data-ttu-id="e2e3d-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e2e3d-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="e2e3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e3d-103">Ottiene tutte le consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="e2e3d-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="e2e3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2e3d-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2e3d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2e3d-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e3d-106">Ottiene tutte le consumergroups eventhub per i diversi EventHubs usati da IotHub.</span><span class="sxs-lookup"><span data-stu-id="e2e3d-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="e2e3d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2e3d-107">EXAMPLES</span></span>

### <span data-ttu-id="e2e3d-108">L'esempio 1 restituisce tutte le consumergroups eventhub per la eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="e2e3d-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="e2e3d-109">Ottiene tutte le consumergroups eventhub per il eventhub di telemetria per il iothub denominato myiothub</span><span class="sxs-lookup"><span data-stu-id="e2e3d-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="e2e3d-110">L'esempio 2 recupera tutte le consumergroups eventhub per operationsmonitoring eventhub</span><span class="sxs-lookup"><span data-stu-id="e2e3d-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="e2e3d-111">Ottiene tutte le consumergroups eventhub per il eventhub operationsMonitoringEvents per il iothub denominato myiothub</span><span class="sxs-lookup"><span data-stu-id="e2e3d-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="e2e3d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2e3d-112">PARAMETERS</span></span>

### <span data-ttu-id="e2e3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e3d-113">-DefaultProfile</span></span>
<span data-ttu-id="e2e3d-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e2e3d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2e3d-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="e2e3d-115">-EventHubEndpointName</span></span>
<span data-ttu-id="e2e3d-116">Nome dell'endpoint dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="e2e3d-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="e2e3d-117">Eventi di valori possibili, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="e2e3d-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e3d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2e3d-118">-Name</span></span>
<span data-ttu-id="e2e3d-119">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="e2e3d-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="e2e3d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e3d-120">-ResourceGroupName</span></span>
<span data-ttu-id="e2e3d-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e2e3d-121">Resource Group Name</span></span>

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

### <span data-ttu-id="e2e3d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e3d-122">CommonParameters</span></span>
<span data-ttu-id="e2e3d-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e3d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e3d-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e3d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e3d-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2e3d-125">INPUTS</span></span>

### <span data-ttu-id="e2e3d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e2e3d-126">System.String</span></span>

## <span data-ttu-id="e2e3d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2e3d-127">OUTPUTS</span></span>

### <span data-ttu-id="e2e3d-128">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="e2e3d-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="e2e3d-129">Note</span><span class="sxs-lookup"><span data-stu-id="e2e3d-129">NOTES</span></span>

## <span data-ttu-id="e2e3d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2e3d-130">RELATED LINKS</span></span>
