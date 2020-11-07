---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: f69910140f2bd7b57a30bd413c74e6f26e646787
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862677"
---
# <span data-ttu-id="51a82-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51a82-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="51a82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51a82-102">SYNOPSIS</span></span>
<span data-ttu-id="51a82-103">Arrestare un monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="51a82-103">Stop a connection monitor</span></span>

## <span data-ttu-id="51a82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51a82-104">SYNTAX</span></span>

### <span data-ttu-id="51a82-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51a82-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="51a82-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="51a82-106">SetByName</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="51a82-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="51a82-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="51a82-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="51a82-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="51a82-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="51a82-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="51a82-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51a82-110">DESCRIPTION</span></span>
<span data-ttu-id="51a82-111">Il cmdlet Stop-AzNetworkWatcherConnectionMonitor arresta il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="51a82-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="51a82-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51a82-112">EXAMPLES</span></span>

### <span data-ttu-id="51a82-113">---------------Esempio 1: arrestare un monitor di connessione---------------</span><span class="sxs-lookup"><span data-stu-id="51a82-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="51a82-114">In questo esempio interrompiamo il monitoraggio delle connessioni specificato per nome e Network Watcher</span><span class="sxs-lookup"><span data-stu-id="51a82-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="51a82-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51a82-115">PARAMETERS</span></span>

### <span data-ttu-id="51a82-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51a82-116">-AsJob</span></span>
<span data-ttu-id="51a82-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="51a82-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51a82-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="51a82-118">-Confirm</span></span>
<span data-ttu-id="51a82-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51a82-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51a82-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a82-120">-DefaultProfile</span></span>
<span data-ttu-id="51a82-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51a82-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51a82-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51a82-122">-InputObject</span></span>
<span data-ttu-id="51a82-123">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="51a82-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="51a82-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="51a82-124">-Location</span></span>
<span data-ttu-id="51a82-125">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="51a82-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="51a82-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="51a82-126">-Name</span></span>
<span data-ttu-id="51a82-127">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="51a82-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="51a82-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51a82-128">-NetworkWatcher</span></span>
<span data-ttu-id="51a82-129">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="51a82-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="51a82-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="51a82-130">-NetworkWatcherName</span></span>
<span data-ttu-id="51a82-131">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="51a82-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="51a82-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51a82-132">-PassThru</span></span>
<span data-ttu-id="51a82-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="51a82-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="51a82-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51a82-134">-ResourceGroupName</span></span>
<span data-ttu-id="51a82-135">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="51a82-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="51a82-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51a82-136">-ResourceId</span></span>
<span data-ttu-id="51a82-137">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="51a82-137">Resource ID.</span></span>

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

### <span data-ttu-id="51a82-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51a82-138">-WhatIf</span></span>
<span data-ttu-id="51a82-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51a82-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51a82-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51a82-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="51a82-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51a82-141">INPUTS</span></span>

### <span data-ttu-id="51a82-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51a82-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="51a82-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="51a82-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="51a82-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51a82-144">OUTPUTS</span></span>

### <span data-ttu-id="51a82-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51a82-145">System.Boolean</span></span>


## <span data-ttu-id="51a82-146">Note</span><span class="sxs-lookup"><span data-stu-id="51a82-146">NOTES</span></span>
<span data-ttu-id="51a82-147">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="51a82-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="51a82-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51a82-148">RELATED LINKS</span></span>
<span data-ttu-id="51a82-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="51a82-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="51a82-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="51a82-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="51a82-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="51a82-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="51a82-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="51a82-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>