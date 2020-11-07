---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: c8464183646ee9a78bad4f8f94a8e2093ad6b21d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866033"
---
# <span data-ttu-id="8e599-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e599-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="8e599-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e599-102">SYNOPSIS</span></span>
<span data-ttu-id="8e599-103">Avviare un monitor di connessione</span><span class="sxs-lookup"><span data-stu-id="8e599-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e599-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e599-104">SYNTAX</span></span>

### <span data-ttu-id="8e599-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e599-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8e599-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8e599-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8e599-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8e599-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8e599-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e599-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8e599-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8e599-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8e599-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e599-110">DESCRIPTION</span></span>
<span data-ttu-id="8e599-111">Il cmdlet Start-AzureRmNetworkWatcherConnectionMonitor avvia il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="8e599-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="8e599-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e599-112">EXAMPLES</span></span>

### <span data-ttu-id="8e599-113">---------------Esempio 1: avviare un monitor di connessione---------------</span><span class="sxs-lookup"><span data-stu-id="8e599-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="8e599-114">In questo esempio viene avviato il monitoraggio delle connessioni specificato per nome e Network Watcher</span><span class="sxs-lookup"><span data-stu-id="8e599-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="8e599-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e599-115">PARAMETERS</span></span>

### <span data-ttu-id="8e599-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e599-116">-AsJob</span></span>
<span data-ttu-id="8e599-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8e599-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e599-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8e599-118">-Confirm</span></span>
<span data-ttu-id="8e599-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e599-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e599-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e599-120">-DefaultProfile</span></span>
<span data-ttu-id="8e599-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e599-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e599-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e599-122">-InputObject</span></span>
<span data-ttu-id="8e599-123">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="8e599-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="8e599-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8e599-124">-Location</span></span>
<span data-ttu-id="8e599-125">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="8e599-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8e599-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e599-126">-Name</span></span>
<span data-ttu-id="8e599-127">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="8e599-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="8e599-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e599-128">-NetworkWatcher</span></span>
<span data-ttu-id="8e599-129">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8e599-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="8e599-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8e599-130">-NetworkWatcherName</span></span>
<span data-ttu-id="8e599-131">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8e599-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="8e599-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e599-132">-PassThru</span></span>
<span data-ttu-id="8e599-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8e599-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8e599-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e599-134">-ResourceGroupName</span></span>
<span data-ttu-id="8e599-135">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="8e599-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8e599-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e599-136">-ResourceId</span></span>
<span data-ttu-id="8e599-137">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="8e599-137">Resource ID.</span></span>

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

### <span data-ttu-id="8e599-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e599-138">-WhatIf</span></span>
<span data-ttu-id="8e599-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e599-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e599-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e599-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="8e599-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e599-141">INPUTS</span></span>

### <span data-ttu-id="8e599-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e599-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8e599-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="8e599-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="8e599-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e599-144">OUTPUTS</span></span>

### <span data-ttu-id="8e599-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e599-145">System.Boolean</span></span>


## <span data-ttu-id="8e599-146">Note</span><span class="sxs-lookup"><span data-stu-id="8e599-146">NOTES</span></span>
<span data-ttu-id="8e599-147">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="8e599-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="8e599-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e599-148">RELATED LINKS</span></span>
<span data-ttu-id="8e599-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="8e599-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="8e599-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="8e599-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="8e599-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="8e599-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="8e599-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="8e599-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
