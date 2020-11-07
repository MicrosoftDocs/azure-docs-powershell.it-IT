---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 10582a0e81fdb9c86902c7a2580ad31fe84f3bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687642"
---
# <span data-ttu-id="bcdcb-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcdcb-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="bcdcb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcdcb-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdcb-103">Rimuovi monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcdcb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcdcb-104">SYNTAX</span></span>

### <span data-ttu-id="bcdcb-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bcdcb-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcdcb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bcdcb-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcdcb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bcdcb-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcdcb-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bcdcb-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcdcb-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="bcdcb-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcdcb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcdcb-110">DESCRIPTION</span></span>
<span data-ttu-id="bcdcb-111">Il cmdlet Remove-AzureRmNetworkWatcherConnectionMonitor rimuove il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="bcdcb-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcdcb-112">EXAMPLES</span></span>

### <span data-ttu-id="bcdcb-113">Esempio 1: rimuovere il monitor di connessione specificato</span><span class="sxs-lookup"><span data-stu-id="bcdcb-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="bcdcb-114">In questo esempio eliminiamo il monitor di connessione specificato da location e Name.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="bcdcb-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcdcb-115">PARAMETERS</span></span>

### <span data-ttu-id="bcdcb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcdcb-116">-AsJob</span></span>
<span data-ttu-id="bcdcb-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bcdcb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcdcb-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bcdcb-118">-Confirm</span></span>
<span data-ttu-id="bcdcb-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcdcb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdcb-120">-DefaultProfile</span></span>
<span data-ttu-id="bcdcb-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcdcb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcdcb-122">-InputObject</span></span>
<span data-ttu-id="bcdcb-123">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="bcdcb-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bcdcb-124">-Location</span></span>
<span data-ttu-id="bcdcb-125">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bcdcb-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcdcb-126">-Name</span></span>
<span data-ttu-id="bcdcb-127">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="bcdcb-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcdcb-128">-NetworkWatcher</span></span>
<span data-ttu-id="bcdcb-129">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="bcdcb-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bcdcb-130">-NetworkWatcherName</span></span>
<span data-ttu-id="bcdcb-131">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="bcdcb-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcdcb-132">-PassThru</span></span>
<span data-ttu-id="bcdcb-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bcdcb-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bcdcb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcdcb-134">-ResourceGroupName</span></span>
<span data-ttu-id="bcdcb-135">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bcdcb-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcdcb-136">-ResourceId</span></span>
<span data-ttu-id="bcdcb-137">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-137">Resource ID.</span></span>

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

### <span data-ttu-id="bcdcb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcdcb-138">-WhatIf</span></span>
<span data-ttu-id="bcdcb-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcdcb-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcdcb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdcb-141">CommonParameters</span></span>
<span data-ttu-id="bcdcb-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcdcb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bcdcb-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcdcb-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdcb-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcdcb-144">INPUTS</span></span>

### <span data-ttu-id="bcdcb-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcdcb-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="bcdcb-146">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="bcdcb-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="bcdcb-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcdcb-147">OUTPUTS</span></span>

### <span data-ttu-id="bcdcb-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bcdcb-148">System.Boolean</span></span>

## <span data-ttu-id="bcdcb-149">Note</span><span class="sxs-lookup"><span data-stu-id="bcdcb-149">NOTES</span></span>
<span data-ttu-id="bcdcb-150">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="bcdcb-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="bcdcb-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcdcb-151">RELATED LINKS</span></span>

[<span data-ttu-id="bcdcb-152">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcdcb-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="bcdcb-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcdcb-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="bcdcb-154">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcdcb-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="bcdcb-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bcdcb-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="bcdcb-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bcdcb-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="bcdcb-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bcdcb-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="bcdcb-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="bcdcb-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="bcdcb-159">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcdcb-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="bcdcb-160">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bcdcb-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="bcdcb-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcdcb-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="bcdcb-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcdcb-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="bcdcb-163">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcdcb-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="bcdcb-164">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcdcb-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="bcdcb-165">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bcdcb-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="bcdcb-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="bcdcb-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

