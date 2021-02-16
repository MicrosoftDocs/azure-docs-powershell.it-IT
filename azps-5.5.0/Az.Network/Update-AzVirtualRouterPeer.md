---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 242a3985d75e0a741c5e2175c098139b448f3e70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184126"
---
# <span data-ttu-id="7256c-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="7256c-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="7256c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7256c-102">SYNOPSIS</span></span>
<span data-ttu-id="7256c-103">Aggiornare un peer in un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="7256c-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="7256c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7256c-104">SYNTAX</span></span>

### <span data-ttu-id="7256c-105">VirtualRouterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7256c-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7256c-106">VirtualRouterParameterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7256c-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7256c-107">VirtualRouterParameobjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7256c-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7256c-108">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7256c-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7256c-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7256c-109">DESCRIPTION</span></span>
<span data-ttu-id="7256c-110">Il cmdlet **Update-AzVirtualRouter Commutr Consente** di aggiornare un peer VirtualRouter a un peer Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="7256c-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="7256c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7256c-111">EXAMPLES</span></span>

### <span data-ttu-id="7256c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7256c-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="7256c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7256c-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="7256c-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7256c-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="7256c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7256c-115">PARAMETERS</span></span>

### <span data-ttu-id="7256c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7256c-116">-AsJob</span></span>
<span data-ttu-id="7256c-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7256c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7256c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7256c-118">-DefaultProfile</span></span>
<span data-ttu-id="7256c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7256c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7256c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7256c-120">-Force</span></span>
<span data-ttu-id="7256c-121">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="7256c-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7256c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7256c-122">-InputObject</span></span>
<span data-ttu-id="7256c-123">Oggetto di input peer router virtuale.</span><span class="sxs-lookup"><span data-stu-id="7256c-123">The virtual router peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7256c-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="7256c-124">-PeerAsn</span></span>
<span data-ttu-id="7256c-125">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="7256c-125">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7256c-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="7256c-126">-PeerIp</span></span>
<span data-ttu-id="7256c-127">Ip peer.</span><span class="sxs-lookup"><span data-stu-id="7256c-127">Peer Ip.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7256c-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="7256c-128">-PeerName</span></span>
<span data-ttu-id="7256c-129">Nome del peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="7256c-129">The name of the virtual router Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7256c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7256c-130">-ResourceGroupName</span></span>
<span data-ttu-id="7256c-131">Nome del gruppo di risorse del router/peer virtuale.</span><span class="sxs-lookup"><span data-stu-id="7256c-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="7256c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7256c-132">-ResourceId</span></span>
<span data-ttu-id="7256c-133">ID della risorsa peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="7256c-133">The virtual router peer resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7256c-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="7256c-134">-VirtualRouterName</span></span>
<span data-ttu-id="7256c-135">Router virtuale in cui esiste il peer.</span><span class="sxs-lookup"><span data-stu-id="7256c-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="7256c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7256c-136">-Confirm</span></span>
<span data-ttu-id="7256c-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7256c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7256c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7256c-138">-WhatIf</span></span>
<span data-ttu-id="7256c-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7256c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7256c-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7256c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7256c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7256c-141">CommonParameters</span></span>
<span data-ttu-id="7256c-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7256c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7256c-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7256c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7256c-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="7256c-144">INPUTS</span></span>

### <span data-ttu-id="7256c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7256c-145">System.String</span></span>

### <span data-ttu-id="7256c-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="7256c-146">System.UInt32</span></span>

### <span data-ttu-id="7256c-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterConverter</span><span class="sxs-lookup"><span data-stu-id="7256c-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="7256c-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7256c-148">OUTPUTS</span></span>

### <span data-ttu-id="7256c-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="7256c-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="7256c-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="7256c-150">NOTES</span></span>

## <span data-ttu-id="7256c-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7256c-151">RELATED LINKS</span></span>
