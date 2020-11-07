---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 44f81008b0693a4ff14a80a818e9d2514dfe0ebf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687628"
---
# <span data-ttu-id="08246-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08246-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="08246-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08246-102">SYNOPSIS</span></span>
<span data-ttu-id="08246-103">Aggiornare un monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="08246-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08246-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08246-104">SYNTAX</span></span>

### <span data-ttu-id="08246-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08246-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08246-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="08246-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08246-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="08246-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08246-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="08246-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08246-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="08246-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08246-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08246-110">DESCRIPTION</span></span>
<span data-ttu-id="08246-111">Il cmdlet Set-AzureRmNetworkWatcherConnectionMonitor aggiorna il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="08246-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="08246-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08246-112">EXAMPLES</span></span>

### <span data-ttu-id="08246-113">Esempio 1: aggiornare un monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="08246-113">Example 1: Update a connection monitor</span></span>
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

<span data-ttu-id="08246-114">In questo esempio aggiorniamo il monitor di connessione esistente modificando destinationAddress e aggiungendo i tag.</span><span class="sxs-lookup"><span data-stu-id="08246-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="08246-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08246-115">PARAMETERS</span></span>

### <span data-ttu-id="08246-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08246-116">-AsJob</span></span>
<span data-ttu-id="08246-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="08246-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08246-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="08246-118">-Confirm</span></span>
<span data-ttu-id="08246-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08246-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08246-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08246-120">-DefaultProfile</span></span>
<span data-ttu-id="08246-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08246-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08246-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="08246-122">-DestinationAddress</span></span>
<span data-ttu-id="08246-123">Indirizzo IP della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="08246-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="08246-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="08246-124">-DestinationPort</span></span>
<span data-ttu-id="08246-125">Porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="08246-125">Destination port.</span></span>

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

### <span data-ttu-id="08246-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="08246-126">-DestinationResourceId</span></span>
<span data-ttu-id="08246-127">ID della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="08246-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="08246-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08246-128">-InputObject</span></span>
<span data-ttu-id="08246-129">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="08246-129">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08246-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="08246-130">-Location</span></span>
<span data-ttu-id="08246-131">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="08246-131">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08246-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="08246-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="08246-133">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="08246-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="08246-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="08246-134">-Name</span></span>
<span data-ttu-id="08246-135">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="08246-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08246-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08246-136">-NetworkWatcher</span></span>
<span data-ttu-id="08246-137">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="08246-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="08246-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="08246-138">-NetworkWatcherName</span></span>
<span data-ttu-id="08246-139">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="08246-139">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08246-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08246-140">-ResourceGroupName</span></span>
<span data-ttu-id="08246-141">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="08246-141">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08246-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08246-142">-ResourceId</span></span>
<span data-ttu-id="08246-143">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="08246-143">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08246-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="08246-144">-SourcePort</span></span>
<span data-ttu-id="08246-145">Porta di origine.</span><span class="sxs-lookup"><span data-stu-id="08246-145">Source port.</span></span>

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

### <span data-ttu-id="08246-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="08246-146">-SourceResourceId</span></span>
<span data-ttu-id="08246-147">ID dell'origine del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="08246-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="08246-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="08246-148">-Tag</span></span>
<span data-ttu-id="08246-149">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="08246-149">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08246-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08246-150">-WhatIf</span></span>
<span data-ttu-id="08246-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08246-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08246-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08246-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08246-153">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="08246-153">-ConfigureOnly</span></span>
<span data-ttu-id="08246-154">Configurare monitor di connessione, ma non avviarlo</span><span class="sxs-lookup"><span data-stu-id="08246-154">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="08246-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08246-155">CommonParameters</span></span>
<span data-ttu-id="08246-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08246-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="08246-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08246-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08246-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08246-158">INPUTS</span></span>

### <span data-ttu-id="08246-159">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08246-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="08246-160">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="08246-160">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="08246-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08246-161">OUTPUTS</span></span>

### <span data-ttu-id="08246-162">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="08246-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="08246-163">Note</span><span class="sxs-lookup"><span data-stu-id="08246-163">NOTES</span></span>
<span data-ttu-id="08246-164">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="08246-164">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="08246-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08246-165">RELATED LINKS</span></span>

[<span data-ttu-id="08246-166">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08246-166">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="08246-167">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08246-167">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="08246-168">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08246-168">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="08246-169">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="08246-169">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="08246-170">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="08246-170">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="08246-171">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="08246-171">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="08246-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="08246-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="08246-173">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08246-173">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="08246-174">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="08246-174">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="08246-175">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08246-175">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="08246-176">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08246-176">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="08246-177">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08246-177">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="08246-178">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08246-178">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="08246-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="08246-179">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="08246-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08246-180">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="08246-181">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08246-181">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="08246-182">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08246-182">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="08246-183">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08246-183">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
