---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
ms.openlocfilehash: e8e8462ded1f122a050c85877e8e82b2ecc0dd9d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865888"
---
# <span data-ttu-id="8cbac-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8cbac-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="8cbac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cbac-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbac-103">Configura la registrazione del flusso per una risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8cbac-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cbac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cbac-104">SYNTAX</span></span>

### <span data-ttu-id="8cbac-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8cbac-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cbac-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8cbac-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cbac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cbac-107">DESCRIPTION</span></span>
<span data-ttu-id="8cbac-108">La Set-AzureRmNetworkWatcherConfigFlowLog configura la registrazione del flusso per una risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8cbac-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="8cbac-109">Le proprietà da configurare includono: indipendentemente dal fatto che sia abilitata o meno la registrazione del flusso per la risorsa specificata, l'account di archiviazione configurato per l'invio dei log e i criteri di conservazione per i registri.</span><span class="sxs-lookup"><span data-stu-id="8cbac-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="8cbac-110">Attualmente i gruppi di sicurezza di rete sono supportati per la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="8cbac-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="8cbac-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cbac-111">EXAMPLES</span></span>

### <span data-ttu-id="8cbac-112">---Esempio 1: configurare la registrazione del flusso per un determinato NSG---</span><span class="sxs-lookup"><span data-stu-id="8cbac-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="8cbac-113">In questo esempio viene configurato lo stato di registrazione del flusso per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="8cbac-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="8cbac-114">Nella risposta viene visualizzato il NSG specificato è abilitato la registrazione del flusso e nessun criterio di conservazione impostato.</span><span class="sxs-lookup"><span data-stu-id="8cbac-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="8cbac-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cbac-115">PARAMETERS</span></span>

### <span data-ttu-id="8cbac-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cbac-116">-AsJob</span></span>
<span data-ttu-id="8cbac-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8cbac-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cbac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbac-118">-DefaultProfile</span></span>
<span data-ttu-id="8cbac-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cbac-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cbac-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="8cbac-120">-EnableFlowLog</span></span>
<span data-ttu-id="8cbac-121">Contrassegna per abilitare/disabilitare la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="8cbac-121">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="8cbac-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="8cbac-122">-EnableRetention</span></span>
<span data-ttu-id="8cbac-123">Contrassegna per abilitare/disabilitare la conservazione.</span><span class="sxs-lookup"><span data-stu-id="8cbac-123">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="8cbac-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8cbac-124">-NetworkWatcher</span></span>
<span data-ttu-id="8cbac-125">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8cbac-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="8cbac-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8cbac-126">-NetworkWatcherName</span></span>
<span data-ttu-id="8cbac-127">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8cbac-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="8cbac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cbac-128">-ResourceGroupName</span></span>
<span data-ttu-id="8cbac-129">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8cbac-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8cbac-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8cbac-130">-RetentionInDays</span></span>
<span data-ttu-id="8cbac-131">Numero di giorni per conservare i record del log di flusso.</span><span class="sxs-lookup"><span data-stu-id="8cbac-131">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="8cbac-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8cbac-132">-StorageAccountId</span></span>
<span data-ttu-id="8cbac-133">ID dell'account di archiviazione usato per archiviare il log di flusso.</span><span class="sxs-lookup"><span data-stu-id="8cbac-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="8cbac-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8cbac-134">-TargetResourceId</span></span>
<span data-ttu-id="8cbac-135">ID risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8cbac-135">The target resource ID.</span></span>

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

### <span data-ttu-id="8cbac-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8cbac-136">-Confirm</span></span>
<span data-ttu-id="8cbac-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cbac-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cbac-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cbac-138">-WhatIf</span></span>
<span data-ttu-id="8cbac-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cbac-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cbac-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cbac-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cbac-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbac-141">CommonParameters</span></span>
<span data-ttu-id="8cbac-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cbac-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbac-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cbac-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbac-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cbac-144">INPUTS</span></span>

### <span data-ttu-id="8cbac-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8cbac-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8cbac-146">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="8cbac-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="8cbac-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cbac-147">OUTPUTS</span></span>

### <span data-ttu-id="8cbac-148">Microsoft. Azure. Commands. Network. Models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="8cbac-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="8cbac-149">Note</span><span class="sxs-lookup"><span data-stu-id="8cbac-149">NOTES</span></span>
<span data-ttu-id="8cbac-150">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Watcher, Flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="8cbac-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="8cbac-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cbac-151">RELATED LINKS</span></span>

[<span data-ttu-id="8cbac-152">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8cbac-152">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8cbac-153">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8cbac-153">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8cbac-154">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8cbac-154">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8cbac-155">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8cbac-155">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="8cbac-156">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8cbac-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8cbac-157">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8cbac-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="8cbac-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8cbac-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8cbac-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8cbac-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8cbac-160">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8cbac-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8cbac-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8cbac-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="8cbac-162">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8cbac-162">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="8cbac-163">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8cbac-163">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8cbac-164">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8cbac-164">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="8cbac-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8cbac-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8cbac-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8cbac-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
