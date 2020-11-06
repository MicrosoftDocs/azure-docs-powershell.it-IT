---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 3f1206b79f8e80793106b1e294b591e21b9fb77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510407"
---
# <span data-ttu-id="8363c-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8363c-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="8363c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8363c-102">SYNOPSIS</span></span>
<span data-ttu-id="8363c-103">Interrompe una sessione di acquisizione di pacchetti in corso</span><span class="sxs-lookup"><span data-stu-id="8363c-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8363c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8363c-104">SYNTAX</span></span>

### <span data-ttu-id="8363c-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8363c-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8363c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8363c-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8363c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8363c-107">DESCRIPTION</span></span>
<span data-ttu-id="8363c-108">L'Stop-AzureRmNetworkWatcherPacketCapture interrompe una sessione di acquisizione di pacchetti in corso.</span><span class="sxs-lookup"><span data-stu-id="8363c-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="8363c-109">Dopo l'interruzione della sessione, il file di acquisizione di pacchetti viene caricato nello spazio di archiviazione e/o salvato localmente nella VM a seconda della configurazione.</span><span class="sxs-lookup"><span data-stu-id="8363c-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="8363c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8363c-110">EXAMPLES</span></span>

### <span data-ttu-id="8363c-111">---Esempio 1: interrompere una sessione di acquisizione di pacchetti---</span><span class="sxs-lookup"><span data-stu-id="8363c-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="8363c-112">In questo esempio interrompiamo una sessione di acquisizione di pacchetti in corso denominata "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="8363c-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="8363c-113">Dopo l'interruzione della sessione, il file di acquisizione di pacchetti viene caricato nello spazio di archiviazione e/o salvato localmente nella VM a seconda della configurazione.</span><span class="sxs-lookup"><span data-stu-id="8363c-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="8363c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8363c-114">PARAMETERS</span></span>

### <span data-ttu-id="8363c-115">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8363c-115">-NetworkWatcher</span></span>
<span data-ttu-id="8363c-116">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8363c-116">The network watcher resource.</span></span>

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

### <span data-ttu-id="8363c-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8363c-117">-NetworkWatcherName</span></span>
<span data-ttu-id="8363c-118">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8363c-118">The name of network watcher.</span></span>

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

### <span data-ttu-id="8363c-119">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="8363c-119">-PacketCaptureName</span></span>
<span data-ttu-id="8363c-120">Nome del pacchetto Capture.</span><span class="sxs-lookup"><span data-stu-id="8363c-120">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8363c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8363c-121">-PassThru</span></span>
<span data-ttu-id="8363c-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8363c-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8363c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8363c-123">-ResourceGroupName</span></span>
<span data-ttu-id="8363c-124">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8363c-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8363c-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8363c-125">-Confirm</span></span>
<span data-ttu-id="8363c-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8363c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8363c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8363c-127">-WhatIf</span></span>
<span data-ttu-id="8363c-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8363c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8363c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8363c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8363c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8363c-130">-DefaultProfile</span></span>
<span data-ttu-id="8363c-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8363c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8363c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8363c-132">CommonParameters</span></span>
<span data-ttu-id="8363c-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8363c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8363c-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8363c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8363c-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8363c-135">INPUTS</span></span>

### <span data-ttu-id="8363c-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8363c-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8363c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8363c-137">System.String</span></span>

## <span data-ttu-id="8363c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8363c-138">OUTPUTS</span></span>

### <span data-ttu-id="8363c-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8363c-139">System.Boolean</span></span>

## <span data-ttu-id="8363c-140">Note</span><span class="sxs-lookup"><span data-stu-id="8363c-140">NOTES</span></span>
<span data-ttu-id="8363c-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Packet, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="8363c-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="8363c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8363c-142">RELATED LINKS</span></span>

[<span data-ttu-id="8363c-143">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8363c-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8363c-144">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8363c-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="8363c-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8363c-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8363c-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8363c-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8363c-147">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8363c-147">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8363c-148">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8363c-148">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8363c-149">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8363c-149">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8363c-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8363c-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="8363c-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8363c-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="8363c-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8363c-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8363c-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8363c-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="8363c-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8363c-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
