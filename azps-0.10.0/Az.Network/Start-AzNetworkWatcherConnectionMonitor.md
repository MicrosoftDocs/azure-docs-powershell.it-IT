---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 61b23db6cfc634b318aa0070b5f784ad7067a234
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862690"
---
# <span data-ttu-id="aca26-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aca26-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="aca26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aca26-102">SYNOPSIS</span></span>
<span data-ttu-id="aca26-103">Avviare un monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="aca26-103">Start a connection monitor</span></span>

## <span data-ttu-id="aca26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aca26-104">SYNTAX</span></span>

### <span data-ttu-id="aca26-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aca26-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="aca26-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="aca26-106">SetByName</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="aca26-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="aca26-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="aca26-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="aca26-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="aca26-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="aca26-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="aca26-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aca26-110">DESCRIPTION</span></span>
<span data-ttu-id="aca26-111">Il cmdlet Start-AzNetworkWatcherConnectionMonitor avvia il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="aca26-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="aca26-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aca26-112">EXAMPLES</span></span>

### <span data-ttu-id="aca26-113">---------------Esempio 1: avviare un monitor di connessione---------------</span><span class="sxs-lookup"><span data-stu-id="aca26-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="aca26-114">In questo esempio viene avviato il monitoraggio delle connessioni specificato per nome e Network Watcher</span><span class="sxs-lookup"><span data-stu-id="aca26-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="aca26-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aca26-115">PARAMETERS</span></span>

### <span data-ttu-id="aca26-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aca26-116">-AsJob</span></span>
<span data-ttu-id="aca26-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="aca26-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aca26-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aca26-118">-Confirm</span></span>
<span data-ttu-id="aca26-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aca26-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aca26-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca26-120">-DefaultProfile</span></span>
<span data-ttu-id="aca26-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aca26-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aca26-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aca26-122">-InputObject</span></span>
<span data-ttu-id="aca26-123">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="aca26-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="aca26-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="aca26-124">-Location</span></span>
<span data-ttu-id="aca26-125">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="aca26-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="aca26-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="aca26-126">-Name</span></span>
<span data-ttu-id="aca26-127">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="aca26-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="aca26-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aca26-128">-NetworkWatcher</span></span>
<span data-ttu-id="aca26-129">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="aca26-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="aca26-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="aca26-130">-NetworkWatcherName</span></span>
<span data-ttu-id="aca26-131">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="aca26-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="aca26-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aca26-132">-PassThru</span></span>
<span data-ttu-id="aca26-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="aca26-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="aca26-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aca26-134">-ResourceGroupName</span></span>
<span data-ttu-id="aca26-135">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="aca26-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="aca26-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aca26-136">-ResourceId</span></span>
<span data-ttu-id="aca26-137">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="aca26-137">Resource ID.</span></span>

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

### <span data-ttu-id="aca26-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aca26-138">-WhatIf</span></span>
<span data-ttu-id="aca26-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aca26-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aca26-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aca26-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="aca26-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aca26-141">INPUTS</span></span>

### <span data-ttu-id="aca26-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="aca26-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="aca26-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="aca26-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="aca26-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aca26-144">OUTPUTS</span></span>

### <span data-ttu-id="aca26-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aca26-145">System.Boolean</span></span>


## <span data-ttu-id="aca26-146">Note</span><span class="sxs-lookup"><span data-stu-id="aca26-146">NOTES</span></span>
<span data-ttu-id="aca26-147">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="aca26-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="aca26-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aca26-148">RELATED LINKS</span></span>
<span data-ttu-id="aca26-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="aca26-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="aca26-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="aca26-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="aca26-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="aca26-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="aca26-152">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="aca26-152">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span></span>