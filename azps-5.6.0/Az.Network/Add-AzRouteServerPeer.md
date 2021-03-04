---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 430292ba3a387a0b2a0285b26c147c375f114398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979774"
---
# <span data-ttu-id="fdfc5-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="fdfc5-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="fdfc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdfc5-102">SYNOPSIS</span></span>
<span data-ttu-id="fdfc5-103">Aggiungere un peer a un RouteServer di Azure</span><span class="sxs-lookup"><span data-stu-id="fdfc5-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="fdfc5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdfc5-104">SYNTAX</span></span>

### <span data-ttu-id="fdfc5-105">RouteServerNParameterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fdfc5-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfc5-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdfc5-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fdfc5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fdfc5-107">DESCRIPTION</span></span>
<span data-ttu-id="fdfc5-108">Il cmdlet **Add-AzRouteServerRoute aggiunge** un peer RouteServer a un Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="fdfc5-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="fdfc5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdfc5-109">EXAMPLES</span></span>

### <span data-ttu-id="fdfc5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fdfc5-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="fdfc5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdfc5-111">PARAMETERS</span></span>

### <span data-ttu-id="fdfc5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdfc5-112">-AsJob</span></span>
<span data-ttu-id="fdfc5-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fdfc5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdfc5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdfc5-114">-DefaultProfile</span></span>
<span data-ttu-id="fdfc5-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdfc5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdfc5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fdfc5-116">-Force</span></span>
<span data-ttu-id="fdfc5-117">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="fdfc5-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fdfc5-118">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="fdfc5-118">-PeerAsn</span></span>
<span data-ttu-id="fdfc5-119">ASN del peer del server del percorso remoto.</span><span class="sxs-lookup"><span data-stu-id="fdfc5-119">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdfc5-120">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="fdfc5-120">-PeerIp</span></span>
<span data-ttu-id="fdfc5-121">Ip del peer del server route remoto.</span><span class="sxs-lookup"><span data-stu-id="fdfc5-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="fdfc5-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="fdfc5-122">-PeerName</span></span>
<span data-ttu-id="fdfc5-123">Nome del peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="fdfc5-123">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdfc5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdfc5-124">-ResourceGroupName</span></span>
<span data-ttu-id="fdfc5-125">Nome del gruppo di risorse del server/peer della route.</span><span class="sxs-lookup"><span data-stu-id="fdfc5-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="fdfc5-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="fdfc5-126">-RouteServerName</span></span>
<span data-ttu-id="fdfc5-127">Server di route in cui è presente il peer.</span><span class="sxs-lookup"><span data-stu-id="fdfc5-127">The route server where peer exists.</span></span>

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

### <span data-ttu-id="fdfc5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdfc5-128">-Confirm</span></span>
<span data-ttu-id="fdfc5-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdfc5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdfc5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdfc5-130">-WhatIf</span></span>
<span data-ttu-id="fdfc5-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdfc5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdfc5-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdfc5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdfc5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdfc5-133">CommonParameters</span></span>
<span data-ttu-id="fdfc5-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdfc5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdfc5-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fdfc5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdfc5-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="fdfc5-136">INPUTS</span></span>

### <span data-ttu-id="fdfc5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fdfc5-137">System.String</span></span>

### <span data-ttu-id="fdfc5-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="fdfc5-138">System.UInt32</span></span>

## <span data-ttu-id="fdfc5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdfc5-139">OUTPUTS</span></span>

### <span data-ttu-id="fdfc5-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="fdfc5-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="fdfc5-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="fdfc5-141">NOTES</span></span>

## <span data-ttu-id="fdfc5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdfc5-142">RELATED LINKS</span></span>
