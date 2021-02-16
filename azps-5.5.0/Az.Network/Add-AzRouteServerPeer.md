---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 70f7573a604ea15c33f1949883503fed2a356e00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192015"
---
# <span data-ttu-id="097fe-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="097fe-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="097fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="097fe-102">SYNOPSIS</span></span>
<span data-ttu-id="097fe-103">Aggiungere un peer a un RouteServer di Azure</span><span class="sxs-lookup"><span data-stu-id="097fe-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="097fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="097fe-104">SYNTAX</span></span>

### <span data-ttu-id="097fe-105">RouteServerNParameterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="097fe-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="097fe-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="097fe-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="097fe-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="097fe-107">DESCRIPTION</span></span>
<span data-ttu-id="097fe-108">Il cmdlet **Add-AzRouteServerRoute aggiunge** un peer RouteServer a un Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="097fe-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="097fe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="097fe-109">EXAMPLES</span></span>

### <span data-ttu-id="097fe-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="097fe-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="097fe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="097fe-111">PARAMETERS</span></span>

### <span data-ttu-id="097fe-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="097fe-112">-AsJob</span></span>
<span data-ttu-id="097fe-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="097fe-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="097fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="097fe-114">-DefaultProfile</span></span>
<span data-ttu-id="097fe-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="097fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="097fe-116">-Force</span><span class="sxs-lookup"><span data-stu-id="097fe-116">-Force</span></span>
<span data-ttu-id="097fe-117">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="097fe-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="097fe-118">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="097fe-118">-PeerAsn</span></span>
<span data-ttu-id="097fe-119">ASN del peer del server route remoto.</span><span class="sxs-lookup"><span data-stu-id="097fe-119">ASN of remote route server peer.</span></span>

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

### <span data-ttu-id="097fe-120">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="097fe-120">-PeerIp</span></span>
<span data-ttu-id="097fe-121">Ip del peer del server route remoto.</span><span class="sxs-lookup"><span data-stu-id="097fe-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="097fe-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="097fe-122">-PeerName</span></span>
<span data-ttu-id="097fe-123">Nome del peer del server di route.</span><span class="sxs-lookup"><span data-stu-id="097fe-123">The name of the route server peer.</span></span>

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

### <span data-ttu-id="097fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="097fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="097fe-125">Nome del gruppo di risorse del server/peer della route.</span><span class="sxs-lookup"><span data-stu-id="097fe-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="097fe-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="097fe-126">-RouteServerName</span></span>
<span data-ttu-id="097fe-127">Server di route in cui è presente il peer.</span><span class="sxs-lookup"><span data-stu-id="097fe-127">The route server where peer exists.</span></span>

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

### <span data-ttu-id="097fe-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="097fe-128">-Confirm</span></span>
<span data-ttu-id="097fe-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="097fe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="097fe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="097fe-130">-WhatIf</span></span>
<span data-ttu-id="097fe-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="097fe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="097fe-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="097fe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="097fe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097fe-133">CommonParameters</span></span>
<span data-ttu-id="097fe-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="097fe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097fe-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="097fe-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097fe-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="097fe-136">INPUTS</span></span>

### <span data-ttu-id="097fe-137">System.String</span><span class="sxs-lookup"><span data-stu-id="097fe-137">System.String</span></span>

### <span data-ttu-id="097fe-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="097fe-138">System.UInt32</span></span>

## <span data-ttu-id="097fe-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="097fe-139">OUTPUTS</span></span>

### <span data-ttu-id="097fe-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="097fe-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="097fe-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="097fe-141">NOTES</span></span>

## <span data-ttu-id="097fe-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="097fe-142">RELATED LINKS</span></span>
