---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 43dc48aaa58f086e6d05f45a81096612d3177a17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687879"
---
# <span data-ttu-id="6b23d-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b23d-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="6b23d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b23d-102">SYNOPSIS</span></span>
<span data-ttu-id="6b23d-103">Interrompe una sessione di acquisizione di pacchetti in corso</span><span class="sxs-lookup"><span data-stu-id="6b23d-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b23d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b23d-104">SYNTAX</span></span>

### <span data-ttu-id="6b23d-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b23d-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b23d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6b23d-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b23d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b23d-107">DESCRIPTION</span></span>
<span data-ttu-id="6b23d-108">L'Stop-AzureRmNetworkWatcherPacketCapture interrompe una sessione di acquisizione di pacchetti in corso.</span><span class="sxs-lookup"><span data-stu-id="6b23d-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="6b23d-109">Dopo l'interruzione della sessione, il file di acquisizione di pacchetti viene caricato nello spazio di archiviazione e/o salvato localmente nella VM a seconda della configurazione.</span><span class="sxs-lookup"><span data-stu-id="6b23d-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="6b23d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b23d-110">EXAMPLES</span></span>

### <span data-ttu-id="6b23d-111">---Esempio 1: interrompere una sessione di acquisizione di pacchetti---</span><span class="sxs-lookup"><span data-stu-id="6b23d-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="6b23d-112">In questo esempio interrompiamo una sessione di acquisizione di pacchetti in corso denominata "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="6b23d-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="6b23d-113">Dopo l'interruzione della sessione, il file di acquisizione di pacchetti viene caricato nello spazio di archiviazione e/o salvato localmente nella VM a seconda della configurazione.</span><span class="sxs-lookup"><span data-stu-id="6b23d-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="6b23d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b23d-114">PARAMETERS</span></span>

### <span data-ttu-id="6b23d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b23d-115">-AsJob</span></span>
<span data-ttu-id="6b23d-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6b23d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b23d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b23d-117">-DefaultProfile</span></span>
<span data-ttu-id="6b23d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b23d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b23d-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b23d-119">-NetworkWatcher</span></span>
<span data-ttu-id="6b23d-120">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="6b23d-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="6b23d-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6b23d-121">-NetworkWatcherName</span></span>
<span data-ttu-id="6b23d-122">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="6b23d-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="6b23d-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="6b23d-123">-PacketCaptureName</span></span>
<span data-ttu-id="6b23d-124">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="6b23d-124">The packet capture name.</span></span>

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

### <span data-ttu-id="6b23d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b23d-125">-PassThru</span></span>
<span data-ttu-id="6b23d-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6b23d-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6b23d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b23d-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b23d-128">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="6b23d-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6b23d-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b23d-129">-Confirm</span></span>
<span data-ttu-id="6b23d-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b23d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b23d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b23d-131">-WhatIf</span></span>
<span data-ttu-id="6b23d-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b23d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b23d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b23d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b23d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b23d-134">CommonParameters</span></span>
<span data-ttu-id="6b23d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b23d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b23d-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b23d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b23d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b23d-137">INPUTS</span></span>

### <span data-ttu-id="6b23d-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b23d-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6b23d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6b23d-139">System.String</span></span>

## <span data-ttu-id="6b23d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b23d-140">OUTPUTS</span></span>

### <span data-ttu-id="6b23d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b23d-141">System.Boolean</span></span>

## <span data-ttu-id="6b23d-142">Note</span><span class="sxs-lookup"><span data-stu-id="6b23d-142">NOTES</span></span>
<span data-ttu-id="6b23d-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="6b23d-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="6b23d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b23d-144">RELATED LINKS</span></span>

[<span data-ttu-id="6b23d-145">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b23d-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b23d-146">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6b23d-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="6b23d-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b23d-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b23d-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b23d-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b23d-149">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b23d-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6b23d-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b23d-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6b23d-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b23d-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6b23d-152">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6b23d-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="6b23d-153">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6b23d-153">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="6b23d-154">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6b23d-154">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6b23d-155">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6b23d-155">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="6b23d-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6b23d-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
