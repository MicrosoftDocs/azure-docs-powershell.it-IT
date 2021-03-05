---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 2c88ac8c0f3f089a4a26bf0e29ec855281e7f8c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005933"
---
# <span data-ttu-id="5979b-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="5979b-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="5979b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5979b-102">SYNOPSIS</span></span>
<span data-ttu-id="5979b-103">Rimuove un peer da un Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5979b-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="5979b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5979b-104">SYNTAX</span></span>

### <span data-ttu-id="5979b-105">VirtualRouterParameterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5979b-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5979b-106">VirtualRouterParameobjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5979b-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5979b-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5979b-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5979b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5979b-108">DESCRIPTION</span></span>
<span data-ttu-id="5979b-109">Il cmdlet **Remove-AzVirtualRouterDir Rimuove** un peer VirtualRouter da un Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5979b-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="5979b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5979b-110">EXAMPLES</span></span>

### <span data-ttu-id="5979b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5979b-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="5979b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5979b-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="5979b-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5979b-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="5979b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5979b-114">PARAMETERS</span></span>

### <span data-ttu-id="5979b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5979b-115">-AsJob</span></span>
<span data-ttu-id="5979b-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5979b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5979b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5979b-117">-DefaultProfile</span></span>
<span data-ttu-id="5979b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5979b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5979b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5979b-119">-Force</span></span>
<span data-ttu-id="5979b-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="5979b-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5979b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5979b-121">-InputObject</span></span>
<span data-ttu-id="5979b-122">Oggetto di input peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="5979b-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="5979b-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="5979b-123">-PeerName</span></span>
<span data-ttu-id="5979b-124">Nome del peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="5979b-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="5979b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5979b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5979b-126">Nome del gruppo di risorse del router/peer virtuale.</span><span class="sxs-lookup"><span data-stu-id="5979b-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="5979b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5979b-127">-ResourceId</span></span>
<span data-ttu-id="5979b-128">ID della risorsa peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="5979b-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="5979b-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="5979b-129">-VirtualRouterName</span></span>
<span data-ttu-id="5979b-130">Router virtuale in cui esiste il peer.</span><span class="sxs-lookup"><span data-stu-id="5979b-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="5979b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5979b-131">-Confirm</span></span>
<span data-ttu-id="5979b-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5979b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5979b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5979b-133">-WhatIf</span></span>
<span data-ttu-id="5979b-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5979b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5979b-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5979b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5979b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5979b-136">CommonParameters</span></span>
<span data-ttu-id="5979b-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5979b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5979b-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5979b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5979b-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="5979b-139">INPUTS</span></span>

### <span data-ttu-id="5979b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5979b-140">System.String</span></span>

### <span data-ttu-id="5979b-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter Enterprise</span><span class="sxs-lookup"><span data-stu-id="5979b-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="5979b-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5979b-142">OUTPUTS</span></span>

### <span data-ttu-id="5979b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5979b-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="5979b-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="5979b-144">NOTES</span></span>

## <span data-ttu-id="5979b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5979b-145">RELATED LINKS</span></span>
