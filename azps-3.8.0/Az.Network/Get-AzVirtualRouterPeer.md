---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: cf662dcd74182776131a5b7cfe3df3d86d20c14b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019320"
---
# <span data-ttu-id="7a212-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="7a212-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="7a212-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a212-102">SYNOPSIS</span></span>
<span data-ttu-id="7a212-103">Ottiene un peer VirtualRouter in un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="7a212-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>


## <span data-ttu-id="7a212-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a212-104">SYNTAX</span></span>

### <span data-ttu-id="7a212-105">VirtualRouterPeerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7a212-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a212-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a212-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a212-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a212-107">DESCRIPTION</span></span>
<span data-ttu-id="7a212-108">Il cmdlet **Get-AzVirtualRouterPeer** ottiene un peer in un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="7a212-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="7a212-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a212-109">EXAMPLES</span></span>

### <span data-ttu-id="7a212-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7a212-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -RouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="7a212-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7a212-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="7a212-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a212-112">PARAMETERS</span></span>

### <span data-ttu-id="7a212-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a212-113">-DefaultProfile</span></span>
<span data-ttu-id="7a212-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7a212-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a212-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="7a212-115">-PeerName</span></span>
<span data-ttu-id="7a212-116">Nome del peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="7a212-116">The name of the virtual router peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a212-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a212-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a212-118">Il nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="7a212-118">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a212-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a212-119">-ResourceId</span></span>
<span data-ttu-id="7a212-120">ResourceId del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="7a212-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="7a212-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="7a212-121">-VirtualRouterName</span></span>
<span data-ttu-id="7a212-122">Nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="7a212-122">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a212-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a212-123">CommonParameters</span></span>
<span data-ttu-id="7a212-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a212-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a212-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a212-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a212-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a212-126">INPUTS</span></span>

### <span data-ttu-id="7a212-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7a212-127">System.String</span></span>

## <span data-ttu-id="7a212-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a212-128">OUTPUTS</span></span>

### <span data-ttu-id="7a212-129">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="7a212-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="7a212-130">Note</span><span class="sxs-lookup"><span data-stu-id="7a212-130">NOTES</span></span>

## <span data-ttu-id="7a212-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a212-131">RELATED LINKS</span></span>
