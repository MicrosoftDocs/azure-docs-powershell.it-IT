---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: c4d31de526132974defc6b3d28542e1ec8de4c67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862669"
---
# <span data-ttu-id="3ae54-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ae54-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="3ae54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ae54-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae54-103">Interrompe una sessione di acquisizione di pacchetti in corso</span><span class="sxs-lookup"><span data-stu-id="3ae54-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="3ae54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ae54-104">SYNTAX</span></span>

### <span data-ttu-id="3ae54-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ae54-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ae54-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3ae54-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ae54-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ae54-107">DESCRIPTION</span></span>
<span data-ttu-id="3ae54-108">L'Stop-AzNetworkWatcherPacketCapture interrompe una sessione di acquisizione di pacchetti in corso.</span><span class="sxs-lookup"><span data-stu-id="3ae54-108">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="3ae54-109">Dopo l'interruzione della sessione, il file di acquisizione di pacchetti viene caricato nello spazio di archiviazione e/o salvato localmente nella VM a seconda della configurazione.</span><span class="sxs-lookup"><span data-stu-id="3ae54-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="3ae54-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ae54-110">EXAMPLES</span></span>

### <span data-ttu-id="3ae54-111">---Esempio 1: interrompere una sessione di acquisizione di pacchetti---</span><span class="sxs-lookup"><span data-stu-id="3ae54-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="3ae54-112">In questo esempio interrompiamo una sessione di acquisizione di pacchetti in corso denominata "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="3ae54-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="3ae54-113">Dopo l'interruzione della sessione, il file di acquisizione di pacchetti viene caricato nello spazio di archiviazione e/o salvato localmente nella VM a seconda della configurazione.</span><span class="sxs-lookup"><span data-stu-id="3ae54-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="3ae54-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ae54-114">PARAMETERS</span></span>

### <span data-ttu-id="3ae54-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ae54-115">-AsJob</span></span>
<span data-ttu-id="3ae54-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3ae54-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ae54-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae54-117">-DefaultProfile</span></span>
<span data-ttu-id="3ae54-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae54-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ae54-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ae54-119">-NetworkWatcher</span></span>
<span data-ttu-id="3ae54-120">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="3ae54-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="3ae54-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3ae54-121">-NetworkWatcherName</span></span>
<span data-ttu-id="3ae54-122">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="3ae54-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="3ae54-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="3ae54-123">-PacketCaptureName</span></span>
<span data-ttu-id="3ae54-124">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="3ae54-124">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae54-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ae54-125">-PassThru</span></span>
<span data-ttu-id="3ae54-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3ae54-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3ae54-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae54-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ae54-128">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="3ae54-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3ae54-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ae54-129">-Confirm</span></span>
<span data-ttu-id="3ae54-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ae54-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ae54-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ae54-131">-WhatIf</span></span>
<span data-ttu-id="3ae54-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ae54-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ae54-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ae54-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ae54-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae54-134">CommonParameters</span></span>
<span data-ttu-id="3ae54-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ae54-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae54-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ae54-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae54-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ae54-137">INPUTS</span></span>

### <span data-ttu-id="3ae54-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ae54-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3ae54-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3ae54-139">System.String</span></span>

## <span data-ttu-id="3ae54-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ae54-140">OUTPUTS</span></span>

### <span data-ttu-id="3ae54-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ae54-141">System.Boolean</span></span>

## <span data-ttu-id="3ae54-142">Note</span><span class="sxs-lookup"><span data-stu-id="3ae54-142">NOTES</span></span>
<span data-ttu-id="3ae54-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="3ae54-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="3ae54-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ae54-144">RELATED LINKS</span></span>

[<span data-ttu-id="3ae54-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ae54-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3ae54-146">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3ae54-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3ae54-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ae54-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3ae54-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ae54-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3ae54-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ae54-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3ae54-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ae54-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3ae54-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3ae54-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3ae54-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3ae54-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3ae54-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3ae54-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3ae54-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3ae54-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3ae54-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3ae54-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3ae54-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3ae54-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
