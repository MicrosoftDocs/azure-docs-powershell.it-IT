---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: e879de96f861c5a102077c3d392944f79a293b10
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406809"
---
# <span data-ttu-id="05bb9-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="05bb9-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="05bb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="05bb9-103">Crea un nuovo oggetto profilo di diagnostica della configurazione di rete.</span><span class="sxs-lookup"><span data-stu-id="05bb9-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="05bb9-104">Questo oggetto viene usato per limitare la configurazione di rete durante una sessione di diagnostica usando i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="05bb9-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="05bb9-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05bb9-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05bb9-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05bb9-106">DESCRIPTION</span></span>
<span data-ttu-id="05bb9-107">Il cmdlet New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile crea un nuovo oggetto profilo di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="05bb9-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="05bb9-108">Questo oggetto viene usato per limitare la configurazione di rete durante una sessione di diagnostica della configurazione di rete usando i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="05bb9-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="05bb9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05bb9-109">EXAMPLES</span></span>

### <span data-ttu-id="05bb9-110">Esempio 1: Richiamare la sessione di diagnostica della configurazione di rete per la macchina virtuale e il profilo di rete specificato</span><span class="sxs-lookup"><span data-stu-id="05bb9-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="05bb9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05bb9-111">PARAMETERS</span></span>

### <span data-ttu-id="05bb9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05bb9-112">-DefaultProfile</span></span>
<span data-ttu-id="05bb9-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05bb9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05bb9-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="05bb9-114">-Destination</span></span>
<span data-ttu-id="05bb9-115">Destinazione del traffico.</span><span class="sxs-lookup"><span data-stu-id="05bb9-115">Traffic destination.</span></span>
<span data-ttu-id="05bb9-116">I valori accettati sono: '\*', Indirizzo IP/CIDR, Tag di servizio.</span><span class="sxs-lookup"><span data-stu-id="05bb9-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="05bb9-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="05bb9-117">-DestinationPort</span></span>
<span data-ttu-id="05bb9-118">Porta di destinazione del traffico.</span><span class="sxs-lookup"><span data-stu-id="05bb9-118">Traffic destination port.</span></span>
<span data-ttu-id="05bb9-119">I valori accettati sono "\*", la porta (ad esempio 3389) e l'intervallo di porte (ad esempio, 80-100).</span><span class="sxs-lookup"><span data-stu-id="05bb9-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="05bb9-120">-Direction</span><span class="sxs-lookup"><span data-stu-id="05bb9-120">-Direction</span></span>
<span data-ttu-id="05bb9-121">Direzione del traffico.</span><span class="sxs-lookup"><span data-stu-id="05bb9-121">The direction of the traffic.</span></span>
<span data-ttu-id="05bb9-122">I valori accettati sono "In ingresso" e "In uscita"</span><span class="sxs-lookup"><span data-stu-id="05bb9-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="05bb9-123">-Protocol</span><span class="sxs-lookup"><span data-stu-id="05bb9-123">-Protocol</span></span>
<span data-ttu-id="05bb9-124">Protocollo da verificare.</span><span class="sxs-lookup"><span data-stu-id="05bb9-124">Protocol to be verified on.</span></span>
<span data-ttu-id="05bb9-125">I valori accettati sono "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="05bb9-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="05bb9-126">-Source</span><span class="sxs-lookup"><span data-stu-id="05bb9-126">-Source</span></span>
<span data-ttu-id="05bb9-127">Origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="05bb9-127">Traffic source.</span></span>
<span data-ttu-id="05bb9-128">I valori accettati sono '\*', Indirizzo IP/CIDR, Tag di servizio.</span><span class="sxs-lookup"><span data-stu-id="05bb9-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="05bb9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05bb9-129">CommonParameters</span></span>
<span data-ttu-id="05bb9-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05bb9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05bb9-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05bb9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05bb9-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="05bb9-132">INPUTS</span></span>

### <span data-ttu-id="05bb9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="05bb9-133">System.String</span></span>

## <span data-ttu-id="05bb9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05bb9-134">OUTPUTS</span></span>

### <span data-ttu-id="05bb9-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="05bb9-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="05bb9-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="05bb9-136">NOTES</span></span>
<span data-ttu-id="05bb9-137">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, watcher, diagnostica, profilo</span><span class="sxs-lookup"><span data-stu-id="05bb9-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="05bb9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05bb9-138">RELATED LINKS</span></span>

[<span data-ttu-id="05bb9-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="05bb9-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="05bb9-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="05bb9-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="05bb9-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="05bb9-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="05bb9-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="05bb9-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="05bb9-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="05bb9-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="05bb9-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="05bb9-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="05bb9-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="05bb9-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="05bb9-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="05bb9-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="05bb9-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="05bb9-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="05bb9-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="05bb9-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="05bb9-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="05bb9-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="05bb9-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="05bb9-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="05bb9-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="05bb9-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="05bb9-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="05bb9-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="05bb9-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="05bb9-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="05bb9-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="05bb9-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="05bb9-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="05bb9-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="05bb9-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="05bb9-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="05bb9-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="05bb9-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="05bb9-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="05bb9-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="05bb9-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="05bb9-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="05bb9-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="05bb9-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="05bb9-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="05bb9-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="05bb9-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="05bb9-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="05bb9-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="05bb9-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="05bb9-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="05bb9-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="05bb9-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="05bb9-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
