---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 2aa49f01b16547987604a7ee978018596c7d9647
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687853"
---
# <span data-ttu-id="50ef3-101">Get-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="50ef3-101">Get-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="50ef3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="50ef3-103">Ottenere informazioni su tutti gli endpoint per il mozzo di un sacco</span><span class="sxs-lookup"><span data-stu-id="50ef3-103">Get information on all the endpoints for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50ef3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50ef3-104">SYNTAX</span></span>

### <span data-ttu-id="50ef3-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50ef3-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String>
 [-EndpointType <PSEndpointType>] [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50ef3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="50ef3-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50ef3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="50ef3-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50ef3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50ef3-108">DESCRIPTION</span></span>
<span data-ttu-id="50ef3-109">Ottenere informazioni sull'endpoint.</span><span class="sxs-lookup"><span data-stu-id="50ef3-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="50ef3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50ef3-110">EXAMPLES</span></span>

### <span data-ttu-id="50ef3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50ef3-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="50ef3-112">Ottenere tutti gli endpoint dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="50ef3-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="50ef3-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="50ef3-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="50ef3-114">Ottenere tutti gli endpoint di tipo EventHub dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="50ef3-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="50ef3-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="50ef3-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="50ef3-116">Ottenere tutti gli endpoint di tipo EventHub dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="50ef3-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="50ef3-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="50ef3-117">Example 4</span></span>
```
PS C:\> Get-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="50ef3-118">Ottenere informazioni sull'endpoint dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="50ef3-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="50ef3-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50ef3-119">PARAMETERS</span></span>

### <span data-ttu-id="50ef3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ef3-120">-DefaultProfile</span></span>
<span data-ttu-id="50ef3-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50ef3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50ef3-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="50ef3-122">-EndpointName</span></span>
<span data-ttu-id="50ef3-123">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="50ef3-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="50ef3-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="50ef3-124">-EndpointType</span></span>
<span data-ttu-id="50ef3-125">Tipo di endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="50ef3-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="50ef3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50ef3-126">-InputObject</span></span>
<span data-ttu-id="50ef3-127">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="50ef3-127">IotHub Object</span></span>

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

### <span data-ttu-id="50ef3-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="50ef3-128">-Name</span></span>
<span data-ttu-id="50ef3-129">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="50ef3-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="50ef3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50ef3-130">-ResourceGroupName</span></span>
<span data-ttu-id="50ef3-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="50ef3-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="50ef3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50ef3-132">-ResourceId</span></span>
<span data-ttu-id="50ef3-133">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="50ef3-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="50ef3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ef3-134">CommonParameters</span></span>
<span data-ttu-id="50ef3-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ef3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ef3-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50ef3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ef3-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50ef3-137">INPUTS</span></span>

### <span data-ttu-id="50ef3-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="50ef3-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="50ef3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="50ef3-139">System.String</span></span>

## <span data-ttu-id="50ef3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50ef3-140">OUTPUTS</span></span>

### <span data-ttu-id="50ef3-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="50ef3-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="50ef3-142">System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingCustomEndpoint, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral</span><span class="sxs-lookup"><span data-stu-id="50ef3-142">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="50ef3-143">Note</span><span class="sxs-lookup"><span data-stu-id="50ef3-143">NOTES</span></span>

## <span data-ttu-id="50ef3-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50ef3-144">RELATED LINKS</span></span>
