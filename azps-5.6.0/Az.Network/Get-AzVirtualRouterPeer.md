---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 7b17b124b7d4e0dc89ee7e61469b26401002db9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962749"
---
# <span data-ttu-id="cd184-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="cd184-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="cd184-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd184-102">SYNOPSIS</span></span>
<span data-ttu-id="cd184-103">Ottiene un peer VirtualRouter in un Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cd184-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="cd184-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd184-104">SYNTAX</span></span>

### <span data-ttu-id="cd184-105">VirtualRouterParameterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd184-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd184-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd184-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd184-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd184-107">DESCRIPTION</span></span>
<span data-ttu-id="cd184-108">Il cmdlet **Get-AzVirtualRouterDir Ottiene** un peer in un Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cd184-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="cd184-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd184-109">EXAMPLES</span></span>

### <span data-ttu-id="cd184-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd184-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="cd184-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cd184-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="cd184-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd184-112">PARAMETERS</span></span>

### <span data-ttu-id="cd184-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd184-113">-DefaultProfile</span></span>
<span data-ttu-id="cd184-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd184-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd184-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="cd184-115">-PeerName</span></span>
<span data-ttu-id="cd184-116">Nome del peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="cd184-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="cd184-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd184-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd184-118">Nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="cd184-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="cd184-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd184-119">-ResourceId</span></span>
<span data-ttu-id="cd184-120">ResourceId del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="cd184-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="cd184-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="cd184-121">-VirtualRouterName</span></span>
<span data-ttu-id="cd184-122">Il nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="cd184-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="cd184-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd184-123">CommonParameters</span></span>
<span data-ttu-id="cd184-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd184-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd184-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd184-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd184-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd184-126">INPUTS</span></span>

### <span data-ttu-id="cd184-127">System.String</span><span class="sxs-lookup"><span data-stu-id="cd184-127">System.String</span></span>

## <span data-ttu-id="cd184-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd184-128">OUTPUTS</span></span>

### <span data-ttu-id="cd184-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterConverter</span><span class="sxs-lookup"><span data-stu-id="cd184-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="cd184-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd184-130">NOTES</span></span>

## <span data-ttu-id="cd184-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd184-131">RELATED LINKS</span></span>
