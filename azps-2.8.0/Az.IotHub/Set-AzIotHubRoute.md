---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: 97304a55c75291e03d92aae1436344819402fcff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674189"
---
# <span data-ttu-id="18bb6-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="18bb6-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="18bb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="18bb6-103">Aggiornare una route in hub molto</span><span class="sxs-lookup"><span data-stu-id="18bb6-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="18bb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18bb6-104">SYNTAX</span></span>

### <span data-ttu-id="18bb6-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18bb6-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18bb6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="18bb6-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18bb6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="18bb6-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18bb6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18bb6-108">DESCRIPTION</span></span>
<span data-ttu-id="18bb6-109">Modificare una route.</span><span class="sxs-lookup"><span data-stu-id="18bb6-109">Edit a route.</span></span> <span data-ttu-id="18bb6-110">È possibile aggiornare tutti i campi di una route, inclusi l'origine dati, l'endpoint, la query di routing e anche abilitare o disabilitare la route.</span><span class="sxs-lookup"><span data-stu-id="18bb6-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="18bb6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18bb6-111">EXAMPLES</span></span>

### <span data-ttu-id="18bb6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18bb6-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="18bb6-113">Aggiornamento delle informazioni sulla route.</span><span class="sxs-lookup"><span data-stu-id="18bb6-113">Updating the route information.</span></span>

### <span data-ttu-id="18bb6-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="18bb6-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="18bb6-115">Aggiornamento delle informazioni sulla route.</span><span class="sxs-lookup"><span data-stu-id="18bb6-115">Updating the route information.</span></span>

### <span data-ttu-id="18bb6-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="18bb6-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="18bb6-117">Aggiornamento delle informazioni sulla route.</span><span class="sxs-lookup"><span data-stu-id="18bb6-117">Updating the route information.</span></span>

## <span data-ttu-id="18bb6-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18bb6-118">PARAMETERS</span></span>

### <span data-ttu-id="18bb6-119">-Condition</span><span class="sxs-lookup"><span data-stu-id="18bb6-119">-Condition</span></span>
<span data-ttu-id="18bb6-120">Condizione che viene valutata per applicare la regola di routing</span><span class="sxs-lookup"><span data-stu-id="18bb6-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="18bb6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18bb6-121">-DefaultProfile</span></span>
<span data-ttu-id="18bb6-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18bb6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18bb6-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="18bb6-123">-Enabled</span></span>
<span data-ttu-id="18bb6-124">Abilitare la route</span><span class="sxs-lookup"><span data-stu-id="18bb6-124">Enable route</span></span>

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

### <span data-ttu-id="18bb6-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="18bb6-125">-EndpointName</span></span>
<span data-ttu-id="18bb6-126">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="18bb6-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="18bb6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18bb6-127">-InputObject</span></span>
<span data-ttu-id="18bb6-128">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="18bb6-128">IotHub Object</span></span>

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

### <span data-ttu-id="18bb6-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="18bb6-129">-Name</span></span>
<span data-ttu-id="18bb6-130">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="18bb6-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="18bb6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18bb6-131">-ResourceGroupName</span></span>
<span data-ttu-id="18bb6-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="18bb6-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="18bb6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18bb6-133">-ResourceId</span></span>
<span data-ttu-id="18bb6-134">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="18bb6-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="18bb6-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="18bb6-135">-RouteName</span></span>
<span data-ttu-id="18bb6-136">Nome della route</span><span class="sxs-lookup"><span data-stu-id="18bb6-136">Name of the Route</span></span>

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

### <span data-ttu-id="18bb6-137">-Origine</span><span class="sxs-lookup"><span data-stu-id="18bb6-137">-Source</span></span>
<span data-ttu-id="18bb6-138">Origine della route</span><span class="sxs-lookup"><span data-stu-id="18bb6-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18bb6-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18bb6-139">-Confirm</span></span>
<span data-ttu-id="18bb6-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18bb6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18bb6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18bb6-141">-WhatIf</span></span>
<span data-ttu-id="18bb6-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18bb6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18bb6-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18bb6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18bb6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18bb6-144">CommonParameters</span></span>
<span data-ttu-id="18bb6-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18bb6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18bb6-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18bb6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18bb6-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18bb6-147">INPUTS</span></span>

### <span data-ttu-id="18bb6-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="18bb6-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="18bb6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="18bb6-149">System.String</span></span>

## <span data-ttu-id="18bb6-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18bb6-150">OUTPUTS</span></span>

### <span data-ttu-id="18bb6-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="18bb6-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="18bb6-152">Note</span><span class="sxs-lookup"><span data-stu-id="18bb6-152">NOTES</span></span>

## <span data-ttu-id="18bb6-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18bb6-153">RELATED LINKS</span></span>
