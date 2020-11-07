---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 97227c27e23c6283fd64e1660262bbec175cf0a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867034"
---
# <span data-ttu-id="d8b7c-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d8b7c-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="d8b7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b7c-103">Ottiene le proprietà di un Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="d8b7c-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8b7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8b7c-104">SYNTAX</span></span>

### <span data-ttu-id="d8b7c-105">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d8b7c-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8b7c-106">Elenco</span><span class="sxs-lookup"><span data-stu-id="d8b7c-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8b7c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8b7c-107">DESCRIPTION</span></span>
<span data-ttu-id="d8b7c-108">Il cmdlet Get-AzureRmNetworkWatcher ottiene una o più risorse di monitoraggio di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="d8b7c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8b7c-109">EXAMPLES</span></span>

### <span data-ttu-id="d8b7c-110">--------------------------Esempio 1: ottenere un Watcher di rete--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8b7c-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="d8b7c-111">Ottiene il monitoraggio della rete denominato NetworkWatcher_westcentralus nel gruppo di risorse NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="d8b7c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8b7c-112">PARAMETERS</span></span>

### <span data-ttu-id="d8b7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b7c-113">-DefaultProfile</span></span>
<span data-ttu-id="d8b7c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8b7c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8b7c-115">-Name</span></span>
<span data-ttu-id="d8b7c-116">Nome del Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-116">The network watcher name.</span></span>

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

### <span data-ttu-id="d8b7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8b7c-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-118">The resource group name.</span></span>

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

### <span data-ttu-id="d8b7c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b7c-119">CommonParameters</span></span>
<span data-ttu-id="d8b7c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b7c-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b7c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b7c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8b7c-122">INPUTS</span></span>

### <span data-ttu-id="d8b7c-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d8b7c-123">None</span></span>

## <span data-ttu-id="d8b7c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8b7c-124">OUTPUTS</span></span>

### <span data-ttu-id="d8b7c-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d8b7c-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="d8b7c-126">Note</span><span class="sxs-lookup"><span data-stu-id="d8b7c-126">NOTES</span></span>
<span data-ttu-id="d8b7c-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="d8b7c-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="d8b7c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8b7c-128">RELATED LINKS</span></span>

[<span data-ttu-id="d8b7c-129">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d8b7c-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d8b7c-130">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d8b7c-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d8b7c-131">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d8b7c-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d8b7c-132">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d8b7c-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d8b7c-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d8b7c-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d8b7c-134">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d8b7c-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d8b7c-135">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d8b7c-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d8b7c-136">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d8b7c-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d8b7c-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d8b7c-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d8b7c-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d8b7c-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d8b7c-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d8b7c-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d8b7c-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d8b7c-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
