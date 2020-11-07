---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b8dd04fa4727465ee9b3be3eaf5e5e06a2243338
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687897"
---
# <span data-ttu-id="9dddc-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dddc-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="9dddc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9dddc-102">SYNOPSIS</span></span>
<span data-ttu-id="9dddc-103">Crea un monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="9dddc-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dddc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9dddc-104">SYNTAX</span></span>

### <span data-ttu-id="9dddc-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9dddc-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9dddc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9dddc-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9dddc-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9dddc-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dddc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9dddc-108">DESCRIPTION</span></span>
<span data-ttu-id="9dddc-109">Il cmdlet New-AzureRmNetworkWatcherConnectionMonitor rcreates un monitor di connessione per un'origine e una destinazione specificate.</span><span class="sxs-lookup"><span data-stu-id="9dddc-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="9dddc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9dddc-110">EXAMPLES</span></span>

### <span data-ttu-id="9dddc-111">Esempio 1: creare un monitor di connessione per una VM e una destinazione Internet</span><span class="sxs-lookup"><span data-stu-id="9dddc-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
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

<span data-ttu-id="9dddc-112">Il cmdlet New-AzureRmNetworkWatcherConnectionMonitor crea un monitor di connessione per un'origine e una destinazione specificate.</span><span class="sxs-lookup"><span data-stu-id="9dddc-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="9dddc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9dddc-113">PARAMETERS</span></span>

### <span data-ttu-id="9dddc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dddc-114">-AsJob</span></span>
<span data-ttu-id="9dddc-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9dddc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dddc-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9dddc-116">-Confirm</span></span>
<span data-ttu-id="9dddc-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dddc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dddc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dddc-118">-DefaultProfile</span></span>
<span data-ttu-id="9dddc-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9dddc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dddc-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="9dddc-120">-DestinationAddress</span></span>
<span data-ttu-id="9dddc-121">Indirizzo IP della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="9dddc-121">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="9dddc-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="9dddc-122">-DestinationPort</span></span>
<span data-ttu-id="9dddc-123">Porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9dddc-123">Destination port.</span></span>

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

### <span data-ttu-id="9dddc-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="9dddc-124">-DestinationResourceId</span></span>
<span data-ttu-id="9dddc-125">ID della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="9dddc-125">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="9dddc-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9dddc-126">-Force</span></span>
<span data-ttu-id="9dddc-127">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="9dddc-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9dddc-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9dddc-128">-Location</span></span>
<span data-ttu-id="9dddc-129">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="9dddc-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9dddc-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9dddc-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="9dddc-131">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="9dddc-131">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="9dddc-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="9dddc-132">-Name</span></span>
<span data-ttu-id="9dddc-133">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="9dddc-133">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddc-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dddc-134">-NetworkWatcher</span></span>
<span data-ttu-id="9dddc-135">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="9dddc-135">The network watcher resource.</span></span>

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

### <span data-ttu-id="9dddc-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9dddc-136">-NetworkWatcherName</span></span>
<span data-ttu-id="9dddc-137">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="9dddc-137">The name of network watcher.</span></span>

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

### <span data-ttu-id="9dddc-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dddc-138">-ResourceGroupName</span></span>
<span data-ttu-id="9dddc-139">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="9dddc-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9dddc-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="9dddc-140">-SourcePort</span></span>
<span data-ttu-id="9dddc-141">Porta di origine.</span><span class="sxs-lookup"><span data-stu-id="9dddc-141">Source port.</span></span>

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

### <span data-ttu-id="9dddc-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="9dddc-142">-SourceResourceId</span></span>
<span data-ttu-id="9dddc-143">ID dell'origine del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="9dddc-143">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dddc-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="9dddc-144">-Tag</span></span>
<span data-ttu-id="9dddc-145">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9dddc-145">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9dddc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dddc-146">-WhatIf</span></span>
<span data-ttu-id="9dddc-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9dddc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dddc-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9dddc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dddc-149">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="9dddc-149">-ConfigureOnly</span></span>
<span data-ttu-id="9dddc-150">Configurare monitor di connessione, ma non avviarlo</span><span class="sxs-lookup"><span data-stu-id="9dddc-150">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="9dddc-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dddc-151">CommonParameters</span></span>
<span data-ttu-id="9dddc-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dddc-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9dddc-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dddc-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dddc-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9dddc-154">INPUTS</span></span>

### <span data-ttu-id="9dddc-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dddc-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="9dddc-156">System. String</span><span class="sxs-lookup"><span data-stu-id="9dddc-156">System.String</span></span>

## <span data-ttu-id="9dddc-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9dddc-157">OUTPUTS</span></span>

### <span data-ttu-id="9dddc-158">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="9dddc-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="9dddc-159">Note</span><span class="sxs-lookup"><span data-stu-id="9dddc-159">NOTES</span></span>
<span data-ttu-id="9dddc-160">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="9dddc-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="9dddc-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9dddc-161">RELATED LINKS</span></span>

[<span data-ttu-id="9dddc-162">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dddc-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="9dddc-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dddc-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="9dddc-164">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9dddc-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="9dddc-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9dddc-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="9dddc-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9dddc-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="9dddc-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9dddc-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="9dddc-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9dddc-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="9dddc-169">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dddc-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9dddc-170">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9dddc-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="9dddc-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dddc-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9dddc-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dddc-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9dddc-173">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9dddc-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="9dddc-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dddc-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9dddc-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9dddc-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="9dddc-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dddc-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9dddc-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dddc-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9dddc-178">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dddc-178">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="9dddc-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9dddc-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
