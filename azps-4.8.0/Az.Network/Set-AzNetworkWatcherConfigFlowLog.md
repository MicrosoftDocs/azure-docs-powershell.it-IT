---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: afa73cab1f0e66ecc9388b9fb2c536ca50bc609d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415428"
---
# <span data-ttu-id="71311-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="71311-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="71311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71311-102">SYNOPSIS</span></span>
<span data-ttu-id="71311-103">Configura la registrazione del flusso per una risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="71311-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="71311-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71311-104">SYNTAX</span></span>

### <span data-ttu-id="71311-105">SetFlowlogByResourceWithoutTA (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71311-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71311-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="71311-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71311-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="71311-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71311-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="71311-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71311-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="71311-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71311-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="71311-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71311-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="71311-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71311-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="71311-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71311-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="71311-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71311-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="71311-114">DESCRIPTION</span></span>
<span data-ttu-id="71311-115">LSet-AzNetworkWatcherConfigFlowLog configura la registrazione del flusso per una risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="71311-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="71311-116">Le proprietà da configurare includono: se la registrazione del flusso è abilitata o meno per la risorsa fornita, l'account di archiviazione configurato per l'invio dei log, il formato della registrazione del flusso e i criteri di conservazione per i log.</span><span class="sxs-lookup"><span data-stu-id="71311-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="71311-117">Attualmente sono supportati i gruppi di sicurezza di rete per la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="71311-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="71311-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71311-118">EXAMPLES</span></span>

### <span data-ttu-id="71311-119">Esempio 1: Configurare la registrazione del flusso per un gruppo di rete specificato</span><span class="sxs-lookup"><span data-stu-id="71311-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
```

<span data-ttu-id="71311-120">In questo esempio viene configurato lo stato della registrazione del flusso per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="71311-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="71311-121">Nella risposta è possibile vedere che per il gruppo di sicurezza NSG specificato è abilitata la registrazione del flusso, il formato predefinito e nessun set di criteri di conservazione.</span><span class="sxs-lookup"><span data-stu-id="71311-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="71311-122">Esempio 2: Configurare la registrazione del flusso per un gruppo di rete specificato e impostare la versione della registrazione del flusso su 2.</span><span class="sxs-lookup"><span data-stu-id="71311-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -FormatVersion 2

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 2
                   }
```

<span data-ttu-id="71311-123">In questo esempio viene configurata la registrazione del flusso in un gruppo di sicurezza di rete (NSG) con i log della versione 2 specificati.</span><span class="sxs-lookup"><span data-stu-id="71311-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="71311-124">Nella risposta, il gruppo di sicurezza NSG specificato ha abilitato la registrazione del flusso, il formato è impostato e non sono configurati criteri di conservazione.</span><span class="sxs-lookup"><span data-stu-id="71311-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="71311-125">Se l'area geografica non supporta la versione specificata, Network Watcher scriverà la versione supportata predefinita nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="71311-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="71311-126">Esempio 3: Configurare la registrazione di flusso e l'analisi del traffico per un NSG specificato</span><span class="sxs-lookup"><span data-stu-id="71311-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="71311-127">In questo esempio vengono configurate lo stato della registrazione del flusso e Analisi del traffico per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="71311-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="71311-128">Nella risposta, il gruppo NSG specificato include la registrazione del flusso e Analisi del traffico abilitata, il formato predefinito e nessun set di criteri di conservazione.</span><span class="sxs-lookup"><span data-stu-id="71311-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="71311-129">Esempio 4: Disabilitare Analisi del traffico per un gruppo NSG specificato con registrazione del flusso e analisi del traffico configurate</span><span class="sxs-lookup"><span data-stu-id="71311-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg
PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics:$false -Workspace $workspace

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": false,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
          "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="71311-130">In questo esempio viene disabilitata analisi del traffico per un gruppo di sicurezza di rete in cui sono configurati in precedenza la registrazione del flusso e Analisi traffico.</span><span class="sxs-lookup"><span data-stu-id="71311-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="71311-131">In risposta, il gruppo di sicurezza NSG specificato ha abilitato la registrazione del flusso, ma Analisi traffico è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="71311-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="71311-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71311-132">PARAMETERS</span></span>

