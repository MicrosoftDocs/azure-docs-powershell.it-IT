---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 01e8a41c8d8854527037c447545f3d0601d4daf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687794"
---
# <span data-ttu-id="c7b24-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b24-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="c7b24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7b24-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b24-103">Rimuovi monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="c7b24-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7b24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7b24-104">SYNTAX</span></span>

### <span data-ttu-id="c7b24-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7b24-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7b24-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c7b24-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b24-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c7b24-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b24-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b24-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7b24-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="c7b24-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7b24-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7b24-110">DESCRIPTION</span></span>
<span data-ttu-id="c7b24-111">Il cmdlet Remove-AzureRmNetworkWatcherConnectionMonitor rimuove il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="c7b24-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="c7b24-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7b24-112">EXAMPLES</span></span>

### <span data-ttu-id="c7b24-113">Esempio 1: rimuovere il monitor di connessione specificato</span><span class="sxs-lookup"><span data-stu-id="c7b24-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="c7b24-114">In questo esempio eliminiamo il monitor di connessione specificato da location e Name.</span><span class="sxs-lookup"><span data-stu-id="c7b24-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="c7b24-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7b24-115">PARAMETERS</span></span>

### <span data-ttu-id="c7b24-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7b24-116">-AsJob</span></span>
<span data-ttu-id="c7b24-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c7b24-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7b24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b24-118">-DefaultProfile</span></span>
<span data-ttu-id="c7b24-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7b24-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7b24-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7b24-120">-InputObject</span></span>
<span data-ttu-id="c7b24-121">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="c7b24-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="c7b24-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c7b24-122">-Location</span></span>
<span data-ttu-id="c7b24-123">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="c7b24-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c7b24-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7b24-124">-Name</span></span>
<span data-ttu-id="c7b24-125">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="c7b24-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="c7b24-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7b24-126">-NetworkWatcher</span></span>
<span data-ttu-id="c7b24-127">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="c7b24-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="c7b24-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c7b24-128">-NetworkWatcherName</span></span>
<span data-ttu-id="c7b24-129">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="c7b24-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="c7b24-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7b24-130">-PassThru</span></span>
<span data-ttu-id="c7b24-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c7b24-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c7b24-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7b24-132">-ResourceGroupName</span></span>
<span data-ttu-id="c7b24-133">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="c7b24-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c7b24-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b24-134">-ResourceId</span></span>
<span data-ttu-id="c7b24-135">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c7b24-135">Resource ID.</span></span>

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

### <span data-ttu-id="c7b24-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c7b24-136">-Confirm</span></span>
<span data-ttu-id="c7b24-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7b24-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7b24-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7b24-138">-WhatIf</span></span>
<span data-ttu-id="c7b24-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7b24-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7b24-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7b24-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7b24-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b24-141">CommonParameters</span></span>
<span data-ttu-id="c7b24-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b24-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b24-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7b24-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b24-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7b24-144">INPUTS</span></span>

### <span data-ttu-id="c7b24-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7b24-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c7b24-146">Parametri: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7b24-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="c7b24-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c7b24-147">System.String</span></span>

### <span data-ttu-id="c7b24-148">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="c7b24-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="c7b24-149">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7b24-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c7b24-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7b24-150">OUTPUTS</span></span>

### <span data-ttu-id="c7b24-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7b24-151">System.Boolean</span></span>

## <span data-ttu-id="c7b24-152">Note</span><span class="sxs-lookup"><span data-stu-id="c7b24-152">NOTES</span></span>
<span data-ttu-id="c7b24-153">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="c7b24-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="c7b24-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7b24-154">RELATED LINKS</span></span>

[<span data-ttu-id="c7b24-155">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7b24-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="c7b24-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7b24-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="c7b24-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c7b24-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="c7b24-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c7b24-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="c7b24-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c7b24-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="c7b24-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c7b24-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="c7b24-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c7b24-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="c7b24-162">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7b24-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c7b24-163">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c7b24-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="c7b24-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7b24-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c7b24-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7b24-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c7b24-166">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c7b24-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="c7b24-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b24-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c7b24-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c7b24-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="c7b24-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b24-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c7b24-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b24-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c7b24-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b24-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c7b24-172">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b24-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c7b24-173">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7b24-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="c7b24-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c7b24-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="c7b24-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c7b24-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="c7b24-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c7b24-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="c7b24-177">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c7b24-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="c7b24-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c7b24-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="c7b24-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c7b24-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="c7b24-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c7b24-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="c7b24-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c7b24-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
