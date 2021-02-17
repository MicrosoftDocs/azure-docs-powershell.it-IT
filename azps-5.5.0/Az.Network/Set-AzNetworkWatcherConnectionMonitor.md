---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184183"
---
# <span data-ttu-id="94127-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94127-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="94127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94127-102">SYNOPSIS</span></span>
<span data-ttu-id="94127-103">Aggiorna la risorsa di Monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="94127-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="94127-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94127-104">SYNTAX</span></span>

### <span data-ttu-id="94127-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94127-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94127-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="94127-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94127-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="94127-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94127-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="94127-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94127-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="94127-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94127-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="94127-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94127-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="94127-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94127-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="94127-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94127-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="94127-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94127-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94127-114">DESCRIPTION</span></span>
<span data-ttu-id="94127-115">Il Set-AzNetworkWatcherConnectionMonitor cmdlet aggiorna la risorsa di Monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="94127-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="94127-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94127-116">EXAMPLES</span></span>

### <span data-ttu-id="94127-117">Esempio 1: Aggiornare un monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="94127-117">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
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

<span data-ttu-id="94127-118">In questo esempio il monitor di connessione esistente viene aggiornato modificando destinationAddress e aggiungendo tag.</span><span class="sxs-lookup"><span data-stu-id="94127-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="94127-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94127-119">PARAMETERS</span></span>

### <span data-ttu-id="94127-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94127-120">-AsJob</span></span>
<span data-ttu-id="94127-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="94127-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94127-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="94127-122">-ConfigureOnly</span></span>
<span data-ttu-id="94127-123">Configurare il monitor di connessione, ma non avviarlo</span><span class="sxs-lookup"><span data-stu-id="94127-123">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94127-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94127-124">-DefaultProfile</span></span>
<span data-ttu-id="94127-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94127-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94127-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="94127-126">-DestinationAddress</span></span>
<span data-ttu-id="94127-127">Indirizzo della destinazione del monitor di connessione (IP o nome di dominio).</span><span class="sxs-lookup"><span data-stu-id="94127-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94127-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="94127-128">-DestinationPort</span></span>
<span data-ttu-id="94127-129">Porta di destinazione utilizzata dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="94127-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94127-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="94127-130">-DestinationResourceId</span></span>
<span data-ttu-id="94127-131">ID della risorsa usata come destinazione dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="94127-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94127-132">-Force</span><span class="sxs-lookup"><span data-stu-id="94127-132">-Force</span></span>
<span data-ttu-id="94127-133">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="94127-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="94127-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94127-134">-InputObject</span></span>
<span data-ttu-id="94127-135">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="94127-135">Connection monitor object.</span></span>

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

### <span data-ttu-id="94127-136">-Location</span><span class="sxs-lookup"><span data-stu-id="94127-136">-Location</span></span>
<span data-ttu-id="94127-137">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="94127-137">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94127-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="94127-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="94127-139">Intervallo di monitoraggio in secondi.</span><span class="sxs-lookup"><span data-stu-id="94127-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="94127-140">Il valore predefinito è 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="94127-140">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94127-141">-Name</span><span class="sxs-lookup"><span data-stu-id="94127-141">-Name</span></span>
<span data-ttu-id="94127-142">Nome del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="94127-142">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94127-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="94127-143">-NetworkWatcher</span></span>
<span data-ttu-id="94127-144">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="94127-144">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94127-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="94127-145">-NetworkWatcherName</span></span>
<span data-ttu-id="94127-146">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="94127-146">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94127-147">-Nota</span><span class="sxs-lookup"><span data-stu-id="94127-147">-Note</span></span>
<span data-ttu-id="94127-148">Note associate al monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="94127-148">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94127-149">-Output</span><span class="sxs-lookup"><span data-stu-id="94127-149">-Output</span></span>
<span data-ttu-id="94127-150">Descrive le destinazioni di output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="94127-150">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94127-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94127-151">-ResourceGroupName</span></span>
<span data-ttu-id="94127-152">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="94127-152">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94127-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94127-153">-ResourceId</span></span>
<span data-ttu-id="94127-154">ID risorsa ConnectionMonitor.</span><span class="sxs-lookup"><span data-stu-id="94127-154">ConnectionMonitor resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94127-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="94127-155">-SourcePort</span></span>
<span data-ttu-id="94127-156">La porta di origine usata dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="94127-156">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94127-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="94127-157">-SourceResourceId</span></span>
<span data-ttu-id="94127-158">ID della risorsa usata come origine dal monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="94127-158">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94127-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="94127-159">-Tag</span></span>
<span data-ttu-id="94127-160">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="94127-160">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94127-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="94127-161">-TestGroup</span></span>
<span data-ttu-id="94127-162">Elenco dei gruppi di test.</span><span class="sxs-lookup"><span data-stu-id="94127-162">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94127-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94127-163">-Confirm</span></span>
<span data-ttu-id="94127-164">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94127-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94127-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94127-165">-WhatIf</span></span>
<span data-ttu-id="94127-166">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94127-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94127-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94127-167">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94127-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94127-168">CommonParameters</span></span>
<span data-ttu-id="94127-169">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94127-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94127-170">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94127-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94127-171">INPUT</span><span class="sxs-lookup"><span data-stu-id="94127-171">INPUTS</span></span>

### <span data-ttu-id="94127-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="94127-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="94127-173">System.String</span><span class="sxs-lookup"><span data-stu-id="94127-173">System.String</span></span>

### <span data-ttu-id="94127-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="94127-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="94127-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94127-175">OUTPUTS</span></span>

### <span data-ttu-id="94127-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="94127-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="94127-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="94127-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="94127-178">NOTE</span><span class="sxs-lookup"><span data-stu-id="94127-178">NOTES</span></span>

## <span data-ttu-id="94127-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94127-179">RELATED LINKS</span></span>
