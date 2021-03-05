---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 903c2d3e425ad64cd83072112f8da37f83e980c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964622"
---
# <span data-ttu-id="cbf46-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="cbf46-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="cbf46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbf46-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf46-103">Ottenere informazioni su tutti gli endpoint per l'Hub IoT</span><span class="sxs-lookup"><span data-stu-id="cbf46-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="cbf46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbf46-104">SYNTAX</span></span>

### <span data-ttu-id="cbf46-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cbf46-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbf46-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cbf46-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbf46-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cbf46-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbf46-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cbf46-108">DESCRIPTION</span></span>
<span data-ttu-id="cbf46-109">Ottenere informazioni sull'endpoint.</span><span class="sxs-lookup"><span data-stu-id="cbf46-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="cbf46-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbf46-110">EXAMPLES</span></span>

### <span data-ttu-id="cbf46-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cbf46-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="cbf46-112">Ottenere tutti gli endpoint dall'Hub IoT di "myiothub".</span><span class="sxs-lookup"><span data-stu-id="cbf46-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="cbf46-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cbf46-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="cbf46-114">Ottenere tutti gli endpoint di tipo EventHub dall'Hub IoT di "myiothub".</span><span class="sxs-lookup"><span data-stu-id="cbf46-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="cbf46-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="cbf46-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="cbf46-116">Ottenere tutti gli endpoint di tipo EventHub dall'Hub IoT di "myiothub".</span><span class="sxs-lookup"><span data-stu-id="cbf46-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="cbf46-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="cbf46-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="cbf46-118">Ottenere informazioni sull'endpoint dall'Hub IoT di "myiothub".</span><span class="sxs-lookup"><span data-stu-id="cbf46-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="cbf46-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbf46-119">PARAMETERS</span></span>

### <span data-ttu-id="cbf46-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf46-120">-DefaultProfile</span></span>
<span data-ttu-id="cbf46-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cbf46-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbf46-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cbf46-122">-EndpointName</span></span>
<span data-ttu-id="cbf46-123">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="cbf46-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="cbf46-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="cbf46-124">-EndpointType</span></span>
<span data-ttu-id="cbf46-125">Tipo di endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="cbf46-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="cbf46-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbf46-126">-InputObject</span></span>
<span data-ttu-id="cbf46-127">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="cbf46-127">IotHub Object</span></span>

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

### <span data-ttu-id="cbf46-128">-Name</span><span class="sxs-lookup"><span data-stu-id="cbf46-128">-Name</span></span>
<span data-ttu-id="cbf46-129">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="cbf46-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cbf46-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf46-130">-ResourceGroupName</span></span>
<span data-ttu-id="cbf46-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cbf46-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cbf46-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbf46-132">-ResourceId</span></span>
<span data-ttu-id="cbf46-133">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="cbf46-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cbf46-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf46-134">CommonParameters</span></span>
<span data-ttu-id="cbf46-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf46-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf46-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbf46-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf46-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="cbf46-137">INPUTS</span></span>

### <span data-ttu-id="cbf46-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cbf46-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cbf46-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cbf46-139">System.String</span></span>

## <span data-ttu-id="cbf46-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbf46-140">OUTPUTS</span></span>

### <span data-ttu-id="cbf46-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="cbf46-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="cbf46-142">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="cbf46-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cbf46-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="cbf46-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="cbf46-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="cbf46-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="cbf46-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="cbf46-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="cbf46-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="cbf46-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="cbf46-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cbf46-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="cbf46-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span><span class="sxs-lookup"><span data-stu-id="cbf46-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="cbf46-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span><span class="sxs-lookup"><span data-stu-id="cbf46-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="cbf46-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="cbf46-150">NOTES</span></span>

## <span data-ttu-id="cbf46-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbf46-151">RELATED LINKS</span></span>
