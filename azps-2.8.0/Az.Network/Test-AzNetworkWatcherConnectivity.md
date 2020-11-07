---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: d5adbad0f6b36375f38202fe9007e9a9f3ea19f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855102"
---
# <span data-ttu-id="9d7ff-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9d7ff-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="9d7ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7ff-103">Restituisce le informazioni di connettività per una VM di origine specificata e una destinazione.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="9d7ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d7ff-104">SYNTAX</span></span>

### <span data-ttu-id="9d7ff-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d7ff-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d7ff-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9d7ff-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d7ff-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9d7ff-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d7ff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d7ff-108">DESCRIPTION</span></span>
<span data-ttu-id="9d7ff-109">Il cmdlet Test-AzNetworkWatcherConnectivity restituisce le informazioni di connettività per una VM di origine specificata e una destinazione.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="9d7ff-110">Se non è possibile stabilire la connettività tra l'origine e la destinazione, il cmdlet restituisce i dettagli sul problema.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="9d7ff-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d7ff-111">EXAMPLES</span></span>

### <span data-ttu-id="9d7ff-112">Esempio 1: testare la connettività di Network Watcher da una VM a un sito Web</span><span class="sxs-lookup"><span data-stu-id="9d7ff-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="9d7ff-113">In questo esempio verifichiamo la connettività da una VM in Azure a www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="9d7ff-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d7ff-114">PARAMETERS</span></span>

### <span data-ttu-id="9d7ff-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d7ff-115">-AsJob</span></span>
<span data-ttu-id="9d7ff-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9d7ff-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d7ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7ff-117">-DefaultProfile</span></span>
<span data-ttu-id="9d7ff-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d7ff-119">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="9d7ff-119">-DestinationAddress</span></span>
<span data-ttu-id="9d7ff-120">Indirizzo IP o URI la risorsa a cui verrà eseguito un tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-120">The IP address or URI the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ff-121">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="9d7ff-121">-DestinationId</span></span>
<span data-ttu-id="9d7ff-122">ID della risorsa a cui verrà eseguito un tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-122">The ID of the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ff-123">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9d7ff-123">-DestinationPort</span></span>
<span data-ttu-id="9d7ff-124">Porta in cui verrà eseguito il controllo della connettività.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-124">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ff-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9d7ff-125">-Location</span></span>
<span data-ttu-id="9d7ff-126">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-126">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ff-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d7ff-127">-NetworkWatcher</span></span>
<span data-ttu-id="9d7ff-128">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="9d7ff-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9d7ff-129">-NetworkWatcherName</span></span>
<span data-ttu-id="9d7ff-130">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-130">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ff-131">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d7ff-131">-ProtocolConfiguration</span></span>
<span data-ttu-id="9d7ff-132">Configurazione del protocollo in cui verrà eseguito il controllo della connettività.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-132">Protocol configuration on which check connectivity will be performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ff-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d7ff-133">-ResourceGroupName</span></span>
<span data-ttu-id="9d7ff-134">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9d7ff-135">-SourceId</span><span class="sxs-lookup"><span data-stu-id="9d7ff-135">-SourceId</span></span>
<span data-ttu-id="9d7ff-136">ID della risorsa da cui verrà avviata una verifica della connettività.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-136">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="9d7ff-137">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="9d7ff-137">-SourcePort</span></span>
<span data-ttu-id="9d7ff-138">La porta di origine da cui verrà eseguito un controllo della connettività.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-138">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7ff-139">CommonParameters</span></span>
<span data-ttu-id="9d7ff-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d7ff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7ff-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d7ff-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7ff-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d7ff-142">INPUTS</span></span>

### <span data-ttu-id="9d7ff-143">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d7ff-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9d7ff-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9d7ff-144">System.String</span></span>

### <span data-ttu-id="9d7ff-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9d7ff-145">System.Int32</span></span>

## <span data-ttu-id="9d7ff-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d7ff-146">OUTPUTS</span></span>

### <span data-ttu-id="9d7ff-147">Microsoft. Azure. Commands. Network. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="9d7ff-147">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="9d7ff-148">Note</span><span class="sxs-lookup"><span data-stu-id="9d7ff-148">NOTES</span></span>
<span data-ttu-id="9d7ff-149">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="9d7ff-149">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="9d7ff-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d7ff-150">RELATED LINKS</span></span>

<span data-ttu-id="9d7ff-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="9d7ff-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="9d7ff-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="9d7ff-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="9d7ff-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="9d7ff-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="9d7ff-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
 [New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
 [Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
 [Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
 [Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
 [Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span><span class="sxs-lookup"><span data-stu-id="9d7ff-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)
[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)
[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)
[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)
[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span></span>