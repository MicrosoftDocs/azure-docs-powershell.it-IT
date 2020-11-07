---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5c7709c234ba762e5b87418cc0e9b3fc4637ac11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686385"
---
# <span data-ttu-id="e8257-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8257-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="e8257-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8257-102">SYNOPSIS</span></span>
<span data-ttu-id="e8257-103">Aggiornare un monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="e8257-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8257-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8257-104">SYNTAX</span></span>

### <span data-ttu-id="e8257-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8257-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8257-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e8257-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8257-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e8257-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8257-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8257-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8257-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8257-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8257-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8257-110">DESCRIPTION</span></span>
<span data-ttu-id="e8257-111">Il cmdlet Set-AzureRmNetworkWatcherConnectionMonitor aggiorna il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="e8257-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="e8257-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8257-112">EXAMPLES</span></span>

### <span data-ttu-id="e8257-113">Esempio 1: aggiornare un monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="e8257-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="e8257-114">In questo esempio aggiorniamo il monitor di connessione esistente modificando destinationAddress e aggiungendo i tag.</span><span class="sxs-lookup"><span data-stu-id="e8257-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="e8257-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8257-115">PARAMETERS</span></span>

### <span data-ttu-id="e8257-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8257-116">-AsJob</span></span>
<span data-ttu-id="e8257-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e8257-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8257-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="e8257-118">-ConfigureOnly</span></span>
<span data-ttu-id="e8257-119">Configurare monitor di connessione, ma non avviarlo</span><span class="sxs-lookup"><span data-stu-id="e8257-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="e8257-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8257-120">-DefaultProfile</span></span>
<span data-ttu-id="e8257-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8257-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8257-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e8257-122">-DestinationAddress</span></span>
<span data-ttu-id="e8257-123">Indirizzo IP della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="e8257-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="e8257-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e8257-124">-DestinationPort</span></span>
<span data-ttu-id="e8257-125">Porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e8257-125">Destination port.</span></span>

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

### <span data-ttu-id="e8257-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="e8257-126">-DestinationResourceId</span></span>
<span data-ttu-id="e8257-127">ID della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="e8257-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="e8257-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8257-128">-InputObject</span></span>
<span data-ttu-id="e8257-129">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="e8257-129">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8257-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e8257-130">-Location</span></span>
<span data-ttu-id="e8257-131">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="e8257-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e8257-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e8257-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="e8257-133">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="e8257-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="e8257-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8257-134">-Name</span></span>
<span data-ttu-id="e8257-135">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="e8257-135">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8257-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e8257-136">-NetworkWatcher</span></span>
<span data-ttu-id="e8257-137">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="e8257-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="e8257-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e8257-138">-NetworkWatcherName</span></span>
<span data-ttu-id="e8257-139">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="e8257-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="e8257-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8257-140">-ResourceGroupName</span></span>
<span data-ttu-id="e8257-141">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="e8257-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e8257-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8257-142">-ResourceId</span></span>
<span data-ttu-id="e8257-143">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e8257-143">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8257-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="e8257-144">-SourcePort</span></span>
<span data-ttu-id="e8257-145">Porta di origine.</span><span class="sxs-lookup"><span data-stu-id="e8257-145">Source port.</span></span>

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

### <span data-ttu-id="e8257-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e8257-146">-SourceResourceId</span></span>
<span data-ttu-id="e8257-147">ID dell'origine del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="e8257-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="e8257-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8257-148">-Tag</span></span>
<span data-ttu-id="e8257-149">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e8257-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e8257-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8257-150">-Confirm</span></span>
<span data-ttu-id="e8257-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8257-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8257-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8257-152">-WhatIf</span></span>
<span data-ttu-id="e8257-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8257-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8257-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8257-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8257-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8257-155">CommonParameters</span></span>
<span data-ttu-id="e8257-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8257-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8257-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8257-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8257-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8257-158">INPUTS</span></span>

### <span data-ttu-id="e8257-159">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e8257-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e8257-160">Parametri: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8257-160">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="e8257-161">System. String</span><span class="sxs-lookup"><span data-stu-id="e8257-161">System.String</span></span>

### <span data-ttu-id="e8257-162">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="e8257-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="e8257-163">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8257-163">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e8257-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8257-164">OUTPUTS</span></span>

### <span data-ttu-id="e8257-165">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="e8257-165">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="e8257-166">Note</span><span class="sxs-lookup"><span data-stu-id="e8257-166">NOTES</span></span>
<span data-ttu-id="e8257-167">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="e8257-167">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="e8257-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8257-168">RELATED LINKS</span></span>

[<span data-ttu-id="e8257-169">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e8257-169">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e8257-170">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e8257-170">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e8257-171">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e8257-171">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="e8257-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e8257-172">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="e8257-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e8257-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="e8257-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e8257-174">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="e8257-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e8257-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="e8257-176">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e8257-176">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e8257-177">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e8257-177">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="e8257-178">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e8257-178">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e8257-179">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e8257-179">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e8257-180">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e8257-180">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="e8257-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8257-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e8257-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e8257-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="e8257-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8257-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e8257-184">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8257-184">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e8257-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8257-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e8257-186">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8257-186">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e8257-187">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8257-187">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="e8257-188">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e8257-188">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="e8257-189">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e8257-189">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="e8257-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e8257-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="e8257-191">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8257-191">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="e8257-192">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e8257-192">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="e8257-193">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e8257-193">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="e8257-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e8257-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="e8257-195">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e8257-195">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
