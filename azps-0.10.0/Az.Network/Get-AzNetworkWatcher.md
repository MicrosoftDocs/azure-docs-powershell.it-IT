---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: d312eaa9f75fc13ecba0b00aa0fea64b5d3ea2e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860746"
---
# <span data-ttu-id="11f30-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11f30-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="11f30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11f30-102">SYNOPSIS</span></span>
<span data-ttu-id="11f30-103">Ottiene le proprietà di un Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="11f30-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="11f30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11f30-104">SYNTAX</span></span>

### <span data-ttu-id="11f30-105">Ottieni</span><span class="sxs-lookup"><span data-stu-id="11f30-105">Get</span></span>
```
Get-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11f30-106">Elenco</span><span class="sxs-lookup"><span data-stu-id="11f30-106">List</span></span>
```
Get-AzNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11f30-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11f30-107">DESCRIPTION</span></span>
<span data-ttu-id="11f30-108">Il cmdlet Get-AzNetworkWatcher ottiene una o più risorse di monitoraggio di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="11f30-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="11f30-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11f30-109">EXAMPLES</span></span>

### <span data-ttu-id="11f30-110">--------------------------Esempio 1: ottenere un Watcher di rete--------------------------</span><span class="sxs-lookup"><span data-stu-id="11f30-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="11f30-111">Ottiene il monitoraggio della rete denominato NetworkWatcher_westcentralus nel gruppo di risorse NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="11f30-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="11f30-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11f30-112">PARAMETERS</span></span>

### <span data-ttu-id="11f30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f30-113">-DefaultProfile</span></span>
<span data-ttu-id="11f30-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11f30-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f30-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="11f30-115">-Name</span></span>
<span data-ttu-id="11f30-116">Nome del Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="11f30-116">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f30-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11f30-117">-ResourceGroupName</span></span>
<span data-ttu-id="11f30-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11f30-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f30-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f30-119">CommonParameters</span></span>
<span data-ttu-id="11f30-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11f30-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f30-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f30-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f30-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11f30-122">INPUTS</span></span>

### <span data-ttu-id="11f30-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="11f30-123">None</span></span>

## <span data-ttu-id="11f30-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11f30-124">OUTPUTS</span></span>

### <span data-ttu-id="11f30-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11f30-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="11f30-126">Note</span><span class="sxs-lookup"><span data-stu-id="11f30-126">NOTES</span></span>
<span data-ttu-id="11f30-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="11f30-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="11f30-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11f30-128">RELATED LINKS</span></span>

[<span data-ttu-id="11f30-129">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11f30-129">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="11f30-130">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="11f30-130">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="11f30-131">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="11f30-131">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="11f30-132">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="11f30-132">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="11f30-133">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="11f30-133">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="11f30-134">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="11f30-134">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="11f30-135">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="11f30-135">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="11f30-136">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="11f30-136">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="11f30-137">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="11f30-137">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="11f30-138">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="11f30-138">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="11f30-139">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="11f30-139">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="11f30-140">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="11f30-140">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
