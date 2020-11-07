---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: f6c25d58588d0b75f67163c50cfa91a6f8e982da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862661"
---
# <span data-ttu-id="7acd4-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7acd4-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="7acd4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7acd4-102">SYNOPSIS</span></span>
<span data-ttu-id="7acd4-103">Restituisce le informazioni di connettività per una VM di origine specificata e una destinazione.</span><span class="sxs-lookup"><span data-stu-id="7acd4-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="7acd4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7acd4-104">SYNTAX</span></span>

### <span data-ttu-id="7acd4-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7acd4-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7acd4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7acd4-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7acd4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7acd4-107">DESCRIPTION</span></span>
<span data-ttu-id="7acd4-108">Il cmdlet Test-AzNetworkWatcherConnectivity restituisce le informazioni di connettività per una VM di origine specificata e una destinazione.</span><span class="sxs-lookup"><span data-stu-id="7acd4-108">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="7acd4-109">Se non è possibile stabilire la connettività tra l'origine e la destinazione, il cmdlet restituisce i dettagli sul problema.</span><span class="sxs-lookup"><span data-stu-id="7acd4-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="7acd4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7acd4-110">EXAMPLES</span></span>

### <span data-ttu-id="7acd4-111">---------------Esempio 1: testare la connettività di monitoraggio di rete da una VM a un sito Web---------------</span><span class="sxs-lookup"><span data-stu-id="7acd4-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
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

<span data-ttu-id="7acd4-112">In questo esempio verifichiamo la connettività da una VM in Azure a www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="7acd4-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="7acd4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7acd4-113">PARAMETERS</span></span>

### <span data-ttu-id="7acd4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7acd4-114">-AsJob</span></span>
<span data-ttu-id="7acd4-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7acd4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7acd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7acd4-116">-DefaultProfile</span></span>
<span data-ttu-id="7acd4-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7acd4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7acd4-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7acd4-118">-DestinationAddress</span></span>
<span data-ttu-id="7acd4-119">Indirizzo IP o URI la risorsa a cui verrà eseguito un tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="7acd4-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acd4-120">-DestinationId</span><span class="sxs-lookup"><span data-stu-id="7acd4-120">-DestinationId</span></span>
<span data-ttu-id="7acd4-121">ID della risorsa a cui verrà eseguito un tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="7acd4-121">The ID of the resource to which a connection attempt will be made.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acd4-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7acd4-122">-DestinationPort</span></span>
<span data-ttu-id="7acd4-123">Porta in cui verrà eseguito il controllo della connettività.</span><span class="sxs-lookup"><span data-stu-id="7acd4-123">Port on which check connectivity will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acd4-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7acd4-124">-NetworkWatcher</span></span>
<span data-ttu-id="7acd4-125">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="7acd4-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="7acd4-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7acd4-126">-NetworkWatcherName</span></span>
<span data-ttu-id="7acd4-127">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="7acd4-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7acd4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7acd4-128">-ResourceGroupName</span></span>
<span data-ttu-id="7acd4-129">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="7acd4-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7acd4-130">-SourceId</span><span class="sxs-lookup"><span data-stu-id="7acd4-130">-SourceId</span></span>
<span data-ttu-id="7acd4-131">ID della risorsa da cui verrà avviata una verifica della connettività.</span><span class="sxs-lookup"><span data-stu-id="7acd4-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="7acd4-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="7acd4-132">-SourcePort</span></span>
<span data-ttu-id="7acd4-133">La porta di origine da cui verrà eseguito un controllo della connettività.</span><span class="sxs-lookup"><span data-stu-id="7acd4-133">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="7acd4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7acd4-134">CommonParameters</span></span>
<span data-ttu-id="7acd4-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7acd4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7acd4-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7acd4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7acd4-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7acd4-137">INPUTS</span></span>

### <span data-ttu-id="7acd4-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7acd4-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7acd4-139">System. String System. Int32</span><span class="sxs-lookup"><span data-stu-id="7acd4-139">System.String System.Int32</span></span>

## <span data-ttu-id="7acd4-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7acd4-140">OUTPUTS</span></span>

### <span data-ttu-id="7acd4-141">Microsoft. Azure. Commands. Network. Models. PSConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="7acd4-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="7acd4-142">Note</span><span class="sxs-lookup"><span data-stu-id="7acd4-142">NOTES</span></span>
<span data-ttu-id="7acd4-143">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="7acd4-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="7acd4-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7acd4-144">RELATED LINKS</span></span>

<span data-ttu-id="7acd4-145">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="7acd4-145">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="7acd4-146">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="7acd4-146">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="7acd4-147">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="7acd4-147">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>
