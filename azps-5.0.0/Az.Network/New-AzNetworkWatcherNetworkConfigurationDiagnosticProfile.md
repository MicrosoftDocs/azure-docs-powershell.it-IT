---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: c559001c68126c42c3d4ae6eaead2beda3ded5f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193932"
---
# <span data-ttu-id="314f7-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="314f7-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="314f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="314f7-102">SYNOPSIS</span></span>
<span data-ttu-id="314f7-103">Crea un nuovo oggetto del profilo di diagnostica della configurazione di rete.</span><span class="sxs-lookup"><span data-stu-id="314f7-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="314f7-104">Questo oggetto viene usato per limitare la configurazione della rete durante una sessione di diagnostica usando i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="314f7-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="314f7-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="314f7-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="314f7-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="314f7-106">DESCRIPTION</span></span>
<span data-ttu-id="314f7-107">Il cmdlet New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile crea un nuovo oggetto del profilo di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="314f7-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="314f7-108">Questo oggetto viene usato per limitare la configurazione della rete durante una sessione di diagnostica della configurazione di rete usando i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="314f7-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="314f7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="314f7-109">EXAMPLES</span></span>

### <span data-ttu-id="314f7-110">Esempio 1: richiamare la sessione di diagnostica della configurazione di rete per VM e il profilo di rete specificato</span><span class="sxs-lookup"><span data-stu-id="314f7-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="314f7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="314f7-111">PARAMETERS</span></span>

### <span data-ttu-id="314f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314f7-112">-DefaultProfile</span></span>
<span data-ttu-id="314f7-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="314f7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="314f7-114">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="314f7-114">-Destination</span></span>
<span data-ttu-id="314f7-115">Destinazione traffico.</span><span class="sxs-lookup"><span data-stu-id="314f7-115">Traffic destination.</span></span>
<span data-ttu-id="314f7-116">I valori accettati sono:' \*', indirizzo IP/CIDR, tag di servizio.</span><span class="sxs-lookup"><span data-stu-id="314f7-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="314f7-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="314f7-117">-DestinationPort</span></span>
<span data-ttu-id="314f7-118">Porta di destinazione del traffico.</span><span class="sxs-lookup"><span data-stu-id="314f7-118">Traffic destination port.</span></span>
<span data-ttu-id="314f7-119">I valori accettati sono "\*", la porta (ad esempio 3389) e l'intervallo di porte, ad esempio 80-100.</span><span class="sxs-lookup"><span data-stu-id="314f7-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="314f7-120">-Direzione</span><span class="sxs-lookup"><span data-stu-id="314f7-120">-Direction</span></span>
<span data-ttu-id="314f7-121">Direzione del traffico.</span><span class="sxs-lookup"><span data-stu-id="314f7-121">The direction of the traffic.</span></span>
<span data-ttu-id="314f7-122">I valori accettati sono "in ingresso" e "in uscita"</span><span class="sxs-lookup"><span data-stu-id="314f7-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="314f7-123">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="314f7-123">-Protocol</span></span>
<span data-ttu-id="314f7-124">Protocollo da verificare.</span><span class="sxs-lookup"><span data-stu-id="314f7-124">Protocol to be verified on.</span></span>
<span data-ttu-id="314f7-125">I valori accettati sono "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="314f7-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="314f7-126">-Origine</span><span class="sxs-lookup"><span data-stu-id="314f7-126">-Source</span></span>
<span data-ttu-id="314f7-127">Origine traffico.</span><span class="sxs-lookup"><span data-stu-id="314f7-127">Traffic source.</span></span>
<span data-ttu-id="314f7-128">I valori accettati sono "\*", indirizzo IP/CIDR, tag di servizio.</span><span class="sxs-lookup"><span data-stu-id="314f7-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="314f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314f7-129">CommonParameters</span></span>
<span data-ttu-id="314f7-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="314f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314f7-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="314f7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314f7-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="314f7-132">INPUTS</span></span>

### <span data-ttu-id="314f7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="314f7-133">System.String</span></span>

## <span data-ttu-id="314f7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="314f7-134">OUTPUTS</span></span>

### <span data-ttu-id="314f7-135">Microsoft. Azure. Commands. Network. Models. PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="314f7-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="314f7-136">Note</span><span class="sxs-lookup"><span data-stu-id="314f7-136">NOTES</span></span>
<span data-ttu-id="314f7-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Watcher, Diagnostic, profile</span><span class="sxs-lookup"><span data-stu-id="314f7-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="314f7-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="314f7-138">RELATED LINKS</span></span>

[<span data-ttu-id="314f7-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="314f7-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="314f7-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="314f7-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="314f7-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="314f7-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="314f7-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="314f7-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="314f7-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="314f7-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="314f7-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="314f7-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="314f7-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="314f7-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="314f7-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="314f7-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="314f7-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="314f7-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="314f7-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="314f7-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="314f7-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="314f7-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="314f7-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="314f7-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="314f7-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="314f7-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="314f7-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="314f7-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="314f7-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="314f7-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="314f7-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="314f7-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="314f7-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="314f7-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="314f7-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="314f7-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="314f7-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="314f7-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="314f7-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="314f7-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="314f7-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="314f7-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="314f7-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="314f7-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="314f7-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="314f7-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="314f7-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="314f7-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="314f7-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="314f7-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="314f7-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="314f7-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="314f7-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="314f7-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)