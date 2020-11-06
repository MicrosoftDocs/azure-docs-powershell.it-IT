---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
ms.openlocfilehash: 9af711bd449bc8c69808f30dc99ceea806dee00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520990"
---
# <span data-ttu-id="fd6bf-101">Remove-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="fd6bf-101">Remove-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="fd6bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="fd6bf-103">Eliminare una route in hub molto</span><span class="sxs-lookup"><span data-stu-id="fd6bf-103">Delete a route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd6bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd6bf-104">SYNTAX</span></span>

### <span data-ttu-id="fd6bf-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd6bf-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd6bf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd6bf-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd6bf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd6bf-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd6bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd6bf-108">DESCRIPTION</span></span>
<span data-ttu-id="fd6bf-109">Eliminare una route in un endpoint</span><span class="sxs-lookup"><span data-stu-id="fd6bf-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="fd6bf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd6bf-110">EXAMPLES</span></span>

### <span data-ttu-id="fd6bf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd6bf-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="fd6bf-112">Eliminare route "R1" dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="fd6bf-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="fd6bf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd6bf-113">PARAMETERS</span></span>

### <span data-ttu-id="fd6bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd6bf-114">-DefaultProfile</span></span>
<span data-ttu-id="fd6bf-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd6bf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd6bf-116">-InputObject</span></span>
<span data-ttu-id="fd6bf-117">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="fd6bf-117">IotHub Object</span></span>

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

### <span data-ttu-id="fd6bf-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd6bf-118">-Name</span></span>
<span data-ttu-id="fd6bf-119">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="fd6bf-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fd6bf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd6bf-120">-PassThru</span></span>
<span data-ttu-id="fd6bf-121">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-121">Allows to return the boolean object.</span></span> <span data-ttu-id="fd6bf-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd6bf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd6bf-123">-ResourceGroupName</span></span>
<span data-ttu-id="fd6bf-124">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fd6bf-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fd6bf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd6bf-125">-ResourceId</span></span>
<span data-ttu-id="fd6bf-126">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="fd6bf-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fd6bf-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="fd6bf-127">-RouteName</span></span>
<span data-ttu-id="fd6bf-128">Nome della route</span><span class="sxs-lookup"><span data-stu-id="fd6bf-128">Name of the Route</span></span>

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

### <span data-ttu-id="fd6bf-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd6bf-129">-Confirm</span></span>
<span data-ttu-id="fd6bf-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd6bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd6bf-131">-WhatIf</span></span>
<span data-ttu-id="fd6bf-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd6bf-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd6bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd6bf-134">CommonParameters</span></span>
<span data-ttu-id="fd6bf-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd6bf-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd6bf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd6bf-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd6bf-137">INPUTS</span></span>

### <span data-ttu-id="fd6bf-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fd6bf-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="fd6bf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fd6bf-139">System.String</span></span>

## <span data-ttu-id="fd6bf-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd6bf-140">OUTPUTS</span></span>

### <span data-ttu-id="fd6bf-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd6bf-141">System.Boolean</span></span>

## <span data-ttu-id="fd6bf-142">Note</span><span class="sxs-lookup"><span data-stu-id="fd6bf-142">NOTES</span></span>

## <span data-ttu-id="fd6bf-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd6bf-143">RELATED LINKS</span></span>
