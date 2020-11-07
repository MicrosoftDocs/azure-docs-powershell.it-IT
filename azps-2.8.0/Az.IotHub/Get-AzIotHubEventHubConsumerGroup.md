---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 3905111a0855eef6421a587bc7151b411106d13a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674240"
---
# <span data-ttu-id="d89ea-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d89ea-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="d89ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d89ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d89ea-103">Ottiene tutte le consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="d89ea-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="d89ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d89ea-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d89ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d89ea-105">DESCRIPTION</span></span>
<span data-ttu-id="d89ea-106">Ottiene tutte le consumergroups eventhub per i diversi EventHubs usati da IotHub.</span><span class="sxs-lookup"><span data-stu-id="d89ea-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="d89ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d89ea-107">EXAMPLES</span></span>

### <span data-ttu-id="d89ea-108">L'esempio 1 restituisce tutte le consumergroups eventhub per la eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="d89ea-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="d89ea-109">Ottiene tutte le consumergroups eventhub per il eventhub di telemetria per il iothub denominato myiothub</span><span class="sxs-lookup"><span data-stu-id="d89ea-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="d89ea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d89ea-110">PARAMETERS</span></span>

### <span data-ttu-id="d89ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89ea-111">-DefaultProfile</span></span>
<span data-ttu-id="d89ea-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d89ea-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d89ea-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="d89ea-113">-EventHubEndpointName</span></span>
<span data-ttu-id="d89ea-114">Nome dell'endpoint dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="d89ea-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="d89ea-115">Eventi di valori possibili, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="d89ea-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="d89ea-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d89ea-116">-Name</span></span>
<span data-ttu-id="d89ea-117">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="d89ea-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="d89ea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d89ea-118">-ResourceGroupName</span></span>
<span data-ttu-id="d89ea-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d89ea-119">Resource Group Name</span></span>

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

### <span data-ttu-id="d89ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89ea-120">CommonParameters</span></span>
<span data-ttu-id="d89ea-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d89ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89ea-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d89ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89ea-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d89ea-123">INPUTS</span></span>

### <span data-ttu-id="d89ea-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d89ea-124">System.String</span></span>

## <span data-ttu-id="d89ea-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d89ea-125">OUTPUTS</span></span>

### <span data-ttu-id="d89ea-126">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="d89ea-126">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="d89ea-127">Note</span><span class="sxs-lookup"><span data-stu-id="d89ea-127">NOTES</span></span>

## <span data-ttu-id="d89ea-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d89ea-128">RELATED LINKS</span></span>
