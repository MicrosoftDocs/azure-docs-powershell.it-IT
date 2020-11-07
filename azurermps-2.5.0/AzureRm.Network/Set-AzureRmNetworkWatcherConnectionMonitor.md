---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
ms.openlocfilehash: e8ebbf4a554ef3dcb13726839ee8b7ebb330bad8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866223"
---
# <span data-ttu-id="df703-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="df703-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="df703-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df703-102">SYNOPSIS</span></span>
<span data-ttu-id="df703-103">Aggiornare un monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="df703-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df703-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df703-104">SYNTAX</span></span>

### <span data-ttu-id="df703-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="df703-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="df703-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="df703-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="df703-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="df703-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="df703-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="df703-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="df703-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="df703-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="df703-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df703-110">DESCRIPTION</span></span>
<span data-ttu-id="df703-111">Il cmdlet Set-AzureRmNetworkWatcherConnectionMonitor aggiorna il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="df703-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="df703-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df703-112">EXAMPLES</span></span>

### <span data-ttu-id="df703-113">---------------Esempio 1: aggiornare un monitor di connessione---------------</span><span class="sxs-lookup"><span data-stu-id="df703-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
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

<span data-ttu-id="df703-114">In questo esempio aggiorniamo il monitor di connessione esistente modificando destinationAddress e aggiungendo i tag.</span><span class="sxs-lookup"><span data-stu-id="df703-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="df703-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df703-115">PARAMETERS</span></span>

### <span data-ttu-id="df703-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df703-116">-AsJob</span></span>
<span data-ttu-id="df703-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="df703-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df703-118">-Autostart</span><span class="sxs-lookup"><span data-stu-id="df703-118">-AutoStart</span></span>
<span data-ttu-id="df703-119">Avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="df703-119">Auto start.</span></span>

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

### <span data-ttu-id="df703-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="df703-120">-Confirm</span></span>
<span data-ttu-id="df703-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df703-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df703-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df703-122">-DefaultProfile</span></span>
<span data-ttu-id="df703-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df703-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df703-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="df703-124">-DestinationAddress</span></span>
<span data-ttu-id="df703-125">Indirizzo IP della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="df703-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="df703-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="df703-126">-DestinationPort</span></span>
<span data-ttu-id="df703-127">Porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df703-127">Destination port.</span></span>

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

### <span data-ttu-id="df703-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="df703-128">-DestinationResourceId</span></span>
<span data-ttu-id="df703-129">ID della destinazione del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="df703-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="df703-130">-Force</span><span class="sxs-lookup"><span data-stu-id="df703-130">-Force</span></span>
<span data-ttu-id="df703-131">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="df703-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="df703-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df703-132">-InputObject</span></span>
<span data-ttu-id="df703-133">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="df703-133">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df703-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="df703-134">-Location</span></span>
<span data-ttu-id="df703-135">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="df703-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="df703-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="df703-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="df703-137">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="df703-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="df703-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="df703-138">-Name</span></span>
<span data-ttu-id="df703-139">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="df703-139">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df703-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="df703-140">-NetworkWatcher</span></span>
<span data-ttu-id="df703-141">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="df703-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="df703-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="df703-142">-NetworkWatcherName</span></span>
<span data-ttu-id="df703-143">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="df703-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="df703-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df703-144">-ResourceGroupName</span></span>
<span data-ttu-id="df703-145">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="df703-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="df703-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df703-146">-ResourceId</span></span>
<span data-ttu-id="df703-147">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="df703-147">Resource ID.</span></span>

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

### <span data-ttu-id="df703-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="df703-148">-SourcePort</span></span>
<span data-ttu-id="df703-149">Porta di origine.</span><span class="sxs-lookup"><span data-stu-id="df703-149">Source port.</span></span>

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

### <span data-ttu-id="df703-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="df703-150">-SourceResourceId</span></span>
<span data-ttu-id="df703-151">ID dell'origine del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="df703-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="df703-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="df703-152">-Tag</span></span>
<span data-ttu-id="df703-153">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="df703-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="df703-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df703-154">-WhatIf</span></span>
<span data-ttu-id="df703-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df703-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df703-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df703-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="df703-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df703-157">INPUTS</span></span>

### <span data-ttu-id="df703-158">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="df703-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="df703-159">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="df703-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="df703-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df703-160">OUTPUTS</span></span>

### <span data-ttu-id="df703-161">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="df703-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="df703-162">Note</span><span class="sxs-lookup"><span data-stu-id="df703-162">NOTES</span></span>
<span data-ttu-id="df703-163">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="df703-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="df703-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df703-164">RELATED LINKS</span></span>
<span data-ttu-id="df703-165">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="df703-165">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="df703-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="df703-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="df703-167">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="df703-167">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="df703-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="df703-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>

