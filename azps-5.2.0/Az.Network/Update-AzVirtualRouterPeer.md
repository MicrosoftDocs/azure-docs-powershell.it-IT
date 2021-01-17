---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 242a3985d75e0a741c5e2175c098139b448f3e70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350740"
---
# <span data-ttu-id="238be-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="238be-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="238be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="238be-102">SYNOPSIS</span></span>
<span data-ttu-id="238be-103">Aggiornare un peer in un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="238be-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="238be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="238be-104">SYNTAX</span></span>

### <span data-ttu-id="238be-105">VirtualRouterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="238be-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="238be-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="238be-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="238be-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="238be-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="238be-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="238be-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="238be-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="238be-109">DESCRIPTION</span></span>
<span data-ttu-id="238be-110">Il cmdlet **Update-AzVirtualRouterPeer** aggiorna un peer VirtualRouter a un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="238be-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="238be-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="238be-111">EXAMPLES</span></span>

### <span data-ttu-id="238be-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="238be-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="238be-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="238be-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="238be-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="238be-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="238be-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="238be-115">PARAMETERS</span></span>

### <span data-ttu-id="238be-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="238be-116">-AsJob</span></span>
<span data-ttu-id="238be-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="238be-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="238be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="238be-118">-DefaultProfile</span></span>
<span data-ttu-id="238be-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="238be-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="238be-120">-Force</span><span class="sxs-lookup"><span data-stu-id="238be-120">-Force</span></span>
<span data-ttu-id="238be-121">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="238be-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="238be-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="238be-122">-InputObject</span></span>
<span data-ttu-id="238be-123">L'oggetto di input peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="238be-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="238be-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="238be-124">-PeerAsn</span></span>
<span data-ttu-id="238be-125">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="238be-125">Peer ASN.</span></span>

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

### <span data-ttu-id="238be-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="238be-126">-PeerIp</span></span>
<span data-ttu-id="238be-127">IP peer.</span><span class="sxs-lookup"><span data-stu-id="238be-127">Peer Ip.</span></span>

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

### <span data-ttu-id="238be-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="238be-128">-PeerName</span></span>
<span data-ttu-id="238be-129">Nome del peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="238be-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="238be-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="238be-130">-ResourceGroupName</span></span>
<span data-ttu-id="238be-131">Nome del gruppo di risorse del router virtuale/peer.</span><span class="sxs-lookup"><span data-stu-id="238be-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="238be-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="238be-132">-ResourceId</span></span>
<span data-ttu-id="238be-133">ID risorsa peer Virtual router.</span><span class="sxs-lookup"><span data-stu-id="238be-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="238be-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="238be-134">-VirtualRouterName</span></span>
<span data-ttu-id="238be-135">Il router virtuale in cui esiste peer.</span><span class="sxs-lookup"><span data-stu-id="238be-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="238be-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="238be-136">-Confirm</span></span>
<span data-ttu-id="238be-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="238be-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="238be-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="238be-138">-WhatIf</span></span>
<span data-ttu-id="238be-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="238be-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="238be-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="238be-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="238be-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="238be-141">CommonParameters</span></span>
<span data-ttu-id="238be-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="238be-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="238be-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="238be-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="238be-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="238be-144">INPUTS</span></span>

### <span data-ttu-id="238be-145">System. String</span><span class="sxs-lookup"><span data-stu-id="238be-145">System.String</span></span>

### <span data-ttu-id="238be-146">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="238be-146">System.UInt32</span></span>

### <span data-ttu-id="238be-147">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="238be-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="238be-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="238be-148">OUTPUTS</span></span>

### <span data-ttu-id="238be-149">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="238be-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="238be-150">Note</span><span class="sxs-lookup"><span data-stu-id="238be-150">NOTES</span></span>

## <span data-ttu-id="238be-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="238be-151">RELATED LINKS</span></span>
