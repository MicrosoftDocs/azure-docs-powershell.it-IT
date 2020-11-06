---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 7f9417fe4ad6e115e73502e953dfcab965ccd17b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510428"
---
# <span data-ttu-id="62f3f-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="62f3f-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="62f3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="62f3f-103">Rimuove una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="62f3f-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62f3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62f3f-104">SYNTAX</span></span>

### <span data-ttu-id="62f3f-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62f3f-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62f3f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="62f3f-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62f3f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62f3f-107">DESCRIPTION</span></span>
<span data-ttu-id="62f3f-108">La Remove-AzureRmNetworkWatcherPacketCapture rimuove una risorsa di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="62f3f-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="62f3f-109">È consigliabile chiamare Stop-AzureRmNetworkWatcherPacketCapture prima di chiamare Remove-AzureRmNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="62f3f-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="62f3f-110">Se la sessione di acquisizione di pacchetti viene eseguita quando si chiama Remove-AzureRmNetworkWatcherPacketCapture l'acquisizione di pacchetti potrebbe non essere salvata.</span><span class="sxs-lookup"><span data-stu-id="62f3f-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="62f3f-111">Se la sessione viene interrotta prima della rimozione, il file CAP contenente i dati di acquisizione non viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="62f3f-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="62f3f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62f3f-112">EXAMPLES</span></span>

### <span data-ttu-id="62f3f-113">---Esempio 1: rimuovere una sessione di acquisizione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="62f3f-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="62f3f-114">In questo esempio rimuoviamo una sessione di acquisizione di pacchetti esistente denominata "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="62f3f-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="62f3f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62f3f-115">PARAMETERS</span></span>

### <span data-ttu-id="62f3f-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62f3f-116">-NetworkWatcher</span></span>
<span data-ttu-id="62f3f-117">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="62f3f-117">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62f3f-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="62f3f-118">-NetworkWatcherName</span></span>
<span data-ttu-id="62f3f-119">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="62f3f-119">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62f3f-120">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="62f3f-120">-PacketCaptureName</span></span>
<span data-ttu-id="62f3f-121">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="62f3f-121">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f3f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62f3f-122">-PassThru</span></span>
<span data-ttu-id="62f3f-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="62f3f-123">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f3f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62f3f-124">-ResourceGroupName</span></span>
<span data-ttu-id="62f3f-125">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="62f3f-125">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f3f-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62f3f-126">-Confirm</span></span>
<span data-ttu-id="62f3f-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62f3f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f3f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62f3f-128">-WhatIf</span></span>
<span data-ttu-id="62f3f-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62f3f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62f3f-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62f3f-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f3f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f3f-131">-DefaultProfile</span></span>
<span data-ttu-id="62f3f-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62f3f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f3f-133">CommonParameters</span></span>
<span data-ttu-id="62f3f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62f3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f3f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62f3f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f3f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62f3f-136">INPUTS</span></span>

### <span data-ttu-id="62f3f-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62f3f-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="62f3f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="62f3f-138">System.String</span></span>

## <span data-ttu-id="62f3f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62f3f-139">OUTPUTS</span></span>

### <span data-ttu-id="62f3f-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="62f3f-140">System.Object</span></span>

## <span data-ttu-id="62f3f-141">Note</span><span class="sxs-lookup"><span data-stu-id="62f3f-141">NOTES</span></span>
<span data-ttu-id="62f3f-142">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic, Remove</span><span class="sxs-lookup"><span data-stu-id="62f3f-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="62f3f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62f3f-143">RELATED LINKS</span></span>

[<span data-ttu-id="62f3f-144">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="62f3f-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="62f3f-145">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="62f3f-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="62f3f-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="62f3f-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="62f3f-147">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="62f3f-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="62f3f-148">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62f3f-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="62f3f-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62f3f-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="62f3f-150">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="62f3f-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="62f3f-151">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="62f3f-151">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="62f3f-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="62f3f-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="62f3f-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="62f3f-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="62f3f-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="62f3f-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="62f3f-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="62f3f-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
