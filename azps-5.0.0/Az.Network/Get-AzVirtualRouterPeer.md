---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200365"
---
# <span data-ttu-id="7a670-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="7a670-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="7a670-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a670-102">SYNOPSIS</span></span>
<span data-ttu-id="7a670-103">Ottiene un peer VirtualRouter in un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="7a670-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="7a670-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a670-104">SYNTAX</span></span>

### <span data-ttu-id="7a670-105">VirtualRouterPeerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a670-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a670-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a670-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a670-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a670-107">DESCRIPTION</span></span>
<span data-ttu-id="7a670-108">Il cmdlet **Get-AzVirtualRouterPeer** ottiene un peer in un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="7a670-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="7a670-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a670-109">EXAMPLES</span></span>

### <span data-ttu-id="7a670-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7a670-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="7a670-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7a670-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="7a670-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a670-112">PARAMETERS</span></span>

### <span data-ttu-id="7a670-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a670-113">-DefaultProfile</span></span>
<span data-ttu-id="7a670-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a670-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a670-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="7a670-115">-PeerName</span></span>
<span data-ttu-id="7a670-116">Nome del peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="7a670-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="7a670-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a670-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a670-118">Il nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="7a670-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="7a670-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a670-119">-ResourceId</span></span>
<span data-ttu-id="7a670-120">ResourceId del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="7a670-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="7a670-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="7a670-121">-VirtualRouterName</span></span>
<span data-ttu-id="7a670-122">Nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="7a670-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="7a670-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a670-123">CommonParameters</span></span>
<span data-ttu-id="7a670-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a670-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a670-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a670-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a670-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a670-126">INPUTS</span></span>

### <span data-ttu-id="7a670-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7a670-127">System.String</span></span>

## <span data-ttu-id="7a670-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a670-128">OUTPUTS</span></span>

### <span data-ttu-id="7a670-129">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="7a670-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="7a670-130">Note</span><span class="sxs-lookup"><span data-stu-id="7a670-130">NOTES</span></span>

## <span data-ttu-id="7a670-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a670-131">RELATED LINKS</span></span>
