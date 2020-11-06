---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 62704390e28f6f6a256b2202a61d1e400de7f7e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515680"
---
# <span data-ttu-id="d95be-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d95be-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="d95be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d95be-102">SYNOPSIS</span></span>
<span data-ttu-id="d95be-103">Ottiene tutte le consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="d95be-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d95be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d95be-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d95be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d95be-105">DESCRIPTION</span></span>
<span data-ttu-id="d95be-106">Ottiene tutte le consumergroups eventhub per i diversi EventHubs usati da IotHub.</span><span class="sxs-lookup"><span data-stu-id="d95be-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="d95be-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d95be-107">EXAMPLES</span></span>

### <span data-ttu-id="d95be-108">L'esempio 1 restituisce tutte le consumergroups eventhub per la eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="d95be-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="d95be-109">Ottiene tutte le consumergroups eventhub per il eventhub di telemetria per il iothub denominato myiothub</span><span class="sxs-lookup"><span data-stu-id="d95be-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="d95be-110">L'esempio 2 recupera tutte le consumergroups eventhub per operationsmonitoring eventhub</span><span class="sxs-lookup"><span data-stu-id="d95be-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="d95be-111">Ottiene tutte le consumergroups eventhub per il eventhub operationsMonitoringEvents per il iothub denominato myiothub</span><span class="sxs-lookup"><span data-stu-id="d95be-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="d95be-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d95be-112">PARAMETERS</span></span>

### <span data-ttu-id="d95be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95be-113">-DefaultProfile</span></span>
<span data-ttu-id="d95be-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d95be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d95be-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="d95be-115">-EventHubEndpointName</span></span>
<span data-ttu-id="d95be-116">Nome dell'endpoint dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="d95be-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="d95be-117">Eventi di valori possibili, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="d95be-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d95be-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d95be-118">-Name</span></span>
<span data-ttu-id="d95be-119">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="d95be-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="d95be-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d95be-120">-ResourceGroupName</span></span>
<span data-ttu-id="d95be-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d95be-121">Resource Group Name</span></span>

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

### <span data-ttu-id="d95be-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95be-122">CommonParameters</span></span>
<span data-ttu-id="d95be-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d95be-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95be-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d95be-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95be-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d95be-125">INPUTS</span></span>

### <span data-ttu-id="d95be-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d95be-126">System.String</span></span>

## <span data-ttu-id="d95be-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d95be-127">OUTPUTS</span></span>

### <span data-ttu-id="d95be-128">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d95be-128">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d95be-129">Note</span><span class="sxs-lookup"><span data-stu-id="d95be-129">NOTES</span></span>

## <span data-ttu-id="d95be-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d95be-130">RELATED LINKS</span></span>

