---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: 0ce0a651444bd30a1bf6c766083b0a8584c5cd71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995495"
---
# <span data-ttu-id="c402a-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="c402a-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="c402a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c402a-102">SYNOPSIS</span></span>
<span data-ttu-id="c402a-103">Eliminare una route nell'Hub IoT</span><span class="sxs-lookup"><span data-stu-id="c402a-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="c402a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c402a-104">SYNTAX</span></span>

### <span data-ttu-id="c402a-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c402a-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c402a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c402a-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c402a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c402a-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c402a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c402a-108">DESCRIPTION</span></span>
<span data-ttu-id="c402a-109">Eliminare un'route a un endpoint</span><span class="sxs-lookup"><span data-stu-id="c402a-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="c402a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c402a-110">EXAMPLES</span></span>

### <span data-ttu-id="c402a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c402a-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="c402a-112">Eliminare la route "R1" dall'Hub IoT di "myiothub".</span><span class="sxs-lookup"><span data-stu-id="c402a-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="c402a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c402a-113">PARAMETERS</span></span>

### <span data-ttu-id="c402a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c402a-114">-DefaultProfile</span></span>
<span data-ttu-id="c402a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c402a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c402a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c402a-116">-InputObject</span></span>
<span data-ttu-id="c402a-117">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="c402a-117">IotHub Object</span></span>

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

### <span data-ttu-id="c402a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c402a-118">-Name</span></span>
<span data-ttu-id="c402a-119">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="c402a-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c402a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c402a-120">-PassThru</span></span>
<span data-ttu-id="c402a-121">Consente di restituire l'oggetto booleano.</span><span class="sxs-lookup"><span data-stu-id="c402a-121">Allows to return the boolean object.</span></span> <span data-ttu-id="c402a-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c402a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c402a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c402a-123">-ResourceGroupName</span></span>
<span data-ttu-id="c402a-124">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c402a-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c402a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c402a-125">-ResourceId</span></span>
<span data-ttu-id="c402a-126">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="c402a-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c402a-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="c402a-127">-RouteName</span></span>
<span data-ttu-id="c402a-128">Nome del percorso</span><span class="sxs-lookup"><span data-stu-id="c402a-128">Name of the Route</span></span>

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

### <span data-ttu-id="c402a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c402a-129">-Confirm</span></span>
<span data-ttu-id="c402a-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c402a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c402a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c402a-131">-WhatIf</span></span>
<span data-ttu-id="c402a-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c402a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c402a-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c402a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c402a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c402a-134">CommonParameters</span></span>
<span data-ttu-id="c402a-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c402a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c402a-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c402a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c402a-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="c402a-137">INPUTS</span></span>

### <span data-ttu-id="c402a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c402a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c402a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c402a-139">System.String</span></span>

## <span data-ttu-id="c402a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c402a-140">OUTPUTS</span></span>

### <span data-ttu-id="c402a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c402a-141">System.Boolean</span></span>

## <span data-ttu-id="c402a-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="c402a-142">NOTES</span></span>

## <span data-ttu-id="c402a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c402a-143">RELATED LINKS</span></span>
