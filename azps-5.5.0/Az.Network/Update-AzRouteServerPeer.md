---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
ms.openlocfilehash: 79d907a5ac1b75bdc65d6ea79ffc6c9dea911479
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193302"
---
# <span data-ttu-id="5ef62-101">Update-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="5ef62-101">Update-AzRouteServerPeer</span></span>

## <span data-ttu-id="5ef62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ef62-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef62-103">Aggiornare un peer in un RouteServer di Azure</span><span class="sxs-lookup"><span data-stu-id="5ef62-103">Update a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="5ef62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ef62-104">SYNTAX</span></span>

### <span data-ttu-id="5ef62-105">RouteServerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ef62-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ef62-106">RouteServerNParamenameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ef62-106">RouteServerNPeerNameParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ef62-107">RouteServerNParameeObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ef62-107">RouteServerNPeerInputObjectParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -InputObject <PSRouteServerPeer>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ef62-108">RouteServerNResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ef62-108">RouteServerNPeerResourceIdParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -ResourceId <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ef62-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5ef62-109">DESCRIPTION</span></span>
<span data-ttu-id="5ef62-110">Il cmdlet **Update-AzRouteServer Firmware** aggiorna un peer RouteServer a un Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="5ef62-110">The **Update-AzRouteServerPeer** cmdlet updates a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="5ef62-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ef62-111">EXAMPLES</span></span>

### <span data-ttu-id="5ef62-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ef62-112">Example 1</span></span>
```powershell
PS C:\> Update-AzRouteServerPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="5ef62-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5ef62-113">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/csr'
Update-AzRouteServerPeer -ResourceId $routeServerPeerId  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="5ef62-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5ef62-114">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServer -RouteServerName routeServer -PeerName csr
Update-AzRouteServerPeer -ResourceGroupName routeServerRG -InputObject $routeServerPeer  -RouteServerName routeServer
```

## <span data-ttu-id="5ef62-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ef62-115">PARAMETERS</span></span>

### <span data-ttu-id="5ef62-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ef62-116">-AsJob</span></span>
<span data-ttu-id="5ef62-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5ef62-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ef62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef62-118">-DefaultProfile</span></span>
<span data-ttu-id="5ef62-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ef62-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ef62-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5ef62-120">-Force</span></span>
<span data-ttu-id="5ef62-121">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="5ef62-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5ef62-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ef62-122">-InputObject</span></span>
<span data-ttu-id="5ef62-123">Oggetto di input peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="5ef62-123">The route server peer input object.</span></span>

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

### <span data-ttu-id="5ef62-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="5ef62-124">-PeerAsn</span></span>
<span data-ttu-id="5ef62-125">ASN del peer del server route remoto.</span><span class="sxs-lookup"><span data-stu-id="5ef62-125">ASN of remote route server peer.</span></span>

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

### <span data-ttu-id="5ef62-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="5ef62-126">-PeerIp</span></span>
<span data-ttu-id="5ef62-127">Ip del peer del server route remoto.</span><span class="sxs-lookup"><span data-stu-id="5ef62-127">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="5ef62-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="5ef62-128">-PeerName</span></span>
<span data-ttu-id="5ef62-129">Nome del peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="5ef62-129">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="5ef62-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef62-130">-ResourceGroupName</span></span>
<span data-ttu-id="5ef62-131">Nome del gruppo di risorse del server/peer della route.</span><span class="sxs-lookup"><span data-stu-id="5ef62-131">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="5ef62-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ef62-132">-ResourceId</span></span>
<span data-ttu-id="5ef62-133">ID della risorsa peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="5ef62-133">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="5ef62-134">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="5ef62-134">-RouteServerName</span></span>
<span data-ttu-id="5ef62-135">Server di route in cui è presente il peer.</span><span class="sxs-lookup"><span data-stu-id="5ef62-135">The route server where peer exists.</span></span>

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

### <span data-ttu-id="5ef62-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ef62-136">-Confirm</span></span>
<span data-ttu-id="5ef62-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ef62-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ef62-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef62-138">-WhatIf</span></span>
<span data-ttu-id="5ef62-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ef62-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef62-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ef62-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ef62-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef62-141">CommonParameters</span></span>
<span data-ttu-id="5ef62-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ef62-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef62-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5ef62-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef62-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="5ef62-144">INPUTS</span></span>

### <span data-ttu-id="5ef62-145">System.String</span><span class="sxs-lookup"><span data-stu-id="5ef62-145">System.String</span></span>

### <span data-ttu-id="5ef62-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="5ef62-146">System.UInt32</span></span>

### <span data-ttu-id="5ef62-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerDir</span><span class="sxs-lookup"><span data-stu-id="5ef62-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="5ef62-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ef62-148">OUTPUTS</span></span>

### <span data-ttu-id="5ef62-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="5ef62-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="5ef62-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="5ef62-150">NOTES</span></span>

## <span data-ttu-id="5ef62-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ef62-151">RELATED LINKS</span></span>
