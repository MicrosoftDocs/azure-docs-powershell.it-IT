---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 69ac1db81294a88f087ab036fd9bc0206a768e7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979501"
---
# <span data-ttu-id="68f22-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="68f22-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="68f22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68f22-102">SYNOPSIS</span></span>
<span data-ttu-id="68f22-103">Aggiorna risorsa log di flusso.</span><span class="sxs-lookup"><span data-stu-id="68f22-103">Updates flow log resource.</span></span>

## <span data-ttu-id="68f22-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68f22-104">SYNTAX</span></span>

### <span data-ttu-id="68f22-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68f22-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f22-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="68f22-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f22-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="68f22-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f22-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="68f22-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f22-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="68f22-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f22-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="68f22-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f22-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="68f22-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f22-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="68f22-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68f22-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="68f22-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68f22-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="68f22-114">DESCRIPTION</span></span>
<span data-ttu-id="68f22-115">Aggiorna risorsa log di flusso.</span><span class="sxs-lookup"><span data-stu-id="68f22-115">Updates flow log resource.</span></span>

## <span data-ttu-id="68f22-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68f22-116">EXAMPLES</span></span>

### <span data-ttu-id="68f22-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="68f22-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="68f22-118">Nome: ID pstest : /subscriptions/bbbbbb-bbbb-bbbb-bbbb-bbbb-bbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag: W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled : True RetentionPolicy : { "Days": 0, "Enabled": false } Format : { "Type": "JSON", "Versione": 2 } FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="68f22-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="68f22-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68f22-119">PARAMETERS</span></span>

### <span data-ttu-id="68f22-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f22-120">-DefaultProfile</span></span>
<span data-ttu-id="68f22-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68f22-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-122">-Enabled</span><span class="sxs-lookup"><span data-stu-id="68f22-122">-Enabled</span></span>
<span data-ttu-id="68f22-123">Contrassegno per abilitare o disabilitare la registrazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="68f22-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="68f22-124">-EnableRetention</span></span>
<span data-ttu-id="68f22-125">Contrassegno per abilitare o disabilitare la conservazione.</span><span class="sxs-lookup"><span data-stu-id="68f22-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="68f22-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="68f22-127">Contrassegno per abilitare/disabilitare TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="68f22-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-128">-Force</span><span class="sxs-lookup"><span data-stu-id="68f22-128">-Force</span></span>
<span data-ttu-id="68f22-129">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="68f22-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="68f22-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="68f22-130">-FormatType</span></span>
<span data-ttu-id="68f22-131">Tipo di file di log di flusso.</span><span class="sxs-lookup"><span data-stu-id="68f22-131">The file type of flow log.</span></span>
<span data-ttu-id="68f22-132">L'unico valore supportato ora è 'JSON'.</span><span class="sxs-lookup"><span data-stu-id="68f22-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="68f22-133">-FormatVersion</span></span>
<span data-ttu-id="68f22-134">Versione (revisione) del log di flusso.</span><span class="sxs-lookup"><span data-stu-id="68f22-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68f22-135">-InputObject</span></span>
<span data-ttu-id="68f22-136">Oggetto flusso lof.</span><span class="sxs-lookup"><span data-stu-id="68f22-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-137">-Location</span><span class="sxs-lookup"><span data-stu-id="68f22-137">-Location</span></span>
<span data-ttu-id="68f22-138">Posizione del network watcher.</span><span class="sxs-lookup"><span data-stu-id="68f22-138">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-139">-Name</span><span class="sxs-lookup"><span data-stu-id="68f22-139">-Name</span></span>
<span data-ttu-id="68f22-140">Nome del log di flusso.</span><span class="sxs-lookup"><span data-stu-id="68f22-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68f22-141">-NetworkWatcher</span></span>
<span data-ttu-id="68f22-142">Risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="68f22-142">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="68f22-143">-NetworkWatcherName</span></span>
<span data-ttu-id="68f22-144">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="68f22-144">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f22-145">-ResourceGroupName</span></span>
<span data-ttu-id="68f22-146">Nome del gruppo di risorse Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="68f22-146">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68f22-147">-ResourceId</span></span>
<span data-ttu-id="68f22-148">ID risorsa FlowLog.</span><span class="sxs-lookup"><span data-stu-id="68f22-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="68f22-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="68f22-150">Numero di giorni per cui conservare i record del log di flusso.</span><span class="sxs-lookup"><span data-stu-id="68f22-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="68f22-151">-StorageId</span></span>
<span data-ttu-id="68f22-152">ID dell'account di archiviazione usato per archiviare il log di flusso.</span><span class="sxs-lookup"><span data-stu-id="68f22-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="68f22-153">-Tag</span></span>
<span data-ttu-id="68f22-154">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="68f22-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="68f22-155">-TargetResourceId</span></span>
<span data-ttu-id="68f22-156">ID del gruppo di sicurezza di rete a cui verrà applicato il log di flusso.</span><span class="sxs-lookup"><span data-stu-id="68f22-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="68f22-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="68f22-158">Intervallo in minuti che stabilisce la frequenza con cui il servizio per l'analisi del flusso deve eseguire l'analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="68f22-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="68f22-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="68f22-160">ID risorsa dell'area di lavoro allegata.</span><span class="sxs-lookup"><span data-stu-id="68f22-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f22-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68f22-161">-Confirm</span></span>
<span data-ttu-id="68f22-162">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68f22-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68f22-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68f22-163">-WhatIf</span></span>
<span data-ttu-id="68f22-164">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68f22-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68f22-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68f22-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68f22-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f22-166">CommonParameters</span></span>
<span data-ttu-id="68f22-167">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68f22-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f22-168">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="68f22-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f22-169">INPUT</span><span class="sxs-lookup"><span data-stu-id="68f22-169">INPUTS</span></span>

### <span data-ttu-id="68f22-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68f22-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="68f22-171">System.String</span><span class="sxs-lookup"><span data-stu-id="68f22-171">System.String</span></span>

### <span data-ttu-id="68f22-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="68f22-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="68f22-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68f22-173">OUTPUTS</span></span>

### <span data-ttu-id="68f22-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="68f22-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="68f22-175">NOTE</span><span class="sxs-lookup"><span data-stu-id="68f22-175">NOTES</span></span>

## <span data-ttu-id="68f22-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68f22-176">RELATED LINKS</span></span>

[<span data-ttu-id="68f22-177">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68f22-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="68f22-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68f22-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="68f22-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="68f22-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="68f22-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="68f22-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="68f22-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="68f22-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="68f22-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="68f22-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="68f22-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="68f22-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="68f22-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68f22-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68f22-185">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="68f22-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="68f22-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68f22-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68f22-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68f22-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68f22-188">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="68f22-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="68f22-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="68f22-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="68f22-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="68f22-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="68f22-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="68f22-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="68f22-192">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68f22-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="68f22-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68f22-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="68f22-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68f22-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="68f22-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="68f22-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="68f22-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68f22-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="68f22-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68f22-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="68f22-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="68f22-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="68f22-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="68f22-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="68f22-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="68f22-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="68f22-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="68f22-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="68f22-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="68f22-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="68f22-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="68f22-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="68f22-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="68f22-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="68f22-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="68f22-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="68f22-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="68f22-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
