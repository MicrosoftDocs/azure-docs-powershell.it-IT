---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 84da4142bdc1b5435ca895be1995c6b48b5881fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520078"
---
# <span data-ttu-id="513fe-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="513fe-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="513fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="513fe-102">SYNOPSIS</span></span>
<span data-ttu-id="513fe-103">Ottiene tutte le consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="513fe-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="513fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="513fe-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="513fe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="513fe-105">DESCRIPTION</span></span>
<span data-ttu-id="513fe-106">Ottiene tutte le consumergroups eventhub per i diversi EventHubs usati da IotHub.</span><span class="sxs-lookup"><span data-stu-id="513fe-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="513fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="513fe-107">EXAMPLES</span></span>

### <span data-ttu-id="513fe-108">L'esempio 1 restituisce tutte le consumergroups eventhub per la eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="513fe-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="513fe-109">Ottiene tutte le consumergroups eventhub per il eventhub di telemetria per il iothub denominato myiothub</span><span class="sxs-lookup"><span data-stu-id="513fe-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="513fe-110">L'esempio 2 recupera tutte le consumergroups eventhub per operationsmonitoring eventhub</span><span class="sxs-lookup"><span data-stu-id="513fe-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="513fe-111">Ottiene tutte le consumergroups eventhub per il eventhub operationsMonitoringEvents per il iothub denominato myiothub</span><span class="sxs-lookup"><span data-stu-id="513fe-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="513fe-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="513fe-112">PARAMETERS</span></span>

### <span data-ttu-id="513fe-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="513fe-113">-EventHubEndpointName</span></span>
<span data-ttu-id="513fe-114">Nome dell'endpoint dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="513fe-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="513fe-115">Eventi di valori possibili, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="513fe-115">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="513fe-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="513fe-116">-Name</span></span>
<span data-ttu-id="513fe-117">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="513fe-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="513fe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="513fe-118">-ResourceGroupName</span></span>
<span data-ttu-id="513fe-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="513fe-119">Resource Group Name</span></span>

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

### <span data-ttu-id="513fe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513fe-120">-DefaultProfile</span></span>
<span data-ttu-id="513fe-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="513fe-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="513fe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513fe-122">CommonParameters</span></span>
<span data-ttu-id="513fe-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="513fe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513fe-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="513fe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513fe-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="513fe-125">INPUTS</span></span>

### <span data-ttu-id="513fe-126">System. String</span><span class="sxs-lookup"><span data-stu-id="513fe-126">System.String</span></span>

## <span data-ttu-id="513fe-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="513fe-127">OUTPUTS</span></span>

### <span data-ttu-id="513fe-128">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="513fe-128">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="513fe-129">Note</span><span class="sxs-lookup"><span data-stu-id="513fe-129">NOTES</span></span>

## <span data-ttu-id="513fe-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="513fe-130">RELATED LINKS</span></span>

