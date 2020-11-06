---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoute.md
ms.openlocfilehash: 1b248225e86f4294603d3a07f1d8a1c7068e2851
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515231"
---
# <span data-ttu-id="fc11e-101">Add-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="fc11e-101">Add-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="fc11e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc11e-102">SYNOPSIS</span></span>
<span data-ttu-id="fc11e-103">Creare una route in hub molto</span><span class="sxs-lookup"><span data-stu-id="fc11e-103">Create a route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc11e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc11e-104">SYNTAX</span></span>

### <span data-ttu-id="fc11e-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc11e-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source] <PSRoutingSource> [-EndpointName] <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc11e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc11e-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source] <PSRoutingSource>
 [-EndpointName] <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc11e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fc11e-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source] <PSRoutingSource>
 [-EndpointName] <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc11e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc11e-108">DESCRIPTION</span></span>
<span data-ttu-id="fc11e-109">Creare una route per inviare una specifica origine dati e una condizione a un endpoint desiderato.</span><span class="sxs-lookup"><span data-stu-id="fc11e-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="fc11e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc11e-110">EXAMPLES</span></span>

### <span data-ttu-id="fc11e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc11e-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="fc11e-112">Creare una nuova route "R1".</span><span class="sxs-lookup"><span data-stu-id="fc11e-112">Create a new route "R1".</span></span>

## <span data-ttu-id="fc11e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc11e-113">PARAMETERS</span></span>

### <span data-ttu-id="fc11e-114">-Condition</span><span class="sxs-lookup"><span data-stu-id="fc11e-114">-Condition</span></span>
<span data-ttu-id="fc11e-115">Condizione che viene valutata per applicare la regola di routing</span><span class="sxs-lookup"><span data-stu-id="fc11e-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="fc11e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc11e-116">-DefaultProfile</span></span>
<span data-ttu-id="fc11e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc11e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc11e-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="fc11e-118">-Enabled</span></span>
<span data-ttu-id="fc11e-119">Abilitare la route</span><span class="sxs-lookup"><span data-stu-id="fc11e-119">Enable route</span></span>

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

### <span data-ttu-id="fc11e-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fc11e-120">-EndpointName</span></span>
<span data-ttu-id="fc11e-121">Nome dell'endpoint di routing</span><span class="sxs-lookup"><span data-stu-id="fc11e-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="fc11e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc11e-122">-InputObject</span></span>
<span data-ttu-id="fc11e-123">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="fc11e-123">IotHub Object</span></span>

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

### <span data-ttu-id="fc11e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc11e-124">-Name</span></span>
<span data-ttu-id="fc11e-125">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="fc11e-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fc11e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc11e-126">-ResourceGroupName</span></span>
<span data-ttu-id="fc11e-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fc11e-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fc11e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc11e-128">-ResourceId</span></span>
<span data-ttu-id="fc11e-129">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="fc11e-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fc11e-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="fc11e-130">-RouteName</span></span>
<span data-ttu-id="fc11e-131">Nome della route</span><span class="sxs-lookup"><span data-stu-id="fc11e-131">Name of the Route</span></span>

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

### <span data-ttu-id="fc11e-132">-Origine</span><span class="sxs-lookup"><span data-stu-id="fc11e-132">-Source</span></span>
<span data-ttu-id="fc11e-133">Origine della route</span><span class="sxs-lookup"><span data-stu-id="fc11e-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc11e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fc11e-134">-Confirm</span></span>
<span data-ttu-id="fc11e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc11e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc11e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc11e-136">-WhatIf</span></span>
<span data-ttu-id="fc11e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc11e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc11e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc11e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc11e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc11e-139">CommonParameters</span></span>
<span data-ttu-id="fc11e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc11e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc11e-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc11e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc11e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc11e-142">INPUTS</span></span>

### <span data-ttu-id="fc11e-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fc11e-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="fc11e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fc11e-144">System.String</span></span>

## <span data-ttu-id="fc11e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc11e-145">OUTPUTS</span></span>

### <span data-ttu-id="fc11e-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="fc11e-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="fc11e-147">Note</span><span class="sxs-lookup"><span data-stu-id="fc11e-147">NOTES</span></span>

## <span data-ttu-id="fc11e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc11e-148">RELATED LINKS</span></span>
