---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 2af7a4518d551509089585877f74468510746dcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188238"
---
# <span data-ttu-id="49738-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="49738-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="49738-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49738-102">SYNOPSIS</span></span>
<span data-ttu-id="49738-103">Aggiungere un endpoint all'Hub IoT</span><span class="sxs-lookup"><span data-stu-id="49738-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="49738-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49738-104">SYNTAX</span></span>

### <span data-ttu-id="49738-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49738-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49738-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="49738-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49738-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="49738-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49738-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="49738-108">DESCRIPTION</span></span>
<span data-ttu-id="49738-109">Aggiungere un nuovo endpoint nell'hub IoT.</span><span class="sxs-lookup"><span data-stu-id="49738-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="49738-110">Per informazioni sugli endpoint supportati, vedi https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="49738-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="49738-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49738-111">EXAMPLES</span></span>

### <span data-ttu-id="49738-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49738-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="49738-113">Aggiungere un nuovo endpoint "E2" di tipo EventHub a un hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="49738-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="49738-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="49738-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container -Encoding json

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : json
```

<span data-ttu-id="49738-115">Aggiungere un nuovo endpoint "S1" di tipo AzureStorageContainer a un hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="49738-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="49738-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49738-116">PARAMETERS</span></span>

### <span data-ttu-id="49738-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="49738-117">-ConnectionString</span></span>
<span data-ttu-id="49738-118">Stringa di connessione dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="49738-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49738-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49738-119">-DefaultProfile</span></span>
<span data-ttu-id="49738-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49738-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49738-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="49738-121">-EndpointName</span></span>
<span data-ttu-id="49738-122">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="49738-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="49738-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="49738-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="49738-124">Gruppo di risorse della risorsa Endpoint</span><span class="sxs-lookup"><span data-stu-id="49738-124">Resource group of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49738-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49738-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="49738-126">SubscriptionId della risorsa Endpoint</span><span class="sxs-lookup"><span data-stu-id="49738-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49738-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="49738-127">-EndpointType</span></span>
<span data-ttu-id="49738-128">Tipo di endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="49738-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49738-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="49738-129">-ContainerName</span></span>
<span data-ttu-id="49738-130">Nome del contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="49738-130">Name of the storage container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49738-131">-Encoding</span><span class="sxs-lookup"><span data-stu-id="49738-131">-Encoding</span></span>
<span data-ttu-id="49738-132">Selezionare il formato in cui instradare i dati.</span><span class="sxs-lookup"><span data-stu-id="49738-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="49738-133">È possibile selezionare JSON o AVRO.</span><span class="sxs-lookup"><span data-stu-id="49738-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="49738-134">L'impostazione predefinita è AVRO.</span><span class="sxs-lookup"><span data-stu-id="49738-134">The default is set to AVRO.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:
Accepted values: JSON, AVRO

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49738-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49738-135">-InputObject</span></span>
<span data-ttu-id="49738-136">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="49738-136">IotHub Object</span></span>

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

### <span data-ttu-id="49738-137">-Name</span><span class="sxs-lookup"><span data-stu-id="49738-137">-Name</span></span>
<span data-ttu-id="49738-138">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="49738-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="49738-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49738-139">-ResourceGroupName</span></span>
<span data-ttu-id="49738-140">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="49738-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="49738-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49738-141">-ResourceId</span></span>
<span data-ttu-id="49738-142">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="49738-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="49738-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49738-143">-Confirm</span></span>
<span data-ttu-id="49738-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49738-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49738-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49738-145">-WhatIf</span></span>
<span data-ttu-id="49738-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49738-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49738-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49738-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49738-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49738-148">CommonParameters</span></span>
<span data-ttu-id="49738-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49738-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49738-150">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49738-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49738-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="49738-151">INPUTS</span></span>

### <span data-ttu-id="49738-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="49738-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="49738-153">System.String</span><span class="sxs-lookup"><span data-stu-id="49738-153">System.String</span></span>

## <span data-ttu-id="49738-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49738-154">OUTPUTS</span></span>

### <span data-ttu-id="49738-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="49738-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="49738-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="49738-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="49738-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="49738-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="49738-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="49738-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="49738-159">NOTE</span><span class="sxs-lookup"><span data-stu-id="49738-159">NOTES</span></span>

## <span data-ttu-id="49738-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49738-160">RELATED LINKS</span></span>
