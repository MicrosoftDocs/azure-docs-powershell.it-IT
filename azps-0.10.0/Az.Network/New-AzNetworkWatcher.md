---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: cace33dd9831dcfcc01f2a57eefb5f28367966d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860450"
---
# <span data-ttu-id="2b73c-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b73c-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="2b73c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b73c-102">SYNOPSIS</span></span>
<span data-ttu-id="2b73c-103">Crea una nuova risorsa di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="2b73c-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="2b73c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b73c-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b73c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b73c-105">DESCRIPTION</span></span>
<span data-ttu-id="2b73c-106">Il cmdlet New-AzNetworkWatcher crea una nuova risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="2b73c-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="2b73c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b73c-107">EXAMPLES</span></span>

### <span data-ttu-id="2b73c-108">Esempio 1: creare un Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="2b73c-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="2b73c-109">Questo esempio crea un nuovo Watcher di rete all'interno di un gruppo di risorse appena creato.</span><span class="sxs-lookup"><span data-stu-id="2b73c-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="2b73c-110">Tieni presente che è possibile creare un solo Watcher di rete per ogni area di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2b73c-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="2b73c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b73c-111">PARAMETERS</span></span>

### <span data-ttu-id="2b73c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b73c-112">-DefaultProfile</span></span>
<span data-ttu-id="2b73c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b73c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b73c-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2b73c-114">-Location</span></span>
<span data-ttu-id="2b73c-115">Posizione.</span><span class="sxs-lookup"><span data-stu-id="2b73c-115">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b73c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b73c-116">-Name</span></span>
<span data-ttu-id="2b73c-117">Nome del Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="2b73c-117">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b73c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b73c-118">-ResourceGroupName</span></span>
<span data-ttu-id="2b73c-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b73c-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b73c-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b73c-120">-Tag</span></span>
<span data-ttu-id="2b73c-121">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2b73c-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2b73c-122">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="2b73c-122">For example:</span></span>

<span data-ttu-id="2b73c-123">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2b73c-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b73c-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b73c-124">-Confirm</span></span>
<span data-ttu-id="2b73c-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b73c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b73c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b73c-126">-WhatIf</span></span>
<span data-ttu-id="2b73c-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b73c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b73c-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b73c-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b73c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b73c-129">CommonParameters</span></span>
<span data-ttu-id="2b73c-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b73c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b73c-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b73c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b73c-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b73c-132">INPUTS</span></span>

### <span data-ttu-id="2b73c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2b73c-133">System.String</span></span>
<span data-ttu-id="2b73c-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2b73c-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2b73c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b73c-135">OUTPUTS</span></span>

### <span data-ttu-id="2b73c-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b73c-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="2b73c-137">Note</span><span class="sxs-lookup"><span data-stu-id="2b73c-137">NOTES</span></span>
<span data-ttu-id="2b73c-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="2b73c-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="2b73c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b73c-139">RELATED LINKS</span></span>

[<span data-ttu-id="2b73c-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b73c-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2b73c-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b73c-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2b73c-142">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b73c-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b73c-143">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2b73c-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2b73c-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b73c-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b73c-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b73c-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b73c-146">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b73c-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b73c-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2b73c-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2b73c-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2b73c-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2b73c-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2b73c-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2b73c-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2b73c-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2b73c-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2b73c-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
