---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: 4efe4ea25260e8e17c35a8f85c9e521355f67300
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958397"
---
# <span data-ttu-id="6b87a-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="6b87a-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="6b87a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b87a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b87a-103">Crea un nuovo oggetto profilo di diagnostica della configurazione di rete.</span><span class="sxs-lookup"><span data-stu-id="6b87a-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="6b87a-104">Questo oggetto viene usato per limitare la configurazione di rete durante una sessione di diagnostica usando i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="6b87a-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="6b87a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b87a-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b87a-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6b87a-106">DESCRIPTION</span></span>
<span data-ttu-id="6b87a-107">Il New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet crea un nuovo oggetto profilo di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="6b87a-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="6b87a-108">Questo oggetto viene usato per limitare la configurazione di rete durante una sessione di diagnostica della configurazione di rete usando i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="6b87a-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="6b87a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b87a-109">EXAMPLES</span></span>

### <span data-ttu-id="6b87a-110">Esempio 1: Richiamare la sessione di diagnostica della configurazione di rete per la macchina virtuale e il profilo di rete specificato</span><span class="sxs-lookup"><span data-stu-id="6b87a-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
```
PS C:\> $profile = New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction Inbound -Protocol Tcp -Source 10.1.1.4 -Destination * -DestinationPort 50
PS C:\> Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location eastus -TargetResourceId /subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/NwRgEastUS/providers/Microsoft.Compute/virtualMachines/vm1 -Profile $profile

Results : [
            {
              "Profile": {
                "Direction": "Inbound",
                "Protocol": "Tcp",
                "Source": "10.1.1.4",
                "Destination": "*",
                "DestinationPort": "50"
              },
              "NetworkSecurityGroupResult": {
                "SecurityRuleAccessResult": "Allow",
                "EvaluatedNetworkSecurityGroups": [
                  {
                    "NetworkSecurityGroupId": "/subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/clean
          upservice/providers/Microsoft.Network/networkSecurityGroups/rg-cleanupservice-nsg1",
                    "MatchedRule": {
                      "RuleName": "UserRule_Cleanuptool-Allow-4001",
                      "Action": "Allow"
                    },
                    "RulesEvaluationResult": [
                      {
                        "Name": "UserRule_Cleanuptool-Allow-100",
                        "ProtocolMatched": true,
                        "SourceMatched": false,
                        "SourcePortMatched": true,
                        "DestinationMatched": true,
                        "DestinationPortMatched": false
                      },
```

## <span data-ttu-id="6b87a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b87a-111">PARAMETERS</span></span>

### <span data-ttu-id="6b87a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b87a-112">-DefaultProfile</span></span>
<span data-ttu-id="6b87a-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b87a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b87a-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="6b87a-114">-Destination</span></span>
<span data-ttu-id="6b87a-115">Destinazione del traffico.</span><span class="sxs-lookup"><span data-stu-id="6b87a-115">Traffic destination.</span></span>
<span data-ttu-id="6b87a-116">I valori accettati sono: '\*', Indirizzo IP/CIDR, Tag di servizio.</span><span class="sxs-lookup"><span data-stu-id="6b87a-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="6b87a-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6b87a-117">-DestinationPort</span></span>
<span data-ttu-id="6b87a-118">Porta di destinazione del traffico.</span><span class="sxs-lookup"><span data-stu-id="6b87a-118">Traffic destination port.</span></span>
<span data-ttu-id="6b87a-119">I valori accettati sono "\*", la porta (ad esempio 3389) e l'intervallo di porte (ad esempio, 80-100).</span><span class="sxs-lookup"><span data-stu-id="6b87a-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="6b87a-120">-Direction</span><span class="sxs-lookup"><span data-stu-id="6b87a-120">-Direction</span></span>
<span data-ttu-id="6b87a-121">Direzione del traffico.</span><span class="sxs-lookup"><span data-stu-id="6b87a-121">The direction of the traffic.</span></span>
<span data-ttu-id="6b87a-122">I valori accettati sono "In ingresso" e "In uscita"</span><span class="sxs-lookup"><span data-stu-id="6b87a-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b87a-123">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6b87a-123">-Protocol</span></span>
<span data-ttu-id="6b87a-124">Protocollo da verificare.</span><span class="sxs-lookup"><span data-stu-id="6b87a-124">Protocol to be verified on.</span></span>
<span data-ttu-id="6b87a-125">I valori accettati sono "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="6b87a-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="6b87a-126">-Source</span><span class="sxs-lookup"><span data-stu-id="6b87a-126">-Source</span></span>
<span data-ttu-id="6b87a-127">Origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="6b87a-127">Traffic source.</span></span>
<span data-ttu-id="6b87a-128">I valori accettati sono '\*', Indirizzo IP/CIDR, Tag di servizio.</span><span class="sxs-lookup"><span data-stu-id="6b87a-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="6b87a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b87a-129">CommonParameters</span></span>
<span data-ttu-id="6b87a-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b87a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b87a-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b87a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b87a-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="6b87a-132">INPUTS</span></span>

### <span data-ttu-id="6b87a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6b87a-133">System.String</span></span>

## <span data-ttu-id="6b87a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b87a-134">OUTPUTS</span></span>

### <span data-ttu-id="6b87a-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="6b87a-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="6b87a-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="6b87a-136">NOTES</span></span>
<span data-ttu-id="6b87a-137">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, watcher, diagnostica, profilo</span><span class="sxs-lookup"><span data-stu-id="6b87a-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="6b87a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b87a-138">RELATED LINKS</span></span>

[<span data-ttu-id="6b87a-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b87a-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6b87a-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b87a-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6b87a-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6b87a-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6b87a-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6b87a-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6b87a-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6b87a-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6b87a-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6b87a-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6b87a-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6b87a-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6b87a-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b87a-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b87a-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6b87a-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6b87a-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b87a-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b87a-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b87a-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b87a-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6b87a-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6b87a-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b87a-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6b87a-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6b87a-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6b87a-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6b87a-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6b87a-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6b87a-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6b87a-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6b87a-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6b87a-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6b87a-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6b87a-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6b87a-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6b87a-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6b87a-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6b87a-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6b87a-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6b87a-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6b87a-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6b87a-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6b87a-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6b87a-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6b87a-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6b87a-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6b87a-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6b87a-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6b87a-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="6b87a-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6b87a-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
