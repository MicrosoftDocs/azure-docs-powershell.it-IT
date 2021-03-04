---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
ms.openlocfilehash: 78de7eb3e8adbda34e53b5a74036a047ddcd4a1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958510"
---
# <span data-ttu-id="b33b1-101">New-AzNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="b33b1-101">New-AzNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="b33b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b33b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b33b1-103">Creare un oggetto Monitor connessione V2.</span><span class="sxs-lookup"><span data-stu-id="b33b1-103">Create a connection monitor V2 object.</span></span>

## <span data-ttu-id="b33b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b33b1-104">SYNTAX</span></span>

### <span data-ttu-id="b33b1-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b33b1-105">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b33b1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b33b1-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b33b1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b33b1-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b33b1-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b33b1-108">DESCRIPTION</span></span>
<span data-ttu-id="b33b1-109">Il cmdlet New-AzNetworkWatcherConnectionMonitorObject crea un oggetto Monitor connessione V2.</span><span class="sxs-lookup"><span data-stu-id="b33b1-109">The New-AzNetworkWatcherConnectionMonitorObject cmdlet creates a connection monitor V2 object.</span></span>

## <span data-ttu-id="b33b1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b33b1-110">EXAMPLES</span></span>

### <span data-ttu-id="b33b1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b33b1-111">Example 1</span></span>
```powershell
PS> $cmtest = New-AzNetworkWatcherConnectionMonitorObject -Location westcentralus -Name cmV2test -TestGroup $testGroup1, $testGroup2 -Tag @{"name" = "value"}
PS> $cmtest
```

<span data-ttu-id="b33b1-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName : NetworkWatcherRG Name : cmV2test TestGroups : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs : null Notes : Tags : { "name": "value" }</span><span class="sxs-lookup"><span data-stu-id="b33b1-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName  : NetworkWatcherRG Name               : cmV2test TestGroups         : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs            : null Notes              : Tags               : { "name": "value" }</span></span>
        
   

## <span data-ttu-id="b33b1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b33b1-113">PARAMETERS</span></span>

### <span data-ttu-id="b33b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b33b1-114">-DefaultProfile</span></span>
<span data-ttu-id="b33b1-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b33b1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b33b1-116">-Location</span><span class="sxs-lookup"><span data-stu-id="b33b1-116">-Location</span></span>
<span data-ttu-id="b33b1-117">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="b33b1-117">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b33b1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b33b1-118">-Name</span></span>
<span data-ttu-id="b33b1-119">Nome del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="b33b1-119">The connection monitor name.</span></span>

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

### <span data-ttu-id="b33b1-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b33b1-120">-NetworkWatcher</span></span>
<span data-ttu-id="b33b1-121">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="b33b1-121">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b33b1-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b33b1-122">-NetworkWatcherName</span></span>
<span data-ttu-id="b33b1-123">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="b33b1-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="b33b1-124">-Nota</span><span class="sxs-lookup"><span data-stu-id="b33b1-124">-Note</span></span>
<span data-ttu-id="b33b1-125">Note associate al monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="b33b1-125">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="b33b1-126">-Output</span><span class="sxs-lookup"><span data-stu-id="b33b1-126">-Output</span></span>
<span data-ttu-id="b33b1-127">Descrive le destinazioni di output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="b33b1-127">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b33b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b33b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="b33b1-129">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="b33b1-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b33b1-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="b33b1-130">-Tag</span></span>
<span data-ttu-id="b33b1-131">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b33b1-131">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b33b1-132">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="b33b1-132">-TestGroup</span></span>
<span data-ttu-id="b33b1-133">Elenco dei gruppi di test.</span><span class="sxs-lookup"><span data-stu-id="b33b1-133">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b33b1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b33b1-134">-Confirm</span></span>
<span data-ttu-id="b33b1-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b33b1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b33b1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b33b1-136">-WhatIf</span></span>
<span data-ttu-id="b33b1-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b33b1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b33b1-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b33b1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b33b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b33b1-139">CommonParameters</span></span>
<span data-ttu-id="b33b1-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b33b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b33b1-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b33b1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b33b1-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="b33b1-142">INPUTS</span></span>

### <span data-ttu-id="b33b1-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b33b1-143">None</span></span>

## <span data-ttu-id="b33b1-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b33b1-144">OUTPUTS</span></span>

### <span data-ttu-id="b33b1-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="b33b1-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="b33b1-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="b33b1-146">NOTES</span></span>

## <span data-ttu-id="b33b1-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b33b1-147">RELATED LINKS</span></span>
