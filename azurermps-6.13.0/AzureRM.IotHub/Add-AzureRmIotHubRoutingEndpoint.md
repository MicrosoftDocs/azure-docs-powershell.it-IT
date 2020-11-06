---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: d251d3159111437cd06880a49069aee7aca6d80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513808"
---
# <span data-ttu-id="e1ad7-101">Add-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1ad7-101">Add-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="e1ad7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ad7-103">Aggiungere un endpoint a un hub molto</span><span class="sxs-lookup"><span data-stu-id="e1ad7-103">Add an endpoint to your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ad7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1ad7-104">SYNTAX</span></span>

### <span data-ttu-id="e1ad7-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e1ad7-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1ad7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e1ad7-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1ad7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e1ad7-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ad7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1ad7-108">DESCRIPTION</span></span>
<span data-ttu-id="e1ad7-109">Aggiungere un nuovo endpoint nell'hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="e1ad7-110">Per informazioni sugli endpoint supportati, vedere https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="e1ad7-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="e1ad7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1ad7-111">EXAMPLES</span></span>

### <span data-ttu-id="e1ad7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1ad7-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="e1ad7-113">Aggiungere un nuovo endpoint "E2" di tipo EventHub a un hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="e1ad7-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="e1ad7-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e1ad7-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : avro
```

<span data-ttu-id="e1ad7-115">Aggiungere un nuovo endpoint "S1" di tipo AzureStorageContainer a un hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="e1ad7-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="e1ad7-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1ad7-116">PARAMETERS</span></span>

### <span data-ttu-id="e1ad7-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e1ad7-117">-ConnectionString</span></span>
<span data-ttu-id="e1ad7-118">Stringa di connessione dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="e1ad7-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ad7-119">-DefaultProfile</span></span>
<span data-ttu-id="e1ad7-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1ad7-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e1ad7-121">-EndpointName</span></span>
<span data-ttu-id="e1ad7-122">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="e1ad7-122">Name of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad7-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e1ad7-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="e1ad7-124">Gruppo di risorse dell'endpoint Resoure</span><span class="sxs-lookup"><span data-stu-id="e1ad7-124">Resource group of the Endpoint resoure</span></span>

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

### <span data-ttu-id="e1ad7-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1ad7-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="e1ad7-126">SubscriptionId della risorsa endpoint</span><span class="sxs-lookup"><span data-stu-id="e1ad7-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad7-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="e1ad7-127">-EndpointType</span></span>
<span data-ttu-id="e1ad7-128">Tipo di endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="e1ad7-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1ad7-129">-InputObject</span></span>
<span data-ttu-id="e1ad7-130">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="e1ad7-130">IotHub Object</span></span>

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

### <span data-ttu-id="e1ad7-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1ad7-131">-Name</span></span>
<span data-ttu-id="e1ad7-132">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="e1ad7-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e1ad7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ad7-133">-ResourceGroupName</span></span>
<span data-ttu-id="e1ad7-134">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e1ad7-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e1ad7-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1ad7-135">-ResourceId</span></span>
<span data-ttu-id="e1ad7-136">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="e1ad7-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e1ad7-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e1ad7-137">-Confirm</span></span>
<span data-ttu-id="e1ad7-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ad7-139">-WhatIf</span></span>
<span data-ttu-id="e1ad7-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1ad7-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ad7-142">CommonParameters</span></span>
<span data-ttu-id="e1ad7-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ad7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ad7-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ad7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ad7-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1ad7-145">INPUTS</span></span>

### <span data-ttu-id="e1ad7-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e1ad7-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="e1ad7-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e1ad7-147">System.String</span></span>

## <span data-ttu-id="e1ad7-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1ad7-148">OUTPUTS</span></span>

### <span data-ttu-id="e1ad7-149">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1ad7-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="e1ad7-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpoint Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1ad7-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="e1ad7-151">Note</span><span class="sxs-lookup"><span data-stu-id="e1ad7-151">NOTES</span></span>

## <span data-ttu-id="e1ad7-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1ad7-152">RELATED LINKS</span></span>