### <span data-ttu-id="71311-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71311-133">-AsJob</span></span>
<span data-ttu-id="71311-134">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="71311-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71311-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71311-135">-DefaultProfile</span></span>
<span data-ttu-id="71311-136">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71311-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71311-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="71311-137">-EnableFlowLog</span></span>
<span data-ttu-id="71311-138">Contrassegno per abilitare o disabilitare la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="71311-138">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="71311-139">-EnableRetention</span></span>
<span data-ttu-id="71311-140">Contrassegno per abilitare o disabilitare la conservazione.</span><span class="sxs-lookup"><span data-stu-id="71311-140">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="71311-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="71311-142">Contrassegno per abilitare o disabilitare la conservazione.</span><span class="sxs-lookup"><span data-stu-id="71311-142">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases: EnableTA

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71311-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="71311-143">-FormatType</span></span>
<span data-ttu-id="71311-144">Tipo di formato del log di flusso.</span><span class="sxs-lookup"><span data-stu-id="71311-144">Type of flow log format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="71311-145">-FormatVersion</span></span>
<span data-ttu-id="71311-146">Versione del formato del log di flusso.</span><span class="sxs-lookup"><span data-stu-id="71311-146">Version of flow log format.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-147">-Location</span><span class="sxs-lookup"><span data-stu-id="71311-147">-Location</span></span>
<span data-ttu-id="71311-148">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="71311-148">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails, SetFlowlogByLocationWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-149">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71311-149">-NetworkWatcher</span></span>
<span data-ttu-id="71311-150">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="71311-150">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetFlowlogByResourceWithoutTA, SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="71311-151">-NetworkWatcherName</span></span>
<span data-ttu-id="71311-152">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="71311-152">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71311-153">-ResourceGroupName</span></span>
<span data-ttu-id="71311-154">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="71311-154">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="71311-155">-RetentionInDays</span></span>
<span data-ttu-id="71311-156">Numero di giorni per cui conservare i record del log di flusso.</span><span class="sxs-lookup"><span data-stu-id="71311-156">Number of days to retain flow log records.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-157">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="71311-157">-StorageAccountId</span></span>
<span data-ttu-id="71311-158">ID dell'account di archiviazione usato per archiviare il log di flusso.</span><span class="sxs-lookup"><span data-stu-id="71311-158">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="71311-159">-TargetResourceId</span></span>
<span data-ttu-id="71311-160">ID della risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="71311-160">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-161">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="71311-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="71311-162">Ottiene o imposta l'intervallo (in minuti) che definisce la frequenza con cui il servizio per l'analisi del flusso deve eseguire l'analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="71311-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71311-163">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="71311-163">-Workspace</span></span>
<span data-ttu-id="71311-164">Oggetto WS usato per archiviare i dati di analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="71311-164">The WS object which is used to store the traffic analytics data.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByResourceWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByLocationWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-165">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="71311-165">-WorkspaceGUID</span></span>
<span data-ttu-id="71311-166">GUID del sistema WS usato per archiviare i dati di analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="71311-166">GUID of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-167">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="71311-167">-WorkspaceLocation</span></span>
<span data-ttu-id="71311-168">Area geografica di Azure del sistema WS usata per archiviare i dati di analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="71311-168">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-169">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="71311-169">-WorkspaceResourceId</span></span>
<span data-ttu-id="71311-170">Abbonamento del sistema WS usato per archiviare i dati di analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="71311-170">Subscription of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71311-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71311-171">-Confirm</span></span>
<span data-ttu-id="71311-172">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71311-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71311-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71311-173">-WhatIf</span></span>
<span data-ttu-id="71311-174">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71311-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71311-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71311-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71311-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71311-176">CommonParameters</span></span>
<span data-ttu-id="71311-177">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71311-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71311-178">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71311-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71311-179">INPUT</span><span class="sxs-lookup"><span data-stu-id="71311-179">INPUTS</span></span>

### <span data-ttu-id="71311-180">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71311-180">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="71311-181">System.String</span><span class="sxs-lookup"><span data-stu-id="71311-181">System.String</span></span>

### <span data-ttu-id="71311-182">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71311-182">System.Boolean</span></span>

### <span data-ttu-id="71311-183">System.Int32</span><span class="sxs-lookup"><span data-stu-id="71311-183">System.Int32</span></span>

### <span data-ttu-id="71311-184">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="71311-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="71311-185">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="71311-185">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="71311-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71311-186">OUTPUTS</span></span>

### <span data-ttu-id="71311-187">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="71311-187">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="71311-188">NOTE</span><span class="sxs-lookup"><span data-stu-id="71311-188">NOTES</span></span>
<span data-ttu-id="71311-189">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete, watcher, flusso, log, flowlog, registrazione</span><span class="sxs-lookup"><span data-stu-id="71311-189">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="71311-190">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71311-190">RELATED LINKS</span></span>

[<span data-ttu-id="71311-191">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71311-191">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="71311-192">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71311-192">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="71311-193">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71311-193">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="71311-194">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="71311-194">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="71311-195">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="71311-195">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="71311-196">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="71311-196">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="71311-197">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="71311-197">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="71311-198">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71311-198">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71311-199">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="71311-199">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="71311-200">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71311-200">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71311-201">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71311-201">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71311-202">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71311-202">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71311-203">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="71311-203">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="71311-204">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="71311-204">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="71311-205">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="71311-205">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="71311-206">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71311-206">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="71311-207">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71311-207">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="71311-208">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71311-208">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="71311-209">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="71311-209">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="71311-210">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71311-210">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="71311-211">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71311-211">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="71311-212">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="71311-212">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="71311-213">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="71311-213">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="71311-214">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="71311-214">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="71311-215">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="71311-215">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="71311-216">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="71311-216">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="71311-217">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="71311-217">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
