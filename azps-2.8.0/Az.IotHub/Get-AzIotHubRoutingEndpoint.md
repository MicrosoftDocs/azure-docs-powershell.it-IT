---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8852139cfcedc5ff0ee42c234c44b1505042ef1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674225"
---
# <span data-ttu-id="50553-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="50553-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="50553-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50553-102">SYNOPSIS</span></span>
<span data-ttu-id="50553-103">Ottenere informazioni su tutti gli endpoint per il mozzo di un sacco</span><span class="sxs-lookup"><span data-stu-id="50553-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="50553-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50553-104">SYNTAX</span></span>

### <span data-ttu-id="50553-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50553-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50553-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="50553-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50553-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="50553-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50553-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50553-108">DESCRIPTION</span></span>
<span data-ttu-id="50553-109">Ottenere informazioni sull'endpoint.</span><span class="sxs-lookup"><span data-stu-id="50553-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="50553-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50553-110">EXAMPLES</span></span>

### <span data-ttu-id="50553-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50553-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="50553-112">Ottenere tutti gli endpoint dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="50553-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="50553-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="50553-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="50553-114">Ottenere tutti gli endpoint di tipo EventHub dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="50553-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="50553-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="50553-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="50553-116">Ottenere tutti gli endpoint di tipo EventHub dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="50553-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="50553-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="50553-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="50553-118">Ottenere informazioni sull'endpoint dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="50553-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="50553-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50553-119">PARAMETERS</span></span>

### <span data-ttu-id="50553-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50553-120">-DefaultProfile</span></span>
<span data-ttu-id="50553-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50553-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50553-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="50553-122">-EndpointName</span></span>
<span data-ttu-id="50553-123">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="50553-123">Name of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50553-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="50553-124">-EndpointType</span></span>
<span data-ttu-id="50553-125">Tipo di endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="50553-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50553-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50553-126">-InputObject</span></span>
<span data-ttu-id="50553-127">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="50553-127">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50553-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="50553-128">-Name</span></span>
<span data-ttu-id="50553-129">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="50553-129">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50553-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50553-130">-ResourceGroupName</span></span>
<span data-ttu-id="50553-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="50553-131">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50553-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50553-132">-ResourceId</span></span>
<span data-ttu-id="50553-133">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="50553-133">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50553-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50553-134">CommonParameters</span></span>
<span data-ttu-id="50553-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50553-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50553-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50553-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50553-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50553-137">INPUTS</span></span>

### <span data-ttu-id="50553-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="50553-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="50553-139">System. String</span><span class="sxs-lookup"><span data-stu-id="50553-139">System.String</span></span>

## <span data-ttu-id="50553-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50553-140">OUTPUTS</span></span>

### <span data-ttu-id="50553-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="50553-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="50553-142">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubProperties, Microsoft. Azure. PowerShell. cmdlet. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="50553-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="50553-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="50553-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="50553-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="50553-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="50553-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="50553-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="50553-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpointProperties []</span><span class="sxs-lookup"><span data-stu-id="50553-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="50553-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="50553-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="50553-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerProperties []</span><span class="sxs-lookup"><span data-stu-id="50553-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="50553-149">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingCustomEndpoint []</span><span class="sxs-lookup"><span data-stu-id="50553-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="50553-150">Note</span><span class="sxs-lookup"><span data-stu-id="50553-150">NOTES</span></span>

## <span data-ttu-id="50553-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50553-151">RELATED LINKS</span></span>
