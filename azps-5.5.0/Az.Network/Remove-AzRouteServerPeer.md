---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
ms.openlocfilehash: d177c0dfa5ff59fde0adfe8ac4e3598ae70127f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202538"
---
# <span data-ttu-id="58e81-101">Remove-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="58e81-101">Remove-AzRouteServerPeer</span></span>

## <span data-ttu-id="58e81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58e81-102">SYNOPSIS</span></span>
<span data-ttu-id="58e81-103">Rimuove un peer da un Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="58e81-103">Removes a Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="58e81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58e81-104">SYNTAX</span></span>

### <span data-ttu-id="58e81-105">RouteServerNParameterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58e81-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58e81-106">RouteServerNParameeObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58e81-106">RouteServerNPeerInputObjectParameterSet</span></span>
```
Remove-AzRouteServerPeer -InputObject <PSRouteServerPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58e81-107">RouteServerNResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58e81-107">RouteServerNPeerResourceIdParameterSet</span></span>
```
Remove-AzRouteServerPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58e81-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="58e81-108">DESCRIPTION</span></span>
<span data-ttu-id="58e81-109">Il cmdlet **Remove-AzRouteServerDir** rimuove un peer RouteServer da un Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="58e81-109">The **Remove-AzRouteServerPeer** cmdlet removes a RouteServer Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="58e81-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58e81-110">EXAMPLES</span></span>

### <span data-ttu-id="58e81-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58e81-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServerPeer -PeerName peer -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="58e81-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="58e81-112">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Remove-AzRouteServerPeer -ResourceId $RouteServerPeerId
```

### <span data-ttu-id="58e81-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="58e81-113">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
Remove-AzRouteServerPeer -InputObject $RouteServerPeer
```
## <span data-ttu-id="58e81-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58e81-114">PARAMETERS</span></span>

### <span data-ttu-id="58e81-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58e81-115">-AsJob</span></span>
<span data-ttu-id="58e81-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="58e81-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58e81-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e81-117">-DefaultProfile</span></span>
<span data-ttu-id="58e81-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58e81-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58e81-119">-Force</span><span class="sxs-lookup"><span data-stu-id="58e81-119">-Force</span></span>
<span data-ttu-id="58e81-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="58e81-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="58e81-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58e81-121">-InputObject</span></span>
<span data-ttu-id="58e81-122">Oggetto di input peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="58e81-122">The route server peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer
Parameter Sets: RouteServerNPeerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58e81-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="58e81-123">-PeerName</span></span>
<span data-ttu-id="58e81-124">Nome del peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="58e81-124">The name of the route server Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e81-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e81-125">-ResourceGroupName</span></span>
<span data-ttu-id="58e81-126">Nome del gruppo di risorse del server/peer della route.</span><span class="sxs-lookup"><span data-stu-id="58e81-126">The resource group name of the route server/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e81-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58e81-127">-ResourceId</span></span>
<span data-ttu-id="58e81-128">ID della risorsa peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="58e81-128">The route server peer resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e81-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="58e81-129">-RouteServerName</span></span>
<span data-ttu-id="58e81-130">Server di route in cui è presente il peer.</span><span class="sxs-lookup"><span data-stu-id="58e81-130">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e81-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58e81-131">-Confirm</span></span>
<span data-ttu-id="58e81-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58e81-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58e81-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58e81-133">-WhatIf</span></span>
<span data-ttu-id="58e81-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58e81-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58e81-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58e81-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58e81-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e81-136">CommonParameters</span></span>
<span data-ttu-id="58e81-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e81-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e81-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="58e81-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e81-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="58e81-139">INPUTS</span></span>

### <span data-ttu-id="58e81-140">System.String</span><span class="sxs-lookup"><span data-stu-id="58e81-140">System.String</span></span>

### <span data-ttu-id="58e81-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerDir</span><span class="sxs-lookup"><span data-stu-id="58e81-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="58e81-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58e81-142">OUTPUTS</span></span>

### <span data-ttu-id="58e81-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="58e81-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="58e81-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="58e81-144">NOTES</span></span>

## <span data-ttu-id="58e81-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58e81-145">RELATED LINKS</span></span>
