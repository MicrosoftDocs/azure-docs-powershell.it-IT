---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 046a2ee4591eb345efd71163d27140799cb229e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866465"
---
# <span data-ttu-id="2b175-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2b175-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="2b175-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b175-102">SYNOPSIS</span></span>
<span data-ttu-id="2b175-103">Rimuovi monitoraggio connessione.</span><span class="sxs-lookup"><span data-stu-id="2b175-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b175-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b175-104">SYNTAX</span></span>

### <span data-ttu-id="2b175-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b175-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2b175-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2b175-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2b175-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2b175-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2b175-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b175-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2b175-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2b175-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2b175-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b175-110">DESCRIPTION</span></span>
<span data-ttu-id="2b175-111">Il cmdlet Remove-AzureRmNetworkWatcherConnectionMonitor rimuove il monitor di connessione specificato.</span><span class="sxs-lookup"><span data-stu-id="2b175-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="2b175-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b175-112">EXAMPLES</span></span>

### <span data-ttu-id="2b175-113">---------------Esempio 1: rimuovere il monitor di connessione specificato---------------</span><span class="sxs-lookup"><span data-stu-id="2b175-113">---------------  Example 1: Remove the specified connection monitor ---------------</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="2b175-114">In questo esempio eliminiamo il monitor di connessione specificato da location e Name.</span><span class="sxs-lookup"><span data-stu-id="2b175-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="2b175-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b175-115">PARAMETERS</span></span>

### <span data-ttu-id="2b175-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b175-116">-AsJob</span></span>
<span data-ttu-id="2b175-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2b175-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b175-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b175-118">-Confirm</span></span>
<span data-ttu-id="2b175-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b175-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b175-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b175-120">-DefaultProfile</span></span>
<span data-ttu-id="2b175-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b175-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b175-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b175-122">-InputObject</span></span>
<span data-ttu-id="2b175-123">Oggetto monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="2b175-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="2b175-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2b175-124">-Location</span></span>
<span data-ttu-id="2b175-125">Posizione del monitoraggio della rete.</span><span class="sxs-lookup"><span data-stu-id="2b175-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2b175-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b175-126">-Name</span></span>
<span data-ttu-id="2b175-127">Nome del monitor della connessione.</span><span class="sxs-lookup"><span data-stu-id="2b175-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="2b175-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b175-128">-NetworkWatcher</span></span>
<span data-ttu-id="2b175-129">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="2b175-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="2b175-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2b175-130">-NetworkWatcherName</span></span>
<span data-ttu-id="2b175-131">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="2b175-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="2b175-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b175-132">-PassThru</span></span>
<span data-ttu-id="2b175-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2b175-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2b175-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b175-134">-ResourceGroupName</span></span>
<span data-ttu-id="2b175-135">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="2b175-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2b175-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b175-136">-ResourceId</span></span>
<span data-ttu-id="2b175-137">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="2b175-137">Resource ID.</span></span>

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

### <span data-ttu-id="2b175-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b175-138">-WhatIf</span></span>
<span data-ttu-id="2b175-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b175-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b175-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b175-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="2b175-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b175-141">INPUTS</span></span>

### <span data-ttu-id="2b175-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b175-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2b175-143">System. String Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="2b175-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="2b175-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b175-144">OUTPUTS</span></span>

### <span data-ttu-id="2b175-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2b175-145">System.Boolean</span></span>


## <span data-ttu-id="2b175-146">Note</span><span class="sxs-lookup"><span data-stu-id="2b175-146">NOTES</span></span>
<span data-ttu-id="2b175-147">Parole chiave: Azure, azurerm, ARM, Resource, Connectivity, Management, Manager, Network, networking, Network Watcher, Connection Monitor</span><span class="sxs-lookup"><span data-stu-id="2b175-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="2b175-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b175-148">RELATED LINKS</span></span>
<span data-ttu-id="2b175-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="2b175-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="2b175-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="2b175-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="2b175-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="2b175-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="2b175-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="2b175-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>

