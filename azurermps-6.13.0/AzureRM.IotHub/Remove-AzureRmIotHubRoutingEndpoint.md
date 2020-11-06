---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 6caad4faec3dd292f902689757b82b90091afcde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520988"
---
# <span data-ttu-id="edb4d-101">Remove-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="edb4d-101">Remove-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="edb4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="edb4d-102">SYNOPSIS</span></span>
<span data-ttu-id="edb4d-103">Eliminare un endpoint per l'hub di un sacco</span><span class="sxs-lookup"><span data-stu-id="edb4d-103">Delete an endpoint for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edb4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edb4d-104">SYNTAX</span></span>

### <span data-ttu-id="edb4d-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="edb4d-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edb4d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="edb4d-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edb4d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="edb4d-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edb4d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edb4d-108">DESCRIPTION</span></span>
<span data-ttu-id="edb4d-109">Eliminare un endpoint.</span><span class="sxs-lookup"><span data-stu-id="edb4d-109">Delete an endpoint.</span></span> <span data-ttu-id="edb4d-110">Ricordarsi di eliminare le route che usano questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="edb4d-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="edb4d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edb4d-111">EXAMPLES</span></span>

### <span data-ttu-id="edb4d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="edb4d-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="edb4d-113">Eliminare l'endpoint "E2" dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="edb4d-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="edb4d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="edb4d-114">PARAMETERS</span></span>

### <span data-ttu-id="edb4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb4d-115">-DefaultProfile</span></span>
<span data-ttu-id="edb4d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="edb4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edb4d-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="edb4d-117">-EndpointName</span></span>
<span data-ttu-id="edb4d-118">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="edb4d-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="edb4d-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="edb4d-119">-EndpointType</span></span>
<span data-ttu-id="edb4d-120">Tipo di endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="edb4d-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edb4d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edb4d-121">-InputObject</span></span>
<span data-ttu-id="edb4d-122">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="edb4d-122">IotHub Object</span></span>

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

### <span data-ttu-id="edb4d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="edb4d-123">-Name</span></span>
<span data-ttu-id="edb4d-124">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="edb4d-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="edb4d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edb4d-125">-PassThru</span></span>
<span data-ttu-id="edb4d-126">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="edb4d-126">Allows to return the boolean object.</span></span> <span data-ttu-id="edb4d-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="edb4d-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edb4d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb4d-128">-ResourceGroupName</span></span>
<span data-ttu-id="edb4d-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="edb4d-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="edb4d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edb4d-130">-ResourceId</span></span>
<span data-ttu-id="edb4d-131">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="edb4d-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="edb4d-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="edb4d-132">-Confirm</span></span>
<span data-ttu-id="edb4d-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edb4d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edb4d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb4d-134">-WhatIf</span></span>
<span data-ttu-id="edb4d-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edb4d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edb4d-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="edb4d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edb4d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb4d-137">CommonParameters</span></span>
<span data-ttu-id="edb4d-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb4d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb4d-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edb4d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb4d-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="edb4d-140">INPUTS</span></span>

### <span data-ttu-id="edb4d-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="edb4d-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="edb4d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="edb4d-142">System.String</span></span>

## <span data-ttu-id="edb4d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edb4d-143">OUTPUTS</span></span>

### <span data-ttu-id="edb4d-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="edb4d-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="edb4d-145">System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusQueueEndpointProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingServiceBusTopicEndpoint System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingStorageContainerProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]] System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRoutingCustomEndpoint, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral</span><span class="sxs-lookup"><span data-stu-id="edb4d-145">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="edb4d-146">Note</span><span class="sxs-lookup"><span data-stu-id="edb4d-146">NOTES</span></span>

## <span data-ttu-id="edb4d-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edb4d-147">RELATED LINKS</span></span>
