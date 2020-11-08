---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: 8d3a714f2798c4866df39cd63c664228f078c37c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189473"
---
# <span data-ttu-id="43ac9-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="43ac9-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="43ac9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="43ac9-103">Restituisce le informazioni di connettività per una VM di origine specificata e una destinazione.</span><span class="sxs-lookup"><span data-stu-id="43ac9-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="43ac9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43ac9-104">SYNTAX</span></span>

### <span data-ttu-id="43ac9-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43ac9-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43ac9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="43ac9-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43ac9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="43ac9-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43ac9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43ac9-108">DESCRIPTION</span></span>
<span data-ttu-id="43ac9-109">Il cmdlet Test-AzNetworkWatcherConnectivity restituisce le informazioni di connettività per una VM di origine specificata e una destinazione.</span><span class="sxs-lookup"><span data-stu-id="43ac9-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="43ac9-110">Se non è possibile stabilire la connettività tra l'origine e la destinazione, il cmdlet restituisce i dettagli sul problema.</span><span class="sxs-lookup"><span data-stu-id="43ac9-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="43ac9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43ac9-111">EXAMPLES</span></span>

### <span data-ttu-id="43ac9-112">Esempio 1: testare la connettività di Network Watcher da una VM a un sito Web</span><span class="sxs-lookup"><span data-stu-id="43ac9-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```powershell
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

<span data-ttu-id="43ac9-113">In questo esempio verifichiamo la connettività da una VM in Azure a www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="43ac9-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

### <span data-ttu-id="43ac9-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="43ac9-114">Example 2</span></span>

<span data-ttu-id="43ac9-115">Restituisce le informazioni di connettività per una VM di origine specificata e una destinazione.</span><span class="sxs-lookup"><span data-stu-id="43ac9-115">Returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="43ac9-116">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="43ac9-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Test-AzNetworkWatcherConnectivity -DestinationAddress 'bing.com' -DestinationPort 80 -NetworkWatcher <PSNetworkWatcher> -SourceId '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0'
```

## <span data-ttu-id="43ac9-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43ac9-117">PARAMETERS</span></span>

### <span data-ttu-id="43ac9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43ac9-118">-AsJob</span></span>
<span data-ttu-id="43ac9-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="43ac9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43ac9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ac9-120">-DefaultProfile</span></span>
<span data-ttu-id="43ac9-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43ac9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43ac9-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="43ac9-122">-DestinationAddress</span></span>
<span data-ttu-id="43ac9-123">Indirizzo IP o URI la risorsa a cui verrà eseguito un tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="43ac9-123">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="43ac9-124">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="43ac9-124">-DestinationId</span></span>
<span data-ttu-id="43ac9-125">ID della risorsa a cui verrà eseguito un tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="43ac9-125">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="43ac9-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="43ac9-126">-DestinationPort</span></span>
<span data-ttu-id="43ac9-127">Porta in cui verrà eseguito il controllo della connettività.</span><span class="sxs-lookup"><span data-stu-id="43ac9-127">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="43ac9-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="43ac9-128">-Location</span></span>
<span data-ttu-id="43ac9-129">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="43ac9-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="43ac9-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43ac9-130">-NetworkWatcher</span></span>
<span data-ttu-id="43ac9-131">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="43ac9-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="43ac9-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="43ac9-132">-NetworkWatcherName</span></span>
<span data-ttu-id="43ac9-133">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="43ac9-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="43ac9-134">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="43ac9-134">-ProtocolConfiguration</span></span>
<span data-ttu-id="43ac9-135">Configurazione del protocollo in cui verrà eseguito il controllo della connettività.</span><span class="sxs-lookup"><span data-stu-id="43ac9-135">Protocol configuration on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="43ac9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ac9-136">-ResourceGroupName</span></span>
<span data-ttu-id="43ac9-137">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="43ac9-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="43ac9-138">-SourceId</span><span class="sxs-lookup"><span data-stu-id="43ac9-138">-SourceId</span></span>
<span data-ttu-id="43ac9-139">ID della risorsa da cui verrà avviata una verifica della connettività.</span><span class="sxs-lookup"><span data-stu-id="43ac9-139">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="43ac9-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="43ac9-140">-SourcePort</span></span>
<span data-ttu-id="43ac9-141">La porta di origine da cui verrà eseguito un controllo della connettività.</span><span class="sxs-lookup"><span data-stu-id="43ac9-141">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="43ac9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ac9-142">CommonParameters</span></span>
<span data-ttu-id="43ac9-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ac9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ac9-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ac9-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ac9-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43ac9-145">INPUTS</span></span>

### <span data-ttu-id="43ac9-146">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="43ac9-146">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="43ac9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="43ac9-147">System.String</span></span>

### <span data-ttu-id="43ac9-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="43ac9-148">System.Int32</span></span>

## <span data-ttu-id="43ac9-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43ac9-149">OUTPUTS</span></span>

### <span data-ttu-id="43ac9-150">Microsoft. Azure. Commands. Network. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="43ac9-150">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="43ac9-151">Note</span><span class="sxs-lookup"><span data-stu-id="43ac9-151">NOTES</span></span>
<span data-ttu-id="43ac9-152">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="43ac9-152">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="43ac9-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43ac9-153">RELATED LINKS</span></span>

<span data-ttu-id="43ac9-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="43ac9-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="43ac9-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="43ac9-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="43ac9-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="43ac9-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="43ac9-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
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
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span><span class="sxs-lookup"><span data-stu-id="43ac9-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
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
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span></span>
