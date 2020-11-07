---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 3e5853d99157fef87c2f02c2be9fab7bb983d1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866472"
---
# <span data-ttu-id="ad370-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ad370-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="ad370-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad370-102">SYNOPSIS</span></span>
<span data-ttu-id="ad370-103">Crea un monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="ad370-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad370-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad370-104">SYNTAX</span></span>

### <span data-ttu-id="ad370-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad370-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ad370-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ad370-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ad370-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ad370-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ad370-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad370-108">DESCRIPTION</span></span>
<span data-ttu-id="ad370-109">Il cmdlet New-AzureRmNetworkWatcherConnectionMonitor rcreates un monitor di connessione per un'origine e una destinazione specificate.</span><span class="sxs-lookup"><span data-stu-id="ad370-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="ad370-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad370-110">EXAMPLES</span></span>

### <span data-ttu-id="ad370-111">---------------Esempio 1: creare un monitor di connessione per una VM e una destinazione Internet---------------</span><span class="sxs-lookup"><span data-stu-id="ad370-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
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

<span data-ttu-id="ad370-112">Il cmdlet New-AzureRmNetworkWatcherConnectionMonitor crea un monitor di connessione per un'origine e una destinazione specificate.</span><span class="sxs-lookup"><span data-stu-id="ad370-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="ad370-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad370-113">PARAMETERS</span></span>

### <span data-ttu-id="ad370-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad370-114">-AsJob</span></span>
<span data-ttu-id="ad370-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ad370-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad370-116">-Autostart</span><span class="sxs-lookup"><span data-stu-id="ad370-116">-AutoStart</span></span>
<span data-ttu-id="ad370-117">Avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="ad370-117">Auto start.</span></span>

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

### <span data-ttu-id="ad370-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad370-118">-Confirm</span></span>
<span data-ttu-id="ad370-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad370-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad370-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad370-120">-DefaultProfile</span></span>
<span data-ttu-id="ad370-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad370-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad370-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ad370-122">-DestinationAddress</span></span>
<span data-ttu-id="ad370-123">Indirizzo IP della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="ad370-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="ad370-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ad370-124">-DestinationPort</span></span>
<span data-ttu-id="ad370-125">Porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ad370-125">Destination port.</span></span>

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

### <span data-ttu-id="ad370-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="ad370-126">-DestinationResourceId</span></span>
<span data-ttu-id="ad370-127">ID della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="ad370-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="ad370-128">-Force</span><span class="sxs-lookup"><span data-stu-id="ad370-128">-Force</span></span>
<span data-ttu-id="ad370-129">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="ad370-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ad370-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ad370-130">-Location</span></span>
<span data-ttu-id="ad370-131">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="ad370-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ad370-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ad370-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="ad370-133">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="ad370-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="ad370-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad370-134">-Name</span></span>
<span data-ttu-id="ad370-135">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="ad370-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="ad370-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ad370-136">-NetworkWatcher</span></span>
<span data-ttu-id="ad370-137">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="ad370-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="ad370-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ad370-138">-NetworkWatcherName</span></span>
<span data-ttu-id="ad370-139">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="ad370-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="ad370-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad370-140">-ResourceGroupName</span></span>
<span data-ttu-id="ad370-141">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="ad370-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ad370-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="ad370-142">-SourcePort</span></span>
<span data-ttu-id="ad370-143">Porta di origine.</span><span class="sxs-lookup"><span data-stu-id="ad370-143">Source port.</span></span>

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

### <span data-ttu-id="ad370-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="ad370-144">-SourceResourceId</span></span>
<span data-ttu-id="ad370-145">ID dell'origine del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="ad370-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="ad370-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad370-146">-Tag</span></span>
<span data-ttu-id="ad370-147">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="ad370-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ad370-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad370-148">-WhatIf</span></span>
<span data-ttu-id="ad370-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad370-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad370-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad370-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="ad370-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad370-151">INPUTS</span></span>

### <span data-ttu-id="ad370-152">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ad370-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ad370-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ad370-153">System.String</span></span>


## <span data-ttu-id="ad370-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad370-154">OUTPUTS</span></span>

### <span data-ttu-id="ad370-155">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="ad370-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="ad370-156">Note</span><span class="sxs-lookup"><span data-stu-id="ad370-156">NOTES</span></span>
<span data-ttu-id="ad370-157">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="ad370-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="ad370-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad370-158">RELATED LINKS</span></span>
<span data-ttu-id="ad370-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="ad370-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="ad370-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="ad370-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="ad370-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="ad370-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="ad370-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="ad370-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
