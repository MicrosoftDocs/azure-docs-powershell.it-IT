---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 781959d3e8738af8c3520cf99762dfa5714a23c6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861342"
---
# <span data-ttu-id="fdbf3-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="fdbf3-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="fdbf3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdbf3-102">SYNOPSIS</span></span>
<span data-ttu-id="fdbf3-103">Eliminare un endpoint per l'hub di un sacco</span><span class="sxs-lookup"><span data-stu-id="fdbf3-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="fdbf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdbf3-104">SYNTAX</span></span>

### <span data-ttu-id="fdbf3-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fdbf3-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdbf3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fdbf3-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdbf3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fdbf3-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdbf3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdbf3-108">DESCRIPTION</span></span>
<span data-ttu-id="fdbf3-109">Eliminare un endpoint.</span><span class="sxs-lookup"><span data-stu-id="fdbf3-109">Delete an endpoint.</span></span> <span data-ttu-id="fdbf3-110">Ricordarsi di eliminare le route che usano questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="fdbf3-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="fdbf3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdbf3-111">EXAMPLES</span></span>

### <span data-ttu-id="fdbf3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fdbf3-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="fdbf3-113">Eliminare l'endpoint "E2" dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="fdbf3-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="fdbf3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdbf3-114">PARAMETERS</span></span>

### <span data-ttu-id="fdbf3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdbf3-115">-DefaultProfile</span></span>
<span data-ttu-id="fdbf3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdbf3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdbf3-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fdbf3-117">-EndpointName</span></span>
<span data-ttu-id="fdbf3-118">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="fdbf3-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="fdbf3-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="fdbf3-119">-EndpointType</span></span>
<span data-ttu-id="fdbf3-120">Tipo di endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="fdbf3-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="fdbf3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdbf3-121">-InputObject</span></span>
<span data-ttu-id="fdbf3-122">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="fdbf3-122">IotHub Object</span></span>

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

### <span data-ttu-id="fdbf3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdbf3-123">-Name</span></span>
<span data-ttu-id="fdbf3-124">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="fdbf3-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fdbf3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdbf3-125">-PassThru</span></span>
<span data-ttu-id="fdbf3-126">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="fdbf3-126">Allows to return the boolean object.</span></span> <span data-ttu-id="fdbf3-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="fdbf3-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fdbf3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdbf3-128">-ResourceGroupName</span></span>
<span data-ttu-id="fdbf3-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fdbf3-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fdbf3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdbf3-130">-ResourceId</span></span>
<span data-ttu-id="fdbf3-131">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="fdbf3-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fdbf3-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fdbf3-132">-Confirm</span></span>
<span data-ttu-id="fdbf3-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdbf3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdbf3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdbf3-134">-WhatIf</span></span>
<span data-ttu-id="fdbf3-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdbf3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdbf3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdbf3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdbf3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdbf3-137">CommonParameters</span></span>
<span data-ttu-id="fdbf3-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdbf3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdbf3-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdbf3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdbf3-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdbf3-140">INPUTS</span></span>

### <span data-ttu-id="fdbf3-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fdbf3-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fdbf3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fdbf3-142">System.String</span></span>

## <span data-ttu-id="fdbf3-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdbf3-143">OUTPUTS</span></span>

### <span data-ttu-id="fdbf3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fdbf3-144">System.Boolean</span></span>

## <span data-ttu-id="fdbf3-145">Note</span><span class="sxs-lookup"><span data-stu-id="fdbf3-145">NOTES</span></span>

## <span data-ttu-id="fdbf3-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdbf3-146">RELATED LINKS</span></span>
