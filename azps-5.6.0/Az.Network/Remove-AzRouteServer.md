---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServer.md
ms.openlocfilehash: 5fc8f30a2ef8a0ee276c9fb7ac3f1e2a503f6ec4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992542"
---
# <span data-ttu-id="1e4cd-101">Remove-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="1e4cd-101">Remove-AzRouteServer</span></span>

## <span data-ttu-id="1e4cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4cd-103">Elimina un server di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-103">Deletes an Azure RouteServer.</span></span>

## <span data-ttu-id="1e4cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e4cd-104">SYNTAX</span></span>

### <span data-ttu-id="1e4cd-105">RouteServerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e4cd-105">RouteServerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e4cd-106">RouteServerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e4cd-106">RouteServerInputObjectParameterSet</span></span>
```
Remove-AzRouteServer -InputObject <PSRouteServer> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e4cd-107">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e4cd-107">RouteServerResourceIdParameterSet</span></span>
```
Remove-AzRouteServer -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e4cd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1e4cd-108">DESCRIPTION</span></span>
<span data-ttu-id="1e4cd-109">Il cmdlet **Remove-AzRouteServer** elimina un Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="1e4cd-109">The **Remove-AzRouteServer** cmdlet deletes an Azure RouteServer</span></span>

## <span data-ttu-id="1e4cd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e4cd-110">EXAMPLES</span></span>

### <span data-ttu-id="1e4cd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e4cd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
```

### <span data-ttu-id="1e4cd-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1e4cd-112">Example 2</span></span>
```powershell
PS C:\> $routeServerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer'
Remove-AzRouteServer -ResourceId $routeServerId
```

### <span data-ttu-id="1e4cd-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1e4cd-113">Example 3</span></span>
```powershell
PS C:\> $routeServer = Get-AzRouteServer -ResourceGroupName routeServerRG -RouteServerName routeServer
Remove-AzRouteServer -InputObject $routeServer
```

## <span data-ttu-id="1e4cd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e4cd-114">PARAMETERS</span></span>

### <span data-ttu-id="1e4cd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e4cd-115">-AsJob</span></span>
<span data-ttu-id="1e4cd-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1e4cd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e4cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4cd-117">-DefaultProfile</span></span>
<span data-ttu-id="1e4cd-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e4cd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1e4cd-119">-Force</span></span>
<span data-ttu-id="1e4cd-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="1e4cd-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1e4cd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e4cd-121">-InputObject</span></span>
<span data-ttu-id="1e4cd-122">Oggetto di input del server di route.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-122">The route server input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServer
Parameter Sets: RouteServerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e4cd-123">-PassThru</span></span>
<span data-ttu-id="1e4cd-124">Restituisce un oggetto che rappresenta l'elemento su cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="1e4cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e4cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="1e4cd-126">Nome del gruppo di risorse del server di route.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-126">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e4cd-127">-ResourceId</span></span>
<span data-ttu-id="1e4cd-128">ID di risorsa del server di route.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-128">The route server resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="1e4cd-129">-RouteServerName</span></span>
<span data-ttu-id="1e4cd-130">Nome del server di route.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-130">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e4cd-131">-Confirm</span></span>
<span data-ttu-id="1e4cd-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e4cd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e4cd-133">-WhatIf</span></span>
<span data-ttu-id="1e4cd-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e4cd-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e4cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4cd-136">CommonParameters</span></span>
<span data-ttu-id="1e4cd-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4cd-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4cd-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="1e4cd-139">INPUTS</span></span>

### <span data-ttu-id="1e4cd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1e4cd-140">System.String</span></span>

### <span data-ttu-id="1e4cd-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="1e4cd-141">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="1e4cd-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e4cd-142">OUTPUTS</span></span>

### <span data-ttu-id="1e4cd-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1e4cd-143">System.Boolean</span></span>

## <span data-ttu-id="1e4cd-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="1e4cd-144">NOTES</span></span>

## <span data-ttu-id="1e4cd-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e4cd-145">RELATED LINKS</span></span>
