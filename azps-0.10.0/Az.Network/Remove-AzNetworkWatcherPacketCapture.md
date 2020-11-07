---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b3095aace7fa8e1959e51ef64aa92b6d2bcaffba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862946"
---
# <span data-ttu-id="da26f-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da26f-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="da26f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da26f-102">SYNOPSIS</span></span>
<span data-ttu-id="da26f-103">Rimuove una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="da26f-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="da26f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da26f-104">SYNTAX</span></span>

### <span data-ttu-id="da26f-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da26f-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da26f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="da26f-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da26f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da26f-107">DESCRIPTION</span></span>
<span data-ttu-id="da26f-108">La Remove-AzNetworkWatcherPacketCapture rimuove una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="da26f-108">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="da26f-109">È consigliabile chiamare Stop-AzNetworkWatcherPacketCapture prima di chiamare Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="da26f-109">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="da26f-110">Se la sessione di acquisizione di pacchetti viene eseguita quando si chiama Remove-AzNetworkWatcherPacketCapture l'acquisizione di pacchetti potrebbe non essere salvata.</span><span class="sxs-lookup"><span data-stu-id="da26f-110">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="da26f-111">Se la sessione viene interrotta prima della rimozione, il file CAP contenente i dati di acquisizione non viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="da26f-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="da26f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da26f-112">EXAMPLES</span></span>

### <span data-ttu-id="da26f-113">---Esempio 1: rimuovere una sessione di acquisizione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="da26f-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="da26f-114">In questo esempio rimuoviamo una sessione di acquisizione di pacchetti esistente denominata "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="da26f-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="da26f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da26f-115">PARAMETERS</span></span>

### <span data-ttu-id="da26f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da26f-116">-AsJob</span></span>
<span data-ttu-id="da26f-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="da26f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da26f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da26f-118">-DefaultProfile</span></span>
<span data-ttu-id="da26f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da26f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da26f-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da26f-120">-NetworkWatcher</span></span>
<span data-ttu-id="da26f-121">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="da26f-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="da26f-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="da26f-122">-NetworkWatcherName</span></span>
<span data-ttu-id="da26f-123">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="da26f-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="da26f-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="da26f-124">-PacketCaptureName</span></span>
<span data-ttu-id="da26f-125">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="da26f-125">The packet capture name.</span></span>

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

### <span data-ttu-id="da26f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da26f-126">-PassThru</span></span>
<span data-ttu-id="da26f-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="da26f-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="da26f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da26f-128">-ResourceGroupName</span></span>
<span data-ttu-id="da26f-129">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="da26f-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="da26f-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da26f-130">-Confirm</span></span>
<span data-ttu-id="da26f-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da26f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da26f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da26f-132">-WhatIf</span></span>
<span data-ttu-id="da26f-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da26f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da26f-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da26f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da26f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da26f-135">CommonParameters</span></span>
<span data-ttu-id="da26f-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da26f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da26f-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da26f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da26f-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da26f-138">INPUTS</span></span>

### <span data-ttu-id="da26f-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da26f-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="da26f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="da26f-140">System.String</span></span>

## <span data-ttu-id="da26f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da26f-141">OUTPUTS</span></span>

### <span data-ttu-id="da26f-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="da26f-142">System.Object</span></span>

## <span data-ttu-id="da26f-143">Note</span><span class="sxs-lookup"><span data-stu-id="da26f-143">NOTES</span></span>
<span data-ttu-id="da26f-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic, Remove</span><span class="sxs-lookup"><span data-stu-id="da26f-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="da26f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da26f-145">RELATED LINKS</span></span>

[<span data-ttu-id="da26f-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da26f-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da26f-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="da26f-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="da26f-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da26f-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da26f-149">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="da26f-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="da26f-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da26f-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="da26f-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da26f-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="da26f-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="da26f-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="da26f-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="da26f-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="da26f-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="da26f-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="da26f-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="da26f-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="da26f-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="da26f-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="da26f-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="da26f-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
