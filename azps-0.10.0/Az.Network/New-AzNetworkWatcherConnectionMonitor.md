---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: bfdcfbf57f44479ad35a2b9075590a0d40351ec9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860449"
---
# <span data-ttu-id="e3725-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e3725-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="e3725-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3725-102">SYNOPSIS</span></span>
<span data-ttu-id="e3725-103">Crea un monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="e3725-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="e3725-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3725-104">SYNTAX</span></span>

### <span data-ttu-id="e3725-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3725-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e3725-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e3725-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e3725-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e3725-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e3725-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3725-108">DESCRIPTION</span></span>
<span data-ttu-id="e3725-109">Il cmdlet New-AzNetworkWatcherConnectionMonitor rcreates un monitor di connessione per un'origine e una destinazione specificate.</span><span class="sxs-lookup"><span data-stu-id="e3725-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="e3725-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3725-110">EXAMPLES</span></span>

### <span data-ttu-id="e3725-111">---------------Esempio 1: creare un monitor di connessione per una VM e una destinazione Internet---------------</span><span class="sxs-lookup"><span data-stu-id="e3725-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="e3725-112">Il cmdlet New-AzNetworkWatcherConnectionMonitor crea un monitor di connessione per un'origine e una destinazione specificate.</span><span class="sxs-lookup"><span data-stu-id="e3725-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="e3725-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3725-113">PARAMETERS</span></span>

### <span data-ttu-id="e3725-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3725-114">-AsJob</span></span>
<span data-ttu-id="e3725-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e3725-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3725-116">-Autostart</span><span class="sxs-lookup"><span data-stu-id="e3725-116">-AutoStart</span></span>
<span data-ttu-id="e3725-117">Avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="e3725-117">Auto start.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3725-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3725-118">-Confirm</span></span>
<span data-ttu-id="e3725-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3725-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3725-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3725-120">-DefaultProfile</span></span>
<span data-ttu-id="e3725-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3725-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3725-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e3725-122">-DestinationAddress</span></span>
<span data-ttu-id="e3725-123">Indirizzo IP della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="e3725-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="e3725-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e3725-124">-DestinationPort</span></span>
<span data-ttu-id="e3725-125">Porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e3725-125">Destination port.</span></span>

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

### <span data-ttu-id="e3725-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="e3725-126">-DestinationResourceId</span></span>
<span data-ttu-id="e3725-127">ID della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="e3725-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="e3725-128">-Force</span><span class="sxs-lookup"><span data-stu-id="e3725-128">-Force</span></span>
<span data-ttu-id="e3725-129">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="e3725-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e3725-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e3725-130">-Location</span></span>
<span data-ttu-id="e3725-131">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="e3725-131">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3725-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e3725-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="e3725-133">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="e3725-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="e3725-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3725-134">-Name</span></span>
<span data-ttu-id="e3725-135">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="e3725-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3725-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3725-136">-NetworkWatcher</span></span>
<span data-ttu-id="e3725-137">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="e3725-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="e3725-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e3725-138">-NetworkWatcherName</span></span>
<span data-ttu-id="e3725-139">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="e3725-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="e3725-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3725-140">-ResourceGroupName</span></span>
<span data-ttu-id="e3725-141">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="e3725-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e3725-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="e3725-142">-SourcePort</span></span>
<span data-ttu-id="e3725-143">Porta di origine.</span><span class="sxs-lookup"><span data-stu-id="e3725-143">Source port.</span></span>

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

### <span data-ttu-id="e3725-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e3725-144">-SourceResourceId</span></span>
<span data-ttu-id="e3725-145">ID dell'origine del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="e3725-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="e3725-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3725-146">-Tag</span></span>
<span data-ttu-id="e3725-147">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e3725-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e3725-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3725-148">-WhatIf</span></span>
<span data-ttu-id="e3725-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3725-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3725-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3725-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e3725-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3725-151">INPUTS</span></span>

### <span data-ttu-id="e3725-152">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e3725-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e3725-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e3725-153">System.String</span></span>


## <span data-ttu-id="e3725-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3725-154">OUTPUTS</span></span>

### <span data-ttu-id="e3725-155">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="e3725-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="e3725-156">Note</span><span class="sxs-lookup"><span data-stu-id="e3725-156">NOTES</span></span>
<span data-ttu-id="e3725-157">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="e3725-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="e3725-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3725-158">RELATED LINKS</span></span>
<span data-ttu-id="e3725-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="e3725-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="e3725-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="e3725-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="e3725-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="e3725-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="e3725-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="e3725-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span></span>
