---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379777"
---
# <span data-ttu-id="fc24a-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="fc24a-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="fc24a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc24a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc24a-103">Percorsi di elenco appresi da un peer di router virtuale specifico</span><span class="sxs-lookup"><span data-stu-id="fc24a-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="fc24a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc24a-104">SYNTAX</span></span>

### <span data-ttu-id="fc24a-105">VirtualRouterPeerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc24a-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc24a-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc24a-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc24a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc24a-107">DESCRIPTION</span></span>
<span data-ttu-id="fc24a-108">Enumerare le route apprese da un peer del router virtuale da altre origini.</span><span class="sxs-lookup"><span data-stu-id="fc24a-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="fc24a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc24a-109">EXAMPLES</span></span>

### <span data-ttu-id="fc24a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc24a-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="fc24a-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fc24a-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="fc24a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc24a-112">PARAMETERS</span></span>

### <span data-ttu-id="fc24a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc24a-113">-AsJob</span></span>
<span data-ttu-id="fc24a-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fc24a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc24a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc24a-115">-DefaultProfile</span></span>
<span data-ttu-id="fc24a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc24a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc24a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc24a-117">-InputObject</span></span>
<span data-ttu-id="fc24a-118">L'oggetto di input peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="fc24a-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="fc24a-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="fc24a-119">-PeerName</span></span>
<span data-ttu-id="fc24a-120">Nome peer del router virtuale</span><span class="sxs-lookup"><span data-stu-id="fc24a-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="fc24a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc24a-121">-ResourceGroupName</span></span>
<span data-ttu-id="fc24a-122">Nome del gruppo risorse peer Virtual router</span><span class="sxs-lookup"><span data-stu-id="fc24a-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="fc24a-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="fc24a-123">-VirtualRouterName</span></span>
<span data-ttu-id="fc24a-124">Nome router virtuale</span><span class="sxs-lookup"><span data-stu-id="fc24a-124">Virtual router name</span></span>

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

### <span data-ttu-id="fc24a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc24a-125">CommonParameters</span></span>
<span data-ttu-id="fc24a-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc24a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc24a-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc24a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc24a-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc24a-128">INPUTS</span></span>

### <span data-ttu-id="fc24a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fc24a-129">System.String</span></span>

### <span data-ttu-id="fc24a-130">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="fc24a-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="fc24a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc24a-131">OUTPUTS</span></span>

### <span data-ttu-id="fc24a-132">Microsoft. Azure. Commands. Network. Models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="fc24a-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="fc24a-133">Note</span><span class="sxs-lookup"><span data-stu-id="fc24a-133">NOTES</span></span>

## <span data-ttu-id="fc24a-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc24a-134">RELATED LINKS</span></span>
