---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7554183d52b263f4eed470295a2574a3d1f487b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521825"
---
# <span data-ttu-id="6af8d-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6af8d-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="6af8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6af8d-102">SYNOPSIS</span></span>
<span data-ttu-id="6af8d-103">Crea un monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="6af8d-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6af8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6af8d-104">SYNTAX</span></span>

### <span data-ttu-id="6af8d-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6af8d-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6af8d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6af8d-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6af8d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6af8d-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6af8d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6af8d-108">DESCRIPTION</span></span>
<span data-ttu-id="6af8d-109">Il cmdlet New-AzureRmNetworkWatcherConnectionMonitor rcreates un monitor di connessione per un'origine e una destinazione specificate.</span><span class="sxs-lookup"><span data-stu-id="6af8d-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="6af8d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6af8d-110">EXAMPLES</span></span>

### <span data-ttu-id="6af8d-111">Esempio 1: creare un monitor di connessione per una VM e una destinazione Internet</span><span class="sxs-lookup"><span data-stu-id="6af8d-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="6af8d-112">Il cmdlet New-AzureRmNetworkWatcherConnectionMonitor crea un monitor di connessione per un'origine e una destinazione specificate.</span><span class="sxs-lookup"><span data-stu-id="6af8d-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="6af8d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6af8d-113">PARAMETERS</span></span>

### <span data-ttu-id="6af8d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6af8d-114">-AsJob</span></span>
<span data-ttu-id="6af8d-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6af8d-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af8d-116">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="6af8d-116">-ConfigureOnly</span></span>
<span data-ttu-id="6af8d-117">Configurare monitor di connessione, ma non avviarlo</span><span class="sxs-lookup"><span data-stu-id="6af8d-117">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="6af8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af8d-118">-DefaultProfile</span></span>
<span data-ttu-id="6af8d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6af8d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6af8d-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6af8d-120">-DestinationAddress</span></span>
<span data-ttu-id="6af8d-121">Indirizzo IP della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="6af8d-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="6af8d-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6af8d-122">-DestinationPort</span></span>
<span data-ttu-id="6af8d-123">Porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6af8d-123">Destination port.</span></span>

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

### <span data-ttu-id="6af8d-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="6af8d-124">-DestinationResourceId</span></span>
<span data-ttu-id="6af8d-125">ID della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="6af8d-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="6af8d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6af8d-126">-Force</span></span>
<span data-ttu-id="6af8d-127">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="6af8d-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af8d-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6af8d-128">-Location</span></span>
<span data-ttu-id="6af8d-129">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="6af8d-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6af8d-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6af8d-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="6af8d-131">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="6af8d-131">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af8d-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="6af8d-132">-Name</span></span>
<span data-ttu-id="6af8d-133">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="6af8d-133">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af8d-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6af8d-134">-NetworkWatcher</span></span>
<span data-ttu-id="6af8d-135">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="6af8d-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="6af8d-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6af8d-136">-NetworkWatcherName</span></span>
<span data-ttu-id="6af8d-137">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="6af8d-137">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af8d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6af8d-138">-ResourceGroupName</span></span>
<span data-ttu-id="6af8d-139">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="6af8d-139">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af8d-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="6af8d-140">-SourcePort</span></span>
<span data-ttu-id="6af8d-141">Porta di origine.</span><span class="sxs-lookup"><span data-stu-id="6af8d-141">Source port.</span></span>

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

### <span data-ttu-id="6af8d-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="6af8d-142">-SourceResourceId</span></span>
<span data-ttu-id="6af8d-143">ID dell'origine del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="6af8d-143">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="6af8d-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="6af8d-144">-Tag</span></span>
<span data-ttu-id="6af8d-145">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6af8d-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6af8d-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6af8d-146">-Confirm</span></span>
<span data-ttu-id="6af8d-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6af8d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6af8d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6af8d-148">-WhatIf</span></span>
<span data-ttu-id="6af8d-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6af8d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6af8d-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6af8d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6af8d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af8d-151">CommonParameters</span></span>
<span data-ttu-id="6af8d-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6af8d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af8d-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6af8d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af8d-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6af8d-154">INPUTS</span></span>

### <span data-ttu-id="6af8d-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6af8d-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6af8d-156">Parametri: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6af8d-156">Parameters: NetworkWatcher (ByValue)</span></span>

## <span data-ttu-id="6af8d-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6af8d-157">OUTPUTS</span></span>

### <span data-ttu-id="6af8d-158">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="6af8d-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="6af8d-159">Note</span><span class="sxs-lookup"><span data-stu-id="6af8d-159">NOTES</span></span>
<span data-ttu-id="6af8d-160">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="6af8d-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="6af8d-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6af8d-161">RELATED LINKS</span></span>

[<span data-ttu-id="6af8d-162">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6af8d-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6af8d-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6af8d-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6af8d-164">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6af8d-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6af8d-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6af8d-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="6af8d-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6af8d-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="6af8d-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6af8d-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="6af8d-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6af8d-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="6af8d-169">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6af8d-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6af8d-170">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6af8d-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="6af8d-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6af8d-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6af8d-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6af8d-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6af8d-173">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6af8d-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6af8d-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6af8d-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6af8d-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6af8d-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="6af8d-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6af8d-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6af8d-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6af8d-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6af8d-178">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6af8d-178">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6af8d-179">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6af8d-179">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6af8d-180">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6af8d-180">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="6af8d-181">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6af8d-181">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="6af8d-182">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6af8d-182">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="6af8d-183">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6af8d-183">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="6af8d-184">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6af8d-184">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6af8d-185">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6af8d-185">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="6af8d-186">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6af8d-186">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="6af8d-187">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6af8d-187">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="6af8d-188">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6af8d-188">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
