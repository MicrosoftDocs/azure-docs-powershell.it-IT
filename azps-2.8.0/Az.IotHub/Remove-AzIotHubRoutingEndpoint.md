---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 1ff1ba2d8e3a4a7ce8a80c364ff8ccee3e91d8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674200"
---
# <span data-ttu-id="25513-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="25513-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="25513-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25513-102">SYNOPSIS</span></span>
<span data-ttu-id="25513-103">Eliminare un endpoint per l'hub di un sacco</span><span class="sxs-lookup"><span data-stu-id="25513-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="25513-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25513-104">SYNTAX</span></span>

### <span data-ttu-id="25513-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="25513-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25513-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="25513-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25513-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="25513-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25513-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25513-108">DESCRIPTION</span></span>
<span data-ttu-id="25513-109">Eliminare un endpoint.</span><span class="sxs-lookup"><span data-stu-id="25513-109">Delete an endpoint.</span></span> <span data-ttu-id="25513-110">Ricordarsi di eliminare le route che usano questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="25513-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="25513-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25513-111">EXAMPLES</span></span>

### <span data-ttu-id="25513-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="25513-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="25513-113">Eliminare l'endpoint "E2" dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="25513-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="25513-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25513-114">PARAMETERS</span></span>

### <span data-ttu-id="25513-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25513-115">-DefaultProfile</span></span>
<span data-ttu-id="25513-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25513-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25513-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="25513-117">-EndpointName</span></span>
<span data-ttu-id="25513-118">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="25513-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="25513-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="25513-119">-EndpointType</span></span>
<span data-ttu-id="25513-120">Tipo di endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="25513-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="25513-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25513-121">-InputObject</span></span>
<span data-ttu-id="25513-122">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="25513-122">IotHub Object</span></span>

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

### <span data-ttu-id="25513-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="25513-123">-Name</span></span>
<span data-ttu-id="25513-124">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="25513-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="25513-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25513-125">-PassThru</span></span>
<span data-ttu-id="25513-126">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="25513-126">Allows to return the boolean object.</span></span> <span data-ttu-id="25513-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="25513-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25513-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25513-128">-ResourceGroupName</span></span>
<span data-ttu-id="25513-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="25513-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="25513-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25513-130">-ResourceId</span></span>
<span data-ttu-id="25513-131">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="25513-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="25513-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="25513-132">-Confirm</span></span>
<span data-ttu-id="25513-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25513-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25513-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25513-134">-WhatIf</span></span>
<span data-ttu-id="25513-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25513-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25513-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25513-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25513-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25513-137">CommonParameters</span></span>
<span data-ttu-id="25513-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25513-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25513-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25513-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25513-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25513-140">INPUTS</span></span>

### <span data-ttu-id="25513-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="25513-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="25513-142">System. String</span><span class="sxs-lookup"><span data-stu-id="25513-142">System.String</span></span>

## <span data-ttu-id="25513-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25513-143">OUTPUTS</span></span>

### <span data-ttu-id="25513-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25513-144">System.Boolean</span></span>

## <span data-ttu-id="25513-145">Note</span><span class="sxs-lookup"><span data-stu-id="25513-145">NOTES</span></span>

## <span data-ttu-id="25513-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25513-146">RELATED LINKS</span></span>
