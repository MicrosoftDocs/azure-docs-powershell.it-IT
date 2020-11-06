---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: e49245fabd4387c48def797168e1d572a43d6bfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512472"
---
# <span data-ttu-id="3f58d-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3f58d-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="3f58d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f58d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f58d-103">Arrestare un monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="3f58d-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f58d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f58d-104">SYNTAX</span></span>

### <span data-ttu-id="3f58d-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3f58d-105">SetByName (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f58d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3f58d-106">SetByResource</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f58d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3f58d-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f58d-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f58d-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f58d-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="3f58d-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f58d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f58d-110">DESCRIPTION</span></span>
<span data-ttu-id="3f58d-111">Il cmdlet Stop-AzureRmNetworkWatcherConnectionMonitor arresta il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="3f58d-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="3f58d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f58d-112">EXAMPLES</span></span>

### <span data-ttu-id="3f58d-113">Esempio 1: arrestare un monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="3f58d-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="3f58d-114">In questo esempio interrompiamo il monitoraggio delle connessioni specificato per nome e Network Watcher</span><span class="sxs-lookup"><span data-stu-id="3f58d-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="3f58d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f58d-115">PARAMETERS</span></span>

### <span data-ttu-id="3f58d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f58d-116">-AsJob</span></span>
<span data-ttu-id="3f58d-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3f58d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f58d-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3f58d-118">-Confirm</span></span>
<span data-ttu-id="3f58d-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f58d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f58d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f58d-120">-DefaultProfile</span></span>
<span data-ttu-id="3f58d-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f58d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f58d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f58d-122">-InputObject</span></span>
<span data-ttu-id="3f58d-123">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="3f58d-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="3f58d-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3f58d-124">-Location</span></span>
<span data-ttu-id="3f58d-125">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="3f58d-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3f58d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f58d-126">-Name</span></span>
<span data-ttu-id="3f58d-127">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="3f58d-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="3f58d-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3f58d-128">-NetworkWatcher</span></span>
<span data-ttu-id="3f58d-129">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="3f58d-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="3f58d-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3f58d-130">-NetworkWatcherName</span></span>
<span data-ttu-id="3f58d-131">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="3f58d-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="3f58d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f58d-132">-PassThru</span></span>
<span data-ttu-id="3f58d-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3f58d-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3f58d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f58d-134">-ResourceGroupName</span></span>
<span data-ttu-id="3f58d-135">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="3f58d-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3f58d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f58d-136">-ResourceId</span></span>
<span data-ttu-id="3f58d-137">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3f58d-137">Resource ID.</span></span>

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

### <span data-ttu-id="3f58d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f58d-138">-WhatIf</span></span>
<span data-ttu-id="3f58d-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f58d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f58d-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f58d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f58d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f58d-141">CommonParameters</span></span>
<span data-ttu-id="3f58d-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f58d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3f58d-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f58d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f58d-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f58d-144">INPUTS</span></span>

### <span data-ttu-id="3f58d-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3f58d-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3f58d-146">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="3f58d-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="3f58d-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f58d-147">OUTPUTS</span></span>

### <span data-ttu-id="3f58d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f58d-148">System.Boolean</span></span>

## <span data-ttu-id="3f58d-149">Note</span><span class="sxs-lookup"><span data-stu-id="3f58d-149">NOTES</span></span>
<span data-ttu-id="3f58d-150">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="3f58d-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="3f58d-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f58d-151">RELATED LINKS</span></span>

[<span data-ttu-id="3f58d-152">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3f58d-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="3f58d-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3f58d-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="3f58d-154">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3f58d-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="3f58d-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3f58d-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="3f58d-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3f58d-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="3f58d-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3f58d-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="3f58d-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3f58d-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="3f58d-159">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3f58d-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3f58d-160">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3f58d-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="3f58d-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3f58d-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3f58d-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3f58d-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3f58d-163">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3f58d-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="3f58d-164">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3f58d-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3f58d-165">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3f58d-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3f58d-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3f58d-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="3f58d-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3f58d-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3f58d-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3f58d-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="3f58d-169">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3f58d-169">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
