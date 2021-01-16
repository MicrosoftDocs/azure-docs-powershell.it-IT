---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379791"
---
# <span data-ttu-id="f3e90-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="f3e90-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="f3e90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3e90-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e90-103">Ottiene un peer VirtualRouter in un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="f3e90-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="f3e90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3e90-104">SYNTAX</span></span>

### <span data-ttu-id="f3e90-105">VirtualRouterPeerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3e90-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3e90-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3e90-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3e90-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3e90-107">DESCRIPTION</span></span>
<span data-ttu-id="f3e90-108">Il cmdlet **Get-AzVirtualRouterPeer** ottiene un peer in un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="f3e90-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="f3e90-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3e90-109">EXAMPLES</span></span>

### <span data-ttu-id="f3e90-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f3e90-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="f3e90-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f3e90-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="f3e90-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3e90-112">PARAMETERS</span></span>

### <span data-ttu-id="f3e90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e90-113">-DefaultProfile</span></span>
<span data-ttu-id="f3e90-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3e90-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3e90-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="f3e90-115">-PeerName</span></span>
<span data-ttu-id="f3e90-116">Nome del peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="f3e90-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="f3e90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e90-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3e90-118">Il nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="f3e90-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="f3e90-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3e90-119">-ResourceId</span></span>
<span data-ttu-id="f3e90-120">ResourceId del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="f3e90-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="f3e90-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="f3e90-121">-VirtualRouterName</span></span>
<span data-ttu-id="f3e90-122">Nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="f3e90-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="f3e90-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e90-123">CommonParameters</span></span>
<span data-ttu-id="f3e90-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3e90-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e90-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3e90-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e90-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3e90-126">INPUTS</span></span>

### <span data-ttu-id="f3e90-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f3e90-127">System.String</span></span>

## <span data-ttu-id="f3e90-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3e90-128">OUTPUTS</span></span>

### <span data-ttu-id="f3e90-129">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="f3e90-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="f3e90-130">Note</span><span class="sxs-lookup"><span data-stu-id="f3e90-130">NOTES</span></span>

## <span data-ttu-id="f3e90-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3e90-131">RELATED LINKS</span></span>
