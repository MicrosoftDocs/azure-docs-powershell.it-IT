---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 034cca094bf6dd7d3911e3e705e03888f0ea10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520694"
---
# <span data-ttu-id="e3a87-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3a87-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="e3a87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3a87-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a87-103">Rimuove una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e3a87-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3a87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3a87-104">SYNTAX</span></span>

### <span data-ttu-id="e3a87-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3a87-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3a87-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e3a87-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3a87-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3a87-107">DESCRIPTION</span></span>
<span data-ttu-id="e3a87-108">La Remove-AzureRmNetworkWatcherPacketCapture rimuove una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e3a87-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="e3a87-109">È consigliabile chiamare Stop-AzureRmNetworkWatcherPacketCapture prima di chiamare Remove-AzureRmNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="e3a87-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="e3a87-110">Se la sessione di acquisizione di pacchetti viene eseguita quando si chiama Remove-AzureRmNetworkWatcherPacketCapture l'acquisizione di pacchetti potrebbe non essere salvata.</span><span class="sxs-lookup"><span data-stu-id="e3a87-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="e3a87-111">Se la sessione viene interrotta prima della rimozione, il file CAP contenente i dati di acquisizione non viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="e3a87-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="e3a87-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3a87-112">EXAMPLES</span></span>

### <span data-ttu-id="e3a87-113">---Esempio 1: rimuovere una sessione di acquisizione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="e3a87-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="e3a87-114">In questo esempio rimuoviamo una sessione di acquisizione di pacchetti esistente denominata "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="e3a87-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="e3a87-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3a87-115">PARAMETERS</span></span>

### <span data-ttu-id="e3a87-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3a87-116">-AsJob</span></span>
<span data-ttu-id="e3a87-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e3a87-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a87-118">-DefaultProfile</span></span>
<span data-ttu-id="e3a87-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a87-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3a87-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3a87-120">-NetworkWatcher</span></span>
<span data-ttu-id="e3a87-121">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="e3a87-121">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a87-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e3a87-122">-NetworkWatcherName</span></span>
<span data-ttu-id="e3a87-123">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="e3a87-123">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a87-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="e3a87-124">-PacketCaptureName</span></span>
<span data-ttu-id="e3a87-125">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="e3a87-125">The packet capture name.</span></span>

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

### <span data-ttu-id="e3a87-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3a87-126">-PassThru</span></span>
<span data-ttu-id="e3a87-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e3a87-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a87-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a87-128">-ResourceGroupName</span></span>
<span data-ttu-id="e3a87-129">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="e3a87-129">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a87-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3a87-130">-Confirm</span></span>
<span data-ttu-id="e3a87-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3a87-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3a87-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a87-132">-WhatIf</span></span>
<span data-ttu-id="e3a87-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3a87-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a87-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3a87-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3a87-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a87-135">CommonParameters</span></span>
<span data-ttu-id="e3a87-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a87-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a87-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a87-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a87-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3a87-138">INPUTS</span></span>

### <span data-ttu-id="e3a87-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3a87-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e3a87-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e3a87-140">System.String</span></span>

## <span data-ttu-id="e3a87-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3a87-141">OUTPUTS</span></span>

### <span data-ttu-id="e3a87-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="e3a87-142">System.Object</span></span>

## <span data-ttu-id="e3a87-143">Note</span><span class="sxs-lookup"><span data-stu-id="e3a87-143">NOTES</span></span>
<span data-ttu-id="e3a87-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic, Remove</span><span class="sxs-lookup"><span data-stu-id="e3a87-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="e3a87-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3a87-145">RELATED LINKS</span></span>

[<span data-ttu-id="e3a87-146">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3a87-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3a87-147">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e3a87-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="e3a87-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3a87-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3a87-149">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e3a87-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e3a87-150">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3a87-150">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e3a87-151">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3a87-151">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e3a87-152">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3a87-152">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e3a87-153">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e3a87-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="e3a87-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e3a87-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="e3a87-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e3a87-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e3a87-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e3a87-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="e3a87-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e3a87-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
