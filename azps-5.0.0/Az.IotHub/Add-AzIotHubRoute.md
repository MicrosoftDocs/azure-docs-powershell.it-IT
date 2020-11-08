---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: a84d432e5771b5f04a7d9f478cd8ef446e08620a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201235"
---
# <span data-ttu-id="13055-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="13055-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="13055-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13055-102">SYNOPSIS</span></span>
<span data-ttu-id="13055-103">Creare una route in hub molto</span><span class="sxs-lookup"><span data-stu-id="13055-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="13055-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13055-104">SYNTAX</span></span>

### <span data-ttu-id="13055-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="13055-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13055-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="13055-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13055-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="13055-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13055-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13055-108">DESCRIPTION</span></span>
<span data-ttu-id="13055-109">Creare una route per inviare una specifica origine dati e una condizione a un endpoint desiderato.</span><span class="sxs-lookup"><span data-stu-id="13055-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="13055-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13055-110">EXAMPLES</span></span>

### <span data-ttu-id="13055-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13055-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="13055-112">Creare una nuova route "R1".</span><span class="sxs-lookup"><span data-stu-id="13055-112">Create a new route "R1".</span></span>

## <span data-ttu-id="13055-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13055-113">PARAMETERS</span></span>

### <span data-ttu-id="13055-114">-Condition</span><span class="sxs-lookup"><span data-stu-id="13055-114">-Condition</span></span>
<span data-ttu-id="13055-115">Condizione che viene valutata per applicare la regola di routing</span><span class="sxs-lookup"><span data-stu-id="13055-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="13055-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13055-116">-DefaultProfile</span></span>
<span data-ttu-id="13055-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13055-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13055-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="13055-118">-Enabled</span></span>
<span data-ttu-id="13055-119">Abilitare la route</span><span class="sxs-lookup"><span data-stu-id="13055-119">Enable route</span></span>

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

### <span data-ttu-id="13055-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="13055-120">-EndpointName</span></span>
<span data-ttu-id="13055-121">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="13055-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="13055-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13055-122">-InputObject</span></span>
<span data-ttu-id="13055-123">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="13055-123">IotHub Object</span></span>

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

### <span data-ttu-id="13055-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="13055-124">-Name</span></span>
<span data-ttu-id="13055-125">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="13055-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="13055-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13055-126">-ResourceGroupName</span></span>
<span data-ttu-id="13055-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="13055-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="13055-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13055-128">-ResourceId</span></span>
<span data-ttu-id="13055-129">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="13055-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="13055-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="13055-130">-RouteName</span></span>
<span data-ttu-id="13055-131">Nome della route</span><span class="sxs-lookup"><span data-stu-id="13055-131">Name of the Route</span></span>

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

### <span data-ttu-id="13055-132">-Origine</span><span class="sxs-lookup"><span data-stu-id="13055-132">-Source</span></span>
<span data-ttu-id="13055-133">Origine della route</span><span class="sxs-lookup"><span data-stu-id="13055-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13055-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="13055-134">-Confirm</span></span>
<span data-ttu-id="13055-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13055-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13055-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13055-136">-WhatIf</span></span>
<span data-ttu-id="13055-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13055-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13055-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13055-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13055-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13055-139">CommonParameters</span></span>
<span data-ttu-id="13055-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13055-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13055-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13055-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13055-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13055-142">INPUTS</span></span>

### <span data-ttu-id="13055-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="13055-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="13055-144">System. String</span><span class="sxs-lookup"><span data-stu-id="13055-144">System.String</span></span>

## <span data-ttu-id="13055-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13055-145">OUTPUTS</span></span>

### <span data-ttu-id="13055-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="13055-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="13055-147">Note</span><span class="sxs-lookup"><span data-stu-id="13055-147">NOTES</span></span>

## <span data-ttu-id="13055-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13055-148">RELATED LINKS</span></span>
