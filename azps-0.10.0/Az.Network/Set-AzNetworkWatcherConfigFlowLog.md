---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f250615837f4953f63a4c5ff5f0a0ea965691856
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862753"
---
# <span data-ttu-id="accab-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="accab-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="accab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="accab-102">SYNOPSIS</span></span>
<span data-ttu-id="accab-103">Configura la registrazione del flusso per una risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="accab-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="accab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="accab-104">SYNTAX</span></span>

### <span data-ttu-id="accab-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="accab-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="accab-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="accab-106">SetByName</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="accab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="accab-107">DESCRIPTION</span></span>
<span data-ttu-id="accab-108">La Set-AzNetworkWatcherConfigFlowLog configura la registrazione del flusso per una risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="accab-108">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="accab-109">Le proprietà da configurare includono: indipendentemente dal fatto che sia abilitata o meno la registrazione del flusso per la risorsa specificata, l'account di archiviazione configurato per l'invio dei log e i criteri di conservazione per i registri.</span><span class="sxs-lookup"><span data-stu-id="accab-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="accab-110">Attualmente i gruppi di sicurezza di rete sono supportati per la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="accab-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="accab-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="accab-111">EXAMPLES</span></span>

### <span data-ttu-id="accab-112">---Esempio 1: configurare la registrazione del flusso per un determinato NSG---</span><span class="sxs-lookup"><span data-stu-id="accab-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="accab-113">In questo esempio viene configurato lo stato di registrazione del flusso per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="accab-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="accab-114">Nella risposta viene visualizzato il NSG specificato è abilitato la registrazione del flusso e nessun criterio di conservazione impostato.</span><span class="sxs-lookup"><span data-stu-id="accab-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="accab-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="accab-115">PARAMETERS</span></span>

### <span data-ttu-id="accab-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="accab-116">-AsJob</span></span>
<span data-ttu-id="accab-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="accab-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="accab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="accab-118">-DefaultProfile</span></span>
<span data-ttu-id="accab-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="accab-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="accab-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="accab-120">-EnableFlowLog</span></span>
<span data-ttu-id="accab-121">Contrassegna per abilitare/disabilitare la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="accab-121">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="accab-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="accab-122">-EnableRetention</span></span>
<span data-ttu-id="accab-123">Contrassegna per abilitare/disabilitare la conservazione.</span><span class="sxs-lookup"><span data-stu-id="accab-123">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="accab-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="accab-124">-NetworkWatcher</span></span>
<span data-ttu-id="accab-125">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="accab-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="accab-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="accab-126">-NetworkWatcherName</span></span>
<span data-ttu-id="accab-127">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="accab-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="accab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="accab-128">-ResourceGroupName</span></span>
<span data-ttu-id="accab-129">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="accab-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="accab-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="accab-130">-RetentionInDays</span></span>
<span data-ttu-id="accab-131">Numero di giorni per conservare i record del log di flusso.</span><span class="sxs-lookup"><span data-stu-id="accab-131">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="accab-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="accab-132">-StorageAccountId</span></span>
<span data-ttu-id="accab-133">ID dell'account di archiviazione usato per archiviare il log di flusso.</span><span class="sxs-lookup"><span data-stu-id="accab-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="accab-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="accab-134">-TargetResourceId</span></span>
<span data-ttu-id="accab-135">ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="accab-135">The target resource ID.</span></span>

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

### <span data-ttu-id="accab-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="accab-136">-Confirm</span></span>
<span data-ttu-id="accab-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="accab-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="accab-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="accab-138">-WhatIf</span></span>
<span data-ttu-id="accab-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="accab-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="accab-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="accab-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="accab-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="accab-141">CommonParameters</span></span>
<span data-ttu-id="accab-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="accab-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="accab-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="accab-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="accab-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="accab-144">INPUTS</span></span>

### <span data-ttu-id="accab-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="accab-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="accab-146">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="accab-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="accab-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="accab-147">OUTPUTS</span></span>

### <span data-ttu-id="accab-148">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="accab-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="accab-149">Note</span><span class="sxs-lookup"><span data-stu-id="accab-149">NOTES</span></span>
<span data-ttu-id="accab-150">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Watcher, Flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="accab-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="accab-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="accab-151">RELATED LINKS</span></span>

[<span data-ttu-id="accab-152">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="accab-152">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="accab-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="accab-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="accab-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="accab-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="accab-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="accab-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="accab-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="accab-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="accab-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="accab-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="accab-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="accab-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="accab-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="accab-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="accab-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="accab-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="accab-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="accab-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="accab-162">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="accab-162">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="accab-163">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="accab-163">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="accab-164">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="accab-164">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="accab-165">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="accab-165">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="accab-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="accab-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
