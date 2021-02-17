---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: 259fb6948abee3a00788e68c8d362196e5c12d51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184591"
---
# <span data-ttu-id="1d1fd-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="1d1fd-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="1d1fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="1d1fd-103">Elencare i percorsi annunciati da uno specifico peer di router virtuale</span><span class="sxs-lookup"><span data-stu-id="1d1fd-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="1d1fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d1fd-104">SYNTAX</span></span>

### <span data-ttu-id="1d1fd-105">VirtualRouterParameterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d1fd-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d1fd-106">VirtualRouterParameobjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d1fd-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d1fd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1d1fd-107">DESCRIPTION</span></span>
<span data-ttu-id="1d1fd-108">Dato un peer di router virtuale per nome o per oggetto, enumerare le route annunciate al peer da uno specifico router virtuale.</span><span class="sxs-lookup"><span data-stu-id="1d1fd-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="1d1fd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d1fd-109">EXAMPLES</span></span>

### <span data-ttu-id="1d1fd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d1fd-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="1d1fd-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1d1fd-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="1d1fd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d1fd-112">PARAMETERS</span></span>

### <span data-ttu-id="1d1fd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d1fd-113">-AsJob</span></span>
<span data-ttu-id="1d1fd-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1d1fd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d1fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d1fd-115">-DefaultProfile</span></span>
<span data-ttu-id="1d1fd-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d1fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d1fd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d1fd-117">-InputObject</span></span>
<span data-ttu-id="1d1fd-118">Oggetto di input peer router virtuale.</span><span class="sxs-lookup"><span data-stu-id="1d1fd-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="1d1fd-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="1d1fd-119">-PeerName</span></span>
<span data-ttu-id="1d1fd-120">Nome peer router virtuale</span><span class="sxs-lookup"><span data-stu-id="1d1fd-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="1d1fd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d1fd-121">-ResourceGroupName</span></span>
<span data-ttu-id="1d1fd-122">Nome del gruppo di risorse peer per router virtuale</span><span class="sxs-lookup"><span data-stu-id="1d1fd-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="1d1fd-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="1d1fd-123">-VirtualRouterName</span></span>
<span data-ttu-id="1d1fd-124">Nome router virtuale</span><span class="sxs-lookup"><span data-stu-id="1d1fd-124">Virtual router name</span></span>

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

### <span data-ttu-id="1d1fd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d1fd-125">CommonParameters</span></span>
<span data-ttu-id="1d1fd-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d1fd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d1fd-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d1fd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d1fd-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="1d1fd-128">INPUTS</span></span>

### <span data-ttu-id="1d1fd-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1d1fd-129">System.String</span></span>

### <span data-ttu-id="1d1fd-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterConverter</span><span class="sxs-lookup"><span data-stu-id="1d1fd-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="1d1fd-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d1fd-131">OUTPUTS</span></span>

### <span data-ttu-id="1d1fd-132">Microsoft.Azure.Commands.Network.Models.PSRoute</span><span class="sxs-lookup"><span data-stu-id="1d1fd-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="1d1fd-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="1d1fd-133">NOTES</span></span>

## <span data-ttu-id="1d1fd-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d1fd-134">RELATED LINKS</span></span>
