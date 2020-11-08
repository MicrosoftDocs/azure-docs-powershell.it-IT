---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199535"
---
# <span data-ttu-id="ac160-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="ac160-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="ac160-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac160-102">SYNOPSIS</span></span>
<span data-ttu-id="ac160-103">Rimuove un peer da un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="ac160-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="ac160-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac160-104">SYNTAX</span></span>

### <span data-ttu-id="ac160-105">VirtualRouterPeerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac160-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac160-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac160-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac160-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac160-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac160-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac160-108">DESCRIPTION</span></span>
<span data-ttu-id="ac160-109">Il cmdlet **Remove-AzVirtualRouterPeer** rimuove un peer VirtualRouter da un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="ac160-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="ac160-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac160-110">EXAMPLES</span></span>

### <span data-ttu-id="ac160-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac160-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="ac160-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ac160-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="ac160-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ac160-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="ac160-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac160-114">PARAMETERS</span></span>

### <span data-ttu-id="ac160-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac160-115">-AsJob</span></span>
<span data-ttu-id="ac160-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ac160-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac160-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac160-117">-DefaultProfile</span></span>
<span data-ttu-id="ac160-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac160-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac160-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ac160-119">-Force</span></span>
<span data-ttu-id="ac160-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="ac160-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ac160-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac160-121">-InputObject</span></span>
<span data-ttu-id="ac160-122">L'oggetto di input peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac160-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="ac160-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="ac160-123">-PeerName</span></span>
<span data-ttu-id="ac160-124">Nome del peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac160-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="ac160-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac160-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac160-126">Nome del gruppo di risorse del router virtuale/peer.</span><span class="sxs-lookup"><span data-stu-id="ac160-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="ac160-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac160-127">-ResourceId</span></span>
<span data-ttu-id="ac160-128">ID risorsa peer Virtual router.</span><span class="sxs-lookup"><span data-stu-id="ac160-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="ac160-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="ac160-129">-VirtualRouterName</span></span>
<span data-ttu-id="ac160-130">Il router virtuale in cui esiste peer.</span><span class="sxs-lookup"><span data-stu-id="ac160-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="ac160-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ac160-131">-Confirm</span></span>
<span data-ttu-id="ac160-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac160-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac160-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac160-133">-WhatIf</span></span>
<span data-ttu-id="ac160-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac160-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac160-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac160-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac160-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac160-136">CommonParameters</span></span>
<span data-ttu-id="ac160-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac160-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac160-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac160-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac160-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac160-139">INPUTS</span></span>

### <span data-ttu-id="ac160-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ac160-140">System.String</span></span>

### <span data-ttu-id="ac160-141">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="ac160-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="ac160-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac160-142">OUTPUTS</span></span>

### <span data-ttu-id="ac160-143">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="ac160-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="ac160-144">Note</span><span class="sxs-lookup"><span data-stu-id="ac160-144">NOTES</span></span>

## <span data-ttu-id="ac160-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac160-145">RELATED LINKS</span></span>