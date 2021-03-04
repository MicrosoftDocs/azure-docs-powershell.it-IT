---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
ms.openlocfilehash: 3c0be49a09758648bcd2301f2643577ea8dcd951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951613"
---
# <span data-ttu-id="cead0-101">Update-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="cead0-101">Update-AzRouteServerPeer</span></span>

## <span data-ttu-id="cead0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cead0-102">SYNOPSIS</span></span>
<span data-ttu-id="cead0-103">Aggiornare un peer in un RouteServer di Azure</span><span class="sxs-lookup"><span data-stu-id="cead0-103">Update a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="cead0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cead0-104">SYNTAX</span></span>

### <span data-ttu-id="cead0-105">RouteServerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cead0-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cead0-106">RouteServerNParamenameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cead0-106">RouteServerNPeerNameParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cead0-107">RouteServerNParameeObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cead0-107">RouteServerNPeerInputObjectParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -InputObject <PSRouteServerPeer>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cead0-108">RouteServerNResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cead0-108">RouteServerNPeerResourceIdParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -ResourceId <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cead0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cead0-109">DESCRIPTION</span></span>
<span data-ttu-id="cead0-110">Il cmdlet **Update-AzRouteServerDir** aggiorna un peer RouteServer a un Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="cead0-110">The **Update-AzRouteServerPeer** cmdlet updates a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="cead0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cead0-111">EXAMPLES</span></span>

### <span data-ttu-id="cead0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cead0-112">Example 1</span></span>
```powershell
PS C:\> Update-AzRouteServerPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="cead0-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cead0-113">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/csr'
Update-AzRouteServerPeer -ResourceId $routeServerPeerId  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="cead0-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="cead0-114">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServer -RouteServerName routeServer -PeerName csr
Update-AzRouteServerPeer -ResourceGroupName routeServerRG -InputObject $routeServerPeer  -RouteServerName routeServer
```

## <span data-ttu-id="cead0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cead0-115">PARAMETERS</span></span>

### <span data-ttu-id="cead0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cead0-116">-AsJob</span></span>
<span data-ttu-id="cead0-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cead0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cead0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cead0-118">-DefaultProfile</span></span>
<span data-ttu-id="cead0-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cead0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cead0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cead0-120">-Force</span></span>
<span data-ttu-id="cead0-121">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="cead0-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cead0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cead0-122">-InputObject</span></span>
<span data-ttu-id="cead0-123">Oggetto di input peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="cead0-123">The route server peer input object.</span></span>

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

### <span data-ttu-id="cead0-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="cead0-124">-PeerAsn</span></span>
<span data-ttu-id="cead0-125">ASN del peer del server route remoto.</span><span class="sxs-lookup"><span data-stu-id="cead0-125">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cead0-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="cead0-126">-PeerIp</span></span>
<span data-ttu-id="cead0-127">Ip del peer del server route remoto.</span><span class="sxs-lookup"><span data-stu-id="cead0-127">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="cead0-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="cead0-128">-PeerName</span></span>
<span data-ttu-id="cead0-129">Nome del peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="cead0-129">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="cead0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cead0-130">-ResourceGroupName</span></span>
<span data-ttu-id="cead0-131">Nome del gruppo di risorse del server/peer della route.</span><span class="sxs-lookup"><span data-stu-id="cead0-131">The resource group name of the route server/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cead0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cead0-132">-ResourceId</span></span>
<span data-ttu-id="cead0-133">ID della risorsa peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="cead0-133">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="cead0-134">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="cead0-134">-RouteServerName</span></span>
<span data-ttu-id="cead0-135">Server di route in cui è presente il peer.</span><span class="sxs-lookup"><span data-stu-id="cead0-135">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cead0-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cead0-136">-Confirm</span></span>
<span data-ttu-id="cead0-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cead0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cead0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cead0-138">-WhatIf</span></span>
<span data-ttu-id="cead0-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cead0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cead0-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cead0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cead0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cead0-141">CommonParameters</span></span>
<span data-ttu-id="cead0-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cead0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cead0-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cead0-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cead0-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="cead0-144">INPUTS</span></span>

### <span data-ttu-id="cead0-145">System.String</span><span class="sxs-lookup"><span data-stu-id="cead0-145">System.String</span></span>

### <span data-ttu-id="cead0-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="cead0-146">System.UInt32</span></span>

### <span data-ttu-id="cead0-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerDir</span><span class="sxs-lookup"><span data-stu-id="cead0-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="cead0-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cead0-148">OUTPUTS</span></span>

### <span data-ttu-id="cead0-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="cead0-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="cead0-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="cead0-150">NOTES</span></span>

## <span data-ttu-id="cead0-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cead0-151">RELATED LINKS</span></span>
