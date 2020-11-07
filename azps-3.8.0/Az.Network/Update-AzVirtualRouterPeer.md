---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 8d7bbf361ee2fc2bf06e1bf3ce6a9bfe1e295338
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865411"
---
# <span data-ttu-id="621e6-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="621e6-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="621e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="621e6-102">SYNOPSIS</span></span>
<span data-ttu-id="621e6-103">Aggiornare un peer in un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="621e6-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="621e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="621e6-104">SYNTAX</span></span>

### <span data-ttu-id="621e6-105">VirtualRouterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="621e6-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="621e6-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="621e6-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="621e6-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="621e6-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="621e6-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="621e6-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="621e6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="621e6-109">DESCRIPTION</span></span>
<span data-ttu-id="621e6-110">Il cmdlet **Update-AzVirtualRouterPeer** aggiorna un peer VirtualRouter a un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="621e6-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="621e6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="621e6-111">EXAMPLES</span></span>

### <span data-ttu-id="621e6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="621e6-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="621e6-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="621e6-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="621e6-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="621e6-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="621e6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="621e6-115">PARAMETERS</span></span>

### <span data-ttu-id="621e6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="621e6-116">-AsJob</span></span>
<span data-ttu-id="621e6-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="621e6-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="621e6-118">-DefaultProfile</span></span>
<span data-ttu-id="621e6-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="621e6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="621e6-120">-Force</span></span>
<span data-ttu-id="621e6-121">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="621e6-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="621e6-122">-InputObject</span></span>
<span data-ttu-id="621e6-123">L'oggetto di input peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="621e6-123">The virtual router peer input object.</span></span>

```yaml
Type: PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="621e6-124">-PeerAsn</span></span>
<span data-ttu-id="621e6-125">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="621e6-125">Peer ASN.</span></span>

```yaml
Type: UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="621e6-126">-PeerIp</span></span>
<span data-ttu-id="621e6-127">IP peer.</span><span class="sxs-lookup"><span data-stu-id="621e6-127">Peer Ip.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="621e6-128">-PeerName</span></span>
<span data-ttu-id="621e6-129">Nome del peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="621e6-129">The name of the virtual router Peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="621e6-130">-ResourceGroupName</span></span>
<span data-ttu-id="621e6-131">Nome del gruppo di risorse del router virtuale/peer.</span><span class="sxs-lookup"><span data-stu-id="621e6-131">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="621e6-132">-ResourceId</span></span>
<span data-ttu-id="621e6-133">ID risorsa peer Virtual router.</span><span class="sxs-lookup"><span data-stu-id="621e6-133">The virtual router peer resource Id.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="621e6-134">-VirtualRouterName</span></span>
<span data-ttu-id="621e6-135">Il router virtuale in cui esiste peer.</span><span class="sxs-lookup"><span data-stu-id="621e6-135">The virtual router where peer exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="621e6-136">-Confirm</span></span>
<span data-ttu-id="621e6-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="621e6-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="621e6-138">-WhatIf</span></span>
<span data-ttu-id="621e6-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="621e6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="621e6-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="621e6-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621e6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="621e6-141">CommonParameters</span></span>
<span data-ttu-id="621e6-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="621e6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="621e6-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="621e6-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="621e6-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="621e6-144">INPUTS</span></span>

### <span data-ttu-id="621e6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="621e6-145">System.String</span></span>

### <span data-ttu-id="621e6-146">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="621e6-146">System.UInt32</span></span>

### <span data-ttu-id="621e6-147">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="621e6-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="621e6-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="621e6-148">OUTPUTS</span></span>

### <span data-ttu-id="621e6-149">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="621e6-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="621e6-150">Note</span><span class="sxs-lookup"><span data-stu-id="621e6-150">NOTES</span></span>

## <span data-ttu-id="621e6-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="621e6-151">RELATED LINKS</span></span>
