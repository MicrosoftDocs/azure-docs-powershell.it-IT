---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
ms.openlocfilehash: 06c20432821336b57764d70b5747759b7517801f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301441"
---
# <span data-ttu-id="ce87a-101">New-AzNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="ce87a-101">New-AzNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="ce87a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce87a-102">SYNOPSIS</span></span>
<span data-ttu-id="ce87a-103">Creare un oggetto di monitor di connessione V2.</span><span class="sxs-lookup"><span data-stu-id="ce87a-103">Create a connection monitor V2 object.</span></span>

## <span data-ttu-id="ce87a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce87a-104">SYNTAX</span></span>

### <span data-ttu-id="ce87a-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ce87a-105">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce87a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ce87a-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce87a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ce87a-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce87a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce87a-108">DESCRIPTION</span></span>
<span data-ttu-id="ce87a-109">Il cmdlet New-AzNetworkWatcherConnectionMonitorObject crea un oggetto di monitor di connessione V2.</span><span class="sxs-lookup"><span data-stu-id="ce87a-109">The New-AzNetworkWatcherConnectionMonitorObject cmdlet creates a connection monitor V2 object.</span></span>

## <span data-ttu-id="ce87a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce87a-110">EXAMPLES</span></span>

### <span data-ttu-id="ce87a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce87a-111">Example 1</span></span>
```powershell
PS> $cmtest = New-AzNetworkWatcherConnectionMonitorObject -Location westcentralus -Name cmV2test -TestGroup $testGroup1, $testGroup2 -Tag @{"name" = "value"}
PS> $cmtest
```

<span data-ttu-id="ce87a-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName : NetworkWatcherRG Name : cmV2test TestGroups : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs : null Notes : Tags : { "name": "value" }</span><span class="sxs-lookup"><span data-stu-id="ce87a-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName  : NetworkWatcherRG Name               : cmV2test TestGroups         : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs            : null Notes              : Tags               : { "name": "value" }</span></span>
        
   

## <span data-ttu-id="ce87a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce87a-113">PARAMETERS</span></span>

### <span data-ttu-id="ce87a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce87a-114">-DefaultProfile</span></span>
<span data-ttu-id="ce87a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce87a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce87a-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ce87a-116">-Location</span></span>
<span data-ttu-id="ce87a-117">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="ce87a-117">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ce87a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce87a-118">-Name</span></span>
<span data-ttu-id="ce87a-119">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="ce87a-119">The connection monitor name.</span></span>

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

### <span data-ttu-id="ce87a-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ce87a-120">-NetworkWatcher</span></span>
<span data-ttu-id="ce87a-121">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="ce87a-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="ce87a-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ce87a-122">-NetworkWatcherName</span></span>
<span data-ttu-id="ce87a-123">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="ce87a-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="ce87a-124">-Nota</span><span class="sxs-lookup"><span data-stu-id="ce87a-124">-Note</span></span>
<span data-ttu-id="ce87a-125">Note associate al monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="ce87a-125">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="ce87a-126">-Output</span><span class="sxs-lookup"><span data-stu-id="ce87a-126">-Output</span></span>
<span data-ttu-id="ce87a-127">Descrive le destinazioni di output di monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="ce87a-127">Describes a connection monitor output destinations.</span></span>

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

### <span data-ttu-id="ce87a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce87a-128">-ResourceGroupName</span></span>
<span data-ttu-id="ce87a-129">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="ce87a-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ce87a-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce87a-130">-Tag</span></span>
<span data-ttu-id="ce87a-131">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="ce87a-131">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ce87a-132">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="ce87a-132">-TestGroup</span></span>
<span data-ttu-id="ce87a-133">Elenco di gruppi di test.</span><span class="sxs-lookup"><span data-stu-id="ce87a-133">The list of test groups.</span></span>

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

### <span data-ttu-id="ce87a-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce87a-134">-Confirm</span></span>
<span data-ttu-id="ce87a-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce87a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce87a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce87a-136">-WhatIf</span></span>
<span data-ttu-id="ce87a-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce87a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce87a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce87a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce87a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce87a-139">CommonParameters</span></span>
<span data-ttu-id="ce87a-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce87a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce87a-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce87a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce87a-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce87a-142">INPUTS</span></span>

### <span data-ttu-id="ce87a-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ce87a-143">None</span></span>

## <span data-ttu-id="ce87a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce87a-144">OUTPUTS</span></span>

### <span data-ttu-id="ce87a-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="ce87a-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="ce87a-146">Note</span><span class="sxs-lookup"><span data-stu-id="ce87a-146">NOTES</span></span>

## <span data-ttu-id="ce87a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce87a-147">RELATED LINKS</span></span>
