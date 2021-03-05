---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: fbb0801dd586731a938c773711d72847e7a96e50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997806"
---
# <span data-ttu-id="d532d-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="d532d-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="d532d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d532d-102">SYNOPSIS</span></span>
<span data-ttu-id="d532d-103">Creare un percorso nell'Hub IoT</span><span class="sxs-lookup"><span data-stu-id="d532d-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="d532d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d532d-104">SYNTAX</span></span>

### <span data-ttu-id="d532d-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d532d-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d532d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d532d-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d532d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d532d-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d532d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d532d-108">DESCRIPTION</span></span>
<span data-ttu-id="d532d-109">Creare una route per inviare una condizione e un'origine dati specifica all'endpoint desiderato.</span><span class="sxs-lookup"><span data-stu-id="d532d-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="d532d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d532d-110">EXAMPLES</span></span>

### <span data-ttu-id="d532d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d532d-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="d532d-112">Creare un nuovo percorso "R1".</span><span class="sxs-lookup"><span data-stu-id="d532d-112">Create a new route "R1".</span></span>

## <span data-ttu-id="d532d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d532d-113">PARAMETERS</span></span>

### <span data-ttu-id="d532d-114">-Condizione</span><span class="sxs-lookup"><span data-stu-id="d532d-114">-Condition</span></span>
<span data-ttu-id="d532d-115">Condizione valutata per l'applicazione della regola di routing</span><span class="sxs-lookup"><span data-stu-id="d532d-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="d532d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d532d-116">-DefaultProfile</span></span>
<span data-ttu-id="d532d-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d532d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d532d-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="d532d-118">-Enabled</span></span>
<span data-ttu-id="d532d-119">Abilita percorso</span><span class="sxs-lookup"><span data-stu-id="d532d-119">Enable route</span></span>

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

### <span data-ttu-id="d532d-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d532d-120">-EndpointName</span></span>
<span data-ttu-id="d532d-121">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="d532d-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="d532d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d532d-122">-InputObject</span></span>
<span data-ttu-id="d532d-123">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="d532d-123">IotHub Object</span></span>

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

### <span data-ttu-id="d532d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d532d-124">-Name</span></span>
<span data-ttu-id="d532d-125">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="d532d-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d532d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d532d-126">-ResourceGroupName</span></span>
<span data-ttu-id="d532d-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d532d-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d532d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d532d-128">-ResourceId</span></span>
<span data-ttu-id="d532d-129">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="d532d-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d532d-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="d532d-130">-RouteName</span></span>
<span data-ttu-id="d532d-131">Nome del percorso</span><span class="sxs-lookup"><span data-stu-id="d532d-131">Name of the Route</span></span>

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

### <span data-ttu-id="d532d-132">-Source</span><span class="sxs-lookup"><span data-stu-id="d532d-132">-Source</span></span>
<span data-ttu-id="d532d-133">Origine del percorso</span><span class="sxs-lookup"><span data-stu-id="d532d-133">Source of the route</span></span>

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

### <span data-ttu-id="d532d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d532d-134">-Confirm</span></span>
<span data-ttu-id="d532d-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d532d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d532d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d532d-136">-WhatIf</span></span>
<span data-ttu-id="d532d-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d532d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d532d-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d532d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d532d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d532d-139">CommonParameters</span></span>
<span data-ttu-id="d532d-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d532d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d532d-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d532d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d532d-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="d532d-142">INPUTS</span></span>

### <span data-ttu-id="d532d-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d532d-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d532d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d532d-144">System.String</span></span>

## <span data-ttu-id="d532d-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d532d-145">OUTPUTS</span></span>

### <span data-ttu-id="d532d-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="d532d-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="d532d-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="d532d-147">NOTES</span></span>

## <span data-ttu-id="d532d-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d532d-148">RELATED LINKS</span></span>
